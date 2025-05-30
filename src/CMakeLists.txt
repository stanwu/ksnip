set(KSNIP_SRCS
	${CMAKE_SOURCE_DIR}/src/main.cpp
	${CMAKE_SOURCE_DIR}/src/backend/config/IConfig.h
	${CMAKE_SOURCE_DIR}/src/backend/config/Config.cpp
	${CMAKE_SOURCE_DIR}/src/backend/config/ConfigOptions.cpp
	${CMAKE_SOURCE_DIR}/src/backend/commandLine/CommandLine.cpp
	${CMAKE_SOURCE_DIR}/src/backend/commandLine/CommandLineCaptureHandler.cpp
	${CMAKE_SOURCE_DIR}/src/backend/commandLine/ICommandLineCaptureHandler.h
	${CMAKE_SOURCE_DIR}/src/backend/imageGrabber/IImageGrabber.h
	${CMAKE_SOURCE_DIR}/src/backend/imageGrabber/AbstractImageGrabber.cpp
	${CMAKE_SOURCE_DIR}/src/backend/imageGrabber/AbstractRectAreaImageGrabber.cpp
	${CMAKE_SOURCE_DIR}/src/backend/uploader/IUploader.h
	${CMAKE_SOURCE_DIR}/src/backend/uploader/UploadHandler.cpp
	${CMAKE_SOURCE_DIR}/src/backend/uploader/IUploadHandler.h
	${CMAKE_SOURCE_DIR}/src/backend/uploader/imgur/IImgurUploader.h
	${CMAKE_SOURCE_DIR}/src/backend/uploader/imgur/ImgurWrapper.cpp
	${CMAKE_SOURCE_DIR}/src/backend/uploader/imgur/ImgurResponse.cpp
	${CMAKE_SOURCE_DIR}/src/backend/uploader/imgur/ImgurUploader.cpp
	${CMAKE_SOURCE_DIR}/src/backend/uploader/imgur/ImgurResponseLogger.cpp
	${CMAKE_SOURCE_DIR}/src/backend/uploader/script/IScriptUploader.h
	${CMAKE_SOURCE_DIR}/src/backend/uploader/script/ScriptUploader.cpp
	${CMAKE_SOURCE_DIR}/src/backend/uploader/ftp/IFtpUploader.h
	${CMAKE_SOURCE_DIR}/src/backend/uploader/ftp/FtpUploader.cpp
	${CMAKE_SOURCE_DIR}/src/backend/saver/SavePathProvider.cpp
	${CMAKE_SOURCE_DIR}/src/backend/saver/ImageSaver.cpp
	${CMAKE_SOURCE_DIR}/src/backend/saver/WildcardResolver.cpp
	${CMAKE_SOURCE_DIR}/src/backend/saver/UniqueNameProvider.cpp
	${CMAKE_SOURCE_DIR}/src/backend/saver/NameProvider.cpp
	${CMAKE_SOURCE_DIR}/src/backend/CapturePrinter.cpp
	${CMAKE_SOURCE_DIR}/src/backend/TranslationLoader.cpp
	${CMAKE_SOURCE_DIR}/src/backend/WatermarkImageLoader.cpp
	${CMAKE_SOURCE_DIR}/src/backend/recentImages/RecentImagesPathStore.cpp
	${CMAKE_SOURCE_DIR}/src/backend/recentImages/ImagePathStorage.cpp
	${CMAKE_SOURCE_DIR}/src/backend/ipc/IpcServer.cpp
	${CMAKE_SOURCE_DIR}/src/backend/ipc/IpcClient.cpp
	${CMAKE_SOURCE_DIR}/src/bootstrapper/BootstrapperFactory.cpp
	${CMAKE_SOURCE_DIR}/src/bootstrapper/StandAloneBootstrapper.cpp
	${CMAKE_SOURCE_DIR}/src/bootstrapper/ImageFromStdInputReader.cpp
	${CMAKE_SOURCE_DIR}/src/bootstrapper/singleInstance/InstanceLock.cpp
	${CMAKE_SOURCE_DIR}/src/bootstrapper/singleInstance/SingleInstanceClientBootstrapper.cpp
	${CMAKE_SOURCE_DIR}/src/bootstrapper/singleInstance/SingleInstanceServerBootstrapper.cpp
	${CMAKE_SOURCE_DIR}/src/bootstrapper/singleInstance/SingleInstanceParameterTranslator.cpp
	${CMAKE_SOURCE_DIR}/src/common/adapter/fileDialog/FileDialogAdapter.cpp
	${CMAKE_SOURCE_DIR}/src/common/helper/MathHelper.cpp
	${CMAKE_SOURCE_DIR}/src/common/helper/PathHelper.cpp
	${CMAKE_SOURCE_DIR}/src/common/helper/FileUrlHelper.cpp
	${CMAKE_SOURCE_DIR}/src/common/helper/RectHelper.cpp
	${CMAKE_SOURCE_DIR}/src/common/helper/EnumTranslator.cpp
	${CMAKE_SOURCE_DIR}/src/common/helper/FileDialogFilterHelper.cpp
	${CMAKE_SOURCE_DIR}/src/common/loader/IconLoader.cpp
	${CMAKE_SOURCE_DIR}/src/common/handler/DelayHandler.cpp
	${CMAKE_SOURCE_DIR}/src/common/handler/IDelayHandler.h
	${CMAKE_SOURCE_DIR}/src/common/provider/ApplicationTitleProvider.cpp
	${CMAKE_SOURCE_DIR}/src/common/provider/NewCaptureNameProvider.cpp
	${CMAKE_SOURCE_DIR}/src/common/provider/PathFromCaptureProvider.cpp
	${CMAKE_SOURCE_DIR}/src/common/provider/scaledSizeProvider/ScaledSizeProvider.cpp
	${CMAKE_SOURCE_DIR}/src/common/provider/TempFileProvider.cpp
	${CMAKE_SOURCE_DIR}/src/common/provider/UsernameProvider.cpp
	${CMAKE_SOURCE_DIR}/src/common/platform/HdpiScaler.cpp
	${CMAKE_SOURCE_DIR}/src/common/platform/PlatformChecker.cpp
	${CMAKE_SOURCE_DIR}/src/common/platform/CommandRunner.cpp
	${CMAKE_SOURCE_DIR}/src/common/provider/directoryPathProvider/DirectoryPathProvider.cpp
	${CMAKE_SOURCE_DIR}/src/dependencyInjector/DependencyInjector.cpp
	${CMAKE_SOURCE_DIR}/src/dependencyInjector/DependencyInjectorBootstrapper.cpp
	${CMAKE_SOURCE_DIR}/src/widgets/CustomToolButton.cpp
	${CMAKE_SOURCE_DIR}/src/widgets/CustomCursor.cpp
	${CMAKE_SOURCE_DIR}/src/widgets/NumericComboBox.cpp
	${CMAKE_SOURCE_DIR}/src/widgets/CustomSpinBox.cpp
	${CMAKE_SOURCE_DIR}/src/widgets/CaptureModePicker.cpp
	${CMAKE_SOURCE_DIR}/src/widgets/ColorButton.cpp
	${CMAKE_SOURCE_DIR}/src/widgets/MainToolBar.cpp
	${CMAKE_SOURCE_DIR}/src/widgets/KeySequenceLineEdit.cpp
	${CMAKE_SOURCE_DIR}/src/widgets/CustomLineEdit.cpp
	${CMAKE_SOURCE_DIR}/src/widgets/ProcessIndicator.cpp
	${CMAKE_SOURCE_DIR}/src/gui/MainWindow.cpp
	${CMAKE_SOURCE_DIR}/src/gui/RecentImagesMenu.cpp
	${CMAKE_SOURCE_DIR}/src/gui/ImgurHistoryDialog.cpp
	${CMAKE_SOURCE_DIR}/src/gui/TrayIcon.cpp
	${CMAKE_SOURCE_DIR}/src/gui/actions/Action.cpp
	${CMAKE_SOURCE_DIR}/src/gui/actions/ActionProcessor.cpp
	${CMAKE_SOURCE_DIR}/src/gui/actions/ActionsMenu.cpp
	${CMAKE_SOURCE_DIR}/src/gui/clipboard/ClipboardAdapter.cpp
	${CMAKE_SOURCE_DIR}/src/gui/clipboard/IClipboard.h
	${CMAKE_SOURCE_DIR}/src/gui/imageAnnotator/KImageAnnotatorAdapter.cpp
	${CMAKE_SOURCE_DIR}/src/gui/imageAnnotator/IImageAnnotator.h
	${CMAKE_SOURCE_DIR}/src/gui/desktopService/DesktopServiceAdapter.cpp
	${CMAKE_SOURCE_DIR}/src/gui/fileService/FileService.cpp
	${CMAKE_SOURCE_DIR}/src/gui/directoryService/DirectoryService.cpp
	${CMAKE_SOURCE_DIR}/src/gui/widgetVisibilityHandler/WidgetVisibilityHandler.cpp
	${CMAKE_SOURCE_DIR}/src/gui/widgetVisibilityHandler/GnomeWaylandWidgetVisibilityHandler.cpp
	${CMAKE_SOURCE_DIR}/src/gui/widgetVisibilityHandler/WidgetVisibilityHandlerFactory.cpp
	${CMAKE_SOURCE_DIR}/src/gui/snippingArea/AbstractSnippingArea.cpp
	${CMAKE_SOURCE_DIR}/src/gui/snippingArea/SnippingAreaAdorner.cpp
	${CMAKE_SOURCE_DIR}/src/gui/snippingArea/AdornerMagnifyingGlass.cpp
	${CMAKE_SOURCE_DIR}/src/gui/snippingArea/AdornerRulers.cpp
	${CMAKE_SOURCE_DIR}/src/gui/snippingArea/AdornerPositionInfo.cpp
	${CMAKE_SOURCE_DIR}/src/gui/snippingArea/AdornerSizeInfo.cpp
	${CMAKE_SOURCE_DIR}/src/gui/snippingArea/SnippingAreaResizer.cpp
	${CMAKE_SOURCE_DIR}/src/gui/snippingArea/SnippingAreaSelector.cpp
	${CMAKE_SOURCE_DIR}/src/gui/snippingArea/SnippingAreaSelectorInfoText.cpp
	${CMAKE_SOURCE_DIR}/src/gui/snippingArea/SnippingAreaResizerInfoText.cpp
	${CMAKE_SOURCE_DIR}/src/gui/snippingArea/AbstractSnippingAreaInfoText.cpp
	${CMAKE_SOURCE_DIR}/src/gui/settingsDialog/AnnotationSettings.cpp
	${CMAKE_SOURCE_DIR}/src/gui/settingsDialog/ApplicationSettings.cpp
	${CMAKE_SOURCE_DIR}/src/gui/settingsDialog/ImageGrabberSettings.cpp
	${CMAKE_SOURCE_DIR}/src/gui/settingsDialog/HotKeySettings.cpp
	${CMAKE_SOURCE_DIR}/src/gui/settingsDialog/SaverSettings.cpp
	${CMAKE_SOURCE_DIR}/src/gui/settingsDialog/StickerSettings.cpp
	${CMAKE_SOURCE_DIR}/src/gui/settingsDialog/SnippingAreaSettings.cpp
	${CMAKE_SOURCE_DIR}/src/gui/settingsDialog/SettingsDialog.cpp
	${CMAKE_SOURCE_DIR}/src/gui/settingsDialog/SettingsFilter.cpp
	${CMAKE_SOURCE_DIR}/src/gui/settingsDialog/TrayIconSettings.cpp
	${CMAKE_SOURCE_DIR}/src/gui/settingsDialog/WatermarkSettings.cpp
	${CMAKE_SOURCE_DIR}/src/gui/settingsDialog/actions/ActionsSettings.cpp
	${CMAKE_SOURCE_DIR}/src/gui/settingsDialog/actions/ActionSettingTab.cpp
	${CMAKE_SOURCE_DIR}/src/gui/settingsDialog/actions/EmptyActionSettingTab.cpp
	${CMAKE_SOURCE_DIR}/src/gui/settingsDialog/uploader/UploaderSettings.cpp
	${CMAKE_SOURCE_DIR}/src/gui/settingsDialog/uploader/ImgurUploaderSettings.cpp
	${CMAKE_SOURCE_DIR}/src/gui/settingsDialog/uploader/ScriptUploaderSettings.cpp
	${CMAKE_SOURCE_DIR}/src/gui/settingsDialog/uploader/FtpUploaderSettings.cpp
	${CMAKE_SOURCE_DIR}/src/gui/settingsDialog/plugins/PluginsSettings.cpp
	${CMAKE_SOURCE_DIR}/src/gui/aboutDialog/AboutDialog.cpp
	${CMAKE_SOURCE_DIR}/src/gui/aboutDialog/AboutTab.cpp
	${CMAKE_SOURCE_DIR}/src/gui/aboutDialog/VersionTab.cpp
	${CMAKE_SOURCE_DIR}/src/gui/aboutDialog/AuthorTab.cpp
	${CMAKE_SOURCE_DIR}/src/gui/aboutDialog/DonateTab.cpp
	${CMAKE_SOURCE_DIR}/src/gui/aboutDialog/ContactTab.cpp
	${CMAKE_SOURCE_DIR}/src/gui/globalHotKeys/GlobalHotKey.cpp
	${CMAKE_SOURCE_DIR}/src/gui/globalHotKeys/NativeKeyEventFilter.cpp
	${CMAKE_SOURCE_DIR}/src/gui/globalHotKeys/GlobalHotKeyHandler.cpp
	${CMAKE_SOURCE_DIR}/src/gui/globalHotKeys/HotKeyMap.cpp
	${CMAKE_SOURCE_DIR}/src/gui/globalHotKeys/keyHandler/DummyKeyHandler.cpp
	${CMAKE_SOURCE_DIR}/src/gui/globalHotKeys/keyHandler/KeyHandlerFactory.cpp
	${CMAKE_SOURCE_DIR}/src/gui/notificationService/NotificationServiceFactory.cpp
	${CMAKE_SOURCE_DIR}/src/gui/operations/SaveOperation.cpp
	${CMAKE_SOURCE_DIR}/src/gui/operations/RenameOperation.cpp
	${CMAKE_SOURCE_DIR}/src/gui/operations/AddWatermarkOperation.cpp
	${CMAKE_SOURCE_DIR}/src/gui/operations/UpdateWatermarkOperation.cpp
	${CMAKE_SOURCE_DIR}/src/gui/operations/WatermarkImagePreparer.cpp
	${CMAKE_SOURCE_DIR}/src/gui/operations/CanDiscardOperation.cpp
	${CMAKE_SOURCE_DIR}/src/gui/operations/UploadOperation.cpp
	${CMAKE_SOURCE_DIR}/src/gui/operations/HandleUploadResultOperation.cpp
	${CMAKE_SOURCE_DIR}/src/gui/operations/NotifyOperation.cpp
	${CMAKE_SOURCE_DIR}/src/gui/operations/DeleteImageOperation.cpp
	${CMAKE_SOURCE_DIR}/src/gui/operations/CopyAsDataUriOperation.cpp
	${CMAKE_SOURCE_DIR}/src/gui/operations/LoadImageFromFileOperation.cpp
	${CMAKE_SOURCE_DIR}/src/gui/captureHandler/CaptureTabStateHandler.cpp
	${CMAKE_SOURCE_DIR}/src/gui/captureHandler/ICaptureTabStateHandler.h
	${CMAKE_SOURCE_DIR}/src/gui/captureHandler/CaptureHandlerFactory.cpp
	${CMAKE_SOURCE_DIR}/src/gui/captureHandler/SingleCaptureHandler.cpp
	${CMAKE_SOURCE_DIR}/src/gui/captureHandler/MultiCaptureHandler.cpp
	${CMAKE_SOURCE_DIR}/src/gui/captureHandler/TabContextMenuAction.cpp
	${CMAKE_SOURCE_DIR}/src/gui/modelessWindows/IModelessWindow.h
	${CMAKE_SOURCE_DIR}/src/gui/modelessWindows/IModelessWindowCreator.h
	${CMAKE_SOURCE_DIR}/src/gui/modelessWindows/ModelessWindowHandler.cpp
	${CMAKE_SOURCE_DIR}/src/gui/modelessWindows/pinWindow/PinWindow.cpp
	${CMAKE_SOURCE_DIR}/src/gui/modelessWindows/pinWindow/PinWindowCreator.cpp
	${CMAKE_SOURCE_DIR}/src/gui/modelessWindows/pinWindow/PinWindowHandler.cpp
	${CMAKE_SOURCE_DIR}/src/gui/modelessWindows/ocrWindow/OcrWindow.cpp
	${CMAKE_SOURCE_DIR}/src/gui/modelessWindows/ocrWindow/OcrWindowCreator.cpp
	${CMAKE_SOURCE_DIR}/src/gui/modelessWindows/ocrWindow/OcrWindowHandler.cpp
	${CMAKE_SOURCE_DIR}/src/gui/messageBoxService/MessageBoxService.cpp
	${CMAKE_SOURCE_DIR}/src/gui/windowResizer/WindowResizer.cpp
	${CMAKE_SOURCE_DIR}/src/gui/dragAndDrop/DragAndDropProcessor.cpp
	${CMAKE_SOURCE_DIR}/src/logging/LogOutputHandler.cpp
	${CMAKE_SOURCE_DIR}/src/logging/ConsoleLogger.cpp
	${CMAKE_SOURCE_DIR}/src/logging/NoneLogger.cpp
	${CMAKE_SOURCE_DIR}/src/plugins/PluginInfo.cpp
	${CMAKE_SOURCE_DIR}/src/plugins/IPluginManager.h
	${CMAKE_SOURCE_DIR}/src/plugins/PluginManager.cpp
	${CMAKE_SOURCE_DIR}/src/plugins/PluginFinder.cpp
	${CMAKE_SOURCE_DIR}/src/plugins/PluginLoader.cpp
	)

