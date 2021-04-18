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
# <a name="in-box-vss-writers"></a><span data-ttu-id="8aa49-104">Instancias de VSS Writer incluidas</span><span class="sxs-lookup"><span data-stu-id="8aa49-104">In-Box VSS Writers</span></span>

<span data-ttu-id="8aa49-105">El sistema operativo Windows incluye un conjunto de VSS Writer que son responsables de enumerar los datos que diversas características de Windows requieren.</span><span class="sxs-lookup"><span data-stu-id="8aa49-105">The Windows operating system includes a set of VSS writers that are responsible for enumerating the data that is required by various Windows features.</span></span> <span data-ttu-id="8aa49-106">Estos se conocen como escritores "en la caja".</span><span class="sxs-lookup"><span data-stu-id="8aa49-106">These are referred to as "in-box" writers.</span></span>

> [!Note]  
> <span data-ttu-id="8aa49-107">El escritor en caja de MSDE no está disponible en Windows Vista, Windows Server 2008 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="8aa49-107">The MSDE in-box writer is not available in Windows Vista, Windows Server 2008, and later.</span></span> <span data-ttu-id="8aa49-108">En su lugar, se debe usar el escritor SQL para realizar una copia de seguridad de SQL Server bases de datos.</span><span class="sxs-lookup"><span data-stu-id="8aa49-108">Instead, the SQL Writer should be used to back up SQL Server databases.</span></span> <span data-ttu-id="8aa49-109">Solo SQL Server 2005 SP2 y versiones posteriores se admiten en Windows Vista, Windows Server 2008 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="8aa49-109">Only SQL Server 2005 SP2 and later are supported on Windows Vista, Windows Server 2008, and later.</span></span>

 

