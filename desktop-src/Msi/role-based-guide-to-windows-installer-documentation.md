---
description: Windows Installer es la solución recomendada para la instalación y la configuración de aplicaciones en Windows.
ms.assetid: 13f41020-5275-44cd-b26b-f45483700d8a
title: Guía basada en roles para Windows Installer documentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8a2138e963b6d29bd161df5e09144cf0cfd36b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082334"
---
# <a name="role-based-guide-to-windows-installer-documentation"></a>Guía basada en roles para Windows Installer documentación

Windows Installer es la solución recomendada para la instalación y la configuración de aplicaciones en Windows. Por lo tanto, parte de la información contenida en este SDK será de interés para una amplia gama de profesionales de ti y desarrollo de software. Esta sección se proporciona como guía a los lectores que prefieren ver vínculos a temas organizados por rol profesional y escenarios de tareas comunes. Dado que los roles pueden diferir en gran medida entre las organizaciones, la siguiente agrupación solo se debe considerar como guía de una ubicación para empezar a buscar la información que necesita.

-   [Desarrolladores de aplicaciones](#application-developers)
-   [Configuración de autores](#setup-authors)
-   [Profesionales de TI](#it-professionals)
-   [Desarrolladores de infraestructura](#infrastructure-developers)

Esta documentación está destinada a desarrolladores de software que desean crear aplicaciones que utilicen Windows Installer. Como origen principal del material de referencia para el instalador, el SDK proporciona información acerca de los paquetes de instalación y el servicio del instalador. Contiene descripciones completas de la interfaz de programación de aplicaciones (API) y los elementos de la base de datos del instalador.

Para obtener más información, vea [otros orígenes de información de Windows Installer](other-sources-of-windows-installer-information.md).

## <a name="application-developers"></a>Desarrolladores de aplicaciones

Los desarrolladores de aplicaciones crean aplicaciones que llaman a la interfaz de programación de aplicaciones Windows Installer e instalan paquetes de Windows Installer en tiempo de ejecución. El Windows Installer puede trabajar en una aplicación como la reparación automática y la instalación a petición. Normalmente, los desarrolladores de aplicaciones hacen lo siguiente:

-   Habilitar la instalación a petición de aplicaciones en tiempo de ejecución desde otra aplicación.

    Para obtener más información, vea lo siguiente:

    -   [Usar las funciones del instalador](using-installer-functions.md)
    -   [Referencia de funciones del instalador](installer-function-reference.md)
    -   [Instalación a petición](installation-on-demand.md)
    -   [Administración de componentes](component-management.md)
    -   [Editar accesos directos del instalador](editing-installer-shortcuts.md)
    -   [**Propiedad OLEAdvtSupport**](oleadvtsupport.md)
    -   [Compatibilidad de la plataforma con el anuncio](platform-support-of-advertisement.md)

-   Habilite la reparación automática de las aplicaciones reinstalando los componentes según sea necesario en tiempo de ejecución.

    Para obtener más información, vea lo siguiente:

    -   [Usar las funciones del instalador](using-installer-functions.md)
    -   [Referencia de funciones del instalador](installer-function-reference.md)
    -   [Resistencia](resiliency.md)
    -   [Resistencia de origen](source-resiliency.md)
    -   [Buscar una característica o componente interrumpido](searching-for-a-broken-feature-or-component.md)
    -   [Reemplazar archivos existentes](replacing-existing-files.md)

-   Mostrar una interfaz de usuario para recopilar las preferencias de configuración e información de usuario la primera vez que se instala o se ejecuta una aplicación. El autor del programa de instalación del paquete de Windows Installer debe agregar la interfaz de usuario.

    Para obtener más información, vea lo siguiente:

    -   [Usar las funciones del instalador](using-installer-functions.md)
    -   [Inicializar una aplicación](initializing-an-application.md)
    -   [Cuadro de diálogo FirstRun](firstrun-dialog.md)
    -   [Acerca de la interfaz de usuario](about-the-user-interface.md)

-   Cree aplicaciones que usen un modelo de direccionamiento indirecto para hacer referencia a componentes con funcionalidad paralela. El autor del programa de instalación del paquete de Windows Installer debe agregar las categorías de componentes cualificadas.

    Para obtener más información, vea lo siguiente:

    -   [Componentes completos](qualified-components.md)
    -   [Uso de componentes calificados](using-qualified-components.md)

-   Use ensamblados privados y en paralelo para aislar las aplicaciones y reducir los conflictos de DLL.

    Para obtener más información, vea lo siguiente:

    -   [Ensamblados](assemblies.md)
    -   [Claves del registro de ensamblado escritas por Windows Installer](assembly-registry-keys-written-by-windows-installer-.md)
    -   [Instalación de ensamblados Win32 para el uso compartido en paralelo en Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
    -   [Instalar ensamblados Win32 para el uso privado de una aplicación en Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)
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
    -   [**Usar UpgradeCode**](using-an-upgradecode.md)
    -   [Impedir que un paquete antiguo se instale en una versión más reciente](preventing-an-old-package-from-installing-over-a-newer-version.md)

-   Prepare la aplicación para instalar sus propias actualizaciones secundarias, pequeñas actualizaciones o correcciones.

    Para obtener más información, vea lo siguiente:

    -   [Revisiones y actualizaciones](patching-and-upgrades.md)
    -   [Actualizaciones pequeñas](small-updates.md)
    -   [Actualizaciones secundarias](minor-upgrades.md)

-   Organice los recursos de la aplicación en componentes que pueden trabajar con el Windows Installer.

    Para obtener más información, vea lo siguiente:

    -   [Componentes de Windows Installer](windows-installer-components.md)
    -   [Trabajar con características y componentes](working-with-features-and-components.md)
    -   [Uso de componentes transitivos](using-transitive-components.md)
    -   [¿Qué ocurre si se interrumpen las reglas de componentes?](what-happens-if-the-component-rules-are-broken.md)
    -   [Organizar aplicaciones en componentes](organizing-applications-into-components.md)
    -   [Componentes aislados](isolated-components.md)
    -   [Componentes completos](qualified-components.md)

## <a name="setup-authors"></a>Configuración de autores

Los autores del programa de instalación crean Windows Installer paquetes (archivos. msi) que contienen la lógica de instalación y la información necesaria para instalar una aplicación. Normalmente usan herramientas de creación como [Orca.exe](orca-exe.md) para rellenar la base de datos Windows Installer con la lógica e información del programa de instalación. Normalmente, los autores de la instalación hacen lo siguiente:

-   Determine la funcionalidad disponible con diferentes versiones de Windows Installer.

    Para obtener más información, vea lo siguiente:

    -   [Determinar la versión de Windows Installer](determining-the-windows-installer-version.md)
    -   [Versiones de lanzamiento de Windows Installer](released-versions-of-windows-installer.md)
    -   [Novedades de Windows Installer](what-s-new-in-windows-installer.md)

-   Organice los recursos de la aplicación en componentes de Windows Installer.

    Para obtener más información, vea lo siguiente:

    -   [Componentes de Windows Installer](windows-installer-components.md)
    -   [Organizar aplicaciones en componentes](organizing-applications-into-components.md)
    -   [Cambiar el código del componente](changing-the-component-code.md)
    -   [¿Qué ocurre si se interrumpen las reglas de componentes?](what-happens-if-the-component-rules-are-broken.md)
    -   [Ejemplos de Windows Installer](windows-installer-examples.md)

-   Use herramientas de creación de paquetes de Windows Installer de terceros o herramientas de SDK como [Orca.exe](orca-exe.md) para rellenar una base de datos de instalación y crear un paquete de Windows Installer.

    Para obtener más información, vea lo siguiente:

    -   [Herramientas de desarrollo de Windows Installer](windows-installer-development-tools.md)
    -   [Paquete de instalación, acerca de la base de datos del instalador](installation-package.md)
    -   [Extensiones de archivo Windows Installer](windows-installer-file-extensions.md)
    -   [Tablas de base de datos](database-tables.md)
    -   [Códigos de paquete](package-codes.md)
    -   [Crear un paquete grande](authoring-a-large-package.md)
    -   [Windows Installer en sistemas operativos de 64 bits](windows-installer-on-64-bit-operating-systems.md)
    -   [Asignar nombres a tablas, propiedades y acciones personalizadas](naming-custom-tables-properties-and-actions.md)
    -   [Limitaciones de OLE en secuencias](ole-limitations-on-streams.md)
    -   [Formato de definición de columna](column-definition-format.md)
    -   [Reducir el tamaño de un archivo. msi](reducing-the-size-of-an--msi-file.md)

-   Cree la base de datos Windows Installer para instalar archivos.

    Para obtener más información, vea lo siguiente:

    -   [Grupo de tablas principales](core-tables-group.md)
    -   [Grupo de tablas de archivos](file-tables-group.md)
    -   [Tabla de archivos](file-table.md)
    -   [Búsqueda de archivos](file-searching.md)
    -   [Costo de archivos](file-costing.md)
    -   [Instalación de archivos](file-installation.md)
    -   [Archivos complementarios](companion-files.md)
    -   [Reglas de control de versiones de archivo](file-versioning-rules.md)
    -   [Control de versiones de archivo predeterminado](default-file-versioning.md)
    -   [Reemplazar archivos existentes](replacing-existing-files.md)
    -   [Uso de archivadores y orígenes comprimidos](using-cabinets-and-compressed-sources.md)
    -   [Quitar archivos en desuso](removing-stranded-files.md)
    -   [Instalación de componentes permanentes, archivos, fuentes y claves del registro](installing-permanent-components-files-fonts-registry-keys.md)
    -   [Tabla FileSFPCatalog](filesfpcatalog-table.md)
    -   [Buscar un archivo y crear una propiedad que contiene la ruta de acceso del archivo](searching-for-a-file-and-creating-a-property-holding-the-file-s-path.md)
    -   [Buscar un directorio y un archivo en el directorio](searching-for-a-directory-and-a-file-in-the-directory.md)
    -   [Ejemplos de Windows Installer](windows-installer-examples.md)

-   Cree una base de datos Windows Installer que instale una estructura de directorios y carpetas.

    Para obtener más información, vea lo siguiente:

    -   [Grupo de tablas principales](core-tables-group.md)
    -   [Grupo de tablas de archivos](file-tables-group.md)
    -   [Tabla de componentes](component-table.md)
    -   [Tabla de directorio](directory-table.md)
    -   [Usar la tabla de directorio](using-the-directory-table.md)
    -   [Usar una propiedad de directorio en una ruta de acceso](using-a-directory-property-in-a-path.md)
    -   [Propiedades de la carpeta del sistema](property-reference.md)
    -   [CreateFolder (tabla)](createfolder-table.md)
    -   [Tabla LockPermissions](lockpermissions-table.md)
    -   [Tabla MsiLockPermissionsEx](msilockpermissionsex-table.md)
    -   [Cambiar la ubicación de destino de un directorio](changing-the-target-location-for-a-directory.md)
    -   [Ejemplos de Windows Installer](windows-installer-examples.md)

-   Cree una base de datos Windows Installer que instale las claves del registro.

    Para obtener más información, vea lo siguiente:

    -   [Grupo de tablas principales](core-tables-group.md)
    -   [Grupo de tablas del registro](registry-tables-group.md)
    -   [Tabla del registro](registry-table.md)
    -   [Modificar el registro](modifying-the-registry.md)
    -   [Agregar o quitar claves del registro en la instalación o desinstalación de componentes](adding-or-removing-registry-keys-on-the-installation-or-removal-of-components.md)
    -   [Agregar y quitar una aplicación y no dejar ningún seguimiento en el registro](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [Instalación de componentes permanentes, archivos, fuentes y claves del registro](installing-permanent-components-files-fonts-registry-keys.md)
    -   [Buscar aplicaciones, archivos, entradas del registro o entradas del archivo. ini existentes](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)
    -   [Buscar una entrada del registro y crear una propiedad que contiene el valor del registro](searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry.md)
    -   [Claves del registro de ensamblado escritas por el Windows Installer](assembly-registry-keys-written-by-windows-installer-.md)
    -   [Desinstalar la clave del registro](uninstall-registry-key.md)
    -   [Tabla SelfReg](selfreg-table.md)
    -   [Especificar el orden de registro automático](specifying-the-order-of-self-registration.md)
    -   [Ejemplos de Windows Installer](windows-installer-examples.md)

-   Cree una base de datos Windows Installer que instale los servicios de.

    Para obtener más información, vea lo siguiente:

    -   [Tabla ServiceInstall](serviceinstall-table.md)
    -   [Tabla ServiceControl](servicecontrol-table.md)
    -   [Tabla de componentes](component-table.md)

-   Cree una base de datos Windows Installer que instale componentes aislados o componentes COM.

    Para obtener más información, vea lo siguiente:

    -   [Grupo de tablas del registro](registry-tables-group.md)
    -   [Tabla de clases](class-table.md)
    -   [Tabla de ComPlus](complus-table.md)
    -   [Componentes aislados](isolated-components.md)
    -   [Usar componentes aislados](using-isolated-components.md)
    -   [Instalación de componentes aislados](installation-of-isolated-components.md)
    -   [Reinstalación de componentes aislados](reinstallation-of-isolated-components.md)
    -   [Eliminación de componentes aislados](removal-of-isolated-components.md)
    -   [Instalar un componente COM en una ubicación privada](installing-a-com-component-to-a-private-location.md)
    -   [Convertir un componente COM en un paquete existente privado](make-a-com-component-in-an-existing-package-private.md)
    -   [Instalación de una aplicación COM+ con el Windows Installer](installing-a-com--application-with-the-windows-installer.md)
    -   [Instalar un componente que no es COM en una ubicación privada](installing-a-non-com-component-to-a-private-location.md)
    -   [Convertir un componente que no sea COM en un paquete existente privado](make-a-non-com-component-in-an-existing-package-private.md)

-   Cree una base de datos Windows Installer que instale los ensamblados.

    Para obtener más información, vea lo siguiente:

    -   [Tabla MsiAssembly](msiassembly-table.md)
    -   [Tabla MsiAssemblyName](msiassemblyname-table.md)
    -   [Ensamblados](assemblies.md)
    -   [Claves del registro de ensamblado escritas por el Windows Installer](assembly-registry-keys-written-by-windows-installer-.md)
    -   [Instalación de ensamblados Win32](installation-of-win32-assemblies.md)

-   Cree una base de datos Windows Installer que instale controladores y traductores ODBC.

    Para obtener más información, vea lo siguiente:

    -   [Tabla ODBCAttribute](odbcattribute-table.md)
    -   [Tabla ODBCDriver](odbcdriver-table.md)
    -   [Tabla ODBCTranslator](odbctranslator-table.md)
    -   [Tabla ODBCDataSource](odbcdatasource-table.md)
    -   [Tabla ODBCSourceAttribute](odbcsourceattribute-table.md)

-   Cree una base de datos Windows Installer que instale MIME.

    Para obtener más información, vea lo siguiente:

    -   [Tabla MIME](mime-table.md)
    -   [Tabla de extensión](extension-table.md)
    -   [Modificar el registro](modifying-the-registry.md)

-   Cree una base de datos Windows Installer que instale variables de entorno.

    Para obtener más información, vea lo siguiente:

    -   [Tabla de entorno](environment-table.md)

-   Cree una base de datos Windows Installer que instale accesos directos.

    Para obtener más información, vea lo siguiente:

    -   [Tabla de acceso directo](shortcut-table.md)
    -   [Tabla MsiShortcutProperty](msishortcutproperty-table.md)
    -   [Editar accesos directos del instalador](editing-installer-shortcuts.md)
    -   [Ejemplos de Windows Installer](windows-installer-examples.md)

-   Cree una base de datos Windows Installer que instale varias instancias de aplicaciones.

    Para obtener más información, vea lo siguiente:

    -   [Instalación de varias instancias de productos y revisiones](installing-multiple-instances-of-products-and-patches.md)
    -   [Crear varias instancias con transformaciones de instancia](authoring-multiple-instances-with-instance-transforms.md)
    -   [Instalar varias instancias con transformaciones de instancia](installing-multiple-instances-with-instance-transforms.md)

-   Especifique las opciones y los Estados de selección de características predeterminados.

    Para obtener más información, vea lo siguiente:

    -   [Grupo de tablas principales](core-tables-group.md)
    -   [Tabla de componentes](component-table.md)
    -   [Tabla de características](feature-table.md)
    -   [Tabla FeatureComponents](featurecomponents-table.md)
    -   [Control de los Estados de selección de características](controlling-feature-selection-states.md)
    -   [Propiedades de opciones de instalación de características](property-reference.md)

-   Especifique las condiciones que deben cumplirse para instalar una aplicación o los componentes seleccionados.

    Para obtener más información, vea lo siguiente:

    -   [Tabla de condiciones](condition-table.md)
    -   [Tabla LaunchCondition](launchcondition-table.md)
    -   [Tabla de componentes](component-table.md)
    -   [Usar propiedades en instrucciones condicionales](using-properties-in-conditional-statements.md)
    -   [Sintaxis de la instrucción condicional](conditional-statement-syntax.md)
    -   [Acciones de acondicionamiento que se ejecutan durante la eliminación](conditioning-actions-to-run-during-removal.md)
    -   [Ejemplos de sintaxis de instrucciones condicionales](examples-of-conditional-statement-syntax.md)

-   Cree la secuencia de acciones que se usa para instalar la aplicación.

    Para obtener más información, vea lo siguiente:

    -   [Usar una tabla de secuencia](using-a-sequence-table.md)
    -   [Grupo de tablas de procedimientos de instalación](installation-procedure-tables-group.md)
    -   [Ejemplo detallado de tabla de secuencias](sequence-table-detailed-example.md)
    -   [Acciones con restricciones de secuenciación](actions-with-sequencing-restrictions.md)
    -   [Acciones sin restricciones de secuenciación](actions-without-sequencing-restrictions.md)
    -   [Usar propiedades en instrucciones condicionales](using-properties-in-conditional-statements.md)
    -   [Sintaxis de la instrucción condicional](conditional-statement-syntax.md)
    -   [Ejemplos de sintaxis de instrucciones condicionales](examples-of-conditional-statement-syntax.md)
    -   [Acciones de acondicionamiento que se ejecutan durante la eliminación](conditioning-actions-to-run-during-removal.md)
    -   [Acciones estándar](standard-actions.md)
    -   [Ejemplos de Windows Installer](windows-installer-examples.md)

-   Preparar el paquete de instalación de la aplicación para futuras actualizaciones de la aplicación mediante el servicio de Windows Installer.

    Para obtener más información, vea lo siguiente:

    -   [Revisiones y actualizaciones](patching-and-upgrades.md)
    -   [Preparación de una aplicación para futuras actualizaciones principales](preparing-an-application-for-future-major-upgrades.md)
    -   [Usar UpgradeCode](using-an-upgradecode.md)
    -   [Actualizar tabla](upgrade-table.md)
    -   [**Propiedad UpgradeCode**](upgradecode.md)
    -   [Impedir que un paquete antiguo se instale en una versión más reciente](preventing-an-old-package-from-installing-over-a-newer-version.md)
    -   [Cambiar el código de producto](changing-the-product-code.md)
    -   [Actualizar ensamblados](updating-assemblies.md)
    -   [Ejemplos de Windows Installer](windows-installer-examples.md)

-   Solucionar problemas de los paquetes de Windows Installer en desarrollo.

    Para obtener más información, vea lo siguiente:

    -   [Validación de paquetes](package-validation.md)
    -   [Evaluadores de coherencia interna-CIEM](internal-consistency-evaluators-ices.md)
    -   [Registro de Windows Installer](windows-installer-logging.md)
    -   [Comprobar la instalación de características, componentes y archivos](checking-the-installation-of-features-components-files.md)
    -   [Crear un paquete grande](authoring-a-large-package.md)
    -   [Wilogutl.exe](wilogutl-exe.md)
    -   [Herramientas de desarrollo de Windows Installer](windows-installer-development-tools.md)
    -   [Validar módulos de combinación](validating-merge-modules.md)
    -   [Validar una base de datos de instalación](validating-an-installation-database.md)
    -   [Validar una actualización de instalación](validating-an-installation-upgrade.md)
    -   [Buscar una característica o componente interrumpido](searching-for-a-broken-feature-or-component.md)
    -   [Windows Installer mensajes de error](windows-installer-error-messages.md)
    -   [Registro de solicitudes de reinicio](logging-of-reboot-requests.md)

-   Asegúrese de configurar e instalar la aplicación de forma segura.

    Para obtener más información, vea lo siguiente:

    -   [Directrices para crear instalaciones seguras](guidelines-for-authoring-secure-installations.md)
    -   [Directrices para proteger las acciones personalizadas](guidelines-for-securing-custom-actions.md)
    -   [Seguridad de la acción personalizada](custom-action-security.md)
    -   [Directrices para proteger paquetes en equipos bloqueados](guidelines-for-securing-packages-on-locked-down-computers.md)
    -   [Crear una instalación firmada completamente comprobada mediante automatización](authoring-a-fully-verified-signed-installation-using-automation.md)
    -   [Ejemplo de instalación de Windows Installer basado en URL](a-url-based-windows-installer-installation-example.md)
    -   [Crear la interfaz de usuario para la entrada de contraseña](authoring-the-user-interface-for-password-input.md)
    -   [Firmas digitales y Windows Installer](digital-signatures-and-windows-installer.md)
    -   [Uso de Windows Installer con UAC](using-windows-installer-with-uac.md)
    -   [Revisión de control de cuentas de usuario (UAC)](user-account-control--uac--patching.md)
    -   [Msicert.exe](msicert-exe.md)
    -   [**Propiedad AdminUser**](adminuser.md)
    -   [**Propiedad privileged**](privileged.md)
    -   [**Propiedad SecureCustomProperties**](securecustomproperties.md)

-   Cree una interfaz de usuario para presentar las opciones de configuración de la instalación y obtener información del usuario sobre el proceso de instalación pendiente.

    Para obtener más información, vea lo siguiente:

    -   [Acerca de la interfaz de usuario](about-the-user-interface.md)
    -   [Agregar controles y texto](adding-controls-and-text.md)
    -   [Crear un control ProgressBar](authoring-a-progressbar-control.md)
    -   [Creación de mensajes de solicitud de disco](authoring-disk-prompt-messages.md)
    -   [Creación de una instrucción condicional "espere...." Cuadro de mensaje](authoring-a-conditional-please-wait-------message-box.md)
    -   [Obtener una vista previa de la interfaz de usuario](previewing-the-user-interface.md)
    -   [Agregar texto almacenado en una propiedad](adding-text-stored-in-a-property.md)
    -   [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)

-   Cree una interfaz de usuario externa para presentar una interfaz de usuario personalizada con el fin de configurar la instalación y obtener información del usuario sobre el proceso de instalación pendiente.

    Para obtener más información, vea lo siguiente:

    -   [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia)
    -   [Supervisión de una instalación mediante MsiSetExternalUIRecord](monitoring-an-installation-using-msisetexternaluirecord.md)
    -   [Analizar mensajes de Windows Installer](parsing-windows-installer-messages.md)
    -   [Devolver valores de un controlador de interfaz de usuario externo](returning-values-from-an-external-user-interface-handler.md)
    -   [\_controlador INSTALLUI](/windows/desktop/api/Msi/nc-msi-installui_handlera)
    -   [Controlar los mensajes de progreso mediante MsiSetExternalUI](handling-progress-messages-using-msisetexternalui.md)
    -   [Supervisión de una instalación mediante MsiSetExternalUI](monitoring-an-installation-using-msisetexternalui.md)

-   Establezca la información de la aplicación en **Agregar o quitar programas** (ARP).

    Para obtener más información, vea lo siguiente:

    -   [Configuración de agregar o quitar programas con Windows Installer](configuring-add-remove-programs-with-windows-installer.md)
    -   [Agregar y quitar una aplicación y no dejar ningún seguimiento en el registro](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)
    -   [Desinstalar la clave del registro](uninstall-registry-key.md)

-   Escriba acciones personalizadas para controlar la lógica de configuración que no se admite de forma nativa en Windows Installer.

    Para obtener más información, vea lo siguiente:

    -   [Acciones personalizadas](custom-actions.md)
    -   [Lista de Resumen de todos los tipos de acciones personalizadas](summary-list-of-all-custom-action-types.md)
    -   [Directrices para proteger las acciones personalizadas](guidelines-for-securing-custom-actions.md)
    -   [Referencia de acción personalizada](custom-action-reference.md)
    -   [Usar una acción personalizada para crear cuentas de usuario en un equipo local](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [Usar una acción personalizada para iniciar un archivo instalado al final de la instalación](using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation.md)
    -   [Obtener acceso a una base de datos o una sesión desde una acción personalizada](accessing-a-database-or-session-from-inside-a-custom-action.md)
    -   [Obtener acceso a la sesión del instalador actual desde una acción personalizada](accessing-the-current-installer-session-from-inside-a-custom-action.md)
    -   [Cambiar el estado del sistema mediante una acción personalizada](changing-the-system-state-using-a-custom-action.md)

-   Arranque el Windows Installer en el equipo de un usuario.

    Para obtener más información, vea lo siguiente:

    -   [Arranque](bootstrapping.md)
    -   [Instmsi.exe](instmsi-exe.md)
    -   [Arranque de descarga de Internet](internet-download-bootstrapping.md)
    -   [Msistuff.exe](msistuff-exe.md)
    -   [Ejemplo de instalación de Windows Installer basado en URL](a-url-based-windows-installer-installation-example.md)
    -   [Configuración de los recursos de Setup.exe](configuring-the-setup-exe-resources.md)
    -   [Descarga de una instalación desde Internet](downloading-an-installation-from-the-internet.md)

-   Siga las instrucciones de Active Accessibility al escribir paquetes de Windows Installer.

    Para obtener más información, vea lo siguiente:

    -   [Accesibilidad](accessibility.md)

-   Prepárese para la internacionalización de una instalación de aplicación.

    Para obtener más información, vea lo siguiente:

    -   [Preparación de un paquete de Windows Installer para la localización](preparing-a-windows-installer-package-for-localization.md)
    -   [Localizar un paquete de Windows Installer](localizing-a-windows-installer-package.md)
    -   [Control de páginas de códigos (Windows Installer)](code-page-handling-windows-installer-.md)
    -   [Agregar recursos localizados](adding-localized-resources.md)
    -   [Un ejemplo de localización](a-localization-example.md)
    -   [Localizar las tablas de error y ActionText](localizing-the-error-and-actiontext-tables.md)
    -   [Localizar columnas de base de datos](localizing-database-columns.md)
    -   [Crear una base de datos con una página de códigos neutra](creating-a-database-with-a-neutral-code-page.md)
    -   [Control de páginas de códigos de tablas importadas y exportadas](code-page-handling-of-imported-and-exported-tables.md)
    -   [Localizar el idioma que se muestra en los cuadros de diálogo](localizing-the-language-displayed-by-dialogs.md)
    -   [Importación de tablas de error y de ActionText localizadas](importing-localized-error-and-actiontext-tables.md)
    -   [Actualización de las propiedades ProductLanguage y ProductCode](updating-productlanguage-and-productcode-properties.md)
    -   [Actualizar una secuencia de información de Resumen](updating-a-summary-information-stream.md)
    -   [Componentes completos](qualified-components.md)
    -   [Tabla UIText](uitext-table.md)
    -   [Administrar idioma y página de códigos](manage-language-and-codepage.md)
    -   [Comprobar la página de códigos de la base de datos de instalación](checking-the-installation-database-code-page.md)

-   Cree paquetes de Windows Installer para plataformas de 32 bits y de 64 bits.

    Para obtener más información, vea lo siguiente:

    -   [Windows Installer en sistemas operativos de 64 bits](windows-installer-on-64-bit-operating-systems.md)
    -   [Acciones personalizadas de 64 bits](64-bit-custom-actions.md)
    -   [Uso de acciones personalizadas de 64 bits](using-64-bit-custom-actions.md)
    -   [Usar módulos de combinación de 64 bits](using-64-bit-merge-modules.md)

-   Redistribuir los componentes Windows Installer compartidos y la lógica de configuración como módulos de combinación.

    Para obtener más información, vea lo siguiente:

    -   [Módulos de combinación](merge-modules.md)
    -   [Crear una transformación de idioma para un módulo de combinación de varios idiomas](authoring-a-language-transform-for-a-multiple-language-merge-module.md)
    -   [Aplicar un módulo de combinación configurable con personalizaciones](applying-a-configurable-merge-module-with-customizations.md)

-   Programar o suprimir los reinicios durante una instalación Windows Installer.

    Para obtener más información, vea lo siguiente:

    -   [Reinicios del sistema](system-reboots.md)
    -   [Registro de solicitudes de reinicio](logging-of-reboot-requests.md)

-   Cree actualizaciones o correcciones para una aplicación existente mediante la creación de una revisión.

    Para obtener más información, vea lo siguiente:

    -   [Crear una revisión de actualización pequeña](creating-a-small-update-patch.md)
    -   [Un pequeño ejemplo de revisión de actualización](a-small-update-patching-example.md)

-   Cree un paquete de propósito dual capaz de instalar una aplicación para solo el usuario actual o para todos los usuarios del equipo.

    Para obtener más información, vea lo siguiente:

    -   [Contexto de instalación](installation-context.md)
    -   [Creación de un solo paquete](single-package-authoring.md)
    -   [Ejemplo de creación de un solo paquete](single-package-authoring-example.md)

-   Personalizar servicios en el equipo mediante el Windows Installer.

    Para obtener más información, vea lo siguiente:

    -   [Uso de la configuración de servicios](using-services-configuration.md)

-   Proteja los recursos del equipo mediante el Windows Installer.

    Para obtener más información, vea lo siguiente:

    -   [Directrices para crear instalaciones seguras](guidelines-for-authoring-secure-installations.md)
    -   [Proteger recursos](securing-resources-.md)

-   Enumerar todos los componentes instalados en el equipo y obtener la ruta de acceso de la clave del componente.

    Para obtener más información, vea lo siguiente:

    -   [Enumerar componentes](enumerating-components-.md)

-   Instalar varios paquetes mediante el [*procesamiento de transacciones*](t-gly.md).

    Para obtener más información, vea lo siguiente:

    -   [Instalaciones de varios paquetes](multiple-package-installations.md)

-   Inserte una interfaz de usuario personalizada en el paquete de Windows Installer.

    Para obtener más información, vea lo siguiente:

    -   [Uso de la interfaz de usuario](using-the-user-interface.md)
    -   [Usar una interfaz de usuario incrustada](using-an-embedded-ui.md)

## <a name="it-professionals"></a>Profesionales de TI

Los profesionales de ti y los administradores personalizan e implementan paquetes de Windows Installer existentes. Estos usuarios reempaquetan las configuraciones de las aplicaciones existentes en Windows Installer paquetes de instalación, e instalan y mantienen imágenes administrativas de instalaciones de Windows Installer en redes.

-   Personalización de aplicaciones y configuración mediante la generación y aplicación de transformaciones de Windows Installer

    Para obtener más información, vea lo siguiente:

    -   [Personalización](customization.md)
    -   [Transformaciones de base de datos](database-transforms.md)
    -   [Ejemplo de transformación de personalización](a-customization-transform-example.md)
    -   [Combinaciones y transformaciones](merges-and-transforms.md)
    -   [Usar transformaciones para agregar recursos](using-transforms-to-add-resources.md)
    -   [Generar una transformación](generate-a-transform.md)
    -   [Opciones de la línea de comandos](command-line-options.md)
    -   [Msitran.exe](msitran-exe.md)
    -   [Aplicar una transformación](apply-a-transform.md)
    -   [Ver una transformación](view-a-transform.md)
    -   [Ver las diferencias entre dos bases de datos](view-differences-between-two-databases.md)
    -   [Aplicación de revisiones a aplicaciones personalizadas](patching-customized-applications.md)

-   Implementar un paquete de instalación de Windows Installer, una actualización o una revisión.

    Para obtener más información, vea lo siguiente:

    -   [Instalación de una aplicación](installing-an-application.md)
    -   [Revisiones y actualizaciones](patching-and-upgrades.md)
    -   [Transformaciones](transforms.md)
    -   [Instalación de un paquete con privilegios elevados para un no administrador](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Aplicar las actualizaciones principales mediante la revisión de la instalación local del producto](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md)
    -   [Aplicar las actualizaciones principales instalando el producto](applying-major-upgrades-by-installing-the-product.md)
    -   [Aplicar actualizaciones pequeñas mediante la revisión de la instalación local del producto](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [Aplicar actualizaciones pequeñas reinstalando el producto](applying-small-updates-by-reinstalling-the-product.md)
    -   [Aplicar actualizaciones pequeñas mediante la revisión de una imagen administrativa](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Aplicar revisiones a las instalaciones iniciales](patching-initial-installations.md)
    -   [Opciones de la línea de comandos](command-line-options.md)

-   Solucionar problemas de Windows Installer paquetes.

    Para obtener más información, vea lo siguiente:

    -   [Registro de Windows Installer](windows-installer-logging.md)
    -   [Comprobar la instalación de características, componentes y archivos](checking-the-installation-of-features-components-files.md)
    -   [Wilogutl.exe](wilogutl-exe.md)
    -   [Buscar una característica o componente interrumpido](searching-for-a-broken-feature-or-component.md)
    -   [Windows Installer mensajes de error](windows-installer-error-messages.md)
    -   [Msicert.exe](msicert-exe.md)

-   Use el scripting para consultar los paquetes de Windows Installer para obtener información sobre un producto y modificar la instalación.

    Para obtener más información, vea lo siguiente:

    -   [Interfaz de automatización](automation-interface.md)
    -   [Ejemplos de scripting Windows Installer](windows-installer-scripting-examples.md)
    -   [Usar Windows Installer con WMI](using-windows-installer-with-wmi.md)

-   Crear y mantener instalaciones administrativas.

    Para obtener más información, vea lo siguiente:

    -   [Instalación administrativa](administrative-installation.md)
    -   [Opciones de la línea de comandos](command-line-options.md)
    -   [**Propiedad AdminProperties**](adminproperties.md)
    -   [Aplicar actualizaciones pequeñas mediante la revisión de una imagen administrativa](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Aplicar un paquete de revisión a una instalación administrativa](applying-a-patch-package-to-an-administrative-installation.md)
    -   [Orden de ejecución de la acción](action-execution-order.md)
    -   [**Propiedad IsAdminPackage**](isadminpackage.md)
    -   [Orden de prioridad de propiedad](order-of-property-precedence.md)
    -   [**Propiedad AdminProperties**](adminproperties.md)

-   Hacer que una aplicación esté disponible para todos los usuarios de un equipo o solo para un usuario especificado.

    Para obtener más información, vea lo siguiente:

    -   [Contexto de instalación](installation-context.md)
    -   [**Propiedad ALLUSERS**](allusers.md)

-   Interpretar paquetes, instalar productos y configurar opciones de características mediante una línea de comandos.

    Para obtener más información, vea lo siguiente:

    -   [Opciones de la línea de comandos](command-line-options.md)
    -   [Establecer valores de propiedades públicas en la línea de comandos](setting-public-property-values-on-the-command-line.md)
    -   [Obtener y establecer propiedades](getting-and-setting-properties.md)
    -   [Reinstalación de una característica o aplicación](reinstalling-a-feature-or-application.md)
    -   [Aplicar actualizaciones pequeñas mediante la revisión de la instalación local del producto](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
    -   [Aplicar actualizaciones pequeñas reinstalando el producto](applying-small-updates-by-reinstalling-the-product.md)
    -   [Cambiar la ubicación de destino de un directorio](changing-the-target-location-for-a-directory.md)
    -   [Aplicar actualizaciones pequeñas mediante la revisión de una imagen administrativa](applying-small-updates-by-patching-an-administrative-image.md)
    -   [Aplicar las actualizaciones principales instalando el producto](applying-major-upgrades-by-installing-the-product.md)
    -   [Propiedades de configuración](property-reference.md)
    -   [Propiedades de opciones de instalación de características](property-reference.md)

-   Trabaje con la Directiva para administrar derechos y permisos de acceso.

    Para obtener más información, vea lo siguiente:

    -   [Directivas de equipo](machine-policies.md),
    -   [Directivas de usuario](user-policies.md),
    -   [Instalación de un paquete con privilegios elevados para un no administrador](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Anunciar una aplicación Per-User que se va a instalar con privilegios elevados](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [Usar una acción personalizada para crear cuentas de usuario en un equipo local](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [**Propiedad AdminUser**](adminuser.md)
    -   [**Propiedad privileged**](privileged.md)
    -   [**Propiedad EnableUserControl**](enableusercontrol.md)
    -   [**UserSID (propiedad)**](usersid.md)
    -   [**Propiedad SecureCustomProperties**](securecustomproperties.md)

-   Instalar varios paquetes mediante el [*procesamiento de transacciones*](t-gly.md).

    Para obtener más información, vea lo siguiente:

    -   [Instalaciones de varios paquetes](multiple-package-installations.md)

-   Incrustar una interfaz de usuario personalizada dentro de un paquete de Windows Installer.

    Para obtener más información, vea lo siguiente:

    -   [Uso de la interfaz de usuario](using-the-user-interface.md)
    -   [Usar una interfaz de usuario incrustada](using-an-embedded-ui.md)

## <a name="infrastructure-developers"></a>Desarrolladores de infraestructura

Los desarrolladores de infraestructura pueden crear plataformas unificadas para la implementación y administración de software que usa el servicio de Windows Installer. Pueden utilizar la interfaz de programación de Windows Installer para consultar, administrar y distribuir aplicaciones, revisiones y orígenes en un sistema.

-   Buscar, inventariar y consultar el estado, la información y los clientes de los componentes.

    Para obtener más información, vea lo siguiente:

    -   [Funciones específicas del componente](installer-function-reference.md)
    -   [Funciones de estado del sistema](installer-function-reference.md)
    -   [Instalador (objeto)](installer-object.md)
    -   [Objeto Product](product-object.md)
    -   [Patch (objeto)](patch-object.md)

-   Inventario y consulta para obtener información y el estado de los productos y las características.

    Para obtener más información, vea lo siguiente:

    -   [Productos y revisiones de inventario](inventory-products-and-patches-.md)
    -   [Funciones de estado del sistema](installer-function-reference.md)
    -   [Funciones de consulta de productos](installer-function-reference.md)
    -   [Instalador (objeto)](installer-object.md)
    -   [Objeto Product](product-object.md)
    -   [Patch (objeto)](patch-object.md)

-   Mejore la resistencia de origen mediante el Windows Installer para inventariar, consultar y modificar la lista de origen de las aplicaciones, las actualizaciones y las revisiones.

    Para obtener más información, vea lo siguiente:

    -   [**Propiedad SOURCELIST**](sourcelist.md)
    -   [**Resistencia de origen**](source-resiliency.md)
    -   [Funciones de instalación y configuración](installer-function-reference.md)
    -   [Instalador (objeto)](installer-object.md)
    -   [Objeto Product](product-object.md)
    -   [Patch (objeto)](patch-object.md)

-   Mejore la resistencia de origen mediante el Windows Installer para inventariar, consultar y modificar orígenes de medios.

    Para obtener más información, vea lo siguiente:

    -   [**Propiedad SOURCELIST**](sourcelist.md)
    -   [Resistencia de origen](source-resiliency.md)
    -   [Funciones de instalación y configuración](installer-function-reference.md)
    -   [Objeto Product](product-object.md)
    -   [Patch (objeto)](patch-object.md)

-   Inventario y consulta para obtener información y el estado de las revisiones.

    Para obtener más información, vea lo siguiente:

    -   [Productos y revisiones de inventario](inventory-products-and-patches-.md)
    -   [Referencia de funciones del instalador](installer-function-reference.md)
    -   [Patch (objeto)](patch-object.md)

-   Trabaje con la Directiva para administrar derechos y permisos de acceso.

    Para obtener más información, vea lo siguiente:

    -   [Directivas de equipo](machine-policies.md)
    -   [Directivas de usuario](user-policies.md)
    -   [Instalación de un paquete con privilegios elevados para un no administrador](installing-a-package-with-elevated-privileges-for-a-non-admin.md)
    -   [Anunciar una aplicación Per-User que se va a instalar con privilegios elevados](advertising-a-per-user-application-to-be-installed-with-elevated-privileges.md)
    -   [Usar una acción personalizada para crear cuentas de usuario en un equipo local](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
    -   [**Propiedad AdminUser**](adminuser.md)
    -   [**Propiedad privileged**](privileged.md)
    -   [**Propiedad EnableUserControl**](enableusercontrol.md)
    -   [**UserSID (propiedad)**](usersid.md)
    -   [**Propiedad SecureCustomProperties**](securecustomproperties.md)

 

 



