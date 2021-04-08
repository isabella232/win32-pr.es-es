---
description: 'En esta sección se enumeran las propiedades definidas por Windows Installer:'
ms.assetid: c91119b9-59d5-4a33-91cd-d3ba63659d12
title: Referencia de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e2ae30800d3c718549ecc887e3438d743881f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813670"
---
# <a name="property-reference"></a>Referencia de propiedades

En esta sección se enumeran las propiedades definidas por Windows Installer:

-   [Propiedades de ubicación del componente](#component-location-properties)
-   [Propiedades de configuración](#configuration-properties)
-   [Propiedades de fecha y hora](#date-time-properties)
-   [Propiedades de opciones de instalación de características](#feature-installation-options-properties)
-   [Propiedades de hardware](#hardware-properties)
-   [Propiedades de estado de la instalación](#installation-status-properties)
-   [Propiedades del sistema operativo](#operating-system-properties)
-   [Propiedades de información del producto](#product-information-properties)
-   [Propiedades de actualización de información de Resumen](#summary-information-update-properties)
-   [Propiedades de la carpeta del sistema](#system-folder-properties)
-   [Propiedades de información de usuario](#user-information-properties)

Se pueden especificar propiedades adicionales mediante datos creados o acciones personalizadas. Las propiedades con nombres que no contienen ninguna letra minúscula son propiedades públicas y se pueden especificar en la línea de comandos.

Para obtener información acerca de los valores de la clave del registro de **desinstalación** que se proporcionan mediante las propiedades del instalador, consulte [desinstalar la clave del registro](uninstall-registry-key.md).

## <a name="component-location-properties"></a>Propiedades de ubicación del componente

En la lista siguiente se proporcionan vínculos para obtener más información sobre las propiedades de ubicación del componente.



| Propiedad                                                            | Descripción                                                                                                                                                                                                        |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OriginalDatabase**](originaldatabase.md)<br/>             | El instalador establece esta propiedad en la base de datos iniciada-desde, la base de datos en el origen o la base de datos almacenada en caché.<br/>                                                                                     |
| [**ParentOriginalDatabase**](parentoriginaldatabase.md)<br/> | El instalador establece esta propiedad para las instalaciones ejecutadas por una acción de [instalación simultánea](concurrent-installations.md) .<br/>                                                                             |
| [**SourceDir**](sourcedir.md)<br/>                           | Directorio raíz que contiene los archivos de código fuente.<br/>                                                                                                                                                          |
| [**TARGETDIR**](targetdir.md)<br/>                           | Especifica el directorio de destino de la instalación. Durante una [instalación administrativa](administrative-installation.md) , esta propiedad es la ubicación donde se va a copiar el paquete de instalación.<br/> |



 

## <a name="configuration-properties"></a>Configuration Properties

En la lista siguiente se proporcionan vínculos para obtener más información acerca de otras propiedades configurables.



| Propiedad                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ACTUAR**](action.md)<br/>                                                     | Acción inicial llamada después de inicializar el instalador.<br/>                                                                                                                                                                                                                                                                                                                          |
| [**ALLUSERS**](allusers.md)<br/>                                                 | Determina dónde se almacena la información de configuración.<br/>                                                                                                                                                                                                                                                                                                                              |
| [**ARPAUTHORIZEDCDFPREFIX**](arpauthorizedcdfprefix.md)<br/>                     | Dirección URL del canal de actualización para una aplicación.<br/>                                                                                                                                                                                                                                                                                                                                      |
| [**ARPCOMMENTS**](arpcomments.md)<br/>                                           | Proporciona comentarios para **Agregar o quitar programas** en el **Panel de control**.<br/>                                                                                                                                                                                                                                                                                                         |
| [**ARPCONTACT**](arpcontact.md)<br/>                                             | Proporciona el contacto para **Agregar o quitar programas** en el **Panel de control**.<br/>                                                                                                                                                                                                                                                                                                          |
| [**ARPINSTALLLOCATION**](arpinstalllocation.md)<br/>                             | Ruta de acceso completa a la carpeta principal de una aplicación.<br/>                                                                                                                                                                                                                                                                                                                      |
| [**ARPNOMODIFY**](arpnomodify.md)<br/>                                           | Deshabilita la funcionalidad que modifica un producto.<br/>                                                                                                                                                                                                                                                                                                                                    |
| [**ARPNOREMOVE**](arpnoremove.md)<br/>                                           | Deshabilita la funcionalidad que quita un producto.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**ARPNOREPAIR**](arpnorepair.md)<br/>                                           | Deshabilita el botón **reparar** del Asistente para programas.<br/>                                                                                                                                                                                                                                                                                                                             |
| [**ARPPRODUCTICON**](arpproducticon.md)<br/>                                     | Especifica el icono principal del paquete de instalación.<br/>                                                                                                                                                                                                                                                                                                                           |
| [**ARPREADME**](arpreadme.md)<br/>                                               | Proporciona un **archivo Léame** para **Agregar o quitar programas** en el **Panel de control**.<br/>                                                                                                                                                                                                                                                                                                     |
| [**ARPSIZE**](arpsize.md)<br/>                                                   | Tamaño estimado de una aplicación en kilobytes.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**ARPSYSTEMCOMPONENT**](arpsystemcomponent.md)<br/>                             | Impide que se muestre una aplicación en la lista **Agregar o quitar programas** .<br/>                                                                                                                                                                                                                                                                                                         |
| [**ARPURLINFOABOUT**](arpurlinfoabout.md)<br/>                                   | Dirección URL de la Página principal de una aplicación.<br/>                                                                                                                                                                                                                                                                                                                                           |
| [**ARPURLUPDATEINFO**](arpurlupdateinfo.md)<br/>                                 | Dirección URL para la información de actualización de la aplicación.<br/>                                                                                                                                                                                                                                                                                                                                            |
| [**AVAILABLEFREEREG**](availablefreereg.md)<br/>                                 | Espacio del registro (en kilobytes) que requiere una aplicación. Usado por la [acción AllocateRegistrySpace](allocateregistryspace-action.md).<br/>                                                                                                                                                                                                                                              |
| [**\_unidad CCP**](ccp-drive.md)<br/>                                              | La ruta de acceso raíz para los productos aptos para CCP.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**DefaultUIFont**](defaultuifont.md)<br/>                                       | Estilo de fuente predeterminado utilizado para los controles.<br/>                                                                                                                                                                                                                                                                                                                                              |
| [**DISABLEADVTSHORTCUTS**](disableadvtshortcuts.md)<br/>                         | Se establece para deshabilitar la generación de los accesos directos específicos que admiten la [instalación a petición](installation-on-demand.md).<br/>                                                                                                                                                                                                                                                            |
| [**DISABLEMEDIA**](-disablemedia.md)<br/>                                        | Impide que el instalador registre orígenes multimedia, como un CD-ROM, como orígenes válidos para el producto.<br/>                                                                                                                                                                                                                                                                        |
| [**DISABLEROLLBACK**](-disablerollback.md)<br/>                                  | Deshabilita la reversión de la configuración actual.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**EXECUTEACTION**](executeaction.md)<br/>                                       | Acción de nivel superior que inicializa ExecuteAction.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**EXECUTEMODE**](executemode.md)<br/>                                           | Modo de ejecución que realiza el instalador.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**FASTOEM**](fastoem.md)<br/>                                                   | Mejora el rendimiento de la instalación en escenarios específicos de OEM.<br/>                                                                                                                                                                                                                                                                                                                    |
| [**INSTALLLEVEL**](installlevel.md)<br/>                                         | Nivel inicial en el que se instalan las características.<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**LIMITUI**](limitui.md)<br/>                                                   | Nivel de IU limitado como básico.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| [**LOGACTION**](logaction.md)<br/>                                               | Lista de nombres de acción que se van a registrar.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**MEDIAPACKAGEPATH**](mediapackagepath.md)<br/>                                 | Esta propiedad debe establecerse en la ruta de acceso relativa si el paquete de instalación no se encuentra en la raíz del CD-ROM.<br/>                                                                                                                                                                                                                                                               |
| [**MSIARPSETTINGSIDENTIFIER**](msiarpsettingsidentifier.md)<br/>                 | Esta propiedad opcional contiene una lista delimitada por punto y coma de las ubicaciones del registro en las que la aplicación almacena las preferencias y la configuración de un usuario. Disponible con Windows Installer 4,0.<br/>                                                                                                                                                                                        |
| [**MSIDISABLEEEUI**](msidisableeeui.md)<br/>                                     | Deshabilite la interfaz de usuario incrustada para la instalación.<br/> **[Windows Installer 4,0 y versiones anteriores](not-supported-in-windows-installer-4-0.md):** No compatible.<br/>                                                                                                                                                                                                           |
| [**MSIFASTINSTALL**](msifastinstall.md)<br/>                                     | Reduzca el tiempo necesario para instalar un paquete de Windows Installer grande.<br/> **[Windows Installer 4,5 y versiones anteriores](not-supported-in-windows-installer-4-5.md):** No compatible.<br/>                                                                                                                                                                                              |
| [**MSIINSTALLPERUSER**](msiinstallperuser.md)<br/>                               | Solicita que el Windows Installer instalar el paquete solo para el usuario actual.<br/> **[Windows Installer 4,5 y versiones anteriores](not-supported-in-windows-installer-4-5.md):** No compatible.<br/>                                                                                                                                                                                  |
| [**MSINODISABLEMEDIA**](msinodisablemedia.md)<br/>                               | Establezca esta propiedad para evitar que el instalador establezca la propiedad [**DISABLEMEDIA**](-disablemedia.md) .<br/>                                                                                                                                                                                                                                                                        |
| [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md)<br/>   | Establezca esta propiedad en 1 (uno) en la línea de comandos o en la [tabla de propiedades](property-table.md) para aplicar las reglas del componente de actualización durante [las actualizaciones pequeñas](small-updates.md) y las actualizaciones [secundarias](minor-upgrades.md) de un producto específico. Disponible a partir de Windows Installer 3,0.<br/>                                                                                     |
| [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md)<br/> | Cuando esta propiedad se ha establecido en 1, el instalador puede anular el registro y desinstalar los componentes redundantes para evitar que los componentes huérfanos queden detrás del equipo.<br/> **[Windows Installer 4,0 y versiones anteriores](not-supported-in-windows-installer-4-0.md):** No compatible.<br/>                                                                                                  |
| [**PRIMARYFOLDER**](primaryfolder.md)<br/>                                       | Permite al autor de designar una carpeta principal para una instalación de. Se usa para determinar los valores de las propiedades [**PrimaryVolumePath**](primaryvolumepath.md), [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md), [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md)y [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md) .<br/> |
| [**Privilegios**](privileged.md)<br/>                                             | Ejecuta una instalación con privilegios elevados.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**PROMPTROLLBACKCOST**](promptrollbackcost.md)<br/>                             | Acción si no hay suficiente espacio en disco para la instalación.<br/>                                                                                                                                                                                                                                                                                                                   |
| [**REINICIO**](reboot.md)<br/>                                                     | Fuerza o suprime un reinicio.<br/>                                                                                                                                                                                                                                                                                                                                                    |
| [**REBOOTPROMPT**](rebootprompt.md)<br/>                                         | Suprime la presentación de mensajes para que el usuario los reinicie. Los reinicios necesarios se producen automáticamente.<br/>                                                                                                                                                                                                                                                                     |
| [**ROOTDRIVE**](rootdrive.md)<br/>                                               | Unidad predeterminada para una instalación de.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**SEQUENCE**](sequence.md)<br/>                                                 | Tabla que tiene el esquema de tabla de secuencia.<br/>                                                                                                                                                                                                                                                                                                                                        |
| [**SHORTFILENAMES**](shortfilenames.md)<br/>                                     | Hace que se usen nombres de archivo cortos.<br/>                                                                                                                                                                                                                                                                                                                                                |
| [**TRANSFORMA**](transforms.md)<br/>                                             | Lista de transformaciones que se van a aplicar a una base de datos.<br/>                                                                                                                                                                                                                                                                                                                                    |
| [**TRANSFORMSATSOURCE**](transformsatsource.md)<br/>                             | Informa al instalador de que las transformaciones de un producto residen en el origen.<br/>                                                                                                                                                                                                                                                                                                      |
| [**TRANSFORMSSECURE**](transformssecure.md)<br/>                                 | Al establecer la propiedad [**TRANSFORMSECURE**](transformssecure.md) en 1 (uno) se informa al instalador de que las transformaciones se almacenan en caché localmente en el equipo del usuario en una ubicación en la que el usuario no tiene acceso de escritura.<br/>                                                                                                                                                           |
| [**MsiLogFileLocation**](msilogfilelocation.md)<br/>                             | El instalador establece el valor de esta propiedad en la ruta de acceso completa del archivo de registro, cuando se ha habilitado el registro. Esta propiedad está disponible a partir de Windows Installer 4,0.<br/>                                                                                                                                                                                                     |
| [**MsiLogging**](msilogging.md)<br/>                                             | Establece el modo de registro predeterminado para el paquete de Windows Installer. Esta propiedad está disponible a partir de Windows Installer 4,0.<br/>                                                                                                                                                                                                                                                   |
| [**MSIUSEREALADMINDETECTION**](msiuserealadmindetection.md)<br/>                 | Establezca esta propiedad en 1 para solicitar que el instalador utilice la información de usuario real al establecer la propiedad [**AdminUser**](adminuser.md) . Esta propiedad está disponible a partir de Windows Installer 4,0.<br/>                                                                                                                                                                         |



 

