---
title: Interfaz IBackgroundCopyError (Deliveryoptimization. h)
description: Use la interfaz IBackgroundCopyError para determinar la causa de un error y si el proceso de transferencia puede continuar.
ms.assetid: 7DCB63CF-4180-4DC3-9093-07C4F8CF7A8E
keywords:
- Interfaz IBackgroundCopyError
- Interfaz IBackgroundCopyError, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f35365d56ce9391a746e479e1b59034342ebf62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490264"
---
# <a name="ibackgroundcopyerror-interface"></a><span data-ttu-id="5682c-105">Interfaz IBackgroundCopyError</span><span class="sxs-lookup"><span data-stu-id="5682c-105">IBackgroundCopyError interface</span></span>

<span data-ttu-id="5682c-106">Use la interfaz **IBackgroundCopyError** para determinar la causa de un error y si el proceso de transferencia puede continuar.</span><span class="sxs-lookup"><span data-stu-id="5682c-106">Use the **IBackgroundCopyError** interface to determine the cause of an error and if the transfer process can proceed.</span></span>

<span data-ttu-id="5682c-107">Crea un objeto de error solo cuando el estado del trabajo es BG_JOB_STATE_ERROR o BG_JOB_STATE_TRANSIENT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="5682c-107">DO creates an error object only when the state of the job is BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSIENT_ERROR.</span></span> <span data-ttu-id="5682c-108">No crea un objeto de error cuando se produce un error en un método de la interfaz **IBackgroundCopyXXXX** .</span><span class="sxs-lookup"><span data-stu-id="5682c-108">DO does not create an error object when an **IBackgroundCopyXXXX** interface method fails.</span></span> <span data-ttu-id="5682c-109">El objeto de error está disponible hasta que comienza la transferencia de datos (el estado del trabajo cambia a BG_JOB_STATE_TRANSFERRING) del trabajo.</span><span class="sxs-lookup"><span data-stu-id="5682c-109">The error object is available until DO begins transferring data (the state of the job changes to BG_JOB_STATE_TRANSFERRING) for the job.</span></span>

<span data-ttu-id="5682c-110">Para obtener un objeto **IBackgroundCopyError** , llame al método [**IBackgroundCopyJob:: GetError**](ibackgroundcopyjob-geterror.md) .</span><span class="sxs-lookup"><span data-stu-id="5682c-110">To get an **IBackgroundCopyError** object, call the [**IBackgroundCopyJob::GetError**](ibackgroundcopyjob-geterror.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="5682c-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="5682c-111">Members</span></span>

<span data-ttu-id="5682c-112">La interfaz **IBackgroundCopyError** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5682c-112">The **IBackgroundCopyError** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5682c-113">**IBackgroundCopyError** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5682c-113">**IBackgroundCopyError** also has these types of members:</span></span>

-   [<span data-ttu-id="5682c-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="5682c-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5682c-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="5682c-115">Methods</span></span>

<span data-ttu-id="5682c-116">La interfaz **IBackgroundCopyError** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5682c-116">The **IBackgroundCopyError** interface has these methods.</span></span>



| <span data-ttu-id="5682c-117">Método</span><span class="sxs-lookup"><span data-stu-id="5682c-117">Method</span></span>                                                   | <span data-ttu-id="5682c-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="5682c-118">Description</span></span>                                                                                 |
|:---------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5682c-119">**GetError**</span><span class="sxs-lookup"><span data-stu-id="5682c-119">**GetError**</span></span>](ibackgroundcopyerror-geterror-method.md) | <span data-ttu-id="5682c-120">Recupera el código de error e identifica el contexto en el que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="5682c-120">Retrieves the error code and identifies the context in which the error occurred.</span></span><br/> |
| [<span data-ttu-id="5682c-121">**GetFile**</span><span class="sxs-lookup"><span data-stu-id="5682c-121">**GetFile**</span></span>](ibackgroundcopyerror-getfile-method.md)   | <span data-ttu-id="5682c-122">Recupera un puntero de interfaz al objeto de archivo asociado al error.</span><span class="sxs-lookup"><span data-stu-id="5682c-122">Retrieves an interface pointer to the file object associated with the error.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="5682c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5682c-123">Requirements</span></span>



| <span data-ttu-id="5682c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5682c-124">Requirement</span></span> | <span data-ttu-id="5682c-125">Value</span><span class="sxs-lookup"><span data-stu-id="5682c-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5682c-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5682c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5682c-127">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="5682c-127">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5682c-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5682c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5682c-129">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="5682c-129">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5682c-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5682c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5682c-131"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="5682c-131"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="5682c-132">IDL</span><span class="sxs-lookup"><span data-stu-id="5682c-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5682c-133"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5682c-133"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="5682c-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5682c-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="5682c-135"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5682c-135"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="5682c-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5682c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5682c-137"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5682c-137"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="5682c-138">IID</span><span class="sxs-lookup"><span data-stu-id="5682c-138">IID</span></span><br/>                      | <span data-ttu-id="5682c-139">IID_IBackgroundCopyError se define como 19C613A0-FCB8-4F28-81AE-897C3D078F81</span><span class="sxs-lookup"><span data-stu-id="5682c-139">IID_IBackgroundCopyError is defined as 19C613A0-FCB8-4F28-81AE-897C3D078F81</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="5682c-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="5682c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5682c-141">**BG_JOB_STATE**</span><span class="sxs-lookup"><span data-stu-id="5682c-141">**BG_JOB_STATE**</span></span>](bg-job-state-.md)
</dt> <dt>

[<span data-ttu-id="5682c-142">**IBackgroundCopyJob::GetError**</span><span class="sxs-lookup"><span data-stu-id="5682c-142">**IBackgroundCopyJob::GetError**</span></span>](ibackgroundcopyjob-geterror.md)
</dt> <dt>

[<span data-ttu-id="5682c-143">**IBackgroundCopyJob:: GetState**</span><span class="sxs-lookup"><span data-stu-id="5682c-143">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> <dt>

[<span data-ttu-id="5682c-144">**IBackgroundCopyCallback::JobError**</span><span class="sxs-lookup"><span data-stu-id="5682c-144">**IBackgroundCopyCallback::JobError**</span></span>](ibackgroundcopycallback-joberror-method.md)
</dt> </dl>

 

