# html_advanced


- [form](#form)
- [Variable Scope](#variable-scope)

## Form

   表单是web应用中非常重要的一个元素，用户和页面的交换大部分是在表单中完成的， 而客户端和服务器端的大部分交互也是
通过用户单击表单中的按钮来完成的。


1. several useful attribute

(1) action attribute

    The action attribute defines the action to be performed when the form is submitted.

Normally, the form data is sent to a web page on the server when the user clicks on the submit button.

In the example above, the form data is sent to a page on the server called "/action_page.php". 

This page contains a server-side script that handles the form data:

<form action="/action_page.php">
If the action attribute is omitted, the action is set to the current page.


(2) method (post or get)

get: 
    The default method when submitting form data is GET. However, when GET is used, the submitted form data will be visible in the page address field:

Appends form-data into the URL in name/value pairs. The length of a URL is limited (about 3000 characters)

Never use GET to send sensitive data! (will be visible in the URL) ;Useful for form submissions where a user want to bookmark the result

GET is better for non-secure data, like query strings in Google

post: 
    Always use POST if the form data contains sensitive or personal information. The POST method does not display the submitted form data in the page address field.
    
POST has no size limitations, and can be used to send large amounts of data.Form submissions with POST cannot be bookmarked