## <a name="date-time-properties"></a>Propiedades de fecha y hora

Las propiedades de [**fecha**](date.md) y [**hora**](time.md) son propiedades activas que el instalador establece cuando se extraen los datos.



| Propiedad                        | Descripción                  |
|---------------------------------|------------------------------|
| [**Date**](date.md)<br/> | Fecha actual.<br/> |
| [**Tiempo**](time.md)<br/> | La hora actual.<br/> |



 

## <a name="feature-installation-options-properties"></a>Propiedades de opciones de instalación de características

En la lista siguiente se proporcionan vínculos para obtener más información sobre las propiedades de las opciones de instalación de características.



| Propiedad                                                                | Descripción                                                                                                                                                                       |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ADDDEFAULT**](adddefault.md)<br/>                             | Lista de características que se van a instalar en la configuración predeterminada.<br/>                                                                                                         |
| [**ADDLOCAL**](addlocal.md)<br/>                                 | Lista de características que se van a instalar localmente.<br/>                                                                                                                              |
| [**ADDSOURCE**](addsource.md)<br/>                               | Lista de características que se ejecutarán desde el origen.<br/>                                                                                                                                |
| [**ANUNCIA**](advertise.md)<br/>                               | Lista de características que se van a anunciar.<br/>                                                                                                                                     |
| [**COMPADDDEFAULT**](compadddefault.md)<br/>                     | Lista de componentes que se van a instalar en la configuración predeterminada.<br/>                                                                                                       |
| [**COMPADDLOCAL**](compaddlocal.md)<br/>                         | Lista de identificadores de componente que se instalarán localmente.<br/>                                                                                                                         |
| [**COMPADDSOURCE**](compaddsource.md)<br/>                       | Lista de identificadores de componente que se ejecutarán desde los medios de origen.<br/>                                                                                                                        |
| [**FILEADDDEFAULT**](fileadddefault.md)<br/>                     | Lista de claves de archivo de los archivos que se van a instalar en la configuración predeterminada.<br/>                                                                                              |
| [**FILEADDLOCAL**](fileaddlocal.md)<br/>                         | Lista de claves de archivo para que los archivos se ejecuten localmente.<br/>                                                                                                                         |
| [**FILEADDSOURCE**](fileaddsource.md)<br/>                       | Lista de claves de archivo que se ejecutarán desde los medios de origen.<br/>                                                                                                                     |
| [**MSIDISABLELUAPATCHING**](msidisableluapatching.md)<br/>       | Al establecer esta propiedad se evita la aplicación de revisiones de usuarios con menos privilegios (LUA) de una aplicación.<br/>                                                                                 |
| [**MsiPatchRemovalList**](msipatchremovallist.md)<br/>           | Lista de revisiones que se quitarán durante la instalación.<br/>                                                                                                                 |
| [**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)<br/> | Especifica si el paquete utiliza la funcionalidad de [Administrador de reinicio](../rstmgr/restart-manager-portal.md) o [FilesInUse](filesinuse-dialog.md) .<br/>                                          |
| [**MSIDISABLERMRESTART**](msidisablermrestart.md)<br/>           | Especifica cómo deben cerrarse y reiniciarse las aplicaciones o servicios que usan actualmente los archivos afectados por una actualización para habilitar la instalación de la actualización.<br/> |
| [**MSIRMSHUTDOWN**](msirmshutdown.md)<br/>                       | Especifica cómo deben cerrarse las aplicaciones o servicios que usan actualmente los archivos afectados por una actualización para habilitar la instalación de la actualización.<br/>               |
| [**MSIPATCHREMOVE**](msipatchremove.md)<br/>                     | Al establecer esta propiedad, se quitan las revisiones.<br/>                                                                                                                                 |
| [**DISTRIBUCIÓN**](patch.md)<br/>                                       | Al establecer esta propiedad se aplica una revisión.<br/>                                                                                                                                 |
| [**REINSTALAR**](reinstall.md)<br/>                               | Lista de características que se van a volver a instalar.<br/>                                                                                                                                    |
| [**REINSTALLMODE**](reinstallmode.md)<br/>                       | Una cadena que contiene letras que especifican el tipo de reinstalación que se va a realizar.<br/>                                                                                          |
| [**RETIRAR**](remove.md)<br/>                                     | Lista de características que se van a quitar.<br/>                                                                                                                                        |



 

