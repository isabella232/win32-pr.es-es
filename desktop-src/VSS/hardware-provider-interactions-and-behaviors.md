---
description: Interacciones y comportamientos del proveedor de hardware
ms.assetid: 059968cf-43e5-4442-b757-80afdd66799f
title: Interacciones y comportamientos del proveedor de hardware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa30add6b34a7f3a0c45c88346c32c43e99398e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276353"
---
# <a name="hardware-provider-interactions-and-behaviors"></a><span data-ttu-id="2f2a9-103">Interacciones y comportamientos del proveedor de hardware</span><span class="sxs-lookup"><span data-stu-id="2f2a9-103">Hardware Provider Interactions and Behaviors</span></span>

<span data-ttu-id="2f2a9-104">Los proveedores de hardware pueden admitir instantáneas de copia en escritura o de reflejo de copia completa (diferencial y/o Plex).</span><span class="sxs-lookup"><span data-stu-id="2f2a9-104">Hardware providers may support copy-on-write and/or full copy mirror (differential and/or plex) shadow copies.</span></span> <span data-ttu-id="2f2a9-105">La asignación de recursos para instantáneas debe seguir el contexto especificado por el solicitante en [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext), enumerado por el [**\_ \_ \_ contexto de instantáneas de VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context), para el conjunto de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="2f2a9-105">Resource allocation for shadow copies should follow the context specified by the requester in [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext), enumerated by [**\_VSS\_SNAPSHOT\_CONTEXT**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context), for the shadow copy set.</span></span>

-   <span data-ttu-id="2f2a9-106">Si el solicitante especifica un contexto de instantánea compatible con el proveedor, el proveedor debe crear una instantánea con ese método.</span><span class="sxs-lookup"><span data-stu-id="2f2a9-106">If the requester specifies a shadow copy context that is supported by the provider, the provider should create a shadow copy using that method.</span></span>
-   <span data-ttu-id="2f2a9-107">Si el solicitante especifica un contexto de instantáneas que no es compatible con el proveedor, el proveedor no debe intentar crear la instantánea y devolver el **valor false** a través del parámetro *pbIsSupported* de [**IVssHardwareSnapshotProvider:: AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported).</span><span class="sxs-lookup"><span data-stu-id="2f2a9-107">If the requester specifies a shadow copy context that is not supported by the provider, then the provider should not attempt to create the shadow copy and return **FALSE** through the *pbIsSupported* parameter in [**IVssHardwareSnapshotProvider::AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported).</span></span>
-   <span data-ttu-id="2f2a9-108">Si el solicitante no especifica explícitamente un contexto de instantáneas, el proveedor debe usar un comportamiento predeterminado razonable para la creación de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="2f2a9-108">If the requester does not explicitly specify a shadow copy context, then the provider should use reasonable default behavior for shadow copy creation.</span></span>

<span data-ttu-id="2f2a9-109">Los proveedores de hardware asociados a los subsistemas RAID de SAN deben admitir instantáneas transportables para permitir el movimiento entre hosts en una red SAN.</span><span class="sxs-lookup"><span data-stu-id="2f2a9-109">Hardware providers associated with SAN RAID subsystems should support transportable shadow copies to allow movement between hosts on a SAN.</span></span>

<span data-ttu-id="2f2a9-110">No es necesario coordinar los proveedores de hardware que se ejecutan en varios equipos en una SAN y administrar el mismo subsistema RAID en una SAN.</span><span class="sxs-lookup"><span data-stu-id="2f2a9-110">Hardware providers running on multiple machines on a SAN yet managing the same RAID subsystem do not need to coordinate between providers on a SAN.</span></span> <span data-ttu-id="2f2a9-111">El Coordinador mantiene cualquier estado necesario.</span><span class="sxs-lookup"><span data-stu-id="2f2a9-111">The coordinator maintains any necessary state.</span></span> <span data-ttu-id="2f2a9-112">Se reconocen dos tipos de estado:</span><span class="sxs-lookup"><span data-stu-id="2f2a9-112">Two kinds of state are recognized:</span></span>

-   <span data-ttu-id="2f2a9-113">Estado necesario para admitir el acceso a los datos a los volúmenes contenidos en una instantánea de hardware.</span><span class="sxs-lookup"><span data-stu-id="2f2a9-113">State necessary to support data access to the volumes contained on a hardware shadow copy.</span></span> <span data-ttu-id="2f2a9-114">Esto incluye cualquier etiquetado de un volumen como de solo lectura u oculto.</span><span class="sxs-lookup"><span data-stu-id="2f2a9-114">This includes any tagging of a volume as read-only or hidden.</span></span> <span data-ttu-id="2f2a9-115">Este estado debe estar en el LUN de hardware y viajar con el LUN.</span><span class="sxs-lookup"><span data-stu-id="2f2a9-115">This state must be on the hardware LUN and travel with the LUN.</span></span> <span data-ttu-id="2f2a9-116">Este estado se conserva entre el tiempo de arranque y/o la detección de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="2f2a9-116">This state is preserved across boot epochs and/or device discovery.</span></span> <span data-ttu-id="2f2a9-117">VSS administra este estado durante la vigencia de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="2f2a9-117">VSS manages this state for the lifetime of the shadow copy.</span></span>
-   <span data-ttu-id="2f2a9-118">Estado necesario para reconocer un volumen específico como parte de un conjunto de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="2f2a9-118">State necessary to recognize a specific volume as part of a shadow copy set.</span></span> <span data-ttu-id="2f2a9-119">VSS conserva este estado junto con el solicitante que creó originalmente el conjunto de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="2f2a9-119">This state is persisted by VSS in conjunction with the requester that originally created the shadow copy set.</span></span>

<span data-ttu-id="2f2a9-120">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="2f2a9-120">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="2f2a9-121">Proceso de creación de instantáneas</span><span class="sxs-lookup"><span data-stu-id="2f2a9-121">The Shadow Copy Creation Process</span></span>](the-shadow-copy-creation-process.md)
-   [<span data-ttu-id="2f2a9-122">Comportamientos necesarios para los proveedores de instantáneas</span><span class="sxs-lookup"><span data-stu-id="2f2a9-122">Required Behaviors for Shadow Copy Providers</span></span>](required-behaviors-for-shadow-copy-providers.md)
-   [<span data-ttu-id="2f2a9-123">Transiciones de estado en proveedores de instantáneas</span><span class="sxs-lookup"><span data-stu-id="2f2a9-123">State Transitions in shadow copy providers</span></span>](state-transitions-in-shadow-copy-providers.md)
-   [<span data-ttu-id="2f2a9-124">Control de errores en los proveedores de instantáneas</span><span class="sxs-lookup"><span data-stu-id="2f2a9-124">Error Handling in shadow copy providers</span></span>](error-handling-in-shadow-copy-providers.md)

 

 



