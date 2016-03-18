   _____ ______ _   _  ____
  / ____|  ____| \ | |/ __ \
 | |    | |__  |  \| | |  | |
 | |    |  __| | . ` | |  | |
 | |____| |____| |\  | |__| |
  \_____|______|_| \_|\____/



README

  CENO is innovative censorship circumvention technology based on a P2P distributed caching network.

  The goal of CENO is to make access to restricted content in areas facing censorship easy and more reliable. CENO exfiltrates document requests out of a censored area using an anonymous transport layer. It then uses networks such as Freenet to store encrypted documents in such a way that they can be easily retrieved securely by individuals in the censored area.

  This all-in-one package includes the following:
    * A Freenet node, preloaded with the WebOfTrust, Freemail and CENO plugins in a way that they will automatically updated via Freenet, as well as preconfigured with the CENO Client identity. Opennet is enabled by default, meaning that your node will try to connect to seed nodes once it gets started.
    * The CENO Client proxy that will forward your browser's traffic via the CENO Freenet plugin.
    * A Chrome and a Firefox plugin that forward all traffic to the CENO Client proxy.



DISCLAIMER

  By using CENO, other people will know that you are using Internet censorship circumvention tools. They won't be able to tell though what websites and files you are trying to access with it.



INSTALL

  1. Un-tar the CENOBox.tar.gz in a directory in your machine.
  2. Navigate to that directory and execute the CENO script:
      ./CENO.sh
     This will start the Freenet node, the CENO client proxy, and a Firefox private session pre-configured to proxy traffic through CENO.
  3. Use the new Firefox window to surf anonymously the Web, evading censorship.

  Optional steps:
  - Configure your Freenet node, by visiting `http://127.0.0.1:8888/wizzard/` using a private/incognito browser session.
  - Use the CeNo intercept plugin on Chrome or Chromium. Instructions on how to do that reside in the CENOChrome directory.
  - If you would like to use a browser other than Firefox or Chrome/Chromium, you have to manually configure proxy settings so that all traffic is proxied through "127.0.0.1:3090". Again, remember to always use a private/incognito session when using CENO.


  Next time you want to use CENO, you can navigate to the directory you had initially un-tared CENOBox.tar.gz and execute the CENO.sh script.
  Remember to configure your browser accordingly and always use a private/incognito session.

  Detailed instructions on how to build and load the CENO client plugin on a running Freenet node can be found at the CENO repository:
  https://github.com/equalitie/ceno



WEB SITE

  Visit the CENO web site for the latest news and downloads:

      https://censorship.no
