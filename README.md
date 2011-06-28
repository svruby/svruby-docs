# The SV Ruby Club Docs

This repo holds all the content (and other bits) for the Silicon Valley Ruby Club documentation, located at [SV Ruby Achievements][svruby-achievements].

Documentation of the SV Ruby Club is written in the tense of Achievements rather than Process. For example, it is an Achievement to [Run a club meetup][doc-run-club-meetup]. The description of this Achievement includes the Process for running a club as a template. The documentation of our club is written from the perspective but it is more important that someone did "Run a club meetup" than how it was run.

Participation and progress are more important than Process and Policy.

As each member performs Achievements, they in turn receive Awards/Badges. Each Award they receive represents personal improvement and progressive achievement.

## Background to Documentation

The inspiration of this method of documentation came from the awesome guys at [Basho][basho] who have the [Basho Wiki][basho-wiki] setup with Gollum. It was also inspired by [Engine Yard's Docs][ey-docs] which Dr Nic was involved with.

We are using [Gollum][gollum] and [Gollum-Site][gol-site] to generate the documentation. Gollum is a great piece of open source software released by the GitHub team that lets you maintain and build wikis from the contents of a Git repo.

`gollum-site` generates html from pages written in any format supported by Gollum (ASCIIDoc, Creole, Markdown, Textile, etc.).

<A name="contrib">
## How to Contribute

Part of the reason we switched to Gollum and GitHub for the SV Ruby docs was to make it easier for people to contribute. Just treat it like a code repo: If you have anything to change or add, simply:

1. [Fork this repo][forking]

2. [Build a local copy][build]

3. Create a new Branch:

        git checkout -b <branch-name>

4. Add your changes

5. Commit changes to your branch

6. [Send us a pull request][pull-req]

If it's a small or obvious change, we're likely to merge it right away.  If we have questions, we'll communicate with you using the pull request's issue page.

The [Gollum README][gol-read] provides a great introduction to using the wiki system.

<A name="build">
## Building the Docs Locally

If you want to build and view the Docs locally, here is what you need to do:

1. Clone this repo:

        git clone git://github.com/svruby/svruby-docs.git

2. Ensure that you have [Bundler][bundler] installed:

        gem install bundler

3. Install all pre-requisite gems:

        bundle install

4. Generate the site and start a local server (This will take a minute. Don't fret.)

        rake generate   # Will generate the files
        rake serve      # Will start the gollum-site server

5. Navigate to <http://localhost:3011/Home.html> (Default) to access a fully-functional copy of the SVRuby Docs.


## Sanitization

You can customize sanitization with three options:

* --allow_elements: custom elements allowed, comma separated
* --allow_attributes: custom attributes allowed, comma separated
* --allow_protocols: custom protocols in *href* allowed, comma separated

       `$ gollum-site generate --allow_elements embed,object --allow_attributes src --allow_protocols irc`

<A name="feedback">
## Issues, Questions, Comments, Etc.

* Create a new [Issue][issues]

[svruby-achievements]:     http://achievements.svruby.com/ "SV Ruby Club Achievements"
[ey-docs]:    http://docs.engineyard.com "EY Docs"
[doc-run-club-meetup]: http://docs.svruby.com/run-club-meetup.html
[forking]:    http://help.github.com/forking/ "Github Forking Guide"
[pull-req]:   http://help.github.com/pull-requests/ "Github Pull-Requests Guide"
[build]:      #build "Building the Wiki"
[bundler]:    https://github.com/carlhuda/bundler/ "Bundler"
[gol-read]:   https://github.com/github/gollum/blob/master/README.md "Gollum README"
[gollum]:     https://github.com/github/gollum "Gollum Repo"
[gol-site]:   https://github.com/dreverri/gollum-site "Gollum-Site Repo"
[basho-wiki]: http://wiki.basho.com "Basho Wiki"
[basho]:      http://basho.com "Basho"
