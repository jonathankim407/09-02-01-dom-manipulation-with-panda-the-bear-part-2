Hacking Panda the Bear's Resume

1. Select the element that contains the profile image (hint: look for the class). Change the src attribute so it points to a picture of your choosing instead.

profile = document.querySelector('.profile-image')
profile.src = "images/clouds-man.jpg"

1b. Use the same approach to select the element that contains the photo of the sky and change the src attribute to another picture URL of your choosing.

sky = document.querySelector('#left-image.portfolio-image img')
sky.src = "images/pikachu-drawing.jpg"

2. Select the heading that says "Panda the Bear" and change it to your own name.

heading = document.querySelector('h1.highlight')
heading.innerText = 'Jonathan Kim'

3. Select the heading that says "Employment" and change it to something else. (hint: use a descendant selector)

employment = document.querySelector('#employment h3.info-title')
employment.innerText = 'Funemployment'

4. Change the colour of the body.

body = document.querySelector('body')
body.style.backgroundColor = 'red'

5. Change the colour used by the highlight class.

highlight = document.querySelectorAll('.highlight')
highlight.forEach(function(item) {item.style.color = 'blue'})

6. Change the font family of the h1 to 'monospace'.

heading = document.querySelectorAll('h1')
heading.forEach(function(item) {item.style.fontFamily = 'monospace'})

7. Find a way to select the round icons in the sidebar and then change their colour.

icon = document.querySelectorAll('a.action-icon-bg')
icon.forEach(function(item) {item.style.backgroundColor = 'red'})

8. Scroll down to the contact form. Change the placeholder attribute of the name field to "identify yourself".

nameField = document.querySelector('input#name.contact-info')
nameField.placeholder = 'Identify yourself'

9. Change the placeholder attribute of the message field to "state your business".

messageField = document.querySelector('textarea#message')
messageField.placeholder = 'State your business'

10. Give the name field a "value" attribute of "your nemesis".

nameField = document.querySelector('input#name.contact-info')
nameField.value = 'Your nemesis'

11. Change the value attribute of the email field to "koalathebear@gmail.com".

emailField = document.querySelector('input#email.contact-info')
emailField.value = 'koalathebear@gmail.com'

12. Change the value of the submit button on the contact form to "En garde!".

submitButton = document.querySelector('input#submit')
submitButton.value = 'En garde!'

13. We should stop Koala from sending an email to Panda that they might regret! Find a way to disable the submit button (hint: familiarize yourself with the disabled attribute).

submitButton = document.querySelector('input#submit')
submitButton.disabled = true

14. We should help Panda protect their privacy by clearing their personal details from the sidebar. You can use reset() to do this.

privacy = document.querySelector('form')
privacy.reset()

PART 2

Removing Elements from the DOM
1. Panda the Bear is lying about their skills! Take the "time travel" skill off the page to satisfy your personal sense of justice. We'll remove it by accessing the parentElement of the Panda skill and using remove().

skills = document.querySelectorAll('.bar-default')[2]
timeTravel = document.querySelector('#time-travel')
skills.removeChild(timeTravel)
