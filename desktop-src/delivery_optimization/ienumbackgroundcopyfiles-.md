---
title: Interfaz IEnumBackgroundCopyFiles (Deliveryoptimization. h)
description: Use la interfaz IEnumBackgroundCopyFiles para enumerar los archivos que contiene un trabajo. Para obtener un puntero de interfaz IEnumBackgroundCopyFiles, llame al método IBackgroundCopyJob Enumfiles (.
ms.assetid: 539973BA-2756-4163-9D8B-4B7C0A708A8D
keywords:
- Interfaz IEnumBackgroundCopyFiles
- Interfaz IEnumBackgroundCopyFiles, descrita
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e46e94139a0c82e6c5b45f9397d76de8b4fdb43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714587"
---
# <a name="ienumbackgroundcopyfiles-interface"></a><span data-ttu-id="3ee92-106">Interfaz IEnumBackgroundCopyFiles</span><span class="sxs-lookup"><span data-stu-id="3ee92-106">IEnumBackgroundCopyFiles interface</span></span>

<span data-ttu-id="3ee92-107">Use la interfaz **IEnumBackgroundCopyFiles** para enumerar los archivos que contiene un trabajo.</span><span class="sxs-lookup"><span data-stu-id="3ee92-107">Use the **IEnumBackgroundCopyFiles** interface to enumerate the files that a job contains.</span></span> <span data-ttu-id="3ee92-108">Para obtener un puntero de interfaz **IEnumBackgroundCopyFiles** , llame al método [**IBackgroundCopyJob:: enumfiles (**](ibackgroundcopyjob-enumfiles.md) .</span><span class="sxs-lookup"><span data-stu-id="3ee92-108">To get an **IEnumBackgroundCopyFiles** interface pointer, call the [**IBackgroundCopyJob::EnumFiles**](ibackgroundcopyjob-enumfiles.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="3ee92-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="3ee92-109">Members</span></span>

<span data-ttu-id="3ee92-110">La interfaz **IEnumBackgroundCopyFiles** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3ee92-110">The **IEnumBackgroundCopyFiles** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3ee92-111">**IEnumBackgroundCopyFiles** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3ee92-111">**IEnumBackgroundCopyFiles** also has these types of members:</span></span>

-   [<span data-ttu-id="3ee92-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="3ee92-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3ee92-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="3ee92-113">Methods</span></span>

<span data-ttu-id="3ee92-114">La interfaz **IEnumBackgroundCopyFiles** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="3ee92-114">The **IEnumBackgroundCopyFiles** interface has these methods.</span></span>



| <span data-ttu-id="3ee92-115">Método</span><span class="sxs-lookup"><span data-stu-id="3ee92-115">Method</span></span>                                                | <span data-ttu-id="3ee92-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ee92-116">Description</span></span>                                                                   |
|:------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="3ee92-117">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="3ee92-117">**GetCount**</span></span>](ienumbackgroundcopyfiles-getcount.md) | <span data-ttu-id="3ee92-118">Recupera el número de elementos de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="3ee92-118">Retrieves the number of items in the enumeration.</span></span><br/>                  |
| [<span data-ttu-id="3ee92-119">**Next**</span><span class="sxs-lookup"><span data-stu-id="3ee92-119">**Next**</span></span>](ienumbackgroundcopyfiles-next.md)         | <span data-ttu-id="3ee92-120">Recupera un número especificado de elementos en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="3ee92-120">Retrieves a specified number of items in the enumeration sequence.</span></span><br/> |
| [<span data-ttu-id="3ee92-121">**Reset**</span><span class="sxs-lookup"><span data-stu-id="3ee92-121">**Reset**</span></span>](ienumbackgroundcopyfiles-reset.md)       | <span data-ttu-id="3ee92-122">Restablece la secuencia de enumeración al principio.</span><span class="sxs-lookup"><span data-stu-id="3ee92-122">Resets the enumeration sequence to the beginning.</span></span><br/>                  |
| [<span data-ttu-id="3ee92-123">**Omitir**</span><span class="sxs-lookup"><span data-stu-id="3ee92-123">**Skip**</span></span>](ienumbackgroundcopyfiles-skip.md)         | <span data-ttu-id="3ee92-124">Omite un número especificado de elementos en la secuencia de enumeración.</span><span class="sxs-lookup"><span data-stu-id="3ee92-124">Skips a specified number of items in the enumeration sequence.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="3ee92-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ee92-125">Requirements</span></span>



| <span data-ttu-id="3ee92-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ee92-126">Requirement</span></span> | <span data-ttu-id="3ee92-127">Value</span><span class="sxs-lookup"><span data-stu-id="3ee92-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ee92-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ee92-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3ee92-129">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="3ee92-129">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3ee92-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ee92-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3ee92-131">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="3ee92-131">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="3ee92-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3ee92-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ee92-133"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ee92-133"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="3ee92-134">IDL</span><span class="sxs-lookup"><span data-stu-id="3ee92-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3ee92-135"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3ee92-135"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="3ee92-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3ee92-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="3ee92-137"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ee92-137"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="3ee92-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3ee92-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ee92-139"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ee92-139"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="3ee92-140">IID</span><span class="sxs-lookup"><span data-stu-id="3ee92-140">IID</span></span><br/>                      | <span data-ttu-id="3ee92-141">IID_IEnumBackgroundCopyFiles se define como CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="3ee92-141">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="3ee92-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ee92-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ee92-143">**IBackgroundCopyJob:: Enumfiles (**</span><span class="sxs-lookup"><span data-stu-id="3ee92-143">**IBackgroundCopyJob::EnumFiles**</span></span>](ibackgroundcopyjob-enumfiles.md)
</dt> </dl>

 

