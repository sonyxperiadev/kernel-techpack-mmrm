MMRM_ROOT := $(srctree)/techpack/mmrm

include $(MMRM_ROOT)/config/waipiommrm.conf
LINUXINCLUDE += -include $(MMRM_ROOT)/config/waipiommrmconf.h

ifneq ($(CONFIG_ARCH_QTI_VM), y)

obj-y += driver/

ifeq ($(CONFIG_MSM_MMRM_VM),y)
LINUXINCLUDE += -I$(MMRM_ROOT)/vm/common/inc/
obj-y += vm/be/
endif

else

LINUXINCLUDE += -I$(MMRM_ROOT)/vm/common/inc/

obj-y += vm/fe/
obj-y += vm/fe/vm_test/

endif
