---
description: Windows Server 2008.
ms.assetid: 2f7b62f8-ba1e-42d2-8872-38d4475e4a2a
title: Novedades de VSS en Windows Server 2008 y Windows Vista SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f053e327a7a54a9597bc06836b37c00effc62f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154326"
---
# <a name="whats-new-in-vss-in-windows-server-2008-and-windows-vista-sp1"></a><span data-ttu-id="5980b-103">Novedades de VSS en Windows Server 2008 y Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="5980b-103">What's New in VSS in Windows Server 2008 and Windows Vista SP1</span></span>

<span data-ttu-id="5980b-104">Windows Server 2008 y Windows Vista con Service Pack 1 (SP1) presentan los siguientes cambios en el Servicio de instantáneas de volumen.</span><span class="sxs-lookup"><span data-stu-id="5980b-104">Windows Server 2008 and Windows Vista with Service Pack 1 (SP1) introduce the following changes to the Volume Shadow Copy Service.</span></span>

> [!Note]  
> <span data-ttu-id="5980b-105">Todos los cambios de Windows Vista se aplican a Windows Server 2008 y Windows Vista con SP1.</span><span class="sxs-lookup"><span data-stu-id="5980b-105">All changes for Windows Vista apply to Windows Server 2008 and Windows Vista with SP1.</span></span> <span data-ttu-id="5980b-106">Para obtener más información sobre estos cambios, consulte [novedades de VSS en Windows Vista](what-s-new-in-vss-in-windows-vista.md).</span><span class="sxs-lookup"><span data-stu-id="5980b-106">For details on those changes, see [What's New in VSS in Windows Vista](what-s-new-in-vss-in-windows-vista.md).</span></span>

 

-   [<span data-ttu-id="5980b-107">Nuevas interfaces VSS</span><span class="sxs-lookup"><span data-stu-id="5980b-107">New VSS Interfaces</span></span>](#new-vss-interfaces)
-   [<span data-ttu-id="5980b-108">Nuevas enumeraciones de VSS</span><span class="sxs-lookup"><span data-stu-id="5980b-108">New VSS Enumerations</span></span>](#new-vss-enumerations)
-   [<span data-ttu-id="5980b-109">Nuevas estructuras de VSS</span><span class="sxs-lookup"><span data-stu-id="5980b-109">New VSS Structures</span></span>](#new-vss-structures)
-   [<span data-ttu-id="5980b-110">Modificaciones de la enumeración de VSS existentes</span><span class="sxs-lookup"><span data-stu-id="5980b-110">Existing VSS Enumeration Modifications</span></span>](#existing-vss-enumeration-modifications)
-   [<span data-ttu-id="5980b-111">Modificaciones de la interfaz de VSS existentes</span><span class="sxs-lookup"><span data-stu-id="5980b-111">Existing VSS Interface Modifications</span></span>](#existing-vss-interface-modifications)
-   [<span data-ttu-id="5980b-112">Nuevos escritores de VSS</span><span class="sxs-lookup"><span data-stu-id="5980b-112">New VSS Writers</span></span>](#new-vss-writers)

## <a name="new-vss-interfaces"></a><span data-ttu-id="5980b-113">Nuevas interfaces VSS</span><span class="sxs-lookup"><span data-stu-id="5980b-113">New VSS Interfaces</span></span>

<dl>

[<span data-ttu-id="5980b-114">**IVssDifferentialSoftwareSnapshotMgmt3**</span><span class="sxs-lookup"><span data-stu-id="5980b-114">**IVssDifferentialSoftwareSnapshotMgmt3**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt3)  
[<span data-ttu-id="5980b-115">**IVssHardwareSnapshotProviderEx**</span><span class="sxs-lookup"><span data-stu-id="5980b-115">**IVssHardwareSnapshotProviderEx**</span></span>](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)  
</dl>

## <a name="new-vss-enumerations"></a><span data-ttu-id="5980b-116">Nuevas enumeraciones de VSS</span><span class="sxs-lookup"><span data-stu-id="5980b-116">New VSS Enumerations</span></span>

<dl>

[<span data-ttu-id="5980b-117">**\_\_Opciones de hardware de VSS \_**</span><span class="sxs-lookup"><span data-stu-id="5980b-117">**\_VSS\_HARDWARE\_OPTIONS**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_hardware_options)  
[<span data-ttu-id="5980b-118">**\_error de protección de VSS \_**</span><span class="sxs-lookup"><span data-stu-id="5980b-118">**VSS\_PROTECTION\_FAULT**</span></span>](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_fault)  
[<span data-ttu-id="5980b-119">**\_nivel de protección de VSS \_**</span><span class="sxs-lookup"><span data-stu-id="5980b-119">**VSS\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/VsMgmt/ne-vsmgmt-vss_protection_level)  
</dl>

## <a name="new-vss-structures"></a><span data-ttu-id="5980b-120">Nuevas estructuras de VSS</span><span class="sxs-lookup"><span data-stu-id="5980b-120">New VSS Structures</span></span>

<dl>

[<span data-ttu-id="5980b-121">**\_información de \_ protección de volumen de VSS \_**</span><span class="sxs-lookup"><span data-stu-id="5980b-121">**VSS\_VOLUME\_PROTECTION\_INFO**</span></span>](/windows/desktop/api/VsMgmt/ns-vsmgmt-vss_volume_protection_info)  
</dl>

## <a name="existing-vss-enumeration-modifications"></a><span data-ttu-id="5980b-122">Modificaciones de la enumeración de VSS existentes</span><span class="sxs-lookup"><span data-stu-id="5980b-122">Existing VSS Enumeration Modifications</span></span>

<dl> <dt>

<span data-ttu-id="5980b-123"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) Enumeración de esquema de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="5980b-123"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS\_BACKUP\_SCHEMA**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="5980b-124"><span id="Added_value_"></span><span id="added_value_"></span><span id="ADDED_VALUE_"></span>Valor agregado:</span><span class="sxs-lookup"><span data-stu-id="5980b-124"><span id="Added_value_"></span><span id="added_value_"></span><span id="ADDED_VALUE_"></span>Added value:</span></span>
</dt> <dd>

<span data-ttu-id="5980b-125">VSS \_ BS \_ Writer \_ admite \_ \_ restauraciones en paralelo</span><span class="sxs-lookup"><span data-stu-id="5980b-125">VSS\_BS\_WRITER\_SUPPORTS\_PARALLEL\_RESTORES</span></span>

</dd> </dl> </dd> </dl>

<dl> <dt>

<span data-ttu-id="5980b-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Enumeración de [**\_ \_ atributos de \_ instantánea \_ de volumen de VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)</span><span class="sxs-lookup"><span data-stu-id="5980b-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="5980b-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valores agregados:</span><span class="sxs-lookup"><span data-stu-id="5980b-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="5980b-128">postinstantánea de \_ atributo VOLSNAP de VSS de VSS \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="5980b-128">VSS\_VOLSNAP\_ATTR\_DELAYED\_POSTSNAPSHOT</span></span>

<span data-ttu-id="5980b-129">\_recuperación de \_ TxF de atributo VOLSNAP \_ de VSS \_</span><span class="sxs-lookup"><span data-stu-id="5980b-129">VSS\_VOLSNAP\_ATTR\_TXF\_RECOVERY</span></span>

</dd> </dl> </dd> </dl>

## <a name="existing-vss-interface-modifications"></a><span data-ttu-id="5980b-130">Modificaciones de la interfaz de VSS existentes</span><span class="sxs-lookup"><span data-stu-id="5980b-130">Existing VSS Interface Modifications</span></span>

<dl> <dt>

<span data-ttu-id="5980b-131"><span id="IVssBackupComponentsEx2_interface"></span><span id="ivssbackupcomponentsex2_interface"></span><span id="IVSSBACKUPCOMPONENTSEX2_INTERFACE"></span>Interfaz [**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)</span><span class="sxs-lookup"><span data-stu-id="5980b-131"><span id="IVssBackupComponentsEx2_interface"></span><span id="ivssbackupcomponentsex2_interface"></span><span id="IVSSBACKUPCOMPONENTSEX2_INTERFACE"></span>[**IVssBackupComponentsEx2**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2) interface</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="5980b-132"><span id="Added_method_"></span><span id="added_method_"></span><span id="ADDED_METHOD_"></span>Método agregado:</span><span class="sxs-lookup"><span data-stu-id="5980b-132"><span id="Added_method_"></span><span id="added_method_"></span><span id="ADDED_METHOD_"></span>Added method:</span></span>
</dt> <dd>

[<span data-ttu-id="5980b-133">**BreakSnapshotSetEx**</span><span class="sxs-lookup"><span data-stu-id="5980b-133">**BreakSnapshotSetEx**</span></span>](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)

</dd> </dl> </dd> </dl>

## <a name="new-vss-writers"></a><span data-ttu-id="5980b-134">Nuevos escritores de VSS</span><span class="sxs-lookup"><span data-stu-id="5980b-134">New VSS Writers</span></span>

<span data-ttu-id="5980b-135">Windows Server 2008 y Windows Vista con SP1 presentan los siguientes escritores de VSS:</span><span class="sxs-lookup"><span data-stu-id="5980b-135">Windows Server 2008 and Windows Vista with SP1 introduce the following VSS writers:</span></span>

-   <span data-ttu-id="5980b-136">Escritor de configuración de IIS</span><span class="sxs-lookup"><span data-stu-id="5980b-136">IIS Configuration Writer</span></span>
-   <span data-ttu-id="5980b-137">Escritor de metabase de IIS</span><span class="sxs-lookup"><span data-stu-id="5980b-137">IIS Metabase Writer</span></span>
-   <span data-ttu-id="5980b-138">VSS Writer de NPS</span><span class="sxs-lookup"><span data-stu-id="5980b-138">NPS VSS Writer</span></span>
-   <span data-ttu-id="5980b-139">VSS Writer de puerta de enlace de Servicios de Escritorio remoto (Terminal Services)</span><span class="sxs-lookup"><span data-stu-id="5980b-139">Remote Desktop Services (Terminal Services) Gateway VSS Writer</span></span>
-   <span data-ttu-id="5980b-140">Escritor de VSS para licencias de Servicios de Escritorio remoto (Terminal Services)</span><span class="sxs-lookup"><span data-stu-id="5980b-140">Remote Desktop Services (Terminal Services) Licensing VSS Writer</span></span>

<span data-ttu-id="5980b-141">Estos escritores están documentados en [escritores de VSS en la caja](in-box-vss-writers.md).</span><span class="sxs-lookup"><span data-stu-id="5980b-141">These writers are documented in [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

 



