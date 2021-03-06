discid API
==========

.. automodule:: discid
   :synopsis: Python binding of Libdiscid

At the module level there is one constant available:

.. autodata:: DEFAULT_DEVICE
   :novalue:


DiscId object
-------------

The user is expected to create a :class:`DiscId` object,
feed it with some type of TOC and extract the generated information.

.. autoclass:: DiscId
   :undoc-members:


   You should use :func:`read` or :func:`put` before getting
   any data from an object of this class:

   .. automethod:: read
   .. automethod:: put


   When the a TOC was successfully populated,
   you can access the informational attributes:

   .. autoattribute:: id
   .. autoattribute:: submission_url
   .. autoattribute:: first_track_num
   .. autoattribute:: last_track_num
   .. autoattribute:: sectors
   .. autoattribute:: track_offsets


   After you are done with the object,
   you should free the memory allocated for it:

   .. automethod:: free


The discid module includes a custom exception to handle specific problems:

.. autoexception:: DiscError
   :show-inheritance:
