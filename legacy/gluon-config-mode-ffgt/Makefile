# Copyright (C) 2012 Nils Schneider <nils at nilsschneider.net>
# This is free software, licensed under the Apache 2.0 license.

include $(TOPDIR)/rules.mk

PKG_NAME:=gluon-config-mode-ffgt
PKG_VERSION:=4

PKG_BUILD_DIR := $(BUILD_DIR)/$(PKG_NAME)

include $(GLUONDIR)/include/package.mk

define Package/gluon-config-mode-ffgt
  SECTION:=gluon
  CATEGORY:=Gluon
  TITLE:=Luci based config mode for user friendly setup of new mesh nodes
  DEPENDS:=+gluon-luci-core +gluon-setup-mode-ffgt +gluon-lock-password +gluon-node-info +gluon-simple-tc
  PROVIDES:=gluon-config-mode
endef

define Package/gluon-config-mode-ffgt/description
	Luci based config mode
endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/gluon-config-mode-ffgt/install
	$(CP) ./files/* $(1)/
endef

define Package/gluon-config-mode-ffgt/postinst
#!/bin/sh
$(call GluonCheckSite,check_site.lua)
endef

$(eval $(call BuildPackage,gluon-config-mode-ffgt))
