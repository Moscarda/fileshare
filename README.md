
<!doctype html>
<html lang="en-us">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1">
    <link rel="shortcut icon" href="https://gitlab.com/assets/favicon-075eba76312e8421991a0c1f89a89ee81678bcde72319dd3e8047e2a47cd3a42.ico" type="image/ico">

    <title>share.riseup.net</title>

    <style>
	.preview .hljs::selection, .preview .hljs span::selection {
		background-color: powderblue;
	}
	.preview .hljs::-moz-selection, .preview .hljs span::-moz-selection {
		background-color: powderblue;
	}
	
        body, html {
            height: 100%;
            margin: 0;
            padding: 0;
            font-family: Sans-Serif;
            overflow: auto;
        }

        body {
            background-color: #1f1f1f;
        }

        .contentarea h1 {
            margin: 0;
        }

        .contentarea .boxarea {
            text-align: center;
            vertical-align: middle;
            display: table-cell;
            background: #474848;
        }

        .contentarea {
            color: white;
            margin: 0;
            text-align: center;
            vertical-align: middle;
        }

        .boxarea {
            -webkit-transition: background-color 400ms ease-out;
            -moz-transition: background-color 400ms ease-out;
            -o-transition: background-color 400ms ease-out;
            -ms-transition: background-color 400ms ease-out;
            transition: background-color 400ms ease-out;
        }

        .noscript {
            color: white;
            text-align: center;
            vertical-align: middle;
            margin: 0;
        }

            #pastearea:hover {
                background-color: #474848;
                -webkit-transition: background-color 100ms ease-in;
                -moz-transition: background-color 100ms ease-in;
                -o-transition: background-color 100ms ease-in;
                -ms-transition: background-color 100ms ease-in;
                transition: background-color 100ms ease-in;
            }

        .contentarea {
            width: 200px;
            height: 200px;
            position: absolute;
            top: 0;
            bottom: 0;
            left: 0;
            right: 0;
            margin: auto;
            border: 2px solid white;
        }

        #pastearea {
            cursor: pointer;
        }

            #pastearea.dragover {
                background-color: rgba(255, 255, 255, .2);
            }

        .footer {
            position: fixed;
            bottom: 0px;
	    padding: 10px;
            background: #000;
            color: #fff;
            margin: auto;
            text-align: center;
            width: 100%;
        }

            .footer a {
                color: #474848;
                opacity: 1;
                font-size: 14px;
                text-decoration: none;
            }

        #progressamountbg {
            position: absolute;
            top: 0;
            left: 0;
            background-color: rgba(0, 10, 0, .5);
            width: 0;
            height: 100%;
            z-index: -1;
        }

        #finallink {
            color: white;
        }


        #module_download, #downloaddetails {
            width: 100%;
            height: 100%;
            position: absolute;
            top: 0;
        }

            #module_download .preview {
                max-width: 100%;
                max-height: 100%;
            }

        #previewimg img {
            display: block;
            margin: 0 auto;
        }

            #previewimg img:not(.dragged) {
                max-width: 100vw;
                max-height: 100vh;
            }

        #module_download .preview {
            display: block;
            margin: 0 auto;
        }


        audio.preview, video.preview, .downloadexplain, #downloadprogress, #previewimg {
            position: relative;
            top: 50%;
            text-align: center;
            -webkit-transform: translateY(-50%);
            transform: translateY(-50%);
            margin: 0 auto;
        }

        .downloadexplain {
            color: #fff;
            font-size: 30px;
        }

        body {
            overflow: auto;
        }

        #pastecatcher {
            position: absolute;
            top: 0;
            left: 0;
            width: 0;
            height: 0;
            opacity: 0;
            overflow: hidden;
        }

        .previewtext {
            position: absolute;
            top: 55px;
            width: 100%;
            height: calc(100% - 110px);
            overflow: auto;
	    background: #000;
        }

            .previewtext pre {
                margin: 14px 0 0;
                margin-left: 50px;
            }

            .previewtext code {
                background: none;
                margin: 0;
		overflow: visible;
		position: relative;
            }

            .previewtext > textarea {
		border: 1px solid #222;
                background: transparent none repeat scroll 0% 0%;
                padding: 10px;
                position: absolute;
	        top: 7px;
                left: 50px;
                font-family: monospace;
                outline: medium none;
                resize: none;
                font-family: monospace !important;
                font-size: 13px;
                color: #c5c8c6 !important;
                width: calc(100% - 100px);
                height: calc(100% - 40px);
                box-sizing: border-box;
                color: white;
            }

        .hidden {
            display: none !important;
        }

        .topbar {
          position: fixed;
          z-index: 1;
          width: 100%;
          height: 40px;
          padding: 5px;
          box-sizing: border-box;
          display: -webkit-flex;
          display: flex;
        }

        #downloaded_filename {
            padding: 5px;
            background-color: rgba(0, 0, 0, .5);
            border-radius: 5px;
            margin: 0;
            color: white;
            height: 40px;
            opacity: .75;
            overflow: hidden;
            text-overflow: ellipsis;
            display: block;
            vertical-align: middle;
            text-align: middle;
            z-index: 1;
            line-height: 30px;
            box-sizing: border-box;
            white-space: nowrap;
            overflow: hidden;
        }

        #create_filename {
            position: fixed;
            font-size: 16px;
            top: 10px;
            left: 10px;
            padding: 5px;
            background-color: rgba(0, 0, 0, .5);
            border-bottom-right-radius: initial;
            border: 1px solid white;
            margin: 0;
            width: 170px;
            color: white;
            opacity: .75;
            z-index: 1;
            max-width: 100%;
            box-sizing: border-box;
            white-space: nowrap;
            overflow: hidden;
        }

        #btnarea {
            position: fixed;
            bottom: 5px;
        }

        .viewswitcher {
            margin-left: auto;
            vertical-align: top;
            white-space: nowrap;
            display: -webkit-flex;
            display: flex;
            -webkit-flex-shrink: 0;
            flex-shrink: 0;
        }

        #btnarea {
            z-index: 1;
        }

        .btn {
            display: inline-block;
            height: 40px;
            margin: 0;
            -webkit-box-align: start;
            font: inherit;
            padding: 10px;
            font-size: 16px;
            border: 2px solid white;
            cursor: pointer;
            color: white !important;
            text-decoration: none;
            line-height: 16px;
            text-align: center;
            vertical-align: middle;
            opacity: 1;
	    font-weight: bold;
            background-color: #474848;
            box-sizing: border-box;
            white-space: nowrap;
            transition: all 400ms ease-out;
            margin-left: 5px;
        }


        #downloadprogress {
            color: white;
        }

        .btn:hover {
            opacity: 1;
            background-color: #474848;
            transition: all 100ms ease-in;
        }

        #linenos, #create_linenos {
            color: #7d7d7d;
            position: absolute;
            top: 20px;
            font-family: monospace;
            left: 5px;
            float: left;
            z-index: 0;
            text-align: right;
            width: 30px;
            overflow: hidden;
        }

        .dragresize.dragging {
            cursor: nwse-resize;
        }
        .viewcontent {
            width: 100%;
            height: 100%;
        }
        .loadingtext {
            color: white;
            text-align: center;
        }

        #uploadview .centerview {
            display: table;
            width: 100%;
            height: 100%;
        }
        span.notice { font-size: 0.8em; }
    </style>

    <script src="https://share.riseup.net/js/main.js"></script>
    <script>
        window.onunload = function () {}
    </script>
    <link rel="stylesheet" href="https://share.riseup.net/deps/hybrid.min.css">
    <script src="https://share.riseup.net/deps/highlight.min.js"></script>

</head>
<body>
    <div class="modulecontent modulearea"></div>

    <noscript class="noscript">
            <h2>
                    Javascript is required to view and upload files.
            </h2>
    </noscript>

    <div id="footer" class="footer">
        <a href="https://github.com/Upload/Up1" target="_blank">Up1</a>
        <span class="notice">Upload is currently limited to 50mb and files are stored no longer than a week!</span>
    </div>
</body>
</html>
