---
title: Interfaz IBackgroundCopyManager (Deliveryoptimization. h)
description: Crea trabajos de transferencia, recupera un objeto de enumerador que contiene los trabajos de la cola y recupera trabajos individuales de la cola.
ms.assetid: EA7CB5CE-5E95-4C6D-8026-4B8375EE216A
keywords:
- Interfaz IBackgroundCopyManager
- Interfaz IBackgroundCopyManager, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyManager
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6fa752398c0849c987e2a28b804e65a8361e15b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996514"
---
# <a name="ibackgroundcopymanager-interface"></a><span data-ttu-id="b8050-105">Interfaz IBackgroundCopyManager</span><span class="sxs-lookup"><span data-stu-id="b8050-105">IBackgroundCopyManager interface</span></span>

<span data-ttu-id="b8050-106">Crea trabajos de transferencia, recupera un objeto de enumerador que contiene los trabajos de la cola y recupera trabajos individuales de la cola.</span><span class="sxs-lookup"><span data-stu-id="b8050-106">Creates transfer jobs, retrieves an enumerator object that contains the jobs in the queue, and retrieves individual jobs from the queue.</span></span>

## <a name="members"></a><span data-ttu-id="b8050-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="b8050-107">Members</span></span>

<span data-ttu-id="b8050-108">La interfaz **IBackgroundCopyManager** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b8050-108">The **IBackgroundCopyManager** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b8050-109">**IBackgroundCopyManager** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b8050-109">**IBackgroundCopyManager** also has these types of members:</span></span>

-   [<span data-ttu-id="b8050-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="b8050-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b8050-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="b8050-111">Methods</span></span>

<span data-ttu-id="b8050-112">La interfaz **IBackgroundCopyManager** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="b8050-112">The **IBackgroundCopyManager** interface has these methods.</span></span>



| <span data-ttu-id="b8050-113">Método</span><span class="sxs-lookup"><span data-stu-id="b8050-113">Method</span></span>                                                | <span data-ttu-id="b8050-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8050-114">Description</span></span>                                          |
|:------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="b8050-115">**CreateJob**</span><span class="sxs-lookup"><span data-stu-id="b8050-115">**CreateJob**</span></span>](ibackgroundcopymanager-createjob.md) | <span data-ttu-id="b8050-116">Crea un trabajo de transferencia.</span><span class="sxs-lookup"><span data-stu-id="b8050-116">Creates a transfer job.</span></span><br/>                   |
| [<span data-ttu-id="b8050-117">**GetJob**</span><span class="sxs-lookup"><span data-stu-id="b8050-117">**GetJob**</span></span>](ibackgroundcopymanager-getjob.md)       | <span data-ttu-id="b8050-118">Recupera un trabajo especificado de la cola.</span><span class="sxs-lookup"><span data-stu-id="b8050-118">Retrieves a specified job from the queue.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b8050-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8050-119">Requirements</span></span>



| <span data-ttu-id="b8050-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8050-120">Requirement</span></span> | <span data-ttu-id="b8050-121">Value</span><span class="sxs-lookup"><span data-stu-id="b8050-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8050-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8050-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b8050-123">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="b8050-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b8050-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b8050-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b8050-125">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="b8050-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b8050-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b8050-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8050-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8050-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="b8050-128">IDL</span><span class="sxs-lookup"><span data-stu-id="b8050-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b8050-129"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b8050-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="b8050-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b8050-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="b8050-131"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b8050-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="b8050-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b8050-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8050-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8050-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="b8050-134">IID</span><span class="sxs-lookup"><span data-stu-id="b8050-134">IID</span></span><br/>                      | <span data-ttu-id="b8050-135">IID_IBackgroundCopyManager se define como 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span><span class="sxs-lookup"><span data-stu-id="b8050-135">IID_IBackgroundCopyManager is defined as 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="b8050-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8050-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8050-137">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="b8050-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

