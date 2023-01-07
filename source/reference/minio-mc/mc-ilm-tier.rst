===============
``mc ilm tier``
===============

.. default-domain:: minio

.. contents:: Table of Contents
   :local:
   :depth: 2

.. mc:: mc ilm tier

.. versionchanged:: RELEASE.2022-12-24T15-21-38Z

   :mc-cmd:`mc ilm tier` replaces ``mc admin tier``.

Description
-----------

.. start-mc-ilm-tier-desc

The :mc:`mc ilm tier` command and its subcommands configure a remote supported S3-compatible service for MinIO :ref:`Lifecycle Management: Object Transition ("Tiering") <minio-lifecycle-management-expiration>`. 

.. end-mc-ilm-tier-desc

After creating one or more tiers with this command, use :mc-cmd:`mc ilm rule` and its subcommands to create the rules that move objects to other storage.

For more information, see the overview of :ref:`lifecycle management <minio-lifecycle-management>`.

Subcommands
-----------

:mc-cmd:`mc ilm tier` includes the following subcommands:

- :mc-cmd:`mc ilm tier add`
- :mc-cmd:`mc ilm tier check`
- :mc-cmd:`mc ilm tier info`
- :mc-cmd:`mc ilm tier ls`
- :mc-cmd:`mc ilm tier rm`
- :mc-cmd:`mc ilm tier update`

Required Permissions
--------------------

To create tiers for object transition, MinIO requires the following administrative permissions on the cluster:

- :policy-action:`admin:SetTier`
- :policy-action:`admin:ListTier`

For example, the following policy provides permission for configuring object transition lifecycle management rules on any bucket in the cluster:.

.. literalinclude:: /extra/examples/LifecycleManagementAdmin.json
   :language: json
   :class: copyable

Transition Permissions
~~~~~~~~~~~~~~~~~~~~~~

Object transition lifecycle management rules require additional permissions on the remote storage tier. 
Specifically, MinIO requires the remote tier credentials provide read, write, list, and delete permissions.

For example, if the remote storage tier implements AWS IAM policy-based access control, the following policy provides the necessary permission for transitioning objects into and out of the remote tier:

.. literalinclude:: /extra/examples/LifecycleManagementUser.json
   :language: json
   :class: copyable

Modify the ``Resource`` for the bucket into which MinIO tiers objects.

Defer to the documentation for the supported tiering targets for more complete information on configuring users and permissions to support MinIO tiering:

- :aws-docs:`Amazon S3 Permissions <service-authorization/latest/reference/list_amazons3.html#amazons3-actions-as-permissions>`
- `Google Cloud Storage Access Control <https://cloud.google.com/storage/docs/access-control>`__
- `Authorizing access to data in Azure storage <https://docs.microsoft.com/en-us/azure/storage/common/storage-auth?toc=/azure/storage/blobs/toc.json>`__


.. toctree::
   :titlesonly:
   :hidden:
   
   /reference/minio-mc/mc-ilm-tier-add
   /reference/minio-mc/mc-ilm-tier-check
   /reference/minio-mc/mc-ilm-tier-info
   /reference/minio-mc/mc-ilm-tier-ls
   /reference/minio-mc/mc-ilm-tier-rm
   /reference/minio-mc/mc-ilm-tier-update