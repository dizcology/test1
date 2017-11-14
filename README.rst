`Google Cloud Storage: Node.js Client <https://github.com/googleapis/nodejs-storage>`__  |logo|
=======================================================================================

here |logo|

.. |logo| image:: https://avatars2.githubusercontent.com/u/2810941?v=3&s=96
   :height: 96px
   :width: 96px
   :alt: Google Cloud Platform logo
   :align: right

|release level| |CircleCI| |AppVeyor| |codecov|

    Node.js idiomatic client for `Cloud
    Storage <https://cloud.google.com/storage/docs>`__.

`Cloud Storage <https://cloud.google.com/storage/docs>`__ allows
world-wide storage and retrieval of any amount of data at any time. You
can use Google Cloud Storage for a range of scenarios including serving
website content, storing data for archival and disaster recovery, or
distributing large data objects to users via direct download.

-  `Cloud Storage Node.js Client API
   Reference <https://cloud.google.com/nodejs/docs/reference/storage/latest/>`__
-  `github.com/googleapis/nodejs-storage <https://github.com/googleapis/nodejs-storage>`__
-  `Cloud Storage
   Documentation <https://cloud.google.com/storage/docs>`__

Read more about the client libraries for Cloud APIs, including the older
Google APIs Client Libraries, in `Client Libraries
Explained <https://cloud.google.com/apis/docs/client-libraries-explained>`__.

**Table of contents:**

-  `Quickstart <#quickstart>`__

   -  `Before you begin <#before-you-begin>`__
   -  `Installing the client library <#installing-the-client-library>`__
   -  `Using the client library <#using-the-client-library>`__

-  `Samples <#samples>`__
-  `Versioning <#versioning>`__
-  `Contributing <#contributing>`__
-  `License <#license>`__

Quickstart
----------

Before you begin
~~~~~~~~~~~~~~~~

1. Select or create a Cloud Platform project.

   `Go to the projects
   page <https://console.cloud.google.com/project>`__

2. Enable billing for your project.

   `Enable
   billing <https://support.google.com/cloud/answer/6293499#enable-billing>`__

3. Enable the Google Cloud Storage API.

   `Enable the
   API <https://console.cloud.google.com/flows/enableapi?apiid=storage-api.googleapis.com>`__

4. `Set up authentication with a service
   account <https://cloud.google.com/docs/authentication/getting-started>`__
   so you can access the API from your local workstation.

Installing the client library
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

::

    npm install --save @google-cloud/storage

Using the client library
~~~~~~~~~~~~~~~~~~~~~~~~

.. code:: javascript

    // Imports the Google Cloud client library
    const Storage = require('@google-cloud/storage');

    // Your Google Cloud Platform project ID
    const projectId = 'YOUR_PROJECT_ID';

    // Creates a client
    const storage = new Storage({
      projectId: projectId,
    });

    // The name for the new bucket
    const bucketName = 'my-new-bucket';

    // Creates the new bucket
    storage
      .createBucket(bucketName)
      .then(() => {
        console.log(`Bucket ${bucketName} created.`);
      })
      .catch(err => {
        console.error('ERROR:', err);
      });

Samples
-------

Samples are in the
```samples/`` <https://github.com/googleapis/nodejs-storage/tree/master/samples>`__
directory. The samples’ ``README.md`` has instructions for running the
samples.

