<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Helpdesk Support - XYZ Company</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        .container {
            width: 90%;
            max-width: 600px;
            margin: auto;
            background: white;
            padding: 20px;
            border-radius: 5px;
            box-shadow: 0px 0px 10px #ccc;
            margin-top: 20px;
        }
        h2 {
            text-align: center;
        }
        input, textarea {
            width: 100%;
            padding: 10px;
            margin: 10px 0;
            border: 1px solid #ccc;
            border-radius: 5px;
            box-sizing: border-box;
        }
        button {
            background: #28a745;
            color: white;
            padding: 10px;
            border: none;
            width: 100%;
            border-radius: 5px;
            cursor: pointer;
        }
        button:hover {
            background: #218838;
        }
        .faq {
            margin-top: 20px;
        }
        .faq h3 {
            cursor: pointer;
            background: #007bff;
            color: white;
            padding: 10px;
            margin: 5px 0;
            border-radius: 5px;
        }
        .faq p {
            display: none;
            padding: 10px;
            background: #e9ecef;
            border-radius: 5px;
        }
        @media (max-width: 768px) {
            .container {
                width: 95%;
                padding: 15px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Helpdesk Support - XYZ Company</h2>
        <form id="helpdesk-form">
            <input type="text" id="name" placeholder="Your Name" required>
            <input type="email" id="email" placeholder="Your Email" required>
            <textarea id="message" placeholder="Describe your issue..." rows="5" required></textarea>
            <button type="submit">Submit</button>
        </form>
        <div class="faq">
            <h3>What services do you offer?</h3>
            <p>We provide technical support, troubleshooting, and general assistance for our products.</p>
            <h3>How can I reset my password?</h3>
            <p>You can reset your password by clicking the "Forgot Password" link on the login page.</p>
            <h3>How do I contact support?</h3>
            <p>You can fill out the form above or call our 24/7 support hotline.</p>
        </div>
    </div>
    <script>
        document.getElementById('helpdesk-form').addEventListener('submit', function(event) {
            event.preventDefault();
            alert('Your request has been submitted. Our support team will contact you soon.');
            document.getElementById('helpdesk-form').reset();
        });
        
        document.querySelectorAll('.faq h3').forEach(question => {
            question.addEventListener('click', () => {
                let answer = question.nextElementSibling;
                answer.style.display = answer.style.display === 'block' ? 'none' : 'block';
            });
        });
    </script>
</body>
</html>
