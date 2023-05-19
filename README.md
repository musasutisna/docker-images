<h1 align="center">docker-images</h1>

<p align="center">
  Collections of docker image projects.
</p>

## Geoserver 1.0.0
GeoServer is a Java-based server that allows users to view and edit geospatial data. Using open standards set forth by the Open Geospatial Consortium (OGC), GeoServer allows for great flexibility in map creation and data sharing.

#### Arguments
| Name | Default Value |
| :- | :- |
| TOMCAT_VERSION | 9.0.74 |
| GS_VERSION | 2.23.0 |
| GS_DATA_PATH | ./geoserver_data/ |
| ADDITIONAL_LIBS_PATH | ./additional_libs/ |
| ADDITIONAL_FONTS_PATH | ./additional_fonts/ |
| CORS_ENABLED | false |
| CORS_ALLOWED_ORIGINS | * |
| CORS_ALLOWED_METHODS | GET,POST,PUT,DELETE,HEAD,OPTIONS |
| CORS_ALLOWED_HEADERS | * |
| WAR_ZIP_URL | https://downloads.sourceforge.net/project/geoserver/GeoServer/${GS_VERSION}/geoserver-${GS_VERSION}-war.zip |
| STABLE_PLUGIN_URL | https://downloads.sourceforge.net/project/geoserver/GeoServer/${GS_VERSION}/extensions |
| COMMUNITY_PLUGIN_URL | '' |

#### Environment variables
| Name | Default Value |
| :- | :- |
| CATALINA_HOME | /opt/apache-tomcat-${TOMCAT_VERSION} |
| GEOSERVER_VERSION | $GS_VERSION |
| GEOSERVER_DATA_DIR | /opt/geoserver_data/ |
| GEOSERVER_REQUIRE_FILE | $GEOSERVER_DATA_DIR/global.xml |
| GEOSERVER_LIB_DIR | $CATALINA_HOME/webapps/geoserver/WEB-INF/lib/ |
| EXTRA_JAVA_OPTS | "-Xms256m -Xmx1g" |
| CORS_ENABLED | $CORS_ENABLED |
| CORS_ALLOWED_ORIGINS | $CORS_ALLOWED_ORIGINS |
| CORS_ALLOWED_METHODS | $CORS_ALLOWED_METHODS |
| CORS_ALLOWED_HEADERS | $CORS_ALLOWED_HEADERS |
| DEBIAN_FRONTEND | noninteractive |
| INSTALL_EXTENSIONS | false |
| WAR_ZIP_URL | $WAR_ZIP_URL |
| STABLE_EXTENSIONS | '' |
| STABLE_PLUGIN_URL | $STABLE_PLUGIN_URL |
| COMMUNITY_EXTENSIONS | '' |
| COMMUNITY_PLUGIN_URL | $COMMUNITY_PLUGIN_URL |
| ADDITIONAL_LIBS_DIR | /opt/additional_libs/ |
| ADDITIONAL_FONTS_DIR | /opt/additional_fonts/ |
| SKIP_DEMO_DATA | false |
| ROOT_WEBAPP_REDIRECT | false |
| CATALINA_OPTS | $EXTRA_JAVA_OPTS -Djava.awt.headless=true -server -Dfile.encoding=UTF-8 -Djavax.servlet.request.encoding=UTF-8 -Djavax.servlet.response.encoding=UTF-8 -D-XX:SoftRefLRUPolicyMSPerMB=36000 -Xbootclasspath/a:$CATALINA_HOME/lib/marlin.jar -Dsun.java2d.renderer=org.marlin.pisces.PiscesRenderingEngine -Dorg.geotools.coverage.jaiext.enabled=true |
