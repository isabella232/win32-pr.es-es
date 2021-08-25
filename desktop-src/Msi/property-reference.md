---
description: 'En esta sección se enumeran las propiedades definidas por Windows Installer:'
ms.assetid: c91119b9-59d5-4a33-91cd-d3ba63659d12
title: Referencia de propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e38f952632609090c69b85786c6aef64243d420b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481571"
---
# <a name="property-reference"></a>Referencia de propiedad

En esta sección se enumeran las propiedades definidas por Windows Installer:

-   [Propiedades de ubicación del componente](#component-location-properties)
-   [Propiedades de configuración](#configuration-properties)
-   [Propiedades de fecha y hora](#date-time-properties)
-   [Propiedades de las opciones de instalación de características](#feature-installation-options-properties)
-   [Propiedades de hardware](#hardware-properties)
-   [Propiedades de estado de instalación](#installation-status-properties)
-   [Propiedades del sistema operativo](#operating-system-properties)
-   [Propiedades de información del producto](#product-information-properties)
-   [Propiedades de actualización de información de resumen](#summary-information-update-properties)
-   [Propiedades de la carpeta del sistema](#system-folder-properties)
-   [Propiedades de información de usuario](#user-information-properties)

Las propiedades adicionales se pueden especificar mediante datos creados o acciones personalizadas. Las propiedades con nombres que no contienen letras minúsculas son propiedades públicas y se pueden especificar en la línea de comandos.

Para obtener información sobre los valores de la **clave** del Registro de desinstalación que proporcionan las propiedades del instalador, vea [Desinstalar clave del Registro](uninstall-registry-key.md).

## <a name="component-location-properties"></a>Propiedades de ubicación del componente

En la lista siguiente se proporcionan vínculos a más información sobre las propiedades de ubicación del componente.



| Propiedad                                                            | Descripción                                                                                                                                                                                                        |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OriginalDatabase**](originaldatabase.md)<br/>             | El instalador establece esta propiedad en la base de datos iniciada desde , la base de datos en el origen o la base de datos almacenada en caché.<br/>                                                                                     |
| [**ParentOriginalDatabase**](parentoriginaldatabase.md)<br/> | El instalador establece esta propiedad para las instalaciones ejecutadas por una [acción de instalación](concurrent-installations.md) simultánea.<br/>                                                                             |
| [**SourceDir**](sourcedir.md)<br/>                           | Directorio raíz que contiene los archivos de origen.<br/>                                                                                                                                                          |
| [**TARGETDIR**](targetdir.md)<br/>                           | Especifica el directorio de destino raíz para la instalación. Durante una [instalación administrativa,](administrative-installation.md) esta propiedad es la ubicación para copiar el paquete de instalación.<br/> |



 

## <a name="configuration-properties"></a>Configuration Properties

En la lista siguiente se proporcionan vínculos a más información sobre otras propiedades configurables.



| Propiedad                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ACCIÓN**](action.md)<br/>                                                     | Acción inicial a la que se llama después de inicializar el instalador.<br/>                                                                                                                                                                                                                                                                                                                          |
| [**ALLUSERS**](allusers.md)<br/>                                                 | Determina dónde se almacena la información de configuración.<br/>                                                                                                                                                                                                                                                                                                                              |
| [**ARPAUTHORIZEDCDFPREFIX**](arpauthorizedcdfprefix.md)<br/>                     | Dirección URL del canal de actualización de una aplicación.<br/>                                                                                                                                                                                                                                                                                                                                      |
| [**ARPCOMMENTS**](arpcomments.md)<br/>                                           | Proporciona comentarios para **agregar o quitar programas** en **Panel de control**.<br/>                                                                                                                                                                                                                                                                                                         |
| [**ARPCONTACT**](arpcontact.md)<br/>                                             | Proporciona Contact para agregar **o quitar programas** en **Panel de control**.<br/>                                                                                                                                                                                                                                                                                                          |
| [**ARPINSTALLLOCATION**](arpinstalllocation.md)<br/>                             | Ruta de acceso completa a la carpeta principal de una aplicación.<br/>                                                                                                                                                                                                                                                                                                                      |
| [**ARPNOMODIFY**](arpnomodify.md)<br/>                                           | Deshabilita la funcionalidad que modifica un producto.<br/>                                                                                                                                                                                                                                                                                                                                    |
| [**ARPNOREMOVE**](arpnoremove.md)<br/>                                           | Deshabilita la funcionalidad que quita un producto.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**ARPNOREPAIR**](arpnorepair.md)<br/>                                           | Deshabilita el botón **Reparar** en el Asistente para programas.<br/>                                                                                                                                                                                                                                                                                                                             |
| [**ARPPRODUCTICON**](arpproducticon.md)<br/>                                     | Especifica el icono principal del paquete de instalación.<br/>                                                                                                                                                                                                                                                                                                                           |
| [**ARPREADME**](arpreadme.md)<br/>                                               | Proporciona un **Archivo Léame** para **agregar o quitar programas** en **Panel de control**.<br/>                                                                                                                                                                                                                                                                                                     |
| [**ARPSIZE**](arpsize.md)<br/>                                                   | Tamaño estimado de una aplicación en kilobytes.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**ARPSYSTEMCOMPONENT**](arpsystemcomponent.md)<br/>                             | Impide la presentación de una aplicación en **la lista Agregar o** quitar programas.<br/>                                                                                                                                                                                                                                                                                                         |
| [**ARPURLINFOABOUT**](arpurlinfoabout.md)<br/>                                   | Dirección URL de la página principal de una aplicación.<br/>                                                                                                                                                                                                                                                                                                                                           |
| [**ARPURLUPDATEINFO**](arpurlupdateinfo.md)<br/>                                 | Dirección URL de la información de actualización de la aplicación.<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**AVAILABLEFREEREG**](availablefreereg.md)<br/>                                 | Espacio del Registro (en kilobytes) que requiere una aplicación. Usado por [la acción AllocateRegistrySpace](allocateregistryspace-action.md).<br/>                                                                                                                                                                                                                                              |
| [**UNIDAD \_ CCP**](ccp-drive.md)<br/>                                              | Ruta de acceso raíz para los productos aptos para CCP.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**DefaultUIFont**](defaultuifont.md)<br/>                                       | Estilo de fuente predeterminado utilizado para los controles.<br/>                                                                                                                                                                                                                                                                                                                                              |
| [**DISABLEADVTSHORTCUTS**](disableadvtshortcuts.md)<br/>                         | Establezca esta opción para deshabilitar la generación de los accesos directos específicos que [admiten la instalación a petición.](installation-on-demand.md)<br/>                                                                                                                                                                                                                                                            |
| [**DISABLEMEDIA**](-disablemedia.md)<br/>                                        | Impide que el instalador registre orígenes multimedia, como CD-ROM, como orígenes válidos para el producto.<br/>                                                                                                                                                                                                                                                                        |
| [**DISABLEROLLBACK**](-disablerollback.md)<br/>                                  | Deshabilita la reversión de la configuración actual.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**EXECUTEACTION**](executeaction.md)<br/>                                       | Acción de nivel superior que inicia ExecuteAction.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**EXECUTEMODE**](executemode.md)<br/>                                           | Modo de ejecución que realiza el instalador.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**FASTOEM**](fastoem.md)<br/>                                                   | Mejora el rendimiento de la instalación en escenarios específicos de OEM.<br/>                                                                                                                                                                                                                                                                                                                    |
| [**INSTALLLEVEL**](installlevel.md)<br/>                                         | Nivel inicial donde se instalan las características.<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**LIMITUI**](limitui.md)<br/>                                                   | El nivel de interfaz de usuario está límite como Básico.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**LOGACTION**](logaction.md)<br/>                                               | Lista de nombres de acción que se registrarán.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**MEDIAPACKAGEPATH**](mediapackagepath.md)<br/>                                 | Esta propiedad debe establecerse en la ruta de acceso relativa si el paquete de instalación no se encuentra en la raíz del CD-ROM.<br/>                                                                                                                                                                                                                                                               |
| [**MSIARPSETTINGSIDENTIFIER**](msiarpsettingsidentifier.md)<br/>                 | Esta propiedad opcional contiene una lista delimitada por punto y coma de las ubicaciones del Registro donde la aplicación almacena la configuración y las preferencias de un usuario. Disponible con Windows Installer 4.0.<br/>                                                                                                                                                                                        |
| [**MSIDISABLEEEUI**](msidisableeeui.md)<br/>                                     | Deshabilite la interfaz de usuario incrustada para la instalación.<br/> **[Windows Installer 4.0 y versiones anteriores:](not-supported-in-windows-installer-4-0.md)** No se admite.<br/>                                                                                                                                                                                                           |
| [**MSIFASTINSTALL**](msifastinstall.md)<br/>                                     | Reduzca el tiempo necesario para instalar un paquete Windows Installer.<br/> **[Windows instalador 4.5 y versiones anteriores:](not-supported-in-windows-installer-4-5.md)** No se admite.<br/>                                                                                                                                                                                              |
| [**MSIINSTALLPERUSER**](msiinstallperuser.md)<br/>                               | Solicita que el Windows instalador instale el paquete solo para el usuario actual.<br/> **[Windows instalador 4.5 y versiones anteriores:](not-supported-in-windows-installer-4-5.md)** No se admite.<br/>                                                                                                                                                                                  |
| [**MSINODISABLEMEDIA**](msinodisablemedia.md)<br/>                               | Establezca esta propiedad para evitar que el instalador establezca la [**propiedad DISABLEMEDIA.**](-disablemedia.md)<br/>                                                                                                                                                                                                                                                                        |
| [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md)<br/>   | Establezca esta propiedad en 1 (uno) en [](property-table.md) la línea de comandos [](small-updates.md) o en la tabla de propiedades para aplicar las reglas del componente de actualización durante pequeñas actualizaciones y actualizaciones [secundarias](minor-upgrades.md) de un producto específico. Disponible a partir Windows Installer 3.0.<br/>                                                                                     |
| [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md)<br/> | Cuando esta propiedad se ha establecido en 1, el instalador puede anular el registro y desinstalar los componentes redundantes para evitar dejar componentes huérfanos en el equipo.<br/> **[Windows Installer 4.0 y versiones anteriores:](not-supported-in-windows-installer-4-0.md)** No se admite.<br/>                                                                                                  |
| [**PRIMARYFOLDER**](primaryfolder.md)<br/>                                       | Permite al autor designar una carpeta principal para una instalación. Se usa para determinar los valores de las propiedades [**PrimaryVolumePath**](primaryvolumepath.md), [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md), [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md)y [**PrimaryVolumeSpaceRemaining.**](primaryvolumespaceremaining.md)<br/> |
| [**Con privilegios**](privileged.md)<br/>                                             | Ejecuta una instalación con privilegios elevados.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**PROMPTROLLBACKCOST**](promptrollbackcost.md)<br/>                             | Acción si no hay suficiente espacio en disco para la instalación.<br/>                                                                                                                                                                                                                                                                                                                   |
| [**REINICIAR**](reboot.md)<br/>                                                     | Fuerza o suprime un reinicio.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| [**REBOOTPROMPT**](rebootprompt.md)<br/>                                         | Suprime la presentación de solicitudes de reinicio al usuario. Los reinicios necesarios se suceden automáticamente.<br/>                                                                                                                                                                                                                                                                     |
| [**ROOTDRIVE**](rootdrive.md)<br/>                                               | Unidad predeterminada para una instalación.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**SEQUENCE**](sequence.md)<br/>                                                 | Tabla que tiene el esquema de tabla de secuencia.<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**SHORTFILENAMES**](shortfilenames.md)<br/>                                     | Hace que se utilicen nombres de archivo cortos.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**TRANSFORMA**](transforms.md)<br/>                                             | Lista de transformaciones que se aplicarán a una base de datos.<br/>                                                                                                                                                                                                                                                                                                                                    |
| [**TRANSFORMSATSOURCE**](transformsatsource.md)<br/>                             | Informa al instalador de que las transformaciones de un producto residen en el origen.<br/>                                                                                                                                                                                                                                                                                                      |
| [**TRANSFORMSSECURE**](transformssecure.md)<br/>                                 | Al establecer la [**propiedad TRANSFORMSECURE**](transformssecure.md) en 1 (uno), se informa al instalador de que las transformaciones se almacenarán en caché localmente en el equipo del usuario en una ubicación en la que el usuario no tenga acceso de escritura.<br/>                                                                                                                                                           |
| [**MsiLogFileLocation**](msilogfilelocation.md)<br/>                             | El instalador establece el valor de esta propiedad en la ruta de acceso completa del archivo de registro, cuando se ha habilitado el registro. Esta propiedad está disponible a partir de Windows Installer 4.0.<br/>                                                                                                                                                                                                     |
| [**MsiLogging**](msilogging.md)<br/>                                             | Establece el modo de registro predeterminado para el paquete Windows Installer. Esta propiedad está disponible a partir de Windows Installer 4.0.<br/>                                                                                                                                                                                                                                                   |
| [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md)<br/>                 | Establezca esta propiedad en 1 para solicitar que el instalador use información de usuario real al establecer la [**propiedad AdminUser.**](adminuser.md) Esta propiedad está disponible a partir de Windows Installer 4.0.<br/>                                                                                                                                                                         |



 

