# landingpage
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Landing Page</title>
    <link rel="StyleSheet" href="./css/style.css">

    <script src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.1/jquery.min.js"></script>

</head>

<body>
    <header>
        <h1>MySite</h1>
        <h3>Slogan go here...</h3>
    </header>
    <nav>
        <ul>
            <li><a data-section="home">Home</a></li>
            <li><a data-section="services">Services</a></li>
            <li class="dropdown">
                <a href="javascript:void(0)" class="dropbtn">Products</a>
                <div class="dropdown-content">
                    <a data-section="link1">Link 1</a>
                    <a data-section="link2">Link 2</a>
                    <a data-section="link3">Link 3</a>
                </div>
            </li>
            <li style="float:right"><a data-section="about">About us</a></li>
        </ul>
    </nav>

    <section id="home" class="hideable-section">
        <div>Home content</div>
    </section>

    <section id="services" class="hideable-section">
        <div>Services content</div>
    </section>

    <section id="about" class="hideable-section">
        <div>About content</div>
    </section>

    <section id="link1" class="hideable-section">
        <div>Link1 content</div>
    </section>

    <section id="link2" class="hideable-section">
        <div>Link2 content</div>
    </section>

    <section id="link3" class="hideable-section">
        <div>Link3 content</div>
    </section>

    <script>
        $(function() {
            $('nav ul li a').click(function() {
                // Lấy section để hiển thị
                var $section = $('#' + $(this).data('section'));

                // Nếu đang hiện thì không làm gì.
                // Nếu không, ẩn tất cả các se cho hiện (kiểu fade in) phần mong muốn.
                if (!$section.is(':visible')) {
                    $('.hideable-section').hide();
                    $section.fadeIn();
                }
            });
        });
    </script>
</body>

</html>
* {
    margin: 0;
    box-sizing: border-box;
    color: #666;
}


/* Header/logo tiêu đề */

header {
    padding: 5px;
    text-align: center;
    background: #1abc9c;
    color: white;
    height: 120px;
}


/* Tăng kích thước font chữ cho header */

header h1 {
    font-size: 40px;
}

header h1,
h2,
h3 {
    color: white;
}

section {
    padding: 20px;
}

ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    overflow: hidden;
    border: 1px solid #e7e7e7;
    background-color: #f3f3f3;
}

li {
    float: left;
}

li a,
.dropbtn {
    display: inline-block;
    color: #666;
    text-align: center;
    padding: 14px 16px;
    text-decoration: none;
}

li a:hover:not(.active),
.dropdown:hover .dropbtn {
    color: white;
    background-color: #4CAF50;
}

li.dropdown {
    display: inline-block;
}

.dropdown-content {
    display: none;
    position: absolute;
    background-color: #f9f9f9;
    min-width: 160px;
    box-shadow: 0px 8px 16px 0px rgba(0, 0, 0, 0.2);
    z-index: 1;
}

.dropdown-content a {
    color: #666;
    padding: 12px 16px;
    text-decoration: none;
    display: block;
    text-align: left;
}

.dropdown-content a:hover {
    background-color: #f1f1f1;
}

.dropdown:hover .dropdown-content {
    display: block;
}


/* Landing page */

.hideable-section {
    display: none;
}

.hideable-section:first-of-type {
    display: block;
}
# Miscellaneous
*.class
*.log
*.pyc
*.swp
.DS_Store
.atom/
.buildlog/
.history
.svn/

# IntelliJ related
*.iml
*.ipr
*.iws
.idea/

# The .vscode folder contains launch configuration and tasks you configure in
# VS Code which you may wish to be included in version control, so this line
# is commented out by default.
#.vscode/

# Flutter/Dart/Pub related
**/doc/api/
.dart_tool/
.flutter-plugins
.flutter-plugins-dependencies
.packages
.pub-cache/
.pub/
/build/

# Web related
lib/generated_plugin_registrant.dart

# Symbolication related
app.*.symbols

# Obfuscation related
app.*.map.json

# Exceptions to above rules.
!/packages/flutter_tools/test/data/dart_dependencies_test/**/.packages