+-----------------------+-----------------------+-----------------------+
| Sample                | Source Code           | Try it                |
+=======================+=======================+=======================+
| ACL (Access Control   | `source               | |Open in Cloud Shell| |
| Lists)                | code <https://github. |                       |
|                       | com/googleapis/nodejs |                       |
|                       | -storage/blob/master/ |                       |
|                       | samples/acl.js>`__    |                       |
+-----------------------+-----------------------+-----------------------+
| Buckets               | `source               | |Open in Cloud Shell| |
|                       | code <https://github. |                       |
|                       | com/googleapis/nodejs |                       |
|                       | -storage/blob/master/ |                       |
|                       | samples/buckets.js>`_ |                       |
|                       | _                     |                       |
+-----------------------+-----------------------+-----------------------+
| Encryption            | `source               | |Open in Cloud Shell| |
|                       | code <https://github. |                       |
|                       | com/googleapis/nodejs |                       |
|                       | -storage/blob/master/ |                       |
|                       | samples/encryption.js |                       |
|                       | >`__                  |                       |
+-----------------------+-----------------------+-----------------------+
| Files                 | `source               | |Open in Cloud Shell| |
|                       | code <https://github. |                       |
|                       | com/googleapis/nodejs |                       |
|                       | -storage/blob/master/ |                       |
|                       | samples/files.js>`__  |                       |
+-----------------------+-----------------------+-----------------------+
| Notifications         | `source               | |Open in Cloud Shell| |
|                       | code <https://github. |                       |
|                       | com/googleapis/nodejs |                       |
|                       | -storage/blob/master/ |                       |
|                       | samples/notifications |                       |
|                       | .js>`__               |                       |
+-----------------------+-----------------------+-----------------------+
| Requester Pays        | `source               | |Open in Cloud Shell| |
|                       | code <https://github. |                       |
|                       | com/googleapis/nodejs |                       |
|                       | -storage/blob/master/ |                       |
|                       | samples/requesterPays |                       |
|                       | .js>`__               |                       |
+-----------------------+-----------------------+-----------------------+

The `Cloud Storage Node.js Client API
Reference <https://cloud.google.com/nodejs/docs/reference/storage/latest/>`__
documentation also contains samples.

Versioning
----------

This library follows `Semantic Versioning <http://semver.org/>`__.

This library is considered to be **General Availability (GA)**. This
means it is stable; the code surface will not change in
backwards-incompatible ways unless absolutely necessary (e.g. because of
critical security issues) or with an extensive deprecation period.
Issues and requests against **GA** libraries are addressed with the
highest priority.

More Information: `Google Cloud Platform Launch
Stages <https://cloud.google.com/terms/launch-stages>`__

Contributing
------------

Contributions welcome! See the `Contributing
Guide <https://github.com/googleapis/nodejs-storage/blob/master/.github/CONTRIBUTING.md>`__.

License
-------

Apache Version 2.0

See
`LICENSE <https://github.com/googleapis/nodejs-storage/blob/master/LICENSE>`__

.. |release level| image:: https://img.shields.io/badge/release%20level-general%20availability%20%28GA%29-brightgreen.svg?style=flat
   :target: https://cloud.google.com/terms/launch-stages
.. |CircleCI| image:: https://img.shields.io/circleci/project/github/googleapis/nodejs-storage.svg?style=flat
   :target: https://circleci.com/gh/googleapis/nodejs-storage
.. |AppVeyor| image:: https://ci.appveyor.com/api/projects/status/github/googleapis/nodejs-storage?branch=master&svg=true
   :target: https://ci.appveyor.com/project/googleapis/nodejs-storage
.. |codecov| image:: https://img.shields.io/codecov/c/github/googleapis/nodejs-storage/master.svg?style=flat
   :target: https://codecov.io/gh/googleapis/nodejs-storage
.. |Open in Cloud Shell| image:: http://gstatic.com/cloudssh/images/open-btn.png
   :target: https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/googleapis/nodejs-storage&page=editor&open_in_editor=samples/acl.js,samples/README.md
.. |Open in Cloud Shell| image:: http://gstatic.com/cloudssh/images/open-btn.png
   :target: https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/googleapis/nodejs-storage&page=editor&open_in_editor=samples/buckets.js,samples/README.md
.. |Open in Cloud Shell| image:: http://gstatic.com/cloudssh/images/open-btn.png
   :target: https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/googleapis/nodejs-storage&page=editor&open_in_editor=samples/encryption.js,samples/README.md
.. |Open in Cloud Shell| image:: http://gstatic.com/cloudssh/images/open-btn.png
   :target: https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/googleapis/nodejs-storage&page=editor&open_in_editor=samples/files.js,samples/README.md
.. |Open in Cloud Shell| image:: http://gstatic.com/cloudssh/images/open-btn.png
   :target: https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/googleapis/nodejs-storage&page=editor&open_in_editor=samples/notifications.js,samples/README.md
.. |Open in Cloud Shell| image:: http://gstatic.com/cloudssh/images/open-btn.png
   :target: https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/googleapis/nodejs-storage&page=editor&open_in_editor=samples/requesterPays.js,samples/README.md
.. |Open in Cloud Shell| image:: http://gstatic.com/cloudssh/images/open-btn.png
   :target: https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/googleapis/nodejs-storage&page=editor&open_in_editor=samples/acl.js,samples/README.md
.. |Open in Cloud Shell| image:: http://gstatic.com/cloudssh/images/open-btn.png
   :target: https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/googleapis/nodejs-storage&page=editor&open_in_editor=samples/buckets.js,samples/README.md
.. |Open in Cloud Shell| image:: http://gstatic.com/cloudssh/images/open-btn.png
   :target: https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/googleapis/nodejs-storage&page=editor&open_in_editor=samples/encryption.js,samples/README.md
.. |Open in Cloud Shell| image:: http://gstatic.com/cloudssh/images/open-btn.png
   :target: https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/googleapis/nodejs-storage&page=editor&open_in_editor=samples/files.js,samples/README.md
.. |Open in Cloud Shell| image:: http://gstatic.com/cloudssh/images/open-btn.png
   :target: https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/googleapis/nodejs-storage&page=editor&open_in_editor=samples/notifications.js,samples/README.md
.. |Open in Cloud Shell| image:: http://gstatic.com/cloudssh/images/open-btn.png
   :target: https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/googleapis/nodejs-storage&page=editor&open_in_editor=samples/requesterPays.js,samples/README.md