## <a name="date-time-properties"></a>Propiedades de fecha y hora

Las [**propiedades Fecha**](date.md) y [**Hora**](time.md) son propiedades activas que el instalador establece cuando se extraen los datos.



| Propiedad                        | Descripción                  |
|---------------------------------|------------------------------|
| [**Date**](date.md)<br/> | Fecha actual.<br/> |
| [**Hora**](time.md)<br/> | La hora actual.<br/> |



 

## <a name="feature-installation-options-properties"></a>Propiedades de las opciones de instalación de características

En la lista siguiente se proporcionan vínculos a más información sobre las propiedades de las opciones de instalación de características.



| Propiedad                                                                | Descripción                                                                                                                                                                       |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ADDDEFAULT**](adddefault.md)<br/>                             | Lista de características que se instalarán en la configuración predeterminada.<br/>                                                                                                         |
| [**ADDLOCAL**](addlocal.md)<br/>                                 | Lista de características que se instalarán localmente.<br/>                                                                                                                              |
| [**ADDSOURCE**](addsource.md)<br/>                               | Lista de características que se ejecutarán desde el origen.<br/>                                                                                                                                |
| [**ANUNCIAR**](advertise.md)<br/>                               | Lista de características que se anunciarán.<br/>                                                                                                                                     |
| [**COMPADDDEFAULT**](compadddefault.md)<br/>                     | Lista de componentes que se instalarán en la configuración predeterminada.<br/>                                                                                                       |
| [**COMPADDLOCAL**](compaddlocal.md)<br/>                         | Lista de los IDs de componente que se instalarán localmente.<br/>                                                                                                                         |
| [**COMPADDSOURCE**](compaddsource.md)<br/>                       | Lista de los IDs de componente que se ejecutarán desde los medios de origen.<br/>                                                                                                                        |
| [**FILEADDDEFAULT**](fileadddefault.md)<br/>                     | Lista de claves de archivo para los archivos que se instalarán en la configuración predeterminada.<br/>                                                                                              |
| [**FILEADDLOCAL**](fileaddlocal.md)<br/>                         | Lista de claves de archivo para que los archivos se ejecuten localmente.<br/>                                                                                                                         |
| [**FILEADDSOURCE**](fileaddsource.md)<br/>                       | Lista de claves de archivo que se ejecutarán desde el medio de origen.<br/>                                                                                                                     |
| [**MSIDISABLELUAPATCHING**](msidisableluapatching.md)<br/>       | Al establecer esta propiedad se evita la aplicación de revisiones de usuario con privilegios mínimos (LUA) de una aplicación.<br/>                                                                                 |
| [**MsiPatchRemovalList**](msipatchremovallist.md)<br/>           | Lista de revisiones que se quitarán durante la instalación.<br/>                                                                                                                 |
| [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)<br/> | Especifica si el paquete usa la funcionalidad [Restart Manager](../rstmgr/restart-manager-portal.md) o [FilesInUse.](filesinuse-dialog.md)<br/>                                          |
| [**MSIDISABLERMRESTART**](msidisablermrestart.md)<br/>           | Especifica cómo se deben apagar y reiniciar las aplicaciones o servicios que usan actualmente archivos afectados por una actualización para habilitar la instalación de la actualización.<br/> |
| [**MSIRMSHUTDOWN**](msirmshutdown.md)<br/>                       | Especifica cómo se deben apagar las aplicaciones o servicios que usan actualmente archivos afectados por una actualización para habilitar la instalación de la actualización.<br/>               |
| [**MSIPATCHREMOVE**](msipatchremove.md)<br/>                     | Al establecer esta propiedad se quitan las revisiones.<br/>                                                                                                                                 |
| [**PARCHE**](patch.md)<br/>                                       | Al establecer esta propiedad se aplica una revisión.<br/>                                                                                                                                 |
| [**REINSTALAR**](reinstall.md)<br/>                               | Lista de características que se reinstalarán.<br/>                                                                                                                                    |
| [**REINSTALLMODE**](reinstallmode.md)<br/>                       | Cadena que contiene letras que especifican el tipo de reinstalación que se debe realizar.<br/>                                                                                          |
| [**ELIMINAR**](remove.md)<br/>                                     | Lista de características que se quitarán.<br/>                                                                                                                                        |



 

