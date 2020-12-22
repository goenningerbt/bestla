<a href="https://berloga-workshop.com/"><img src="https://github.com/goenningerbt/bestla/raw/main/images/bestla.png" height="200"/></a> Bestla: Mother of the gods Odin, Vili and Vé. <p style="font-size:10px">  Image by berloga-workshop.com</p>

# BESTLA

## What Is This?
BESTLA is a Common Lisp utility library for handling application configuration. It implements a layered configuration facility that allows for
b
1. using `.ini` file style config files,

2. using Common Lisp source code files as config files,

3. using [Consul](https://www.consul.io) by [HashiCorp](https://www.hashicorp.com) as a KV-store for configuration KV pairs,

4. using environment variables for storing configuration data.

BESTLA follows these rules of precedence:

1. If an environment variable is defined for the configuration key, then the value of this environment variable is taken as the configuration value. This returns two values: value, `:env` .

2. If `consul` is configured as a configuration value store and there is an entry for the configuration key, then the stored value for the key is taken as the configuration value. This returns two values: value, `:consul` .

3. If a config file is set as the configuration store and the configuration key is found in the config file, then the value for the key is taken as the configuration value. This returns two values: value, `:file` .

4. If there is a default value configured for the given configuration key, then this value is taken as the configuration value. This returns two values: value, `:default` .

5. If no configuration information is found, then this returns the values `nil`, `nil` .

## Licensing

### License and Rights To Use for Non-Commercial Purposes
<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.

### Commercial Use

For commercial licensing options, please contact Gönninger B&T's sales at [sales@goenninger.net](mailto:sales@goenninger.net) - Thank you.

## Reporting Problems
Generally you can report problems by [opening an issue](https://github.com/goenningerbt/bestla/issues). You should have the following pieces handy in order for us to be able to help you out as quickly and painlessly as possible:

* The application or module that is affected.
* The branch of of this softyware that you are using.
* A paste of the build log or failure message/ backtrace of the execution point you reached.
* Your operating system name and version.
* A short description of the actions that produced the issue.
* Patience.

## Contact
Currently, this repository is managed by Frank Goenninger (a.k.a. as "[frgo](http://ham-and-eggs-from-frgo.blogspot.com)"). He may be reached via email at [frank.goenninger@goenninger.net](mailto:frank.goenninger@goenninger.net).
