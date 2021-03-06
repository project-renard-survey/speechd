Speech Dispatcher Coding Guidelines
===================================

This document describes the coding style used in this repository. All
patches or changes must follow this style. If you have any questions,
please contact the speech dispatcher mailing list.

Coding Style Guidelines for C Code
----------------------------------

The indenting style we use is the same as the linux kernel, with the following exceptions and extensions:

  * Goto statements should not be used unless in very special cases.

  * Function names should be
    * lowercase words separated by underscores.
    * functions which are only implementation details of the given source file
  should be declared as static

  * Variable names
    * global variables should follow the same conventions as functions (e.g.
    `output_modules`)
    * the verbosity of the name of local variables should be appropriate to its
    scope

  * Macro names
    * Macro names should be in uppercase, words separated by underscores
    (e.g. `SPEECHD_OPTION_CB_STR`)

  * Type names
    * New types are defined in mixed uppercase (e.g. MessageType)

If you use
GNU indent 2.2.10 or later, you should run it as follows:

    indent -npro -kr -i8 -ts8 -sob -l80 -ss -ncs -cp1 -il0

For versions of indent earlier than 2.2.10, drop the -il0 from the parameters.

In emacs environment the following can be used (untested):

    (defun speechd-c-mode ()
      "C mode with adjusted defaults for use with Speech Dispatcher."
      (interactive)
      (c-mode)
      (c-set-style "K&R"))
  
Coding Style Guideline for other code
-------------------------------------

Please respect the coding style of the given component.