## <a name="hardware-properties"></a>Propiedades de hardware

En la lista siguiente se identifican las propiedades de hardware que el Windows establece en el inicio.




| Propiedad | Descripción | 
|----------|-------------|
| <a href="alpha.md"><strong>Alpha</strong></a><br /> | Nivel de procesador numérico cuando se ejecuta en un procesador Alfa.<br /><blockquote>[!Note]<br />Esta propiedad está obsoleta, la plataforma Alpha no es compatible con Windows Installer.</blockquote><br /> | 
| <a href="borderside.md"><strong>BorderSide</strong></a><br /> | Ancho de los bordes de la ventana, en píxeles.<br /> | 
| <a href="bordertop.md"><strong>BorderTop</strong></a><br /> | Alto de los bordes de la ventana, en píxeles.<br /> | 
| <a href="captionheight.md"><strong>CaptionHeight</strong></a><br /> | Alto del área de título normal, en píxeles.<br /> | 
| <a href="colorbits.md"><strong>ColorBits</strong></a><br /> | Número de bits de color adyacentes para cada píxel.<br /> | 
| <a href="intel.md"><strong>Intel</strong></a><br /> | Nivel de procesador numérico cuando se ejecuta en un procesador Intel.<br /> | 
| <a href="intel64.md"><strong>Intel64</strong></a><br /> | Nivel de procesador numérico cuando se ejecuta en un procesador Itanium.<br /> | 
| <a href="msix64.md"><strong>Msix64</strong></a><br /> | Nivel de procesador numérico cuando se ejecuta en un procesador x64.<br /> | 
| <a href="physicalmemory.md"><strong>PhysicalMemory</strong></a><br /> | Tamaño de la RAM instalada, en megabytes.<br /> | 
| <a href="screenx.md"><strong>ScreenX</strong></a><br /> | Ancho de la pantalla, en píxeles.<br /> | 
| <a href="screeny.md"><strong>ScreenY</strong></a><br /> | Alto de la pantalla, en píxeles.<br /> | 
| <a href="textheight.md"><strong>TextHeight</strong></a><br /> | Alto de caracteres, en unidades lógicas.<br /> | 
| <a href="virtualmemory.md"><strong>VirtualMemory</strong></a><br /> | Cantidad de espacio disponible en el archivo de página, en megabytes.<br /> | 




 

