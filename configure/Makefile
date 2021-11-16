TOP=..

include $(TOP)/configure/CONFIG

TARGETS = $(CONFIG_TARGETS)
CONFIGS += $(subst ../,,$(wildcard $(CONFIG_INSTALLS)))

CFG += CONFIG_PVXS_VERSION
CFG += CONFIG_PVXS_MODULE
CFG += RULES_PVXS_MODULE

include $(TOP)/configure/RULES

ifdef T_A
install: $(TOP)/configure/CONFIG_SITE.Common.$(T_A)

$(TOP)/configure/CONFIG_SITE.Common.$(T_A): toolchain.c
	$(ECHO) $(PREPROCESS.cpp)
	$(PREPROCESS.cpp)

endif

CLEANS += CONFIG_SITE.Common.*

clean:	clean_toolchain

clean_toolchain:
	$(RM) $(CLEANS)

