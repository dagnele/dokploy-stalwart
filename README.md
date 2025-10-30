# dokploy-stalwart
How to setup stalwart in dokploy installation


Edit the file `/opt/stalwart/etc/config.toml` adding the following at the very bottom.

```toml
certificate.default.cert = "%{file:/certs/[domain]/certificate.crt}%"
certificate.default.private-key = "%{file:/certs/[domain]/privatekey.key}%"
certificate.default.default = true
```
