# One page Portfolio Website (HTML CSS Project) sample

spawebapp

index.htlm
contains matomo js code snipet

<!-- Matomo -->
<script>
  var _paq = window._paq = window._paq || [];
  /* tracker methods like "setCustomDimension" should be called before "trackPageView" */
  _paq.push(['trackPageView']);
  _paq.push(['enableLinkTracking']);
  (function() {
    var u="//matomo.local:8443/";
    _paq.push(['setTrackerUrl', u+'matomo.php']);
    _paq.push(['setSiteId', '1']);
    var d=document, g=d.createElement('script'), s=d.getElementsByTagName('script')[0];
    g.async=true; g.src=u+'matomo.js'; s.parentNode.insertBefore(g,s);
  })();
</script>
<!-- End Matomo Code -->


build docker image

docker build -t spaapp_nginx .
docker login
docker tag spaapp_nginx lihovach/spaapp_nginx
docker push lihovach/spaapp_nginx

use deployment.yaml to deploy to k8s

kubectl apply -f deployment.yaml -n default

