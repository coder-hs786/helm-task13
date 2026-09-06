# Troubleshooting

## Issue 1: Ingress Resource Was Not Created

**Error:**  
No resources found in dev namespace.

**Root Cause:**  
templates/ingress.yaml was missing.

**Solution:**  
Created the Ingress template and upgraded the Helm release.

## Issue 2: Ingress Controller Was Unavailable

**Error:**  
No resources found for IngressClass.

**Root Cause:**  
NGINX Ingress Controller was not installed.

**Solution:**  
Installed the NGINX Ingress Controller.

## Issue 3: Browser Could Not Resolve ecommerce.local

**Error:**  
DNS_PROBE_FINISHED_NXDOMAIN

**Root Cause:**  
The custom hostname was not mapped in the Windows hosts file.

**Solution:**  
Added the following entry:

<EC2-PUBLIC-IP> ecommerce.local

Then flushed the DNS cache:

ipconfig /flushdns

## Lesson Learned

Learned to troubleshoot Helm deployments, configure NGINX Ingress, debug routing and hostname resolution, and access a Kubernetes application using a custom hostname.
