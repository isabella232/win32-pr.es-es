---
description: El sistema operativo Windows incluye un conjunto de VSS Writer que son responsables de enumerar los datos que diversas características de Windows requieren. Estos se conocen como escritores &\# 0034;in-box&\# 0034; writers.
ms.assetid: e20a303d-9440-42be-b383-85f6fad89157
title: Instancias de VSS Writer incluidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e34591cb046a8cc702d32452c159e5b8877f2e66603cbd1b048a0841a04e3bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767805"
---
# <a name="in-box-vss-writers"></a>Instancias de VSS Writer incluidas

El sistema operativo Windows incluye un conjunto de VSS Writer que son responsables de enumerar los datos que diversas características de Windows requieren. Estos se conocen como escritores "en la caja".

> [!Note]  
> MSDE in-box writer no está disponible en Windows Vista, Windows Server 2008 y versiones posteriores. En su lugar, SQL Writer debe usarse para realizar una copia de seguridad SQL Server bases de datos. Solo SQL Server 2005 SP2 y versiones posteriores se admiten en Windows Vista, Windows Server 2008 y versiones posteriores.

 

-   [Active Directory Domain Services (NTDS) VSS Writer](#active-directory-domain-services-ntds-vss-writer)
-   [Servicios de federación de Active Directory (AD FS) Writer](#active-directory-federation-services-writer)
-   [Active Directory Lightweight Directory Services (LDS) VSS Writer](#active-directory-lightweight-directory-services-lds-vss-writer)
-   [Active Directory Rights Management Services (AD RMS) Writer](#active-directory-rights-management-services-ad-rms-writer)
-   [Escritor Recuperación del sistema automático (ASR)](#automated-system-recovery-asr-writer)
-   [escritor Servicio de transferencia inteligente en segundo plano (BITS)](#background-intelligent-transfer-service-bits-writer)
-   [Escritor de entidad de certificación](#certificate-authority-writer)
-   [Escritor de servicios de clúster](#cluster-service-writer)
-   [Volumen compartido de clúster (CSV) VSS Writer](#cluster-shared-volume-csv-vss-writer)
-   [Escritor de base de datos de registro de clases COM+](#com-class-registration-database-writer)
-   [Escritor de desduplicación de datos](#data-deduplication-writer)
-   [Sistema de replicación de archivos distribuido (DFSR)](#distributed-file-system-replication-dfsr)
-   [Escritor del Protocolo de configuración dinámica de host (DHCP)](#dynamic-host-configuration-protocol-dhcp-writer)
-   [Servicio de replicación de archivos (FRS)](#file-replication-service-frs)
-   [Escritor de Resource Manager servidor de archivos (FSRM)](#file-server-resource-manager-fsrm-writer)
-   [Escritor de Hyper-V](#hyper-v-writer)
-   [Escritor de configuración de IIS](#iis-configuration-writer)
-   [Escritor de metabase de IIS](#iis-metabase-writer)
-   [escritor Microsoft Message Queuing (MSMQ)](#microsoft-message-queuing-msmq-writer)
-   [Escritor del servicio MSSearch](#mssearch-service-writer)
-   [NPS VSS Writer](#nps-vss-writer)
-   [Escritor de contadores de rendimiento](#performance-counters-writer)
-   [Escritor del Registro](#registry-writer)
-   [vsS Writer de puerta de enlace de Servicios de Escritorio remoto (Terminal Services)](#remote-desktop-services-terminal-services-gateway-vss-writer)
-   [Servicios de Escritorio remoto (Terminal Services) Licensing VSS Writer](#remote-desktop-services-terminal-services-licensing-vss-writer)
-   [Escritor de optimización de instantáneas](#shadow-copy-optimization-writer)
-   [Sincronización del escritor de servicios compartidos](#sync-share-service-writer)
-   [System Writer](#system-writer)
-   [Programador de tareas Writer](#task-scheduler-writer)
-   [Escritor del almacén de metadatos de VSS](#vss-metadata-store-writer)
-   [Windows Escritor de Servicios de implementación (WDS)](#windows-deployment-services-wds-writer)
-   [escritor Windows Internal Database (WID)](#windows-internal-database-wid-writer)
-   [Windows Escritor del Servicio de nombres de Internet (WINS)](#windows-internet-name-service-wins-writer)
-   [Escritor WMI](#wmi-writer)

## <a name="active-directory-domain-services-ntds-vss-writer"></a>Active Directory Domain Services (NTDS) VSS Writer

Este escritor notifica el archivo de base de datos NTDS (ntds.dit) y los archivos de registro asociados. Estos archivos son necesarios para restaurar el Active Directory correctamente.

Solo hay un archivo ntds.dit por controlador de dominio y se notifica en los metadatos del escritor como en el ejemplo siguiente:

``` syntax
    <DATABASE_FILES path="C:\Windows\NTDS" 
                     filespec="ntds.dit" 
                     filespecBackupType="3855"/>
```

Este es un ejemplo que muestra cómo enumerar componentes en los metadatos del escritor:

``` syntax
    <BACKUP_LOCATIONS>
        <DATABASE logicalPath="C:_Windows_NTDS" 
                     componentName="ntds" 
                     caption="" restoreMetadata="no" 
                     notifyOnBackupComplete="no" 
                     selectable="no" 
                     selectableForRestore="no" 
                     componentFlags="3">
        <DATABASE_FILES path="C:\Windows\NTDS" 
                     filespec="ntds.dit" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Windows\NTDS" 
                     filespec="edb*.log" 
                     filespecBackupType="3855"/> 
        <DATABASE_LOGFILES path="C:\Windows\NTDS" 
                     filespec="edb.chk" 
                     filespecBackupType="3855"/>
        </DATABASE>
    </BACKUP_LOCATIONS>
```

En el momento de la copia de seguridad, el escritor establece la hora de expiración de la copia de seguridad en los metadatos de copia de seguridad del escritor. Los solicitantes deben recuperar estos metadatos mediante [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) para determinar si la base de datos ha expirado. Las bases de datos expiradas no se pueden restaurar.

Si el equipo que contiene la base de datos NTDS es un controlador de dominio, la aplicación de copia de seguridad siempre debe realizar una copia de seguridad del estado del sistema en todos los volúmenes que contengan información de estado del sistema crítica. En el momento de la restauración, la aplicación debe reiniciar primero el equipo en Modo de restauración de servicios de directorio después realizar una restauración del estado del sistema.

La cadena de nombre del escritor para este escritor es "NTDS".

El identificador de escritor para este escritor es B2014C9E-8711-4C5C-A5A9-3CF384484757.

## <a name="active-directory-federation-services-writer"></a>Servicios de federación de Active Directory (AD FS) Writer

Este sistema de escritura informa de Servicios de federación de Active Directory (AD FS) archivos de datos de Servicios de federación de Active Directory (AD FS) (ADFS).

**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** No se admite este sistema de escritura.

La cadena de nombre del escritor para este escritor es "ADFS VSS Writer".

El identificador de escritor para este escritor es 772C45F8-AE01-4F94-940C-94961864ACAD.

## <a name="active-directory-lightweight-directory-services-lds-vss-writer"></a>Active Directory Lightweight Directory Services (LDS) VSS Writer

Este escritor notifica el archivo de base de datos ADAM (adamntds.dit) y los archivos de registro asociados para cada instancia en %archivos de programa% datos de la instancia N de Microsoft ADAM, donde N es el número de instancia \\ \\ de \\ ADAM.  Estos archivos de registro de base de datos son necesarios para restaurar instancias de ADAM.

**Windows XP:** No se admite este sistema de escritura.

Este es un ejemplo que muestra cómo enumerar componentes en los metadatos del escritor:

``` syntax
    <BACKUP_LOCATIONS>
        <DATABASE logicalPath="C:_Program Files_Microsoft ADAM_instance1_data" 
                     componentName="adamntds" 
                     caption="" 
                     restoreMetadata="no" 
                     notifyOnBackupComplete="no" 
                     selectable="no" 
                     selectableForRestore="no" 
                     componentFlags="3">
        <DATABASE_FILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="adamntds.dit" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="edb*.log" 
                     filespecBackupType="3855"/>
        <DATABASE_LOGFILES path="C:\Program Files\Microsoft ADAM\instance1\data" 
                     filespec="edb.chk" 
                     filespecBackupType="3855"/>
        </DATABASE>
    </BACKUP_LOCATIONS>
```

En el momento de la copia de seguridad, el escritor establece la hora de expiración de la copia de seguridad en los metadatos de copia de seguridad. Las aplicaciones de copia de seguridad deben recuperar estos metadatos mediante el método [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) para determinar si la base de datos ha expirado. Las bases de datos expiradas no se pueden restaurar.

La cadena de nombre del escritor para este escritor es "ADAM (instancia *N*) Writer", donde *N* es el número de instancia de ADAM, por ejemplo, "ADAM (instance1) Writer", "ADAM (instance2) Writer", y así sucesivamente.

El identificador de escritor para este escritor es DD846AAAA-A1B6-42A8-AAF8-03DCB6114BFD. Este identificador de escritor es el mismo para todas las instancias.

## <a name="active-directory-rights-management-services-ad-rms-writer"></a>Active Directory Rights Management Services (AD RMS) Writer

Este escritor notifica los archivos de Active Directory Rights Management Service (AD RMS).

**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** No se admite este sistema de escritura.

La cadena de nombre del escritor para este escritor es "AD RMS Writer".

El identificador de escritor para este escritor es 886C43B1-D455-4428-A37F-4D6B9E43F50F.

## <a name="automated-system-recovery-asr-writer"></a>Escritor de Recuperación del sistema automatizado (ASR)

Asr Writer almacena la configuración de los discos en el sistema. Este escritor informa de la base de datos de configuración de arranque (BCD) y también es responsable de desmontar el subárbol del Registro que representa el BCD durante la creación de instantáneas. AsR Writer debe incluirse en las copias de seguridad necesarias para la recuperación sin sistema. Para obtener más información sobre ASR, vea [Using VSS Automated Recuperación del sistema for Disaster Recovery](using-vss-automated-system-recovery-for-disaster-recovery.md).

**Windows Server 2003 y Windows XP:** No se admite este sistema de escritura.

La cadena de nombre del escritor para este escritor es "ASR Writer".

El identificador del escritor de ASR es BE000CBE-11FE-4426-9C58-531AA6355FC4.

## <a name="background-intelligent-transfer-service-bits-writer"></a>escritor Servicio de transferencia inteligente en segundo plano (BITS)

El sistema de escritura de BITS usa la clave del Registro **FilesNotToBackup** para excluir archivos de la carpeta de caché de BITS. La ubicación de caché predeterminada es %AllUsersProfile% \\ Microsoft \\ Network Downloader \\ \\ Cache.

**Windows Server 2003 y Windows XP:** No se admite este sistema de escritura.

Además, el sistema de escritura de BITS excluye los siguientes archivos de copia de seguridad: los archivos de estado bits (qmgr0.dat y qmgr1.dat), el archivo de registro de depuración de BITS y los archivos bits descargados parcialmente.

Si el archivo de destino de descarga de BITS es un archivo SMB, la cuenta de cliente debe tener una relación de confianza con el servidor o, de lo contrario, se pueden producir errores en las copias de seguridad.

La cadena de nombre del escritor para este escritor es "ESCRITOR DE BITS".

El identificador del escritor de BITS es 4969D978-BE47-48B0-B100-F328F07AC1E0.

## <a name="certificate-authority-writer"></a>Escritor de entidad de certificación

Este escritor es responsable de enumerar los archivos de datos del servidor de certificados.

La cadena de nombre del escritor para este escritor es "Entidad de certificación".

**Windows XP:** La cadena de nombre del escritor para este escritor es "Escritor de servidor de certificados".

El identificador del escritor es 6F5B15B5-DA24-4D88-B737-63063E3A1F86.

## <a name="cluster-service-writer"></a>Escritor de servicios de clúster

Cluster Service VSS Writer se documenta en la documentación de [Cluster Service](/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-failover-cluster-configuration-using-vss) API.

**Windows Vista, Windows Server 2003 y Windows XP:** Este escritor no se admite hasta Windows Vista con Service Pack 1 (SP1) y Windows Server 2008.

## <a name="cluster-shared-volume-csv-vss-writer"></a>Volumen compartido de clúster (CSV) VSS Writer

Este sistema de escritura informa de Volumen compartido de clúster archivos de datos (CSV). Este sistema de escritura es un sistema de escritura integrado para las Windows del sistema operativo server. no se incluye en Windows cliente.

**Windows Server 2008 R2, Windows Server 2008 y Windows Server 2003:** No se admite este sistema de escritura.

La cadena de nombre del escritor para este escritor es "Volumen compartido de clúster VSS Writer".

El identificador del escritor es 1072AE1C-E5A7-4EA1-9E4A-6F7964656570.

## <a name="com-class-registration-database-writer"></a>Escritor de base de datos de registro de clases COM+

Este escritor es responsable del contenido del directorio %SystemRoot% \\ Registration. El catálogo de COM+ es un archivo en %SystemRoot% Registration con un nombre que sigue el patrón \\ R *xxxxxxxxxxxx*.clb, donde *xxxxxxxxxxxx* es un número hexadecimal de 12 dígitos. Puede haber varios archivos de este tipo si las aplicaciones COM+ se han configurado en el equipo. El archivo que contiene el catálogo actual de COM+ es el archivo con el valor más grande de *xxxxxxxxxxxx.*

**Windows Server 2003 y Windows XP:** No se admite este sistema de escritura.

La base de datos de registro de clases COM+ depende de una clave del Registro de la que se va a realizar una copia de seguridad y, por tanto, es necesario realizar una copia de seguridad y restaurarla junto con el registro.

Para restaurar la base de datos de registro de COM+, una aplicación de copia de seguridad (solicitante) debe llamar al [**método ICOMAdminCatalog::RestoreREGDB.**](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb)

La cadena de nombre del escritor para este escritor es "ESCRITOR DE REGDB DE COM+".

El identificador de escritor para el escritor de base de datos de registro de clases COM+ es 542DA469-D3E1-473C-9F4F-7847F01FC64F.

## <a name="data-deduplication-writer"></a>Escritor de desduplicación de datos

VsS Writer de desduplicación de datos se documenta en la documentación [de Data Deduplication](/previous-versions/windows/desktop/dedup/backup-and-restore-of-data-deduplication-enabled-volumes) API. Este sistema de escritura es un sistema de escritura integrado para las Windows del sistema operativo server. no se incluye en Windows cliente.

**Windows Server 2008 R2, Windows Server 2008 y Windows Server 2003:** No se admite este sistema de escritura.

## <a name="distributed-file-system-replication-dfsr"></a>Sistema de replicación de archivos distribuido (DFSR)

El componente siguiente incluye vss writer: [Sistema de archivos distribuido Replication (DFSR)](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders)

**Windows Vista, Windows Server 2003 y Windows XP:** Este sistema de escritura no se admite hasta Windows Vista con SP1 y Windows Server 2008.

## <a name="dynamic-host-configuration-protocol-dhcp-writer"></a>Escritor del Protocolo de configuración dinámica de host (DHCP)

Este escritor es responsable de enumerar los archivos necesarios para el rol de servidor DHCP. Este sistema de escritura es un sistema de escritura integrado para las Windows del sistema operativo server. no se incluye en Windows cliente.

La cadena de nombre del escritor para este escritor es "Dhcp Jet Writer".

El identificador de escritor para este escritor es BE9AC81E-3619-421F-920F-4C6FEA9E93AD.

## <a name="file-replication-service-frs"></a>Servicio de replicación de archivos (FRS)

El escritor del servicio de replicación de archivos se documenta en Copia de seguridad y restauración de FRS-Replicated [carpeta SYSVOL](backing-up-and-restoring-an-frs-replicated-sysvol-folder.md).

**Windows Vista, Windows Server 2003 y Windows XP:** Este sistema de escritura no se admite hasta Windows Vista con SP1 y Windows Server 2008.

## <a name="file-server-resource-manager-fsrm-writer"></a>Escritor de Resource Manager servidor de archivos (FSRM)

Este sistema de escritura enumera los archivos de configuración de FSRM que se usan para la copia de seguridad de estado del sistema. Durante las operaciones de restauración, evita cambios en la configuración de FSRM y detiene temporalmente el cumplimiento de cuotas y pantallas de archivos. Una vez completada la restauración, el sistema de escritura actualiza FSRM con la configuración que se restauró. Este sistema de escritura solo está presente cuando FSRM (parte del rol Servicios de archivos) está instalado y en ejecución. Este sistema de escritura es un sistema de escritura integrado para las Windows del sistema operativo server. no se incluye en Windows cliente.

**Windows Server 2003:** Este sistema de escritura no se admite hasta Windows Server 2003 R2.

La cadena de nombre del escritor para este escritor es "FSRM Writer".

El identificador de escritor para este escritor es 12CE4370-5BB7-4C58-A76A-E5D5097E3674.

## <a name="hyper-v-writer"></a>Escritor de Hyper-V

VsS Writer de Hyper-V se documenta en la documentación de la API [de Hyper-V.](/previous-versions/windows/desktop/virtual/backing-up-and-restoring-virtual-machines) Este sistema de escritura es un sistema de escritura integrado para las Windows del sistema operativo server. no se incluye en Windows cliente.

**Windows Server 2003:** Este sistema de escritura no se admite hasta Windows Server 2008.

## <a name="iis-configuration-writer"></a>Escritor de configuración de IIS

El escritor de configuración de IIS es responsable de enumerar los archivos de configuración de IIS.

**Windows Vista, Windows Server 2003 y Windows XP:** Este sistema de escritura no se admite hasta Windows Vista con SP1 y Windows Server 2008. Los solicitantes deben realizar una copia de seguridad de los archivos de configuración de IIS, incluido el archivo de machine.config .NET FX o el ASP.NET raíz web.config archivo.

Este sistema de escritura no realiza una copia de seguridad del archivo .NET FX machine.config o del archivo ASP.NET raíz web.config porque system writer enumera estos archivos.

Este sistema de escritura hace una copia de seguridad de todos los archivos que se encuentran en los directorios de configuración %windir% \\ system32 \\ inetsrv y \\ \\ %windir% \\ system32 \\ inetsrv, \\ excepto los archivos enumerados por System Writer.

El identificador de escritor para el escritor de configuración de IIS es 2A40FD15-DFCA-4aa8-A654-1F8C654603F6.

## <a name="iis-metabase-writer"></a>Escritor de metabase de IIS

El escritor de metabases de Internet Information Server (IIS) es responsable de enumerar el archivo de metabase de IIS.

**Windows Vista, Windows Server 2003 y Windows XP:** Este sistema de escritura no se admite hasta Windows Vista con SP1 y Windows Server 2008. Los solicitantes deben realizar una copia de seguridad del archivo de metabase de IIS.

El identificador de escritor del sistema de escritura de la metabase de IIS es 59B1f0CF-90EF-465F-9609-6CA8B2938366.

## <a name="microsoft-message-queuing-msmq-writer"></a>escritor Microsoft Message Queuing (MSMQ)

Este sistema de escritura informa Microsoft Message Queuing archivos de datos de Microsoft Message Queuing (MSMQ).

**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** No se admite este sistema de escritura.

La cadena de nombre del escritor para este escritor es "MSMQ Writer (*SvcName*)", donde *SvcName* es el nombre del servicio MSMQ al que está asociado el escritor. Para la instalación predeterminada, el nombre del servicio es "MSMQ". En el caso de las instancias en clúster, el nombre del servicio es MSMQ$*ResourceName,* donde *ResourceName* es el nombre del recurso MSMQ en clúster.

El identificador de escritor para este escritor es 7E47B561-971A-46E6-96B9-696EEAA53B2A.

## <a name="mssearch-service-writer"></a>Escritor del servicio MSSearch

Este sistema de escritura existe para eliminar archivos de índice de búsqueda de instantáneas después de la creación. Esto se hace para minimizar el impacto de la E/S de copia en escritura durante la E/S normal en estos archivos en el volumen de instantáneas.

**Windows Server 2003:** No se admite este sistema de escritura.

Para instalar este sistema de escritura en el servidor, debe instalar el rol Servicios de archivos y habilitar Windows Search Service.

La cadena de nombre del escritor para este escritor es "MSSearch Service Writer".

El identificador del escritor del servicio MSSearch es CD3F2362-8BEF-46C7-9181-D62844CDC0B2.

## <a name="nps-vss-writer"></a>NPS VSS Writer

El sistema de escritura de NPS es responsable de enumerar los archivos de configuración del servidor de directivas de red (NPS) para los servidores que tienen instalados la directiva de red y Access Services rol.

**Windows Vista, Windows Server 2003 y Windows XP:** Este sistema de escritura no se admite hasta Windows Vista con SP1 y Windows Server 2008.

La cadena de nombre del escritor para este escritor es "NPS VSS Writer".

El identificador de escritor para NPS VSS Writer es 0x35E81631-13E1-48DB-97FC-D5BC721BB18A.

## <a name="performance-counters-writer"></a>Escritor de contadores de rendimiento

Este escritor informa de los archivos de configuración del contador de rendimiento. Estos archivos solo se modifican durante la instalación de la aplicación y deben realizarse copias de seguridad y restaurarse durante las copias de seguridad y restauraciones del estado del sistema.

**Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** No se admite este sistema de escritura. Los solicitantes deben realizar una copia de seguridad de estos archivos manualmente. (Vea [Copia de seguridad y restauración del estado del sistema).](locating-additional-system-files.md)

La cadena de nombre del escritor para este escritor es "Escritor de contadores de rendimiento".

El identificador de escritor para el escritor de contadores de rendimiento es 0BADA1DE-01A9-4625-8278-69E735F39DDD2.

## <a name="registry-writer"></a>Escritor del Registro

El sistema de escritura del registro informa de Windows archivos del Registro para habilitar copias de seguridad y restauraciones locales del registro. No informa de los subárboles de usuario.

**Windows Server 2003:** En Windows Server 2003, este escritor usa un archivo de repositorio intermedio (a veces denominado "archivo de almacenamiento") para almacenar datos del Registro. (Vea [Operaciones de copia de seguridad y restauración del Registro en VSS).](registry-backup-and-restore-operations-under-vss.md)

**Windows XP:** No se admite este sistema de escritura. (Vea [Operaciones de copia de seguridad y restauración del Registro en VSS).](registry-backup-and-restore-operations-under-vss.md)

La cadena de nombre del escritor para este escritor es "Escritor del Registro".

El identificador del escritor del registro es AFBAB4A2-367D-4D15-A586-71DBB18F8485.

## <a name="remote-desktop-services-terminal-services-gateway-vss-writer"></a>vsS Writer de puerta de enlace de Servicios de Escritorio remoto (Terminal Services)

Este escritor es responsable de enumerar los archivos de puerta de enlace de Servicios de Escritorio remoto (Terminal Services) para los servidores que tienen Escritorio remoto Gateway, un subrole de Servicios de Escritorio remoto rol, instalado.

**Windows Server 2003:** No se admite este sistema de escritura.

Este sistema de escritura es un sistema de escritura integrado para las Windows del sistema operativo server. no se incluye en Windows cliente.

La Servicios de Escritorio remoto de enlace depende de varias claves del Registro de las que se va a realizar una copia de seguridad y, por tanto, es necesario realizar una copia de seguridad y restaurarla junto con el registro.

La cadena de nombre del escritor para este escritor es "TS Gateway Writer".

El identificador de escritor para este escritor es 368753EC-572E-4FC7-B4B9-CCD9BDC624CB.

## <a name="remote-desktop-services-terminal-services-licensing-vss-writer"></a>Servicios de Escritorio remoto (Terminal Services) Licensing VSS Writer

Este escritor es responsable de enumerar los archivos de licencias de Servicios de Escritorio remoto (licencias de Escritorio remoto) o licencias de Terminal Services (licencias de TS) para servidores que tienen instalado Escritorio remoto Licensing, un subrole de Servicios de Escritorio remoto role.

**Windows Server 2003:** No se admite este sistema de escritura.

Este sistema de escritura es un sistema de escritura integrado para las Windows del sistema operativo server. no se envía en Windows cliente.

Servicios de Escritorio remoto licencias depende de varias claves del Registro de las que se va a realizar una copia de seguridad y, por tanto, es necesario realizar una copia de seguridad y restaurarla junto con el registro.

La cadena de nombre del escritor para este escritor es "TermServLicensing".

El identificador de escritor para este escritor es 5382579C-98DF-47A7-AC6C-98A6D7106E09.

## <a name="shadow-copy-optimization-writer"></a>Escritor de optimización de instantáneas

Este sistema de escritura elimina determinados archivos de instantáneas de volumen. Esto se hace para minimizar el impacto de la E/S de copia en escritura durante la E/S normal en estos archivos en el volumen de instantáneas. Los archivos que se eliminan suelen ser archivos temporales o archivos que no contienen el estado del usuario o del sistema.

**Windows Server 2003 y Windows XP:** No se admite este sistema de escritura.

La cadena de nombre del escritor para este escritor es "Escritor de optimización de instantáneas".

El identificador de escritor para el escritor de optimización de instantáneas es 4DC3BDD4-AB48-4D07-ADB0-3BEE2926FD7F.

## <a name="sync-share-service-writer"></a>Sincronización del escritor de servicios compartidos

**Windows Server 2012 R2:** Este sistema de escritura se incluye con Windows Server 2012 R2 y versiones de servidor más recientes. No es compatible con las versiones de escritorio.

Este escritor es responsable de enumerar los recursos compartidos de sincronización en los servidores que tienen instalado el servicio de recurso compartido de sincronización y de garantizar que sus metadatos y datos sigan siendo coherentes durante la copia de seguridad y restauración.

Este sistema de escritura solo está presente cuando sync share service está instalado y en ejecución.

Habrá un componente vss writer para cada recurso compartido de sincronización. Esto incluye los metadatos y las rutas de acceso de datos. Se deben realizar una copia de seguridad conjuntamente para mantener la coherencia.

La cadena de nombre del escritor es "Sync Share Service VSS Writer".

El identificador de escritor es D46BF321-FDBA-4A35-8EC3-454DF03BC86A.

## <a name="system-writer"></a>System Writer

El sistema de escritura enumera todos los archivos binarios del sistema operativo y del controlador y es necesario para una copia de seguridad del estado del sistema.

**Windows Server 2003 y Windows XP:** No se admite este sistema de escritura.

Este sistema de escritura se ejecuta como parte del servicio Servicios criptográficos (CryptSvc). El sistema de escritura genera una lista de archivos que contiene los siguientes archivos:

-   Todos los archivos estáticos que se han instalado. Un archivo estático es un archivo que se muestra en el manifiesto de componente con el atributo de archivo **writeableType** establecido en "static" o "". Los archivos estáticos incluyen todos los archivos protegidos por Windows Resource Protection (WRP). Sin embargo, no todos los archivos estáticos son archivos protegidos por WRP. Por ejemplo, los archivos de juego son estáticos pero no están protegidos por WRP para que los administradores puedan cambiar la configuración del control parental.
-   El contenido del Windows en paralelo (WinSxS), incluidos todos los manifiestos, componentes opcionales y archivos Win32 de terceros.
    > [!Note]  
    > Muchos de los archivos del directorio %windir% system32 son vínculos duros a archivos \\ del directorio WinSxS.

     

-   Todos los archivos PnP para los controladores instalados (propiedad de PnP).
-   Todos los servicios en modo de usuario y controladores que no son PnP.
-   Todos los catálogos propiedad de CryptSvc.

La aplicación de restauración es responsable de establecer los archivos y el registro y de establecer las ACL para que coincidan con la instantánea del sistema. También se deben crear los vínculos duros adecuados para que una restauración del estado del sistema se realiza correctamente.

La cadena de nombre del escritor para este escritor es "System Writer".

El identificador de escritor para el sistema de escritura es E8132975-6F93-4464-A53E-1050253AE220.

## <a name="task-scheduler-writer"></a>Programador de tareas Writer

Este escritor informa de los archivos de tareas del programador de tareas.

**Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** No se admite este sistema de escritura. Los solicitantes deben realizar una copia de seguridad de estos archivos manualmente. (Vea [Copia de seguridad y restauración del estado del sistema).](locating-additional-system-files.md)

La cadena de nombre del escritor para este escritor es "Programador de tareas Writer".

El identificador del escritor es D61D61C8-D73A-4EEE-8CDD-F6F9786B7124.

## <a name="vss-metadata-store-writer"></a>Escritor del almacén de metadatos de VSS

Este escritor informa de los archivos de metadatos del escritor para todos los escritores express de VSS.

**Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** No se admite este sistema de escritura.

La cadena de nombre del escritor para este escritor es "VSS Express Writer Metadata Store Writer".

El identificador del escritor es 75DFB225-E2E4-4D39-9AC9-FFAFF65DDF06.

## <a name="windows-deployment-services-wds-writer"></a>Windows Escritor de Servicios de implementación (WDS)

Este sistema de escritura notifica los Windows de datos de Deployment Services (WDS).

**Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** No se admite este sistema de escritura.

La cadena de nombre del escritor para este escritor es "WDS VSS Writer".

El identificador de escritor para este escritor es 82CB5521-68DB-4626-83A4-7FC6F88853E9.

## <a name="windows-internal-database-wid-writer"></a>escritor Windows Internal Database (WID)

Este sistema de escritura informa de Windows Internal Database archivos de datos de Windows Internal Database (WID).

**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** No se admite este sistema de escritura.

La cadena de nombre del escritor para este escritor es "WIDWriter".

El identificador de escritor para este escritor es 8D5194E1-E455-434A-B2E5-51296CCE67DF.

## <a name="windows-internet-name-service-wins-writer"></a>Windows Escritor del Servicio de nombres de Internet (WINS)

Este escritor es responsable de enumerar los archivos necesarios para WINS.

**Windows XP:** No se admite este sistema de escritura.

La cadena de nombre del escritor para este escritor es "WINS Jet Writer".

El identificador de escritor para este escritor es F08C1483-8407-4A26-8C26-6C267A629741.

## <a name="wmi-writer"></a>Escritor WMI

Este sistema de escritura se usa para identificar el estado y los datos específicos de WMI durante las operaciones de copia de seguridad. Los datos incluyen archivos del repositorio WBEM.

**Windows Server 2003 y Windows XP:** No se admite este sistema de escritura.

La cadena de nombre del escritor para este escritor es "Escritor WMI".

El identificador de escritor para este escritor es A6AD56C2-B509-4E6C-BB19-49D8F43532F0.

 

 
