   .. data:: delete.writeConcernError.code

     An integer value identifying the cause of the write concern error.

   .. data:: delete.writeConcernError.errmsg

     A description of the cause of the write concern error.

   .. data:: delete.writeConcernError.errInfo.writeConcern

     A document containing information on the write concern used for
     the operation.

     .. data:: delete.writeConcernError.errInfo.writeConcern.w

        An integer value indicating the number of nodes to which
        the operation must propagate.

     .. data:: delete.writeConcernError.errInfo.writeConcern.wtimeout

        An integer value indicating the time limit in milliseconds for
        the write concern.

     .. data:: delete.writeConcernError.errInfo.writeConcern.provenance

        A string value indicating where the write concern originated.
        The following table shows the possible values for this field
        and their significance:

        .. list-table::
           :header-rows: 1
           :widths: 20 40

           * - Value
             - Significance

           * - ``clientSupplied``
             - The write concern was specified in the application.

           * - ``customDefault``
             - The write concern originated from a custom defined
               default value. See :dbcommand:`setDefaultRWConcern`.

           * - ``getLastErrorDefaults``
             - The write concern originated from the replica set's
               :rsconf:`settings.getLastErrorDefaults` field.

           * - ``implicitDefault``
             - The write concern originated from the server in absence
               of all other write concern specifications.
