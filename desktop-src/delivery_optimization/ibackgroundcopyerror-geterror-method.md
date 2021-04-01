---
title: Método IBackgroundCopyError GetError (Deliveryoptimization. h)
description: Recupera el código de error e identifica el contexto en el que se produjo el error.
ms.assetid: C87897CD-9648-4CEF-B963-68EE35356929
keywords:
- Método GetError
- Método GetError, interfaz IBackgroundCopyError
- Interfaz IBackgroundCopyError, método GetError
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e14803c225ade6085658582e18b9ba2d52fc90c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996301"
---
# <a name="ibackgroundcopyerrorgeterror-method"></a><span data-ttu-id="598e9-106">IBackgroundCopyError:: GetError (método)</span><span class="sxs-lookup"><span data-stu-id="598e9-106">IBackgroundCopyError::GetError method</span></span>

<span data-ttu-id="598e9-107">Recupera el código de error e identifica el contexto en el que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="598e9-107">Retrieves the error code and identify the context in which the error occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="598e9-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="598e9-108">Syntax</span></span>


```C++
HRESULT GetError(
  [out] BG_ERROR_CONTEXT *pContext,
  [out] HRESULT          *pErrorCode
);
```



## <a name="parameters"></a><span data-ttu-id="598e9-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="598e9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="598e9-110">*pContext* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="598e9-110">*pContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="598e9-111">Contexto en el que se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="598e9-111">Context in which the error occurred.</span></span> <span data-ttu-id="598e9-112">Para obtener una lista de valores de contexto, consulte la enumeración [**BG_ERROR_CONTEXT**](bg-error-context.md) .</span><span class="sxs-lookup"><span data-stu-id="598e9-112">For a list of context values, see the [**BG_ERROR_CONTEXT**](bg-error-context.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="598e9-113">*pErrorCode* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="598e9-113">*pErrorCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="598e9-114">Código de error del error que se ha producido.</span><span class="sxs-lookup"><span data-stu-id="598e9-114">Error code of the error that occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="598e9-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="598e9-115">Return value</span></span>

<span data-ttu-id="598e9-116">Este método devuelve **S_OK** si se ejecuta correctamente o uno de los valores de HRESULT de com estándar en caso de error.</span><span class="sxs-lookup"><span data-stu-id="598e9-116">This method returns **S_OK** on success or one of the standard COM HRESULT values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="598e9-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="598e9-117">Requirements</span></span>



| <span data-ttu-id="598e9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="598e9-118">Requirement</span></span> | <span data-ttu-id="598e9-119">Value</span><span class="sxs-lookup"><span data-stu-id="598e9-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="598e9-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="598e9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="598e9-121">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="598e9-121">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="598e9-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="598e9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="598e9-123">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="598e9-123">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="598e9-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="598e9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="598e9-125"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="598e9-125"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="598e9-126">IDL</span><span class="sxs-lookup"><span data-stu-id="598e9-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="598e9-127"><dt>DeliveryOptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="598e9-127"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="598e9-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="598e9-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="598e9-129"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="598e9-129"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="598e9-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="598e9-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="598e9-131"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="598e9-131"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="598e9-132">IID</span><span class="sxs-lookup"><span data-stu-id="598e9-132">IID</span></span><br/>                      | <span data-ttu-id="598e9-133">IID_IBackgroundCopyError se define como 19C613A0-FCB8-4F28-81AE-897C3D078F81</span><span class="sxs-lookup"><span data-stu-id="598e9-133">IID_IBackgroundCopyError is defined as 19C613A0-FCB8-4F28-81AE-897C3D078F81</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="598e9-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="598e9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="598e9-135">**IBackgroundCopyError**</span><span class="sxs-lookup"><span data-stu-id="598e9-135">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="598e9-136">**IBackgroundCopyError:: GetFile**</span><span class="sxs-lookup"><span data-stu-id="598e9-136">**IBackgroundCopyError::GetFile**</span></span>](ibackgroundcopyerror-getfile-method.md)
</dt> </dl>

 

 





