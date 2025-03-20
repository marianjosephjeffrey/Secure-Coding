# 🔐 Secure Coding for Software Engineering  

## 📌 Overview  
As part of a **secure coding course at the University of Maryland**, I developed and analyzed **web applications** with a strong focus on **secure coding practices**. This project covered **threat modeling, abuse case analysis, secure code review, and vulnerability identification** to enhance software security.  

---

## 🛠 Key Contributions  

- 🏗 **Planned, designed, and implemented a secure web-based application**, following **OWASP Secure Coding Guidelines**.  
- 🔍 **Conducted threat modeling and abuse case analysis** to identify **potential attack vectors**.  
- 🔎 **Performed a secure code review** on an existing **web-based application**, identifying **Common Weakness Enumerations (CWEs)**.  
- ⚡ **Mitigated security vulnerabilities**, applying **best practices for input validation, authentication, and access control**.  
- 🌍 **Ensured compliance with secure development frameworks**, such as **OWASP Top 10 and NIST guidelines**.  

---

## 🛠 Tools & Technologies Used  

| Category                     | Tools & Technologies |
|------------------------------|----------------------|
| 🏗 Web Development           | C#, ASP.NET MVC, React.js, JavaScript, HTML |
| 🔍 Security Testing          | Burp Suite, OWASP ZAP |
| 📜 Secure Coding Frameworks  | OWASP Top 10, NIST Guidelines |
| 🔑 Authentication & Security | JWT, OAuth, Role-Based Access Control (RBAC) |
| 🔄 Code Review & Analysis    | CWE Database, Static Code Analysis |
| 🚀 Threat Modeling           | STRIDE, Abuse Case Development |
| 🛡 Secure Input Handling     | Parameterized Queries, Input Validation |

---

## ⚙️ Sample Secure Code Implementations  

### 🔐 Implementing Secure Authentication in ASP.NET (C#)  
```csharp
public async Task<IActionResult> Login(UserLoginModel model)
{
    if (!ModelState.IsValid)
        return View(model);

    var user = await _userManager.FindByEmailAsync(model.Email);
    if (user != null && await _userManager.CheckPasswordAsync(user, model.Password))
    {
        var token = GenerateJwtToken(user);
        return Ok(new { Token = token });
    }

    return Unauthorized("Invalid credentials");
}
```
🛡 Preventing SQL Injection in C# with Parameterized Queries
```csharp
string query = "SELECT * FROM Users WHERE Username = @username";
using (SqlCommand cmd = new SqlCommand(query, connection))
{
    cmd.Parameters.AddWithValue("@username", userInput);
    SqlDataReader reader = cmd.ExecuteReader();
}
```
🔍 Secure Input Validation in React.js
```javascript
const validateInput = (input) => {
    const sanitizedInput = input.replace(/[<>]/g, ""); // Prevents XSS attacks
    return sanitizedInput;
};
```

⸻

📋 Final Report & Evaluation

The project concluded with a comprehensive report detailing:

✅ Threat modeling analysis, including STRIDE and abuse cases for secure design.
✅ Secure coding practices applied, mitigating risks from SQL Injection, XSS, and CSRF.
✅ Code review findings, identifying Common Weakness Enumerations (CWEs) and security flaws.
✅ Best practice recommendations, ensuring a resilient web application security model.
✅ Final submission and presentation, demonstrating real-world secure coding implementations.

⸻

🎤 Presentation & Impact

I compiled the findings and security improvements into a technical presentation, demonstrating how secure coding practices reduce vulnerabilities in software development.

⸻

💬 Have Questions?

Feel free to reach out or open an issue! 🚀🔐
