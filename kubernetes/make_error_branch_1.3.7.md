
```  
root@SZX1000067823:/home/niujie/work/src/k8s.io/kubernetes# make
+++ [0926 16:12:31] Generating bindata:
    /home/niujie/work/src/k8s.io/kubernetes/test/e2e/framework/gobindata_util.go
Cannot find go-bindata. Install with
  go get -u github.com/jteeuwen/go-bindata/go-bindata
../../../../../../test/e2e/framework/gobindata_util.go:19: running "../../../hack/update-bindata.sh": exit status 5
make[1]: *** [_output/bin/deepcopy-gen] Error 1
make: *** [generated_files] Error 2
```

* set the GOPATH, the path may have pkg, src, bin
* make sure the $GOPATH include the path `bin`
* execute `go get -u github.com/jteeuwen/go-bindata/go-bindata`  or `make clean && make` 
* 

```  
root@SZX1000067823:/home/niujie/work/src/k8s.io/kubernetes# make
+++ [0926 17:08:55] Generating bindata:
    /home/niujie/work/src/k8s.io/kubernetes/test/e2e/framework/gobindata_util.go
+++ [0926 17:08:55] Building the toolchain targets:
    k8s.io/kubernetes/hack/cmd/teststale
+++ [0926 17:08:56] Building go targets for linux/amd64:
    cmd/libs/go2idl/deepcopy-gen
+++ [0926 17:09:01] Generating bindata:
    /home/niujie/work/src/k8s.io/kubernetes/test/e2e/framework/gobindata_util.go
+++ [0926 17:09:01] Building the toolchain targets:
    k8s.io/kubernetes/hack/cmd/teststale
+++ [0926 17:09:02] Building go targets for linux/amd64:
    cmd/libs/go2idl/conversion-gen
E0926 17:09:05.866109  109261 conversion.go:594] Warning: could not generate autoConvert functions for k8s.io/kubernetes/pkg/apis/apps/v1alpha1.PetSetSpec <-> k8s.io/kubernetes/pkg/apis/apps.PetSetSpec
E0926 17:09:06.184870  109261 conversion.go:594] Warning: could not generate autoConvert functions for k8s.io/kubernetes/pkg/apis/extensions/v1beta1.HorizontalPodAutoscalerSpec <-> k8s.io/kubernetes/pkg/apis/autoscaling.HorizontalPodAutoscalerSpec
E0926 17:09:06.196642  109261 conversion.go:594] Warning: could not generate autoConvert functions for k8s.io/kubernetes/pkg/apis/extensions/v1beta1.JobSpec <-> k8s.io/kubernetes/pkg/apis/batch.JobSpec
E0926 17:09:06.216026  109261 conversion.go:594] Warning: could not generate autoConvert functions for k8s.io/kubernetes/pkg/apis/extensions/v1beta1.RollingUpdateDeployment <-> k8s.io/kubernetes/pkg/apis/extensions.RollingUpdateDeployment
E0926 17:09:06.219176  109261 conversion.go:594] Warning: could not generate autoConvert functions for k8s.io/kubernetes/pkg/apis/extensions/v1beta1.ScaleStatus <-> k8s.io/kubernetes/pkg/apis/extensions.ScaleStatus
+++ [0926 17:09:06] Generating bindata:
    /home/niujie/work/src/k8s.io/kubernetes/test/e2e/framework/gobindata_util.go
+++ [0926 17:09:07] Building the toolchain targets:
    k8s.io/kubernetes/hack/cmd/teststale
+++ [0926 17:09:07] Building go targets for linux/amd64:
    cmd/libs/go2idl/openapi-gen
+++ [0926 17:09:14] Generating bindata:
    /home/niujie/work/src/k8s.io/kubernetes/test/e2e/framework/gobindata_util.go
+++ [0926 17:09:14] Building the toolchain targets:
    k8s.io/kubernetes/hack/cmd/teststale
+++ [0926 17:09:14] Building go targets for linux/amd64:
    cmd/kube-dns
    cmd/kube-proxy
    cmd/kube-apiserver
    cmd/kube-controller-manager
    cmd/kubelet
    cmd/kubemark
    cmd/hyperkube
    plugin/cmd/kube-scheduler
    cmd/kubectl
    cmd/gendocs
    cmd/genkubedocs
    cmd/genman
    cmd/genyaml
    cmd/mungedocs
    cmd/genswaggertypedocs
    cmd/linkcheck
    examples/k8petstore/web-server/src
    federation/cmd/genfeddocs
    vendor/github.com/onsi/ginkgo/ginkgo
    test/e2e/e2e.test
    vendor/github.com/onsi/ginkgo/ginkgo
    test/e2e_node/e2e_node.test
root@SZX1000067823:/home/niujie/work/src/k8s.io/kubernetes#
```
