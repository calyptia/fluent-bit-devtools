# Development tools

Helper scripts to deploy the various end points we want to develop or debug locally.

Most of these scripts work on K8S deployments so a kube-context should be set up for them if you want it to work with a specific K8S cluster, e.g. in GKE or similar.
There is a [helper script](./create-kind-cluster.sh) to deploy a local K8S cluster with Kubernetes-in-docker (KIND) as well that should be run first.

| Script                | Description                                                                                                        |
|-----------------------|--------------------------------------------------------------------------------------------------------------------|
|create-kind-cluster.sh | Spins up a local KIND cluster for you to use. Not required for the rest but make sure a valid kube-context is set. |
|deploy-elastic.sh      | Deploys an Elasticsearch instance into a separate namespace within K8S.                                            |
|deploy-kafka.sh        | Deploys a Kafka instance into a separate namespace within K8S.                                                     |
|deploy-loki.sh         | Deploys a Loki instance into a separate namespace within K8S.                                                      |
|deploy-prometheus.s    | Deploys a Prometheus instance into a separate namespace within K8S.                                                |
|deploy-splunk.sh       | Deploys a Splunk instance into a separate namespace within K8S.                                                    |
|local-minio.sh         | Deploys a container running Minio to your local machine, not in K8S.                                               |
|run-unit-tests.sh      | Uses a CMake-based container to run unit tests with various tools (valgrind, coverage, etc.)                       |
|monitoring/run.sh      | Runs up a local Prometheus and Grafana stack with Fluent Bit to monitor it all.                                    |
