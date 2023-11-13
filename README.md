# CDN-Cloudflare
# دریافت سرتیفیکت
Get your server up to date:

```bash
apt update && apt upgrade -y
```

Also install ``curl`` and ``socat``:

```bash
apt install curl socat -y
```

# Install Acme Script

Download and install the Acme script for getting a free SSL certificate:

```bash
curl https://get.acme.sh | sh
```

# Get Free SSL Certificate

Set the default provider to Let’s Encrypt:

```bash
~/.acme.sh/acme.sh --set-default-ca --server letsencrypt
```

Register your account for a free SSL certificate. In the next command, replace ``xxxx@xxxx.com`` by your actual email address:

```bash
~/.acme.sh/acme.sh --register-account -m xxxx@xxxx.com
```

Obtain an SSL certificate. In the next command, replace host.mydomain.com by your actual host name:

``` bash
~/.acme.sh/acme.sh --issue -d host.mydomain.com --standalone
```

After a minute or so, the script terminates. On success, you will receive feedback as to the location of the certificate and key:

<pre>
Your cert is in: /root/.acme.sh/host.mydomain.com/host.mydomain.com.cer
Your cert key is in: /root/.acme.sh/host.mydomain.com/host.mydomain.com.key
The intermediate CA cert is in: /root/.acme.sh/host.mydomain.com/ca.cer
And the full chain certs is there: /root/.acme.sh/host.mydomain.com/fullchain.cer
</pre>

You cannot use the certificate and key in their current locations, as these may be temporary. Therefore install the certificate and key to a permanent location. In the next command, replace host.mydomain.com by your actual host name:

```bash
~/.acme.sh/acme.sh --installcert -d host.mydomain.com --key-file /root/private.key --fullchain-file /root/cert.crt
```

# اسکن آی پی سالم کلادفلر (تحت وب)  
<a href="https://vfarid.github.io/cf-ip-scanner" target="_blank"> CF IP Scanner github (تحت وب) </a>

<a href="https://cloudflare-v2ray.vercel.app/" target="_blank"> V2ray Cloudflare github (تحت وب) </a>

<a href="https://cloudflare-scanner.vercel.app/" target="_blank"> Cloudflare Scanner github (تحت وب) </a>

<a href="https://ircfspace.github.io/scanner/" target="_blank"> IRCF Scanner github (تحت وب) </a>

با تشکر از [ircf.space](https://github.com/ircfspace/scanner)
