.. Copyright 2016 FUJITSU LIMITED

.. _workspace-create:

workspace_create
----------------

.. function:: POST /orgs/{oid}/workspaces

.. sidebar:: Summary

	* Method: ``POST``
	* Response Code: ``201``
	* Response Formats: ``application/xml`` ``application/json``
	* Since: ``UForge 3.3.2``

Creates a new workspace in an organization. 

This request is similar to :ref:`userWorkspace-create` 

Please refer to :ref:`workspace-object` for a complete list of all the ``workspace`` attributes.

Security Summary
~~~~~~~~~~~~~~~~

* Requires Authentication: ``true``
* Entitlements Required: ``workspace_create``

URI Parameters
~~~~~~~~~~~~~~

* ``oid`` (required): the id of the :ref:`org-object`

HTTP Request Body Parameters
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

A :ref:`workspace-object` object

Example Request
~~~~~~~~~~~~~~~

.. code-block:: bash

	curl "https://uforge.example.com/api/orgs/{oid}/workspaces" -X POST \
	-u USER_LOGIN:PASSWORD -H "Accept: application/xml" --data-binary "@representation.xml"

Example of representation.xml content (the request body):

.. code-block:: xml

	<ns0:workspace xmlns:ns0="http://www.usharesoft.com/uforge">
		<name>Workspace Example</name>
	</ns0:workspace>


.. seealso::

	 * :ref:`workspacemembers-api-resources`
	 * :ref:`workspacetemplate-api-resources`
	 * :ref:`workspacecomments-api-resources`
	 * :ref:`workspace-object`
	 * :ref:`workspace-getAll`
	 * :ref:`workspace-get`
	 * :ref:`workspace-delete`
	 * :ref:`userWorkspace-getAll`
	 * :ref:`userWorkspace-create`
