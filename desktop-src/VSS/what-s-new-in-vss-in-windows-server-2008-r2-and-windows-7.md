---
description: Windows Server 2008 R2 y Windows 7 presentan los siguientes cambios en el Servicio de instantáneas de volumen.
ms.assetid: 1287f175-29e4-40be-804b-d78542e76efc
title: 'Novedades: VSS en Windows Server 2008 R2 & Windows 7'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3677f89517a770a4519369ae11f2eed7e7985414
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696439"
---
# <a name="whats-new-vss-in-windows-server-2008-r2--windows-7"></a><span data-ttu-id="bb8fa-103">Novedades: VSS en Windows Server 2008 R2 & Windows 7</span><span class="sxs-lookup"><span data-stu-id="bb8fa-103">What's New: VSS in Windows Server 2008 R2 & Windows 7</span></span>

<span data-ttu-id="bb8fa-104">Windows Server 2008 R2 y Windows 7 presentan los siguientes cambios en el Servicio de instantáneas de volumen.</span><span class="sxs-lookup"><span data-stu-id="bb8fa-104">Windows Server 2008 R2 and Windows 7 introduce the following changes to the Volume Shadow Copy Service.</span></span>

## <a name="new-vss-interfaces"></a><span data-ttu-id="bb8fa-105">Nuevas interfaces VSS</span><span class="sxs-lookup"><span data-stu-id="bb8fa-105">New VSS Interfaces</span></span>

<dl>

[<span data-ttu-id="bb8fa-106">**IVssBackupComponentsEx3**</span><span class="sxs-lookup"><span data-stu-id="bb8fa-106">**IVssBackupComponentsEx3**</span></span>](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponentsex3)  
[<span data-ttu-id="bb8fa-107">**IVssComponentEx2**</span><span class="sxs-lookup"><span data-stu-id="bb8fa-107">**IVssComponentEx2**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponentex2)  
[<span data-ttu-id="bb8fa-108">**IVssCreateExpressWriterMetadata**</span><span class="sxs-lookup"><span data-stu-id="bb8fa-108">**IVssCreateExpressWriterMetadata**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreateexpresswritermetadata)  
[<span data-ttu-id="bb8fa-109">**IVssExpressWriter**</span><span class="sxs-lookup"><span data-stu-id="bb8fa-109">**IVssExpressWriter**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-ivssexpresswriter)  
</dl>

## <a name="new-vss-classes"></a><span data-ttu-id="bb8fa-110">Nuevas clases de VSS</span><span class="sxs-lookup"><span data-stu-id="bb8fa-110">New VSS Classes</span></span>

<dl>

[<span data-ttu-id="bb8fa-111">**CVssWriterEx2**</span><span class="sxs-lookup"><span data-stu-id="bb8fa-111">**CVssWriterEx2**</span></span>](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriterex2)  
</dl>

## <a name="new-vss-enumerations"></a><span data-ttu-id="bb8fa-112">Nuevas enumeraciones de VSS</span><span class="sxs-lookup"><span data-stu-id="bb8fa-112">New VSS Enumerations</span></span>

<dl>

[<span data-ttu-id="bb8fa-113">**\_Opciones de recuperación de VSS \_**</span><span class="sxs-lookup"><span data-stu-id="bb8fa-113">**VSS\_RECOVERY\_OPTIONS**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_recovery_options)  
</dl>

## <a name="new-vss-functions"></a><span data-ttu-id="bb8fa-114">Nuevas funciones de VSS</span><span class="sxs-lookup"><span data-stu-id="bb8fa-114">New VSS Functions</span></span>

<dl>

[<span data-ttu-id="bb8fa-115">**CreateVssExpressWriter**</span><span class="sxs-lookup"><span data-stu-id="bb8fa-115">**CreateVssExpressWriter**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-createvssexpresswriter)  
</dl>

