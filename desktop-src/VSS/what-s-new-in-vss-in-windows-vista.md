---
description: Windows Vista.
ms.assetid: 3b16744d-b9c2-4462-a409-de94d9103c39
title: Novedades de VSS en Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 122caa350ede984d5b05eb7eedd6039d82a76f1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696438"
---
# <a name="whats-new-in-vss-in-windows-vista"></a><span data-ttu-id="6a5a9-103">Novedades de VSS en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a5a9-103">What's New in VSS in Windows Vista</span></span>

<span data-ttu-id="6a5a9-104">Windows Vista presenta los siguientes cambios en el Servicio de instantáneas de volumen.</span><span class="sxs-lookup"><span data-stu-id="6a5a9-104">Windows Vista introduces the following changes to the Volume Shadow Copy Service.</span></span>

<span data-ttu-id="6a5a9-105">Tenga en cuenta que todos los cambios de Windows Vista también se aplican a Windows Server 2008 y Windows Vista con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="6a5a9-105">Note that all changes for Windows Vista also apply to Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

## <a name="new-vss-interfaces"></a><span data-ttu-id="6a5a9-106">Nuevas interfaces VSS</span><span class="sxs-lookup"><span data-stu-id="6a5a9-106">New VSS Interfaces</span></span>

[<span data-ttu-id="6a5a9-107">**IVssBackupComponentsEx2**</span><span class="sxs-lookup"><span data-stu-id="6a5a9-107">**IVssBackupComponentsEx2**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex2)

[<span data-ttu-id="6a5a9-108">**IVssComponentEx**</span><span class="sxs-lookup"><span data-stu-id="6a5a9-108">**IVssComponentEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex)

[<span data-ttu-id="6a5a9-109">**IVssCreateWriterMetadataEx**</span><span class="sxs-lookup"><span data-stu-id="6a5a9-109">**IVssCreateWriterMetadataEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadataex)

[<span data-ttu-id="6a5a9-110">**IVssDifferentialSoftwareSnapshotMgmt2**</span><span class="sxs-lookup"><span data-stu-id="6a5a9-110">**IVssDifferentialSoftwareSnapshotMgmt2**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivssdifferentialsoftwaresnapshotmgmt2)

[<span data-ttu-id="6a5a9-111">**IVssExamineWriterMetadataEx2**</span><span class="sxs-lookup"><span data-stu-id="6a5a9-111">**IVssExamineWriterMetadataEx2**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadataex2)

## <a name="new-vss-classes"></a><span data-ttu-id="6a5a9-112">Nuevas clases de VSS</span><span class="sxs-lookup"><span data-stu-id="6a5a9-112">New VSS Classes</span></span>

[<span data-ttu-id="6a5a9-113">**CVssWriterEx**</span><span class="sxs-lookup"><span data-stu-id="6a5a9-113">**CVssWriterEx**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex)

## <a name="new-vss-enumerations"></a><span data-ttu-id="6a5a9-114">Nuevas enumeraciones de VSS</span><span class="sxs-lookup"><span data-stu-id="6a5a9-114">New VSS Enumerations</span></span>