if (APPLE)
        list(APPEND KSNIP_SRCS
                ${CMAKE_SOURCE_DIR}/src/backend/imageGrabber/MacImageGrabber.cpp
                ${CMAKE_SOURCE_DIR}/src/backend/imageGrabber/MacWrapper.cpp
                ${CMAKE_SOURCE_DIR}/src/backend/config/MacConfig.cpp
                ${CMAKE_SOURCE_DIR}/src/gui/snippingArea/MacSnippingArea.cpp
                ${CMAKE_SOURCE_DIR}/src/gui/globalHotKeys/keyHandler/MacKeyHandler.cpp
                ${CMAKE_SOURCE_DIR}/src/gui/globalHotKeys/KeySequenceToMacKeyCodeTranslator.cpp
				${CMAKE_SOURCE_DIR}/src/plugins/searchPathProvider/MacPluginSearchPathProvider.cpp
                )
elseif (UNIX)
        list(APPEND KSNIP_SRCS
                ${CMAKE_SOURCE_DIR}/src/backend/imageGrabber/BaseX11ImageGrabber.cpp
                ${CMAKE_SOURCE_DIR}/src/backend/imageGrabber/X11ImageGrabber.cpp
                ${CMAKE_SOURCE_DIR}/src/backend/imageGrabber/GnomeX11ImageGrabber.cpp
                ${CMAKE_SOURCE_DIR}/src/backend/imageGrabber/KdeWaylandImageGrabber.cpp
                ${CMAKE_SOURCE_DIR}/src/backend/imageGrabber/X11Wrapper.cpp
                ${CMAKE_SOURCE_DIR}/src/backend/imageGrabber/GnomeX11Wrapper.cpp
                ${CMAKE_SOURCE_DIR}/src/backend/imageGrabber/GnomeWaylandImageGrabber.cpp
                ${CMAKE_SOURCE_DIR}/src/backend/imageGrabber/WaylandImageGrabber.cpp
                ${CMAKE_SOURCE_DIR}/src/backend/config/WaylandConfig.cpp
                ${CMAKE_SOURCE_DIR}/src/common/adapter/fileDialog/SnapFileDialogAdapter.cpp
                ${CMAKE_SOURCE_DIR}/src/common/provider/directoryPathProvider/SnapDirectoryPathProvider.cpp
                ${CMAKE_SOURCE_DIR}/src/common/provider/scaledSizeProvider/GnomeScaledSizeProvider.cpp
                ${CMAKE_SOURCE_DIR}/src/gui/snippingArea/X11SnippingArea.cpp
                ${CMAKE_SOURCE_DIR}/src/gui/snippingArea/WaylandSnippingArea.cpp
                ${CMAKE_SOURCE_DIR}/src/gui/globalHotKeys/keyHandler/X11KeyHandler.cpp
                ${CMAKE_SOURCE_DIR}/src/gui/globalHotKeys/KeySequenceToX11KeyCodeTranslator.cpp
                ${CMAKE_SOURCE_DIR}/src/gui/globalHotKeys/X11ErrorLogger.cpp
                ${CMAKE_SOURCE_DIR}/src/gui/notificationService/FreeDesktopNotificationService.cpp
                ${CMAKE_SOURCE_DIR}/src/gui/notificationService/KdeDesktopNotificationService.cpp
                ${CMAKE_SOURCE_DIR}/src/gui/desktopService/SnapDesktopServiceAdapter.cpp
                ${CMAKE_SOURCE_DIR}/src/plugins/searchPathProvider/LinuxPluginSearchPathProvider.cpp
                )
elseif (WIN32)
        list(APPEND KSNIP_SRCS
                ${CMAKE_SOURCE_DIR}/src/backend/imageGrabber/WinImageGrabber.cpp
                ${CMAKE_SOURCE_DIR}/src/backend/imageGrabber/WinWrapper.cpp
                ${CMAKE_SOURCE_DIR}/src/gui/snippingArea/WinSnippingArea.cpp
                ${CMAKE_SOURCE_DIR}/src/gui/globalHotKeys/keyHandler/WinKeyHandler.cpp
                ${CMAKE_SOURCE_DIR}/src/gui/globalHotKeys/KeySequenceToWinKeyCodeTranslator.cpp
                ${CMAKE_SOURCE_DIR}/src/gui/modelessWindows/ocrWindow/WinOcrWindow.cpp
                ${CMAKE_SOURCE_DIR}/src/gui/modelessWindows/ocrWindow/WinOcrWindowCreator.cpp
				${CMAKE_SOURCE_DIR}/src/plugins/WinPluginLoader.cpp
				${CMAKE_SOURCE_DIR}/src/plugins/searchPathProvider/WinPluginSearchPathProvider.cpp
				)
endif ()

# Set the sources variable in the top-level as well, since the tests/
# directory wants to (re)build as well.
set(KSNIP_SRCS ${KSNIP_SRCS} PARENT_SCOPE)

