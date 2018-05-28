# traefik-consul-demo

Simply running `vagrant up` will spin up this and test that it works via curl.
On success you will see something like this in your terminal:

```bash
default: ++ curl --header Host:tester8000.lb.local localhost
default:   % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
default:                                  Dload  Upload   Total   Spent    Left  Speed
           0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0
default: <xmp>
default: Hello World
default:
default:
default:                                        ##         .
default:                                  ## ## ##        ==
default:                               ## ## ## ## ##    ===
default:                            /""""""""""""""""\___/ ===
default:                       ~~~ {~~ ~~~~ ~~~ ~~~~ ~~ ~ /  ===- ~~~
default:                            \______ o          _,/
default:                             \      \       _,'
default:                              `'--.._\..--''
default: </xmp>
```

1.访问 consul : http://192.168.16.11:8500/ui
2.访问 traefik   http://192.168.16.11:8080/dashboard/
3.通过 consulDemo 注入服务信息到consul，然后traefik dashboard自动发现该服务
4.curl 测试 ： curl -H Host:tester8001.lb.local http://127.0.0.1
