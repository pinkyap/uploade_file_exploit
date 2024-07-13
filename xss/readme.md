
https://blog.isec.pl/injection-points-in-popular-image-formats/

u can use exiftoool 

# My Markdown File

This is a paragraph of text.

**Bold Text**

*Italic Text*

brutelogic.com.br/poc.svg

dhundene se ahca h ki payloade banana sik


so hum SVG 
SVG (Scalable Vector Graphics) file format allows for the inclusion of XML-based scripting, including JavaScript, which can indeed lead to XSS (Cross-Site Scripting) vulnerabilities.
 
wht about png formate ?
PNG images does not directly execute JavaScript code in web browsers.

No, you cannot directly embed JavaScript code within a PNG image file to execute it in a web browser. Unlike SVG files, PNG files are not designed to support scripting or interactive content. PNG is a raster image format, which means it represents images as a grid of pixels, without any inherent support for scripting or interactivity.
While you can embed metadata within a PNG file using tools like ExifTool, this metadata is typically used for storing information about the image itself (such as camera settings, author information, etc.) and is not executed by web browsers.
Therefore, attempting to embed JavaScript code within a PNG file's metadata would not result in the code being executed by a web browser when the image is opened. Browsers generally do not interpret or execute JavaScript code embedded in image files for security reasons.

( png ke through possoible h ,web application me  jub uploade krete time png ka content data check na ho tab a.png file name h but iska content svg wala hi h tub jake png ke though xss ho araha h  )

In this scenario, the JavaScript embedded in the PNG image is not executed directly by the browser when the image is viewed. Instead, it's executed in the context of the web application's HTML page where the image is displayed. This is why it's categorized as XSS.

 xss though png 
 https://hackerone.com/reports/964550
 https://hackerone.com/reports/880099
 
You've raised a crucial point regarding how vulnerabilities in web applications can lead to security risks like XSS (Cross-Site Scripting) when attackers upload PNG images with embedded scripts. Let me clarify how this works:

1. **File Upload Vulnerabilities**: In some web applications, there might be flaws in the file upload functionality. These flaws could allow attackers to upload files with unintended content, including PNG images containing embedded JavaScript code.

2. **Bypassing File Type Validation**: Many web applications perform basic file type validation by checking the file extension or MIME type. However, these checks can be bypassed by renaming the file extension or manipulating the file headers to make the server think it's receiving a different type of file.

3. **Stored XSS**: When the uploaded PNG image containing JavaScript code is stored on the server and later served to other users, it becomes a vector for a stored XSS attack. When a victim accesses a page that includes the uploaded image, their browser will execute the embedded JavaScript code, leading to XSS.

4. **Execution Context**: In this scenario, the JavaScript embedded in the PNG image is not executed directly by the browser when the image is viewed. Instead, it's executed in the context of the web application's HTML page where the image is displayed. This is why it's categorized as XSS.

5. **Impact**: Depending on the nature of the vulnerability and the security context of the web application, the impact of such an attack can vary. It could range from stealing session cookies to performing actions on behalf of the user, such as sending requests to the server, accessing sensitive data, or even spreading malware.

In summary, while PNG images themselves do not execute JavaScript code in web browsers, vulnerabilities in web applications that allow the upload and serving of arbitrary files can lead to scenarios where PNG images with embedded scripts can be used to exploit XSS vulnerabilities. This underscores the importance of robust input validation, proper sanitization, and secure coding practices in web application development to mitigate such risks.


 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
 