if (WIN32)
        set(CPACK_GENERATOR WIX)
        set(CPACK_PACKAGE_NAME "ksnip")
        set(CPACK_PACKAGE_VENDOR "ksnip")
        set(CPACK_WIX_UPGRADE_GUID "4c7ed545-c0dd-4d45-bf69-c29c7998f668")
        set(CPACK_PACKAGE_DESCRIPTION_SUMMARY "Cross-platform screenshot tool that provides many annotation features for your screenshots.")
        set(CPACK_PACKAGE_VERSION "${PROJECT_VERSION}")
        set(CPACK_PACKAGE_INSTALL_DIRECTORY "ksnip")
        set(CPACK_RESOURCE_FILE_LICENSE "${CMAKE_SOURCE_DIR}/LICENSE.txt")
        set(CPACK_WIX_PRODUCT_ICON "${CMAKE_SOURCE_DIR}/icons/ksnip.ico")

        INCLUDE(CPack)

        add_executable(ksnip ${KSNIP_SRCS} ${CMAKE_SOURCE_DIR}/icons/ksnip_icons.qrc ${CMAKE_SOURCE_DIR}/icons/ksnip_windows_icon.rc)
elseif (APPLE)
        set(MACOSX_BUNDLE_EXECUTABLE_NAME "ksnip")
        set(MACOSX_BUNDLE_GUI_IDENTIFIER "org.ksnip.ksnip")
        set(MACOSX_BUNDLE_ICON_FILE "ksnip.icns")
        set(MACOSX_BUNDLE_INFO_STRING "Cross-Platform Screenshot and Annotation Tool")
        set(MACOSX_BUNDLE_SHORT_VERSION_STRING ${PROJECT_VERSION})
        set(MACOSX_BUNDLE_LONG_VERSION_STRING ${KSNIP_VERSION})
        set(MACOSX_BUNDLE_BUNDLE_VERSION ${PROJECT_VERSION})

        set(MACOSX_ICON ${CMAKE_SOURCE_DIR}/icons/ksnip.icns)
        set_source_files_properties(${MACOSX_ICON} PROPERTIES MACOSX_PACKAGE_LOCATION "Resources")

        add_executable(ksnip MACOSX_BUNDLE ${KSNIP_SRCS} ${CMAKE_SOURCE_DIR}/icons/ksnip_icons.qrc ${MACOSX_ICON})
