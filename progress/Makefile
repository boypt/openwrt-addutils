#
# Copyright (C) 2009-2011 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=progress
PKG_VERSION:=0.9
PKG_RELEASE:=1

https://github.com/Xfennec/progress/archive/v0.9.tar.gz

PKG_SOURCE:=v$(PKG_VERSION).tar.gz
PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_URL:=https://github.com/Xfennec/progress/archive/
PKG_MD5SUM:=

include $(INCLUDE_DIR)/package.mk

define Package/progress
	SECTION:=utils
	CATEGORY:=Utilities
	TITLE:=Coreutils Progress Viewer (formerly known as cv)
	URL:=https://github.com/Xfennec/progress
	DEPENDS:=+libncurses
endef

define Package/progress/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/$(PKG_NAME) $(1)/usr/bin/
endef

$(eval $(call BuildPackage,progress))
