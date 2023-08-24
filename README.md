# k8s-cheatsheet

## kubectl
### General commands
| Command           | Description |
| ------------------|---------------------------------------|
| `kubectl get all` | Get all resources |
| `kubectl describe <res-type> <resource>` | Get details on a resource |
| `kubectl delete <res-type> <resource>` | Delete a resource |
| `kubectl logs <pod-name>` | Get logs for an pod |


### Types of resources
| Resource          | Description |
| ------------------|---------------------------------------|
| pods | More than one container pod |
| pod | One container pod |
| deployment |  |
| service |  |

## How to configure ZSH for autocomplete
Taken from [here](https://gist.github.com/GusAntoniassi/2f58e716b67f648d13f91c1d780b05bf).

Use the following commands to add the kubectl autocomplete to zsh:

```shell
mkdir -p ~/.oh-my-zsh/custom/plugins/kubectl-autocomplete/
kubectl completion zsh > ~/.oh-my-zsh/custom/plugins/kubectl-autocomplete/kubectl-autocomplete.plugin.zsh
```

After that, edit your `~/.zshrc` to include the plugin `kubectl-autocomplete`, like so:

```
# ~/.zshrc
# ...
plugins=(kubectl-autocomplete)
```
