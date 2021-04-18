---
title: Método GetFile de IBackgroundCopyError (Deliveryoptimization. h)
description: Recupera un puntero de interfaz al objeto de archivo asociado al error.
ms.assetid: 7E1DB3EE-0690-4D0E-BA98-70F5FBDCF12F
keywords:
- GetFile (método)
- Método GetFile, interfaz IBackgroundCopyError
- Interfaz IBackgroundCopyError, método GetFile
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b84396797378c77a6f774b4c63a3966b0d601b7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105720214"
---
# <a name="ibackgroundcopyerrorgetfile-method"></a><span data-ttu-id="75092-106">IBackgroundCopyError:: GetFile (método)</span><span class="sxs-lookup"><span data-stu-id="75092-106">IBackgroundCopyError::GetFile method</span></span>

<span data-ttu-id="75092-107">Recupera un puntero de interfaz al objeto de archivo asociado al error.</span><span class="sxs-lookup"><span data-stu-id="75092-107">Retrieves an interface pointer to the file object associated with the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="75092-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75092-108">Syntax</span></span>


```C++
HRESULT GetFile(
  [out] IBackgroundCopyFile **ppFile
);
```



## <a name="parameters"></a><span data-ttu-id="75092-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75092-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75092-110">*ppFile* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="75092-110">*ppFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75092-111">Puntero a la interfaz [**IBackgroundCopyFile**](ibackgroundcopyfile.md) cuyos métodos se usan para determinar los nombres de archivo locales y remotos asociados al error.</span><span class="sxs-lookup"><span data-stu-id="75092-111">An [**IBackgroundCopyFile**](ibackgroundcopyfile.md) interface pointer whose methods you use to determine the local and remote file names associated with the error.</span></span> <span data-ttu-id="75092-112">El parámetro *ppFile* se establece en **null** si el error no está asociado con el archivo local o remoto.</span><span class="sxs-lookup"><span data-stu-id="75092-112">The *ppFile* parameter is set to **NULL** if the error is not associated with the local or remote file.</span></span> <span data-ttu-id="75092-113">Cuando termine, libere *ppFile*.</span><span class="sxs-lookup"><span data-stu-id="75092-113">When done, release *ppFile*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75092-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75092-114">Return value</span></span>

<span data-ttu-id="75092-115">Este método devuelve los siguientes valores **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="75092-115">This method returns the following **HRESULT** values.</span></span>



| <span data-ttu-id="75092-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="75092-116">Return code</span></span>                                                                                                | <span data-ttu-id="75092-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="75092-117">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="75092-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="75092-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>                   | <span data-ttu-id="75092-119">Un puntero de interfaz se recuperó correctamente en el objeto de archivo.</span><span class="sxs-lookup"><span data-stu-id="75092-119">Successfully retrieved an interface pointer to the file object.</span></span><br/>                                     |
| <dl> <span data-ttu-id="75092-120"><dt>**DO_E_FILE_NOT_AVAILABLE**</dt></span><span class="sxs-lookup"><span data-stu-id="75092-120"><dt>**DO_E_FILE_NOT_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="75092-121">El error no está asociado a un archivo local o remoto.</span><span class="sxs-lookup"><span data-stu-id="75092-121">The error is not associated with a local or remote file.</span></span> <span data-ttu-id="75092-122">El parámetro *ppFile* se establece en **null**.</span><span class="sxs-lookup"><span data-stu-id="75092-122">The *ppFile* parameter is set to **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="75092-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75092-123">Requirements</span></span>



| <span data-ttu-id="75092-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="75092-124">Requirement</span></span> | <span data-ttu-id="75092-125">Value</span><span class="sxs-lookup"><span data-stu-id="75092-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75092-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75092-126">Minimum supported client</span></span><br/> | <span data-ttu-id="75092-127">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="75092-127">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="75092-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75092-128">Minimum supported server</span></span><br/> | <span data-ttu-id="75092-129">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="75092-129">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="75092-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="75092-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="75092-131"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="75092-131"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="75092-132">IDL</span><span class="sxs-lookup"><span data-stu-id="75092-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="75092-133"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="75092-133"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="75092-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="75092-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="75092-135"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75092-135"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="75092-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="75092-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75092-137"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75092-137"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="75092-138">IID</span><span class="sxs-lookup"><span data-stu-id="75092-138">IID</span></span><br/>                      | <span data-ttu-id="75092-139">IID_IBackgroundCopyError se define como 19C613A0-FCB8-4F28-81AE-897C3D078F81</span><span class="sxs-lookup"><span data-stu-id="75092-139">IID_IBackgroundCopyError is defined as 19C613A0-FCB8-4F28-81AE-897C3D078F81</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="75092-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="75092-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75092-141">**IBackgroundCopyError**</span><span class="sxs-lookup"><span data-stu-id="75092-141">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="75092-142">**IBackgroundCopyError::GetError**</span><span class="sxs-lookup"><span data-stu-id="75092-142">**IBackgroundCopyError::GetError**</span></span>](ibackgroundcopyerror-geterror-method.md)
</dt> </dl>

 

 





