[![CircleCI](https://circleci.com/gh/greenbone/ospd/tree/master.svg?style=svg)](https://circleci.com/gh/greenbone/ospd/tree/master)

About OSPD
----------

OSPD is a base class for scanner wrappers which share the same communication
protocol: OSP (Open Scanner Protocol). OSP creates a unified interface for
different security scanners and make their control flow and scan results
consistently available under the central Greenbone Vulnerability Manager service.

OSP is similar in many ways to GMP (Greenbone Management Protocol): XML-based,
stateless and non-permanent connection.

The design supports wrapping arbitrary scanners with same protocol OSP,
sharing the core daemon options while adding scanner specific parameters and
options.

OSPD is licensed under GNU General Public License Version 2 or
any later version.  Please see file COPYING for details.

All parts of OSPD are Copyright (C) by Greenbone Networks GmbH
(see http://www.greenbone.net).


How to write your own OSP Scanner Wrapper
-----------------------------------------

As a core you need to derive from the class OSPDaemon from ospd.py.
See the documentation there for the single steps to establish the
full wrapper.

See the file INSTALL about how to register a OSP scanner at
the Greenbone Vulnerability Manager which will automatically establish a full
GUI integration for the Greenbone Security Assistant (GSA).

There are some online resources about this topic:
http://docs.greenbone.net/GSM-Manual/gos-3.1/en/osp.html#how-to-write-your-own-osp-wrapper


Module structure
----------------

* ospd/ospd.py:       Core OSP Daemon class.
* ospd/misc.py:       Miscellaneous code and classes related to OSPD.
* ospd/ospd_ssh.py:   OSP Daemon class for simple remote SSH-based command execution.
* ospd/win_socket.py: Network class/functions for running a OSP daemon on Windows systems.
