---
title: 'Personal Fav'
images:
    -
        title: 'Narrows at Zion National Park'
        thumbnail: pshots_Zion1.jpg
    -
        title: 'Foliage Canopy'
        thumbnail: pshots_HDR1.jpg
    -
        title: 'Spring - Cherry Blossom Festival '
        thumbnail: pshots_IMG_2024.jpg
    -
        title: 'Zion National Park'
        thumbnail: pshots_IMG_3620_blacknwhite.jpg
    -
        title: 'Sunset in Florida'
        thumbnail: pshots_IMG_4547.jpg
    -
        title: 'Little Humans'
        thumbnail: pshots_IMG_5780.jpg
    -
        title: 'Niagara Falls'
        thumbnail: pshots_IMG_6653.jpg
    -
        title: 'Aqua beast - Pittsburgh Zoo'
        thumbnail: pshots_IMG_7067.jpg
form:
    action: /home
    name: contact-form
    fields:
        -
            name: name
            label: Name
            placeholder: Name
            type: text
            validate:
                required: true
        -
            name: email
            label: Email
            placeholder: Email
            type: email
            validate:
                required: true
        -
            name: message
            label: Message
            placeholder: Message
            type: textarea
            rows: 4
            validate:
                required: true
    buttons:
        -
            type: submit
            value: Send
            classes: special
        -
            type: reset
            value: Reset
    process:
        -
            email:
                from: '{{ config.plugins.email.from }}'
                to: ['{{ config.plugins.email.from }}']
                subject: '[Contact] Message from {{ form.value.name|e }}'
                body: '{% include ''forms/data.html.twig'' %}'
        -
            save:
                fileprefix: contact-
                dateformat: Ymd-His-u
                extension: txt
                body: '{% include ''forms/data.txt.twig'' %}'
        -
            display: thank-you
---

![](pshots_IMG_4547.jpg)![](pshots_IMG_3620_blacknwhite.jpg)