## <a name="existing-vss-interface-modifications"></a><span data-ttu-id="bb8fa-116">Modificaciones de la interfaz de VSS existentes</span><span class="sxs-lookup"><span data-stu-id="bb8fa-116">Existing VSS Interface Modifications</span></span>

<dl>

<span data-ttu-id="bb8fa-117">Interfaz [**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex)</span><span class="sxs-lookup"><span data-stu-id="bb8fa-117">[**IVssHardwareSnapshotProviderEx**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotproviderex) interface</span></span><dl> <span data-ttu-id="bb8fa-118">Método agregado: [ **ResyncLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotproviderex-resyncluns)</span><span class="sxs-lookup"><span data-stu-id="bb8fa-118">Added method: [**ResyncLuns**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotproviderex-resyncluns)</span></span>  
</dl> </dd> </dl>

## <a name="vss-event-tracing-and-logging"></a><span data-ttu-id="bb8fa-119">Seguimiento y registro de eventos de VSS</span><span class="sxs-lookup"><span data-stu-id="bb8fa-119">VSS Event Tracing and Logging</span></span>

<span data-ttu-id="bb8fa-120">A partir de Windows Server 2008 R2 y Windows 7, puede usar la herramienta VssTrace, la herramienta Logman o la herramienta tracelog para recopilar información de seguimiento de la infraestructura de VSS.</span><span class="sxs-lookup"><span data-stu-id="bb8fa-120">Beginning with Windows Server 2008 R2 and Windows 7, you can use the VssTrace tool, the Logman tool, or the Tracelog tool to collect tracing information for the VSS infrastructure.</span></span> <span data-ttu-id="bb8fa-121">Para obtener más información, vea [uso de herramientas de seguimiento con VSS](using-tracing-tools-with-vss.md).</span><span class="sxs-lookup"><span data-stu-id="bb8fa-121">For more information, see [Using Tracing Tools with VSS](using-tracing-tools-with-vss.md).</span></span>

## <a name="lun-resynchronization"></a><span data-ttu-id="bb8fa-122">Resincronización de LUN</span><span class="sxs-lookup"><span data-stu-id="bb8fa-122">LUN Resynchronization</span></span>

<span data-ttu-id="bb8fa-123">En Windows Server 2008 R2 y Windows 7, los solicitantes de VSS pueden usar una característica del proveedor de instantáneas de hardware llamada resincronización de LUN.</span><span class="sxs-lookup"><span data-stu-id="bb8fa-123">In Windows Server 2008 R2 and Windows 7, VSS requesters can use a hardware shadow copy provider feature called LUN resynchronization (or "LUN resync").</span></span> <span data-ttu-id="bb8fa-124">Se trata de un esquema de recuperación rápida que permite a un administrador de aplicaciones restaurar datos de una instantánea en el número de unidad lógica (LUN) original o en un LUN nuevo.</span><span class="sxs-lookup"><span data-stu-id="bb8fa-124">This is a fast-recovery scheme that allows an application administrator to restore data from a shadow copy to the original logical unit number (LUN) or to a new LUN.</span></span> <span data-ttu-id="bb8fa-125">La instantánea puede ser un clon completo o una instantánea diferencial.</span><span class="sxs-lookup"><span data-stu-id="bb8fa-125">The shadow copy can be a full clone or a differential shadow copy.</span></span> <span data-ttu-id="bb8fa-126">En ambos casos, al final de la operación de resincronización, el LUN de destino tendrá el mismo contenido que el LUN de instantánea.</span><span class="sxs-lookup"><span data-stu-id="bb8fa-126">In either case, at the end of the resync operation, the destination LUN will have the same contents as the shadow copy LUN.</span></span> <span data-ttu-id="bb8fa-127">Durante la operación de resincronización, la matriz realiza una copia del nivel de bloque de la instantánea en el LUN de destino.</span><span class="sxs-lookup"><span data-stu-id="bb8fa-127">During the resync operation, the array performs a block-level copy from the shadow copy to the destination LUN.</span></span> <span data-ttu-id="bb8fa-128">Para obtener más información, vea lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="bb8fa-128">For more information, see the following:</span></span>

