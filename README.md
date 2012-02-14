HockeyApp gem
=============

This gem enables you to easily access the JSON Rest API of http://www.hockeyapp.net.

More info available on this API here : http://support.hockeyapp.net/kb/api


HOW-TO
======

1° Configure your connection :

HockeyApp::Config.configure do |config|
      config.token = "ABCDEF"
end

2° Make a client

client = HockeyApp.build_client

3° use the client

apps = client.get_apps
versions = apps.first.versions
crashes = apps.first.crashes
....

4° Read the specs formore use cases