## <a name="installation-status-properties"></a>Propiedades de estado de instalación

En la lista siguiente se proporcionan vínculos a más información sobre las propiedades de estado que actualiza el instalador durante la instalación.



| Propiedad                                                                      | Descripción                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AFTERREBOOT**](afterreboot.md)<br/>                                 | Indica que la instalación actual sigue a un reinicio que invoca [la acción ForceReboot.](forcereboot-action.md)<br/>                                                                                                                                                |
| [**CostingComplete**](costingcomplete.md)<br/>                         | Indica si se ha completado el costo del espacio en disco.<br/>                                                                                                                                                                                                             |
| [**Instalado**](installed.md)<br/>                                     | Indica que un producto ya está instalado.<br/>                                                                                                                                                                                                                |
| [**MSICHECKCRCS**](msicheckcrcs.md)<br/>                               | El instalador realiza una CRC en los archivos solo si se establece la propiedad [**MSICHECKCRCS.**](msicheckcrcs.md)<br/>                                                                                                                                                           |
| [**MsiRestartManagerSessionKey**](msirestartmanagersessionkey.md)<br/> | El instalador establece esta propiedad en la clave de sesión de la [sesión del Administrador de](../rstmgr/restart-manager-portal.md) reinicio.<br/>                                                                                                                                                         |
| [**MsiRunningElevated**](msirunningelevated-.md)<br/>                  | El instalador establece el valor de esta propiedad en 1 cuando el instalador se ejecuta con [*privilegios*](e-gly.md) elevados.<br/>                                                                                                                   |
| [**MsiSystemRebootPending**](msisystemrebootpending.md)<br/>           | El instalador establece esta propiedad en 1 si hay un reinicio del sistema operativo pendiente actualmente.<br/>                                                                                                                                                              |
| [**MsiUIHideCancel**](msiuihidecancel.md)<br/>                         | El instalador establece [**MsiUIHideCancel**](msiuihidecancel.md) en 1 cuando el nivel de instalación interno incluye **INSTALLUILEVEL \_ HIDECANCEL**.<br/>                                                                                                                   |
| [**MsiUIProgressOnly**](msiuiprogressonly.md)<br/>                     | El instalador establece [**MsiUIProgressOnly**](msiuiprogressonly.md) en 1 cuando el nivel de instalación interno incluye **INSTALLUILEVEL \_ PROGRESSONLY**.<br/>                                                                                                             |
| [**MsiUISourceResOnly**](msiuisourceresonly.md)<br/>                   | [**MsiUISourceResOnly**](msiuisourceresonly.md) a 1 (uno) cuando el nivel de instalación interno incluye **INSTALLUILEVEL \_ SOURCERESONLY**.<br/>                                                                                                                       |
| [**NOCOMPANYNAME**](nocompanyname.md)<br/>                             | Suprime la configuración automática de la [**propiedad COMPANYNAME.**](companyname.md)<br/>                                                                                                                                                                          |
| [**NOUSERNAME**](nousername.md)<br/>                                   | Suprime la configuración automática de la [**propiedad USERNAME.**](username.md)<br/>                                                                                                                                                                                |
| [**OutOfDiskSpace**](outofdiskspace.md)<br/>                           | Espacio en disco insuficiente para dar cabida a la instalación.<br/>                                                                                                                                                                                                      |
| [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md)<br/>                   | Espacio en disco insuficiente con la reversión desactivada.<br/>                                                                                                                                                                                                             |
| [**Preseleccionado**](preselected.md)<br/>                                 | Las características ya están seleccionadas.<br/>                                                                                                                                                                                                                                |
| [**PrimaryVolumePath**](primaryvolumepath.md)<br/>                     | El instalador establece el valor de esta propiedad en la ruta de acceso del volumen que la [**propiedad PRIMARYFOLDER**](primaryfolder.md) designa.<br/>                                                                                                                  |
| [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md)<br/> | El instalador establece el valor de esta propiedad en una cadena que representa el número total de bytes disponibles en el volumen al que hace referencia la propiedad [**PrimaryVolumePath.**](primaryvolumepath.md)<br/>                                                      |
| [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md)<br/> | El instalador establece el valor de esta propiedad en una cadena que representa el número total de bytes restantes en el volumen al que hace referencia la propiedad [**PrimaryVolumePath**](primaryvolumepath.md) si están instaladas todas las características seleccionadas actualmente.<br/> |
| [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md)<br/>   | El instalador establece el valor de esta propiedad en una cadena que representa el número total de bytes requerido por todas las características seleccionadas actualmente en el volumen al que hace referencia la propiedad [**PrimaryVolumePath.**](primaryvolumepath.md)<br/>                    |
| [**ProductLanguage**](productlanguage.md)<br/>                         | Identificador de idioma numérico (LANGID) para la base de datos. (OBLIGATORIO)<br/>                                                                                                                                                                                             |
| [**ReplacedInUseFiles**](replacedinusefiles.md)<br/>                   | Establezca si el instalador se instala en un archivo que se mantiene en uso.<br/>                                                                                                                                                                                          |
| [**REANUDAR**](resume.md)<br/>                                           | Se reanudó la instalación.<br/>                                                                                                                                                                                                                                         |
| [**RollbackDisabled**](rollbackdisabled.md)<br/>                       | El instalador establece esta propiedad cuando la reversión está deshabilitada.<br/>                                                                                                                                                                                                   |
| [**UILevel**](uilevel.md)<br/>                                         | Indica el nivel de interfaz de usuario.<br/>                                                                                                                                                                                                                           |
| [**UpdateStarted**](updatestarted.md)<br/>                             | Establezca cuándo han comenzado los cambios en el sistema para esta instalación.<br/>                                                                                                                                                                                              |
| [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md)<br/>               | Lo establece el instalador cuando una actualización quita una aplicación.<br/>                                                                                                                                                                                                  |
| [**VersionMsi**](versionmsi.md)<br/>                                   | El instalador establece esta propiedad en la versión de Windows Installer que se ejecuta durante la instalación.<br/>                                                                                                                                                     |



 

