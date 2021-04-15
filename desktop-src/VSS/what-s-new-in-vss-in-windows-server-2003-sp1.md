---
description: 'La lista siguiente indica las adiciones y los cambios en la interfaz de Servicio de instantáneas de volumen en Windows Server 2003 con Service Pack 1 (SP1):'
ms.assetid: 9e0dba98-5d23-444d-bd2f-cb72de8fb2d2
title: Novedades de VSS en Windows Server 2003 SP1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 559b51d5b019d9d57aa154c4728ef5c8f4bb19d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497518"
---
# <a name="whats-new-in-vss-in-windows-server-2003-sp1"></a><span data-ttu-id="aed4e-103">Novedades de VSS en Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="aed4e-103">What's New in VSS in Windows Server 2003 SP1</span></span>

<span data-ttu-id="aed4e-104">La lista siguiente indica las adiciones y los cambios en la interfaz de Servicio de instantáneas de volumen en Windows Server 2003 con Service Pack 1 (SP1):</span><span class="sxs-lookup"><span data-stu-id="aed4e-104">The following list indicates additions and changes to the Volume Shadow Copy Service interface in Windows Server 2003 with Service Pack 1 (SP1):</span></span>

## <a name="auto-recovery"></a><span data-ttu-id="aed4e-105">Recuperación automática</span><span class="sxs-lookup"><span data-stu-id="aed4e-105">Auto-recovery</span></span>

<span data-ttu-id="aed4e-106">La [*recuperación automática*](vssgloss-a.md) permite a los escritores actualizar los componentes de una instantánea antes de que la instantánea cambie permanentemente a solo lectura.</span><span class="sxs-lookup"><span data-stu-id="aed4e-106">[*Auto-recovery*](vssgloss-a.md) allows writers a time to update components in a shadow copy before the shadow copy is permanently changed to read-only.</span></span> <span data-ttu-id="aed4e-107">Por ejemplo, una base de datos puede necesitar revertir las transacciones incompletas para todas las instantáneas (el escritor de la base de datos establecería la marca de **recuperación de copia de seguridad de CF de VSS \_ \_ \_** para los componentes de base de datos).</span><span class="sxs-lookup"><span data-stu-id="aed4e-107">For example, a database may need to rollback any incomplete transactions for all shadow copies (the database writer would set the **VSS\_CF\_BACKUP\_RECOVERY** flag for the database components).</span></span> <span data-ttu-id="aed4e-108">La recuperación automática iniciada por el solicitante permite la restauración específica (por ejemplo, la restauración de una tabla en una base de datos o una carpeta en un servidor de correo), o la reversión para admitir la minería de datos para realizar análisis que serían demasiado lentas para un servidor de producción (el solicitante agregaría **VSS \_ VOLSNAP \_ atributo \_ Rollback \_ Recovery** al contexto de instantánea). La recuperación automática no es compatible con las instantáneas transportables, pero se admite la misma funcionalidad mediante la [recuperación rápida mediante el uso de volúmenes de instantáneas transportables](fast-recovery-using-transportable-shadow-copied-volumes.md).</span><span class="sxs-lookup"><span data-stu-id="aed4e-108">Auto-recovery initiated by the requester allows both fine-grained restore (for example restoring one table in a database or one folder on a mail server), or the rollback to support data mining to perform analysis that would be too slow for a production server (the requester would add **VSS\_VOLSNAP\_ATTR\_ROLLBACK\_RECOVERY** to the shadow copy context.) Auto-recovery is not compatible with transportable shadow copies, but the same functionality is supported by using [Fast Recovery Using Transportable Shadow Copied Volumes](fast-recovery-using-transportable-shadow-copied-volumes.md).</span></span>

<span data-ttu-id="aed4e-109">Los siguientes elementos de programación tienen cambios para admitir la recuperación automática:</span><span class="sxs-lookup"><span data-stu-id="aed4e-109">The following programming elements have changes to support auto-recovery:</span></span>

<span data-ttu-id="aed4e-110">Métodos de clase</span><span class="sxs-lookup"><span data-stu-id="aed4e-110">Class methods</span></span>

-   [<span data-ttu-id="aed4e-111">**CVssWriter::GetSnapshotDeviceName**</span><span class="sxs-lookup"><span data-stu-id="aed4e-111">**CVssWriter::GetSnapshotDeviceName**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-getsnapshotdevicename)
-   [<span data-ttu-id="aed4e-112">**CVssWriter::OnPostSnapshot**</span><span class="sxs-lookup"><span data-stu-id="aed4e-112">**CVssWriter::OnPostSnapshot**</span></span>](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostsnapshot)

<span data-ttu-id="aed4e-113">Enumeraciones</span><span class="sxs-lookup"><span data-stu-id="aed4e-113">Enumerations</span></span>

-   [<span data-ttu-id="aed4e-114">**\_marcas de componentes de VSS \_**</span><span class="sxs-lookup"><span data-stu-id="aed4e-114">**VSS\_COMPONENT\_FLAGS**</span></span>](/windows/desktop/api/VsWriter/ne-vswriter-vss_component_flags)
-   [<span data-ttu-id="aed4e-115">**\_\_atributos de \_ instantáneas de volumen de VSS \_**</span><span class="sxs-lookup"><span data-stu-id="aed4e-115">**\_VSS\_VOLUME\_SNAPSHOT\_ATTRIBUTES**</span></span>](/windows/desktop/api/Vss/ne-vss-vss_volume_snapshot_attributes)

<span data-ttu-id="aed4e-116">Métodos de interfaz</span><span class="sxs-lookup"><span data-stu-id="aed4e-116">Interface methods</span></span>

-   [<span data-ttu-id="aed4e-117">**IVssProviderCreateSnapshotSet::P reFinalCommitSnapshots**</span><span class="sxs-lookup"><span data-stu-id="aed4e-117">**IVssProviderCreateSnapshotSet::PreFinalCommitSnapshots**</span></span>](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-prefinalcommitsnapshots)
-   [<span data-ttu-id="aed4e-118">**IVssProviderCreateSnapshotSet::P ostFinalCommitSnapshots**</span><span class="sxs-lookup"><span data-stu-id="aed4e-118">**IVssProviderCreateSnapshotSet::PostFinalCommitSnapshots**</span></span>](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postfinalcommitsnapshots)

## <a name="full-support-for-transportable-shadow-copies"></a><span data-ttu-id="aed4e-119">Compatibilidad total con instantáneas transportables</span><span class="sxs-lookup"><span data-stu-id="aed4e-119">Full Support for Transportable Shadow Copies</span></span>

<span data-ttu-id="aed4e-120">Las instantáneas transportables se admiten en todas las ediciones de Windows Server 2003 con SP1.</span><span class="sxs-lookup"><span data-stu-id="aed4e-120">Transportable shadow copies are supported in all editions of Windows Server 2003 with SP1.</span></span> <span data-ttu-id="aed4e-121">Para obtener más información, vea [importar volúmenes de instantáneas transportables](importing-transportable-shadow-copied-volumes.md).</span><span class="sxs-lookup"><span data-stu-id="aed4e-121">For more information, see [Importing Transportable Shadow Copied Volumes](importing-transportable-shadow-copied-volumes.md).</span></span>

## <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a><span data-ttu-id="aed4e-122">Recuperación rápida mediante el uso de volúmenes de instantáneas transportables</span><span class="sxs-lookup"><span data-stu-id="aed4e-122">Fast Recovery Using Transportable Shadow Copied Volumes</span></span>

[<span data-ttu-id="aed4e-123">Recuperación rápida mediante el uso de volúmenes de instantáneas transportables</span><span class="sxs-lookup"><span data-stu-id="aed4e-123">Fast Recovery Using Transportable Shadow Copied Volumes</span></span>](fast-recovery-using-transportable-shadow-copied-volumes.md)

## <a name="shadow-copy-storage-area-management"></a><span data-ttu-id="aed4e-124">Administración de área de almacenamiento de instantáneas</span><span class="sxs-lookup"><span data-stu-id="aed4e-124">Shadow copy storage area management</span></span>

[<span data-ttu-id="aed4e-125">**IVssSnapshotMgmt2**</span><span class="sxs-lookup"><span data-stu-id="aed4e-125">**IVssSnapshotMgmt2**</span></span>](/windows/desktop/api/VsMgmt/nn-vsmgmt-ivsssnapshotmgmt2)

 

 



