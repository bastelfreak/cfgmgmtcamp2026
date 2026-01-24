flowchart LR
  clj-http-client
  clj-i18n
  clj-kitchensink
  clj-rbac-client
  clj-shell-utils
  clj-typesafe-config
  comidi
  dujour-version-check
  jruby-deps
  jruby-utils
  jvm-ssl-utils
  ring-middleware
  stockpile
  structured-logging
  trapperkeeper
  trapperkeeper-authorization
  trapperkeeper-comidi-metrics
  trapperkeeper-filesystem-watcher
  trapperkeeper-metrics
  trapperkeeper-scheduler
  trapperkeeper-status
  trapperkeeper-webserver-jetty10

  clj-i18n ==> clj-http-client
  jvm-ssl-utils ==> clj-http-client

  clj-kitchensink ==> clj-i18n
  
  clj-http-client ==> clj-rbac-client
  clj-i18n ==> clj-rbac-client
  clj-kitchensink ==> clj-rbac-client
  ring-middleware ==> clj-rbac-client
  trapperkeeper ==> clj-rbac-client

  clj-i18n ==> clj-shell-utils
  clj-kitchensink ==> clj-shell-utils
  trapperkeeper ==> clj-shell-utils

  clj-kitchensink ==> comidi

  clj-http-client ==> dujour-version-check

  clj-i18n ==> jruby-utils
  jruby-deps ==> jruby-utils
  clj-kitchensink ==> jruby-utils
  ring-middleware ==> jruby-utils
  trapperkeeper ==> jruby-utils

  clj-i18n ==> jvm-ssl-utils
  
  clj-http-client ==> ring-middleware

  clj-i18n ==> stockpile

  clj-i18n ==> trapperkeeper
  clj-kitchensink ==> trapperkeeper
  clj-typesafe-config ==> trapperkeeper
  
  clj-i18n ==> trapperkeeper-authorization
  clj-kitchensink ==> trapperkeeper-authorization
  clj-rbac-client ==> trapperkeeper-authorization
  ring-middleware ==> trapperkeeper-authorization
  jvm-ssl-utils ==> trapperkeeper-authorization
  trapperkeeper ==> trapperkeeper-authorization
  
  comidi ==> trapperkeeper-comidi-metrics
  trapperkeeper-metrics ==> trapperkeeper-comidi-metrics

  trapperkeeper ==> trapperkeeper-filesystem-watcher
  clj-kitchensink ==> trapperkeeper-filesystem-watcher
  clj-i18n ==> trapperkeeper-filesystem-watcher

  comidi ==> trapperkeeper-metrics
  clj-i18n ==> trapperkeeper-metrics
  clj-kitchensink ==> trapperkeeper-metrics
  ring-middleware ==> trapperkeeper-metrics
  trapperkeeper ==> trapperkeeper-metrics
  trapperkeeper-authorization ==> trapperkeeper-metrics
  
  clj-i18n ==> trapperkeeper-scheduler
  clj-kitchensink ==> trapperkeeper-scheduler
  trapperkeeper ==> trapperkeeper-scheduler
  
  clj-kitchensink ==> trapperkeeper-status
  trapperkeeper ==> trapperkeeper-status
  trapperkeeper-scheduler ==> trapperkeeper-status
  ring-middleware ==> trapperkeeper-status
  comidi ==> trapperkeeper-status
  clj-i18n ==> trapperkeeper-status
  trapperkeeper-authorization ==> trapperkeeper-status

  clj-i18n ==> trapperkeeper-webserver-jetty10
  clj-kitchensink ==> trapperkeeper-webserver-jetty10
  jvm-ssl-utils ==> trapperkeeper-webserver-jetty10
  trapperkeeper ==> trapperkeeper-webserver-jetty10
  trapperkeeper-filesystem-watcher ==> trapperkeeper-webserver-jetty10
