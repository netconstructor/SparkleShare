ASSEMBLY = SparkleLib
TARGET = library

ASSEMBLY_INFO_SOURCE = Defines.cs

SOURCES =  \
	Defines.cs \
	SparkleAnnouncement.cs \
	SparkleBackend.cs \
	SparkleConfig.cs \
	SparkleExceptions.cs \
	SparkleExtensions.cs \
	SparkleFetcherBase.cs \
	SparkleHelpers.cs \
	SparkleListenerBase.cs \
	SparkleListenerFactory.cs \
	SparkleListenerTcp.cs \
	SparkleRepoBase.cs \
	SparkleUser.cs \
	SparkleWatcher.cs \
	SparkleWrappers.cs


install-data-hook:
	for ASM in $(EXTRA_BUNDLE); do \
		$(INSTALL) -m 0755 $$ASM $(DESTDIR)$(moduledir); \
	done;

uninstall-hook:
	for ASM in $(EXTRA_BUNDLE); do \
		rm -f $(DESTDIR)$(moduledir)/`basename $$ASM`; \
	done;

include $(top_srcdir)/build/build.mk
