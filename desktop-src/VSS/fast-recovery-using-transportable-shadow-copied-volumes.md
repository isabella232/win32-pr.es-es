---
description: Las instantáneas transportables se pueden usar para facilitar una recuperación rápida.
ms.assetid: 2eaffcf7-01b2-44ce-8bc4-fd9fa42c8a8c
title: Recuperación rápida mediante el uso de volúmenes de instantáneas transportables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a588395de36b0e6773eacf7f46a45452a69c13c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697738"
---
# <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a><span data-ttu-id="6670f-103">Recuperación rápida mediante el uso de volúmenes de instantáneas transportables</span><span class="sxs-lookup"><span data-stu-id="6670f-103">Fast Recovery Using Transportable Shadow Copied Volumes</span></span>

<span data-ttu-id="6670f-104">Las [*instantáneas transportables*](vssgloss-t.md) se pueden usar para facilitar una *recuperación rápida*.</span><span class="sxs-lookup"><span data-stu-id="6670f-104">[*Transportable shadow copies*](vssgloss-t.md) can be used to facilitate a *fast recovery*.</span></span>

<span data-ttu-id="6670f-105">La recuperación rápida se puede usar para revertir rápidamente a una instantánea anterior.</span><span class="sxs-lookup"><span data-stu-id="6670f-105">Fast recovery can be used to quickly revert to an earlier shadow copy.</span></span> <span data-ttu-id="6670f-106">Estos son los pasos que hay que realizar:</span><span class="sxs-lookup"><span data-stu-id="6670f-106">The steps involved are:</span></span>

1.  <span data-ttu-id="6670f-107">Cree la instantánea transportable de los LUN correspondientes.</span><span class="sxs-lookup"><span data-stu-id="6670f-107">Create the transportable shadow copy of the appropriate LUNs.</span></span> <span data-ttu-id="6670f-108">La instantánea puede ser [*persistente*](vssgloss-p.md) o no persistente.</span><span class="sxs-lookup"><span data-stu-id="6670f-108">The shadow copy can be either [*persistent*](vssgloss-p.md) or nonpersistent.</span></span>
2.  <span data-ttu-id="6670f-109">Quitar los LUN originales</span><span class="sxs-lookup"><span data-stu-id="6670f-109">Remove the original LUNs</span></span>
    1.  <span data-ttu-id="6670f-110">Si el equipo está dentro de un clúster, marque los recursos de disco afectados como sin conexión o habilite el [modo de mantenimiento](/previous-versions/windows/desktop/mscs/maintaining-physical-disk-resources) para estos recursos de disco.</span><span class="sxs-lookup"><span data-stu-id="6670f-110">If the computer is inside a cluster, mark the affected disk resources as offline, or enable the [maintenance mode](/previous-versions/windows/desktop/mscs/maintaining-physical-disk-resources) for these disk resources.</span></span>
    2.  <span data-ttu-id="6670f-111">Enmascarar los LUN afectados desde este equipo (y todos los demás nodos si el equipo está en un clúster).</span><span class="sxs-lookup"><span data-stu-id="6670f-111">Mask the affected LUNs from this computer (and all other nodes if the computer is in a cluster).</span></span>
3.  <span data-ttu-id="6670f-112">Importe la instantánea con el método [**IVssBackupComponents:: ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) .</span><span class="sxs-lookup"><span data-stu-id="6670f-112">Import the shadow copy using the [**IVssBackupComponents::ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) method.</span></span>
4.  <span data-ttu-id="6670f-113">Divida la instantánea con el método [**IVssBackupComponents:: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) .</span><span class="sxs-lookup"><span data-stu-id="6670f-113">Break the shadow copy using the [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) method.</span></span>
5.  <span data-ttu-id="6670f-114">Marque los nuevos volúmenes de instantáneas como de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="6670f-114">Mark the new shadow copy volumes as read/write.</span></span>
6.  <span data-ttu-id="6670f-115">Si el equipo está en un clúster, exponga los LUN de instantáneas nuevos como los LUN originales.</span><span class="sxs-lookup"><span data-stu-id="6670f-115">If the computer is in a cluster, expose the new shadow copy LUNs as the original LUNs.</span></span>
    1.  <span data-ttu-id="6670f-116">Desenmascarar los LUN de instantánea en los otros nodos del clúster.</span><span class="sxs-lookup"><span data-stu-id="6670f-116">Unmask the shadow copy LUNs to the other nodes in the cluster.</span></span>
    2.  <span data-ttu-id="6670f-117">Marque los recursos que se han marcado previamente como sin conexión como en línea o deshabilite el modo de mantenimiento para esos recursos de disco.</span><span class="sxs-lookup"><span data-stu-id="6670f-117">Mark the resources that were previously marked as offline as online, or disable the maintenance mode for those disk resources.</span></span>

> [!Note]  
> <span data-ttu-id="6670f-118">No se admiten las instantáneas transportables en un clúster antes de Windows Server 2003 con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="6670f-118">Transportable shadow copies in a cluster are not supported before Windows Server 2003 with Service Pack 1 (SP1).</span></span> <span data-ttu-id="6670f-119">Esto solo es compatible con los LUN compatibles, que tienen al menos una página de datos vitales de producto (VPD) de SCSI 0x83 \_ identificador de almacenamiento de tipo 1, 2 u 8, y la Asociación 0, y los LUN deben mantener un disco básico con particiones MBR.</span><span class="sxs-lookup"><span data-stu-id="6670f-119">This is only supported with compliant LUNs, which have at least one SCSI Vital Product Data (VPD) page 0x83 STORAGE\_IDENTIFIER of type 1,2, or 8, and association 0, and the LUNs must maintain a basic disk with MBR partitioning.</span></span>

 

 

 
