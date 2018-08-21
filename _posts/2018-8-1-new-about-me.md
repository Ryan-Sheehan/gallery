---
layout: post
title: "About me cont."
description: "Your message has been delivered"
tags: [web design]
---

Although I like how succinct the 'about me' section of my personal site's home page is, I wanted something more comprehensive that could also be 1) more in-depth than the verbose tweet I currently had, and 2) interactive. For this project I wanted to recreate a screen that felt as if someone were texting me via Apple's iMessage. I figured this was a natural environment to get to know someone in an online context and I liked the idea of being able to recreate that in a new domain.

The trickiest part of the CSS was managing the little tail on each of the messages, as well as knowing the only put that tail on the final message sent.

```
form.chat .myMessage:before {
  ... 
  border-right: 20px solid #000;
  border-bottom-left-radius: 16px 14px;
  -webkit-transform: translate(0, -2px);
  transform: translate(0, -2px);
  border-bottom-left-radius: 15px 0px\9;
  transform: translate(-1px, -2px)\9;
}

form.chat .myMessage:after {
  ...
  border-bottom-left-radius: 10px;
  -webkit-transform: translate(-30px, -2px);
  transform: translate(-30px, -2px);
}
```

Now that I had that in place, I just needed to lay out the messages as if they were on a phone screen.

{% include image.html path="aboutme/001.png" path-detail="aboutme/001.png" alt="" %}

With that done, I then abstracted the html layout of the phone screen into a javascript method that would automatically generate a message when provided the Element to attach this message to, the Sender, the Origin, the Date, and the Message.

```javascript

function responsiveChatPush(element, sender, origin, date, message) {
    var originClass;
    if (origin == 'me') {
        originClass = 'myMessage';
    } else {
        originClass = 'fromThem';
    }
    $(element + ' .messages').append('<div class="message"><div class="' + originClass + '"><p>' + message + '</p><date><b>' + sender + '</b> ' + date + '</date></div></div>');
}
```

You can see the live version of it now [here](http://ryanwsheehan.com/about/).
