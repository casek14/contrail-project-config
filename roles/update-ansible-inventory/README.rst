Purpose
=======

Use this role to add new hosts to Zuul executors ansible inventory based on the names they were given in Zuul's nodesets.
For example the following configuration would add all Zuul hosts with names prefixed 'openshift-master'
to both the 'openshift-master' and 'openshift-compute' ansible host groups.

zuul_host_matchers:
  - zuul_prefix: openshift-master
    ansible_host_group: openshift-masters
  - zuul_prefix: openshift-master
    ansible_host_group: openshift-compute
