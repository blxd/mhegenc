Converts between text notation and ASN.1 for UK Profile MHEG-5. Other profiles may be added.

As encoder, it takes a source file containing an Application or Scene described in the MHEG-5 textual notation and outputs an ASN.1 DER file ready for transmission. It's targeted at the Freeview derived profiles but could be modified for other profiles without too much work.

As decoder, it reproduces the textual notation and can add a few helpful comments too.

### History ###
The nice people at Samsung Electronics created it as a simple in-house tool for testing their Digital TV products. When the DTG test group started creating the conformance tests for the UK profile of MHEG-5, Samsung supplied their compiler for use by all members. Having little time to devote to maintenance, they released the source under the GPL license.

SpongeLava took on the maintenance for a while and provided upgrades for freesat and the NZ profile (testing really). The source has always been available, but working with tar files from the SpongeLava site is a pain, so we've moved the hosting to google code.

### The Downloads ###
The latest versions are available via subversion or tar files from the download tab. You can also get the original SERI (Samsung) provided version.

The binaries package includes the mhegasn.exe convertor used in testing: it converts DER to XER and is needed for the python test scripts in the source package. I can't distribute the source for copyright reasons.

mhegasn.exe is a cygwin executable so the cygwin1.dll is included, mhegenc.exe is mingw so it should run stand-alone.

A summary of changes since the original Samsung version:

  * Use a dynamic buffer to remove 16k restriction on source.
  * Extensions for freesat
  * Use --no-cygwin
  * Expanded support for classes
  * Tests for NZ profile