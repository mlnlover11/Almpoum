ARCHS = armv7 armv7s arm64
CFLAGS = -fobjc-arc

include $(THEOS)/makefiles/common.mk

BUNDLE_NAME = AlmpoumSettings
AlmpoumSettings_FILES := AlmpoumSettings.mm $(shell find $(THEOS)/include/SettingsKit -name '*.m')
AlmpoumSettings_INSTALL_PATH = /Library/PreferenceBundles
AlmpoumSettings_FRAMEWORKS = UIKit MessageUI Social QuartzCore CoreGraphics
AlmpoumSettings_PRIVATE_FRAMEWORKS = Preferences

include $(THEOS_MAKE_PATH)/bundle.mk

internal-stage::
	$(ECHO_NOTHING)cp $(THEOS)/include/SettingsKit/Resources/*.png $(THEOS_STAGING_DIR)/Library/PreferenceBundles/AlmpoumSettings.bundle/$(ECHO_END)
	$(ECHO_NOTHING)mkdir -p $(THEOS_STAGING_DIR)/Library/PreferenceLoader/Preferences$(ECHO_END)
	$(ECHO_NOTHING)cp entry.plist $(THEOS_STAGING_DIR)/Library/PreferenceLoader/Preferences/AlmpoumSettings.plist$(ECHO_END)