-   [<span data-ttu-id="bb8fa-129">Resincronización de LUN: un escenario de recuperación rápida en Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="bb8fa-129">LUN Resync - A fast recovery scenario in Server 2008 R2</span></span>](https://blogs.technet.com/filecab/archive/2009/04/11/lun-resync-a-fast-recovery-scenario-in-server-2008-r2.aspx)
-   <span data-ttu-id="bb8fa-130">"Cómo se usan las instantáneas" en [servicio de instantáneas de volumen](/windows-server/storage/file-server/volume-shadow-copy-service)</span><span class="sxs-lookup"><span data-stu-id="bb8fa-130">"How Shadow Copies Are Used" in [Volume Shadow Copy Service](/windows-server/storage/file-server/volume-shadow-copy-service)</span></span>
-   [<span data-ttu-id="bb8fa-131">Problemas comunes de resincronización de LUN</span><span class="sxs-lookup"><span data-stu-id="bb8fa-131">Common LUN Resync gotchas</span></span>](https://blogs.msdn.com/gregd/archive/2009/07/27/common-lun-resync-gotchas.aspx)

## <a name="express-writers"></a><span data-ttu-id="bb8fa-132">Escritores de Express</span><span class="sxs-lookup"><span data-stu-id="bb8fa-132">Express Writers</span></span>

<span data-ttu-id="bb8fa-133">En Windows Server 2008 R2 y Windows 7, la interfaz de VSS Express permite que una aplicación registre la ubicación de sus archivos de datos sin implementar una VSS Writer.</span><span class="sxs-lookup"><span data-stu-id="bb8fa-133">In Windows Server 2008 R2 and Windows 7, the VSS express interface allows an application to register the location of its data files without implementing a VSS writer.</span></span> <span data-ttu-id="bb8fa-134">Para obtener más información, consulte [escritores de servicio de instantáneas de volumen (VSS) Express](https://blogs.technet.com/filecab/archive/2009/06/17/volume-shadow-copy-service-vss-express-writers.aspx).</span><span class="sxs-lookup"><span data-stu-id="bb8fa-134">For more information, see [Volume Shadow Copy Service (VSS) Express Writers](https://blogs.technet.com/filecab/archive/2009/06/17/volume-shadow-copy-service-vss-express-writers.aspx).</span></span>

## <a name="new-vss-writers"></a><span data-ttu-id="bb8fa-135">Nuevos escritores de VSS</span><span class="sxs-lookup"><span data-stu-id="bb8fa-135">New VSS Writers</span></span>

<span data-ttu-id="bb8fa-136">Windows Server 2008 R2 y Windows 7 presentan los siguientes escritores de VSS:</span><span class="sxs-lookup"><span data-stu-id="bb8fa-136">Windows Server 2008 R2 and Windows 7 introduce the following VSS writers:</span></span>

-   <span data-ttu-id="bb8fa-137">Escritor de contadores de rendimiento</span><span class="sxs-lookup"><span data-stu-id="bb8fa-137">Performance Counters Writer</span></span>
-   <span data-ttu-id="bb8fa-138">Escritor de Programador de tareas</span><span class="sxs-lookup"><span data-stu-id="bb8fa-138">Task Scheduler Writer</span></span>
-   <span data-ttu-id="bb8fa-139">Escritor de almacén de metadatos de VSS</span><span class="sxs-lookup"><span data-stu-id="bb8fa-139">VSS Metadata Store Writer</span></span>

<span data-ttu-id="bb8fa-140">Estos nuevos escritores están documentados en [escritores de VSS en la caja](in-box-vss-writers.md).</span><span class="sxs-lookup"><span data-stu-id="bb8fa-140">These new writers are documented in [In-Box VSS Writers](in-box-vss-writers.md).</span></span>

 

 
