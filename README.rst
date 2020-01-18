===================================================================
Simple CLI utility to append one or more PDFs at the end of another
===================================================================

This is a thin wrapper around pypdf2.

::

    pdfappend base_document.pdf [document_to_append.pdf ...]

If no document to append is specified, ``tmp.pdf`` is assumed.  The base
document is replaced in place and ``tmp.pdf`` (or the specified
documents to append) are deleted.

License
=======

© 2020 Antonis Christofides

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.

Creating a Windows executable
=============================

On Windows; the first time:

 1. Install ``git``.
 2. Install a recent Python 3 version.
 3. Execute Git Bash.
 4. Clone pdfappend.
 5. Change to the working directory of ``pdfappend``.
 6. ``pip install virtualenv``
 7. ``virtualenv ../venv``
 8. ``../venv/Scripts/pip install -r requirements.txt``
 9. ``../venv/Scripts/pip install pyinstaller``

Next times:

 1. ``rm -r dist build pdfappend.spec``
 2. ``../venv/Scripts/pyinstaller --onefile --name=pdfappend pdfappend``

After this, ``pdfappend.exe`` should be in the ``dist`` directory.
