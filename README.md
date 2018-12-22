# PKS-Ninja-Patch

## This script is a stop-gap fix for issues in the current PKS-Ninja lab template.

## Use this file immediately after deploying lab v10 template.

### Fixes:

- CLI-VM
  - DNS name resolution
    - Set name switch resolution to hosts file and DNS only (/etc/nsswitch.conf)
    
  - PKS pipeline install
    - Remark out pipeline property conflicts (~/nsx-t-ci-pipeline/tasks/config-pks/task.yml, ~/nsx-t-ci-pipeline/tasks/config-pks/task.sh, ~/nsx-t-ci-pipeline/tasks/config-pks/config-pks-1.1.sh, ~/nsx-t-ci-pipeline/pipelines/install-pks-pipeline.yml, ~/nsx-t-ci-pipeline/pipelines/pks-params.yml)

    - Restrict platform deployment to Ops Man 2.3.0 and PKS 1.2.0 (~/nsx-t-ci-pipeline/pipelines/pks-params.yml)
    
### Directions:

- Execute `source cc-p1.sh` at the command line on cli-vm
