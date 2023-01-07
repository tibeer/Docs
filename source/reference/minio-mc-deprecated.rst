===================
Deprecated Commands
===================

.. default-domain:: minio

.. contents:: Table of Contents
   :local:
   :depth: 1

.. mc:: mc

The following table lists the commands deprecated by MinIO.
The table includes:

- Deprecated Command
- Replacement command (if applicable)
- Version of deprecation

Table of Deprecated Commands
----------------------------

.. list-table::
   :header-rows: 1
   :widths: 30 30 40
   :width: 100%

   * - Deprecated Command
     - Replacement Command
     - Version of Change

   * - ``mc ilm add``
     - :mc-cmd:`mc ilm rule add`
     - mc RELEASE.2022-12-24T15-21-38Z

   * - ``mc ilm edit``
     - :mc-cmd:`mc ilm rule edit`
     - mc RELEASE.2022-12-24T15-21-38Z

   * - ``mc ilm export``
     - :mc-cmd:`mc ilm rule export`
     - mc RELEASE.2022-12-24T15-21-38Z

   * - ``mc ilm import``
     - :mc-cmd:`mc ilm rule import`
     - mc RELEASE.2022-12-24T15-21-38Z

   * - ``mc ilm ls``
     - :mc-cmd:`mc ilm rule ls`
     - mc RELEASE.2022-12-24T15-21-38Z

   * - ``mc ilm rm``
     - :mc-cmd:`mc ilm rule rm`
     - mc RELEASE.2022-12-24T15-21-38Z


Table of Deprecated Admin Commands
----------------------------------

.. list-table::
   :header-rows: 1
   :widths: 30 30 40
   :width: 100%

   * - Deprecated Command
     - Replacement Command
     - Version of Change

   * - ``mc admin tier``
     - :mc-cmd:`mc ilm tier add`
     - mc RELEASE.2022-12-24T15-21-38Z


.. toctree::
   :titlesonly:
   :hidden:
   
   /reference/minio-mc/mc-ilm-add
   /reference/minio-mc/mc-ilm-edit
   /reference/minio-mc/mc-ilm-export
   /reference/minio-mc/mc-ilm-import
   /reference/minio-mc/mc-ilm-ls
   /reference/minio-mc/mc-ilm-rm
   /reference/minio-mc-admin/mc-admin-tier