else ()
        add_executable(ksnip ${KSNIP_SRCS} ${CMAKE_SOURCE_DIR}/icons/ksnip_icons.qrc)
endif ()

set(DEPENDENCY_LIBRARIES
        Qt${QT_MAJOR_VERSION}::Widgets
        Qt${QT_MAJOR_VERSION}::Network
        Qt${QT_MAJOR_VERSION}::Xml
        Qt${QT_MAJOR_VERSION}::PrintSupport
        Qt${QT_MAJOR_VERSION}::Svg
        )

if (BUILD_WITH_QT6)
        list(APPEND DEPENDENCY_LIBRARIES Qt6::GuiPrivate)
elseif (UNIX AND NOT APPLE)
        list(APPEND DEPENDENCY_LIBRARIES Qt5::X11Extras)
endif ()

if (APPLE)
        list(APPEND DEPENDENCY_LIBRARIES
                kImageAnnotator::kImageAnnotator
                kColorPicker::kColorPicker
                "-framework CoreGraphics -framework AppKit"
                )
elseif (UNIX)
        list(APPEND DEPENDENCY_LIBRARIES
                Qt${QT_MAJOR_VERSION}::DBus
                kImageAnnotator::kImageAnnotator
                kColorPicker::kColorPicker
                XCB::XFIXES
                )

        # X11::X11 imported target only available with sufficiently new CMake
        if (CMAKE_VERSION VERSION_GREATER_EQUAL 3.14.0)
                list(APPEND DEPENDENCY_LIBRARIES X11::X11)
        else()
                list(APPEND DEPENDENCY_LIBRARIES X11)
        endif()

        # This is the "UNIX AND NOT APPLE" case, which is the Free Desktop
        # world: Linux and the BSDs and Illumos. To simplify #ifdefs in
        # the source, add a UNIX_X11 defined to be used instead of __linux__ etc.
        # While the "X11" part of the define isn't necessarily accurate,
        # it is easy to spot.
        target_compile_definitions(ksnip PRIVATE UNIX_X11)
