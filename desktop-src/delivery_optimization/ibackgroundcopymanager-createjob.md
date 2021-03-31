---
title: Método IBackgroundCopyManager::CreateJob (Deliveryoptimization.h)
description: Crea un trabajo.
ms.assetid: BDE5BE4D-9AE9-463D-B900-850D255EAB58
keywords:
- Método CreateJob
- Método CreateJob, interfaz IBackgroundCopyManager
- Interfaz IBackgroundCopyManager, método CreateJob
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.CreateJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de7f0b61cdbc5d5776039c3bf13b83ca0a6f8fdc
ms.sourcegitcommit: ea73413ee4f69fa573ee0cd4422f20d17bd42e1f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/27/2021
ms.locfileid: "104083511"
---
# <a name="ibackgroundcopymanagercreatejob-method"></a><span data-ttu-id="7ffbf-106">IBackgroundCopyManager:: CreateJob (método)</span><span class="sxs-lookup"><span data-stu-id="7ffbf-106">IBackgroundCopyManager::CreateJob method</span></span>

<span data-ttu-id="7ffbf-107">Crea un trabajo.</span><span class="sxs-lookup"><span data-stu-id="7ffbf-107">Creates a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ffbf-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7ffbf-108">Syntax</span></span>


```C++
HRESULT CreateJob(
  [in]  LPCWSTR            pDisplayName,
  [in]  BG_JOB_TYPE        Type,
  [out] GUID               *pJobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a><span data-ttu-id="7ffbf-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7ffbf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ffbf-110">*pDisplayName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7ffbf-110">*pDisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ffbf-111">Cadena terminada en null que contiene un nombre para mostrar del trabajo.</span><span class="sxs-lookup"><span data-stu-id="7ffbf-111">Null-terminated string that contains a display name for the job.</span></span> <span data-ttu-id="7ffbf-112">Normalmente, el nombre para mostrar se usa para identificar el trabajo en una interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="7ffbf-112">Typically, the display name is used to identify the job in a user interface.</span></span> <span data-ttu-id="7ffbf-113">Tenga en cuenta que más de un trabajo puede tener el mismo nombre para mostrar.</span><span class="sxs-lookup"><span data-stu-id="7ffbf-113">Note that more than one job may have the same display name.</span></span> <span data-ttu-id="7ffbf-114">No debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="7ffbf-114">Must not be **NULL**.</span></span> <span data-ttu-id="7ffbf-115">El nombre está limitado a 256 caracteres, sin incluir el terminador nulo.</span><span class="sxs-lookup"><span data-stu-id="7ffbf-115">The name is limited to 256 characters, not including the null terminator.</span></span>

</dd> <dt>

<span data-ttu-id="7ffbf-116">*Tipo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="7ffbf-116">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ffbf-117">Tipo de trabajo de transferencia, como BG_JOB_TYPE_DOWNLOAD.</span><span class="sxs-lookup"><span data-stu-id="7ffbf-117">Type of transfer job, such as BG_JOB_TYPE_DOWNLOAD.</span></span> <span data-ttu-id="7ffbf-118">Para obtener una lista de tipos de transferencia, vea la enumeración [**BG_JOB_TYPE**](bg-job-type.md) .</span><span class="sxs-lookup"><span data-stu-id="7ffbf-118">For a list of transfer types, see the [**BG_JOB_TYPE**](bg-job-type.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="7ffbf-119">*pJobID* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7ffbf-119">*pJobID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ffbf-120">Identifica de forma única el trabajo en la cola.</span><span class="sxs-lookup"><span data-stu-id="7ffbf-120">Uniquely identifies your job in the queue.</span></span> <span data-ttu-id="7ffbf-121">Use este identificador al llamar al método [**IBackgroundCopyManager:: GetJob**](ibackgroundcopymanager-getjob.md) para obtener un trabajo de la cola.</span><span class="sxs-lookup"><span data-stu-id="7ffbf-121">Use this identifier when you call the [**IBackgroundCopyManager::GetJob**](ibackgroundcopymanager-getjob.md) method to get a job from the queue.</span></span>

</dd> <dt>

<span data-ttu-id="7ffbf-122">*ppJob* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7ffbf-122">*ppJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ffbf-123">Puntero de interfaz [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) que se usa para modificar las propiedades del trabajo y especificar los archivos que se van a transferir.</span><span class="sxs-lookup"><span data-stu-id="7ffbf-123">An [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) interface pointer that you use to modify the job's properties and specify the files to be transferred.</span></span> <span data-ttu-id="7ffbf-124">Para activar el trabajo en la cola, llame al método [**IBackgroundCopyJob:: resume**](ibackgroundcopyjob-resume.md) .</span><span class="sxs-lookup"><span data-stu-id="7ffbf-124">To activate the job in the queue, call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method.</span></span> <span data-ttu-id="7ffbf-125">Suelte *ppJob* cuando termine.</span><span class="sxs-lookup"><span data-stu-id="7ffbf-125">Release *ppJob* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ffbf-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7ffbf-126">Return value</span></span>

<span data-ttu-id="7ffbf-127">Este método devuelve los siguientes valores **HRESULT** , así como otros.</span><span class="sxs-lookup"><span data-stu-id="7ffbf-127">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="7ffbf-128">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="7ffbf-128">Return code</span></span>                                                                              | <span data-ttu-id="7ffbf-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ffbf-129">Description</span></span>                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="7ffbf-130"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="7ffbf-130"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="7ffbf-131">El nuevo trabajo se generó correctamente.</span><span class="sxs-lookup"><span data-stu-id="7ffbf-131">Successfully generated the new job.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7ffbf-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7ffbf-132">Remarks</span></span>

<span data-ttu-id="7ffbf-133">Solo el usuario que crea el trabajo o un usuario con privilegios de administrador puede [Agregar archivos al trabajo](https://www.bing.com/search?q=add+files+to+the+job) y [cambiar las propiedades del trabajo](https://www.bing.com/search?q=change+the+job's+properties).</span><span class="sxs-lookup"><span data-stu-id="7ffbf-133">Only the user who creates the job or a user with administrator privileges can [add files to the job](https://www.bing.com/search?q=add+files+to+the+job) and [change the job's properties](https://www.bing.com/search?q=change+the+job's+properties).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ffbf-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ffbf-134">Requirements</span></span>



| <span data-ttu-id="7ffbf-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ffbf-135">Requirement</span></span> | <span data-ttu-id="7ffbf-136">Value</span><span class="sxs-lookup"><span data-stu-id="7ffbf-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ffbf-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ffbf-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7ffbf-138">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="7ffbf-138">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7ffbf-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7ffbf-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7ffbf-140">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="7ffbf-140">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7ffbf-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7ffbf-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ffbf-142"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ffbf-142"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="7ffbf-143">IDL</span><span class="sxs-lookup"><span data-stu-id="7ffbf-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7ffbf-144"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7ffbf-144"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="7ffbf-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7ffbf-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="7ffbf-146"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ffbf-146"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="7ffbf-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7ffbf-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ffbf-148"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ffbf-148"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="7ffbf-149">IID</span><span class="sxs-lookup"><span data-stu-id="7ffbf-149">IID</span></span><br/>                      | <span data-ttu-id="7ffbf-150">IID_IBackgroundCopyManager se define como 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span><span class="sxs-lookup"><span data-stu-id="7ffbf-150">IID_IBackgroundCopyManager is defined as 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="7ffbf-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="7ffbf-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ffbf-152">**IBackgroundCopyManager**</span><span class="sxs-lookup"><span data-stu-id="7ffbf-152">**IBackgroundCopyManager**</span></span>](ibackgroundcopymanager.md)
</dt> <dt>

[<span data-ttu-id="7ffbf-153">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="7ffbf-153">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="7ffbf-154">**IBackgroundCopyJob:: resume**</span><span class="sxs-lookup"><span data-stu-id="7ffbf-154">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> </dl>
