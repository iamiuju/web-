<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
    <style>
        * {
            padding: 0;
            margin: 0;
            box-sizing: content-box;
        }

        body {
            width: 100%;
            height: 100%;
            overflow: hidden;
        }

        .wrap {
            width: 100%;
            height: 100%;
        }

        .show-box {
            position: fixed;
            width: 100%;
            height: 70%;
        }

        .barrage-box {
            position: fixed;
            left: 0;
            bottom: 0;
            width: 100%;
            height: 30%;
            z-index: 1;
            background-color: rgba(0, 0, 0, .7);
        }

        .input-box {
            position: absolute;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            width: 700px;
            height: 37px;
            margin: auto;
        }

        .search-box {
            width: 100%;
            height: 100%;
            border-radius: 20px;
            background-color: white;
        }

        input, button {
            float: left;
            border: none;
            outline: none;
            background: none;
            font-size: 14px;
        }

        label {
            float: left;
            color: #fff;
        }

        input {
            width: 585px;
            line-height: 37px;
            padding-left: 15px;
            font-size: 16px;
            caret-color: green;
            border-radius: 20px 0 0 20px;
        }

        button {
            width: 100px;
            color: #fff;
            line-height: 37px;
            cursor: pointer;
            font-size: 16px;
            border-radius: 0 20px 20px 0;
            background-color: #5AA700;
        }

        .output-txt {
            position: absolute;
            display: block;
            font-size: 20px;
            left: 110%;
            /*top: 0;*/
        }
        .content{
            position: absolute;
            right: 0;
            width: auto;
            font-size: 16px;
            color: #fff;
            white-space: nowrap;
            padding: 3px 15px;
            z-index: 999;
            border-radius: 30px 0 0 30px;
            background-color: #5AA700;
            /*transition: all 2s ease-in-out;*/
        }
    </style>
</head>
<body>
<div class="wrap">
    <div class="show-box"></div>  
    <div class="barrage-box">
        <div class="input-box">
            <div class="search-box">
                <input class="input-txt" type="text">
                <button class="issue">发射</button>
            </div>
        </div>
    </div>
</div>
<script type="text/javascript" src="js/jquery-3.2.1.min.js"></script>
<script>
    var showBox = $('.show-box');
    var issue = $('.issue');
    var h = showBox.height();
    var w = showBox.width();
    var txt = $('.input-txt');
    issue.click(function(){
        var content=$('<div class="content">'+txt.val()+'</div>');
        txt.val('');
        txt.focus();
        showBox.append(content);
        var posY=Math.random()*h;
        content.css({
            'top': posY,
            'background-color': getColor()
        });
        content.animate({'right': w+100},8000, function() {
            $(this).remove();
        });
    })

    function getColor() {
        var r = Math.ceil(Math.random() * 255);
        var g = Math.ceil(Math.random() * 255);
        var b = Math.ceil(Math.random() * 255);
        return ("rgb(" + r + "," + g + "," + b + ")");
    }

    $(document).keydown(function(e) {
        var e=e || window.event;
        // console.log(e.keyCode);
        if(e.keyCode==13){
            issue.click();
        }
    });
</script>
</body>
</html>