-   [<span data-ttu-id="8aa49-110">Escritor VSS de Active Directory Domain Services (NTDS)</span><span class="sxs-lookup"><span data-stu-id="8aa49-110">Active Directory Domain Services (NTDS) VSS Writer</span></span>](#active-directory-domain-services-ntds-vss-writer)
-   [<span data-ttu-id="8aa49-111">Escritor de Servicios de federación de Active Directory (AD FS)</span><span class="sxs-lookup"><span data-stu-id="8aa49-111">Active Directory Federation Services Writer</span></span>](#active-directory-federation-services-writer)
-   [<span data-ttu-id="8aa49-112">Escritor VSS de Active Directory Lightweight Directory Services (LDS)</span><span class="sxs-lookup"><span data-stu-id="8aa49-112">Active Directory Lightweight Directory Services (LDS) VSS Writer</span></span>](#active-directory-lightweight-directory-services-lds-vss-writer)
-   [<span data-ttu-id="8aa49-113">Escritor de Active Directory Rights Management Services (AD RMS)</span><span class="sxs-lookup"><span data-stu-id="8aa49-113">Active Directory Rights Management Services (AD RMS) Writer</span></span>](#active-directory-rights-management-services-ad-rms-writer)
-   [<span data-ttu-id="8aa49-114">Escritor de recuperación automática del sistema (ASR)</span><span class="sxs-lookup"><span data-stu-id="8aa49-114">Automated System Recovery (ASR) Writer</span></span>](#automated-system-recovery-asr-writer)
-   [<span data-ttu-id="8aa49-115">Escritor de Servicio de transferencia inteligente en segundo plano (BITS)</span><span class="sxs-lookup"><span data-stu-id="8aa49-115">Background Intelligent Transfer Service (BITS) Writer</span></span>](#background-intelligent-transfer-service-bits-writer)
-   [<span data-ttu-id="8aa49-116">Escritor de la entidad de certificación</span><span class="sxs-lookup"><span data-stu-id="8aa49-116">Certificate Authority Writer</span></span>](#certificate-authority-writer)
-   [<span data-ttu-id="8aa49-117">Escritor del servicio de Cluster Server</span><span class="sxs-lookup"><span data-stu-id="8aa49-117">Cluster Service Writer</span></span>](#cluster-service-writer)
-   [<span data-ttu-id="8aa49-118">Escritor VSS de Volumen compartido de clúster (CSV)</span><span class="sxs-lookup"><span data-stu-id="8aa49-118">Cluster Shared Volume (CSV) VSS Writer</span></span>](#cluster-shared-volume-csv-vss-writer)
-   [<span data-ttu-id="8aa49-119">Escritor de base de datos de registro de clase COM+</span><span class="sxs-lookup"><span data-stu-id="8aa49-119">COM+ Class Registration Database Writer</span></span>](#com-class-registration-database-writer)
-   [<span data-ttu-id="8aa49-120">Escritor de desduplicación de datos</span><span class="sxs-lookup"><span data-stu-id="8aa49-120">Data Deduplication Writer</span></span>](#data-deduplication-writer)
-   [<span data-ttu-id="8aa49-121">Sistema de replicación de archivos distribuido (DFSR)</span><span class="sxs-lookup"><span data-stu-id="8aa49-121">Distributed File System Replication (DFSR)</span></span>](#distributed-file-system-replication-dfsr)
-   [<span data-ttu-id="8aa49-122">Escritor del Protocolo de configuración dinámica de host (DHCP)</span><span class="sxs-lookup"><span data-stu-id="8aa49-122">Dynamic Host Configuration Protocol (DHCP) Writer</span></span>](#dynamic-host-configuration-protocol-dhcp-writer)
-   [<span data-ttu-id="8aa49-123">Servicio de replicación de archivos (FRS)</span><span class="sxs-lookup"><span data-stu-id="8aa49-123">File Replication Service (FRS)</span></span>](#file-replication-service-frs)
-   [<span data-ttu-id="8aa49-124">Escritor de Administrador de recursos de servidor de archivos (FSRM)</span><span class="sxs-lookup"><span data-stu-id="8aa49-124">File Server Resource Manager (FSRM) Writer</span></span>](#file-server-resource-manager-fsrm-writer)
-   [<span data-ttu-id="8aa49-125">Escritor de Hyper-V</span><span class="sxs-lookup"><span data-stu-id="8aa49-125">Hyper-V Writer</span></span>](#hyper-v-writer)
-   [<span data-ttu-id="8aa49-126">Escritor de configuración de IIS</span><span class="sxs-lookup"><span data-stu-id="8aa49-126">IIS Configuration Writer</span></span>](#iis-configuration-writer)
-   [<span data-ttu-id="8aa49-127">Escritor de metabase de IIS</span><span class="sxs-lookup"><span data-stu-id="8aa49-127">IIS Metabase Writer</span></span>](#iis-metabase-writer)
-   [<span data-ttu-id="8aa49-128">Escritor de Microsoft Message Queuing (MSMQ)</span><span class="sxs-lookup"><span data-stu-id="8aa49-128">Microsoft Message Queuing (MSMQ) Writer</span></span>](#microsoft-message-queuing-msmq-writer)
-   [<span data-ttu-id="8aa49-129">Escritor del servicio MSSearch</span><span class="sxs-lookup"><span data-stu-id="8aa49-129">MSSearch Service Writer</span></span>](#mssearch-service-writer)
-   [<span data-ttu-id="8aa49-130">VSS Writer de NPS</span><span class="sxs-lookup"><span data-stu-id="8aa49-130">NPS VSS Writer</span></span>](#nps-vss-writer)
-   [<span data-ttu-id="8aa49-131">Escritor de contadores de rendimiento</span><span class="sxs-lookup"><span data-stu-id="8aa49-131">Performance Counters Writer</span></span>](#performance-counters-writer)
-   [<span data-ttu-id="8aa49-132">Escritor del registro</span><span class="sxs-lookup"><span data-stu-id="8aa49-132">Registry Writer</span></span>](#registry-writer)
-   [<span data-ttu-id="8aa49-133">VSS Writer de puerta de enlace de Servicios de Escritorio remoto (Terminal Services)</span><span class="sxs-lookup"><span data-stu-id="8aa49-133">Remote Desktop Services (Terminal Services) Gateway VSS Writer</span></span>](#remote-desktop-services-terminal-services-gateway-vss-writer)
-   [<span data-ttu-id="8aa49-134">Escritor de VSS para licencias de Servicios de Escritorio remoto (Terminal Services)</span><span class="sxs-lookup"><span data-stu-id="8aa49-134">Remote Desktop Services (Terminal Services) Licensing VSS Writer</span></span>](#remote-desktop-services-terminal-services-licensing-vss-writer)
-   [<span data-ttu-id="8aa49-135">Escritor de optimización de instantáneas</span><span class="sxs-lookup"><span data-stu-id="8aa49-135">Shadow Copy Optimization Writer</span></span>](#shadow-copy-optimization-writer)
-   [<span data-ttu-id="8aa49-136">Escritor de servicio de recurso compartido de sincronización</span><span class="sxs-lookup"><span data-stu-id="8aa49-136">Sync Share Service Writer</span></span>](#sync-share-service-writer)
-   [<span data-ttu-id="8aa49-137">Escritor del sistema</span><span class="sxs-lookup"><span data-stu-id="8aa49-137">System Writer</span></span>](#system-writer)
-   [<span data-ttu-id="8aa49-138">Escritor de Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="8aa49-138">Task Scheduler Writer</span></span>](#task-scheduler-writer)
-   [<span data-ttu-id="8aa49-139">Escritor de almacén de metadatos de VSS</span><span class="sxs-lookup"><span data-stu-id="8aa49-139">VSS Metadata Store Writer</span></span>](#vss-metadata-store-writer)
-   [<span data-ttu-id="8aa49-140">Escritor de servicios de implementación de Windows (WDS)</span><span class="sxs-lookup"><span data-stu-id="8aa49-140">Windows Deployment Services (WDS) Writer</span></span>](#windows-deployment-services-wds-writer)
-   [<span data-ttu-id="8aa49-141">Escritor de Windows Internal Database (WID)</span><span class="sxs-lookup"><span data-stu-id="8aa49-141">Windows Internal Database (WID) Writer</span></span>](#windows-internal-database-wid-writer)
-   [<span data-ttu-id="8aa49-142">Escritor del servicio de nombres Internet de Windows (WINS)</span><span class="sxs-lookup"><span data-stu-id="8aa49-142">Windows Internet Name Service (WINS) Writer</span></span>](#windows-internet-name-service-wins-writer)
-   [<span data-ttu-id="8aa49-143">Escritor WMI</span><span class="sxs-lookup"><span data-stu-id="8aa49-143">WMI Writer</span></span>](#wmi-writer)

## <a name="active-directory-domain-services-ntds-vss-writer"></a><span data-ttu-id="8aa49-144">Escritor VSS de Active Directory Domain Services (NTDS)</span><span class="sxs-lookup"><span data-stu-id="8aa49-144">Active Directory Domain Services (NTDS) VSS Writer</span></span>

<span data-ttu-id="8aa49-145">Este escritor informa del archivo de base de datos NTDS (Ntds. DIT) y de los archivos de registro asociados.</span><span class="sxs-lookup"><span data-stu-id="8aa49-145">This writer reports the NTDS database file (ntds.dit) and the associated log files.</span></span> <span data-ttu-id="8aa49-146">Estos archivos son necesarios para restaurar el Active Directory correctamente.</span><span class="sxs-lookup"><span data-stu-id="8aa49-146">These files are required to restore the Active Directory correctly.</span></span>

<span data-ttu-id="8aa49-147">Solo hay un archivo Ntds. dit por cada controlador de dominio y se incluye en los metadatos del escritor como en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8aa49-147">There is only one ntds.dit file per domain controller, and it is reported in the writer metadata as in the following example:</span></span>

``` syntax
    <DATABASE_FILES path="C:\Windows\NTDS" 
                     filespec="ntds.dit" 
                     filespecBackupType="3855"/>
```

<span data-ttu-id="8aa49-148">Este es un ejemplo que muestra cómo enumerar los componentes en los metadatos del escritor:</span><span class="sxs-lookup"><span data-stu-id="8aa49-148">Here is an example that shows how to list components in the writer's metadata:</span></span>

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

<span data-ttu-id="8aa49-149">Durante la copia de seguridad, el escritor establece la hora de expiración de la copia de seguridad en los metadatos de copia de seguridad del escritor.</span><span class="sxs-lookup"><span data-stu-id="8aa49-149">At backup time, the writer sets the backup expiration time in the writer's backup metadata.</span></span> <span data-ttu-id="8aa49-150">Los solicitantes deben recuperar estos metadatos mediante [**IVssComponent:: GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) para determinar si la base de datos ha expirado.</span><span class="sxs-lookup"><span data-stu-id="8aa49-150">Requesters should retrieve this metadata by using [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) to determine whether the database has expired.</span></span> <span data-ttu-id="8aa49-151">Las bases de datos expiradas no se pueden restaurar.</span><span class="sxs-lookup"><span data-stu-id="8aa49-151">Expired databases cannot be restored.</span></span>

<span data-ttu-id="8aa49-152">Si el equipo que contiene la base de datos NTDS es un controlador de dominio, la aplicación de copia de seguridad debe realizar siempre una copia de seguridad del estado del sistema en todos los volúmenes que contengan información crítica sobre el estado del sistema.</span><span class="sxs-lookup"><span data-stu-id="8aa49-152">If the computer that contains the NTDS database is a domain controller, the backup application should always perform a system state backup across all volumes containing critical system state information.</span></span> <span data-ttu-id="8aa49-153">En el momento de la restauración, la aplicación debe reiniciar primero el equipo en Modo de restauración de servicios de directorio y, a continuación, realizar una restauración del estado del sistema.</span><span class="sxs-lookup"><span data-stu-id="8aa49-153">At restore time, the application should first restart the computer in Directory Services Restore Mode and then perform a system state restore.</span></span>

<span data-ttu-id="8aa49-154">La cadena de nombre de escritor para este escritor es "NTDS".</span><span class="sxs-lookup"><span data-stu-id="8aa49-154">The writer name string for this writer is "NTDS".</span></span>

<span data-ttu-id="8aa49-155">El identificador del escritor de este escritor es B2014C9E-8711-4C5C-A5A9-3CF384484757.</span><span class="sxs-lookup"><span data-stu-id="8aa49-155">The writer ID for this writer is B2014C9E-8711-4C5C-A5A9-3CF384484757.</span></span>

## <a name="active-directory-federation-services-writer"></a><span data-ttu-id="8aa49-156">Escritor de Servicios de federación de Active Directory (AD FS)</span><span class="sxs-lookup"><span data-stu-id="8aa49-156">Active Directory Federation Services Writer</span></span>

<span data-ttu-id="8aa49-157">Este escritor informa de los archivos de datos de Servicios de federación de Active Directory (AD FS) (ADFS).</span><span class="sxs-lookup"><span data-stu-id="8aa49-157">This writer reports the Active Directory Federation Services (ADFS) data files.</span></span>

<span data-ttu-id="8aa49-158">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP:** No se admite este escritor.</span><span class="sxs-lookup"><span data-stu-id="8aa49-158">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8aa49-159">La cadena de nombre de escritor para este escritor es "ADFS VSS Writer".</span><span class="sxs-lookup"><span data-stu-id="8aa49-159">The writer name string for this writer is "ADFS VSS Writer".</span></span>

<span data-ttu-id="8aa49-160">El identificador del escritor de este escritor es 772C45F8-AE01-4F94-940C-94961864ACAD.</span><span class="sxs-lookup"><span data-stu-id="8aa49-160">The writer ID for this writer is 772C45F8-AE01-4F94-940C-94961864ACAD.</span></span>

## <a name="active-directory-lightweight-directory-services-lds-vss-writer"></a><span data-ttu-id="8aa49-161">Escritor VSS de Active Directory Lightweight Directory Services (LDS)</span><span class="sxs-lookup"><span data-stu-id="8aa49-161">Active Directory Lightweight Directory Services (LDS) VSS Writer</span></span>

<span data-ttu-id="8aa49-162">Este sistema de escritura notifica el archivo de base de datos de ADAM (Adamntds. DIT) y los archivos de registro asociados para cada instancia en% archivos de programa% \\ Microsoft Adam \\ Instance *n* \\ Data, donde *N* es el número de instancia de Adam.</span><span class="sxs-lookup"><span data-stu-id="8aa49-162">This writer reports the ADAM database file (adamntds.dit) and the associated log files for each instance in %program files%\\Microsoft ADAM\\instance *N*\\data, where *N* is the ADAM instance number.</span></span> <span data-ttu-id="8aa49-163">Estos archivos de registro de base de datos son necesarios para restaurar instancias de ADAM.</span><span class="sxs-lookup"><span data-stu-id="8aa49-163">These database log files are required to restore ADAM instances.</span></span>

<span data-ttu-id="8aa49-164">**Windows XP:** No se admite este escritor.</span><span class="sxs-lookup"><span data-stu-id="8aa49-164">**Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8aa49-165">Este es un ejemplo que muestra cómo enumerar los componentes en los metadatos del escritor:</span><span class="sxs-lookup"><span data-stu-id="8aa49-165">Here is an example that shows how to list components in the writer's metadata:</span></span>

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

<span data-ttu-id="8aa49-166">Durante la copia de seguridad, el escritor establece la hora de expiración de la copia de seguridad en los metadatos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="8aa49-166">At backup time, the writer sets the backup expiration time in the backup metadata.</span></span> <span data-ttu-id="8aa49-167">Las aplicaciones de copia de seguridad deben recuperar estos metadatos mediante el método [**IVssComponent:: GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) para determinar si la base de datos ha expirado.</span><span class="sxs-lookup"><span data-stu-id="8aa49-167">Backup applications should retrieve this metadata by using the [**IVssComponent::GetBackupMetadata**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getbackupmetadata) method to determine whether the database has expired.</span></span> <span data-ttu-id="8aa49-168">Las bases de datos expiradas no se pueden restaurar.</span><span class="sxs-lookup"><span data-stu-id="8aa49-168">Expired databases cannot be restored.</span></span>

<span data-ttu-id="8aa49-169">La cadena de nombre de escritor para este escritor es "ADAM (instancia *N*) Writer", donde *N* es el número de instancia de Adam, por ejemplo, "Adam (Instance1) Writer", "Adam (instance2) Writer", etc.</span><span class="sxs-lookup"><span data-stu-id="8aa49-169">The writer name string for this writer is "ADAM (instance *N*) Writer", where *N* is the ADAM instance number, for example, "ADAM (instance1) Writer", "ADAM (instance2) Writer", and so on.</span></span>

<span data-ttu-id="8aa49-170">El identificador del escritor de este escritor es DD846AAA-A1B6-42A8-AAF8-03DCB6114BFD.</span><span class="sxs-lookup"><span data-stu-id="8aa49-170">The writer ID for this writer is DD846AAA-A1B6-42A8-AAF8-03DCB6114BFD.</span></span> <span data-ttu-id="8aa49-171">Este identificador de escritor es el mismo para todas las instancias.</span><span class="sxs-lookup"><span data-stu-id="8aa49-171">This writer ID is the same for all instances.</span></span>

## <a name="active-directory-rights-management-services-ad-rms-writer"></a><span data-ttu-id="8aa49-172">Escritor de Active Directory Rights Management Services (AD RMS)</span><span class="sxs-lookup"><span data-stu-id="8aa49-172">Active Directory Rights Management Services (AD RMS) Writer</span></span>

<span data-ttu-id="8aa49-173">Este escritor informa de los archivos de datos del servicio de Active Directory Rights Management (AD RMS).</span><span class="sxs-lookup"><span data-stu-id="8aa49-173">This writer reports the Active Directory Rights Management Service (AD RMS) data files.</span></span>

<span data-ttu-id="8aa49-174">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP:** No se admite este escritor.</span><span class="sxs-lookup"><span data-stu-id="8aa49-174">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8aa49-175">La cadena de nombre de escritor para este escritor es "AD RMS redactor".</span><span class="sxs-lookup"><span data-stu-id="8aa49-175">The writer name string for this writer is "AD RMS Writer".</span></span>

<span data-ttu-id="8aa49-176">El identificador del escritor de este escritor es 886C43B1-D455-4428-A37F-4D6B9E43F50F.</span><span class="sxs-lookup"><span data-stu-id="8aa49-176">The writer ID for this writer is 886C43B1-D455-4428-A37F-4D6B9E43F50F.</span></span>

## <a name="automated-system-recovery-asr-writer"></a><span data-ttu-id="8aa49-177">Escritor de recuperación automática del sistema (ASR)</span><span class="sxs-lookup"><span data-stu-id="8aa49-177">Automated System Recovery (ASR) Writer</span></span>

<span data-ttu-id="8aa49-178">El escritor de ASR almacena la configuración de discos en el sistema.</span><span class="sxs-lookup"><span data-stu-id="8aa49-178">The ASR writer stores the configuration of disks on the system.</span></span> <span data-ttu-id="8aa49-179">Este sistema de escritura informa de la base de datos de configuración de arranque (BCD) y también es responsable de desmontar el subárbol del registro que representa la BCD durante la creación de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="8aa49-179">This writer reports the Boot Configuration Database (BCD) and is also responsible for dismounting the registry hive that represents the BCD during shadow copy creation.</span></span> <span data-ttu-id="8aa49-180">El escritor de ASR debe estar incluido en las copias de seguridad necesarias para la reconstrucción completa.</span><span class="sxs-lookup"><span data-stu-id="8aa49-180">The ASR writer must be included in any backups required for bare-metal recovery.</span></span> <span data-ttu-id="8aa49-181">Para obtener más información acerca de ASR, consulte [uso de la recuperación automática del sistema de VSS para la recuperación ante desastres](using-vss-automated-system-recovery-for-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="8aa49-181">For more information about ASR, see [Using VSS Automated System Recovery for Disaster Recovery](using-vss-automated-system-recovery-for-disaster-recovery.md).</span></span>

<span data-ttu-id="8aa49-182">**Windows Server 2003 y Windows XP:** No se admite este escritor.</span><span class="sxs-lookup"><span data-stu-id="8aa49-182">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8aa49-183">La cadena de nombre de escritor para este escritor es "escritor de ASR".</span><span class="sxs-lookup"><span data-stu-id="8aa49-183">The writer name string for this writer is "ASR Writer".</span></span>

<span data-ttu-id="8aa49-184">El identificador del escritor de ASR es BE000CBE-11FE-4426-9C58-531AA6355FC4.</span><span class="sxs-lookup"><span data-stu-id="8aa49-184">The writer ID for the ASR writer is BE000CBE-11FE-4426-9C58-531AA6355FC4.</span></span>

## <a name="background-intelligent-transfer-service-bits-writer"></a><span data-ttu-id="8aa49-185">Escritor de Servicio de transferencia inteligente en segundo plano (BITS)</span><span class="sxs-lookup"><span data-stu-id="8aa49-185">Background Intelligent Transfer Service (BITS) Writer</span></span>

<span data-ttu-id="8aa49-186">El escritor de BITS usa la clave del registro **FilesNotToBackup** para excluir archivos de la carpeta de caché de bits.</span><span class="sxs-lookup"><span data-stu-id="8aa49-186">The BITS writer uses the **FilesNotToBackup** registry key to exclude files from the BITS cache folder.</span></span> <span data-ttu-id="8aa49-187">La ubicación de caché predeterminada es% AllUsersProfile% \\ Microsoft \\ Network \\ Downloader \\ Cache.</span><span class="sxs-lookup"><span data-stu-id="8aa49-187">The default cache location is %AllUsersProfile%\\Microsoft\\Network\\Downloader\\Cache.</span></span>

<span data-ttu-id="8aa49-188">**Windows Server 2003 y Windows XP:** No se admite este escritor.</span><span class="sxs-lookup"><span data-stu-id="8aa49-188">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8aa49-189">Además, el escritor de BITS excluye los siguientes archivos de copia de seguridad: los archivos de estado de BITS (qmgr0. dat y qmgr1. dat), el archivo de registro de depuración de BITS y los archivos de BITS descargados parcialmente.</span><span class="sxs-lookup"><span data-stu-id="8aa49-189">In addition, the BITS writer excludes the following files from backup: the BITS state files (qmgr0.dat and qmgr1.dat), the BITS debug log file, and BITS partially downloaded files.</span></span>

<span data-ttu-id="8aa49-190">Si el archivo de destino de descarga de BITS es un archivo SMB, la cuenta de cliente debe tener una relación de confianza con el servidor, de lo contrario se puede producir un error en las copias de seguridad.</span><span class="sxs-lookup"><span data-stu-id="8aa49-190">If the BITS download destination file is an SMB file, the client account must have a trust relationship to the server, or else backups may fail.</span></span>

<span data-ttu-id="8aa49-191">La cadena de nombre de escritor para este escritor es "escritor de BITS".</span><span class="sxs-lookup"><span data-stu-id="8aa49-191">The writer name string for this writer is "BITS Writer".</span></span>

<span data-ttu-id="8aa49-192">El identificador del escritor de BITS es 4969D978-BE47-48B0-B100-F328F07AC1E0.</span><span class="sxs-lookup"><span data-stu-id="8aa49-192">The writer ID for the BITS writer is 4969D978-BE47-48B0-B100-F328F07AC1E0.</span></span>

## <a name="certificate-authority-writer"></a><span data-ttu-id="8aa49-193">Escritor de la entidad de certificación</span><span class="sxs-lookup"><span data-stu-id="8aa49-193">Certificate Authority Writer</span></span>

<span data-ttu-id="8aa49-194">Este escritor es responsable de enumerar los archivos de datos para el servidor de certificados.</span><span class="sxs-lookup"><span data-stu-id="8aa49-194">This writer is responsible for enumerating the data files for the Certificate Server.</span></span>

<span data-ttu-id="8aa49-195">La cadena de nombre de escritor para este escritor es "entidad de certificación".</span><span class="sxs-lookup"><span data-stu-id="8aa49-195">The writer name string for this writer is "Certificate Authority".</span></span>

<span data-ttu-id="8aa49-196">**Windows XP:** La cadena de nombre de escritor para este escritor es "servidor de escritura de servidor de certificados".</span><span class="sxs-lookup"><span data-stu-id="8aa49-196">**Windows XP:** The writer name string for this writer is "Certificate Server Writer".</span></span>

<span data-ttu-id="8aa49-197">El ID. de escritor del escritor es 6F5B15B5-DA24-4D88-B737-63063E3A1F86.</span><span class="sxs-lookup"><span data-stu-id="8aa49-197">The writer ID for the writer is 6F5B15B5-DA24-4D88-B737-63063E3A1F86.</span></span>

## <a name="cluster-service-writer"></a><span data-ttu-id="8aa49-198">Escritor del servicio de Cluster Server</span><span class="sxs-lookup"><span data-stu-id="8aa49-198">Cluster Service Writer</span></span>

<span data-ttu-id="8aa49-199">El servicio de Cluster Server VSS Writer se documenta en la documentación de la API del [servicio de Cluster Server](/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-failover-cluster-configuration-using-vss) .</span><span class="sxs-lookup"><span data-stu-id="8aa49-199">The Cluster Service VSS writer is documented in the [Cluster Service](/previous-versions/windows/desktop/mscs/backing-up-and-restoring-the-failover-cluster-configuration-using-vss) API documentation.</span></span>

<span data-ttu-id="8aa49-200">**Windows Vista, Windows Server 2003 y Windows XP:** Este escritor no se admite hasta Windows Vista con Service Pack 1 (SP1) y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8aa49-200">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with Service Pack 1 (SP1) and Windows Server 2008.</span></span>

## <a name="cluster-shared-volume-csv-vss-writer"></a><span data-ttu-id="8aa49-201">Escritor VSS de Volumen compartido de clúster (CSV)</span><span class="sxs-lookup"><span data-stu-id="8aa49-201">Cluster Shared Volume (CSV) VSS Writer</span></span>

<span data-ttu-id="8aa49-202">Este escritor informa de los archivos de datos de Volumen compartido de clúster (CSV).</span><span class="sxs-lookup"><span data-stu-id="8aa49-202">This writer reports the Cluster Shared Volume (CSV) data files.</span></span> <span data-ttu-id="8aa49-203">Este sistema de escritura es un escritor de la caja para las versiones del sistema operativo Windows Server; no se incluye en el cliente de Windows.</span><span class="sxs-lookup"><span data-stu-id="8aa49-203">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="8aa49-204">**Windows server 2008 R2, Windows server 2008 y Windows server 2003:** No se admite este escritor.</span><span class="sxs-lookup"><span data-stu-id="8aa49-204">**Windows Server 2008 R2, Windows Server 2008 and Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="8aa49-205">La cadena de nombre de escritor para este escritor es "Volumen compartido de clúster VSS Writer".</span><span class="sxs-lookup"><span data-stu-id="8aa49-205">The writer name string for this writer is "Cluster Shared Volume VSS Writer".</span></span>

<span data-ttu-id="8aa49-206">El ID. de escritor del escritor es 1072AE1C-E5A7-4EA1-9E4A-6F7964656570.</span><span class="sxs-lookup"><span data-stu-id="8aa49-206">The writer ID for the writer is 1072AE1C-E5A7-4EA1-9E4A-6F7964656570.</span></span>

## <a name="com-class-registration-database-writer"></a><span data-ttu-id="8aa49-207">Escritor de base de datos de registro de clase COM+</span><span class="sxs-lookup"><span data-stu-id="8aa49-207">COM+ Class Registration Database Writer</span></span>

<span data-ttu-id="8aa49-208">Este escritor es responsable del contenido del directorio de registro% SystemRoot% \\ .</span><span class="sxs-lookup"><span data-stu-id="8aa49-208">This writer is responsible for the contents of the %SystemRoot%\\Registration directory.</span></span> <span data-ttu-id="8aa49-209">El catálogo de COM+ es un archivo en el registro% SystemRoot% \\ con un nombre que sigue el patrón R *XXXXXXXXXXXX*. CLB, donde *XXXXXXXXXXXX* es un número hexadecimal de 12 dígitos.</span><span class="sxs-lookup"><span data-stu-id="8aa49-209">The COM+ catalog is a file in %SystemRoot%\\Registration with a name that follows the pattern R *xxxxxxxxxxxx*.clb, where *xxxxxxxxxxxx* is a 12-digit hexadecimal number.</span></span> <span data-ttu-id="8aa49-210">Puede haber varios archivos de este tipo si las aplicaciones COM+ se han configurado en el equipo.</span><span class="sxs-lookup"><span data-stu-id="8aa49-210">There can potentially be multiple such files if COM+ applications have been configured on the computer.</span></span> <span data-ttu-id="8aa49-211">El archivo que contiene el catálogo de COM+ actual es el archivo con el mayor valor de *XXXXXXXXXXXX*.</span><span class="sxs-lookup"><span data-stu-id="8aa49-211">The file that contains the current COM+ catalog is the file with the largest value of *xxxxxxxxxxxx*.</span></span>

<span data-ttu-id="8aa49-212">**Windows Server 2003 y Windows XP:** No se admite este escritor.</span><span class="sxs-lookup"><span data-stu-id="8aa49-212">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8aa49-213">La base de datos de registro de clase COM+ depende de una clave del registro de la que se realiza una copia de seguridad y, por tanto, debe realizarse una copia de seguridad y restaurarse junto con el registro.</span><span class="sxs-lookup"><span data-stu-id="8aa49-213">The COM+ class registration database depends on a registry key being backed up and hence needs to be backed up and restored together with the registry.</span></span>

<span data-ttu-id="8aa49-214">Para restaurar la base de datos de registro de COM+, una aplicación de copia de seguridad (solicitante) debe llamar al método [**ICOMAdminCatalog:: RestoreREGDB**](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) .</span><span class="sxs-lookup"><span data-stu-id="8aa49-214">To restore the COM+ Registration Database, a backup application (requester) must call the [**ICOMAdminCatalog::RestoreREGDB**](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) method.</span></span>

<span data-ttu-id="8aa49-215">La cadena de nombre de escritor para este escritor es "COM+ REGDB Writer".</span><span class="sxs-lookup"><span data-stu-id="8aa49-215">The writer name string for this writer is "COM+ REGDB Writer".</span></span>

<span data-ttu-id="8aa49-216">El ID. de escritor del escritor de la base de datos de registro de clase COM+ es 542DA469-D3E1-473C-9F4F-7847F01FC64F.</span><span class="sxs-lookup"><span data-stu-id="8aa49-216">The writer ID for the COM+ class registration database writer is 542DA469-D3E1-473C-9F4F-7847F01FC64F.</span></span>

## <a name="data-deduplication-writer"></a><span data-ttu-id="8aa49-217">Escritor de desduplicación de datos</span><span class="sxs-lookup"><span data-stu-id="8aa49-217">Data Deduplication Writer</span></span>

<span data-ttu-id="8aa49-218">La VSS Writer de desduplicación de datos se documenta en la documentación de la API de [desduplicación de datos](/previous-versions/windows/desktop/dedup/backup-and-restore-of-data-deduplication-enabled-volumes) .</span><span class="sxs-lookup"><span data-stu-id="8aa49-218">The Data Deduplication VSS writer is documented in the [Data Deduplication](/previous-versions/windows/desktop/dedup/backup-and-restore-of-data-deduplication-enabled-volumes) API documentation.</span></span> <span data-ttu-id="8aa49-219">Este sistema de escritura es un escritor de la caja para las versiones del sistema operativo Windows Server; no se incluye en el cliente de Windows.</span><span class="sxs-lookup"><span data-stu-id="8aa49-219">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="8aa49-220">**Windows server 2008 R2, Windows server 2008 y Windows server 2003:** No se admite este escritor.</span><span class="sxs-lookup"><span data-stu-id="8aa49-220">**Windows Server 2008 R2, Windows Server 2008 and Windows Server 2003:** This writer is not supported.</span></span>

## <a name="distributed-file-system-replication-dfsr"></a><span data-ttu-id="8aa49-221">Sistema de replicación de archivos distribuido (DFSR)</span><span class="sxs-lookup"><span data-stu-id="8aa49-221">Distributed File System Replication (DFSR)</span></span>

<span data-ttu-id="8aa49-222">El componente siguiente incluye un VSS Writer: [replicación de sistema de archivos distribuido (DFSR)](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders)</span><span class="sxs-lookup"><span data-stu-id="8aa49-222">The following component includes a VSS writer: [Distributed File System Replication (DFSR)](/previous-versions/windows/desktop/dfsr/dfsr-replicated-folders)</span></span>

<span data-ttu-id="8aa49-223">**Windows Vista, Windows Server 2003 y Windows XP:** Este escritor no se admite hasta Windows Vista con SP1 y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8aa49-223">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span>

## <a name="dynamic-host-configuration-protocol-dhcp-writer"></a><span data-ttu-id="8aa49-224">Escritor del Protocolo de configuración dinámica de host (DHCP)</span><span class="sxs-lookup"><span data-stu-id="8aa49-224">Dynamic Host Configuration Protocol (DHCP) Writer</span></span>

<span data-ttu-id="8aa49-225">Este escritor es responsable de enumerar los archivos necesarios para el rol de servidor DHCP.</span><span class="sxs-lookup"><span data-stu-id="8aa49-225">This writer is responsible for enumerating files required for the DHCP server role.</span></span> <span data-ttu-id="8aa49-226">Este sistema de escritura es un escritor de la caja para las versiones del sistema operativo Windows Server; no se incluye en el cliente de Windows.</span><span class="sxs-lookup"><span data-stu-id="8aa49-226">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="8aa49-227">La cadena de nombre de escritor para este escritor es "DHCP jet Writer".</span><span class="sxs-lookup"><span data-stu-id="8aa49-227">The writer name string for this writer is "Dhcp Jet Writer".</span></span>

<span data-ttu-id="8aa49-228">El identificador del escritor de este escritor es BE9AC81E-3619-421F-920F-4C6FEA9E93AD.</span><span class="sxs-lookup"><span data-stu-id="8aa49-228">The writer ID for this writer is BE9AC81E-3619-421F-920F-4C6FEA9E93AD.</span></span>

## <a name="file-replication-service-frs"></a><span data-ttu-id="8aa49-229">Servicio de replicación de archivos (FRS)</span><span class="sxs-lookup"><span data-stu-id="8aa49-229">File Replication Service (FRS)</span></span>

<span data-ttu-id="8aa49-230">El escritor del servicio de replicación de archivos se documenta en [realizar copias de seguridad y restaurar una FRS-Replicated carpeta Sysvol](backing-up-and-restoring-an-frs-replicated-sysvol-folder.md).</span><span class="sxs-lookup"><span data-stu-id="8aa49-230">The File Replication Service writer is documented in [Backing Up and Restoring an FRS-Replicated SYSVOL Folder](backing-up-and-restoring-an-frs-replicated-sysvol-folder.md).</span></span>

<span data-ttu-id="8aa49-231">**Windows Vista, Windows Server 2003 y Windows XP:** Este escritor no se admite hasta Windows Vista con SP1 y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8aa49-231">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span>

## <a name="file-server-resource-manager-fsrm-writer"></a><span data-ttu-id="8aa49-232">Escritor de Administrador de recursos de servidor de archivos (FSRM)</span><span class="sxs-lookup"><span data-stu-id="8aa49-232">File Server Resource Manager (FSRM) Writer</span></span>

<span data-ttu-id="8aa49-233">Este sistema de escritura enumera los archivos de configuración de FSRM que se usan para la copia de seguridad del estado del sistema.</span><span class="sxs-lookup"><span data-stu-id="8aa49-233">This writer enumerates the FSRM configuration files that are used for system state backup.</span></span> <span data-ttu-id="8aa49-234">Durante las operaciones de restauración, se evitan los cambios en la configuración de FSRM y se detiene temporalmente la aplicación de cuotas y filtros de archivos.</span><span class="sxs-lookup"><span data-stu-id="8aa49-234">During restore operations it prevents changes in FSRM configuration and temporarily halts enforcement of quotas and file screens.</span></span> <span data-ttu-id="8aa49-235">Una vez finalizada la restauración, el escritor actualiza FSRM con la configuración que se restauró.</span><span class="sxs-lookup"><span data-stu-id="8aa49-235">After the restore is complete, the writer refreshes FSRM with the configuration that was restored.</span></span> <span data-ttu-id="8aa49-236">Este escritor solo está presente cuando FSRM (parte del rol servicios de archivo) está instalado y en ejecución.</span><span class="sxs-lookup"><span data-stu-id="8aa49-236">This writer is only present when FSRM (part of File Services role) is both installed and running.</span></span> <span data-ttu-id="8aa49-237">Este sistema de escritura es un escritor de la caja para las versiones del sistema operativo Windows Server; no se incluye en el cliente de Windows.</span><span class="sxs-lookup"><span data-stu-id="8aa49-237">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="8aa49-238">**Windows Server 2003:** Este escritor no se admite hasta Windows Server 2003 R2.</span><span class="sxs-lookup"><span data-stu-id="8aa49-238">**Windows Server 2003:** This writer is not supported until Windows Server 2003 R2.</span></span>

<span data-ttu-id="8aa49-239">La cadena de nombre de escritor para este escritor es "FSRM Writer".</span><span class="sxs-lookup"><span data-stu-id="8aa49-239">The writer name string for this writer is "FSRM Writer".</span></span>

<span data-ttu-id="8aa49-240">El identificador del escritor de este escritor es 12CE4370-5BB7-4C58-A76A-E5D5097E3674.</span><span class="sxs-lookup"><span data-stu-id="8aa49-240">The writer ID for this writer is 12CE4370-5BB7-4C58-A76A-E5D5097E3674.</span></span>

## <a name="hyper-v-writer"></a><span data-ttu-id="8aa49-241">Escritor de Hyper-V</span><span class="sxs-lookup"><span data-stu-id="8aa49-241">Hyper-V Writer</span></span>

<span data-ttu-id="8aa49-242">La VSS Writer de Hyper-V se documenta en la documentación de la API de [Hyper-v](/previous-versions/windows/desktop/virtual/backing-up-and-restoring-virtual-machines) .</span><span class="sxs-lookup"><span data-stu-id="8aa49-242">The Hyper-V VSS writer is documented in the [Hyper-V](/previous-versions/windows/desktop/virtual/backing-up-and-restoring-virtual-machines) API documentation.</span></span> <span data-ttu-id="8aa49-243">Este sistema de escritura es un escritor de la caja para las versiones del sistema operativo Windows Server; no se incluye en el cliente de Windows.</span><span class="sxs-lookup"><span data-stu-id="8aa49-243">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="8aa49-244">**Windows Server 2003:** Este escritor no se admite hasta Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8aa49-244">**Windows Server 2003:** This writer is not supported until Windows Server 2008.</span></span>

## <a name="iis-configuration-writer"></a><span data-ttu-id="8aa49-245">Escritor de configuración de IIS</span><span class="sxs-lookup"><span data-stu-id="8aa49-245">IIS Configuration Writer</span></span>

<span data-ttu-id="8aa49-246">El escritor de configuración de IIS es responsable de enumerar los archivos de configuración de IIS.</span><span class="sxs-lookup"><span data-stu-id="8aa49-246">The IIS configuration writer is responsible for enumerating the IIS configuration files.</span></span>

<span data-ttu-id="8aa49-247">**Windows Vista, Windows Server 2003 y Windows XP:** Este escritor no se admite hasta Windows Vista con SP1 y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8aa49-247">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span> <span data-ttu-id="8aa49-248">Los solicitantes son necesarios para realizar una copia de seguridad de los archivos de configuración de IIS, incluido el archivo de machine.config de .NET FX o el archivo de web.config raíz ASP.NET.</span><span class="sxs-lookup"><span data-stu-id="8aa49-248">Requesters are required to back up the IIS configuration files, including the .NET FX machine.config file or the ASP.NET root web.config file.</span></span>

<span data-ttu-id="8aa49-249">Este sistema de escritura no realiza una copia de seguridad del archivo de machine.config de .NET FX o del archivo de web.config raíz ASP.NET porque el sistema de escritura del sistema enumera estos archivos.</span><span class="sxs-lookup"><span data-stu-id="8aa49-249">This writer does not back up the .NET FX machine.config file or the ASP.NET root web.config file because these files are enumerated by the System Writer.</span></span>

<span data-ttu-id="8aa49-250">Este escritor realiza una copia de seguridad de todos los archivos que se encuentran en el esquema de configuración% WINDIR% \\ system32 \\ Inetsrv y en los directorios de \\ \\ configuración% WINDIR% \\ system32 \\ Inetsrv \\ , excepto los archivos enumerados por el escritor del sistema.</span><span class="sxs-lookup"><span data-stu-id="8aa49-250">This writer backs up all files that are in the %windir%\\system32\\inetsrv\\config\\schema and %windir%\\system32\\inetsrv\\config directories, except for files that are enumerated by the System Writer.</span></span>

<span data-ttu-id="8aa49-251">El ID. de escritor del escritor de configuración de IIS es 2A40FD15-DFCA-4aa8-A654-1F8C654603F6.</span><span class="sxs-lookup"><span data-stu-id="8aa49-251">The writer ID for the IIS configuration writer is 2A40FD15-DFCA-4aa8-A654-1F8C654603F6.</span></span>

## <a name="iis-metabase-writer"></a><span data-ttu-id="8aa49-252">Escritor de metabase de IIS</span><span class="sxs-lookup"><span data-stu-id="8aa49-252">IIS Metabase Writer</span></span>

<span data-ttu-id="8aa49-253">El escritor de la metabase de Internet Information Server (IIS) es responsable de enumerar el archivo de la metabase de IIS.</span><span class="sxs-lookup"><span data-stu-id="8aa49-253">The Internet Information Server (IIS) metabase writer is responsible for enumerating the IIS metabase file.</span></span>

<span data-ttu-id="8aa49-254">**Windows Vista, Windows Server 2003 y Windows XP:** Este escritor no se admite hasta Windows Vista con SP1 y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8aa49-254">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span> <span data-ttu-id="8aa49-255">Los solicitantes son necesarios para realizar una copia de seguridad del archivo de la metabase de IIS.</span><span class="sxs-lookup"><span data-stu-id="8aa49-255">Requesters are required to back up the IIS metabase file.</span></span>

<span data-ttu-id="8aa49-256">El ID. de escritor del escritor de la metabase de IIS es 59B1f0CF-90EF-465F-9609-6CA8B2938366.</span><span class="sxs-lookup"><span data-stu-id="8aa49-256">The writer ID for the IIS metabase writer is 59B1f0CF-90EF-465F-9609-6CA8B2938366.</span></span>

## <a name="microsoft-message-queuing-msmq-writer"></a><span data-ttu-id="8aa49-257">Escritor de Microsoft Message Queuing (MSMQ)</span><span class="sxs-lookup"><span data-stu-id="8aa49-257">Microsoft Message Queuing (MSMQ) Writer</span></span>

<span data-ttu-id="8aa49-258">Este escritor informa de los archivos de datos de Microsoft Message Queuing (MSMQ).</span><span class="sxs-lookup"><span data-stu-id="8aa49-258">This writer reports the Microsoft Message Queuing (MSMQ) data files.</span></span>

<span data-ttu-id="8aa49-259">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP:** No se admite este escritor.</span><span class="sxs-lookup"><span data-stu-id="8aa49-259">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8aa49-260">La cadena de nombre de escritor para este escritor es "MSMQ Writer (*SvcName*)", donde *SvcName* es el nombre del servicio de MSMQ con el que está asociado el escritor.</span><span class="sxs-lookup"><span data-stu-id="8aa49-260">The writer name string for this writer is "MSMQ Writer (*SvcName*)", where *SvcName* is the name of the MSMQ service the writer is associated with.</span></span> <span data-ttu-id="8aa49-261">En la instalación predeterminada, el nombre del servicio es "MSMQ".</span><span class="sxs-lookup"><span data-stu-id="8aa49-261">For default installation, the service name is "MSMQ".</span></span> <span data-ttu-id="8aa49-262">En el caso de las instancias en clúster, el nombre del servicio es MSMQ $*ResourceName*, donde *ResourceName* es el nombre del recurso de MSMQ agrupado.</span><span class="sxs-lookup"><span data-stu-id="8aa49-262">For clustered instances, the service name is MSMQ$*ResourceName*, where *ResourceName* is the clustered MSMQ resource name.</span></span>

<span data-ttu-id="8aa49-263">El identificador del escritor de este escritor es 7E47B561-971A-46E6-96B9-696EEAA53B2A.</span><span class="sxs-lookup"><span data-stu-id="8aa49-263">The writer ID for this writer is 7E47B561-971A-46E6-96B9-696EEAA53B2A.</span></span>

## <a name="mssearch-service-writer"></a><span data-ttu-id="8aa49-264">Escritor del servicio MSSearch</span><span class="sxs-lookup"><span data-stu-id="8aa49-264">MSSearch Service Writer</span></span>

<span data-ttu-id="8aa49-265">Este escritor existe para eliminar los archivos de índice de búsqueda de instantáneas después de crearlos.</span><span class="sxs-lookup"><span data-stu-id="8aa49-265">This writer exists to delete search index files from shadow copies after creation.</span></span> <span data-ttu-id="8aa49-266">Esto se hace para minimizar el impacto de la e/s de copia en escritura durante la e/s normal en estos archivos en el volumen de copia sombra.</span><span class="sxs-lookup"><span data-stu-id="8aa49-266">This is done to minimize the impact of Copy-on-Write I/O during regular I/O on these files on the shadow-copied volume.</span></span>

<span data-ttu-id="8aa49-267">**Windows Server 2003:** No se admite este escritor.</span><span class="sxs-lookup"><span data-stu-id="8aa49-267">**Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="8aa49-268">Para instalar este escritor en el servidor, debe instalar el rol servicios de archivo y habilitar el Search Service de Windows.</span><span class="sxs-lookup"><span data-stu-id="8aa49-268">To install this writer on the server, you must install the File Services role and enable the Windows Search Service.</span></span>

<span data-ttu-id="8aa49-269">La cadena de nombre de escritor para este escritor es "MSSearch Service Writer".</span><span class="sxs-lookup"><span data-stu-id="8aa49-269">The writer name string for this writer is "MSSearch Service Writer".</span></span>

<span data-ttu-id="8aa49-270">El ID. de escritor del escritor del servicio MSSearch es CD3F2362-8BEF-46C7-9181-D62844CDC0B2.</span><span class="sxs-lookup"><span data-stu-id="8aa49-270">The writer ID for the MSSearch service writer is CD3F2362-8BEF-46C7-9181-D62844CDC0B2.</span></span>

## <a name="nps-vss-writer"></a><span data-ttu-id="8aa49-271">VSS Writer de NPS</span><span class="sxs-lookup"><span data-stu-id="8aa49-271">NPS VSS Writer</span></span>

<span data-ttu-id="8aa49-272">El escritor de NPS es responsable de enumerar los archivos de configuración del servidor de directivas de redes (NPS) para los servidores que tienen instalado el rol servicios de acceso y directivas de redes.</span><span class="sxs-lookup"><span data-stu-id="8aa49-272">The NPS writer is responsible for enumerating the Network Policy Server (NPS) configuration files for servers that have the Network Policy and Access Services role installed.</span></span>

<span data-ttu-id="8aa49-273">**Windows Vista, Windows Server 2003 y Windows XP:** Este escritor no se admite hasta Windows Vista con SP1 y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8aa49-273">**Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported until Windows Vista with SP1 and Windows Server 2008.</span></span>

<span data-ttu-id="8aa49-274">La cadena de nombre de escritor para este escritor es "VSS VSS Writer".</span><span class="sxs-lookup"><span data-stu-id="8aa49-274">The writer name string for this writer is "NPS VSS Writer".</span></span>

<span data-ttu-id="8aa49-275">El identificador de escritor del VSS Writer NPS es 0x35E81631-13E1-48DB-97FC-D5BC721BB18A.</span><span class="sxs-lookup"><span data-stu-id="8aa49-275">The writer ID for the NPS VSS writer is 0x35E81631-13E1-48DB-97FC-D5BC721BB18A.</span></span>

## <a name="performance-counters-writer"></a><span data-ttu-id="8aa49-276">Escritor de contadores de rendimiento</span><span class="sxs-lookup"><span data-stu-id="8aa49-276">Performance Counters Writer</span></span>

<span data-ttu-id="8aa49-277">Este sistema de escritura informa de los archivos de configuración del contador de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="8aa49-277">This writer reports the performance counter configuration files.</span></span> <span data-ttu-id="8aa49-278">Estos archivos solo se modifican durante la instalación de la aplicación y se deben realizar copias de seguridad y restaurar durante las copias de seguridad y restauraciones del estado del sistema.</span><span class="sxs-lookup"><span data-stu-id="8aa49-278">These files are only modified during application installation and should be backed up and restored during system state backups and restores.</span></span>

<span data-ttu-id="8aa49-279">**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** No se admite este escritor.</span><span class="sxs-lookup"><span data-stu-id="8aa49-279">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span> <span data-ttu-id="8aa49-280">Los solicitantes son necesarios para realizar una copia de seguridad manual de estos archivos.</span><span class="sxs-lookup"><span data-stu-id="8aa49-280">Requesters are required to back up these files manually.</span></span> <span data-ttu-id="8aa49-281">(Consulte [copia de seguridad y restauración del estado del sistema](locating-additional-system-files.md)).</span><span class="sxs-lookup"><span data-stu-id="8aa49-281">(See [Backing Up and Restoring System State](locating-additional-system-files.md).)</span></span>

<span data-ttu-id="8aa49-282">La cadena de nombre de escritor para este sistema de escritura es "escritor de contadores de rendimiento".</span><span class="sxs-lookup"><span data-stu-id="8aa49-282">The writer name string for this writer is "Performance Counters Writer".</span></span>

<span data-ttu-id="8aa49-283">El ID. de escritor del escritor de contadores de rendimiento es 0BADA1DE-01A9-4625-8278-69E735F39DD2.</span><span class="sxs-lookup"><span data-stu-id="8aa49-283">The writer ID for the Performance Counters Writer is 0BADA1DE-01A9-4625-8278-69E735F39DD2.</span></span>

## <a name="registry-writer"></a><span data-ttu-id="8aa49-284">Escritor del registro</span><span class="sxs-lookup"><span data-stu-id="8aa49-284">Registry Writer</span></span>

<span data-ttu-id="8aa49-285">El sistema de escritura del registro informa de los archivos de registro de Windows para habilitar las copias de seguridad en contexto y las restauraciones del registro.</span><span class="sxs-lookup"><span data-stu-id="8aa49-285">The registry writer is reports the Windows registry files to enable in-place backups and restores of the registry.</span></span> <span data-ttu-id="8aa49-286">No notifica subárboles de usuario.</span><span class="sxs-lookup"><span data-stu-id="8aa49-286">It does not report user hives.</span></span>

<span data-ttu-id="8aa49-287">**Windows Server 2003:** En Windows Server 2003, este sistema de escritura usa un archivo de repositorio intermedio (a veces denominado "archivo de prosección") para almacenar los datos del registro.</span><span class="sxs-lookup"><span data-stu-id="8aa49-287">**Windows Server 2003:** In Windows Server 2003, this writer uses an intermediate repository file (sometimes called a "spit file") to store registry data.</span></span> <span data-ttu-id="8aa49-288">(Consulte [operaciones de copia de seguridad y restauración del registro en VSS](registry-backup-and-restore-operations-under-vss.md)).</span><span class="sxs-lookup"><span data-stu-id="8aa49-288">(See [Registry Backup and Restore Operations Under VSS](registry-backup-and-restore-operations-under-vss.md).)</span></span>

<span data-ttu-id="8aa49-289">**Windows XP:** No se admite este escritor.</span><span class="sxs-lookup"><span data-stu-id="8aa49-289">**Windows XP:** This writer is not supported.</span></span> <span data-ttu-id="8aa49-290">(Consulte [operaciones de copia de seguridad y restauración del registro en VSS](registry-backup-and-restore-operations-under-vss.md)).</span><span class="sxs-lookup"><span data-stu-id="8aa49-290">(See [Registry Backup and Restore Operations Under VSS](registry-backup-and-restore-operations-under-vss.md).)</span></span>

<span data-ttu-id="8aa49-291">La cadena de nombre de escritor para este escritor es "escritor del registro".</span><span class="sxs-lookup"><span data-stu-id="8aa49-291">The writer name string for this writer is "Registry Writer".</span></span>

<span data-ttu-id="8aa49-292">El ID. de escritor del sistema de escritura del registro es AFBAB4A2-367D-4D15-A586-71DBB18F8485.</span><span class="sxs-lookup"><span data-stu-id="8aa49-292">The writer ID for the registry writer is AFBAB4A2-367D-4D15-A586-71DBB18F8485.</span></span>

## <a name="remote-desktop-services-terminal-services-gateway-vss-writer"></a><span data-ttu-id="8aa49-293">VSS Writer de puerta de enlace de Servicios de Escritorio remoto (Terminal Services)</span><span class="sxs-lookup"><span data-stu-id="8aa49-293">Remote Desktop Services (Terminal Services) Gateway VSS Writer</span></span>

<span data-ttu-id="8aa49-294">Este escritor es responsable de enumerar los archivos de puerta de enlace de Servicios de Escritorio remoto (Terminal Services) para los servidores que tienen Escritorio remoto puerta de enlace, un subrol de Servicios de Escritorio remoto rol, instalado.</span><span class="sxs-lookup"><span data-stu-id="8aa49-294">This writer is responsible for enumerating the Remote Desktop Services (Terminal Services) Gateway files for servers that have Remote Desktop Gateway, a subrole of Remote Desktop Services role, installed.</span></span>

<span data-ttu-id="8aa49-295">**Windows Server 2003:** No se admite este escritor.</span><span class="sxs-lookup"><span data-stu-id="8aa49-295">**Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="8aa49-296">Este sistema de escritura es un escritor de la caja para las versiones del sistema operativo Windows Server; no se incluye en el cliente de Windows.</span><span class="sxs-lookup"><span data-stu-id="8aa49-296">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="8aa49-297">La puerta de enlace de Servicios de Escritorio remoto depende de varias claves del registro de las que se realiza una copia de seguridad y, por tanto, debe realizarse una copia de seguridad y restaurarse junto con el registro.</span><span class="sxs-lookup"><span data-stu-id="8aa49-297">The Remote Desktop Services Gateway depends on several registry keys being backed up and therefore needs to be backed up and restored together with the registry.</span></span>

<span data-ttu-id="8aa49-298">La cadena de nombre de escritor para este escritor es "escritor de puerta de enlace de TS".</span><span class="sxs-lookup"><span data-stu-id="8aa49-298">The writer name string for this writer is "TS Gateway Writer".</span></span>

<span data-ttu-id="8aa49-299">El identificador del escritor de este escritor es 368753EC-572E-4FC7-B4B9-CCD9BDC624CB.</span><span class="sxs-lookup"><span data-stu-id="8aa49-299">The writer ID for this writer is 368753EC-572E-4FC7-B4B9-CCD9BDC624CB.</span></span>

## <a name="remote-desktop-services-terminal-services-licensing-vss-writer"></a><span data-ttu-id="8aa49-300">Escritor de VSS para licencias de Servicios de Escritorio remoto (Terminal Services)</span><span class="sxs-lookup"><span data-stu-id="8aa49-300">Remote Desktop Services (Terminal Services) Licensing VSS Writer</span></span>

<span data-ttu-id="8aa49-301">Este escritor es responsable de enumerar los archivos de licencias de Servicios de Escritorio remoto (licencias de escritorio remoto) o licencias de Terminal Services (licencias de TS) para los servidores que tienen instalado Escritorio remoto licencias, un subrol de Servicios de Escritorio remoto rol.</span><span class="sxs-lookup"><span data-stu-id="8aa49-301">This writer is responsible for enumerating the Remote Desktop Services Licensing (RD Licensing) or Terminal Services Licensing (TS Licensing) files for servers that have Remote Desktop Licensing, a subrole of Remote Desktop Services role, installed.</span></span>

<span data-ttu-id="8aa49-302">**Windows Server 2003:** No se admite este escritor.</span><span class="sxs-lookup"><span data-stu-id="8aa49-302">**Windows Server 2003:** This writer is not supported.</span></span>

<span data-ttu-id="8aa49-303">Este sistema de escritura es un escritor de la caja para las versiones del sistema operativo Windows Server; no se incluye en el cliente de Windows.</span><span class="sxs-lookup"><span data-stu-id="8aa49-303">This writer is an in-box writer for Windows Server operating system versions; it does not ship in Windows Client.</span></span>

<span data-ttu-id="8aa49-304">La concesión de licencias de Servicios de Escritorio remoto depende de varias claves del registro de las que se realiza una copia de seguridad y, por tanto, debe realizarse una copia de seguridad y restaurarse junto con el registro.</span><span class="sxs-lookup"><span data-stu-id="8aa49-304">Remote Desktop Services Licensing depends on several registry keys being backed up and therefore needs to be backed up and restored together with the registry.</span></span>

<span data-ttu-id="8aa49-305">La cadena de nombre de escritor para este escritor es "TermServLicensing".</span><span class="sxs-lookup"><span data-stu-id="8aa49-305">The writer name string for this writer is "TermServLicensing".</span></span>

<span data-ttu-id="8aa49-306">El identificador del escritor de este escritor es 5382579C-98DF-47A7-AC6C-98A6D7106E09.</span><span class="sxs-lookup"><span data-stu-id="8aa49-306">The writer ID for this writer is 5382579C-98DF-47A7-AC6C-98A6D7106E09.</span></span>

## <a name="shadow-copy-optimization-writer"></a><span data-ttu-id="8aa49-307">Escritor de optimización de instantáneas</span><span class="sxs-lookup"><span data-stu-id="8aa49-307">Shadow Copy Optimization Writer</span></span>

<span data-ttu-id="8aa49-308">Este escritor elimina determinados archivos de instantáneas de volumen.</span><span class="sxs-lookup"><span data-stu-id="8aa49-308">This writer deletes certain files from volume shadow copies.</span></span> <span data-ttu-id="8aa49-309">Esto se hace para minimizar el impacto de la e/s de copia en escritura durante la e/s normal en estos archivos en el volumen de copia sombra.</span><span class="sxs-lookup"><span data-stu-id="8aa49-309">This is done to minimize the impact of Copy-on-Write I/O during regular I/O on these files on the shadow-copied volume.</span></span> <span data-ttu-id="8aa49-310">Los archivos que se eliminan suelen ser archivos temporales que no contienen el estado del usuario o del sistema.</span><span class="sxs-lookup"><span data-stu-id="8aa49-310">The files that are deleted are typically temporary files or files that do not contain user or system state.</span></span>

<span data-ttu-id="8aa49-311">**Windows Server 2003 y Windows XP:** No se admite este escritor.</span><span class="sxs-lookup"><span data-stu-id="8aa49-311">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8aa49-312">La cadena de nombre de escritor para este escritor es "escritor de optimización de instantáneas".</span><span class="sxs-lookup"><span data-stu-id="8aa49-312">The writer name string for this writer is "Shadow Copy Optimization Writer".</span></span>

<span data-ttu-id="8aa49-313">El ID. de escritor del escritor de optimización de instantáneas es 4DC3BDD4-AB48-4D07-ADB0-3BEE2926FD7F.</span><span class="sxs-lookup"><span data-stu-id="8aa49-313">The writer ID for the shadow copy optimization writer is 4DC3BDD4-AB48-4D07-ADB0-3BEE2926FD7F.</span></span>

## <a name="sync-share-service-writer"></a><span data-ttu-id="8aa49-314">Escritor de servicio de recurso compartido de sincronización</span><span class="sxs-lookup"><span data-stu-id="8aa49-314">Sync Share Service Writer</span></span>

<span data-ttu-id="8aa49-315">**Windows Server 2012 R2:** Este escritor está incluido en Windows Server 2012 R2 y versiones de servidor más recientes.</span><span class="sxs-lookup"><span data-stu-id="8aa49-315">**Windows Server 2012 R2:** This writer is included with Windows Server 2012 R2 and newer server versions.</span></span> <span data-ttu-id="8aa49-316">No es compatible con las versiones de escritorio.</span><span class="sxs-lookup"><span data-stu-id="8aa49-316">It is not compatible with desktop versions.</span></span>

<span data-ttu-id="8aa49-317">Este escritor es responsable de enumerar los recursos compartidos de sincronización en los servidores que tienen instalado el servicio de recurso compartido de sincronización y para garantizar que los metadatos y los datos sigan siendo coherentes durante las copias de seguridad y restauración.</span><span class="sxs-lookup"><span data-stu-id="8aa49-317">This writer is responsible for enumerating the sync shares on servers that have the Sync Share Service installed, and for ensuring that their metadata and data remain consistent during backup and restore.</span></span>

<span data-ttu-id="8aa49-318">Este escritor solo está presente cuando el servicio de recurso compartido de sincronización está instalado y en ejecución.</span><span class="sxs-lookup"><span data-stu-id="8aa49-318">This writer is only present when Sync Share Service is both installed and running.</span></span>

<span data-ttu-id="8aa49-319">Habrá un VSS Writer componente para cada recurso compartido de sincronización.</span><span class="sxs-lookup"><span data-stu-id="8aa49-319">There will be one VSS writer component for each sync share.</span></span> <span data-ttu-id="8aa49-320">Esto incluye los metadatos y las rutas de acceso de datos.</span><span class="sxs-lookup"><span data-stu-id="8aa49-320">This includes the metadata and data paths.</span></span> <span data-ttu-id="8aa49-321">Se debe hacer una copia de seguridad conjunta de ellas para mantener la coherencia.</span><span class="sxs-lookup"><span data-stu-id="8aa49-321">These must be backed up together for consistency.</span></span>

<span data-ttu-id="8aa49-322">La cadena de nombre de escritor es "Sync share Service VSS Writer".</span><span class="sxs-lookup"><span data-stu-id="8aa49-322">The writer name string is "Sync Share Service VSS writer".</span></span>

<span data-ttu-id="8aa49-323">El identificador del escritor es D46BF321-FDBA-4A35-8EC3-454DF03BC86A.</span><span class="sxs-lookup"><span data-stu-id="8aa49-323">The writer ID is D46BF321-FDBA-4A35-8EC3-454DF03BC86A.</span></span>

## <a name="system-writer"></a><span data-ttu-id="8aa49-324">Escritor del sistema</span><span class="sxs-lookup"><span data-stu-id="8aa49-324">System Writer</span></span>

<span data-ttu-id="8aa49-325">El escritor del sistema enumera todos los archivos binarios del sistema operativo y del controlador, y es necesario para una copia de seguridad del estado del sistema.</span><span class="sxs-lookup"><span data-stu-id="8aa49-325">The system writer enumerates all operating system and driver binaries and it is required for a system state backup.</span></span>

<span data-ttu-id="8aa49-326">**Windows Server 2003 y Windows XP:** No se admite este escritor.</span><span class="sxs-lookup"><span data-stu-id="8aa49-326">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8aa49-327">Este escritor se ejecuta como parte del servicio de servicios de cifrado (CryptSvc).</span><span class="sxs-lookup"><span data-stu-id="8aa49-327">This writer runs as part of the Cryptographic Services (CryptSvc) service.</span></span> <span data-ttu-id="8aa49-328">El escritor del sistema genera una lista de archivos que contiene los archivos siguientes:</span><span class="sxs-lookup"><span data-stu-id="8aa49-328">The system writer generates a file list that contains the following files:</span></span>

-   <span data-ttu-id="8aa49-329">Todos los archivos estáticos que se han instalado.</span><span class="sxs-lookup"><span data-stu-id="8aa49-329">All static files that have been installed.</span></span> <span data-ttu-id="8aa49-330">Un archivo estático es un archivo que aparece en el manifiesto del componente con el atributo de archivo **writeableType** establecido en "Static" o "".</span><span class="sxs-lookup"><span data-stu-id="8aa49-330">A static file is a file that is listed in the component manifest with the **writeableType** file attribute set to "static" or "".</span></span> <span data-ttu-id="8aa49-331">Los archivos estáticos incluyen todos los archivos protegidos por Protección de recursos de Windows (WRP).</span><span class="sxs-lookup"><span data-stu-id="8aa49-331">Static files include all files that are protected by Windows Resource Protection (WRP).</span></span> <span data-ttu-id="8aa49-332">Sin embargo, no todos los archivos estáticos son archivos protegidos por WRP.</span><span class="sxs-lookup"><span data-stu-id="8aa49-332">However, not all static files are WRP-protected files.</span></span> <span data-ttu-id="8aa49-333">Por ejemplo, los archivos de juego son estáticos pero no protegidos por WRP para que los administradores puedan cambiar la configuración del control parental.</span><span class="sxs-lookup"><span data-stu-id="8aa49-333">For example, game files are static but not WRP-protected so that administrators can change parental control settings.</span></span>
-   <span data-ttu-id="8aa49-334">El contenido del directorio de Windows en paralelo (WinSxS), incluidos todos los manifiestos, componentes opcionales y archivos Win32 de terceros.</span><span class="sxs-lookup"><span data-stu-id="8aa49-334">The contents of the Windows Side-by-Side (WinSxS) directory, including all manifests, optional components, and third-party Win32 files.</span></span>
    > [!Note]  
    > <span data-ttu-id="8aa49-335">Muchos de los archivos del directorio% WINDIR% \\ system32 son vínculos físicos a archivos del directorio WinSxS.</span><span class="sxs-lookup"><span data-stu-id="8aa49-335">Many of the files in the %windir%\\system32 directory are hard links to files in the WinSxS directory.</span></span>

     

-   <span data-ttu-id="8aa49-336">Todos los archivos PnP para los controladores instalados (propiedad de PnP).</span><span class="sxs-lookup"><span data-stu-id="8aa49-336">All PnP files for installed drivers (owned by PnP).</span></span>
-   <span data-ttu-id="8aa49-337">Todos los servicios de modo de usuario y controladores no PnP.</span><span class="sxs-lookup"><span data-stu-id="8aa49-337">All user-mode services and non-PnP drivers.</span></span>
-   <span data-ttu-id="8aa49-338">Todos los catálogos propiedad de CryptSvc.</span><span class="sxs-lookup"><span data-stu-id="8aa49-338">All catalogs owned by CryptSvc.</span></span>

<span data-ttu-id="8aa49-339">La aplicación de restauración es responsable de la colocación de los archivos y del registro y de la configuración de las ACL para que coincidan con la instantánea del sistema.</span><span class="sxs-lookup"><span data-stu-id="8aa49-339">The restore application is responsible for laying down the files and registry and setting ACLs to match the system shadow copy.</span></span> <span data-ttu-id="8aa49-340">También se deben crear los vínculos físicos adecuados para que una restauración del estado del sistema se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="8aa49-340">The appropriate hard links must also be created for a system state restore to succeed.</span></span>

<span data-ttu-id="8aa49-341">La cadena de nombre de escritor para este escritor es "escritor del sistema".</span><span class="sxs-lookup"><span data-stu-id="8aa49-341">The writer name string for this writer is "System Writer".</span></span>

<span data-ttu-id="8aa49-342">El ID. de escritor del escritor del sistema es E8132975-6F93-4464-A53E-1050253AE220.</span><span class="sxs-lookup"><span data-stu-id="8aa49-342">The writer ID for the system writer is E8132975-6F93-4464-A53E-1050253AE220.</span></span>

## <a name="task-scheduler-writer"></a><span data-ttu-id="8aa49-343">Escritor de Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="8aa49-343">Task Scheduler Writer</span></span>

<span data-ttu-id="8aa49-344">Este escritor informa de los archivos de tareas del programador de tareas.</span><span class="sxs-lookup"><span data-stu-id="8aa49-344">This writer reports the task scheduler's task files.</span></span>

<span data-ttu-id="8aa49-345">**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** No se admite este escritor.</span><span class="sxs-lookup"><span data-stu-id="8aa49-345">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span> <span data-ttu-id="8aa49-346">Los solicitantes son necesarios para realizar una copia de seguridad manual de estos archivos.</span><span class="sxs-lookup"><span data-stu-id="8aa49-346">Requesters are required to back up these files manually.</span></span> <span data-ttu-id="8aa49-347">(Consulte [copia de seguridad y restauración del estado del sistema](locating-additional-system-files.md)).</span><span class="sxs-lookup"><span data-stu-id="8aa49-347">(See [Backing Up and Restoring System State](locating-additional-system-files.md).)</span></span>

<span data-ttu-id="8aa49-348">La cadena de nombre de escritor para este escritor es "Programador de tareas redactor".</span><span class="sxs-lookup"><span data-stu-id="8aa49-348">The writer name string for this writer is "Task Scheduler Writer".</span></span>

<span data-ttu-id="8aa49-349">El ID. de escritor del escritor es D61D61C8-D73A-4EEE-8CDD-F6F9786B7124.</span><span class="sxs-lookup"><span data-stu-id="8aa49-349">The writer ID for the writer is D61D61C8-D73A-4EEE-8CDD-F6F9786B7124.</span></span>

## <a name="vss-metadata-store-writer"></a><span data-ttu-id="8aa49-350">Escritor de almacén de metadatos de VSS</span><span class="sxs-lookup"><span data-stu-id="8aa49-350">VSS Metadata Store Writer</span></span>

<span data-ttu-id="8aa49-351">Este escritor notifica los archivos de metadatos de escritura para todos los escritores de VSS Express.</span><span class="sxs-lookup"><span data-stu-id="8aa49-351">This writer reports the writer metadata files for all VSS express writers.</span></span>

<span data-ttu-id="8aa49-352">**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** No se admite este escritor.</span><span class="sxs-lookup"><span data-stu-id="8aa49-352">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8aa49-353">La cadena de nombre de escritor para este escritor es "VSS Express Writer Metadata Store Writer".</span><span class="sxs-lookup"><span data-stu-id="8aa49-353">The writer name string for this writer is "VSS Express Writer Metadata Store Writer".</span></span>

<span data-ttu-id="8aa49-354">El ID. de escritor del escritor es 75DFB225-E2E4-4D39-9AC9-FFAFF65DDF06.</span><span class="sxs-lookup"><span data-stu-id="8aa49-354">The writer ID for the writer is 75DFB225-E2E4-4D39-9AC9-FFAFF65DDF06.</span></span>

## <a name="windows-deployment-services-wds-writer"></a><span data-ttu-id="8aa49-355">Escritor de servicios de implementación de Windows (WDS)</span><span class="sxs-lookup"><span data-stu-id="8aa49-355">Windows Deployment Services (WDS) Writer</span></span>

<span data-ttu-id="8aa49-356">Este escritor informa de los archivos de datos de servicios de implementación de Windows (WDS).</span><span class="sxs-lookup"><span data-stu-id="8aa49-356">This writer reports the Windows Deployment Services (WDS) data files.</span></span>

<span data-ttu-id="8aa49-357">**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** No se admite este escritor.</span><span class="sxs-lookup"><span data-stu-id="8aa49-357">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8aa49-358">La cadena de nombre de escritor para este escritor es "WDS VSS Writer".</span><span class="sxs-lookup"><span data-stu-id="8aa49-358">The writer name string for this writer is "WDS VSS Writer".</span></span>

<span data-ttu-id="8aa49-359">El identificador del escritor de este escritor es 82CB5521-68DB-4626-83A4-7FC6F88853E9.</span><span class="sxs-lookup"><span data-stu-id="8aa49-359">The writer ID for this writer is 82CB5521-68DB-4626-83A4-7FC6F88853E9.</span></span>

## <a name="windows-internal-database-wid-writer"></a><span data-ttu-id="8aa49-360">Escritor de Windows Internal Database (WID)</span><span class="sxs-lookup"><span data-stu-id="8aa49-360">Windows Internal Database (WID) Writer</span></span>

<span data-ttu-id="8aa49-361">Este escritor informa de los archivos de datos de Windows Internal Database (WID).</span><span class="sxs-lookup"><span data-stu-id="8aa49-361">This writer reports the Windows Internal Database (WID) data files.</span></span>

<span data-ttu-id="8aa49-362">**Windows server 2008 R2, Windows 7, Windows server 2008, Windows Vista, Windows Server 2003 y Windows XP:** No se admite este escritor.</span><span class="sxs-lookup"><span data-stu-id="8aa49-362">**Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8aa49-363">La cadena de nombre de escritor para este escritor es "WIDWriter".</span><span class="sxs-lookup"><span data-stu-id="8aa49-363">The writer name string for this writer is "WIDWriter".</span></span>

<span data-ttu-id="8aa49-364">El identificador del escritor de este escritor es 8D5194E1-E455-434A-B2E5-51296CCE67DF.</span><span class="sxs-lookup"><span data-stu-id="8aa49-364">The writer ID for this writer is 8D5194E1-E455-434A-B2E5-51296CCE67DF.</span></span>

## <a name="windows-internet-name-service-wins-writer"></a><span data-ttu-id="8aa49-365">Escritor del servicio de nombres Internet de Windows (WINS)</span><span class="sxs-lookup"><span data-stu-id="8aa49-365">Windows Internet Name Service (WINS) Writer</span></span>

<span data-ttu-id="8aa49-366">Este escritor es responsable de enumerar los archivos necesarios para WINS.</span><span class="sxs-lookup"><span data-stu-id="8aa49-366">This writer is responsible for enumerating files required for WINS.</span></span>

<span data-ttu-id="8aa49-367">**Windows XP:** No se admite este escritor.</span><span class="sxs-lookup"><span data-stu-id="8aa49-367">**Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8aa49-368">La cadena de nombre de escritor para este escritor es "WINS jet Writer".</span><span class="sxs-lookup"><span data-stu-id="8aa49-368">The writer name string for this writer is "WINS Jet Writer".</span></span>

<span data-ttu-id="8aa49-369">El identificador del escritor de este escritor es F08C1483-8407-4A26-8C26-6C267A629741.</span><span class="sxs-lookup"><span data-stu-id="8aa49-369">The writer ID for this writer is F08C1483-8407-4A26-8C26-6C267A629741.</span></span>

## <a name="wmi-writer"></a><span data-ttu-id="8aa49-370">Escritor WMI</span><span class="sxs-lookup"><span data-stu-id="8aa49-370">WMI Writer</span></span>

<span data-ttu-id="8aa49-371">Este escritor se utiliza para identificar el estado específico de WMI y los datos durante las operaciones de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="8aa49-371">This writer is used for identifying WMI-specific state and data during backup operations.</span></span> <span data-ttu-id="8aa49-372">Los datos incluyen archivos del repositorio WBEM.</span><span class="sxs-lookup"><span data-stu-id="8aa49-372">The data includes files from the WBEM repository.</span></span>

<span data-ttu-id="8aa49-373">**Windows Server 2003 y Windows XP:** No se admite este escritor.</span><span class="sxs-lookup"><span data-stu-id="8aa49-373">**Windows Server 2003 and Windows XP:** This writer is not supported.</span></span>

<span data-ttu-id="8aa49-374">La cadena de nombre de escritor para este escritor es "escritor de WMI".</span><span class="sxs-lookup"><span data-stu-id="8aa49-374">The writer name string for this writer is "WMI Writer".</span></span>

<span data-ttu-id="8aa49-375">El identificador del escritor de este escritor es A6AD56C2-B509-4E6C-BB19-49D8F43532F0.</span><span class="sxs-lookup"><span data-stu-id="8aa49-375">The writer ID for this writer is A6AD56C2-B509-4E6C-BB19-49D8F43532F0.</span></span>

 

 