## <a name="operating-system-properties"></a>Propiedades del sistema operativo

En la lista siguiente se proporcionan vínculos a más información sobre las propiedades del sistema operativo que el instalador establece en el inicio.



| Nombre de la propiedad                                                                             | Breve descripción                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdminUser**](adminuser.md)<br/>                                                 | Establezca en Windows 2000 si el usuario tiene privilegios de administrador.<br/>                                                                                                                                                                                                                        |
| [**ComputerName**](computername.md)<br/>                                           | Nombre de equipo del sistema actual.<br/>                                                                                                                                                                                                                                                 |
| [**MsiNetAssemblySupport**](msinetassemblysupport.md)<br/>                         | En los sistemas que admiten ensamblados de Common Language Runtime, el instalador establece el valor de esta propiedad en la versión de archivo de fusion.dll. El instalador no establece esta propiedad si el sistema operativo no admite ensamblados de Common Language Runtime.<br/>                   |
| [**MsiNTProductType**](msintproducttype.md)<br/>                                   | Indica el tipo Windows producto.<br/>                                                                                                                                                                                                                                                  |
| [**MsiNTSuiteBackOffice**](msintsuitebackoffice.md)<br/>                           | En Windows 2000 y versiones posteriores, el instalador establece esta propiedad en 1 (uno) solo si están instalados los componentes de Microsoft BackOffice.<br/>                                                                                                                                      |
| [**MsiNTSuiteDataCenter**](msintsuitedatacenter.md)<br/>                           | En Windows 2000 y versiones posteriores, el instalador establece esta propiedad en 1 (uno) solo si Windows 2000 Datacenter Server está instalado.<br/>                                                                                                                                        |
| [**MsiNTSuiteEnterprise**](msintsuiteenterprise.md)<br/>                           | En Windows 2000 y versiones posteriores, el instalador establece esta propiedad en 1 (uno) solo si Windows 2000 Advanced Server está instalado.<br/>                                                                                                                                          |
| [**MsiNTSuitePersonal**](msintsuitepersonal.md)<br/>                               | En Windows XP y sistemas operativos posteriores, el instalador establece esta propiedad en 1 (uno) solo si el sistema operativo es Inicio (no Professional).<br/>                                                                                                                                      |
| [**MsiNTSuiteSmallBusiness**](msintsuitesmallbusiness.md)<br/>                     | En Windows sistemas operativos 2000 y versiones posteriores, el instalador establece esta propiedad en 1 (uno) solo si está instalado Microsoft Small Business Server.<br/>                                                                                                                                       |
| [**MsiNTSuiteSmallBusinessRestricted**](msintsuitesmallbusinessrestricted.md)<br/> | En Windows 2000 y versiones posteriores, el instalador establece esta propiedad en 1 (uno) solo si Microsoft Small Business Server está instalado con la licencia de cliente restrictiva.<br/>                                                                                                   |
| [**MsiNTSuiteWebServer**](msintsuitewebserver.md)<br/>                             | En Windows 2000 y versiones posteriores, el instalador establece la propiedad [**MsiNTSuiteWebServer**](msintsuitewebserver.md) en 1 (uno) si está instalada la edición web de Windows Server 2003. Solo está disponible con la Windows Server 2003 del instalador Windows.<br/> |
| [**MsiTabletPC**](msitabletpc.md)<br/>                                             | El instalador establece esta propiedad en un valor distinto de cero si el sistema operativo actual Windows XP Tablet PC Edition.<br/>                                                                                                                                                                 |
| [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md)<br/>                     | En los sistemas que admiten ensamblados Win32, el instalador establece el valor de esta propiedad en la versión de archivo de sxs.dll. El instalador no establece esta propiedad si el sistema operativo no admite ensamblados Win32.<br/>                                                          |
| [**OLEAdvtSupport**](oleadvtsupport.md)<br/>                                       | Establezca si OLE admite Windows Instalador.<br/>                                                                                                                                                                                                                                           |
| [**RedirectedDllSupport**](redirecteddllsupport.md)<br/>                           | El instalador establece la [**propiedad RedirectedDllSupport**](redirecteddllsupport.md) si el sistema que realiza la instalación admite [componentes aislados.](isolated-components.md)<br/>                                                                                              |
| [**RemoteAdminTS**](remoteadmints.md)<br/>                                         | El instalador establece la [**propiedad RemoteAdminTS**](remoteadmints.md) cuando el sistema es un servidor de administración remota que ejecuta el servicio de rol de Terminal Server.<br/>                                                                                                                   |
| [**ServicePackLevel**](servicepacklevel.md)<br/>                                   | Número de versión del Service Pack del sistema operativo.<br/>                                                                                                                                                                                                                             |
| [**ServicePackLevelMinor**](servicepacklevelminor.md)<br/>                         | Número de versión secundaria del Service Pack del sistema operativo.<br/>                                                                                                                                                                                                                       |
| [**SharedWindows**](sharedwindows.md)<br/>                                         | Establezca cuando el sistema esté funcionando como Compartido Windows.<br/>                                                                                                                                                                                                                                  |
| [**ShellAdvtSupport**](shelladvtsupport.md)<br/>                                   | Establezca si el shell admite la publicidad de características.<br/>                                                                                                                                                                                                                                       |
| [**SystemLanguageID**](systemlanguageid.md)<br/>                                   | Identificador de idioma predeterminado del sistema.<br/>                                                                                                                                                                                                                                          |
| [**TerminalServer**](terminalserver.md)<br/>                                       | Se establece cuando el sistema es un servidor que ejecuta el servicio de rol de Terminal Server.<br/>                                                                                                                                                                                                            |
| [**TTCSupport**](ttcsupport.md)<br/>                                               | Indica si el sistema operativo admite el uso de archivos .ttc (colecciones de fuentes de tipo true).<br/>                                                                                                                                                                                            |
| [**Versión9X**](version9x.md)<br/>                                                 | Número de versión del Windows operativo.<br/>                                                                                                                                                                                                                                     |
| [**VersionDatabase**](versiondatabase.md)<br/>                                     | Versión numérica de la base de datos de la instalación actual.<br/>                                                                                                                                                                                                                                |
| [**VersionNT**](versionnt.md)<br/>                                                 | Número de versión del sistema operativo.<br/>                                                                                                                                                                                                                                             |
| [**VersionNT64**](versionnt64.md)<br/>                                             | Número de versión del sistema operativo si el sistema se ejecuta en un equipo de 64 bits.<br/>                                                                                                                                                                                               |
| [**Windows compilación**](windowsbuild.md)<br/>                                          | Número de compilación del sistema operativo.<br/>                                                                                                                                                                                                                                                |



 

