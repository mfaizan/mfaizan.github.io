---
title: blog
layout: null
---

<html>
<head>
    <title>Faizan Muhammad</title>
    <meta charset='UTF-8'>
    <meta content='width=device-width, initial-scale=1' name='viewport'/>

    <meta name='description' content='Faizan Muhammad is a Software Engineer at Google'>
    <!-- A decent browser will parse this fine:
         https://webmasters.stackexchange.com/questions/92744. -->
    <meta name='keywords' content='
        machine learning,
        statistical machine learning,
        bayesian inference,
        statistics,
        computational statistics,
        linear algebra,
        numerical linear algebra,
        statistical software,
        deep learning,
        computer science
    '>
    <meta name='author' content='Faizan Muhammad'>

    <link rel='shortcut icon' href='/favicon.png?v=e' />
    <link href='/css/blog.css' rel='stylesheet'/>

</head>
<body>
    {% include nav.html %}
    <div id='blog' class='wrap'>
        <div id='intro'>
        </div>
        <div id='posts' class='section'>
	    <h2> Posts </h2>
            {% for post in site.posts %}
                <div class='post-row'>
                    <p class='post-title'>
                        <a href="{{ post.url }}">
                            {{ post.title }}
                        </a>
                    </p>
                    <p class='post-date'>
                        {{ post.date | date_to_long_string }}
                    </p>
                </div>
                <p class='post-subtitle'>
                    {{ post.subtitle }}
                </p>
                <span class='hidden'>{{ forloop.index }}</span>
            {% endfor %}
        </div>
    </div>
</body>
</html>
