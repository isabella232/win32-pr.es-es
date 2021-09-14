---
description: La categoría Sistema operativo agrupa las clases que representan objetos relacionados con el sistema operativo.
ms.assetid: D0756D8C-A3D3-4C75-96A3-8C7F05300B39
ms.tgt_platform: multiple
title: Clases de sistema operativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f47df8a949e3ac07bf2099ea708d496bed87298
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062695"
---
# <a name="operating-system-classes"></a>Clases de sistema operativo

La categoría Sistema operativo agrupa las clases que representan objetos relacionados con el sistema operativo. Denotan las distintas configuraciones y configuraciones que definen un entorno informático. Algunos ejemplos son: la configuración de arranque, la configuración del Modelo de objetos componentes (COM), la configuración del entorno de escritorio, los controladores, la configuración de seguridad, la configuración del usuario y la configuración del Registro.

La categoría Sistema operativo se agrupa en las subcategorías siguientes:

-   [COM](#com)
-   [Dispositivo de escritorio](#desktop)
-   [Controladores](#drivers)
-   [Registro de eventos](#windows-event-log)
-   [Sistema de archivos](#file-system)
-   [Objetos de trabajo](#job-objects)
-   [Archivos de memoria y de página](#memory-and-page-files)
-   [Audio multimedia o objeto visual](#multimedia-audio-or-visual)
-   [Redes](#networking)
-   [Eventos del sistema operativo](#operating-system-events)
-   [Configuración del sistema operativo](#operating-system-settings)
-   [Procesos](#processes)
-   [Registro](#registry)
-   [Trabajos de Scheduler](#scheduler-jobs)
-   [Seguridad](#security)
-   [Servicios](#services)
-   [Recursos compartidos](#shares)
-   [Menú Inicio](#start-menu)
-   [Storage](#storage)
-   [Usuarios](#users)
-   [Windows activación del producto](#windows-product-activation)

## <a name="com"></a>COM

La subcategoría COM agrupa las clases que representan la configuración de COM y DCOM, las clases y la configuración de la aplicación cliente.



| Clase                                                                                           | Descripción                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ClassicCOMApplicationClasses**](win32-classiccomapplicationclasses.md)               | Association (clase)<br/> Relaciona una aplicación DCOM y un componente COM agrupado en ella.<br/>                                                                             |
| [**Win32 \_ ClassicCOMClass**](win32-classiccomclass.md)                                         | Clase de instancia<br/> Representa las propiedades de un componente COM.<br/>                                                                                                   |
| [**Win32 \_ ClassicCOMClassSettings**](win32-classiccomclasssettings.md)                         | Association (clase)<br/> Relaciona una clase COM y la configuración utilizada para configurar instancias de la clase COM.<br/>                                                           |
| [**ClientApplicationSetting de Win32 \_**](win32-clientapplicationsetting.md)                       | Association (clase)<br/> Relaciona un archivo ejecutable y una aplicación DCOM que contiene las opciones de configuración de DCOM para el archivo ejecutable.<br/>                           |
| [**ComApplication de Win32 \_**](win32-comapplication.md)                                           | Clase de instancia<br/> Representa una aplicación COM.<br/>                                                                                                                   |
| [**ComApplicationClasses de Win32 \_**](win32-comapplicationclasses.md)                             | Association (clase)<br/> Relaciona un componente COM y la aplicación COM donde reside.<br/>                                                                            |
| [**ComApplicationSettings de Win32 \_**](win32-comapplicationsettings.md)                           | Association (clase)<br/> Relaciona una aplicación DCOM y sus opciones de configuración.<br/>                                                                                   |
| [**Win32 \_ COMClass**](win32-comclass.md)                                                       | Clase de instancia<br/> Representa las propiedades de un componente COM.<br/>                                                                                                   |
| [**Win32 \_ ComClassAutoEmulator**](win32-comclassautoemulator.md)                               | Association (clase)<br/> Relaciona una clase COM y otra clase COM que emula automáticamente.<br/>                                                                    |
| [**Win32 \_ ComClassEmulator**](win32-comclassemulator.md)                                       | Association (clase)<br/> Relaciona dos versiones de una clase COM.<br/>                                                                                                         |
| [**ComponentCategory de Win32 \_**](win32-componentcategory.md)                                     | Clase de instancia<br/> Representa una categoría de componente.<br/>                                                                                                                |
| [**ComSetting de Win32 \_**](win32-comsetting.md)                                                   | Clase de instancia<br/> Representa la configuración asociada a un componente COM o una aplicación COM.<br/>                                                                     |
| [**DCOMApplication de Win32 \_**](win32-dcomapplication.md)                                         | Clase de instancia<br/> Representa las propiedades de una aplicación DCOM.<br/>                                                                                                |
| [**Win32 \_ DCOMApplicationAccessAllowedSetting**](/previous-versions/windows/desktop/secrcw32prov/win32-dcomapplicationaccessallowedsetting) | Association (clase)<br/> Relaciona la instancia [**de \_ DCOMApplication de Win32**](win32-dcomapplication.md) y las identificaciones de seguridad de usuario (SID) que pueden acceder a ella.<br/> |
| [**Win32 \_ DCOMApplicationLaunchAllowedSetting**](/previous-versions/windows/desktop/secrcw32prov/win32-dcomapplicationlaunchallowedsetting) | Association (clase)<br/> Relaciona la instancia [**de \_ DCOMApplication de Win32**](win32-dcomapplication.md) y los SID de usuario que pueden iniciarla.<br/>                           |
| [**Win32 \_ DCOMApplicationSetting**](win32-dcomapplicationsetting.md)                           | Clase de instancia<br/> Representa la configuración de una aplicación DCOM.<br/>                                                                                                  |
| [**Win32 \_ ImplementedCategory**](win32-implementedcategory.md)                                 | Association (clase)<br/> Relaciona una categoría de componente y la clase COM mediante sus interfaces.<br/>                                                                         |



 

## <a name="desktop"></a>Escritorio

La subcategoría Desktop agrupa clases que representan objetos que definen una configuración de escritorio específica.



| Clase                                           | Descripción                                                                                                                        |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Escritorio \_ win32**](win32-desktop.md)         | Clase de instancia<br/> Representa las características comunes del escritorio de un usuario.<br/>                                    |
| [**Entorno de \_ Win32**](win32-environment.md) | Clase de instancia<br/> Representa una configuración de entorno o entorno del sistema en un sistema informático que ejecuta Windows.<br/> |
| [**Zona horaria \_ win32**](win32-timezone.md)       | Clase de instancia<br/> Representa la información de zona horaria de un sistema informático que ejecuta Windows.<br/>                   |
| [**UserDesktop de Win32 \_**](win32-userdesktop.md) | Association (clase)<br/> Relaciona una cuenta de usuario y la configuración de escritorio que son específicas de ella.<br/>                   |



 

## <a name="drivers"></a>Controladores

La subcategoría Controladores agrupa clases que representan controladores de dispositivos virtuales y controladores del sistema para los servicios base.



| Clase                                             | Descripción                                                                           |
|---------------------------------------------------|---------------------------------------------------------------------------------------|
| [**Win32 \_ SystemDriver**](win32-systemdriver.md) | Clase de instancia<br/> Representa el controlador del sistema para un servicio base.<br/> |



 

## <a name="file-system"></a>Sistema de archivos

La subcategoría Sistema de archivos agrupa clases que representan la manera en que se organiza lógicamente un disco duro. Esto incluye el tipo de sistema de archivos utilizado, la estructura de directorios y la forma en que se particiona el disco.



| Clase                                                                               | Descripción                                                                                                                                                                          |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CimLogicalDeviceCIMDataFile de Win32 \_**](win32-cimlogicaldevicecimdatafile.md)     | Association (clase)<br/> Relaciona los dispositivos lógicos y los archivos de datos, lo que indica los archivos de controlador utilizados por el dispositivo.<br/>                                                      |
| [**Directorio \_ Win32**](win32-directory.md)                                         | Clase de instancia<br/> Representa una entrada de directorio en un sistema de equipo que ejecuta Windows.<br/>                                                                              |
| [**DirectorySpecification de Win32 \_**](/previous-versions/windows/desktop/msiprov/win32-directoryspecification)               | Clase de instancia<br/> Representa el diseño del directorio para el producto.<br/>                                                                                                |
| [**Win32 \_ DiskDriveToDiskPartition**](win32-diskdrivetodiskpartition.md)           | Association (clase)<br/> Relaciona una unidad de disco y una partición existente en ella.<br/>                                                                                         |
| [**Win32 \_ DiskPartition**](win32-diskpartition.md)                                 | Clase de instancia<br/> Representa las capacidades y la capacidad de administración de un área con particiones de un disco físico en un equipo que ejecuta Windows.<br/>              |
| [**Win32 \_ DiskQuota**](/previous-versions/windows/desktop/wmipdskq/win32-diskquota)                                    | Association (clase)<br/> Realiza un seguimiento del uso del espacio en disco para los volúmenes del sistema de archivos NTFS.<br/>                                                                                        |
| [**Disco lógico de Win32 \_**](win32-logicaldisk.md)                                     | Representa un origen de datos que se resuelve en un dispositivo de almacenamiento local real en un equipo que ejecuta Windows.<br/>                                                            |
| [**Win32 \_ LogicalDiskRootDirectory**](win32-logicaldiskrootdirectory.md)           | Association (clase)<br/> Relaciona un disco lógico y su estructura de directorios.<br/>                                                                                          |
| [**Win32 \_ LogicalDiskToPartition**](win32-logicaldisktopartition.md)               | Association (clase)<br/> Relaciona una unidad de disco lógico y la partición de disco en la que reside.<br/>                                                                           |
| [**Win32 \_ MappedLogicalDisk**](win32-mappedlogicaldisk.md)                         | Representa los dispositivos de almacenamiento de red que se asignan como discos lógicos en el sistema informático que ejecuta Windows.<br/>                                                               |
| [**Win32 \_ OperatingSystemAutochkSetting**](/previous-versions//aa394240(v=vs.85)) | Association (clase)<br/> Representa la asociación entre una [**instancia \_ de ManagedSystemElement de CIM**](cim-managedsystemelement.md) y la configuración definida para ella.<br/> |
| [**QuotaSetting de Win32 \_**](/previous-versions/windows/desktop/wmipdskq/win32-quotasetting)                              | Clase de instancia<br/> Contiene información de configuración para las cuotas de disco en un volumen.<br/>                                                                                       |
| [**Win32 \_ ShortcutFile**](win32-shortcutfile.md)                                   | Clase de instancia<br/> Representa archivos que son accesos directos a otros archivos, directorios y comandos.<br/>                                                                  |
| [**\_Subdirectorio win32**](win32-subdirectory.md)                                   | Association (clase)<br/> Relaciona un directorio (carpeta) y uno de sus subdirectorios (subcarpetas).<br/>                                                                     |
| [**Win32 \_ SystemPartitions**](win32-systempartitions.md)                           | Association (clase)<br/> Relaciona un sistema informático y una partición de disco en ese sistema.<br/>                                                                               |
| [**Volumen \_ win32**](/previous-versions/windows/desktop/legacy/aa394515(v=vs.85))                                               | Clase de instancia<br/> Representa un área de almacenamiento en un disco duro.<br/>                                                                                                   |
| [**Win32 \_ VolumeQuota**](/previous-versions/windows/desktop/vdswmi/win32-volumequota)                                     | Association (clase)<br/> Relaciona un volumen con la configuración de cuota por volumen.<br/>                                                                                           |
| [**Win32 \_ VolumeQuotaSetting**](/previous-versions/windows/desktop/wmipdskq/win32-volumequotasetting)                  | Association (clase)<br/> Relaciona la configuración de cuota de disco con un volumen de disco específico.<br/>                                                                                     |
| [**Win32 \_ VolumeUserQuota**](/previous-versions/windows/desktop/vdswmi/win32-volumeuserquota)                             | Association (clase)<br/> Relaciona las cuotas por usuario con volúmenes habilitados para cuota.<br/>                                                                                            |



 

## <a name="job-objects"></a>Objetos de trabajo

La subcategoría Objetos de trabajo agrupa clases que representan clases que proporcionan los medios para instrumentar objetos de trabajo con nombre. No se puede instrumentar un objeto de trabajo sin nombre.



| Clase                                                                               | Descripción                                                                                                                                                                                |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ CollectionStatistics**](/previous-versions/windows/desktop/cimwin32a/win32-collectionstatistics)                   | Association (clase)<br/> Relaciona una colección de elementos del sistema administrado y la clase que representa información estadística sobre la colección.<br/>                               |
| [**LUID de Win32 \_**](/previous-versions/windows/desktop/wmipjobobjprov/win32-luid)                                                   | Clase de instancia<br/> Representa un identificador único local (LUID)<br/>                                                                                                         |
| [**Win32 \_ LUIDandAttributes**](/previous-versions/windows/desktop/wmipjobobjprov/win32-luidandattributes)                         | Clase de instancia<br/> Representa un LUID y sus atributos.<br/>                                                                                                                 |
| [**Win32 \_ NamedJobObject**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobject)                               | Clase de instancia<br/> Representa un objeto kernel que se usa para agrupar procesos con el fin de controlar la vida y los recursos de los procesos dentro del objeto de trabajo.<br/> |
| [**Win32 \_ NamedJobObjectActgInfo**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectactginfo)               | Clase de instancia<br/> Representa la información de contabilidad de E/S para un objeto de trabajo.<br/>                                                                                           |
| [**Win32 \_ NamedJobObjectLimit**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectlimit)                     | Clase de instancia<br/> Representa una asociación entre un objeto de trabajo y la configuración de límite de objetos de trabajo.<br/>                                                                     |
| [**Win32 \_ NamedJobObjectLimitSetting**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectlimitsetting)       | Clase de instancia<br/> Representa la configuración de límite de un objeto de trabajo.<br/>                                                                                                       |
| [**Win32 \_ NamedJobObjectProcess**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectprocess)                 | Clase de instancia<br/> Relaciona un objeto de trabajo y el proceso contenido en el objeto de trabajo.<br/>                                                                                     |
| [**Win32 \_ NamedJobObjectSecLimit**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectseclimit)               | Clase de instancia<br/> Relaciona un objeto de trabajo y la configuración del límite de seguridad del objeto de trabajo.<br/>                                                                                      |
| [**Win32 \_ NamedJobObjectSecLimitSetting**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectseclimitsetting) | Clase de instancia<br/> Representa la configuración del límite de seguridad para un objeto de trabajo.<br/>                                                                                              |
| [**Win32 \_ NamedJobObjectStatistics**](/previous-versions/windows/desktop/wmipjobobjprov/win32-namedjobobjectstatistics)           | Clase de instancia<br/> Representa una asociación entre un objeto de trabajo y la clase de información de contabilidad de E/S del objeto de trabajo.<br/>                                                   |
| [**SIDandAttributes de Win32 \_**](/previous-versions/windows/desktop/wmipjobobjprov/win32-sidandattributes)                           | Clase de instancia<br/> Representa un identificador de seguridad (SID) y sus atributos.<br/>                                                                                            |
| [**TokenGroups de Win32 \_**](/previous-versions/windows/desktop/wmipjobobjprov/win32-tokengroups)                                     | Clase de evento<br/> Representa información sobre los SID de grupo en un token de acceso.<br/>                                                                                          |
| [**TokenPrivileges de Win32 \_**](/previous-versions/windows/desktop/wmipjobobjprov/win32-tokenprivileges)                             | Clase de evento<br/> Representa información sobre un conjunto de privilegios para un token de acceso.<br/>                                                                                    |



 

## <a name="memory-and-page-files"></a>Archivos de memoria y de página

La subcategoría Archivos de memoria y Página agrupa las clases que representan los valores de configuración del archivo de página.



| Clase                                                                 | Descripción                                                                                                                                   |
|-----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ PageFile**](win32-pagefile.md)                             | Clase de instancia<br/> Representa el archivo utilizado para controlar el intercambio de archivos de memoria virtual en un Windows virtual.<br/>                  |
| [**Win32 \_ PageFileElementSetting**](win32-pagefileelementsetting.md) | Association (clase)<br/> Relaciona la configuración inicial de un archivo de página y el estado de dicha configuración durante el uso normal.<br/>        |
| [**Win32 \_ PageFileSetting**](win32-pagefilesetting.md)               | Clase de instancia<br/> Representa la configuración de un archivo de página.<br/>                                                                  |
| [**Win32 \_ PageFileUsage**](win32-pagefileusage.md)                   | Clase de instancia<br/> Representa el archivo usado para controlar el intercambio de archivos de memoria virtual en un sistema de equipo que ejecuta Windows.<br/> |



 

## <a name="multimedia-audio-or-visual"></a>Audio multimedia o objeto visual

La clase de la subcategoría Multimedia Audio o Visual representa las propiedades del códec de audio o vídeo instalado en el sistema del equipo.



| Clase                                       | Descripción                                                                                                |
|---------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**CódecFile de \_ Win32**](win32-codecfile.md) | Clase de instancia<br/> Representa el códec de audio o vídeo instalado en el sistema informático.<br/> |



 

## <a name="networking"></a>Redes

La subcategoría Redes agrupa las clases que representan las conexiones de red, los clientes de red y la configuración de conexión de red, como el protocolo utilizado.



| Clase                                                                            | Descripción                                                                                                                      |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ActiveRoute**](/previous-versions/windows/desktop/wmiiprouteprov/win32-activeroute)                       | Association (clase)<br/> Relaciona la ruta IP4 actual con la tabla de rutas IP persistente.<br/>                           |
| [**Win32 \_ IP4PersistedRouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4persistedroutetable) | Clase de instancia<br/> Representa las rutas IP persistentes.<br/>                                                             |
| [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable)                   | Clase de instancia<br/> Representa información que rige el enrutamiento de paquetes de datos de red.<br/>                    |
| [**Win32 \_ IP4RouteTableEvent**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetableevent)         | Clase de evento<br/> Representa eventos de cambio de ruta IP.<br/>                                                             |
| [**Win32 \_ NetworkClient**](win32-networkclient.md)                              | Clase de instancia<br/> Representa un cliente de red en un sistema informático que ejecuta Windows.<br/>                           |
| [**Win32 \_ NetworkConnection**](win32-networkconnection.md)                      | Clase de instancia<br/> Representa una conexión de red activa en un Windows activo.<br/>                           |
| [**Win32 \_ NetworkProtocol**](win32-networkprotocol.md)                          | Clase de instancia<br/> Representa un protocolo y sus características de red en un sistema informático que ejecuta Windows.<br/> |
| [**Win32 \_ NTDomain**](/previous-versions/windows/desktop/cimwin32a/win32-ntdomain)                                        | Clase de instancia<br/> Representa un Windows NT.<br/>                                                             |
| [**PingStatus de Win32 \_**](/previous-versions/windows/desktop/wmipicmp/win32-pingstatus)                               | Clase de instancia<br/> Representa los valores devueltos por el comando **ping** estándar.<br/>                            |
| [**Win32 \_ ProtocolBinding**](win32-protocolbinding.md)                          | Association (clase)<br/> Relaciona un controlador de nivel de sistema, un protocolo de red y un adaptador de red.<br/>                    |



 

## <a name="operating-system-events"></a>Eventos del sistema operativo

La subcategoría Eventos del sistema operativo agrupa clases que representan eventos en el sistema operativo relacionados con procesos, subprocesos y apagado del sistema.



| Clase                                                                                 | Descripción                                                                                                                                                              |
|---------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ComputerShutdownEvent**](/previous-versions/windows/desktop/cimwin32a/win32-computershutdownevent)                   | Clase de evento<br/> Representa los eventos de apagado del equipo.<br/>                                                                                                   |
| [**Win32 \_ ComputerSystemEvent**](/previous-versions/windows/desktop/cimwin32a/win32-computersystemevent)                       | Clase de evento<br/> Representa eventos relacionados con un sistema informático.<br/>                                                                                        |
| [**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md)                           | Clase de evento<br/> Representa los eventos de cambio de dispositivo resultantes de la adición, eliminación o modificación de dispositivos en el sistema informático.<br/>               |
| [**Módulo \_ Win32LoadTrace**](/previous-versions/windows/desktop/krnlprov/win32-moduleloadtrace)                               | Clase de evento<br/> Indica que un proceso ha cargado un nuevo módulo.<br/>                                                                                      |
| [**Módulo \_ Win32Trace**](/previous-versions/windows/desktop/krnlprov/win32-moduletrace)                                       | Clase de evento<br/> Evento base para eventos de módulo.<br/>                                                                                                          |
| [**Win32 \_ ProcessStartTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstarttrace)                           | Clase de evento<br/> Indica que se ha iniciado un nuevo proceso.<br/>                                                                                              |
| [**Win32 \_ ProcessStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-processstoptrace)                             | Clase de evento<br/> Indica que un proceso ha finalizado.<br/>                                                                                               |
| [**Win32 \_ ProcessTrace**](/previous-versions/windows/desktop/krnlprov/win32-processtrace)                                     | Clase de evento<br/> Evento base para eventos de proceso.<br/>                                                                                                         |
| [**Win32 \_ SystemConfigurationChangeEvent**](win32-systemconfigurationchangeevent.md) | Clase de evento<br/> Indica que se ha actualizado la lista de dispositivos del sistema (se ha agregado o quitado un dispositivo o se ha cambiado la configuración).<br/>    |
| [**Win32 \_ SystemTrace**](/previous-versions/windows/desktop/krnlprov/win32-systemtrace)                                       | Clase de evento<br/> Clase base para todos los eventos de seguimiento del sistema, incluidos los seguimientos de módulos, procesos y subprocesos.<br/>                                                  |
| [**ThreadStartTrace de Win32 \_**](/previous-versions/windows/desktop/krnlprov/win32-threadstarttrace)                             | Clase de evento<br/> Indica que se ha iniciado un nuevo subproceso.<br/>                                                                                                    |
| [**Win32 \_ ThreadStopTrace**](/previous-versions/windows/desktop/krnlprov/win32-threadstoptrace)                               | Clase de evento<br/> Indica que un subproceso se ha detenido.<br/>                                                                                                   |
| [**Win32 \_ ThreadTrace**](/previous-versions/windows/desktop/krnlprov/win32-threadtrace)                                       | Clase de evento<br/> Clase de eventos base para eventos de subproceso.<br/>                                                                                                    |
| [**Win32 \_ VolumeChangeEvent**](win32-volumechangeevent.md)                           | Clase de evento<br/> Representa un evento de unidad asignada a la red resultante de la adición de una letra de unidad de red o una unidad montada en el sistema del equipo.<br/> |



 

## <a name="operating-system-settings"></a>Sistema operativo Configuración

El sistema operativo Configuración clases de subcategoría que representan el sistema operativo y su configuración.



| Clase                                                                                       | Descripción                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BootConfiguration de Win32 \_**](win32-bootconfiguration.md)                                 | Clase de instancia<br/> Representa la configuración de arranque de un sistema informático que ejecuta Windows.<br/>                                                                       |
| [**Equipo \_ Win32System**](win32-computersystem.md)                                       | Clase de instancia<br/> Representa un sistema informático que funciona en un Windows operativo.<br/>                                                                              |
| [**Equipo \_ Win32SystemProcessor**](win32-computersystemprocessor.md)                     | Association (clase)<br/> Relaciona un sistema informático y un procesador que se ejecuta en ese sistema.<br/>                                                                          |
| [**Win32 \_ ComputerSystemProduct**](win32-computersystemproduct.md)                         | Clase de instancia<br/> Representa un producto.<br/>                                                                                                                         |
| [**DependentService de Win32 \_**](win32-dependentservice.md)                                   | Association (clase)<br/> Relaciona dos servicios base interdependientes.<br/>                                                                                                  |
| [**LoadOrderGroup de Win32 \_**](win32-loadordergroup.md)                                       | Clase de instancia<br/> Representa un grupo de servicios del sistema que definen las dependencias de ejecución.<br/>                                                                     |
| [**\_LoadOrderGroupServiceDependencies de Win32**](win32-loadordergroupservicedependencies.md) | Clase de instancia<br/> Representa una asociación entre un servicio base y un grupo de orden de carga del que depende el servicio para empezar a ejecutarse.<br/>                         |
| [**\_LoadOrderGroupServiceMembers de Win32**](win32-loadordergroupservicemembers.md)           | Association (clase)<br/> Relaciona un grupo de pedidos de carga y un servicio base.<br/>                                                                                             |
| [**Sistema operativo \_ Win32**](win32-operatingsystem.md)                                     | Clase de instancia<br/> Representa un sistema operativo instalado en un sistema informático que ejecuta Windows.<br/>                                                                |
| [**Win32 \_ OperatingSystemQFE**](win32-operatingsystemqfe.md)                               | Association (clase)<br/> Relaciona un sistema operativo y las actualizaciones de productos aplicadas como se representa en [**\_ QuickFixEngineering de Win32.**](win32-quickfixengineering.md)<br/> |
| [**Win32 \_ OSRecoveryConfiguration**](win32-osrecoveryconfiguration.md)                     | Clase de instancia<br/> Representa los tipos de información que se recopilarán de la memoria cuando se produce un error en el sistema operativo.<br/>                                        |
| [**QuickFixEngineering de Win32 \_**](win32-quickfixengineering.md)                             | Clase de instancia<br/> Representa las actualizaciones de ingeniería Corrección rápida todo el sistema (QFE) o las actualizaciones que se han aplicado al sistema operativo actual.<br/>                         |
| [**Win32 \_ StartupCommand**](win32-startupcommand.md)                                       | Clase de instancia<br/> Representa un comando que se ejecuta automáticamente cuando un usuario inicia sesión en el sistema del equipo.<br/>                                                       |
| [**SystemBootConfiguration de Win32 \_**](win32-systembootconfiguration.md)                     | Association (clase)<br/> Relaciona un sistema informático y su configuración de arranque.<br/>                                                                                      |
| [**Win32 \_ SystemDesktop**](win32-systemdesktop.md)                                         | Association (clase)<br/> Relaciona un sistema informático y su configuración de escritorio.<br/>                                                                                   |
| [**Sistema \_ Win32Dispositivos**](win32-systemdevices.md)                                         | Association (clase)<br/> Relaciona un sistema informático y un dispositivo lógico instalado en ese sistema.<br/>                                                                   |
| [**SystemLoadOrderGroups de Win32 \_**](win32-systemloadordergroups.md)                         | Association (clase)<br/> Relaciona un sistema informático y un grupo de pedidos de carga.<br/>                                                                                          |
| [**Win32 \_ SystemNetworkConnections**](win32-systemnetworkconnections.md)                   | Association (clase)<br/> Relaciona una conexión de red y el sistema informático en el que reside.<br/>                                                                  |
| [**Sistema \_ Win32OperatingSystem**](win32-systemoperatingsystem.md)                         | Association (clase)<br/> Relaciona un sistema informático y su sistema operativo.<br/>                                                                                        |
| [**Win32 \_ SystemProcesses**](win32-systemprocesses.md)                                     | Association (clase) <br/> Relaciona un sistema informático y un proceso que se ejecuta en ese sistema.<br/>                                                                           |
| [**SystemProgramGroups de Win32 \_**](win32-systemprogramgroups.md)                             | Association (clase)<br/> Relaciona un sistema informático y un grupo de programas lógicos.<br/>                                                                                     |
| [**Win32 \_ SystemResources**](win32-systemresources.md)                                     | Association (clase)<br/> Relaciona un recurso del sistema y el sistema informático en el que reside.<br/>                                                                           |
| [**Win32 \_ SystemServices**](win32-systemservices.md)                                       | Association (clase)<br/> Relaciona un sistema informático y un programa de servicio que existe en el sistema.<br/>                                                                 |
| [**SystemSetting de Win32 \_**](win32-systemsetting.md)                                         | Association (clase)<br/> Relaciona un sistema informático y una configuración general en ese sistema.<br/>                                                                            |
| [**Win32 \_ SystemSystemDriver**](win32-systemsystemdriver.md)                               | Association (clase)<br/> Relaciona un sistema informático y un controlador del sistema que se ejecuta en ese sistema informático.<br/>                                                             |
| [**Win32 \_ SystemTimeZone**](win32-systemtimezone.md)                                       | Association (clase)<br/> Relaciona un sistema informático y una zona horaria.<br/>                                                                                                 |
| [**Sistema \_ Win32Usuario**](win32-systemusers.md)                                             | Association (clase)<br/> Relaciona un sistema informático y una cuenta de usuario en ese sistema.<br/>                                                                               |



 

## <a name="processes"></a>Procesos

La subcategoría Procesos agrupa clases que representan subprocesos y procesos del sistema.



| Clase                                                 | Descripción                                                                                                     |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**Proceso \_ win32**](win32-process.md)               | Clase de instancia<br/> Representa una secuencia de eventos en un sistema informático que ejecuta Windows.<br/>      |
| [**Win32 \_ ProcessStartup**](win32-processstartup.md) | Clase de instancia<br/> Representa la configuración de inicio de un sistema informático que ejecuta Windows.<br/> |
| [**Subproceso \_ win32**](win32-thread.md)                 | Clase de instancia<br/> Representa un subproceso de ejecución.<br/>                                          |



 

## <a name="registry"></a>Registro

La clase de la subcategoría Registry representa el contenido del Windows registro.



| Clase                                     | Descripción                                                                                               |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**Registro de \_ Win32**](win32-registry.md) | Clase de instancia<br/> Representa el registro del sistema en un sistema de equipo que ejecuta Windows.<br/> |



 

## <a name="scheduler-jobs"></a>Trabajos del Programador

La subcategoría Trabajos del programador agrupa las clases que representan la configuración del trabajo programado.



| Clase                                                | Descripción                                                                                                                                                                                                                                                           |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CurrentTime de Win32 \_**](/previous-versions/windows/desktop/wmitimepprov/win32-currenttime) | Clase abstracta<br/> Representa una instancia en el tiempo como segundos de componente, minutos, día de la semana, y así sucesivamente.<br/>                                                                                                                                        |
| [**ScheduledJob de Win32 \_**](win32-scheduledjob.md)    | Clase de instancia<br/> Representa un trabajo programado mediante el servicio Windows programación.<br/>                                                                                                                                                                   |
| [**Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime)     | Clase de instancia<br/> Representa un momento dado devuelto como [**objetos \_ LocalTime de Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) que resultan de una consulta. La **propiedad Hour** se devuelve como la hora local en un reloj de 24 horas.<br/>                                |
| [**Hora UTC de Win32 \_**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)         | Clase de instancia<br/> Representa un momento dado que se devuelve como [**objetos \_ UtcTime de Win32**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) que resultan de una consulta. La **propiedad Hour** se devuelve como la hora universal coordinada (UTC) en un reloj de 24 horas.<br/> |



 

## <a name="security"></a>Seguridad

La subcategoría Seguridad agrupa las clases que representan la configuración de seguridad del sistema.



| Clase                                                                               | Descripción                                                                                                                                                  |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccountSID de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-accountsid)                                       | Association (clase)<br/> Relaciona una instancia de cuenta de seguridad con una instancia de descriptor de seguridad.<br/>                                             |
| [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)                                                     | Clase de instancia<br/> Representa una entrada de control de acceso (ACE).<br/>                                                                               |
| [**Win32 \_ LogicalFileAccess**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileaccess)                         | Association (clase)<br/> Relaciona la configuración de seguridad de un archivo o directorio y un miembro de su lista de control de acceso discrecional (DACL).<br/> |
| [**LogicalFileAuditing de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileauditing)                     | Association (clase)<br/> Relaciona la configuración de seguridad de un archivo o directorio de un miembro de su lista de control de acceso del sistema (SACL).<br/>            |
| [**LogicalFileGroup de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilegroup)                           | Association (clase)<br/> Relaciona la configuración de seguridad de un archivo o directorio y su grupo.<br/>                                                  |
| [**Win32 \_ LogicalFileOwner**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfileowner)                           | Association (clase)<br/> Relaciona la configuración de seguridad de un archivo o directorio y su propietario.<br/>                                                  |
| [**Win32 \_ LogicalFileSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)       | Clase de instancia<br/> Representa la configuración de seguridad de un archivo lógico.<br/>                                                                        |
| [**Win32 \_ LogicalShareAccess**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalshareaccess)                       | Association (clase)<br/> Relaciona la configuración de seguridad de un recurso compartido y un miembro de su DACL.<br/>                                                 |
| [**LogicalShareAuditing de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalshareauditing)                   | Association (clase)<br/> Relaciona la configuración de seguridad de un recurso compartido y un miembro de su SACL.<br/>                                                 |
| [**Win32 \_ LogicalShareSecuritySetting**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting)     | Clase de instancia<br/> Representa la configuración de seguridad de un archivo lógico.<br/>                                                                        |
| [**Privilegios de \_ Win32Status**](win32-privilegesstatus.md)                           | Clase de instancia<br/> Representa información sobre los privilegios necesarios para completar una operación.<br/>                                          |
| [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)                       | Clase de instancia<br/> Representa una representación estructural de un [**DESCRIPTOR DE \_ SEGURIDAD**](/windows/desktop/api/winnt/ns-winnt-security_descriptor).<br/>                   |
| [**Seguridad de \_ Win32Setting**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysetting)                             | Clase de instancia<br/> Representa la configuración de seguridad de un elemento administrado.<br/>                                                                     |
| [**Win32 \_ SecuritySettingAccess**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingaccess)                 | Clase de instancia<br/> Representa los derechos concedidos y denegados a un administrador de confianza para un objeto determinado.<br/>                                               |
| [**Seguridad de \_ Win32SettingAuditing**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingauditing)             | Clase de instancia<br/> Representa la auditoría de un administrador de confianza determinado en un objeto determinado.<br/>                                                          |
| [**SecuritySettingGroup de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettinggroup)                   | Association (clase)<br/> Relaciona la seguridad de un objeto y su grupo.<br/>                                                                     |
| [**SecuritySettingOfLogicalFile de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingoflogicalfile)   | Clase de instancia<br/> Representa la configuración de seguridad de un objeto de archivo o directorio.<br/>                                                             |
| [**Seguridad de \_ Win32SettingOfLogicalShare**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingoflogicalshare) | Clase de instancia<br/> Representa la configuración de seguridad de un objeto compartido.<br/>                                                                        |
| [**Win32 \_ SecuritySettingOfObject**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingofobject)             | Association (clase)<br/> Relaciona un objeto con su configuración de seguridad.<br/>                                                                          |
| [**Win32 \_ SecuritySettingOwner**](/previous-versions/windows/desktop/secrcw32prov/win32-securitysettingowner)                   | Association (clase)<br/> Relaciona la configuración de seguridad de un objeto y su propietario.<br/>                                                            |
| [**SID de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-sid)                                                     | Clase de instancia<br/> Representa un SID arbitrario.<br/>                                                                                            |
| [**Administrador de \_ Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)                                             | Clase de instancia<br/> Representa un administrador de confianza.<br/>                                                                                                   |



 

## <a name="services"></a>Servicios

La subcategoría Services agrupa las clases que representan servicios y servicios base.



| Clase                                           | Descripción                                                                                                                                             |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ BaseService**](win32-baseservice.md) | Clase de instancia<br/> Representa objetos ejecutables que se instalan en una base de datos del Registro mantenida por el Administrador de control de servicios.<br/> |
| [**Servicio \_ Win32**](win32-service.md)         | Clase de instancia<br/> Representa un servicio en un sistema informático que ejecuta Windows.<br/>                                                         |



 

## <a name="shares"></a>Recursos compartidos

La subcategoría Recursos compartidos agrupa clases que representan detalles de recursos compartidos, como impresoras y carpetas.



| Clase                                                       | Descripción                                                                                                                                                                                          |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ DFSNode**](/previous-versions/windows/desktop/wmipdfs/win32-dfsnode)                     | Association (clase)<br/> Representa un nodo raíz o de unión de un sistema de archivos distribuido basado en dominio o independiente (DFS).<br/>                                                           |
| [**Win32 \_ DFSNodeTarget**](/previous-versions/windows/desktop/wmipdfs/win32-dfsnodetarget)         | Association (clase)<br/> Representa la relación de un nodo DFS con uno de sus destinos.<br/>                                                                                             |
| [**Win32 \_ DFSTarget**](/previous-versions/windows/desktop/wmipdfs/win32-dfstarget)                 | Association (clase)<br/> Representa el destino de un nodo DFS.<br/>                                                                                                                         |
| [**Win32 \_ ServerConnection**](/previous-versions/windows/desktop/wmipsess/win32-serverconnection)   | Clase de instancia<br/> Representa las conexiones realizadas desde un equipo remoto a un recurso compartido en el equipo local.<br/>                                                              |
| [**Win32 \_ ServerSession**](/previous-versions/windows/desktop/wmipsess/win32-serversession)         | Clase de instancia<br/> Representa las sesiones que los usuarios de un equipo remoto establecen con el equipo local.<br/>                                                             |
| [**Win32 \_ ConnectionShare**](/previous-versions/windows/desktop/wmipsess/win32-connectionshare)     | Association (clase)<br/> Relaciona un recurso compartido en el equipo y la conexión realizada al recurso compartido.<br/>                                                                    |
| [**PrinterShare de Win32 \_**](win32-printershare.md)           | Association (clase)<br/> Relaciona una impresora local y el recurso compartido que la representa a medida que se ve a través de una red.<br/>                                                                     |
| [**SessionConnection de Win32 \_**](/previous-versions/windows/desktop/wmipsess/win32-sessionconnection) | Association (clase)<br/> Representa una asociación entre una sesión establecida con el servidor local por un usuario en un equipo remoto y las conexiones que dependen de la sesión.<br/> |
| [**Win32 \_ SessionProcess**](win32-sessionprocess.md)       | Association (clase)<br/> Representa una asociación entre una sesión de inicio de sesión y los procesos asociados a esa sesión.<br/>                                                            |
| [**ShareToDirectory de Win32 \_**](win32-sharetodirectory.md)   | Association (clase)<br/> Relaciona un recurso compartido en el sistema del equipo y el directorio al que está asignado.<br/>                                                                    |
| [**Recurso compartido de \_ Win32**](win32-share.md)                         | Clase de instancia<br/> Representa un recurso compartido en un sistema informático que ejecuta Windows.<br/>                                                                                              |



 

## <a name="start-menu"></a>Menú Inicio

La subcategoría Menú Inicio agrupa las clases que representan grupos de programas.



| Clase                                                                                   | Descripción                                                                                                                                                              |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**LogicalProgramGroup de Win32 \_**](win32-logicalprogramgroup.md)                         | Clase de instancia<br/> Representa un grupo de programas en un sistema informático que ejecuta Windows.<br/>                                                                    |
| [**LogicalProgramGroupDirectory de Win32 \_**](win32-logicalprogramgroupdirectory.md)       | Association (clase)<br/> Relaciona grupos de programas lógicos (agrupaciones en el menú Inicio) y los directorios de archivos en los que se almacenan.<br/>                 |
| [**LogicalProgramGroupItem de Win32 \_**](win32-logicalprogramgroupitem.md)                 | Clase de instancia<br/> Representa un elemento contenido por una instancia de **\_ ProgramGroup de Win32,** que no es en sí otra **instancia de \_ ProgramGroup de Win32.**<br/> |
| [**LogicalProgramGroupItemDataFile de Win32 \_**](win32-logicalprogramgroupitemdatafile.md) | Association (clase)<br/> Relaciona los elementos de grupo de programas del menú Inicio y los archivos en los que se almacenan.<br/>                                       |
| [**ProgramGroupContents de Win32 \_**](win32-programgroupcontents.md)                       | Association (clase)<br/> Relaciona un orden de grupo de programas y un grupo de programas individual o un elemento contenido en él.<br/>                                           |
| [**ProgramGroupOrItem de Win32 \_**](win32-programgrouporitem.md)                           | Clase de instancia<br/> Representa una agrupación lógica de programas en el menú **Iniciar** \| **programas del** usuario.<br/>                                               |



 

## <a name="storage"></a>Almacenamiento

La subcategoría Users agrupa las clases que representan información de almacenamiento.



| Clase                                                                   | Descripción                                                                                                                                  |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ShadowBy**](/previous-versions/windows/desktop/vsswmi/win32-shadowby)                               | Association (clase)<br/> Representa la asociación entre una instantánea y el proveedor que crea la instantánea.<br/>      |
| [**ShadowContext de Win32 \_**](/previous-versions/windows/desktop/vsswmi/win32-shadowcontext)                     | Association (clase)<br/> Especifica cómo se va a crear, consultar o eliminar una instantánea.<br/>                                   |
| [**ShadowCopy de Win32 \_**](/previous-versions/windows/desktop/legacy/aa394428(v=vs.85))                           | Clase de instancia<br/> Representa una copia duplicada del volumen original en un momento anterior.<br/>                                  |
| [**Win32 \_ ShadowDiffVolumeSupport**](/previous-versions/windows/desktop/vsswmi/win32-shadowdiffvolumesupport) | Association (clase)<br/> Representa una asociación entre un proveedor de instantáneas y un volumen de almacenamiento.<br/>                       |
| [**Win32 \_ ShadowFor**](/previous-versions/windows/desktop/vsswmi/win32-shadowfor)                             | Association (clase)<br/> Representa una asociación entre una instantánea y el volumen para el que se crea la instantánea.<br/> |
| [**Win32 \_ ShadowOn**](/previous-versions/windows/desktop/vsswmi/win32-shadowon)                               | Association (clase)<br/> Representa una asociación entre una instantánea y donde se escriben los datos diferenciales.<br/>          |
| [**ShadowProvider de Win32 \_**](/previous-versions/windows/desktop/vsswmi/win32-shadowprovider)                   | Association (clase)<br/> Representa un componente que crea y representa instantáneas de volumen.<br/>                             |
| [**Win32 \_ ShadowStorage**](/previous-versions/windows/desktop/legacy/aa394433(v=vs.85))                     | Association (clase)<br/> Representa una asociación entre una instantánea y donde se escriben los datos diferenciales.<br/>          |
| [**Win32 \_ ShadowVolumeSupport**](/previous-versions/windows/desktop/vsswmi/win32-shadowvolumesupport)         | Association (clase)<br/> Representa una asociación entre un proveedor de instantáneas con un volumen admitido.<br/>                    |
| [**Volumen \_ win32**](/previous-versions/windows/desktop/legacy/aa394515(v=vs.85))                                   | Clase de instancia<br/> Representa un área de almacenamiento en un disco duro.<br/>                                                           |
| [**Win32 \_ VolumeUserQuota**](/previous-versions/windows/desktop/vdswmi/win32-volumeuserquota)                 | Association (clase)<br/> Representa un volumen para la configuración de cuota por volumen.<br/>                                                |



 

## <a name="users"></a>Usuarios

La subcategoría Usuarios agrupa clases que representan la información de la cuenta de usuario, como los detalles de pertenencia a grupos.



| Clase                                                                 | Descripción                                                                                                                                      |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Cuenta \_ win32**](win32-account.md)                               | Clase de instancia<br/> Representa información sobre las cuentas de usuario y las cuentas de grupo conocidas por el sistema informático que ejecuta Windows.<br/> |
| [**Grupo \_ Win32**](win32-group.md)                                   | Clase de instancia<br/> Representa datos sobre una cuenta de grupo.<br/>                                                                      |
| [**GroupInDomain de Win32 \_**](/previous-versions/windows/desktop/cimwin32a/win32-groupindomain)                   | Association (clase)<br/> Identifica las cuentas de grupo asociadas a un Windows NT.<br/>                                       |
| [**GroupUser de Win32 \_**](win32-groupuser.md)                           | Association (clase)<br/> Relaciona un grupo y una cuenta que es miembro de ese grupo.<br/>                                           |
| [**LogonSession de Win32 \_**](win32-logonsession.md)                     | Clase de instancia<br/> Describe la sesión de inicio de sesión o las sesiones asociadas a un usuario que ha iniciado sesión en Windows.<br/>                        |
| [**LogonSessionMappedDisk de Win32 \_**](/windows/desktop/CIMWin32Prov/win32-logonsessionmappeddisk) | Clase de instancia<br/> Representa los discos lógicos asignados asociados a la sesión.<br/>                                            |
| [**Win32 \_ NetworkLoginProfile**](win32-networkloginprofile.md)       | Clase de instancia<br/> Representa la información de inicio de sesión de red de un usuario específico en un sistema informático que ejecuta Windows.<br/>           |
| [**SystemAccount de Win32 \_**](win32-systemaccount.md)                   | Clase de instancia<br/> Representa una cuenta del sistema.<br/>                                                                                |
| [**UserAccount de Win32 \_**](win32-useraccount.md)                       | Clase de instancia<br/> Representa información sobre una cuenta de usuario en un sistema informático que ejecuta Windows.<br/>                           |
| [**UserInDomain de Win32 \_**](/previous-versions/windows/desktop/cimwin32a/win32-userindomain)                     | Association (clase)<br/> Relaciona una cuenta de usuario y un dominio Windows NT.<br/>                                                          |



 

## <a name="windows-event-log"></a>Registro de sucesos de Windows

La subcategoría Windows registro de eventos agrupa clases que representan eventos, entradas del registro de eventos, valores de configuración del registro de eventos, entre otras.



| Clase                                                         | Descripción                                                                                                                                                                   |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))         | Clase de instancia<br/> Representa los datos almacenados en un Windows de registro de eventos.<br/>                                                                                      |
| [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent)                 | Clase de instancia<br/> Representa Windows eventos.<br/>                                                                                                               |
| [**Win32 \_ NTLogEventComputer**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventcomputer) | Association (clase)<br/> Relaciona las instancias de [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) y [**Win32 \_ ComputerSystem**](win32-computersystem.md).<br/>         |
| [**Win32 \_ NTLogEventLog**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventlog)           | Association (clase)<br/> Relaciona instancias de las clases [**\_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) y [**Win32 \_ NTEventlogFile de Win32.**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85))<br/> |
| [**Win32 \_ NTLogEventUser**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogeventuser)         | Association (clase)<br/> Relaciona las instancias de [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent) y [**Win32 \_ UserAccount**](win32-useraccount.md).<br/>               |



 

## <a name="windows-product-activation"></a>Windows Activación del producto

Windows Activación de productos (WPA) es una tecnología antianficia para reducir la copia ocasional de software.



| Clase                                                                                                               | Descripción                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ ComputerSystemWindowsProductActivationSetting**](/previous-versions/windows/desktop/licwmiprov/win32-computersystemwindowsproductactivationsetting) | Association (clase)<br/> Relaciona las instancias de [**Win32 \_ ComputerSystem**](win32-computersystem.md) y [**Win32 \_ WindowsProductActivation**](/previous-versions/windows/desktop/legacy/aa394520(v=vs.85)).<br/> |
| [**Win32 \_ Proxy**](/previous-versions/windows/desktop/legacy/aa394389(v=vs.85))                                                                                 | Clase de instancia<br/> Contiene propiedades y métodos para consultar y configurar una conexión a Internet relacionada con WPA.<br/>                                                                |
| [**WindowsProductActivation de Win32 \_**](/previous-versions/windows/desktop/legacy/aa394520(v=vs.85))                                           | Clase de instancia<br/> Contiene propiedades y métodos relacionados con WPA.<br/>                                                                                                              |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clases Win32](/previous-versions//aa394084(v=vs.85))
</dt> </dl>

 

