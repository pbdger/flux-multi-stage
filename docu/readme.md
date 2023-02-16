https://www.awstutorials.cloud/post/tutorials/flux-multi-stage/


```
kubectx mini-acpt
kubectl create ns flux

export GHUSER="pbdger"
fluxctl install \
--git-user=${GHUSER} \
--git-email=${GHUSER}@users.noreply.github.com \
--git-path=releases/acpt \
--git-branch=main \
--manifest-generation=true \
--git-url=git@github.com:${GHUSER}/flux-multi-stage \
--namespace=flux | kubectl apply -f -


```
