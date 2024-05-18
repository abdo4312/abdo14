<!DOCTYPE html>
<html lang="ar">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>تفانينو</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header class="header">
        <h1>تفانينو</h1>
        <nav>
            <ul>
                <li><a href="#section1">القسم 1</a></li>
                <li><a href="#section2">القسم 2</a></li>
                <li><a href="#section3">القسم 3</a></li>
            </ul>
        </nav>
    </header>
    
    <section id="section1" class="section">
        <h2>القسم 1</h2>
        <p>محتوى القسم الأول...</p>
    </section>
    
    <section id="section2" class="section">
        <h2>القسم 2</h2>
        <p>محتوى القسم الثاني...</p>
    </section>
    
    <section id="section3" class="section">
        <h2>القسم 3</h2>
        <p>محتوى القسم الثالث...</p>
    </section>
    
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script src="scripts.js"></script>
</body>
</html>
body {
    background-color: #f0f0f0; /* خلفية الموقع */
    color: #333; /* لون النص */
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

.header {
    background-color: #3b5998; /* لون الهيدر */
    color: #fff; /* لون نص الهيدر */
    padding: 20px;
    text-align: center;
}

.header nav ul {
    list-style-type: none;
    padding: 0;
}

.header nav ul li {
    display: inline;
    margin: 0 10px;
}

.header nav ul li a {
    color: #fff;
    text-decoration: none;
    font-size: 18px;
}

.section {
    padding: 20px;
    margin: 10px 0;
    background-color: #fff;
    border: 1px solid #ddd;
}

.section h2 {
    color: #3b5998; /* لون عناوين الأقسام */
}
$(document).ready(function(){
    $('a[href^="#"]').on('click', function(event) {
        var target = $(this.getAttribute('href'));
        if( target.length ) {
            event.preventDefault();
            $('html, body').stop().animate({
                scrollTop: target.offset().top
            }, 1000);
        }
    });
});
