cmdline-fu
====================
CLI based front end for [ commandlinefu ]( http://www.commandlinefu.com/ ). 
commandlinefu is community based repository for usefull commandline such as one-liner or complex `find`, `openssl`, `mysql`... command. 

This script scrape available TAG from site's top page with `hpricot` for supporting query based on TAG.  
TAGS file are stored to `~/.cmdline-fu.tags`. 

Install
----------------------------------
gem install cmdline-fu


Sample Configuration("~/.cmdline-fu.conf")
----------------------------------
    {
      #--------------------------------------------------------
      # Proxy setting. you can overwrite this 
      # with HTTP_PROXY environment variable
      #--------------------------------------------------------
      # :http_proxy_  => 'http://192.168.1.1:3128',

      #--------------------------------------------------------
      # Disable colorized output
      #--------------------------------------------------------
      #:colorize     => false,

      #--------------------------------------------------------
      # Supported colors are...
      #  black red green yellow blue magenta cyan white
      #--------------------------------------------------------
      :color_match  => 'yellow',
      :color_desc   => 'cyan',
      :color_footer => 'green',

      #--------------------------------------------------------
      # Web Browser command used such as 'cmdline-fu browse o'.
      #--------------------------------------------------------
      # for linux
      :browse_cmd   => 'firefox',
      # :browse_cmd   => 'google-chrome',
      
      # Mac OSX's default
      # :browse_cmd   => 'open',
    }

Usage
----------------------------------

    cmdline-fu COMMAND [PAGE] [o] [-n]
    
      COMMAND: list_tag [MATCHER], browse, using WORD, by USER, tagged TAG, matching WORD
      PAGE: 1-999 (defaut: 1)
      o:    open in browser
      -n:   not colorize

Example
----------------------------------
  
    cmdline-fu renew_tag
    cmdline-fu list_tag
    cmdline-fu list_tag vm
    cmdline-fu browse
    cmdline-fu browse o
    cmdline-fu using find
    cmdline-fu by t9md
    cmdline-fu tagged install
    cmdline-fu matching find

Abbreviation
----------------------------------
    Unique abbreviation for command is supported.

    cmdline-fu r
    cmdline-fu l
    cmdline-fu l vm
    cmdline-fu br
    cmdline-fu u find 2
    cmdline-fu u find 2 o
    cmdline-fu by t9md
    cmdline-fu t install
    cmdline-fu m find

Copyright
====================
Copyright (c) 2010 t9md. See LICENSE.txt for
further details.
