---
description: La categoría sistema operativo agrupa las clases que representan objetos relacionados con el sistema operativo.
ms.assetid: D0756D8C-A3D3-4C75-96A3-8C7F05300B39
ms.tgt_platform: multiple
title: Clases de sistema operativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f47df8a949e3ac07bf2099ea708d496bed87298
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659761"
---
# <a name="operating-system-classes"></a>Clases de sistema operativo

La categoría sistema operativo agrupa las clases que representan objetos relacionados con el sistema operativo. Denotan las diversas configuraciones y valores que definen un entorno informático. Algunos ejemplos son: la configuración de arranque, la configuración del modelo de objetos componentes (COM), la configuración del entorno de escritorio, los controladores, la configuración de seguridad, la configuración de usuario y la configuración del registro.

La categoría sistema operativo se agrupa en las subcategorías siguientes:

-   [COM](#com)
-   [Dispositivo de escritorio](#desktop)
-   [Controladores](#drivers)
-   [Registro de eventos](#windows-event-log)
-   [Sistema de archivos](#file-system)
-   [Objetos de trabajo](#job-objects)
-   [Archivos de memoria y de página](#memory-and-page-files)
-   [Audio multimedia o visual](#multimedia-audio-or-visual)
-   [Redes](#networking)
-   [Eventos del sistema operativo](#operating-system-events)
-   [Configuración del sistema operativo](#operating-system-settings)
-   [Procesos](#processes)
-   [Registro](#registry)
-   [Trabajos del programador](#scheduler-jobs)
-   [Seguridad](#security)
-   [Servicios](#services)
-   [Recursos compartidos](#shares)
-   [Menú Inicio](#start-menu)
-   [Storage](#storage)
-   [Usuarios](#users)
-   [Activación de productos de Windows](#windows-product-activation)

## <a name="com"></a>COM

La subcategoría COM agrupa las clases que representan la configuración de COM y DCOM, las clases y la configuración de la aplicación cliente.



| Clase                                                                                           | Descripción                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ClassicCOMApplicationClasses**](win32-classiccomapplicationclasses.md)               | Clase de asociación<br/> Relaciona una aplicación DCOM y un componente COM agrupados en él.<br/>                                                                             |
| [**Win32 \_ ClassicCOMClass**](win32-classiccomclass.md)                                         | Clase de instancia<br/> Representa las propiedades de un componente COM.<br/>                                                                                                   |
| [**Win32 \_ ClassicCOMClassSettings**](win32-classiccomclasssettings.md)                         | Clase de asociación<br/> Relaciona una clase COM y la configuración utilizada para configurar las instancias de la clase COM.<br/>                                                           |
| [**Win32 \_ ClientApplicationSetting**](win32-clientapplicationsetting.md)                       | Clase de asociación<br/> Relaciona un ejecutable y una aplicación DCOM que contiene las opciones de configuración de DCOM para el archivo ejecutable.<br/>                           |
| [**Comaplicación Win32 \_**](win32-comapplication.md)                                           | Clase de instancia<br/> Representa una aplicación COM.<br/>                                                                                                                   |
| [**Win32 \_ COMApplicationClasses**](win32-comapplicationclasses.md)                             | Clase de asociación<br/> Relaciona un componente COM y la aplicación COM donde reside.<br/>                                                                            |
| [**Win32 \_ COMApplicationSettings**](win32-comapplicationsettings.md)                           | Clase de asociación<br/> Relaciona una aplicación DCOM y sus valores de configuración.<br/>                                                                                   |
| [**Comclase Win32 \_**](win32-comclass.md)                                                       | Clase de instancia<br/> Representa las propiedades de un componente COM.<br/>                                                                                                   |
| [**Win32 \_ ComClassAutoEmulator**](win32-comclassautoemulator.md)                               | Clase de asociación<br/> Relaciona una clase COM y otra clase COM que emula automáticamente.<br/>                                                                    |
| [**Win32 \_ ComClassEmulator**](win32-comclassemulator.md)                                       | Clase de asociación<br/> Relaciona dos versiones de una clase COM.<br/>                                                                                                         |
| [**Win32 \_ ComponentCategory**](win32-componentcategory.md)                                     | Clase de instancia<br/> Representa una categoría de componente.<br/>                                                                                                                |
| [**Establecimiento de Win32 \_**](win32-comsetting.md)                                                   | Clase de instancia<br/> Representa la configuración asociada a un componente COM o aplicación COM.<br/>                                                                     |
| [**Win32 \_ DCOMApplication**](win32-dcomapplication.md)                                         | Clase de instancia<br/> Representa las propiedades de una aplicación DCOM.<br/>                                                                                                |
| [**Win32 \_ DCOMApplicationAccessAllowedSetting**](/previous-versions/windows/desktop/secrcw32prov/win32-dcomapplicationaccessallowedsetting) | Clase de asociación<br/> Relaciona la instancia de [**Win32 \_ DCOMApplication**](win32-dcomapplication.md) y las identificaciones de seguridad (SID) del usuario que pueden tener acceso a ella.<br/> |
| [**Win32 \_ DCOMApplicationLaunchAllowedSetting**](/previous-versions/windows/desktop/secrcw32prov/win32-dcomapplicationlaunchallowedsetting) | Clase de asociación<br/> Relaciona la instancia de [**Win32 \_ DCOMApplication**](win32-dcomapplication.md) y los SID de usuario que pueden iniciarlo.<br/>                           |
| [**Win32 \_ DCOMApplicationSetting**](win32-dcomapplicationsetting.md)                           | Clase de instancia<br/> Representa la configuración de una aplicación DCOM.<br/>                                                                                                  |
| [**Win32 \_ ImplementedCategory**](win32-implementedcategory.md)                                 | Clase de asociación<br/> Relaciona una categoría de componente y la clase COM mediante sus interfaces.<br/>                                                                         |



 

## <a name="desktop"></a>Escritorio

La subcategoría escritorio agrupa las clases que representan objetos que definen una configuración de escritorio específica.



| Clase                                           | Descripción                                                                                                                        |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Escritorio Win32**](win32-desktop.md)         | Clase de instancia<br/> Representa las características comunes del escritorio de un usuario.<br/>                                    |
| [**\_Entorno Win32**](win32-environment.md) | Clase de instancia<br/> Representa un entorno o una configuración de entorno del sistema en un equipo que ejecuta Windows.<br/> |
| [**\_Zona horaria de Win32**](win32-timezone.md)       | Clase de instancia<br/> Representa la información de zona horaria de un equipo que ejecuta Windows.<br/>                   |
| [**Win32 \_ UserDesktop**](win32-userdesktop.md) | Clase de asociación<br/> Relaciona una cuenta de usuario y la configuración de escritorio específica de la misma.<br/>                   |



 

## <a name="drivers"></a>Controladores

La subcategoría drivers agrupa las clases que representan controladores de dispositivos virtuales y controladores del sistema para los servicios básicos.



| Clase                                             | Descripción                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [**Win32 \_ SystemDriver**](win32-systemdriver.md) | Clase de instancia<br/> Representa el controlador del sistema para un servicio base.<br/> |



 

## <a name="file-system"></a>Sistema de archivos

La subcategoría sistema de archivos agrupa las clases que representan el modo en que se organiza lógicamente un disco duro. Esto incluye el tipo de sistema de archivos usado, la estructura de directorios y el modo en que se crean las particiones del disco.



| Clase                                                                               | Descripción                                                                                                                                                                          |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ CIMLogicalDeviceCIMDataFile**](win32-cimlogicaldevicecimdatafile.md)     | Clase de asociación<br/> Relaciona los dispositivos lógicos y los archivos de datos, que indican los archivos de controlador utilizados por el dispositivo.<br/>                                                      |
| [**\_Directorio Win32**](win32-directory.md)                                         | Clase de instancia<br/> Representa una entrada de directorio en un equipo que ejecuta Windows.<br/>                                                                              |
| [**Win32 \_ DirectorySpecification**](/previous-versions/windows/desktop/msiprov/win32-directoryspecification)               | Clase de instancia<br/> Representa el diseño del directorio para el producto.<br/>                                                                                                |
| [**Win32 \_ DiskDriveToDiskPartition**](win32-diskdrivetodiskpartition.md)           | Clase de asociación<br/> Relaciona una unidad de disco y una partición existente.<br/>                                                                                         |
| [**Win32 \_ DiskPartition**](win32-diskpartition.md)                                 | Clase de instancia<br/> Representa las capacidades y la capacidad de administración de un área con particiones de un disco físico en un equipo que ejecuta Windows.<br/>              |
| [**Win32 \_ DiskQuota**](/previous-versions/windows/desktop/wmipdskq/win32-diskquota)                                    | Clase de asociación<br/> Realiza un seguimiento del uso del espacio en disco para volúmenes del sistema de archivos NTFS.<br/>                                                                                        |
| [**LogicalDisk de Win32 \_**](win32-logicaldisk.md)                                     | Representa un origen de datos que se resuelve en un dispositivo de almacenamiento local real en un equipo con Windows.<br/>                                                            |
| [**Win32 \_ LogicalDiskRootDirectory**](win32-logicaldiskrootdirectory.md)           | Clase de asociación<br/> Relaciona un disco lógico y su estructura de directorios.<br/>                                                                                          |
| [**Win32 \_ LogicalDiskToPartition**](win32-logicaldisktopartition.md)               | Clase de asociación<br/> Relaciona una unidad de disco lógico y la partición de disco en la que reside.<br/>                                                                           |
| [**Win32 \_ MappedLogicalDisk**](win32-mappedlogicaldisk.md)                         | Representa los dispositivos de almacenamiento de red que se asignan como discos lógicos en el equipo que ejecuta Windows.<br/>                                                               |
| [**Win32 \_ OperatingSystemAutochkSetting**](/previous-versions//aa394240(v=vs.85)) | Clase de asociación<br/> Representa la asociación entre una instancia de un [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) y los valores definidos para ella.<br/> |
| [**Win32 \_ QuotaSetting**](/previous-versions/windows/desktop/wmipdskq/win32-quotasetting)                              | Clase de instancia<br/> Contiene información de configuración para las cuotas de disco en un volumen.<br/>                                                                                       |
| [**Win32 \_ ShortcutFile**](win32-shortcutfile.md)                                   | Clase de instancia<br/> Representa archivos que son accesos directos a otros archivos, directorios y comandos.<br/>                                                                  |
| [**\_Subdirectorio Win32**](win32-subdirectory.md)                                   | Clase de asociación<br/> Relaciona un directorio (carpeta) y uno de sus subdirectorios (subcarpetas).<br/>                                                                     |
| [**Win32 \_ SystemPartitions**](win32-systempartitions.md)                           | Clase de asociación<br/> Relaciona un sistema de equipo y una partición de disco en ese sistema.<br/>                                                                               |
| [**\_Volumen Win32**](/previous-versions/windows/desktop/legacy/aa394515(v=vs.85))                                               | Clase de instancia<br/> Representa un área de almacenamiento en un disco duro.<br/>                                                                                                   |
| [**Win32 \_ VolumeQuota**](/previous-versions/windows/desktop/vdswmi/win32-volumequota)                                     | Clase de asociación<br/> Relaciona un volumen con la configuración de cuota por volumen.<br/>                                                                                           |
| [**Win32 \_ VolumeQuotaSetting**](/previous-versions/windows/desktop/wmipdskq/win32-volumequotasetting)                  | Clase de asociación<br/> Relaciona la configuración de la cuota de disco con un volumen de disco específico.<br/>                                                                                     |
| [**Win32 \_ VolumeUserQuota**](/previous-versions/windows/desktop/vdswmi/win32-volumeuserquota)                             | Clase de asociación<br/> Relaciona las cuotas por usuario con los volúmenes habilitados para cuotas.<br/>                                                                                            |



 

## <a name="job-objects"></a>Objetos de trabajo

La subcategoría objetos de trabajo agrupa las clases que representan clases que proporcionan los medios para instrumentar objetos de trabajo con nombre. No se puede instrumentar un objeto de trabajo sin nombre.



| Clase                                                                               | Descripción                                                                                                                                                                                |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ CollectionStatistics**](/previous-versions/windows/desktop/cimwin32a/win32-collectionstatistics)                   | Clase de asociación<br/> Relaciona una colección de elementos del sistema administrados y la clase que representa la información estadística acerca de la colección.<br/>                               |
| [**LUID de Win32 \_**](/previous-versions/windows/desktop/wmipjobobjprov/win32-luid)                                                   | Clase de instancia<br/> Representa un identificador local único (LUID)<br/>                                                                                                         |
| [**Win32 \_ LUIDandAttributes**](/previous-versions/windows/desktop/wmipjobobjprov/win32-luidandattributes)                         | Clase de instancia<br/> Representa un LUID y sus atributos.<br/>                                                                                                                 |
| [**Win32 \_ NamedJobObject**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobject)                               | Clase de instancia<br/> Representa un objeto de kernel que se utiliza para agrupar procesos con el fin de controlar la vida y los recursos de los procesos dentro del objeto de trabajo.<br/> |
| [**Win32 \_ NamedJobObjectActgInfo**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectactginfo)               | Clase de instancia<br/> Representa la información de cuentas de e/s para un objeto de trabajo.<br/>                                                                                           |
| [**Win32 \_ NamedJobObjectLimit**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectlimit)                     | Clase de instancia<br/> Representa una asociación entre un objeto de trabajo y la configuración de límite de objetos de trabajo.<br/>                                                                     |
| [**Win32 \_ NamedJobObjectLimitSetting**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectlimitsetting)       | Clase de instancia<br/> Representa la configuración de límite para un objeto de trabajo.<br/>                                                                                                       |
| [**Win32 \_ NamedJobObjectProcess**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectprocess)                 | Clase de instancia<br/> Relaciona un objeto de trabajo y el proceso incluido en el objeto de trabajo.<br/>                                                                                     |
| [**Win32 \_ NamedJobObjectSecLimit**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectseclimit)               | Clase de instancia<br/> Relaciona un objeto de trabajo y la configuración de límite de seguridad del objeto de trabajo.<br/>                                                                                      |
| [**Win32 \_ NamedJobObjectSecLimitSetting**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectseclimitsetting) | Clase de instancia<br/> Representa la configuración de límite de seguridad para un objeto de trabajo.<br/>                                                                                              |
| [**Win32 \_ NamedJobObjectStatistics**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectstatistics)           | Clase de instancia<br/> Representa una asociación entre un objeto de trabajo y la clase de información de cuentas de e/s de objetos de trabajo.<br/>                                                   |
| [**Win32 \_ SIDandAttributes**](/previous-versions/windows/desktop/wmipjobobjprov/win32-sidandattributes)                           | Clase de instancia<br/> Representa un identificador de seguridad (SID) y sus atributos.<br/>                                                                                            |
| [**Win32 \_ TokenGroups**](/previous-versions/windows/desktop/wmipjobobjprov/win32-tokengroups)                                     | Clase de evento<br/> Representa información sobre los SID de grupo en un token de acceso.<br/>                                                                                          |
| [**Win32 \_ TokenPrivileges**](/previous-versions/windows/desktop/wmipjobobjprov/win32-tokenprivileges)                             | Clase de evento<br/> Representa información sobre un conjunto de privilegios para un token de acceso.<br/>                                                                                    |



 

## <a name="memory-and-page-files"></a>Archivos de memoria y de página

La subcategoría archivos de página y memoria agrupa las clases que representan los valores de configuración del archivo de paginación.



| Clase                                                                 | Descripción                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Archivo de \_ paginación Win32**](win32-pagefile.md)                             | Clase de instancia<br/> Representa el archivo usado para controlar el intercambio de archivos de memoria virtual en un sistema Windows.<br/>                  |
| [**Win32 \_ PageFileElementSetting**](win32-pagefileelementsetting.md) | Clase de asociación<br/> Relaciona la configuración inicial de un archivo de paginación y el estado de esos valores durante el uso normal.<br/>        |
| [**Win32 \_ PageFileSetting**](win32-pagefilesetting.md)               | Clase de instancia<br/> Representa la configuración de un archivo de paginación.<br/>                                                                  |
| [**Win32 \_ PageFileUsage**](win32-pagefileusage.md)                   | Clase de instancia<br/> Representa el archivo usado para controlar el intercambio de archivos de memoria virtual en un equipo que ejecuta Windows.<br/> |



 

## <a name="multimedia-audio-or-visual"></a>Audio multimedia o visual

La clase de la subcategoría audio o visual de multimedia representa las propiedades del códec de audio o vídeo instalado en el sistema del equipo.



| Clase                                       | Descripción                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ CodecFile**](win32-codecfile.md) | Clase de instancia<br/> Representa el códec de audio o vídeo instalado en el sistema del equipo.<br/> |



 

## <a name="networking"></a>Redes

La subcategoría redes agrupa las clases que representan las conexiones de red, los clientes de red y la configuración de conexión de red, como el protocolo usado.



| Clase                                                                            | Descripción                                                                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ActiveRoute**](/previous-versions/windows/desktop/wmiiprouteprov/win32-activeroute)                       | Clase de asociación<br/> Relaciona la ruta de IP4 actual con la tabla de rutas IP persistentes.<br/>                           |
| [**Win32 \_ IP4PersistedRouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4persistedroutetable) | Clase de instancia<br/> Representa rutas IP persistentes.<br/>                                                             |
| [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)                   | Clase de instancia<br/> Representa información que rige el enrutamiento de paquetes de datos de red.<br/>                    |
| [**Win32 \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)         | Clase de evento<br/> Representa los eventos de cambio de ruta IP.<br/>                                                             |
| [**Win32 \_ NetworkClient**](win32-networkclient.md)                              | Clase de instancia<br/> Representa un cliente de red en un equipo que ejecuta Windows.<br/>                           |
| [**Win32 \_ NetworkConnection**](win32-networkconnection.md)                      | Clase de instancia<br/> Representa una conexión de red activa en un entorno de Windows.<br/>                           |
| [**Win32 \_ NetworkProtocol**](win32-networkprotocol.md)                          | Clase de instancia<br/> Representa un protocolo y sus características de red en un equipo que ejecuta Windows.<br/> |
| [**Win32 \_ NTDomain**](/previous-versions/windows/desktop/cimwin32a/win32-ntdomain)                                        | Clase de instancia<br/> Representa un dominio de Windows NT.<br/>                                                             |
| [**Win32 \_ PingStatus**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus)                               | Clase de instancia<br/> Representa los valores devueltos por el comando **ping** estándar.<br/>                            |
| [**Win32 \_ ProtocolBinding**](win32-protocolbinding.md)                          | Clase de asociación<br/> Relaciona un controlador de nivel de sistema, el protocolo de red y el adaptador de red.<br/>                    |



 

## <a name="operating-system-events"></a>Eventos del sistema operativo

La subcategoría eventos del sistema operativo agrupa las clases que representan eventos del sistema operativo relacionados con los procesos, los subprocesos y el cierre del sistema.



| Clase                                                                                 | Descripción                                                                                                                                                              |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ComputerShutdownEvent**](/previous-versions/windows/desktop/cimwin32a/win32-computershutdownevent)                   | Clase de evento<br/> Representa eventos de cierre del equipo.<br/>                                                                                                   |
| [**Win32 \_ ComputerSystemEvent**](/previous-versions/windows/desktop/cimwin32a/win32-computersystemevent)                       | Clase de evento<br/> Representa los eventos relacionados con un sistema informático.<br/>                                                                                        |
| [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md)                           | Clase de evento<br/> Representa eventos de cambio de dispositivo resultantes de la adición, eliminación o modificación de dispositivos en el sistema del equipo.<br/>               |
| [**Win32 \_ ModuleLoadTrace**](/previous-versions/windows/desktop/krnlprov/win32-moduleloadtrace)                               | Clase de evento<br/> Indica que un proceso ha cargado un nuevo módulo.<br/>                                                                                      |
| [**Win32 \_ ModuleTrace**](/previous-versions/windows/desktop/krnlprov/win32-moduletrace)                                       | Clase de evento<br/> Evento base para los eventos del módulo.<br/>                                                                                                          |
| [**Win32 \_ ProcessStartTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstarttrace)                           | Clase de evento<br/> Indica que se ha iniciado un nuevo proceso.<br/>                                                                                              |
| [**Win32 \_ ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace)                             | Clase de evento<br/> Indica que un proceso ha terminado.<br/>                                                                                               |
| [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace)                                     | Clase de evento<br/> Evento base para los eventos de proceso.<br/>                                                                                                         |
| [**Win32 \_ SystemConfigurationChangeEvent**](win32-systemconfigurationchangeevent.md) | Clase de evento<br/> Indica que se ha actualizado la lista de dispositivos del sistema (se ha agregado o quitado un dispositivo o se ha cambiado la configuración).<br/>    |
| [**Win32 \_ SystemTrace**](/previous-versions/windows/desktop/krnlprov/win32-systemtrace)                                       | Clase de evento<br/> Clase base para todos los eventos de seguimiento del sistema, incluidos los seguimientos de módulos, procesos y subprocesos.<br/>                                                  |
| [**Win32 \_ ThreadStartTrace**](/previous-versions/windows/desktop/krnlprov/win32-threadstarttrace)                             | Clase de evento<br/> Indica que se ha iniciado un nuevo subproceso.<br/>                                                                                                    |
| [**Win32 \_ ThreadStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-threadstoptrace)                               | Clase de evento<br/> Indica que un subproceso se ha detenido.<br/>                                                                                                   |
| [**Win32 \_ ThreadTrace**](/previous-versions/windows/desktop/krnlprov/win32-threadtrace)                                       | Clase de evento<br/> Clase de eventos base para eventos de subproceso.<br/>                                                                                                    |
| [**Win32 \_ VolumeChangeEvent**](win32-volumechangeevent.md)                           | Clase de evento<br/> Representa un evento de unidad asignada a la red resultante de la adición de una letra de unidad de red o unidad montada en el sistema del equipo.<br/> |



 

## <a name="operating-system-settings"></a>Configuración del sistema operativo

La subcategoría configuración del sistema operativo agrupa las clases que representan el sistema operativo y su configuración.



| Clase                                                                                       | Descripción                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ BootConfiguration**](win32-bootconfiguration.md)                                 | Clase de instancia<br/> Representa la configuración de arranque de un equipo que ejecuta Windows.<br/>                                                                       |
| [**ComputerSystem de Win32 \_**](win32-computersystem.md)                                       | Clase de instancia<br/> Representa un sistema de equipo que funciona en un entorno de Windows.<br/>                                                                              |
| [**Win32 \_ ComputerSystemProcessor**](win32-computersystemprocessor.md)                     | Clase de asociación<br/> Relaciona un equipo y un procesador que se ejecutan en ese sistema.<br/>                                                                          |
| [**Win32 \_ ComputerSystemProduct**](win32-computersystemproduct.md)                         | Clase de instancia<br/> Representa un producto.<br/>                                                                                                                         |
| [**Win32 \_ DependentService**](win32-dependentservice.md)                                   | Clase de asociación<br/> Relaciona dos servicios base interdependientes.<br/>                                                                                                  |
| [**Win32 \_ LoadOrderGroup**](win32-loadordergroup.md)                                       | Clase de instancia<br/> Representa un grupo de servicios del sistema que definen las dependencias de la ejecución.<br/>                                                                     |
| [**Win32 \_ LoadOrderGroupServiceDependencies**](win32-loadordergroupservicedependencies.md) | Clase de instancia<br/> Representa una asociación entre un servicio base y un grupo de orden de carga del que depende el servicio para empezar a ejecutarse.<br/>                         |
| [**Win32 \_ LoadOrderGroupServiceMembers**](win32-loadordergroupservicemembers.md)           | Clase de asociación<br/> Relaciona un grupo de orden de carga y un servicio base.<br/>                                                                                             |
| [**OperatingSystem de Win32 \_**](win32-operatingsystem.md)                                     | Clase de instancia<br/> Representa un sistema operativo instalado en un equipo con Windows.<br/>                                                                |
| [**Win32 \_ OperatingSystemQFE**](win32-operatingsystemqfe.md)                               | Clase de asociación<br/> Relaciona un sistema operativo y las actualizaciones del producto aplicadas tal y como se representan en [**Win32 \_ QuickFixEngineering**](win32-quickfixengineering.md).<br/> |
| [**Win32 \_ OSRecoveryConfiguration**](win32-osrecoveryconfiguration.md)                     | Clase de instancia<br/> Representa los tipos de información que se van a recopilar de la memoria cuando se produce un error en el sistema operativo.<br/>                                        |
| [**Win32 \_ QuickFixEngineering**](win32-quickfixengineering.md)                             | Clase de instancia<br/> Representa la ingeniería de corrección rápida (QFE) para todo el sistema o las actualizaciones que se han aplicado al sistema operativo actual.<br/>                         |
| [**Win32 \_ StartupCommand**](win32-startupcommand.md)                                       | Clase de instancia<br/> Representa un comando que se ejecuta automáticamente cuando un usuario inicia sesión en el sistema del equipo.<br/>                                                       |
| [**Win32 \_ SystemBootConfiguration**](win32-systembootconfiguration.md)                     | Clase de asociación<br/> Relaciona un equipo con su configuración de arranque.<br/>                                                                                      |
| [**Win32 \_ SystemDesktop**](win32-systemdesktop.md)                                         | Clase de asociación<br/> Relaciona un equipo con su configuración de escritorio.<br/>                                                                                   |
| [**Win32 \_ SystemDevices**](win32-systemdevices.md)                                         | Clase de asociación<br/> Relaciona un equipo y un dispositivo lógico instalado en ese sistema.<br/>                                                                   |
| [**Win32 \_ SystemLoadOrderGroups**](win32-systemloadordergroups.md)                         | Clase de asociación<br/> Relaciona un equipo y un grupo de pedidos de carga.<br/>                                                                                          |
| [**Win32 \_ SystemNetworkConnections**](win32-systemnetworkconnections.md)                   | Clase de asociación<br/> Relaciona una conexión de red y el sistema informático en el que reside.<br/>                                                                  |
| [**Win32 \_ SystemOperatingSystem**](win32-systemoperatingsystem.md)                         | Clase de asociación<br/> Relaciona un equipo con el sistema operativo.<br/>                                                                                        |
| [**Win32 \_ SystemProcesses**](win32-systemprocesses.md)                                     | Clase de asociación <br/> Relaciona un sistema informático y un proceso que se ejecuta en ese sistema.<br/>                                                                           |
| [**Win32 \_ SystemProgramGroups**](win32-systemprogramgroups.md)                             | Clase de asociación<br/> Relaciona un equipo y un grupo de programas lógicos.<br/>                                                                                     |
| [**Win32 \_ SystemResources**](win32-systemresources.md)                                     | Clase de asociación<br/> Relaciona un recurso del sistema y el sistema del equipo en el que reside.<br/>                                                                           |
| [**Win32 \_ SystemServices**](win32-systemservices.md)                                       | Clase de asociación<br/> Relaciona un equipo y un programa de servicio que existe en el sistema.<br/>                                                                 |
| [**Win32 \_ SystemSetting**](win32-systemsetting.md)                                         | Clase de asociación<br/> Relaciona un equipo y una configuración general en ese sistema.<br/>                                                                            |
| [**Win32 \_ SystemSystemDriver**](win32-systemsystemdriver.md)                               | Clase de asociación<br/> Relaciona un equipo y un controlador del sistema que se ejecutan en ese sistema.<br/>                                                             |
| [**Win32 \_ SystemTimeZone**](win32-systemtimezone.md)                                       | Clase de asociación<br/> Relaciona un equipo y una zona horaria.<br/>                                                                                                 |
| [**Win32 \_ SystemUsers**](win32-systemusers.md)                                             | Clase de asociación<br/> Relaciona un equipo y una cuenta de usuario en ese sistema.<br/>                                                                               |



 

## <a name="processes"></a>Procesos

La subcategoría processes agrupa las clases que representan procesos y subprocesos del sistema.



| Clase                                                 | Descripción                                                                                                     |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**\_Proceso Win32**](win32-process.md)               | Clase de instancia<br/> Representa una secuencia de eventos en un equipo que ejecuta Windows.<br/>      |
| [**Win32 \_ ProcessStartup**](win32-processstartup.md) | Clase de instancia<br/> Representa la configuración de inicio de un equipo que ejecuta Windows.<br/> |
| [**Subproceso Win32 \_**](win32-thread.md)                 | Clase de instancia<br/> Representa un subproceso de ejecución.<br/>                                          |



 

## <a name="registry"></a>Registro

La clase de la subcategoría del registro representa el contenido del registro de Windows.



| Clase                                     | Descripción                                                                                               |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**Registro de Win32 \_**](win32-registry.md) | Clase de instancia<br/> Representa el registro del sistema en un equipo que ejecuta Windows.<br/> |



 

## <a name="scheduler-jobs"></a>Trabajos del Programador

La subcategoría trabajos del programador agrupa las clases que representan la configuración del trabajo programado.



| Clase                                                | Descripción                                                                                                                                                                                                                                                           |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ CurrentTime**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) | Clase abstracta<br/> Representa una instancia de en el tiempo como componentes segundos, minutos, día de la semana, etc.<br/>                                                                                                                                        |
| [**Win32 \_ ScheduledJob**](win32-scheduledjob.md)    | Clase de instancia<br/> Representa un trabajo programado mediante el servicio de programación de Windows.<br/>                                                                                                                                                                   |
| [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime)     | Clase de instancia<br/> Representa un punto en el tiempo devuelto como objetos [**\_ localtime de Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) que son el resultado de una consulta. La propiedad **hour** se devuelve como la hora local en un reloj de 24 horas.<br/>                                |
| [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)         | Clase de instancia<br/> Representa un punto en el tiempo que se devuelve como objetos [**\_ UTCTime de Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) que son el resultado de una consulta. La propiedad **hour** se devuelve como hora universal coordinada (UTC) en un reloj de 24 horas.<br/> |



 

## <a name="security"></a>Seguridad

La subcategoría seguridad agrupa las clases que representan la configuración de seguridad del sistema.



| Clase                                                                               | Descripción                                                                                                                                                  |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ AccountSID**](/previous-versions/windows/desktop/secrcw32prov/win32-accountsid)                                       | Clase de asociación<br/> Relaciona una instancia de cuenta de seguridad con una instancia de descriptor de seguridad.<br/>                                             |
| [**ACE de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)                                                     | Clase de instancia<br/> Representa una entrada de control de acceso (ACE).<br/>                                                                               |
| [**Win32 \_ LogicalFileAccess**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileaccess)                         | Clase de asociación<br/> Relaciona la configuración de seguridad de un archivo o directorio y un miembro de su lista de control de acceso discrecional (DACL).<br/> |
| [**Win32 \_ LogicalFileAuditing**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileauditing)                     | Clase de asociación<br/> Relaciona la configuración de seguridad de un archivo o directorio con un miembro de su lista de control de acceso de sistema (SACL).<br/>            |
| [**Win32 \_ LogicalFileGroup**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilegroup)                           | Clase de asociación<br/> Relaciona la configuración de seguridad de un archivo o directorio y su grupo.<br/>                                                  |
| [**Win32 \_ LogicalFileOwner**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileowner)                           | Clase de asociación<br/> Relaciona la configuración de seguridad de un archivo o directorio y su propietario.<br/>                                                  |
| [**Win32 \_ LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)       | Clase de instancia<br/> Representa la configuración de seguridad de un archivo lógico.<br/>                                                                        |
| [**Win32 \_ LogicalShareAccess**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalshareaccess)                       | Clase de asociación<br/> Relaciona la configuración de seguridad de un recurso compartido y un miembro de su DACL.<br/>                                                 |
| [**Win32 \_ LogicalShareAuditing**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalshareauditing)                   | Clase de asociación<br/> Relaciona la configuración de seguridad de un recurso compartido y un miembro de su SACL.<br/>                                                 |
| [**Win32 \_ LogicalShareSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting)     | Clase de instancia<br/> Representa la configuración de seguridad de un archivo lógico.<br/>                                                                        |
| [**Win32 \_ PrivilegesStatus**](win32-privilegesstatus.md)                           | Clase de instancia<br/> Representa información sobre los privilegios necesarios para completar una operación.<br/>                                          |
| [**SecurityDescriptor de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)                       | Clase de instancia<br/> Representa una representación estructural de un [**\_ descriptor de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor).<br/>                   |
| [**Win32 \_ SecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysetting)                             | Clase de instancia<br/> Representa la configuración de seguridad para un elemento administrado.<br/>                                                                     |
| [**Win32 \_ SecuritySettingAccess**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingaccess)                 | Clase de instancia<br/> Representa los derechos concedidos y denegados a un administrador de confianza para un objeto determinado.<br/>                                               |
| [**Win32 \_ SecuritySettingAuditing**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingauditing)             | Clase de instancia<br/> Representa la auditoría para un administrador de confianza determinado en un objeto determinado.<br/>                                                          |
| [**Win32 \_ SecuritySettingGroup**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettinggroup)                   | Clase de asociación<br/> Relaciona la seguridad de un objeto y su grupo.<br/>                                                                     |
| [**Win32 \_ SecuritySettingOfLogicalFile**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingoflogicalfile)   | Clase de instancia<br/> Representa la configuración de seguridad de un objeto de archivo o de directorio.<br/>                                                             |
| [**Win32 \_ SecuritySettingOfLogicalShare**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingoflogicalshare) | Clase de instancia<br/> Representa la configuración de seguridad de un objeto compartido.<br/>                                                                        |
| [**Win32 \_ SecuritySettingOfObject**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingofobject)             | Clase de asociación<br/> Relaciona un objeto con su configuración de seguridad.<br/>                                                                          |
| [**Win32 \_ SecuritySettingOwner**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingowner)                   | Clase de asociación<br/> Relaciona la configuración de seguridad de un objeto y su propietario.<br/>                                                            |
| [**SID de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-sid)                                                     | Clase de instancia<br/> Representa un SID arbitrario.<br/>                                                                                            |
| [**Administrador de confianza de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)                                             | Clase de instancia<br/> Representa un administrador de confianza.<br/>                                                                                                   |



 

## <a name="services"></a>Servicios

La subcategoría servicios agrupa las clases que representan servicios y servicios básicos.



| Clase                                           | Descripción                                                                                                                                             |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ BaseService**](win32-baseservice.md) | Clase de instancia<br/> Representa objetos ejecutables que se instalan en una base de datos del registro que mantiene el administrador de control de servicios.<br/> |
| [**\_Servicio Win32**](win32-service.md)         | Clase de instancia<br/> Representa un servicio en un equipo que ejecuta Windows.<br/>                                                         |



 

## <a name="shares"></a>Recursos compartidos

Las clases de grupos de subcategoría de recursos compartidos que representan detalles de recursos compartidos, como impresoras y carpetas.



| Clase                                                       | Descripción                                                                                                                                                                                          |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ DFSNode**](/previous-versions/windows/desktop/wmipdfs/win32-dfsnode)                     | Clase de asociación<br/> Representa un nodo raíz o de unión de un sistema de archivos distribuido (DFS) basado en dominio o independiente.<br/>                                                           |
| [**Win32 \_ DFSNodeTarget**](/previous-versions/windows/desktop/wmipdfs/win32-dfsnodetarget)         | Clase de asociación<br/> Representa la relación de un nodo DFS con uno de sus destinos.<br/>                                                                                             |
| [**Win32 \_ DFSTarget**](/previous-versions/windows/desktop/wmipdfs/win32-dfstarget)                 | Clase de asociación<br/> Representa el destino de un nodo DFS.<br/>                                                                                                                         |
| [**Win32 \_ ServerConnection**](/previous-versions/windows/desktop/wmipsess/win32-serverconnection)   | Clase de instancia<br/> Representa las conexiones realizadas desde un equipo remoto con un recurso compartido en el equipo local.<br/>                                                              |
| [**Win32 \_ ServerSession**](/previous-versions/windows/desktop/wmipsess/win32-serversession)         | Clase de instancia<br/> Representa las sesiones que los usuarios establecen con el equipo local en un equipo remoto.<br/>                                                             |
| [**Win32 \_ ConnectionShare**](/previous-versions/windows/desktop/wmipsess/win32-connectionshare)     | Clase de asociación<br/> Relaciona un recurso compartido en el equipo y la conexión realizada al recurso compartido.<br/>                                                                    |
| [**Win32 \_ PrinterShare**](win32-printershare.md)           | Clase de asociación<br/> Relaciona una impresora local y el recurso compartido que la representa como se ve a través de una red.<br/>                                                                     |
| [**Win32 \_ SessionConnection**](/previous-versions/windows/desktop/wmipsess/win32-sessionconnection) | Clase de asociación<br/> Representa una asociación entre una sesión establecida con el servidor local por un usuario en un equipo remoto y las conexiones que dependen de la sesión.<br/> |
| [**Win32 \_ SessionProcess**](win32-sessionprocess.md)       | Clase de asociación<br/> Representa una asociación entre una sesión de inicio de sesión y los procesos asociados a esa sesión.<br/>                                                            |
| [**Win32 \_ ShareToDirectory**](win32-sharetodirectory.md)   | Clase de asociación<br/> Relaciona un recurso compartido en el sistema del equipo y el directorio al que está asignado.<br/>                                                                    |
| [**\_Recurso compartido de Win32**](win32-share.md)                         | Clase de instancia<br/> Representa un recurso compartido en un equipo que ejecuta Windows.<br/>                                                                                              |



 

## <a name="start-menu"></a>Menú Inicio

La subcategoría menú Inicio agrupa las clases que representan grupos de programas.



| Clase                                                                                   | Descripción                                                                                                                                                              |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ LogicalProgramGroup**](win32-logicalprogramgroup.md)                         | Clase de instancia<br/> Representa un grupo de programas en un equipo con Windows.<br/>                                                                    |
| [**Win32 \_ LogicalProgramGroupDirectory**](win32-logicalprogramgroupdirectory.md)       | Clase de asociación<br/> Relaciona los grupos de programas lógicos (agrupaciones en el menú Inicio) y los directorios de archivos en los que se almacenan.<br/>                 |
| [**Win32 \_ LogicalProgramGroupItem**](win32-logicalprogramgroupitem.md)                 | Clase de instancia<br/> Representa un elemento incluido en una instancia de **\_ ProgramGroup de Win32** , que no es otra instancia de **Win32 \_ ProgramGroup** .<br/> |
| [**Win32 \_ LogicalProgramGroupItemDataFile**](win32-logicalprogramgroupitemdatafile.md) | Clase de asociación<br/> Relaciona los elementos del grupo de programas del menú Inicio y los archivos en los que se almacenan.<br/>                                       |
| [**Win32 \_ ProgramGroupContents**](win32-programgroupcontents.md)                       | Clase de asociación<br/> Relaciona un orden de grupo de programas y un grupo de programas o un elemento individual que contiene.<br/>                                           |
| [**Win32 \_ ProgramGroupOrItem**](win32-programgrouporitem.md)                           | Clase de instancia<br/> Representa una agrupación lógica de programas en el menú **Inicio** de \| **programas** del usuario.<br/>                                               |



 

## <a name="storage"></a>Almacenamiento

La subcategoría usuarios agrupa las clases que representan información de almacenamiento.



| Clase                                                                   | Descripción                                                                                                                                  |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ShadowBy**](/previous-versions/windows/desktop/vsswmi/win32-shadowby)                               | Clase de asociación<br/> Representa la asociación entre una instantánea y el proveedor que crea la instantánea.<br/>      |
| [**Win32 \_ ShadowContext**](/previous-versions/windows/desktop/vsswmi/win32-shadowcontext)                     | Clase de asociación<br/> Especifica cómo se va a crear, consultar o eliminar una instantánea.<br/>                                   |
| [**\_Instantánea Win32**](/previous-versions/windows/desktop/legacy/aa394428(v=vs.85))                           | Clase de instancia<br/> Representa una copia duplicada del volumen original en un momento anterior.<br/>                                  |
| [**Win32 \_ ShadowDiffVolumeSupport**](/previous-versions/windows/desktop/vsswmi/win32-shadowdiffvolumesupport) | Clase de asociación<br/> Representa una asociación entre un proveedor de instantáneas y un volumen de almacenamiento.<br/>                       |
| [**Win32 \_ ShadowFor**](/previous-versions/windows/desktop/vsswmi/win32-shadowfor)                             | Clase de asociación<br/> Representa una asociación entre una instantánea y el volumen para el que se crea la instantánea.<br/> |
| [**Sombras de Win32 \_**](/previous-versions/windows/desktop/vsswmi/win32-shadowon)                               | Clase de asociación<br/> Representa una asociación entre una instantánea y dónde se escriben los datos diferenciales.<br/>          |
| [**Win32 \_ ShadowProvider**](/previous-versions/windows/desktop/vsswmi/win32-shadowprovider)                   | Clase de asociación<br/> Representa un componente que crea y representa instantáneas de volumen.<br/>                             |
| [**Win32 \_ ShadowStorage**](/previous-versions/windows/desktop/legacy/aa394433(v=vs.85))                     | Clase de asociación<br/> Representa una asociación entre una instantánea y dónde se escriben los datos diferenciales.<br/>          |
| [**Win32 \_ ShadowVolumeSupport**](/previous-versions/windows/desktop/vsswmi/win32-shadowvolumesupport)         | Clase de asociación<br/> Representa una asociación entre un proveedor de instantáneas con un volumen compatible.<br/>                    |
| [**\_Volumen Win32**](/previous-versions/windows/desktop/legacy/aa394515(v=vs.85))                                   | Clase de instancia<br/> Representa un área de almacenamiento en un disco duro.<br/>                                                           |
| [**Win32 \_ VolumeUserQuota**](/previous-versions/windows/desktop/vdswmi/win32-volumeuserquota)                 | Clase de asociación<br/> Representa un volumen para la configuración de cuota por volumen.<br/>                                                |



 

## <a name="users"></a>Usuarios

La subcategoría usuarios agrupa las clases que representan la información de la cuenta de usuario, como los detalles de la pertenencia a grupos.



| Clase                                                                 | Descripción                                                                                                                                      |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Cuenta Win32**](win32-account.md)                               | Clase de instancia<br/> Representa información acerca de las cuentas de usuario y las cuentas de grupo que conoce el equipo que ejecuta Windows.<br/> |
| [**\_Grupo Win32**](win32-group.md)                                   | Clase de instancia<br/> Representa los datos de una cuenta de grupo.<br/>                                                                      |
| [**Win32 \_ GroupInDomain**](/previous-versions/windows/desktop/cimwin32a/win32-groupindomain)                   | Clase de asociación<br/> Identifica las cuentas de grupo asociadas a un dominio de Windows NT.<br/>                                       |
| [**Win32 \_ GroupUser**](win32-groupuser.md)                           | Clase de asociación<br/> Relaciona un grupo y una cuenta que es miembro de ese grupo.<br/>                                           |
| [**Win32 \_ LogonSession**](win32-logonsession.md)                     | Clase de instancia<br/> Describe la sesión de inicio de sesión o las sesiones asociadas a un usuario que ha iniciado sesión en Windows.<br/>                        |
| [**Win32 \_ LogonSessionMappedDisk**](/windows/desktop/CIMWin32Prov/win32-logonsessionmappeddisk) | Clase de instancia<br/> Representa los discos lógicos asignados asociados a la sesión.<br/>                                            |
| [**Win32 \_ NetworkLoginProfile**](win32-networkloginprofile.md)       | Clase de instancia<br/> Representa la información de inicio de sesión de red de un usuario específico en un equipo que ejecuta Windows.<br/>           |
| [**Win32 \_ SystemAccount**](win32-systemaccount.md)                   | Clase de instancia<br/> Representa una cuenta del sistema.<br/>                                                                                |
| [**Cuentadeusuario de Win32 \_**](win32-useraccount.md)                       | Clase de instancia<br/> Representa información acerca de una cuenta de usuario en un equipo que ejecuta Windows.<br/>                           |
| [**Win32 \_ UserInDomain**](/previous-versions/windows/desktop/cimwin32a/win32-userindomain)                     | Clase de asociación<br/> Relaciona una cuenta de usuario y un dominio de Windows NT.<br/>                                                          |



 

## <a name="windows-event-log"></a>Registro de errores de Windows

La subcategoría registro de eventos de Windows agrupa las clases que representan eventos, entradas del registro de eventos, opciones de configuración del registro de eventos, etc.



| Clase                                                         | Descripción                                                                                                                                                                   |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))         | Clase de instancia<br/> Representa los datos almacenados en un archivo de registro de eventos de Windows.<br/>                                                                                      |
| [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent)                 | Clase de instancia<br/> Representa los eventos de Windows.<br/>                                                                                                               |
| [**Win32 \_ NTLogEventComputer**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventcomputer) | Clase de asociación<br/> Relaciona las instancias de [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) y [**Win32 \_ ComputerSystem**](win32-computersystem.md).<br/>         |
| [**Win32 \_ NTLogEventLog**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventlog)           | Clase de asociación<br/> Relaciona las instancias de [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) y las clases [**\_ NTEventlogFile de Win32**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) .<br/> |
| [**Win32 \_ NTLogEventUser**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventuser)         | Clase de asociación<br/> Relaciona las instancias de [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) y [**Win32 \_ cuentadeusuario**](win32-useraccount.md).<br/>               |



 

## <a name="windows-product-activation"></a>Activación de productos de Windows

La activación de productos de Windows (WPA) es una tecnología antipiratería para reducir la copia casual del software.



| Clase                                                                                                               | Descripción                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ComputerSystemWindowsProductActivationSetting**](/previous-versions/windows/desktop/licwmiprov/win32-computersystemwindowsproductactivationsetting) | Clase de asociación<br/> Relaciona las instancias de [**Win32 \_ ComputerSystem**](win32-computersystem.md) y [**Win32 \_ WindowsProductActivation**](/previous-versions/windows/desktop/legacy/aa394520(v=vs.85)).<br/> |
| [**\_Proxy Win32**](/previous-versions/windows/desktop/legacy/aa394389(v=vs.85))                                                                                 | Clase de instancia<br/> Contiene propiedades y métodos para consultar y configurar una conexión a Internet relacionada con WPA.<br/>                                                                |
| [**Win32 \_ WindowsProductActivation**](/previous-versions/windows/desktop/legacy/aa394520(v=vs.85))                                           | Clase de instancia<br/> Contiene propiedades y métodos relacionados con WPA.<br/>                                                                                                              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clases Win32](/previous-versions//aa394084(v=vs.85))
</dt> </dl>

 

