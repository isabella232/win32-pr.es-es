---
description: El sistema operativo Windows incluye un conjunto de VSS Writer que son responsables de enumerar los datos que diversas características de Windows requieren. Estos se conocen como &\# 0034; en el&\# 0034; escritores.
ms.assetid: e20a303d-9440-42be-b383-85f6fad89157
title: Instancias de VSS Writer incluidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc256cfe72f3653d4af282148c87c2b45bcac51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105697007"
---
# <a name="in-box-vss-writers"></a>Instancias de VSS Writer incluidas

El sistema operativo Windows incluye un conjunto de VSS Writer que son responsables de enumerar los datos que diversas características de Windows requieren. Estos se conocen como escritores "en la caja".

> [!Note]  
> El escritor en caja de MSDE no está disponible en Windows Vista, Windows Server 2008 y versiones posteriores. En su lugar, se debe usar el escritor SQL para realizar una copia de seguridad de SQL Server bases de datos. Solo SQL Server 2005 SP2 y versiones posteriores se admiten en Windows Vista, Windows Server 2008 y versiones posteriores.

 

-   [Escritor VSS de Active Directory Domain Services (NTDS)](#active-directory-domain-services-ntds-vss-writer)
-   [Escritor de Servicios de federación de Active Directory (AD FS)](#active-directory-federation-services-writer)
-   [Escritor VSS de Active Directory Lightweight Directory Services (LDS)](#active-directory-lightweight-directory-services-lds-vss-writer)
-   [Escritor de Active Directory Rights Management Services (AD RMS)](#active-directory-rights-management-services-ad-rms-writer)
-   [Escritor de recuperación automática del sistema (ASR)](#automated-system-recovery-asr-writer)
-   [Escritor de Servicio de transferencia inteligente en segundo plano (BITS)](#background-intelligent-transfer-service-bits-writer)
-   [Escritor de la entidad de certificación](#certificate-authority-writer)
-   [Escritor del servicio de Cluster Server](#cluster-service-writer)
-   [Escritor VSS de Volumen compartido de clúster (CSV)](#cluster-shared-volume-csv-vss-writer)
-   [Escritor de base de datos de registro de clase COM+](#com-class-registration-database-writer)
-   [Escritor de desduplicación de datos](#data-deduplication-writer)
-   [Sistema de replicación de archivos distribuido (DFSR)](#distributed-file-system-replication-dfsr)
-   [Escritor del Protocolo de configuración dinámica de host (DHCP)](#dynamic-host-configuration-protocol-dhcp-writer)
-   [Servicio de replicación de archivos (FRS)](#file-replication-service-frs)
-   [Escritor de Administrador de recursos de servidor de archivos (FSRM)](#file-server-resource-manager-fsrm-writer)
-   [Escritor de Hyper-V](#hyper-v-writer)
-   [Escritor de configuración de IIS](#iis-configuration-writer)
-   [Escritor de metabase de IIS](#iis-metabase-writer)
-   [Escritor de Microsoft Message Queuing (MSMQ)](#microsoft-message-queuing-msmq-writer)
-   [Escritor del servicio MSSearch](#mssearch-service-writer)
-   [VSS Writer de NPS](#nps-vss-writer)
-   [Escritor de contadores de rendimiento](#performance-counters-writer)
-   [Escritor del registro](#registry-writer)
-   [VSS Writer de puerta de enlace de Servicios de Escritorio remoto (Terminal Services)](#remote-desktop-services-terminal-services-gateway-vss-writer)
-   [Escritor de VSS para licencias de Servicios de Escritorio remoto (Terminal Services)](#remote-desktop-services-terminal-services-licensing-vss-writer)
-   [Escritor de optimización de instantáneas](#shadow-copy-optimization-writer)
-   [Escritor de servicio de recurso compartido de sincronización](#sync-share-service-writer)
-   [Escritor del sistema](#system-writer)
-   [Escritor de Programador de tareas](#task-scheduler-writer)
-   [Escritor de almacén de metadatos de VSS](#vss-metadata-store-writer)
-   [Escritor de servicios de implementación de Windows (WDS)](#windows-deployment-services-wds-writer)
-   [Escritor de Windows Internal Database (WID)](#windows-internal-database-wid-writer)
-   [Escritor del servicio de nombres Internet de Windows (WINS)](#windows-internet-name-service-wins-writer)
-   [Escritor WMI](#wmi-writer)

## <a name="active-directory-domain-services-ntds-vss-writer"></a>Escritor VSS de Active Directory Domain Services (NTDS)

Este escritor informa del archivo de base de datos NTDS (Ntds. DIT) y de los archivos de registro asociados. Estos archivos son necesarios para restaurar el Active Directory correctamente.

Solo hay un archivo Ntds. dit por cada controlador de dominio y se incluye en los metadatos del escritor como en el ejemplo siguiente:

``` syntax
    <DATABASE_FILES path="C:\Windows\NTDS" 
                     filespec="ntds.dit" 
                     filespecBackupType="3855"/>
```

Este es un ejemplo que muestra cómo enumerar los componentes en los metadatos del escritor:

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

Durante la copia de seguridad, el escritor establece la hora de expiración de la copia de seguridad en los metadatos de copia de seguridad del escritor. Los solicitantes deben recuperar estos metadatos mediante [**IVssComponent:: GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) para determinar si la base de datos ha expirado. Las bases de datos expiradas no se pueden restaurar.

Si el equipo que contiene la base de datos NTDS es un controlador de dominio, la aplicación de copia de seguridad debe realizar siempre una copia de seguridad del estado del sistema en todos los volúmenes que contengan información crítica sobre el estado del sistema. En el momento de la restauración, la aplicación debe reiniciar primero el equipo en Modo de restauración de servicios de directorio y, a continuación, realizar una restauración del estado del sistema.

La cadena de nombre de escritor para este escritor es "NTDS".

El identificador del escritor de este escritor es B2014C9E-8711-4C5C-A5A9-3CF384484757.

## <a name="active-directory-federation-services-writer"></a>Escritor de Servicios de federación de Active Directory (AD FS)

Este escritor informa de los archivos de datos de Servicios de federación de Active Directory (AD FS) (ADFS).

**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP:** No se admite este escritor.

La cadena de nombre de escritor para este escritor es "ADFS VSS Writer".

El identificador del escritor de este escritor es 772C45F8-AE01-4F94-940C-94961864ACAD.

## <a name="active-directory-lightweight-directory-services-lds-vss-writer"></a>Escritor VSS de Active Directory Lightweight Directory Services (LDS)

Este sistema de escritura notifica el archivo de base de datos de ADAM (Adamntds. DIT) y los archivos de registro asociados para cada instancia en% archivos de programa% \\ Microsoft Adam \\ Instance *n* \\ Data, donde *N* es el número de instancia de Adam. Estos archivos de registro de base de datos son necesarios para restaurar instancias de ADAM.

**Windows XP:** No se admite este escritor.

Este es un ejemplo que muestra cómo enumerar los componentes en los metadatos del escritor:

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

Durante la copia de seguridad, el escritor establece la hora de expiración de la copia de seguridad en los metadatos de copia de seguridad. Las aplicaciones de copia de seguridad deben recuperar estos metadatos mediante el método [**IVssComponent:: GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) para determinar si la base de datos ha expirado. Las bases de datos expiradas no se pueden restaurar.

La cadena de nombre de escritor para este escritor es "ADAM (instancia *N*) Writer", donde *N* es el número de instancia de Adam, por ejemplo, "Adam (Instance1) Writer", "Adam (instance2) Writer", etc.

El identificador del escritor de este escritor es DD846AAA-A1B6-42A8-AAF8-03DCB6114BFD. Este identificador de escritor es el mismo para todas las instancias.

## <a name="active-directory-rights-management-services-ad-rms-writer"></a>Escritor de Active Directory Rights Management Services (AD RMS)

Este escritor informa de los archivos de datos del servicio de Active Directory Rights Management (AD RMS).

**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP:** No se admite este escritor.

La cadena de nombre de escritor para este escritor es "AD RMS redactor".

El identificador del escritor de este escritor es 886C43B1-D455-4428-A37F-4D6B9E43F50F.

## <a name="automated-system-recovery-asr-writer"></a>Escritor de recuperación automática del sistema (ASR)

El escritor de ASR almacena la configuración de discos en el sistema. Este sistema de escritura informa de la base de datos de configuración de arranque (BCD) y también es responsable de desmontar el subárbol del registro que representa la BCD durante la creación de la instantánea. El escritor de ASR debe estar incluido en las copias de seguridad necesarias para la reconstrucción completa. Para obtener más información acerca de ASR, consulte [uso de la recuperación automática del sistema de VSS para la recuperación ante desastres](using-vss-automated-system-recovery-for-disaster-recovery.md).

**Windows Server 2003 y Windows XP:** No se admite este escritor.

La cadena de nombre de escritor para este escritor es "escritor de ASR".

El identificador del escritor de ASR es BE000CBE-11FE-4426-9C58-531AA6355FC4.

## <a name="background-intelligent-transfer-service-bits-writer"></a>Escritor de Servicio de transferencia inteligente en segundo plano (BITS)

El escritor de BITS usa la clave del registro **FilesNotToBackup** para excluir archivos de la carpeta de caché de bits. La ubicación de caché predeterminada es% AllUsersProfile% \\ Microsoft \\ Network \\ Downloader \\ Cache.

**Windows Server 2003 y Windows XP:** No se admite este escritor.

Además, el escritor de BITS excluye los siguientes archivos de copia de seguridad: los archivos de estado de BITS (qmgr0. dat y qmgr1. dat), el archivo de registro de depuración de BITS y los archivos de BITS descargados parcialmente.

Si el archivo de destino de descarga de BITS es un archivo SMB, la cuenta de cliente debe tener una relación de confianza con el servidor, de lo contrario se puede producir un error en las copias de seguridad.

La cadena de nombre de escritor para este escritor es "escritor de BITS".

El identificador del escritor de BITS es 4969D978-BE47-48B0-B100-F328F07AC1E0.

## <a name="certificate-authority-writer"></a>Escritor de la entidad de certificación

Este escritor es responsable de enumerar los archivos de datos para el servidor de certificados.

La cadena de nombre de escritor para este escritor es "entidad de certificación".

**Windows XP:** La cadena de nombre de escritor para este escritor es "servidor de escritura de servidor de certificados".

El ID. de escritor del escritor es 6F5B15B5-DA24-4D88-B737-63063E3A1F86.

## <a name="cluster-service-writer"></a>Escritor del servicio de Cluster Server

El servicio de Cluster Server VSS Writer se documenta en la documentación de la API del [servicio de Cluster Server](/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-failover-cluster-configuration-using-vss) .

**Windows Vista, Windows Server 2003 y Windows XP:** Este escritor no se admite hasta Windows Vista con Service Pack 1 (SP1) y Windows Server 2008.

## <a name="cluster-shared-volume-csv-vss-writer"></a>Escritor VSS de Volumen compartido de clúster (CSV)

Este escritor informa de los archivos de datos de Volumen compartido de clúster (CSV). Este sistema de escritura es un escritor de la caja para las versiones del sistema operativo Windows Server; no se incluye en el cliente de Windows.

**Windows server 2008 R2, Windows server 2008 y Windows server 2003:** No se admite este escritor.

La cadena de nombre de escritor para este escritor es "Volumen compartido de clúster VSS Writer".

El ID. de escritor del escritor es 1072AE1C-E5A7-4EA1-9E4A-6F7964656570.

## <a name="com-class-registration-database-writer"></a>Escritor de base de datos de registro de clase COM+

Este escritor es responsable del contenido del directorio de registro% SystemRoot% \\ . El catálogo de COM+ es un archivo en el registro% SystemRoot% \\ con un nombre que sigue el patrón R *XXXXXXXXXXXX*. CLB, donde *XXXXXXXXXXXX* es un número hexadecimal de 12 dígitos. Puede haber varios archivos de este tipo si las aplicaciones COM+ se han configurado en el equipo. El archivo que contiene el catálogo de COM+ actual es el archivo con el mayor valor de *XXXXXXXXXXXX*.

**Windows Server 2003 y Windows XP:** No se admite este escritor.

La base de datos de registro de clase COM+ depende de una clave del registro de la que se realiza una copia de seguridad y, por tanto, debe realizarse una copia de seguridad y restaurarse junto con el registro.

Para restaurar la base de datos de registro de COM+, una aplicación de copia de seguridad (solicitante) debe llamar al método [**ICOMAdminCatalog:: RestoreREGDB**](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) .

La cadena de nombre de escritor para este escritor es "COM+ REGDB Writer".

El ID. de escritor del escritor de la base de datos de registro de clase COM+ es 542DA469-D3E1-473C-9F4F-7847F01FC64F.

## <a name="data-deduplication-writer"></a>Escritor de desduplicación de datos

La VSS Writer de desduplicación de datos se documenta en la documentación de la API de [desduplicación de datos](/previous-versions/windows/desktop/dedup/backup-and-restore-of-data-deduplication-enabled-volumes) . Este sistema de escritura es un escritor de la caja para las versiones del sistema operativo Windows Server; no se incluye en el cliente de Windows.

**Windows server 2008 R2, Windows server 2008 y Windows server 2003:** No se admite este escritor.

## <a name="distributed-file-system-replication-dfsr"></a>Sistema de replicación de archivos distribuido (DFSR)

El componente siguiente incluye un VSS Writer: [replicación de sistema de archivos distribuido (DFSR)](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders)

**Windows Vista, Windows Server 2003 y Windows XP:** Este escritor no se admite hasta Windows Vista con SP1 y Windows Server 2008.

## <a name="dynamic-host-configuration-protocol-dhcp-writer"></a>Escritor del Protocolo de configuración dinámica de host (DHCP)

Este escritor es responsable de enumerar los archivos necesarios para el rol de servidor DHCP. Este sistema de escritura es un escritor de la caja para las versiones del sistema operativo Windows Server; no se incluye en el cliente de Windows.

La cadena de nombre de escritor para este escritor es "DHCP jet Writer".

El identificador del escritor de este escritor es BE9AC81E-3619-421F-920F-4C6FEA9E93AD.

## <a name="file-replication-service-frs"></a>Servicio de replicación de archivos (FRS)

El escritor del servicio de replicación de archivos se documenta en [realizar copias de seguridad y restaurar una FRS-Replicated carpeta Sysvol](backing-up-and-restoring-an-frs-replicated-sysvol-folder.md).

**Windows Vista, Windows Server 2003 y Windows XP:** Este escritor no se admite hasta Windows Vista con SP1 y Windows Server 2008.

## <a name="file-server-resource-manager-fsrm-writer"></a>Escritor de Administrador de recursos de servidor de archivos (FSRM)

Este sistema de escritura enumera los archivos de configuración de FSRM que se usan para la copia de seguridad del estado del sistema. Durante las operaciones de restauración, se evitan los cambios en la configuración de FSRM y se detiene temporalmente la aplicación de cuotas y filtros de archivos. Una vez finalizada la restauración, el escritor actualiza FSRM con la configuración que se restauró. Este escritor solo está presente cuando FSRM (parte del rol servicios de archivo) está instalado y en ejecución. Este sistema de escritura es un escritor de la caja para las versiones del sistema operativo Windows Server; no se incluye en el cliente de Windows.

**Windows Server 2003:** Este escritor no se admite hasta Windows Server 2003 R2.

La cadena de nombre de escritor para este escritor es "FSRM Writer".

El identificador del escritor de este escritor es 12CE4370-5BB7-4C58-A76A-E5D5097E3674.

## <a name="hyper-v-writer"></a>Escritor de Hyper-V

La VSS Writer de Hyper-V se documenta en la documentación de la API de [Hyper-v](/previous-versions/windows/desktop/virtual/backing-up-and-restoring-virtual-machines) . Este sistema de escritura es un escritor de la caja para las versiones del sistema operativo Windows Server; no se incluye en el cliente de Windows.

**Windows Server 2003:** Este escritor no se admite hasta Windows Server 2008.

## <a name="iis-configuration-writer"></a>Escritor de configuración de IIS

El escritor de configuración de IIS es responsable de enumerar los archivos de configuración de IIS.

**Windows Vista, Windows Server 2003 y Windows XP:** Este escritor no se admite hasta Windows Vista con SP1 y Windows Server 2008. Los solicitantes son necesarios para realizar una copia de seguridad de los archivos de configuración de IIS, incluido el archivo de machine.config de .NET FX o el archivo de web.config raíz ASP.NET.

Este sistema de escritura no realiza una copia de seguridad del archivo de machine.config de .NET FX o del archivo de web.config raíz ASP.NET porque el sistema de escritura del sistema enumera estos archivos.

Este escritor realiza una copia de seguridad de todos los archivos que se encuentran en el esquema de configuración% WINDIR% \\ system32 \\ Inetsrv y en los directorios de \\ \\ configuración% WINDIR% \\ system32 \\ Inetsrv \\ , excepto los archivos enumerados por el escritor del sistema.

El ID. de escritor del escritor de configuración de IIS es 2A40FD15-DFCA-4aa8-A654-1F8C654603F6.

## <a name="iis-metabase-writer"></a>Escritor de metabase de IIS

El escritor de la metabase de Internet Information Server (IIS) es responsable de enumerar el archivo de la metabase de IIS.

**Windows Vista, Windows Server 2003 y Windows XP:** Este escritor no se admite hasta Windows Vista con SP1 y Windows Server 2008. Los solicitantes son necesarios para realizar una copia de seguridad del archivo de la metabase de IIS.

El ID. de escritor del escritor de la metabase de IIS es 59B1f0CF-90EF-465F-9609-6CA8B2938366.

## <a name="microsoft-message-queuing-msmq-writer"></a>Escritor de Microsoft Message Queuing (MSMQ)

Este escritor informa de los archivos de datos de Microsoft Message Queuing (MSMQ).

**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP:** No se admite este escritor.

La cadena de nombre de escritor para este escritor es "MSMQ Writer (*SvcName*)", donde *SvcName* es el nombre del servicio de MSMQ con el que está asociado el escritor. En la instalación predeterminada, el nombre del servicio es "MSMQ". En el caso de las instancias en clúster, el nombre del servicio es MSMQ $*ResourceName*, donde *ResourceName* es el nombre del recurso de MSMQ agrupado.

El identificador del escritor de este escritor es 7E47B561-971A-46E6-96B9-696EEAA53B2A.

## <a name="mssearch-service-writer"></a>Escritor del servicio MSSearch

Este escritor existe para eliminar los archivos de índice de búsqueda de instantáneas después de crearlos. Esto se hace para minimizar el impacto de la e/s de copia en escritura durante la e/s normal en estos archivos en el volumen de copia sombra.

**Windows Server 2003:** No se admite este escritor.

Para instalar este escritor en el servidor, debe instalar el rol servicios de archivo y habilitar el Search Service de Windows.

La cadena de nombre de escritor para este escritor es "MSSearch Service Writer".

El ID. de escritor del escritor del servicio MSSearch es CD3F2362-8BEF-46C7-9181-D62844CDC0B2.

## <a name="nps-vss-writer"></a>VSS Writer de NPS

El escritor de NPS es responsable de enumerar los archivos de configuración del servidor de directivas de redes (NPS) para los servidores que tienen instalado el rol servicios de acceso y directivas de redes.

**Windows Vista, Windows Server 2003 y Windows XP:** Este escritor no se admite hasta Windows Vista con SP1 y Windows Server 2008.

La cadena de nombre de escritor para este escritor es "VSS VSS Writer".

El identificador de escritor del VSS Writer NPS es 0x35E81631-13E1-48DB-97FC-D5BC721BB18A.

## <a name="performance-counters-writer"></a>Escritor de contadores de rendimiento

Este sistema de escritura informa de los archivos de configuración del contador de rendimiento. Estos archivos solo se modifican durante la instalación de la aplicación y se deben realizar copias de seguridad y restaurar durante las copias de seguridad y restauraciones del estado del sistema.

**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** No se admite este escritor. Los solicitantes son necesarios para realizar una copia de seguridad manual de estos archivos. (Consulte [copia de seguridad y restauración del estado del sistema](locating-additional-system-files.md)).

La cadena de nombre de escritor para este sistema de escritura es "escritor de contadores de rendimiento".

El ID. de escritor del escritor de contadores de rendimiento es 0BADA1DE-01A9-4625-8278-69E735F39DD2.

## <a name="registry-writer"></a>Escritor del registro

El sistema de escritura del registro informa de los archivos de registro de Windows para habilitar las copias de seguridad en contexto y las restauraciones del registro. No notifica subárboles de usuario.

**Windows Server 2003:** En Windows Server 2003, este sistema de escritura usa un archivo de repositorio intermedio (a veces denominado "archivo de prosección") para almacenar los datos del registro. (Consulte [operaciones de copia de seguridad y restauración del registro en VSS](registry-backup-and-restore-operations-under-vss.md)).

**Windows XP:** No se admite este escritor. (Consulte [operaciones de copia de seguridad y restauración del registro en VSS](registry-backup-and-restore-operations-under-vss.md)).

La cadena de nombre de escritor para este escritor es "escritor del registro".

El ID. de escritor del sistema de escritura del registro es AFBAB4A2-367D-4D15-A586-71DBB18F8485.

## <a name="remote-desktop-services-terminal-services-gateway-vss-writer"></a>VSS Writer de puerta de enlace de Servicios de Escritorio remoto (Terminal Services)

Este escritor es responsable de enumerar los archivos de puerta de enlace de Servicios de Escritorio remoto (Terminal Services) para los servidores que tienen Escritorio remoto puerta de enlace, un subrol de Servicios de Escritorio remoto rol, instalado.

**Windows Server 2003:** No se admite este escritor.

Este sistema de escritura es un escritor de la caja para las versiones del sistema operativo Windows Server; no se incluye en el cliente de Windows.

La puerta de enlace de Servicios de Escritorio remoto depende de varias claves del registro de las que se realiza una copia de seguridad y, por tanto, debe realizarse una copia de seguridad y restaurarse junto con el registro.

La cadena de nombre de escritor para este escritor es "escritor de puerta de enlace de TS".

El identificador del escritor de este escritor es 368753EC-572E-4FC7-B4B9-CCD9BDC624CB.

## <a name="remote-desktop-services-terminal-services-licensing-vss-writer"></a>Escritor de VSS para licencias de Servicios de Escritorio remoto (Terminal Services)

Este escritor es responsable de enumerar los archivos de licencias de Servicios de Escritorio remoto (licencias de escritorio remoto) o licencias de Terminal Services (licencias de TS) para los servidores que tienen instalado Escritorio remoto licencias, un subrol de Servicios de Escritorio remoto rol.

**Windows Server 2003:** No se admite este escritor.

Este sistema de escritura es un escritor de la caja para las versiones del sistema operativo Windows Server; no se incluye en el cliente de Windows.

La concesión de licencias de Servicios de Escritorio remoto depende de varias claves del registro de las que se realiza una copia de seguridad y, por tanto, debe realizarse una copia de seguridad y restaurarse junto con el registro.

La cadena de nombre de escritor para este escritor es "TermServLicensing".

El identificador del escritor de este escritor es 5382579C-98DF-47A7-AC6C-98A6D7106E09.

## <a name="shadow-copy-optimization-writer"></a>Escritor de optimización de instantáneas

Este escritor elimina determinados archivos de instantáneas de volumen. Esto se hace para minimizar el impacto de la e/s de copia en escritura durante la e/s normal en estos archivos en el volumen de copia sombra. Los archivos que se eliminan suelen ser archivos temporales que no contienen el estado del usuario o del sistema.

**Windows Server 2003 y Windows XP:** No se admite este escritor.

La cadena de nombre de escritor para este escritor es "escritor de optimización de instantáneas".

El ID. de escritor del escritor de optimización de instantáneas es 4DC3BDD4-AB48-4D07-ADB0-3BEE2926FD7F.

## <a name="sync-share-service-writer"></a>Escritor de servicio de recurso compartido de sincronización

**Windows Server 2012 R2:** Este escritor está incluido en Windows Server 2012 R2 y versiones de servidor más recientes. No es compatible con las versiones de escritorio.

Este escritor es responsable de enumerar los recursos compartidos de sincronización en los servidores que tienen instalado el servicio de recurso compartido de sincronización y para garantizar que los metadatos y los datos sigan siendo coherentes durante las copias de seguridad y restauración.

Este escritor solo está presente cuando el servicio de recurso compartido de sincronización está instalado y en ejecución.

Habrá un VSS Writer componente para cada recurso compartido de sincronización. Esto incluye los metadatos y las rutas de acceso de datos. Se debe hacer una copia de seguridad conjunta de ellas para mantener la coherencia.

La cadena de nombre de escritor es "Sync share Service VSS Writer".

El identificador del escritor es D46BF321-FDBA-4A35-8EC3-454DF03BC86A.

## <a name="system-writer"></a>Escritor del sistema

El escritor del sistema enumera todos los archivos binarios del sistema operativo y del controlador, y es necesario para una copia de seguridad del estado del sistema.

**Windows Server 2003 y Windows XP:** No se admite este escritor.

Este escritor se ejecuta como parte del servicio de servicios de cifrado (CryptSvc). El escritor del sistema genera una lista de archivos que contiene los archivos siguientes:

-   Todos los archivos estáticos que se han instalado. Un archivo estático es un archivo que aparece en el manifiesto del componente con el atributo de archivo **writeableType** establecido en "Static" o "". Los archivos estáticos incluyen todos los archivos protegidos por Protección de recursos de Windows (WRP). Sin embargo, no todos los archivos estáticos son archivos protegidos por WRP. Por ejemplo, los archivos de juego son estáticos pero no protegidos por WRP para que los administradores puedan cambiar la configuración del control parental.
-   El contenido del directorio de Windows en paralelo (WinSxS), incluidos todos los manifiestos, componentes opcionales y archivos Win32 de terceros.
    > [!Note]  
    > Muchos de los archivos del directorio% WINDIR% \\ system32 son vínculos físicos a archivos del directorio WinSxS.

     

-   Todos los archivos PnP para los controladores instalados (propiedad de PnP).
-   Todos los servicios de modo de usuario y controladores no PnP.
-   Todos los catálogos propiedad de CryptSvc.

La aplicación de restauración es responsable de la colocación de los archivos y del registro y de la configuración de las ACL para que coincidan con la instantánea del sistema. También se deben crear los vínculos físicos adecuados para que una restauración del estado del sistema se realice correctamente.

La cadena de nombre de escritor para este escritor es "escritor del sistema".

El ID. de escritor del escritor del sistema es E8132975-6F93-4464-A53E-1050253AE220.

## <a name="task-scheduler-writer"></a>Escritor de Programador de tareas

Este escritor informa de los archivos de tareas del programador de tareas.

**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** No se admite este escritor. Los solicitantes son necesarios para realizar una copia de seguridad manual de estos archivos. (Consulte [copia de seguridad y restauración del estado del sistema](locating-additional-system-files.md)).

La cadena de nombre de escritor para este escritor es "Programador de tareas redactor".

El ID. de escritor del escritor es D61D61C8-D73A-4EEE-8CDD-F6F9786B7124.

## <a name="vss-metadata-store-writer"></a>Escritor de almacén de metadatos de VSS

Este escritor notifica los archivos de metadatos de escritura para todos los escritores de VSS Express.

**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** No se admite este escritor.

La cadena de nombre de escritor para este escritor es "VSS Express Writer Metadata Store Writer".

El ID. de escritor del escritor es 75DFB225-E2E4-4D39-9AC9-FFAFF65DDF06.

## <a name="windows-deployment-services-wds-writer"></a>Escritor de servicios de implementación de Windows (WDS)

Este escritor informa de los archivos de datos de servicios de implementación de Windows (WDS).

**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** No se admite este escritor.

La cadena de nombre de escritor para este escritor es "WDS VSS Writer".

El identificador del escritor de este escritor es 82CB5521-68DB-4626-83A4-7FC6F88853E9.

## <a name="windows-internal-database-wid-writer"></a>Escritor de Windows Internal Database (WID)

Este escritor informa de los archivos de datos de Windows Internal Database (WID).

**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP:** No se admite este escritor.

La cadena de nombre de escritor para este escritor es "WIDWriter".

El identificador del escritor de este escritor es 8D5194E1-E455-434A-B2E5-51296CCE67DF.

## <a name="windows-internet-name-service-wins-writer"></a>Escritor del servicio de nombres Internet de Windows (WINS)

Este escritor es responsable de enumerar los archivos necesarios para WINS.

**Windows XP:** No se admite este escritor.

La cadena de nombre de escritor para este escritor es "WINS jet Writer".

El identificador del escritor de este escritor es F08C1483-8407-4A26-8C26-6C267A629741.

## <a name="wmi-writer"></a>Escritor WMI

Este escritor se utiliza para identificar el estado específico de WMI y los datos durante las operaciones de copia de seguridad. Los datos incluyen archivos del repositorio WBEM.

**Windows Server 2003 y Windows XP:** No se admite este escritor.

La cadena de nombre de escritor para este escritor es "escritor de WMI".

El identificador del escritor de este escritor es A6AD56C2-B509-4E6C-BB19-49D8F43532F0.

 

 
