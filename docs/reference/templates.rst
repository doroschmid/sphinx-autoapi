Templates
=========

A lot of the power from AutoAPI comes from templates.
We are basically building a mapping from Code to Docs,
and templates let you highly customize the display of said docs.

Structure
---------

Every type of data structure gets its own template.
It uses the form :samp:`{language}/{type}.rst` to find the template to render.
The full search path is:

	* :samp:`{language}/{type}.rst`
	* :samp:`{language}/unknown.rst`
	* :samp:`base/unknown.rst`

So for a .NET Class, this would resolve to:

	* :samp:`{dotnet}/{class}.rst`
	* :samp:`{dotnet}/unknown.rst`
	* :samp:`base/unknown.rst`

We provide :samp:`base/member.rst` as an incredibly basic output of every object::

	.. {language}:{type}:: {name}

Context
-------

Every template will be given a set context that can be access in the templates.
It will contain:

* ``obj``: A Python object derived from :class:`PythonMapperBase`.

This object has a number of standard attributes you can reliably access per language.

.. warning::

	These classes should not be constructed manually.
	They can be reliably accessed through templates only.

Python
~~~~~~

.. autoapiclass:: autoapi.mappers.python.objects.PythonPythonMapper
	:members:

.. autoapiclass:: autoapi.mappers.python.objects.PythonFunction
	:members:
	:show-inheritance:

.. autoapiclass:: autoapi.mappers.python.objects.PythonMethod
	:members:
	:show-inheritance:

.. autoapiclass:: autoapi.mappers.python.objects.PythonData
	:members:
	:show-inheritance:

.. autoapiclass:: autoapi.mappers.python.objects.PythonAttribute
	:members:
	:show-inheritance:

.. autoapiclass:: autoapi.mappers.python.objects.TopLevelPythonMapper
	:members:
	:show-inheritance:

.. autoapiclass:: autoapi.mappers.python.objects.PythonModule
	:members:
	:show-inheritance:

.. autoapiclass:: autoapi.mappers.python.objects.PythonPackage
	:members:
	:show-inheritance:

.. autoapiclass:: autoapi.mappers.python.objects.PythonClass
	:members:
	:show-inheritance:

.. autoapiclass:: autoapi.mappers.python.objects.PythonException
	:members:
	:show-inheritance:

Go
~~~

.. autoapiclass:: autoapi.mappers.go.GoPythonMapper
	:members:

Javascript
~~~~~~~~~~

.. autoapiclass:: autoapi.mappers.javascript.JavaScriptPythonMapper
	:members:

.NET
~~~~

.. autoapiclass:: autoapi.mappers.dotnet.DotNetPythonMapper
	:members:
