---
description: Los solicitantes controlan las características de la instantánea estableciendo su contexto. Este contexto indica si la instantánea sobreviverá a la operación actual y el grado de la coordinación del escritor o del proveedor.
ms.assetid: adf79bc8-e893-444a-b750-d7ffd09de7c9
title: Configuraciones de contexto de instantáneas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdb41d0e2604dcf92d27f490175cdcbafd49822c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544955"
---
# <a name="shadow-copy-context-configurations"></a><span data-ttu-id="0c8ea-104">Configuraciones de contexto de instantáneas</span><span class="sxs-lookup"><span data-stu-id="0c8ea-104">Shadow Copy Context Configurations</span></span>

<span data-ttu-id="0c8ea-105">Los solicitantes controlan las características de la instantánea estableciendo su contexto.</span><span class="sxs-lookup"><span data-stu-id="0c8ea-105">Requesters control a shadow copy's features by setting its context.</span></span> <span data-ttu-id="0c8ea-106">Este contexto indica si la instantánea sobreviverá a la operación actual y el grado de la coordinación del escritor o del proveedor.</span><span class="sxs-lookup"><span data-stu-id="0c8ea-106">This context indicates whether the shadow copy will survive the current operation, and the degree of writer/provider coordination.</span></span>

## <a name="persistence-and-shadow-copy-context"></a><span data-ttu-id="0c8ea-107">Persistencia y contexto de instantáneas</span><span class="sxs-lookup"><span data-stu-id="0c8ea-107">Persistence and Shadow Copy Context</span></span>

<span data-ttu-id="0c8ea-108">Una instantánea puede ser [*persistente*](vssgloss-p.md), es decir, la instantánea no se elimina después de la finalización de una operación de copia de seguridad o de la liberación de un objeto [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) .</span><span class="sxs-lookup"><span data-stu-id="0c8ea-108">A shadow copy may be [*persistent*](vssgloss-p.md)—that is, the shadow copy is not deleted following the termination of a backup operation or the release of an [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) object.</span></span>

<span data-ttu-id="0c8ea-109">Las instantáneas persistentes requieren contextos de [**\_ \_ \_ contexto de instantáneas de VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) del **cliente de VSS \_ CTX \_ \_ accesible**, **\_ \_ \_ reversión de aplicación de VSS CTX** o **\_ \_ \_ reversión de NAS de VSS CTX**.</span><span class="sxs-lookup"><span data-stu-id="0c8ea-109">Persistent shadow copies require [**\_VSS\_SNAPSHOT\_CONTEXT**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) contexts of **VSS\_CTX\_CLIENT\_ACCESSIBLE**, **VSS\_CTX\_APP\_ROLLBACK**, or **VSS\_CTX\_NAS\_ROLLBACK**.</span></span> <span data-ttu-id="0c8ea-110">Solo se pueden realizar instantáneas persistentes para volúmenes NTFS.</span><span class="sxs-lookup"><span data-stu-id="0c8ea-110">Persistent shadow copies can be made only for NTFS volumes.</span></span>

<span data-ttu-id="0c8ea-111">Las instantáneas no persistentes se crean con contextos de la copia de seguridad de **VSS \_ CTX \_** o del **\_ \_ \_ recurso compartido \_ de archivos de VSS CTX**.</span><span class="sxs-lookup"><span data-stu-id="0c8ea-111">Nonpersistent shadow copies are created with contexts of **VSS\_CTX\_BACKUP** or **VSS\_CTX\_FILE\_SHARE\_BACKUP**.</span></span> <span data-ttu-id="0c8ea-112">Se pueden realizar instantáneas no persistentes para volúmenes NTFS y no NTFS.</span><span class="sxs-lookup"><span data-stu-id="0c8ea-112">Nonpersistent shadow copies can be made for NTFS and non-NTFS volumes.</span></span>

## <a name="writer-participation-and-shadow-copies"></a><span data-ttu-id="0c8ea-113">Participación y instantáneas del escritor</span><span class="sxs-lookup"><span data-stu-id="0c8ea-113">Writer Participation and Shadow Copies</span></span>

<span data-ttu-id="0c8ea-114">Un contexto de instantánea se puede clasificar como que implique A escritores o que no implique escritores.</span><span class="sxs-lookup"><span data-stu-id="0c8ea-114">A shadow copy context can be classified as either involving writers or not involving writers.</span></span>

<span data-ttu-id="0c8ea-115">Entre los contextos de instantáneas que implican escritores en su creación se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="0c8ea-115">Shadow copy contexts that involve writers in their creation include:</span></span>

-   <span data-ttu-id="0c8ea-116">**reversión de la aplicación de VSS \_ CTX \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0c8ea-116">**VSS\_CTX\_APP\_ROLLBACK**</span></span>
-   <span data-ttu-id="0c8ea-117">**copia de seguridad de VSS \_ CTX \_**</span><span class="sxs-lookup"><span data-stu-id="0c8ea-117">**VSS\_CTX\_BACKUP**</span></span>
-   <span data-ttu-id="0c8ea-118">**\_ \_ \_ escritores accesibles del cliente \_ de VSS CTX**</span><span class="sxs-lookup"><span data-stu-id="0c8ea-118">**VSS\_CTX\_CLIENT\_ACCESSIBLE\_WRITERS**</span></span>

<span data-ttu-id="0c8ea-119">Entre los que no implican escritores en su creación se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="0c8ea-119">Those that do not involve writers in their creation include:</span></span>

-   <span data-ttu-id="0c8ea-120">**cliente de VSS \_ CTX \_ \_ accesible**</span><span class="sxs-lookup"><span data-stu-id="0c8ea-120">**VSS\_CTX\_CLIENT\_ACCESSIBLE**</span></span>
-   <span data-ttu-id="0c8ea-121">**\_copia de \_ \_ seguridad de recurso compartido de archivos de VSS CTX \_**</span><span class="sxs-lookup"><span data-stu-id="0c8ea-121">**VSS\_CTX\_FILE\_SHARE\_BACKUP**</span></span>
-   <span data-ttu-id="0c8ea-122">**reversión de NAS de VSS \_ CTX \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0c8ea-122">**VSS\_CTX\_NAS\_ROLLBACK**</span></span>

<span data-ttu-id="0c8ea-123">Un contexto se puede usar con ambos tipos de instantáneas, pero no se puede usar para crear una instantánea:</span><span class="sxs-lookup"><span data-stu-id="0c8ea-123">One context can be used with both types of shadow copies, but cannot be used in creating a shadow copy:</span></span>

-   <span data-ttu-id="0c8ea-124">**All de VSS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0c8ea-124">**VSS\_CTX\_ALL**</span></span>

<span data-ttu-id="0c8ea-125">No se admite la creación de una instantánea con un contexto de **VSS \_ CTX \_ All** (mediante [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) y [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)).</span><span class="sxs-lookup"><span data-stu-id="0c8ea-125">Creating a shadow copy with a context of **VSS\_CTX\_ALL** (using [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) and [**IVssBackupComponents::DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)) is not supported.</span></span>

<span data-ttu-id="0c8ea-126">Las operaciones que admiten un contexto de **VSS \_ CTX \_** son las operaciones administrativas [**IVssBackupComponents:: query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query), [**IVssBackupComponents::D Eletesnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots), [**IVssBackupComponents:: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset)y [**IVssBackupComponents:: ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot).</span><span class="sxs-lookup"><span data-stu-id="0c8ea-126">Operations that support a context of **VSS\_CTX\_ALL** are the administrative operations [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query), [**IVssBackupComponents::DeleteSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots), [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset), and [**IVssBackupComponents::ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot).</span></span>

## <a name="obtaining-shadow-copy-information"></a><span data-ttu-id="0c8ea-127">Obtener información de instantáneas</span><span class="sxs-lookup"><span data-stu-id="0c8ea-127">Obtaining Shadow Copy Information</span></span>

<span data-ttu-id="0c8ea-128">Si un solicitante conoce el GUID de identificación de una instantánea (su **\_ identificador de VSS**), puede obtener información sobre el contexto de una instantánea específica (identificada por su **\_ identificador de VSS**) desempaquetando la estructura de la [**\_ instantánea \_ de VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) devuelta por una llamada a [**IVssBackupComponents:: GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).</span><span class="sxs-lookup"><span data-stu-id="0c8ea-128">If a requester knows the identifying GUID of a shadow copy (its **VSS\_ID**), it can obtain information about the context of a specific shadow copy (identified by its **VSS\_ID**) by unpacking the [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure returned by a call to [**IVssBackupComponents::GetSnapshotProperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).</span></span>

<span data-ttu-id="0c8ea-129">Para obtener información de contexto sobre todas las instantáneas de un sistema, un solicitante examina el miembro **m \_ lSnapshotAttributes** del miembro **obj. Snap** del [**\_ objeto VSS \_ prop**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (que es una estructura de [**\_ instantáneas \_ de VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) ) obtenida mediante [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) para iterar por la lista de objetos devueltos por una llamada a [**IVssBackupComponents:: query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span><span class="sxs-lookup"><span data-stu-id="0c8ea-129">To obtain context information about all shadow copies on a system, a requester examines the **m\_lSnapshotAttributes** member of the **Obj.Snap** member of the [**VSS\_OBJECT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (which is a [**VSS\_SNAPSHOT\_PROP**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) structure) structure obtained by using [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) to iterate over the list of objects returned by a call to [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span></span>

 

 



