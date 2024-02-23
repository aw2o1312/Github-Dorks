**JavaScript (Node.js)**

> XSS (Reflected and Stored)

    /\bres.send\(\s*.*\breq.query\b/

    /\bres.send\(\s*.*\breq.body\b/

    /\bdocument\.write\(\s*.*\blocation\.search\b/


> NoSQL Injection (MongoDB with Node.js)

    /\.find\(\s*.*\breq\.body\b/

    /\.find\(\s*.*\breq\.query\b/

> Remote Code Execution (RCE)

    /\beval\(\s*.*\breq\.body\b/

    /\beval\(\s*.*\breq\.query\b/

**Python (Django/Flask)**

> XSS (Template Injection)    

    /{{\s*.*\brequest\.GET\b/

    /{{\s*.*\brequest\.form\b/

> SQL Injection

    /\bexecute\(\s*.*\brequest\.form\b/

    /\bexecute\(\s*.*\brequest\.args\b/

> Command Injection

    /subprocess\.call\(\s*.*\brequest\.form\b/

    /os\.system\(\s*.*\brequest\.form\b/

**Java (Spring Framework)**

> XSS (Spring MVC)

    /\bModelAndView.addObject\(\s*.*\bHttpServletRequest.getParameter\b/

> SQL Injection (JDBC)  

    /\.executeQuery\(\s*.*\brequest\.getParameter\b/

> Command Injection

    /Runtime\.getRuntime\(\)\.exec\(\s*.*\brequest\.getParameter\b/

**General**
> File Upload Vulnerabilities

    /\bmove_uploaded_file\(\s*.*\b$_FILES\b/` (PHP)



    /\.save\(\s*.*\brequest\.files\b/` (Python Flask)



    /MultipartFile\.transferTo\(\s*.*\brequest\.getParameter\b/` (Java Spring)

> Insecure Direct Object References (IDOR)

    /\.findById\(\s*.*\breq\.params\b/` (Node.js)



    /\.get\(\s*.*\brequest\.GET\b/` (Python Django)
