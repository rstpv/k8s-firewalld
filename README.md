# k8s-firewalld
Firewalld service configuration files for rancher 2.x hosts (Based on the job done by wrightrocket in his repo k8s-firewalld)

To test on a node with etcd role:
<ul>
  <li>Copy the k8s-etcd.xml file to the /etc/firewalld/services directory</li>
  <li>Reload the firewall daemon with firewall-cmd --reload</li>
  <li>Add the service to the appropriate zone with firewall-cmd --add-service=k8s-etcd --zone=public</li>
  <li>Execute firewall-cmd --runtime-to-permanent</li>
</ul>

To test on a node with control role:
<ul>
  <li>Copy the k8s-control.xml file to the /etc/firewalld/services directory</li>
  <li>Reload the firewall daemon with firewall-cmd --reload</li>
  <li>Add the service to the appropriate zone with firewall-cmd --add-service=k8s-control --zone=public</li>
  <li>Execute firewall-cmd --runtime-to-permanent</li>
</ul>


To test on a Kubernetes Worker:
<ul>
  <li>Copy the k8s-worker.xml file to the /etc/firewalld/services directory</li>
  <li>Reload the firewall daemon with firewall-cmd --reload</li>
  <li>Add the service to the appropriate zone with firewall-cmd --add-service=k8s-worker --zone=public</li>
  <li>Execute firewall-cmd --runtime-to-permanent</li>
</ul>

If a node has more than one role you can follow the steps for each role.