## <a name="hardware-properties"></a>Propiedades de hardware

En la lista siguiente se identifican las propiedades de hardware que el Windows Installer establece en el inicio.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Propiedad</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="alpha.md"><strong>Alpha</strong></a><br/></td>
<td>Nivel numérico del procesador cuando se ejecuta en un procesador Alpha.<br/>
<blockquote>
[!Note]<br />
Esta propiedad está obsoleta, Windows Installer no admite la plataforma Alpha.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="borderside.md"><strong>BorderSide</strong></a><br/></td>
<td>Ancho de los bordes de la ventana, en píxeles.<br/></td>
</tr>
<tr class="odd">
<td><a href="bordertop.md"><strong>BorderTop</strong></a><br/></td>
<td>Alto de los bordes de la ventana, en píxeles.<br/></td>
</tr>
<tr class="even">
<td><a href="captionheight.md"><strong>CaptionHeight</strong></a><br/></td>
<td>Alto del área de título normal, en píxeles.<br/></td>
</tr>
<tr class="odd">
<td><a href="colorbits.md"><strong>ColorBits</strong></a><br/></td>
<td>El número de bits de color adyacentes para cada píxel.<br/></td>
</tr>
<tr class="even">
<td><a href="intel.md"><strong>Intel</strong></a><br/></td>
<td>Nivel numérico del procesador cuando se ejecuta en un procesador Intel.<br/></td>
</tr>
<tr class="odd">
<td><a href="intel64.md"><strong>Intel64</strong></a><br/></td>
<td>Nivel numérico del procesador cuando se ejecuta en un procesador Itanium.<br/></td>
</tr>
<tr class="even">
<td><a href="msix64.md"><strong>Msix64</strong></a><br/></td>
<td>Nivel numérico del procesador cuando se ejecuta en un procesador x64.<br/></td>
</tr>
<tr class="odd">
<td><a href="physicalmemory.md"><strong>PhysicalMemory</strong></a><br/></td>
<td>Tamaño de la RAM instalada, en megabytes.<br/></td>
</tr>
<tr class="even">
<td><a href="screenx.md"><strong>ScreenX</strong></a><br/></td>
<td>Ancho de la pantalla, en píxeles.<br/></td>
</tr>
<tr class="odd">
<td><a href="screeny.md"><strong>Pantalla</strong></a><br/></td>
<td>Alto de la pantalla, en píxeles.<br/></td>
</tr>
<tr class="even">
<td><a href="textheight.md"><strong>TextHeight</strong></a><br/></td>
<td>Alto de caracteres, en unidades lógicas.<br/></td>
</tr>
<tr class="odd">
<td><a href="virtualmemory.md"><strong>VirtualMemory</strong></a><br/></td>
<td>Cantidad de espacio disponible en el archivo de paginación, en megabytes.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="installation-status-properties"></a>Propiedades de estado de la instalación

En la lista siguiente se proporcionan vínculos para obtener más información acerca de las propiedades de estado que actualiza el instalador durante la instalación.



| Propiedad                                                                      | Descripción                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AFTERREBOOT**](afterreboot.md)<br/>                                 | Indica que la instalación actual sigue un reinicio que invoca la [acción ForceReboot](forcereboot-action.md) .<br/>                                                                                                                                                |
| [**CostingComplete**](costingcomplete.md)<br/>                         | Indica si se ha completado el costo del espacio en disco.<br/>                                                                                                                                                                                                             |
| [**Instalado**](installed.md)<br/>                                     | Indica que un producto ya está instalado.<br/>                                                                                                                                                                                                                |
| [**MSICHECKCRCS**](msicheckcrcs.md)<br/>                               | El instalador realiza una CRC en archivos solo si se establece la propiedad [**MSICHECKCRCS**](msicheckcrcs.md) .<br/>                                                                                                                                                           |
| [**MsiRestartManagerSessionKey**](msirestartmanagersessionkey.md)<br/> | El instalador establece esta propiedad en la clave de sesión para la sesión del [Administrador de reinicio](../rstmgr/restart-manager-portal.md) .<br/>                                                                                                                                                         |
| [**MsiRunningElevated**](msirunningelevated-.md)<br/>                  | El instalador establece el valor de esta propiedad en 1 cuando el instalador se ejecuta con privilegios [*elevados*](e-gly.md) .<br/>                                                                                                                   |
| [**MsiSystemRebootPending**](msisystemrebootpending.md)<br/>           | El instalador establece esta propiedad en 1 Si actualmente está pendiente un reinicio del sistema operativo.<br/>                                                                                                                                                              |
| [**MsiUIHideCancel**](msiuihidecancel.md)<br/>                         | El instalador establece [**MsiUIHideCancel**](msiuihidecancel.md) en 1 cuando el nivel de instalación interno incluye **INSTALLUILEVEL \_ HIDECANCEL**.<br/>                                                                                                                   |
| [**MsiUIProgressOnly**](msiuiprogressonly.md)<br/>                     | El instalador establece [**MsiUIProgressOnly**](msiuiprogressonly.md) en 1 cuando el nivel de instalación interno incluye **INSTALLUILEVEL \_ PROGRESSONLY**.<br/>                                                                                                             |
| [**MsiUISourceResOnly**](msiuisourceresonly.md)<br/>                   | [**MsiUISourceResOnly**](msiuisourceresonly.md) a 1 (uno) cuando el nivel de instalación interno incluye **INSTALLUILEVEL \_ SOURCERESONLY**.<br/>                                                                                                                       |
| [**NoCompanyName**](nocompanyname.md)<br/>                             | Suprime la configuración automática de la propiedad [**CompanyName**](companyname.md) .<br/>                                                                                                                                                                          |
| [**NoUserName**](nousername.md)<br/>                                   | Suprime la configuración automática de la propiedad [**username**](username.md) .<br/>                                                                                                                                                                                |
| [**OutOfDiskSpace**](outofdiskspace.md)<br/>                           | Espacio en disco insuficiente para alojar la instalación.<br/>                                                                                                                                                                                                      |
| [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md)<br/>                   | Espacio en disco insuficiente con la reversión desactivada.<br/>                                                                                                                                                                                                             |
| [**Preseleccionadas**](preselected.md)<br/>                                 | Las características ya están seleccionadas.<br/>                                                                                                                                                                                                                                |
| [**PrimaryVolumePath**](primaryvolumepath.md)<br/>                     | El instalador establece el valor de esta propiedad en la ruta de acceso del volumen que designa la propiedad [**PRIMARYFOLDER**](primaryfolder.md) .<br/>                                                                                                                  |
| [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md)<br/> | El instalador establece el valor de esta propiedad en una cadena que representa el número total de bytes disponibles en el volumen al que hace referencia la propiedad [**PrimaryVolumePath**](primaryvolumepath.md) .<br/>                                                      |
| [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md)<br/> | El instalador establece el valor de esta propiedad en una cadena que representa el número total de bytes restantes en el volumen al que hace referencia la propiedad [**PrimaryVolumePath**](primaryvolumepath.md) si están instaladas todas las características seleccionadas actualmente.<br/> |
| [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md)<br/>   | El instalador establece el valor de esta propiedad en una cadena que representa el número total de bytes que necesitan todas las características seleccionadas actualmente en el volumen al que hace referencia la propiedad [**PrimaryVolumePath**](primaryvolumepath.md) .<br/>                    |
| [**ProductLanguage**](productlanguage.md)<br/>                         | Identificador de idioma numérico (LANGID) de la base de datos. DESEE<br/>                                                                                                                                                                                             |
| [**ReplacedInUseFiles**](replacedinusefiles.md)<br/>                   | Se establece si el instalador se instala en un archivo que se está usando.<br/>                                                                                                                                                                                          |
| [**RECUPER**](resume.md)<br/>                                           | Instalación reanudada.<br/>                                                                                                                                                                                                                                         |
| [**RollbackDisabled**](rollbackdisabled.md)<br/>                       | El instalador establece esta propiedad cuando la reversión está deshabilitada.<br/>                                                                                                                                                                                                   |
| [**Elemento uilevel**](uilevel.md)<br/>                                         | Indica el nivel de la interfaz de usuario.<br/>                                                                                                                                                                                                                           |
| [**UpdateStarted**](updatestarted.md)<br/>                             | Se establece cuando se han iniciado cambios en el sistema para esta instalación.<br/>                                                                                                                                                                                              |
| [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md)<br/>               | Lo establece el instalador cuando una actualización quita una aplicación.<br/>                                                                                                                                                                                                  |
| [**VersionMsi**](versionmsi.md)<br/>                                   | El instalador establece esta propiedad en la versión de Windows Installer que se ejecuta durante la instalación.<br/>                                                                                                                                                     |



 

## <a name="operating-system-properties"></a>Propiedades del sistema operativo

En la lista siguiente se proporcionan vínculos a más información sobre las propiedades del sistema operativo que el instalador establece en el inicio.



| Nombre de la propiedad                                                                             | Breve descripción                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdminUser**](adminuser.md)<br/>                                                 | Establezca en Windows 2000 si el usuario tiene privilegios de administrador.<br/>                                                                                                                                                                                                                        |
| [**ComputerName**](computername.md)<br/>                                           | Nombre de equipo del sistema actual.<br/>                                                                                                                                                                                                                                                 |
| [**MsiNetAssemblySupport**](msinetassemblysupport.md)<br/>                         | En los sistemas que admiten ensamblados de Common Language Runtime, el instalador establece el valor de esta propiedad en la versión de archivo de fusion.dll. El instalador no establece esta propiedad si el sistema operativo no admite ensamblados de Common Language Runtime.<br/>                   |
| [**MsiNTProductType**](msintproducttype.md)<br/>                                   | Indica el tipo de producto de Windows.<br/>                                                                                                                                                                                                                                                  |
| [**MsiNTSuiteBackOffice**](msintsuitebackoffice.md)<br/>                           | En los sistemas operativos Windows 2000 y posteriores, el instalador establece esta propiedad en 1 (uno) solo si se instalan los componentes de Microsoft BackOffice.<br/>                                                                                                                                      |
| [**MsiNTSuiteDataCenter**](msintsuitedatacenter.md)<br/>                           | En los sistemas operativos Windows 2000 y posteriores, el instalador establece esta propiedad en 1 (uno) solo si Windows 2000 Datacenter Server está instalado.<br/>                                                                                                                                        |
| [**MsiNTSuiteEnterprise**](msintsuiteenterprise.md)<br/>                           | En los sistemas operativos Windows 2000 y posteriores, el instalador establece esta propiedad en 1 (uno) solo si Windows 2000 Advanced Server está instalado.<br/>                                                                                                                                          |
| [**MsiNTSuitePersonal**](msintsuitepersonal.md)<br/>                               | En Windows XP y sistemas operativos posteriores, el instalador establece esta propiedad en 1 (uno) solo si el sistema operativo es Home (no Professional).<br/>                                                                                                                                      |
| [**MsiNTSuiteSmallBusiness**](msintsuitesmallbusiness.md)<br/>                     | En los sistemas operativos Windows 2000 y posteriores, el instalador establece esta propiedad en 1 (uno) solo si está instalado Microsoft Small Business Server.<br/>                                                                                                                                       |
| [**MsiNTSuiteSmallBusinessRestricted**](msintsuitesmallbusinessrestricted.md)<br/> | En los sistemas operativos Windows 2000 y posteriores, el instalador establece esta propiedad en 1 (uno) solo si Microsoft Small Business Server se instala con la licencia de cliente restrictiva.<br/>                                                                                                   |
| [**MsiNTSuiteWebServer**](msintsuitewebserver.md)<br/>                             | En los sistemas operativos Windows 2000 y posteriores, el instalador establece la propiedad [**MsiNTSuiteWebServer**](msintsuitewebserver.md) en 1 (uno) si la edición web de Windows Server 2003 está instalada. Solo está disponible con la versión 2003 de Windows Server del Windows Installer.<br/> |
| [**MsiTabletPC**](msitabletpc.md)<br/>                                             | El instalador establece esta propiedad en un valor distinto de cero si el sistema operativo actual es Windows XP Tablet PC Edition.<br/>                                                                                                                                                                 |
| [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md)<br/>                     | En los sistemas que admiten ensamblados Win32, el instalador establece el valor de esta propiedad en la versión de archivo de sxs.dll. El instalador no establece esta propiedad si el sistema operativo no admite ensamblados Win32.<br/>                                                          |
| [**OLEAdvtSupport**](oleadvtsupport.md)<br/>                                       | Establezca si OLE admite el Windows Installer.<br/>                                                                                                                                                                                                                                           |
| [**RedirectedDllSupport**](redirecteddllsupport.md)<br/>                           | El instalador establece la propiedad [**RedirectedDllSupport**](redirecteddllsupport.md) si el sistema que realiza la instalación admite [componentes aislados](isolated-components.md).<br/>                                                                                              |
| [**RemoteAdminTS**](remoteadmints.md)<br/>                                         | El instalador establece la propiedad [**RemoteAdminTS**](remoteadmints.md) cuando el sistema es un servidor de administración remoto que ejecuta el servicio de rol Terminal Server.<br/>                                                                                                                   |
| [**ServicePackLevel**](servicepacklevel.md)<br/>                                   | Número de versión del Service Pack del sistema operativo.<br/>                                                                                                                                                                                                                             |
| [**ServicePackLevelMinor**](servicepacklevelminor.md)<br/>                         | Número de versión secundaria del Service Pack del sistema operativo.<br/>                                                                                                                                                                                                                       |
| [**SharedWindows**](sharedwindows.md)<br/>                                         | Se establece cuando el sistema funciona como ventanas compartidas.<br/>                                                                                                                                                                                                                                  |
| [**ShellAdvtSupport**](shelladvtsupport.md)<br/>                                   | Se establece si el shell admite la publicidad de características.<br/>                                                                                                                                                                                                                                       |
| [**SystemLanguageID**](systemlanguageid.md)<br/>                                   | Identificador de idioma predeterminado del sistema.<br/>                                                                                                                                                                                                                                          |
| [**TerminalServer**](terminalserver.md)<br/>                                       | Se establece cuando el sistema es un servidor que ejecuta el servicio de rol Terminal Server.<br/>                                                                                                                                                                                                            |
| [**TTCSupport**](ttcsupport.md)<br/>                                               | Indica si el sistema operativo admite el uso de archivos. TTC (colecciones de fuentes de tipo verdadero).<br/>                                                                                                                                                                                            |
| [**Version9X**](version9x.md)<br/>                                                 | Número de versión del sistema operativo Windows.<br/>                                                                                                                                                                                                                                     |
| [**VersionDatabase**](versiondatabase.md)<br/>                                     | Versión de la base de datos numérica de la instalación actual.<br/>                                                                                                                                                                                                                                |
| [**VersionNT**](versionnt.md)<br/>                                                 | Número de versión del sistema operativo.<br/>                                                                                                                                                                                                                                             |
| [**VersionNT64**](versionnt64.md)<br/>                                             | Número de versión del sistema operativo Si el sistema se ejecuta en un equipo de 64 bits.<br/>                                                                                                                                                                                               |
| [**Compilación de Windows**](windowsbuild.md)<br/>                                          | Número de compilación del sistema operativo.<br/>                                                                                                                                                                                                                                                |



 

## <a name="product-information-properties"></a>Propiedades de información del producto

En la lista siguiente se proporcionan vínculos para obtener más información sobre las propiedades específicas del producto especificadas en la [tabla de propiedades](property-table.md).



| Nombre de la propiedad                                                  | Breve descripción                                                                                                                         |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**ARPHELPLINK**](arphelplink.md)<br/>                  | Dirección de Internet o dirección URL de soporte técnico.<br/>                                                                                 |
| [**ARPHELPTELEPHONE**](arphelptelephone.md)<br/>        | Números de teléfono de soporte técnico.<br/>                                                                                               |
| [**DiskPrompt**](diskprompt.md)<br/>                    | Cadena mostrada por un cuadro de mensaje que solicita un disco.<br/>                                                                     |
| [**IsAdminPackage**](isadminpackage.md)<br/>            | Se establece en 1 (uno) si la instalación actual se ejecuta desde un paquete creado a través de una instalación administrativa.<br/>           |
| [**LeftUnit**](leftunit.md)<br/>                        | Coloca las unidades a la izquierda del número.<br/>                                                                                        |
| [**Le**](manufacturer.md)<br/>                | Nombre del fabricante de la aplicación. (Requerido)<br/>                                                                               |
| [**MediaSourceDir**](mediasourcedir.md)<br/>            | El instalador establece esta propiedad en 1 (uno) cuando la instalación utiliza un origen de medios, como un CD-ROM.<br/>                       |
| [**MSIINSTANCEGUID**](msiinstanceguid.md)<br/>          | La presencia de esta propiedad indica que una transformación de cambio de código de producto se registra en el producto.<br/>                   |
| [**MSINEWINSTANCE**](msinewinstance.md)<br/>            | Esta propiedad indica la instalación de una nueva instancia de un producto con transformaciones de instancia.<br/>                              |
| [**ParentProductCode**](parentoriginaldatabase.md)<br/> | El instalador establece esta propiedad para las instalaciones en las que se ejecuta una acción de [instalación simultánea](concurrent-installations.md) .<br/> |
| [**PIDTemplate**](pidtemplate.md)<br/>                  | Cadena usada como plantilla para la propiedad [**PIDKEY**](pidkey.md) .<br/>                                                           |
| [**ProductCode**](productcode.md)<br/>                  | Un identificador único para una versión de producto específica. (Requerido)<br/>                                                                 |
| [**ProductName**](productname.md)<br/>                  | Nombre legible de una aplicación. (Requerido)<br/>                                                                              |
| [**ProductState**](productstate.md)<br/>                | Se establece en el estado instalado de un producto.<br/>                                                                                       |
| [**ProductVersion**](productversion.md)<br/>            | Formato de cadena de la versión del producto como un valor numérico. (Requerido)<br/>                                                            |
| [**UpgradeCode**](upgradecode.md)<br/>                  | GUID que representa un conjunto relacionado de productos.<br/>                                                                              |



 

