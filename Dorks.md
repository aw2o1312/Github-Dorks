JavaScript (Node.js)
XSS (Reflected and Stored)

    regex

/\bres.send\(\s*.*\breq.query\b/

regex

/\bres.send\(\s*.*\breq.body\b/

regex

    /\bdocument\.write\(\s*.*\blocation\.search\b/

NoSQL Injection (MongoDB with Node.js)

    regex

/\.find\(\s*.*\breq\.body\b/

regex

    /\.find\(\s*.*\breq\.query\b/

Remote Code Execution (RCE)

    regex

/\beval\(\s*.*\breq\.body\b/

regex

    /\beval\(\s*.*\breq\.query\b/

Python (Django/Flask)
XSS (Template Injection)

    regex

/{{\s*.*\brequest\.GET\b/

regex

    /{{\s*.*\brequest\.form\b/

SQL Injection

    regex

/\bexecute\(\s*.*\brequest\.form\b/

regex

    /\bexecute\(\s*.*\brequest\.args\b/

Command Injection

    regex

/subprocess\.call\(\s*.*\brequest\.form\b/

regex

    /os\.system\(\s*.*\brequest\.form\b/

Java (Spring Framework)
XSS (Spring MVC)

    regex

    /\bModelAndView.addObject\(\s*.*\bHttpServletRequest.getParameter\b/

SQL Injection (JDBC)

    regex

    /\.executeQuery\(\s*.*\brequest\.getParameter\b/

Command Injection

    regex

    /Runtime\.getRuntime\(\)\.exec\(\s*.*\brequest\.getParameter\b/

General
File Upload Vulnerabilities

    regex

/\bmove_uploaded_file\(\s*.*\b$_FILES\b/` (PHP)

regex

/\.save\(\s*.*\brequest\.files\b/` (Python Flask)

regex

    /MultipartFile\.transferTo\(\s*.*\brequest\.getParameter\b/` (Java Spring)

Insecure Direct Object References (IDOR)

    regex

/\.findById\(\s*.*\breq\.params\b/` (Node.js)

regex

/\.get\(\s*.*\brequest\.GET\b/` (Python Django)
