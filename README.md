# IoT-zbouayya

Kubernetes manifests deployed by Argo CD for Part 3 of
[Inception-of-Things](https://github.com/zakariabouayyad/Inception-of-Things).

Argo CD watches the `dev/` folder on `main` and syncs it into the `dev` namespace.

Switch the app version:

```bash
sed -i 's/playground:v1/playground:v2/' dev/deployment.yaml
git commit -am "v2" && git push
# a few minutes later
curl http://localhost:8888/   # {"status":"ok", "message": "v2"}
```
