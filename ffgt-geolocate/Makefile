include $(TOPDIR)/rules.mk

PKG_NAME:=ffgt-geolocate
PKG_VERSION:=2
PKG_RELEASE:=1

PKG_BUILD_DIR := $(BUILD_DIR)/$(PKG_NAME)

include $(INCLUDE_DIR)/package.mk

define Package/ffgt-geolocate
  SECTION:=gluon
  CATEGORY:=Gluon
  DEPENDS:=+gluon-core +gluon-cron
  TITLE:=Assist geolocating the node and survey the wifi spectrum
endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/ffgt-geolocate/install
	$(CP) ./files/* $(1)/
endef

$(eval $(call BuildPackage,ffgt-geolocate))
