<!doctype html>
<html>
    <head>
        <link href="https://fonts.googleapis.com/css?family=Noto+Sans+Devanagari" rel="stylesheet"/>
        <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
        <title>{{ title }}</title>

        <style>
            html {
                font-family: 'Noto Sans Devanagari';
            }
            .note, .video{
                text-align: center;
                font-size: 20px;
            }
            .topic_button{
              background-color: #777;
              color: white;
              cursor: pointer;
              padding: 18px;
              width: 100%;
              border: none;
              text-align: center;
              outline: none;
              font-size: 35px;
            }

            .active, .topic_button:hover {
              background-color: #555;
            }

            @media print {
                .topic_content {
                    display: block;
                }
            }

            @media not print {
                .topic_content {
                    display: none;
                }
            }

            p{page-break-inside: avoid ;}

            .topic_content {
              padding: 0 18px;
              overflow: hidden;
              text-align:center;
              background-color: #f1f1f1;
            }
        </style>
    </head>
    <body>
        <h1 id="batch" style="text-align:center;font-size:50px;color:Red">
            {{ batch }}
        </h1>
        <p id="info" style="text-align:center;font-size:25px;color:Blue">
        Links grabber made by <a href="https://t.me/arrowazaad" rel="noopener noreferrer" target="_blank">ARROW AZAAD</a>
        <br>
        <br>
        </p>
        {% if type == "notes" %}
            <div id="notes" class="files">
                {% for note in notes %}
                    <p class="note">
                    <span class="note_name">{{note}}</span>
                    <br>
                    <a href="{{ notes[note] }}" rel="noopener noreferrer" target="_blank">{{ notes[note] }}</a>
                    <br>
                    <br>
