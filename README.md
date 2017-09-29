**Backporting the Global Reques ID feature to the old versions of OpenStack**

Links
=====
* [Spec](https://specs.openstack.org/openstack/oslo-specs/specs/pike/global-req-id.html)
* [List of patches on review.openstack.org](https://review.openstack.org/#/q/topic:global_request_id+OR+topic:request_id+OR+topic:global-request-id+OR+topic:request-id)
* [OpenStack-dev mailing list](http://lists.openstack.org/pipermail/openstack-dev/2017-June/117924.html)

Usage
=====
Copy all patches onto controller and compute hosts:
```bash
scp fuel/*.diff root@10.20.0.3:/usr/lib/python2.7/dist-packages/grid_patches/
```
Apply patches on the hosts:
```bash
cd /usr/lib/python2.7/dist-packages
cat grid_patches/*.diff | patch -p1
```
