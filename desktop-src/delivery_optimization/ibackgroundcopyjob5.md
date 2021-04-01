---
title: Interfaz IBackgroundCopyJob5 (Deliveryoptimization. h)
description: Use esta interfaz para consultar o establecer varios comportamientos opcionales de un trabajo.
ms.assetid: C4706E10-40E6-489B-9772-59D581781038
keywords:
- Interfaz IBackgroundCopyJob5
- Interfaz IBackgroundCopyJob5, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e76898f7bbfe4d4dc34aec035b842e6671091630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150834"
---
# <a name="ibackgroundcopyjob5-interface"></a><span data-ttu-id="6e922-105">Interfaz IBackgroundCopyJob5</span><span class="sxs-lookup"><span data-stu-id="6e922-105">IBackgroundCopyJob5 interface</span></span>

<span data-ttu-id="6e922-106">Use esta interfaz para consultar o establecer varios comportamientos opcionales de un trabajo.</span><span class="sxs-lookup"><span data-stu-id="6e922-106">Use this interface to query or set several optional behaviors of a job.</span></span>

<span data-ttu-id="6e922-107">Para obtener esta interfaz, llame al método **IBackgroundCopyJob:: QueryInterface** usando `__uuidof(IBackgroundCopyJob5)` como identificador de interfaz.</span><span class="sxs-lookup"><span data-stu-id="6e922-107">To get this interface, call the **IBackgroundCopyJob::QueryInterface** method using `__uuidof(IBackgroundCopyJob5)` as the interface identifier.</span></span>

## <a name="members"></a><span data-ttu-id="6e922-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="6e922-108">Members</span></span>

<span data-ttu-id="6e922-109">La interfaz **IBackgroundCopyJob5** hereda de [**IBackgroundCopyJob**](ibackgroundcopyjob-.md).</span><span class="sxs-lookup"><span data-stu-id="6e922-109">The **IBackgroundCopyJob5** interface inherits from [**IBackgroundCopyJob**](ibackgroundcopyjob-.md).</span></span> <span data-ttu-id="6e922-110">**IBackgroundCopyJob5** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6e922-110">**IBackgroundCopyJob5** also has these types of members:</span></span>

-   [<span data-ttu-id="6e922-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="6e922-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6e922-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="6e922-112">Methods</span></span>

<span data-ttu-id="6e922-113">La interfaz **IBackgroundCopyJob5** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="6e922-113">The **IBackgroundCopyJob5** interface has these methods.</span></span>



| <span data-ttu-id="6e922-114">Método</span><span class="sxs-lookup"><span data-stu-id="6e922-114">Method</span></span>                                                 | <span data-ttu-id="6e922-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e922-115">Description</span></span>                                                |
|:-------------------------------------------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="6e922-116">**GetProperty**</span><span class="sxs-lookup"><span data-stu-id="6e922-116">**GetProperty**</span></span>](ibackgroundcopyjob5-getproperty.md) | <span data-ttu-id="6e922-117">Método genérico para obtener las propiedades de los trabajos.</span><span class="sxs-lookup"><span data-stu-id="6e922-117">A generic method for getting DO job properties.</span></span><br/> |
| [<span data-ttu-id="6e922-118">**SetProperty**</span><span class="sxs-lookup"><span data-stu-id="6e922-118">**SetProperty**</span></span>](ibackgroundcopyjob5-setproperty.md) | <span data-ttu-id="6e922-119">Método genérico para establecer las propiedades de los trabajos.</span><span class="sxs-lookup"><span data-stu-id="6e922-119">A generic method for setting DO job properties.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6e922-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e922-120">Requirements</span></span>



| <span data-ttu-id="6e922-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e922-121">Requirement</span></span> | <span data-ttu-id="6e922-122">Value</span><span class="sxs-lookup"><span data-stu-id="6e922-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e922-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e922-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6e922-124">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="6e922-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6e922-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e922-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6e922-126">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="6e922-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6e922-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e922-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e922-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e922-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="6e922-129">IDL</span><span class="sxs-lookup"><span data-stu-id="6e922-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6e922-130"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6e922-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="6e922-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6e922-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="6e922-132"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6e922-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="6e922-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6e922-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e922-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e922-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="6e922-135">IID</span><span class="sxs-lookup"><span data-stu-id="6e922-135">IID</span></span><br/>                      | <span data-ttu-id="6e922-136">IID_IBackgroundCopyJob5 se define como E847030C-BBBA-4657-AF6D-484AA42BF1FE</span><span class="sxs-lookup"><span data-stu-id="6e922-136">IID_IBackgroundCopyJob5 is defined as E847030C-BBBA-4657-AF6D-484AA42BF1FE</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="6e922-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e922-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e922-138">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="6e922-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





