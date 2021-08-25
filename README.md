# Data Science Desafios

Aqui ire almancenando los desafios del curso Data Science en Coder House. Los primeros seran importados de Google Colab y dependiendo de la complejidad o versitilidad de Colab tendran otros origenes. 

Para ver ejercicios de practica: https://github.com/chmedinap/DS-Practicas

As you already know, Last Fm is a service (kind of a social network) to store your music listening activity, that is called *scrobbling*, and I have been using that service since late 2008. The goal of this project is to create new visualization, Last Fm itself shows some nice charts and numbers but I wanted a little more.

In this first part I'm going to show you how to extract the data and clean it using Python, but please keep in mind that **I'm new in the data analytics/science world and English is not my native language. I'm still learning. If you could give  me your feedback about these two topics, I would really appreciate it.**

<h2>Understating the API.</h2>

Last Fm offer a very simple API. It doesn't need authentication and the payload is very simple. But they ask you some things: 

* To use an identifiable User-Agent header on all requests.
* To be reasonable, don't make an excessive number of calls. 
* And of course, the assumption that if you use the API you are accepting its terms of service.

Link: https://www.last.fm/api/intro

You can create an API KEY https://www.last.fm/api/account/create or find the API at http://ws.audioscrobbler.com/2.0/

The API have some methods like album, artist, users, playlist. Each one has some customizable options. In this post I'm going to use two: recent tracks and loved tracks.

<h2>Building the script</h2>

I'm going to do a lot of request with the same user, key and user-agent, so the best way to do it is to create a function.
