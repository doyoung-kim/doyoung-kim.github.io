# 자주 사용사는 명령어 모음

## Kubernetes

### K3S
```
curl -sfL https://get.k3s.io | sh -s - --write-kubeconfig-mode 644 --bind-address 0.0.0.0 --tls-san  192.168.0.91 --disable traefik

# 기본 설치
curl -sfL https://get.k3s.io | sh -

# 특정 버전을 설치(traefik 비활성화하고 nginx ingress로 대체) 
curl -sfL https://get.k3s.io | INSTALL_K3S_VERSION="v1.23.7+k3s1" sh -s - --write-kubeconfig-mode 644 "--bind-address 0.0.0.0 --tls-san 192.168.56.10(HOST의IP) --disable traefik"

# k8s config 파일 생성 및 적용
mkdir -p ~/.kube
cp /etc/rancher/k3s/k3s.yaml ~/.kube/config

```
