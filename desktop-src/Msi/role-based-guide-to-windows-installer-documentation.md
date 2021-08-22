---
description: Windows El instalador es la solución recomendada para la instalación y configuración de aplicaciones en Windows.
ms.assetid: 13f41020-5275-44cd-b26b-f45483700d8a
title: Guía basada en roles para la documentación Windows instalador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029f886050f3bb0256f6f0f993e613be940cee9cd2fe748b2d17b5dc0f0f84a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625867"
---
# <a name="role-based-guide-to-windows-installer-documentation"></a>Guía basada en roles para la documentación Windows instalador

Windows El instalador es la solución recomendada para la instalación y configuración de aplicaciones en Windows. Por lo tanto, parte de la información contenida en este SDK será de interés para una amplia gama de profesionales de DESARROLLO de software y DE. Esta sección se proporciona como guía para los lectores que prefieren ver vínculos a temas organizados por roles profesionales y escenarios de tareas comunes. Dado que los roles pueden diferir en gran medida entre organizaciones, la siguiente agrupación solo debe considerarse como una guía para una ubicación para empezar a buscar la información que necesita.

-   [Desarrolladores de aplicaciones](#application-developers)
-   [Autores de la instalación](#setup-authors)
-   [Profesionales de TI](#it-professionals)
-   [Desarrolladores de infraestructura](#infrastructure-developers)

Esta documentación está pensada para desarrolladores de software que desean crear aplicaciones que usan Windows Installer. Como origen principal del material de referencia para el instalador, el SDK proporciona información sobre los paquetes de instalación y el servicio de instalador. Contiene descripciones completas de la interfaz de programación de aplicaciones (API) y los elementos de la base de datos del instalador.

Para obtener más información, vea [Otros orígenes de Windows información del instalador](other-sources-of-windows-installer-information.md).

## <a name="application-developers"></a>Desarrolladores de aplicaciones

Los desarrolladores de aplicaciones crean aplicaciones que llaman a la interfaz de programación de aplicaciones Windows Installer e instalan Windows paquetes del instalador en tiempo de ejecución. El Windows puede realizar el trabajo en una aplicación, como la reparación automática y la instalación a petición. Normalmente, los desarrolladores de aplicaciones hacen lo siguiente:

-   Habilite la instalación a petición de aplicaciones en tiempo de ejecución desde otra aplicación.

    Para obtener más información, vea lo siguiente:

    -   [Uso de funciones del instalador](using-installer-functions.md)
    -   [Referencia de función del instalador](installer-function-reference.md)
    -   [Instalación a petición](installation-on-demand.md)
    -   [Administración de componentes](component-management.md)
    -   [Edición de métodos abreviados del instalador](editing-installer-shortcuts.md)
    -   [**Propiedad OLEAdvtSupport**](oleadvtsupport.md)
    -   [Compatibilidad de la plataforma con anuncios](platform-support-of-advertisement.md)

-   Habilite la reparación de aplicaciones mediante la reinstalación de componentes según sea necesario en tiempo de ejecución.

    Para obtener más información, vea lo siguiente:

    -   [Uso de funciones del instalador](using-installer-functions.md)
    -   [Referencia de función del instalador](installer-function-reference.md)
    -   [Resistencia](resiliency.md)
    -   [Resistencia de origen](source-resiliency.md)
    -   [Buscar una característica o un componente rotos](searching-for-a-broken-feature-or-component.md)
    -   [Reemplazar archivos existentes](replacing-existing-files.md)

-   Mostrar una interfaz de usuario para recopilar información de usuario y preferencias de configuración la primera vez que se instala o ejecuta una aplicación. El autor del programa de instalación del paquete Windows installer debe agregar la interfaz de usuario.

    Para obtener más información, vea lo siguiente:

    -   [Uso de funciones del instalador](using-installer-functions.md)
    -   [Inicialización de una aplicación](initializing-an-application.md)
    -   [Cuadro de diálogo FirstRun](firstrun-dialog.md)
    -   [Acerca de la Interfaz de usuario](about-the-user-interface.md)

-   Cree aplicaciones que usen un modelo de direccionamiento indirecto para hacer referencia a componentes con funcionalidad paralela. El autor del programa de instalación del paquete Windows installer debe agregar las categorías de componentes calificados.

    Para obtener más información, vea lo siguiente:

    -   [Componentes calificados](qualified-components.md)
    -   [Uso de componentes calificados](using-qualified-components.md)

-   Use ensamblados privados y en paralelo para aislar las aplicaciones y reducir los conflictos de DLL.

    Para obtener más información, vea lo siguiente:

    -   [Ensamblados](assemblies.md)
    -   [Claves del Registro de ensamblados escritas por Windows Installer](assembly-registry-keys-written-by-windows-installer-.md)
    -   [Instalación de ensamblados Win32 para el uso compartido en paralelo en Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
    -   [Instalación de ensamblados Win32 para el uso privado de una aplicación en Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)
    -   [Tabla MsiAssembly](msiassembly-table.md)
    -   [Tabla MsiAssemblyName](msiassemblyname-table.md)
    -   [**MsiProvideAssembly**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)
    -   [**Propiedad MsiWin32AssemblySupport**](msiwin32assemblysupport.md)
    -   [**Propiedad MsiNetAssemblySupport**](msinetassemblysupport.md)
    -   [**Componentes aislados**](isolated-components.md)

-   Prepare la aplicación para instalar sus propias actualizaciones principales completas.

    Para obtener más información, vea lo siguiente:

    -   [Revisiones y actualizaciones](patching-and-upgrades.md)
    -   [Actualizaciones principales](major-upgrades.md)
    -   [**Propiedad UpgradeCode**](upgradecode.md)
    -   [**Uso de UpgradeCode**](using-an-upgradecode.md)
    -   [Impedir que un paquete antiguo se instale en una versión más reciente](preventing-an-old-package-from-installing-over-a-newer-version.md)

-   Prepare la aplicación para instalar sus propias actualizaciones secundarias, actualizaciones pequeñas o correcciones.

    Para obtener más información, vea lo siguiente:

    -   [Revisiones y actualizaciones](patching-and-upgrades.md)
    -   [Actualizaciones pequeñas](small-updates.md)
    -   [Actualizaciones secundarias](minor-upgrades.md)

-   Organice los recursos de la aplicación en componentes que puedan funcionar con Windows Installer.

    Para obtener más información, vea lo siguiente:

    -   [Windows Componentes del instalador](windows-installer-components.md)
    -   [Trabajar con características y componentes](working-with-features-and-components.md)
    -   [Uso de componentes transitivos](using-transitive-components.md)
    -   [¿Qué ocurre si se han roto las reglas de componentes?](what-happens-if-the-component-rules-are-broken.md)
    -   [Organización de aplicaciones en componentes](organizing-applications-into-components.md)
    -   [Componentes aislados](isolated-components.md)
    -   [Componentes calificados](qualified-components.md)

## <a name="setup-authors"></a>Autores de la instalación

Los autores de la instalación Windows paquetes del instalador (.msi archivos) que contienen la lógica de instalación y la información necesaria para instalar una aplicación. Normalmente usan herramientas de creación, como [Orca.exe](orca-exe.md) para rellenar la base de datos Windows Installer con la lógica y la información de instalación. Normalmente, los autores de la instalación hacen lo siguiente:

-   Determine la funcionalidad disponible con diferentes versiones Windows Instalador.

    Para obtener más información, vea lo siguiente:

    -   [Determinar la versión Windows instalador](determining-the-windows-installer-version.md)
    -   [Versiones publicadas de Windows Installer](released-versions-of-windows-installer.md)
    -   [Novedades del instalador de Windows](what-s-new-in-windows-installer.md)

-   Organice los recursos de la aplicación Windows componentes del instalador.

    Para obtener más información, vea lo siguiente:

    -   [Windows Componentes del instalador](windows-installer-components.md)
    -   [Organización de aplicaciones en componentes](organizing-applications-into-components.md)
    -   [Cambiar el código de componente](changing-the-component-code.md)
    -   [¿Qué ocurre si se han roto las reglas de componentes?](what-happens-if-the-component-rules-are-broken.md)
    -   [Windows Ejemplos de instalador](windows-installer-examples.md)

-   Use herramientas de creación de paquetes Windows Installer de terceros o herramientas del SDK como [Orca.exe](orca-exe.md) para rellenar una base de datos de instalación y crear un paquete Windows Installer.

    Para obtener más información, vea lo siguiente:

    -   [Windows Herramientas de desarrollo del instalador](windows-installer-development-tools.md)
    -   [Paquete de instalación, Acerca de la base de datos del instalador](installation-package.md)
    -   [Windows Extensiones de archivo del instalador](windows-installer-file-extensions.md)
    -   [Tablas de base de datos](database-tables.md)
    -   [Códigos de paquete](package-codes.md)
    -   [Creación de un paquete grande](authoring-a-large-package.md)
    -   [Windows Instalador en sistemas operativos de 64 bits](windows-installer-on-64-bit-operating-systems.md)
    -   [Asignar nombres a tablas, propiedades y acciones personalizadas](naming-custom-tables-properties-and-actions.md)
    -   [Limitaciones de OLE en Secuencias](ole-limitations-on-streams.md)
    -   [Formato de definición de columna](column-definition-format.md)
    -   [Reducir el tamaño de un archivo .msi archivo](reducing-the-size-of-an--msi-file.md)

-   Cree la base de Windows installer para instalar archivos.

    Para obtener más información, vea lo siguiente:

    -   [Grupo de tablas principales](core-tables-group.md)
    -   [Grupo de tablas de archivos](file-tables-group.md)
    -   [Tabla de archivos](file-table.md)
    -   [Búsqueda de archivos](file-searching.md)
    -   [Costo de archivos](file-costing.md)
    -   [Instalación de archivos](file-installation.md)
    -   [Archivos complementarios](companion-files.md)
    -   [Reglas de control de versiones de archivos](file-versioning-rules.md)
    -   [Control de versiones de archivo predeterminado](default-file-versioning.md)
    -   [Reemplazar archivos existentes](replacing-existing-files.md)
    -   [Uso de gabinetes y orígenes comprimidos](using-cabinets-and-compressed-sources.md)
    -   [Eliminación de archivos desenlazados](removing-stranded-files.md)
    -   [Instalación de componentes permanentes, archivos, fuentes y claves del Registro](installing-permanent-components-files-fonts-registry-keys.md)
    -   [Tabla FileSFPCatalog](filesfpcatalog-table.md)
    -   [Buscar un archivo y crear una propiedad que mantiene la ruta de acceso del archivo](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
    -   [Buscar un directorio y un archivo en el directorio](searching-for-a-directory-and-a-file-in-the-directory.md)
    -   [Windows Ejemplos de instalador](windows-installer-examples.md)

-   Cree una base de Windows installer que instale una estructura de directorios y carpetas.

    Para obtener más información, vea lo siguiente:

    -   [Grupo de tablas principales](core-tables-group.md)
    -   [Grupo de tablas de archivos](file-tables-group.md)
    -   [Tabla de componentes](component-table.md)
    -   [Tabla de directorios](directory-table.md)
    -   [Uso de la tabla de directorios](using-the-directory-table.md)
    -   [Usar una propiedad de directorio en una ruta de acceso](using-a-directory-property-in-a-path.md)
    -   [Propiedades de la carpeta del sistema](property-reference.md)
    -   [CreateFolder Table](createfolder-table.md)
    -   [Tabla LockPermissions](lockpermissions-table.md)
    -   [Tabla MsiLockPermissionsEx](msilockpermissionsex-table.md)
    -   [Cambiar la ubicación de destino de un directorio](changing-the-target-location-for-a-directory.md)
    -   [Windows Ejemplos de instalador](windows-installer-examples.md)

-   Cree una base de Windows installer que instale las claves del Registro.

    Para obtener más información, vea lo siguiente:

    -   [Grupo de tablas principales](core-tables-group.md)
    -   [Grupo de tablas del Registro](registry-tables-group.md)
    -   [Tabla del Registro](registry-table.md)
    -   [Modificar el Registro](modifying-the-registry.md)
    -   [Agregar o quitar claves del Registro en la instalación o eliminación de componentes](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md)
    -   [Agregar y quitar una aplicación y no dejar ningún seguimiento en el Registro](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [Instalación de componentes permanentes, archivos, fuentes y claves del Registro](installing-permanent-components-files-fonts-registry-keys.md)
    -   [Buscar aplicaciones, archivos, entradas del Registro o entradas de .ini existentes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
    -   [Buscar una entrada del Registro y crear una propiedad que mantiene el valor del Registro](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)
    -   [Claves del Registro de ensamblado escritas por el instalador Windows ensamblado](assembly-registry-keys-written-by-windows-installer-.md)
    -   [Desinstalar clave del Registro](uninstall-registry-key.md)
    -   [Tabla SelfReg](selfreg-table.md)
    -   [Especificar el orden de registro propio](specifying-the-order-of-self-registration.md)
    -   [Windows Ejemplos de instalador](windows-installer-examples.md)

-   Cree una base de Windows installer que instale los servicios.

    Para obtener más información, vea lo siguiente:

    -   [Tabla ServiceInstall](serviceinstall-table.md)
    -   [Tabla ServiceControl](servicecontrol-table.md)
    -   [Tabla de componentes](component-table.md)

-   Cree una base de Windows installer que instale componentes aislados o componentes COM.

    Para obtener más información, vea lo siguiente:

    -   [Grupo de tablas del Registro](registry-tables-group.md)
    -   [Tabla de clases](class-table.md)
    -   [Complus Table](complus-table.md)
    -   [Componentes aislados](isolated-components.md)
    -   [Uso de componentes aislados](using-isolated-components.md)
    -   [Instalación de componentes aislados](installation-of-isolated-components.md)
    -   [Reinstalación de componentes aislados](reinstallation-of-isolated-components.md)
    -   [Eliminación de componentes aislados](removal-of-isolated-components.md)
    -   [Instalación de un componente COM en una ubicación privada](installing-a-com-component-to-a-private-location.md)
    -   [Hacer que un componente COM en un paquete existente sea privado](make-a-com-component-in-an-existing-package-private.md)
    -   [Instalación de una aplicación COM+ con Windows Instalador](installing-a-com--application-with-the-windows-installer.md)
    -   [Instalación de un componente que no es COM en una ubicación privada](installing-a-non-com-component-to-a-private-location.md)
    -   [Hacer que un componente que no sea COM en un paquete existente sea privado](make-a-non-com-component-in-an-existing-package-private.md)

-   Cree una base de Windows installer que instale ensamblados.

    Para obtener más información, vea lo siguiente:

    -   [Tabla MsiAssembly](msiassembly-table.md)
    -   [Tabla MsiAssemblyName](msiassemblyname-table.md)
    -   [Ensamblados](assemblies.md)
    -   [Claves del Registro de ensamblado escritas por el instalador Windows ensamblado](assembly-registry-keys-written-by-windows-installer-.md)
    -   [Instalación de ensamblados win32](installation-of-win32-assemblies.md)

-   Cree una base de Windows installer que instale controladores ODBC y traductores.

    Para obtener más información, vea lo siguiente:

    -   [Tabla ODBCAttribute](odbcattribute-table.md)
    -   [Tabla ODBCDriver](odbcdriver-table.md)
    -   [Tabla ODBCTranslator](odbctranslator-table.md)
    -   [Tabla ODBCDataSource](odbcdatasource-table.md)
    -   [Tabla ODBCSourceAttribute](odbcsourceattribute-table.md)

-   Cree una base de Windows installer que instale MIME.

    Para obtener más información, vea lo siguiente:

    -   [Tabla MIME](mime-table.md)
    -   [Tabla de extensiones](extension-table.md)
    -   [Modificar el Registro](modifying-the-registry.md)

-   Cree una base Windows installer que instale variables de entorno.

    Para obtener más información, vea lo siguiente:

    -   [Tabla de entorno](environment-table.md)

-   Cree una base de Windows installer que instale accesos directos.

    Para obtener más información, vea lo siguiente:

    -   [Tabla de métodos abreviados](shortcut-table.md)
    -   [Tabla MsiShortcutProperty](msishortcutproperty-table.md)
    -   [Edición de métodos abreviados del instalador](editing-installer-shortcuts.md)
    -   [Windows Ejemplos de instalador](windows-installer-examples.md)

-   Cree una base de Windows installer que instale varias instancias de aplicaciones.

    Para obtener más información, vea lo siguiente:

    -   [Instalación de varias instancias de productos y revisiones](installing-multiple-instances-of-products-and-patches.md)
    -   [Creación de varias instancias con transformaciones de instancia](authoring-multiple-instances-with-instance-transforms.md)
    -   [Instalación de varias instancias con transformaciones de instancia](installing-multiple-instances-with-instance-transforms.md)

-   Especifique opciones y estados de selección de características predeterminados.

    Para obtener más información, vea lo siguiente:

    -   [Grupo de tablas principales](core-tables-group.md)
    -   [Tabla de componentes](component-table.md)
    -   [Tabla de características](feature-table.md)
    -   [Tabla FeatureComponents](featurecomponents-table.md)
    -   [Controlar los estados de selección de características](controlling-feature-selection-states.md)
    -   [Propiedades de las opciones de instalación de características](property-reference.md)

-   Especifique las condiciones que se deben cumplir para instalar una aplicación o componentes seleccionados.

    Para obtener más información, vea lo siguiente:

    -   [Tabla de condiciones](condition-table.md)
    -   [Tabla LaunchCondition](launchcondition-table.md)
    -   [Tabla de componentes](component-table.md)
    -   [Usar propiedades en instrucciones condicionales](using-properties-in-conditional-statements.md)
    -   [Sintaxis de instrucciones condicionales](conditional-statement-syntax.md)
    -   [Acciones de aseación que se ejecutarán durante la eliminación](conditioning-actions-to-run-during-removal.md)
    -   [Ejemplos de sintaxis de instrucciones condicionales](examples-of-conditional-statement-syntax.md)

-   Cree la secuencia de acciones usadas para instalar la aplicación.

    Para obtener más información, vea lo siguiente:

    -   [Uso de una tabla de secuencias](using-a-sequence-table.md)
    -   [Grupo de tablas de procedimientos de instalación](installation-procedure-tables-group.md)
    -   [Ejemplo detallado de tabla de secuencias](sequence-table-detailed-example.md)
    -   [Acciones con restricciones de secuenciación](actions-with-sequencing-restrictions.md)
    -   [Acciones sin restricciones de secuenciación](actions-without-sequencing-restrictions.md)
    -   [Usar propiedades en instrucciones condicionales](using-properties-in-conditional-statements.md)
    -   [Sintaxis de instrucciones condicionales](conditional-statement-syntax.md)
    -   [Ejemplos de sintaxis de instrucciones condicionales](examples-of-conditional-statement-syntax.md)
    -   [Acciones de aseación que se ejecutarán durante la eliminación](conditioning-actions-to-run-during-removal.md)
    -   [Acciones estándar](standard-actions.md)
    -   [Windows Ejemplos de instalador](windows-installer-examples.md)

-   Prepare el paquete de instalación de la aplicación para futuras actualizaciones de la aplicación mediante el Windows Installer.

    Para obtener más información, vea lo siguiente:

    -   [Revisiones y actualizaciones](patching-and-upgrades.md)
    -   [Preparación de una aplicación para futuras actualizaciones principales](preparing-an-application-for-future-major-upgrades.md)
    -   [Uso de UpgradeCode](using-an-upgradecode.md)
    -   [Actualizar tabla](upgrade-table.md)
    -   [**Propiedad UpgradeCode**](upgradecode.md)
    -   [Impedir que un paquete antiguo se instale en una versión más reciente](preventing-an-old-package-from-installing-over-a-newer-version.md)
    -   [Cambiar el código del producto](changing-the-product-code.md)
    -   [Actualizar ensamblados](updating-assemblies.md)
    -   [Windows Ejemplos de instalador](windows-installer-examples.md)

-   Solución de Windows paquetes del instalador en desarrollo.

    Para obtener más información, vea lo siguiente:

    -   [Validación de paquetes](package-validation.md)
    -   [Evaluadores de coherencia internos: TIC](internal-consistency-evaluators-ices.md)
    -   [Windows Registro del instalador](windows-installer-logging.md)
    -   [Comprobar la instalación de características, componentes, archivos](checking-the-installation-of-features-components-files.md)
    -   [Creación de un paquete grande](authoring-a-large-package.md)
    -   [Wilogutl.exe](wilogutl-exe.md)
    -   [Windows Herramientas de desarrollo del instalador](windows-installer-development-tools.md)
    -   [Validación de módulos de mezcla](validating-merge-modules.md)
    -   [Validar una base de datos de instalación](validating-an-installation-database.md)
    -   [Validación de una actualización de instalación](validating-an-installation-upgrade.md)
    -   [Buscar una característica o un componente rotos](searching-for-a-broken-feature-or-component.md)
    -   [Windows Mensajes de error del instalador](windows-installer-error-messages.md)
    -   [Registro de solicitudes de reinicio](logging-of-reboot-requests.md)

-   Asegúrese de una instalación e instalación seguras de la aplicación.

    Para obtener más información, vea lo siguiente:

    -   [Directrices para crear instalaciones seguras](guidelines-for-authoring-secure-installations.md)
    -   [Directrices para proteger acciones personalizadas](guidelines-for-securing-custom-actions.md)
    -   [Seguridad de acciones personalizadas](custom-action-security.md)
    -   [Directrices para proteger paquetes en equipos bloqueados](guidelines-for-securing-packages-on-locked-down-computers.md)
    -   [Creación de una instalación firmada totalmente verificada mediante Automation](authoring-a-fully-verified-signed-installation-using-automation.md)
    -   [Ejemplo de instalación de Windows Installer basado en URL](a-url-based-windows-installer-installation-example.md)
    -   [Creación de la Interfaz de usuario para la entrada de contraseña](authoring-the-user-interface-for-password-input.md)
    -   [Instalador de firmas digitales Windows datos](digital-signatures-and-windows-installer.md)
    -   [Uso Windows Installer con UAC](using-windows-installer-with-uac.md)
    -   [Aplicación de revisiones de control de cuentas de usuario (UAC)](user-account-control--uac--patching.md)
    -   [Msicert.exe](msicert-exe.md)
    -   [**AdminUser, propiedad**](adminuser.md)
    -   [**Propiedad con privilegios**](privileged.md)
    -   [**Propiedad SecureCustomProperties**](securecustomproperties.md)

-   Cree una interfaz de usuario para presentar opciones para configurar la instalación y obtener información del usuario sobre el proceso de instalación pendiente.

    Para obtener más información, vea lo siguiente:

    -   [Acerca de la Interfaz de usuario](about-the-user-interface.md)
    -   [Agregar controles y texto](adding-controls-and-text.md)
    -   [Creación de un control ProgressBar](authoring-a-progressbar-control.md)
    -   [Creación de mensajes de solicitud de disco](authoring-disk-prompt-messages.md)
    -   [Creación de un condicional "Please Wait . . ." Cuadro de mensaje](authoring-a-conditional-please-wait-------message-box.md)
    -   [Vista previa de la Interfaz de usuario](previewing-the-user-interface.md)
    -   [Agregar texto almacenado en una propiedad](adding-text-stored-in-a-property.md)
    -   [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

-   Cree una interfaz de usuario externa para presentar una interfaz de usuario personalizada para configurar la instalación y obtener información del usuario sobre el proceso de instalación pendiente.

    Para obtener más información, vea lo siguiente:

    -   [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
    -   [Supervisión de una instalación mediante MsiSetExternalUIRecord](monitoring-an-installation-using-msisetexternaluirecord.md)
    -   [Análisis de Windows del instalador](parsing-windows-installer-messages.md)
    -   [Devolver valores de un controlador de Interfaz de usuario externo](returning-values-from-an-external-user-interface-handler.md)
    -   [CONTROLADOR \_ INSTALLUI](/windows/desktop/api/Msi/nc-msi-installui_handlera)
    -   [Control de mensajes de progreso mediante MsiSetExternalUI](handling-progress-messages-using-msisetexternalui.md)
    -   [Supervisión de una instalación mediante MsiSetExternalUI](monitoring-an-installation-using-msisetexternalui.md)

-   Establezca la información de la aplicación **en Agregar o quitar programas** (ARP).

    Para obtener más información, vea lo siguiente:

    -   [Configuración de agregar o quitar programas con Windows instalador](configuring-add-remove-programs-with-windows-installer.md)
    -   [Agregar y quitar una aplicación y no dejar ningún seguimiento en el Registro](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [Desinstalar clave del Registro](uninstall-registry-key.md)

-   Escriba acciones personalizadas para controlar la lógica de instalación que no es compatible de forma nativa con Windows Instalador.

    Para obtener más información, vea lo siguiente:

    -   [Acciones personalizadas](custom-actions.md)
    -   [Lista de resumen de todos los tipos de acción personalizados](summary-list-of-all-custom-action-types.md)
    -   [Directrices para proteger acciones personalizadas](guidelines-for-securing-custom-actions.md)
    -   [Referencia de acción personalizada](custom-action-reference.md)
    -   [Usar una acción personalizada para crear cuentas de usuario en un equipo local](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [Usar una acción personalizada para iniciar un archivo instalado al final de la instalación](using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation.md)
    -   [Acceso a una base de datos o una sesión desde dentro de una acción personalizada](accessing-a-database-or-session-from-inside-a-custom-action.md)
    -   [Acceso a la sesión actual del instalador desde dentro de una acción personalizada](accessing-the-current-installer-session-from-inside-a-custom-action.md)
    -   [Cambiar el estado del sistema mediante una acción personalizada](changing-the-system-state-using-a-custom-action.md)

-   Arranque el Windows en el equipo de un usuario.

    Para obtener más información, vea lo siguiente:

    -   [Arranque](bootstrapping.md)
    -   [Instmsi.exe](instmsi-exe.md)
    -   [Arranque de descarga de Internet](internet-download-bootstrapping.md)
    -   [Msistuff.exe](msistuff-exe.md)
    -   [Ejemplo de instalación de Windows Installer basado en URL](a-url-based-windows-installer-installation-example.md)
    -   [Configuración de los Setup.exe recursos](configuring-the-setup-exe-resources.md)
    -   [Descarga de una instalación desde Internet](downloading-an-installation-from-the-internet.md)

-   Siga las directrices Active Accessibility al escribir Windows paquetes del instalador.

    Para obtener más información, vea lo siguiente:

    -   [Accesibilidad](accessibility.md)

-   Prepárese para la internacionalización de la configuración de una aplicación.

    Para obtener más información, vea lo siguiente:

    -   [Preparar un paquete Windows instalador para la localización](preparing-a-windows-installer-package-for-localization.md),
    -   [Localización de un paquete Windows instalador](localizing-a-windows-installer-package.md)
    -   [Control de páginas de códigos (Windows instalador)](code-page-handling-windows-installer-.md)
    -   [Agregar recursos localizados](adding-localized-resources.md)
    -   [Un ejemplo de localización](a-localization-example.md)
    -   [Localización de las tablas Error y ActionText](localizing-the-error-and-actiontext-tables.md)
    -   [Localización de columnas de base de datos](localizing-database-columns.md)
    -   [Crear una base de datos con una página de códigos neutra](creating-a-database-with-a-neutral-code-page.md)
    -   [Control de páginas de códigos de tablas importadas y exportadas](code-page-handling-of-imported-and-exported-tables.md)
    -   [Localización del idioma mostrado por los diálogos](localizing-the-language-displayed-by-dialogs.md)
    -   [Importar tablas De error localizadas y ActionText](importing-localized-error-and-actiontext-tables.md)
    -   [Actualización de las propiedades ProductLanguage y ProductCode](updating-productlanguage-and-productcode-properties.md)
    -   [Actualizar un flujo de información de resumen](updating-a-summary-information-stream.md)
    -   [Componentes calificados](qualified-components.md)
    -   [UIText Table](uitext-table.md)
    -   [Administrar lenguaje y página de códigos](manage-language-and-codepage.md)
    -   [Comprobar la página de códigos de la base de datos de instalación](checking-the-installation-database-code-page.md)

-   Cree Windows installer para plataformas de 32 y 64 bits.

    Para obtener más información, vea lo siguiente:

    -   [Windows Instalador en sistemas operativos de 64 bits](windows-installer-on-64-bit-operating-systems.md)
    -   [Acciones personalizadas de 64 bits](64-bit-custom-actions.md)
    -   [Uso de acciones personalizadas de 64 bits](using-64-bit-custom-actions.md)
    -   [Uso de módulos de combinación de 64 bits](using-64-bit-merge-modules.md)

-   Redistribuya los componentes compartidos Windows installer y la lógica de instalación como módulos de combinación.

    Para obtener más información, vea lo siguiente:

    -   [Módulos de combinación](merge-modules.md)
    -   [Creación de una transformación de idioma para un módulo de combinación de varios idiomas](authoring-a-language-transform-for-a-multiple-language-merge-module.md)
    -   [Aplicación de un módulo de combinación configurable con personalizaciones](applying-a-configurable-merge-module-with-customizations.md)

-   Programe o suprima los reinicios durante Windows instalación del instalador.

    Para obtener más información, vea lo siguiente:

    -   [Reinicios del sistema](system-reboots.md)
    -   [Registro de solicitudes de reinicio](logging-of-reboot-requests.md)

-   Cree actualizaciones o correcciones para una aplicación existente mediante la creación de una revisión.

    Para obtener más información, vea lo siguiente:

    -   [Crear una revisión de actualización pequeña](creating-a-small-update-patch.md)
    -   [Ejemplo pequeño de aplicación de revisiones de actualizaciones](a-small-update-patching-example.md)

-   Cree un paquete de doble propósito capaz de instalar una aplicación solo para el usuario actual o para todos los usuarios del equipo.

    Para obtener más información, vea lo siguiente:

    -   [Contexto de instalación](installation-context.md)
    -   [Creación de paquete único](single-package-authoring.md)
    -   [Ejemplo de creación de paquete único](single-package-authoring-example.md)

-   Personalice los servicios en el equipo mediante Windows instalador.

    Para obtener más información, vea lo siguiente:

    -   [Uso de la configuración de servicios](using-services-configuration.md)

-   Proteja los recursos en el equipo mediante Windows instalador.

    Para obtener más información, vea lo siguiente:

    -   [Directrices para crear instalaciones seguras](guidelines-for-authoring-secure-installations.md)
    -   [Protección de recursos](securing-resources-.md)

-   Enumerar todos los componentes instalados en el equipo y obtener la ruta de acceso de la clave para el componente.

    Para obtener más información, vea lo siguiente:

    -   [Enumeración de componentes](enumerating-components-.md)

-   Instale varios paquetes mediante el [*procesamiento de transacciones.*](t-gly.md)

    Para obtener más información, vea lo siguiente:

    -   [Instalaciones de varios paquetes](multiple-package-installations.md)

-   Inserte una interfaz de usuario personalizada en el paquete Windows Installer.

    Para obtener más información, vea lo siguiente:

    -   [Uso de la interfaz de usuario](using-the-user-interface.md)
    -   [Uso de una interfaz de usuario insertadas](using-an-embedded-ui.md)

## <a name="it-professionals"></a>Profesionales de TI

Los profesionales y administradores de TI personalizan e implementan los paquetes Windows Installer existentes. Estos usuarios reempaquete las configuraciones de las aplicaciones existentes en los paquetes de instalación de Windows Installer e instalan y mantienen imágenes administrativas de las instalaciones de Windows Installer en redes.

-   Personalización de aplicaciones y configuración mediante la generación y aplicación de Windows del instalador

    Para obtener más información, vea lo siguiente:

    -   [Personalización](customization.md)
    -   [Transformaciones de base de datos](database-transforms.md)
    -   [Un ejemplo de transformación de personalización](a-customization-transform-example.md)
    -   [Mezclas y transformaciones](merges-and-transforms.md)
    -   [Uso de transformaciones para agregar recursos](using-transforms-to-add-resources.md)
    -   [Generar una transformación](generate-a-transform.md)
    -   [Opciones de línea de comandos](command-line-options.md)
    -   [Msitran.exe](msitran-exe.md)
    -   [Aplicar una transformación](apply-a-transform.md)
    -   [Ver una transformación](view-a-transform.md)
    -   [Ver diferencias entre dos bases de datos](view-differences-between-two-databases.md)
    -   [Aplicación de revisiones a aplicaciones personalizadas](patching-customized-applications.md)

-   Implemente un Windows de instalación, actualización o revisión del instalador de aplicaciones.

    Para obtener más información, vea lo siguiente:

    -   [Instalación de una aplicación](installing-an-application.md)
    -   [Aplicación de revisiones y actualizaciones](patching-and-upgrades.md)
    -   [Transformaciones](transforms.md)
    -   [Instalación de un paquete con privilegios elevados para un usuario que no es administrador](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Aplicación de actualizaciones principales mediante la aplicación de revisiones a la instalación local del producto](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)
    -   [Aplicación de actualizaciones principales mediante la instalación del producto](applying-major-upgrades-by-installing-the-product.md)
    -   [Aplicación de actualizaciones pequeñas mediante la aplicación de revisiones a la instalación local del producto](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [Aplicación de actualizaciones pequeñas mediante la reinstalación del producto](applying-small-updates-by-reinstalling-the-product.md)
    -   [Aplicación de actualizaciones pequeñas mediante la aplicación de revisiones a una imagen administrativa](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Aplicación de revisiones a las instalaciones iniciales](patching-initial-installations.md)
    -   [Opciones de línea de comandos](command-line-options.md)

-   Solución de Windows paquetes del instalador.

    Para obtener más información, vea lo siguiente:

    -   [Windows Registro del instalador](windows-installer-logging.md)
    -   [Comprobar la instalación de características, componentes, archivos](checking-the-installation-of-features-components-files.md)
    -   [Wilogutl.exe](wilogutl-exe.md)
    -   [Buscar una característica o componente rotos](searching-for-a-broken-feature-or-component.md)
    -   [Windows Mensajes de error del instalador](windows-installer-error-messages.md)
    -   [Msicert.exe](msicert-exe.md)

-   Use scripting para consultar Windows instalador para obtener información sobre un producto y modificar la instalación.

    Para obtener más información, vea lo siguiente:

    -   [Interfaz de Automation](automation-interface.md)
    -   [Windows Ejemplos de scripting del instalador](windows-installer-scripting-examples.md)
    -   [Usar Windows instalador con WMI](using-windows-installer-with-wmi.md)

-   Crear y mantener instalaciones administrativas.

    Para obtener más información, vea lo siguiente:

    -   [Instalación administrativa](administrative-installation.md)
    -   [Opciones de línea de comandos](command-line-options.md)
    -   [**Propiedad AdminProperties**](adminproperties.md)
    -   [Aplicación de actualizaciones pequeñas mediante la aplicación de revisiones a una imagen administrativa](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Aplicación de un paquete de revisión a una instalación administrativa](applying-a-patch-package-to-an-administrative-installation.md)
    -   [Orden de ejecución de la acción](action-execution-order.md)
    -   [**Propiedad IsAdminPackage**](isadminpackage.md)
    -   [Orden de prioridad de propiedad](order-of-property-precedence.md)
    -   [**Propiedad AdminProperties**](adminproperties.md)

-   Hacer que una aplicación esté disponible para todos los usuarios de un equipo o solo para un usuario especificado.

    Para obtener más información, vea lo siguiente:

    -   [Contexto de instalación](installation-context.md)
    -   [**AllUSERS( Propiedad)**](allusers.md)

-   Interpretar paquetes, instalar productos y configurar opciones de características mediante una línea de comandos.

    Para obtener más información, vea lo siguiente:

    -   [Opciones de línea de comandos](command-line-options.md)
    -   [Establecer valores de propiedad pública en la línea de comandos](setting-public-property-values-on-the-command-line.md)
    -   [Obtener y establecer propiedades](getting-and-setting-properties.md)
    -   [Reinstalación de una característica o aplicación](reinstalling-a-feature-or-application.md)
    -   [Aplicación de actualizaciones pequeñas mediante la aplicación de revisiones a la instalación local del producto](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [Aplicación de actualizaciones pequeñas mediante la reinstalación del producto](applying-small-updates-by-reinstalling-the-product.md)
    -   [Cambiar la ubicación de destino de un directorio](changing-the-target-location-for-a-directory.md)
    -   [Aplicación de actualizaciones pequeñas mediante la aplicación de revisiones a una imagen administrativa](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Aplicación de actualizaciones principales mediante la instalación del producto](applying-major-upgrades-by-installing-the-product.md)
    -   [Propiedades de configuración](property-reference.md)
    -   [Propiedades de opciones de instalación de características](property-reference.md)

-   Trabajar con directivas para administrar permisos y derechos de acceso.

    Para obtener más información, vea lo siguiente:

    -   [Directivas de máquina](machine-policies.md),
    -   [Directivas de usuario](user-policies.md),
    -   [Instalación de un paquete con privilegios elevados para un usuario que no es administrador](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Anuncio de Per-User aplicación que se va a instalar con privilegios elevados](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [Usar una acción personalizada para crear cuentas de usuario en un equipo local](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [**AdminUser (propiedad)**](adminuser.md)
    -   [**Privileged (Propiedad)**](privileged.md)
    -   [**Propiedad EnableUserControl**](enableusercontrol.md)
    -   [**Propiedad UserSID**](usersid.md)
    -   [**Propiedad SecureCustomProperties**](securecustomproperties.md)

-   Instale varios paquetes mediante el [*procesamiento de transacciones.*](t-gly.md)

    Para obtener más información, vea lo siguiente:

    -   [Instalaciones de varios paquetes](multiple-package-installations.md)

-   Inserte una interfaz de usuario personalizada dentro de un Windows installer.

    Para obtener más información, vea lo siguiente:

    -   [Uso de la interfaz de usuario](using-the-user-interface.md)
    -   [Uso de una interfaz de usuario insertadas](using-an-embedded-ui.md)

## <a name="infrastructure-developers"></a>Desarrolladores de infraestructura

Los desarrolladores de infraestructura pueden crear plataformas unificadas para la implementación y administración de software que usa el Windows Installer. Pueden usar la interfaz de programación Windows Installer para consultar, administrar y distribuir aplicaciones, revisiones y orígenes en un sistema.

-   Buscar, inventariar y consultar el estado, la información y los clientes de los componentes.

    Para obtener más información, vea lo siguiente:

    -   [Funciones específicas de componentes](installer-function-reference.md)
    -   [Funciones de estado del sistema](installer-function-reference.md)
    -   [Installer (objeto)](installer-object.md)
    -   [Product (Objeto)](product-object.md)
    -   [Patch (objeto)](patch-object.md)

-   Inventario y consulta para obtener información y el estado de los productos y características.

    Para obtener más información, vea lo siguiente:

    -   [Productos y revisiones de inventario](inventory-products-and-patches-.md)
    -   [Funciones de estado del sistema](installer-function-reference.md)
    -   [Funciones de consulta de productos](installer-function-reference.md)
    -   [Installer (objeto)](installer-object.md)
    -   [Product (Objeto)](product-object.md)
    -   [Patch (objeto)](patch-object.md)

-   Mejore la resistencia de origen mediante Windows Installer para inventariar, consultar y modificar la lista de origen de aplicaciones, actualizaciones y revisiones.

    Para obtener más información, vea lo siguiente:

    -   [**Propiedad SOURCELIST**](sourcelist.md)
    -   [**Resistencia de origen**](source-resiliency.md)
    -   [Funciones de instalación y configuración](installer-function-reference.md)
    -   [Installer (objeto)](installer-object.md)
    -   [Objeto Product](product-object.md)
    -   [Patch (objeto)](patch-object.md)

-   Mejore la resistencia del origen mediante Windows Installer para inventariar, consultar y modificar orígenes multimedia.

    Para obtener más información, vea lo siguiente:

    -   [**Propiedad SOURCELIST**](sourcelist.md)
    -   [Resistencia de origen](source-resiliency.md)
    -   [Funciones de instalación y configuración](installer-function-reference.md)
    -   [Objeto Product](product-object.md)
    -   [Patch (objeto)](patch-object.md)

-   Inventario y consulta de información y el estado de las revisiones.

    Para obtener más información, vea lo siguiente:

    -   [Productos y revisiones de inventario](inventory-products-and-patches-.md)
    -   [Referencia de función del instalador](installer-function-reference.md)
    -   [Patch (objeto)](patch-object.md)

-   Trabaje con la directiva para administrar permisos y derechos de acceso.

    Para obtener más información, vea lo siguiente:

    -   [Directivas de máquina](machine-policies.md)
    -   [Directivas de usuario](user-policies.md)
    -   [Instalación de un paquete con privilegios elevados para un usuario que no es administrador](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Anuncio de Per-User aplicación que se va a instalar con privilegios elevados](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [Usar una acción personalizada para crear cuentas de usuario en un equipo local](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [**Propiedad AdminUser**](adminuser.md)
    -   [**Propiedad privileged**](privileged.md)
    -   [**Propiedad EnableUserControl**](enableusercontrol.md)
    -   [**Propiedad UserSID**](usersid.md)
    -   [**Propiedad SecureCustomProperties**](securecustomproperties.md)

 

 