## <a name="product-information-properties"></a>Propiedades de información del producto

En la lista siguiente se proporcionan vínculos a más información sobre las propiedades específicas del producto especificadas en la [tabla de propiedades](property-table.md).



| Nombre de la propiedad                                                  | Breve descripción                                                                                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**ARPHELPLINK**](arphelplink.md)<br/>                  | Dirección de Internet o dirección URL del soporte técnico.<br/>                                                                                 |
| [**ARPHELPTELEPHONE**](arphelptelephone.md)<br/>        | Números de teléfono de soporte técnico.<br/>                                                                                               |
| [**DiskPrompt**](diskprompt.md)<br/>                    | Cadena mostrada por un cuadro de mensaje que solicita un disco.<br/>                                                                     |
| [**IsAdminPackage**](isadminpackage.md)<br/>            | Establezca en 1 (uno) si la instalación actual se ejecuta desde un paquete creado a través de una instalación administrativa.<br/>           |
| [**LeftUnit**](leftunit.md)<br/>                        | Coloca las unidades a la izquierda del número.<br/>                                                                                        |
| [**Fabricante**](manufacturer.md)<br/>                | Nombre del fabricante de la aplicación. (Requerido)<br/>                                                                               |
| [**MediaSourceDir**](mediasourcedir.md)<br/>            | El instalador establece esta propiedad en 1 (una) cuando la instalación usa un origen multimedia, como un CD-ROM.<br/>                       |
| [**MSIINSTANCEGUID**](msiinstanceguid.md)<br/>          | La presencia de esta propiedad indica que una transformación de cambio de código de producto está registrada en el producto.<br/>                   |
| [**MSINEWINSTANCE**](msinewinstance.md)<br/>            | Esta propiedad indica la instalación de una nueva instancia de un producto con transformaciones de instancia.<br/>                              |
| [**ParentProductCode**](parentoriginaldatabase.md)<br/> | El instalador establece esta propiedad para las instalaciones en las que [se ejecuta una acción de instalación](concurrent-installations.md) simultánea.<br/> |
| [**PIDTemplate**](pidtemplate.md)<br/>                  | Cadena utilizada como plantilla para la [**propiedad PIDKEY.**](pidkey.md)<br/>                                                           |
| [**ProductCode**](productcode.md)<br/>                  | Identificador único para una versión de producto específica. (Requerido)<br/>                                                                 |
| [**Productname**](productname.md)<br/>                  | Nombre legible de una aplicación. (Requerido)<br/>                                                                              |
| [**ProductState**](productstate.md)<br/>                | Establezca en el estado instalado de un producto.<br/>                                                                                       |
| [**ProductVersion**](productversion.md)<br/>            | Formato de cadena de la versión del producto como un valor numérico. (Requerido)<br/>                                                            |
| [**UpgradeCode**](upgradecode.md)<br/>                  | GUID que representa un conjunto relacionado de productos.<br/>                                                                              |



 

