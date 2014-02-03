golang_transformer
==================

Summary
-------

Transformer to help work with a Golang backend while working with Dartlang

Background
----------

I created this transformer to help me work with the Dart Editor. I built my backend in Go and wanted my Dart app to talk to it by way of HTML FORMs. This proved difficult when I used the Dart Editor to test and debug my Dart front end. The main reason was because the Dart Editor's 'pub serve' ran it's own server and I could not do FORM POSTs or GETs using relative URLS which I needed for my back end.

So what I did was made this transformer that would run whenever you built your Dart app. The transformer goes through all your HTML files looking for FORM ACTION attributes. When it finds one, it will remove it thus converting my Absolute URL into a relative URL. You add the part to remove in the 'pubspec.yaml' file.

Naming
------

I named this the golang_transformer keeping in mind that I'll use it to solve more quirks that I encounter when trying to plug a Dart frontend into a Go backend. For the moment, all it does is FORM ACTION fields, but it can easily be extended. If you have ideas for extending it, please send me a Pull Request.

