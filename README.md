# redis-sentinel-k8s
redis sentinel for k8s
## Usage
```bash
git clone https://github.com/fwt11/redis-sentinel-k8s.git
cd redis-sentinel-k8s
kubectl apply -k .
```
the cluster will run. Ｂy default there is only one master, all they other pod in the "redis" statefulset are replicas．If you want to
add another master, just copy `redis.yam`, then modify the statefulset's name, create that statefulset. `redis-test.yaml` is an example.
Maybe you need to modify `nfs-volume.yaml`.