## <a name="summary-information-update-properties"></a>Propiedades de actualización de información de resumen

Las siguientes propiedades solo se establecen mediante transformaciones en archivos .msp que se usan para actualizar el flujo de información de resumen de una imagen administrativa.



| Propiedad                                                              | Descripción                                                                                                                  |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**PATCHNEWPACKAGECODE**](patchnewpackagecode.md)<br/>         | El valor de esta propiedad se escribe en la propiedad [**Resumen del número de revisión.**](revision-number-summary.md)<br/> |
| [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md)<br/> | El valor de esta propiedad se escribe en la [**propiedad Resumen de**](comments-summary.md) comentarios.<br/>               |
| [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md)<br/>   | El valor de esta propiedad se escribe en la [**propiedad Resumen del**](subject-summary.md) sujeto.<br/>                 |



 

## <a name="system-folder-properties"></a>Propiedades de la carpeta del sistema

En la lista siguiente se proporcionan vínculos a más información sobre las carpetas del sistema que el instalador establece durante la instalación.



| Propiedad                                                        | Descripción                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**AdminToolsFolder**](admintoolsfolder.md)<br/>         | Ruta de acceso completa al directorio que contiene herramientas administrativas.<br/>         |
| [**AppDataFolder**](appdatafolder.md)<br/>               | Ruta de acceso completa a **la carpeta Roaming** del usuario actual.<br/>              |
| [**CommonAppDataFolder**](commonappdatafolder.md)<br/>   | Ruta de acceso completa a los datos de la aplicación para todos los usuarios.<br/>                           |
| [**CommonFiles64Folder**](commonfiles64folder.md)<br/>   | Ruta de acceso completa a la carpeta Common Files predefinida de **64** bits.<br/>            |
| [**CommonFilesFolder**](commonfilesfolder.md)<br/>       | Ruta de acceso completa a **la carpeta Common Files** del usuario actual.<br/>         |
| [**DesktopFolder**](desktopfolder.md)<br/>               | Ruta de acceso completa a la **carpeta** Desktop.<br/>                                   |
| [**FavoritesFolder**](favoritesfolder.md)<br/>           | Ruta de acceso completa a **la carpeta Favoritos** del usuario actual.<br/>            |
| [**FontsFolder**](fontsfolder.md)<br/>                   | Ruta de acceso completa a la **carpeta Fuentes.**<br/>                                     |
| [**LocalAppDataFolder**](localappdatafolder.md)<br/>     | Ruta de acceso completa a la carpeta que contiene aplicaciones locales (no móviles).<br/> |
| [**MyPicturesFolder**](mypicturesfolder.md)<br/>         | Ruta de acceso completa a la **carpeta Imágenes.**<br/>                                  |
| [**NetFolderFolder**](nethoodfolder.md)<br/>               | Ruta de acceso completa a la **carpeta Net Folder.**<br/>                                   |
| [**PersonalFolder**](personalfolder.md)<br/>             | Ruta de acceso completa a **la carpeta Documentos** del usuario actual.<br/>            |
| [**PrintFolderFolder**](printhoodfolder.md)<br/>           | Ruta de acceso completa a **la carpeta Print Folder.**<br/>                                 |
| [**ProgramFiles64Folder**](programfiles64folder.md)<br/> | Ruta de acceso completa a la carpeta Archivos de programa de **64 bits predefinida.**<br/>           |
| [**ProgramFilesFolder**](programfilesfolder.md)<br/>     | Ruta de acceso completa a la carpeta Archivos de programa de **32 bits predefinida.**<br/>           |
| [**ProgramMenuFolder**](programmenufolder.md)<br/>       | Ruta de acceso completa a la **carpeta Menú del** programa.<br/>                              |
| [**RecentFolder**](recentfolder.md)<br/>                 | Ruta de acceso completa a la **carpeta** Recent.<br/>                                    |
| [**SendToFolder**](sendtofolder.md)<br/>                 | Ruta de acceso completa a **la carpeta SendTo** del usuario actual.<br/>               |
| [**StartMenuFolder**](startmenufolder.md)<br/>           | Ruta de acceso completa a **la menú Inicio** carpeta.<br/>                                |
| [**StartupFolder**](startupfolder.md)<br/>               | Ruta de acceso completa a la **carpeta Inicio.**<br/>                                   |
| [**System16Folder**](system16folder.md)<br/>             | Ruta de acceso completa a la carpeta para archivos DLL del sistema de 16 bits.<br/>                            |
| [**System64Folder**](system64folder.md)<br/>             | Ruta de acceso completa a la carpeta **System64** predefinida.<br/>                       |
| [**SystemFolder**](systemfolder.md)<br/>                 | Ruta de acceso completa a **la carpeta System** del usuario actual.<br/>               |
| [**TempFolder**](tempfolder.md)<br/>                     | Ruta de acceso completa a la **carpeta** Temp.<br/>                                      |
| [**TemplateFolder**](templatefolder.md)<br/>             | Ruta de acceso completa a **la carpeta Template** del usuario actual.<br/>             |
| [**WindowsFolder**](windowsfolder.md)<br/>               | Ruta de acceso completa a la **Windows** carpeta.<br/>                                   |
| [**WindowsVolume**](windowsvolume.md)<br/>               | Volumen de la **Windows** carpeta.<br/>                                      |



 

