SET (DB_MANAGER_POSTGIS_DIR ${DB_MANAGER_PLUGIN_DIR}/db_plugins/postgis)

FILE(GLOB PY_FILES *.py)
FILE(GLOB ICON_FILES icons/*.png)

PYQT4_ADD_RESOURCES(PYRC_FILES resources.qrc)
ADD_CUSTOM_TARGET(db_manager_postgis ALL DEPENDS ${PYRC_FILES})

INSTALL(FILES ${PY_FILES} DESTINATION ${DB_MANAGER_POSTGIS_DIR})
INSTALL(FILES ${PYRC_FILES} DESTINATION ${DB_MANAGER_POSTGIS_DIR})
INSTALL(FILES ${ICON_FILES} DESTINATION ${DB_MANAGER_POSTGIS_DIR}/icons)

ADD_SUBDIRECTORY(plugins)
