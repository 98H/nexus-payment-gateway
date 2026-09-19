# Deployment & Operations Guide: Payment Gateway

## 🚀 Live Access & URLs
- **Live Public Access URL:** [/preview/prod-payment-gateway-e7deee/](/preview/prod-payment-gateway-e7deee/)
- **Internal Port:** `0`
- **Runtime Engine:** `python_preview`
- **Deployment Status:** `DEPLOYED / ACTIVE`
- **Timestamp:** `2026-09-19T16:14:54.940662+00:00`

## 🛠️ Management & Service Control
### Launch Command
```bash
python3 app.py --port 0
```

### Health Check Probe
```bash
curl -I http://127.0.0.1:0/
```

### Systemd Service Template
```ini
[Unit]
Description=Payment Gateway Service
After=network.target

[Service]
Type=simple
WorkingDirectory=/tmp/pytest-of-root/pytest-0/test_human_blocker_resolution_0/repo/workspaces/prod-payment-gateway-e7deee
ExecStart=/usr/bin/python3 /tmp/pytest-of-root/pytest-0/test_human_blocker_resolution_0/repo/workspaces/prod-payment-gateway-e7deee/app.py
Restart=always
RestartSec=3

[Install]
WantedBy=multi-user.target
```

## 🔒 Production Security Protocols
- HTTP-only reverse proxy via Nexus Gateway.
- Dedicated port allocation with zero port conflict.