## <a name="summary-information-update-properties"></a>Propiedades de actualización de información de Resumen

Las siguientes propiedades solo las establecen las transformaciones en archivos. MSP que se usan para actualizar el flujo de información de Resumen de una imagen administrativa.



| Propiedad                                                              | Descripción                                                                                                                  |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**PATCHNEWPACKAGECODE**](patchnewpackagecode.md)<br/>         | El valor de esta propiedad se escribe en la propiedad [**Resumen del número de revisión**](revision-number-summary.md) .<br/> |
| [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md)<br/> | El valor de esta propiedad se escribe en la propiedad de [**Resumen comentarios**](comments-summary.md) .<br/>               |
| [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md)<br/>   | El valor de esta propiedad se escribe en la propiedad de [**Resumen de asunto**](subject-summary.md) .<br/>                 |



 

## <a name="system-folder-properties"></a>Propiedades de la carpeta del sistema

La lista siguiente contiene vínculos a más información acerca de las carpetas del sistema que el instalador establece en el programa de instalación.



| Propiedad                                                        | Descripción                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**AdminToolsFolder**](admintoolsfolder.md)<br/>         | La ruta de acceso completa al directorio que contiene las herramientas administrativas.<br/>         |
| [**AppDataFolder**](appdatafolder.md)<br/>               | La ruta de acceso completa a la carpeta **móvil** del usuario actual.<br/>              |
| [**CommonAppDataFolder**](commonappdatafolder.md)<br/>   | La ruta de acceso completa a los datos de la aplicación para todos los usuarios.<br/>                           |
| [**CommonFiles64Folder**](commonfiles64folder.md)<br/>   | La ruta de acceso completa a la carpeta de **archivos comunes de 64** bits predefinida.<br/>            |
| [**CommonFilesFolder**](commonfilesfolder.md)<br/>       | La ruta de acceso completa a la carpeta de **archivos comunes** del usuario actual.<br/>         |
| [**DesktopFolder**](desktopfolder.md)<br/>               | La ruta de acceso completa a la carpeta del **escritorio** .<br/>                                   |
| [**FavoritesFolder**](favoritesfolder.md)<br/>           | La ruta de acceso completa a la carpeta **Favoritos** del usuario actual.<br/>            |
| [**FontsFolder**](fontsfolder.md)<br/>                   | Ruta de acceso completa a la carpeta **Fonts** .<br/>                                     |
| [**LocalAppDataFolder**](localappdatafolder.md)<br/>     | La ruta de acceso completa a la carpeta que contiene aplicaciones locales (no móviles).<br/> |
| [**MyPicturesFolder**](mypicturesfolder.md)<br/>         | Ruta de acceso completa a la carpeta **imágenes** .<br/>                                  |
| [**NetHoodFolder**](nethoodfolder.md)<br/>               | La ruta de acceso completa a la carpeta **NetHood** .<br/>                                   |
| [**PersonalFolder**](personalfolder.md)<br/>             | La ruta de acceso completa a la carpeta **documentos** del usuario actual.<br/>            |
| [**PrintHoodFolder**](printhoodfolder.md)<br/>           | La ruta de acceso completa a la carpeta **PrintHood** .<br/>                                 |
| [**ProgramFiles64Folder**](programfiles64folder.md)<br/> | La ruta de acceso completa a la carpeta de **archivos de programa de 64** bits predefinida.<br/>           |
| [**ProgramFilesFolder**](programfilesfolder.md)<br/>     | La ruta de acceso completa a la carpeta de **archivos de programa de 32** bits predefinida.<br/>           |
| [**ProgramMenuFolder**](programmenufolder.md)<br/>       | Ruta de acceso completa a la carpeta de **menú del programa** .<br/>                              |
| [**RecentFolder**](recentfolder.md)<br/>                 | Ruta de acceso completa a la carpeta **reciente** .<br/>                                    |
| [**SendToFolder**](sendtofolder.md)<br/>                 | La ruta de acceso completa a la carpeta **SendTo** para el usuario actual.<br/>               |
| [**StartMenuFolder**](startmenufolder.md)<br/>           | Ruta de acceso completa a la carpeta del **menú Inicio** .<br/>                                |
| [**StartupFolder**](startupfolder.md)<br/>               | Ruta de acceso completa a la carpeta de **Inicio** .<br/>                                   |
| [**System16Folder**](system16folder.md)<br/>             | La ruta de acceso completa a la carpeta para los archivos DLL del sistema de 16 bits.<br/>                            |
| [**System64Folder**](system64folder.md)<br/>             | La ruta de acceso completa a la carpeta **System64** predefinida.<br/>                       |
| [**Carpetadelsistema**](systemfolder.md)<br/>                 | La ruta de acceso completa a la carpeta **del sistema** para el usuario actual.<br/>               |
| [**TempFolder**](tempfolder.md)<br/>                     | Ruta de acceso completa a la carpeta **temporal** .<br/>                                      |
| [**TemplateFolder**](templatefolder.md)<br/>             | La ruta de acceso completa a la carpeta de **plantillas** para el usuario actual.<br/>             |
| [**WindowsFolder**](windowsfolder.md)<br/>               | La ruta de acceso completa a la carpeta de **Windows** .<br/>                                   |
| [**WindowsVolume**](windowsvolume.md)<br/>               | El volumen de la carpeta de **Windows** .<br/>                                      |



 

