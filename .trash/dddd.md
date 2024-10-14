---
title: "Untitled"
draft: false
tags:
  - 
---

<head>
<style>
     /* Main timeline grid container */
      .timeline {
        display: grid;
        grid-template-columns: 1fr auto 1fr; /* 3 columns: left content, timeline, right content */
        grid-gap: 10px;
        max-width: 100%; /* Control the width of the timeline */
            margin: 0 auto; /* Center the timeline horizontally */
            position: relative;
        }

        /* Timeline line in the middle */
        .timeline::before {
            content: '';
            position: absolute;
            width: 6px;
            background-color: #ddd;
            top: 0;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%); /* Center the timeline line */
        }

		/* Shared container styles */ 
		.container { 
			position: relative; 
			padding: 0px 20px; 
		}

        /* Left content container */
        .container.left {
            grid-column: 1 / 2; /* Left content spans first column */
        }

        /* Right content container */
        .container.right {
            grid-column: 3 / 4; /* Right content spans third column */
        }
		
	
        /* Circle for the left side */
        .container.left::after {
            content: '';
            position: absolute;
            width: 25px;
            height: 25px;
            background-color: white;
            border: 4px solid #2196F3;
            top: -4px;
            right: -27px; /* Position the circle on the right edge of the left content */
            border-radius: 50%;
            z-index: 1;
        }

        /* Circle for the right side */
        .container.right::after {
            content: '';
            position: absolute;
            width: 25px;
            height: 25px;
            background-color: white;
            border: 4px solid #2196F3;
            top: -4px;
            left: -27px; /* Position the circle on the left edge of the right content */
            border-radius: 50%;
            z-index: 1;
        }

        /* Date box for the left side */
        .container.left .date {
            padding: 10px;
            background-color: #2196F3;
            color: white;
            position: absolute;
            width: 60px;
            text-align: center;
            border-radius: 6px;
            top: -8px;
            right: -98px; /* Position the date box to the left of the left content */
        }

        /* Date box for the right side */
        .container.right .date {
            padding: 10px;
            background-color: #2196F3;
            color: white;
            position: absolute;
            width: 60px;
            text-align: center;
            border-radius: 6px;
            top: -8px;
            left: -95px; /* Position the date box to the right of the right content */
        }

        /* Content box styling */
        .content {
            padding: 20px 30px;
            background-color: white;
            position: relative;
            border-radius: 6px;
            border: 1px solid #ddd;
        }
</style>
</head>



<div class="timeline" style="grid-row: 1;">
    <div class="container left">
        <div class="date">date</div>
        <div class="content">
            <h2><a href="./Useful Syntax.md">Useful Synta</a></h2>
            <p>testing 123</p>
        </div>
    </div>
    <div class="container right" style="grid-row: 2;">
        <div class="date">2004</div>
        <div class="content">
            <h2><a href="https://www.facebook.com" target="_blank">Facebook</a></h2>
            <p>Facebook started as a social networking site for students. with really long line whatever blablablabla n;an;an;an;akjsdfakjkdvns</p>
        </div>
    </div>
    <div class="container left" style="grid-row: 3;">
        <div class="date">2005</div>
        <div class="content">
            <h2><a href="https://www.youtube.com" target="_blank">YouTube</a></h2>
            <p>YouTube, a video sharing platform, was launched.</p>
        </div>
    </div>
    <div class="container right" style="grid-row: 4;">
        <div class="date">2006</div>
        <div class="content">
            <h2><a href="https://www.twitter.com" target="_blank">Twitter</a></h2>
            <p>Twitter, a microblogging platform, was introduced.</p>
        </div>
    </div>
</div>

</body>