elseif (WIN32)
        list(APPEND DEPENDENCY_LIBRARIES
                Qt${QT_MAJOR_VERSION}::WinExtras
				kImageAnnotator::kImageAnnotator
                kColorPicker
                Dwmapi
                )
endif ()

target_link_libraries(ksnip ${DEPENDENCY_LIBRARIES})

# install target
if (WIN32)
        install(TARGETS ksnip RUNTIME DESTINATION .)

        find_program(WINDEPLOYQT windeployqt HINTS $ENV{QTDIR} PATH_SUFFIXES bin)
        SET(WINDEPLOYQT_PARAMETERS "--no-opengl-sw --no-system-d3d-compiler --no-compiler-runtime --release")
        install(CODE "execute_process(COMMAND ${WINDEPLOYQT} ${WINDEPLOYQT_PARAMETERS} . WORKING_DIRECTORY \${CMAKE_INSTALL_PREFIX})")

        find_program(COPY cp)

        if (DEFINED ENV{OPENSSL_DIR})
                file(TO_CMAKE_PATH "$ENV{OPENSSL_DIR}" OPENSSL_DIR)
                install(CODE "execute_process(COMMAND ${COPY} ${OPENSSL_DIR}/*.dll \${CMAKE_INSTALL_PREFIX})")
        else ()
                message("OPENSSL_DIR not set, not able to install openssl dependencies, skipping.")
        endif()

        if (DEFINED ENV{COMPILE_RUNTIME_DIR})
                file(TO_CMAKE_PATH "$ENV{COMPILE_RUNTIME_DIR}" COMPILE_RUNTIME_DIR)
                install(CODE "execute_process(COMMAND ${COPY} ${COMPILE_RUNTIME_DIR}/*.dll \${CMAKE_INSTALL_PREFIX})")
        else ()
                message("COMPILE_RUNTIME_DIR not set, not able to install compile runtime dependencies, skipping.")
        endif()

        if (DEFINED ENV{KIMAGEANNOTATOR_DIR})
                file(TO_CMAKE_PATH "$ENV{KIMAGEANNOTATOR_DIR}" KIMAGEANNOTATOR_DIR)
                install(CODE "execute_process(COMMAND ${COPY} -r \"${KIMAGEANNOTATOR_DIR}/${KIMAGEANNOTATOR_LANG_INSTALL_DIR}\" \${CMAKE_INSTALL_PREFIX})")
        else ()
                message("KIMAGEANNOTATOR_DIR not set, not able to install kImageAnnotator translations, skipping.")
        endif()

        set_property(INSTALL "ksnip.exe"
                PROPERTY CPACK_START_MENU_SHORTCUTS "ksnip Screenshot Tool"
        )
elseif (UNIX AND NOT APPLE)
        install(TARGETS ksnip RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR})
else ()
        message("DEBUG: NOT WIN32, NOT UNIX")
endif ()

# uninstall target
if (UNIX AND NOT APPLE)
        if(NOT TARGET uninstall)
                configure_file(
                                "${CMAKE_CURRENT_SOURCE_DIR}/../cmake/cmake_uninstall.cmake.in"
                                "${CMAKE_CURRENT_BINARY_DIR}/cmake_uninstall.cmake"
                                IMMEDIATE @ONLY)

                add_custom_target(uninstall COMMAND ${CMAKE_COMMAND} -P ${CMAKE_CURRENT_BINARY_DIR}/cmake_uninstall.cmake)
        endif ()
endif ()