## <a name="user-information-properties"></a>Propiedades de información de usuario

En la lista siguiente se proporcionan vínculos para obtener más información acerca de la información proporcionada por el usuario.



| Propiedad                                                      | Descripción                                                                             |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**AdminProperties**](adminproperties.md)<br/>         | Lista de propiedades que se establecen durante una instalación de administración.<br/>       |
| [**COMPAÑÍA**](companyname.md)<br/>                 | Nombre de la organización del usuario que está realizando la instalación.<br/>            |
| [**LogonUser**](logonuser.md)<br/>                     | Nombre de usuario del usuario que ha iniciado sesión actualmente.<br/>                           |
| [**MsiHiddenProperties**](msihiddenproperties.md)<br/> | Lista de propiedades que no se pueden escribir en el registro.<br/>       |
| [**PIDKEY**](pidkey.md)<br/>                           | Parte del ID. de producto que especifica el usuario.<br/>                                 |
| [**IdProducto**](productid.md)<br/>                     | IDENTIFICADOR del producto completo después de una validación correcta.<br/>                               |
| [**UserLanguageID**](userlanguageid.md)<br/>           | Identificador de idioma predeterminado del usuario actual.<br/>                             |
| [**NOMBRE**](username.md)<br/>                       | Usuario que está realizando la instalación.<br/>                                     |
| [**UserSID (propiedad)**](usersid.md)<br/>                | Lo establece el instalador según el identificador de seguridad (SID) del usuario.<br/> |



 

 

 
