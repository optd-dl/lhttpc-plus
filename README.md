Dependencies:
 * Erlang/OTP R13-B or newer
   * Application compiler to build, kernel, stdlib and ssl to run

Building: 
For versions > 1.2.5, lhttpc is built using rebar. Take a look at http://bitbucket.org/basho/rebar/wiki/Home for more information. There is still a Makefile with some of the old make targets, such as all, doc, test etc. for those who prefer that. The makefile will however just call rebar.

Configuration: (environment variables)
 * connection_timeout: The time (in milliseconds) the client will try to
                       kepp a HTTP/1.1 connection open. Changing this value
                       in runtime has no effect, this can however be done
                       through lhttpc_manager:update_connection_timeout/1.

NOTE: THIS FORK OF LHTTPC IS ONLY RECOMMENDED IF YOU HAVE MANY REQUESTS TO DO TO A FEW RESTRICTED DOMAINS.
It contains load-balancing mechanisms described in http://ferd.ca/rtb-where-erlang-blooms.html. It is not meant for general purpose use.


Plus:
 Increased more OTP service for getting worker process.
 * RANDOM_SIZE: define OTP server number. 