[<span data-ttu-id="6a5a9-115">**tipo de puesta al día de VSS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6a5a9-115">**VSS\_ROLLFORWARD\_TYPE**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_rollforward_type)

## <a name="existing-vss-enumeration-modifications"></a><span data-ttu-id="6a5a9-116">Modificaciones de la enumeración de VSS existentes</span><span class="sxs-lookup"><span data-stu-id="6a5a9-116">Existing VSS Enumeration Modifications</span></span>

<dl> <dt>

<span data-ttu-id="6a5a9-117"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS \_ \_**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) Enumeración de esquema de copia de seguridad</span><span class="sxs-lookup"><span data-stu-id="6a5a9-117"><span id="VSS_BACKUP_SCHEMA_enumeration"></span><span id="vss_backup_schema_enumeration"></span><span id="VSS_BACKUP_SCHEMA_ENUMERATION"></span>[**VSS\_BACKUP\_SCHEMA**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="6a5a9-118"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valores agregados:</span><span class="sxs-lookup"><span data-stu-id="6a5a9-118"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="6a5a9-119">\_ \_ restauración autoritativa de VSS BS \_</span><span class="sxs-lookup"><span data-stu-id="6a5a9-119">VSS\_BS\_AUTHORITATIVE\_RESTORE</span></span>

<span data-ttu-id="6a5a9-120">\_ \_ \_ Estado del sistema independiente de VSS BS \_</span><span class="sxs-lookup"><span data-stu-id="6a5a9-120">VSS\_BS\_INDEPENDENT\_SYSTEM\_STATE</span></span>

<span data-ttu-id="6a5a9-121">\_cambio de \_ nombre de restauración de VSS BS \_</span><span class="sxs-lookup"><span data-stu-id="6a5a9-121">VSS\_BS\_RESTORE\_RENAME</span></span>

<span data-ttu-id="6a5a9-122">restauración con puesta al día de VSS \_ BS \_ \_</span><span class="sxs-lookup"><span data-stu-id="6a5a9-122">VSS\_BS\_ROLLFORWARD\_RESTORE</span></span>

</dd> </dl> </dd> </dl>

<dl> <dt>

<span data-ttu-id="6a5a9-123"><span id="VSS_COMPONENT_FLAGS_enumeration"></span><span id="vss_component_flags_enumeration"></span><span id="VSS_COMPONENT_FLAGS_ENUMERATION"></span>[**VSS \_ \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags) Enumeración de marcas de componentes</span><span class="sxs-lookup"><span data-stu-id="6a5a9-123"><span id="VSS_COMPONENT_FLAGS_enumeration"></span><span id="vss_component_flags_enumeration"></span><span id="VSS_COMPONENT_FLAGS_ENUMERATION"></span>[**VSS\_COMPONENT\_FLAGS**](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="6a5a9-124"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valores agregados:</span><span class="sxs-lookup"><span data-stu-id="6a5a9-124"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="6a5a9-125">\_ \_ \_ Estado del sistema de VSS CF no \_</span><span class="sxs-lookup"><span data-stu-id="6a5a9-125">VSS\_CF\_NOT\_SYSTEM\_STATE</span></span>

</dd> </dl> </dd> </dl>

<dl> <dt>

<span data-ttu-id="6a5a9-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>Enumeración de [**\_ \_ atributos de \_ instantánea \_ de volumen de VSS**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)</span><span class="sxs-lookup"><span data-stu-id="6a5a9-126"><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_enumeration"></span><span id="_vss_volume_snapshot_attributes_enumeration"></span><span id="_VSS_VOLUME_SNAPSHOT_ATTRIBUTES_ENUMERATION"></span>[**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes) enumeration</span></span>
</dt> <dd>

<dl> <dt>

<span data-ttu-id="6a5a9-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Valores agregados:</span><span class="sxs-lookup"><span data-stu-id="6a5a9-127"><span id="Added_values_"></span><span id="added_values_"></span><span id="ADDED_VALUES_"></span>Added values:</span></span>
</dt> <dd>

<span data-ttu-id="6a5a9-128">VSS \_ VOLSNAP \_ ATTR \_ no \_ autoRecovery</span><span class="sxs-lookup"><span data-stu-id="6a5a9-128">VSS\_VOLSNAP\_ATTR\_NO\_AUTORECOVERY</span></span>

<span data-ttu-id="6a5a9-129">\_atributo VOLSNAP de VSS \_ \_ no \_ transaccionado</span><span class="sxs-lookup"><span data-stu-id="6a5a9-129">VSS\_VOLSNAP\_ATTR\_NOT\_TRANSACTED</span></span>

</dd> </dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a><span data-ttu-id="6a5a9-130">Seguimiento y registro de eventos de VSS</span><span class="sxs-lookup"><span data-stu-id="6a5a9-130">VSS Event Tracing and Logging</span></span>

-   <span data-ttu-id="6a5a9-131">El archivo de seguimiento de VSS ahora se puede encontrar en cualquier volumen local.</span><span class="sxs-lookup"><span data-stu-id="6a5a9-131">The VSS trace file can now be located on any local volume.</span></span> <span data-ttu-id="6a5a9-132">En las versiones de Windows anteriores a Windows Vista, el archivo de seguimiento de VSS no se encontró en un volumen que se encontraba en el conjunto de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="6a5a9-132">On versions of Windows prior to Windows Vista, the VSS trace file could not be located on a volume that was in the shadow copy set.</span></span>
-   <span data-ttu-id="6a5a9-133">Muchas de las entradas del registro de eventos se han reparado para que sean más claras.</span><span class="sxs-lookup"><span data-stu-id="6a5a9-133">Many event log entries have been reworded to make them clearer.</span></span>
-   <span data-ttu-id="6a5a9-134">Todas las entradas del registro de eventos de VSS contienen ahora información de contexto.</span><span class="sxs-lookup"><span data-stu-id="6a5a9-134">All VSS event log entries now contain context information.</span></span>

## <a name="vss-error-reporting"></a><span data-ttu-id="6a5a9-135">Informe de errores de VSS</span><span class="sxs-lookup"><span data-stu-id="6a5a9-135">VSS Error Reporting</span></span>

-   <span data-ttu-id="6a5a9-136">Ahora se pueden recuperar las descripciones de todos los códigos de error de VSS mediante una llamada a la función [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) con el \_ mensaje Format desde la \_ \_ marca HMODULE especificado en el parámetro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="6a5a9-136">Descriptions of all VSS error codes can now be retrieved by calling the [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_HMODULE flag specified in the *dwFlags* parameter.</span></span>
-   <span data-ttu-id="6a5a9-137">Los mensajes del código de error de VSS se incluyen en vsstrace.dll.</span><span class="sxs-lookup"><span data-stu-id="6a5a9-137">The VSS error code messages are contained in vsstrace.dll.</span></span> <span data-ttu-id="6a5a9-138">Se debe especificar un identificador para este módulo en el parámetro *lpSource* .</span><span class="sxs-lookup"><span data-stu-id="6a5a9-138">A handle to this module must be specified in the *lpSource* parameter.</span></span>

## <a name="excluding-files-from-shadow-copies"></a><span data-ttu-id="6a5a9-139">Excluir archivos de instantáneas</span><span class="sxs-lookup"><span data-stu-id="6a5a9-139">Excluding Files from Shadow Copies</span></span>

<span data-ttu-id="6a5a9-140">Las aplicaciones o los servicios pueden usar la clave del registro FilesNotToSnapshot para especificar los archivos que se van a eliminar de las instantáneas recién creadas.</span><span class="sxs-lookup"><span data-stu-id="6a5a9-140">Applications or services can use the FilesNotToSnapshot registry key to specify files to be deleted from newly created shadow copies.</span></span> <span data-ttu-id="6a5a9-141">Para obtener más información, vea [excluir archivos de instantáneas](excluding-files-from-shadow-copies.md).</span><span class="sxs-lookup"><span data-stu-id="6a5a9-141">For more information, see [Excluding Files from Shadow Copies](excluding-files-from-shadow-copies.md).</span></span>

## <a name="backup-and-restore-application-compatibility"></a><span data-ttu-id="6a5a9-142">Compatibilidad de aplicaciones de copia de seguridad y restauración</span><span class="sxs-lookup"><span data-stu-id="6a5a9-142">Backup and Restore Application Compatibility</span></span>

<span data-ttu-id="6a5a9-143">Los desarrolladores de aplicaciones de copia de seguridad y restauración deben tener en cuenta ciertas características nuevas de Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="6a5a9-143">Developers of backup and restore applications need to be aware of certain new features in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="6a5a9-144">Para obtener una lista de comprobación de compatibilidad de aplicaciones, vea [compatibilidad de aplicaciones para copias de seguridad y restauración](application-compatibility-for-backup-and-restore.md).</span><span class="sxs-lookup"><span data-stu-id="6a5a9-144">For an application compatibility checklist, see [Application Compatibility for Backup and Restore](application-compatibility-for-backup-and-restore.md).</span></span>

 

 
