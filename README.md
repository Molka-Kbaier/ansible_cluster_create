Ansible Kubernetes cluster automation scaffold.

Structure:
- inventory.ini : inventory for 1 master + 2 workers (edit IPs if needed)
- site.yml : main playbook orchestrator
- roles/ : roles used by the playbook (common, containerd, kubeadm, master, worker, cni, ingress, k8s-secrets)

Usage:
1. Review inventory.ini and update IPs and ansible_user if needed.
2. Copy this directory to your Ansible control host.
3. Run: ansible-playbook -i inventory.ini site.yml -u root
