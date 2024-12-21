<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Proposal</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f0f8ff;
        }
        .container {
            margin: 50px auto;
            max-width: 600px;
        }
        .image-note {
            margin: 20px auto;
            display: none;
            text-align: center;
        }
        .image-note img {
            width: 100%;
            max-width: 400px;
            border-radius: 10px;
        }
        .image-note p {
            margin: 15px 0;
            font-size: 18px;
            color: #555;
        }
        #final-message {
            display: none;
            font-size: 28px;
            font-weight: bold;
            color: red;
            margin-top: 30px;
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Image Notes -->
        <div class="image-note" id="note1">
            <img src="file-5faK7KgQ4XT1B6LP8Q7bKR" alt="Picture 1">
            <p>তোমার হাসিটা আমার সবচেয়ে প্রিয়।</p>
        </div>
        <div class="image-note" id="note2">
            <img src="file-VVMf7VccXGbtgir9v8jEGc" alt="Picture 2">
            <p>এই মুহূর্তগুলো তোমার সাথে কাটাতে পেরে আমি ধন্য।</p>
        </div>
        <div class="image-note" id="note3">
            <img src="file-JGXXm4fXjBVaQaqpe4ZtH7" alt="Picture 3">
            <p>তুমি ছাড়া আমি অসম্পূর্ণ।</p>
        </div>

        <!-- Final Message -->
        <div id="final-message">আমি তোমাকে ভালোবাসি!</div>
    </div>

    <script>
        // JavaScript to handle interactions
        const notes = document.querySelectorAll('.image-note');
        const finalMessage = document.getElementById('final-message');
        let currentNote = 0;

        // Show the first note
        showNextNote();

        // Function to show the next note
        function showNextNote() {
            if (currentNote < notes.length) {
                notes[currentNote].style.display = 'block';
                notes[currentNote].addEventListener('click', () => {
                    notes[currentNote].style.display = 'none';
                    currentNote++;
                    showNextNote();
                });
            } else {
                finalMessage.style.display = 'block';
            }
        }
    </script>
</body>
</html>