## <a name="user-information-properties"></a>Propiedades de información de usuario

En la lista siguiente se proporcionan vínculos a más información sobre la información proporcionada por el usuario.



| Propiedad                                                      | Descripción                                                                             |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**AdminProperties**](adminproperties.md)<br/>         | Lista de propiedades que se establecen durante una instalación de administración.<br/>       |
| [**COMPANYNAME**](companyname.md)<br/>                 | Nombre de la organización del usuario que realiza la instalación.<br/>            |
| [**LogonUser**](logonuser.md)<br/>                     | Nombre de usuario del usuario que ha iniciado sesión actualmente.<br/>                           |
| [**MsiHiddenProperties**](msihiddenproperties.md)<br/> | Lista de propiedades que no se pueden escribir en el registro.<br/>       |
| [**PIDKEY**](pidkey.md)<br/>                           | Parte del id. de producto que especifica el usuario.<br/>                                 |
| [**ProductID**](productid.md)<br/>                     | Id. de producto completo después de una validación correcta.<br/>                               |
| [**UserLanguageID**](userlanguageid.md)<br/>           | Identificador de idioma predeterminado del usuario actual.<br/>                             |
| [**NOMBRE DE USUARIO**](username.md)<br/>                       | Usuario que realiza la instalación.<br/>                                     |
| [**UserSID, propiedad**](usersid.md)<br/>                | Lo establece el instalador según el identificador de seguridad (SID) del usuario.<br/> |



 

 

 
