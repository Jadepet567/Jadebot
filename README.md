[![Gem](https://img.shields.io/gem/v/discordrb.svg)](https://rubygems.org/gems/discordrb)



2
[![Gem](https://img.shields.io/gem/dt/discordrb.svg)](https://rubygems.org/gems/discordrb)



3
[![Build Status](https://travis-ci.org/meew0/discordrb.svg?branch=master)](https://travis-ci.org/meew0/discordrb)



4
[![Inline docs](http://inch-ci.org/github/meew0/discordrb.svg?branch=master&style=shields)](http://inch-ci.org/github/meew0/discordrb)



5
[![Code Climate](https://codeclimate.com/github/meew0/discordrb/badges/gpa.svg)](https://codeclimate.com/github/meew0/discordrb)



6
[![Test Coverage](https://codeclimate.com/github/meew0/discordrb/badges/coverage.svg)](https://codeclimate.com/github/meew0/discordrb/coverage)



7
[![Join Discord](https://img.shields.io/badge/discord-join-7289DA.svg)](https://discord.gg/0SBTUU1wZTWfFQL2)



8
# discordrb



9
​



10
An implementation of the [Discord](https://discordapp.com/) API using Ruby.



11
​



12
## Quick links to sections



13
​



14
* [Dependencies](https://github.com/meew0/discordrb#dependencies)



15
* [Installation](https://github.com/meew0/discordrb#installation)



16
* [Usage](https://github.com/meew0/discordrb#usage)



17
* [Support](https://github.com/meew0/discordrb#support)



18
* [Development](https://github.com/meew0/discordrb#development), [Contributing](https://github.com/meew0/discordrb#contributing)



19
* [License](https://github.com/meew0/discordrb#license)



20
​



21
See also: [Documentation](http://www.rubydoc.info/gems/discordrb), [Tutorials](https://github.com/meew0/discordrb/wiki)



22
​



23
## Dependencies



24
​



25
* Ruby 2.1+



26
* An installed build system for native extensions (on Windows, try the [DevKit](http://rubyinstaller.org/downloads/); installation instructions [here](https://github.com/oneclick/rubyinstaller/wiki/Development-Kit#quick-start) - you only need to do the quick start)



27
​



28
### Voice dependencies



29
​



30
This section only applies to you if you want to use voice functionality.



31
* [libsodium](https://github.com/meew0/discordrb/wiki/Installing-libsodium)



32
* A compiled libopus distribution for your system, anywhere the script can find it. See [here](https://github.com/meew0/discordrb/wiki/Installing-libopus) for installation instructions.



33
* [FFmpeg](https://www.ffmpeg.org/download.html) installed and in your PATH



34
​



35
In addition to this, if you're on Windows and want to use voice functionality, your installed Ruby version **needs to be 32 bit**, as otherwise Opus won't work.



36
​



37
## Installation



38
​



39
### Linux



40
​



41
On Linux, it should be as simple as running:



42
​



43
    gem install discordrb



44
​



45
### Windows



46
​



47
On Windows, to install discordrb, run this in a shell **(make sure you have the DevKit installed! See the [Dependencies](https://github.com/meew0/discordrb#dependencies) section)**:



48
​



49
    gem install discordrb --platform=ruby



50
​



51
Run the [ping example](https://github.com/meew0/discordrb/blob/master/examples/ping.rb) to verify that the installation works (make sure to replace the username and password in there with your own or your bots'!):



52
​



53
    ruby ping.rb



54
​



55
#### Troubleshooting



56
​



57
**If you get an error like this when installing the gem**:



58
​



59
    ERROR:  Error installing discordrb:



60
            The 'websocket-driver' native gem requires installed build tools.



61
​



62
You're missing the development kit required to build native extensions. Download the development kit [here](http://rubyinstaller.org/downloads/) (scroll down to "Development Kit", then choose the one for Ruby 2.0 and your system architecture) and extract it somewhere. Open a command prompt in that folder and run:



63
​



64
    ruby dk.rb init



65
    ruby dk.rb install



66
​



67
Then reinstall discordrb:



68
​



69
    gem uninstall discordrb



70
    gem install discordrb



71

