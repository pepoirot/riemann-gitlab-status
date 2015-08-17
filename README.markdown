# Riemann Gitlab Status

Report the statuses and uptimes of the [individual components](https://github.com/gitlabhq/gitlabhq/blob/v7.13.5/doc/development/architecture.md#components) of a Gitlab ([Omnibus](https://github.com/gitlabhq/gitlabhq/blob/v7.13.5/doc/development/omnibus.md#what-you-should-know-about-omnibus-packages)) instance (Nginx, Unicorn, Redis, etc.) using `gitlab-ctl`:

```sh
$ gitlab-ctl status
run: logrotate: (pid 20055) 442s; run: log: (pid 5834) 76135s
run: nginx: (pid 20718) 374s; run: log: (pid 5725) 76141s
run: redis: (pid 20084) 441s; run: log: (pid 5563) 76160s
run: sidekiq: (pid 20102) 438s; run: log: (pid 5662) 76147s
run: unicorn: (pid 20122) 436s; run: log: (pid 5613) 76154s
```

## Platform(s)

This was tested on Centos 6 against [Gitlab 7.11.4 EE Omnibus](https://packages.gitlab.com/gitlab/gitlab-ee?filter=rpms).

## Limitation(s)

This only supports the [Omnibus versions](https://github.com/gitlabhq/gitlabhq/blob/v7.13.5/doc/development/omnibus.md#what-you-should-know-about-omnibus-packages) versions of Gitlab.
