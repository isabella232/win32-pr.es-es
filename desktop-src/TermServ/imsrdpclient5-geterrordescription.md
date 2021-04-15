---
title: IMsRdpClient5 GetErrorDescription, método
description: Recupera la descripción del error para los eventos de desconexión de la sesión.
ms.assetid: 8c8f7b10-7f79-4586-845e-e99f5ca81905
ms.tgt_platform: multiple
keywords:
- Método GetErrorDescription Servicios de Escritorio remoto
- Método GetErrorDescription Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto, método GetErrorDescription
- Método GetErrorDescription Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto, método GetErrorDescription
- Método GetErrorDescription Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto, método GetErrorDescription
- Método GetErrorDescription Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto, método GetErrorDescription
- Método GetErrorDescription Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto, método GetErrorDescription
- Método GetErrorDescription Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto, método GetErrorDescription
topic_type:
- apiref
api_name:
- IMsRdpClient5.GetErrorDescription
- IMsRdpClient6.GetErrorDescription
- IMsRdpClient7.GetErrorDescription
- IMsRdpClient8.GetErrorDescription
- IMsRdpClient9.GetErrorDescription
- IMsRdpClient10.GetErrorDescription
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c402a0128286964ddeb1c53cd805e4ef6414bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422571"
---
# <a name="imsrdpclient5geterrordescription-method"></a><span data-ttu-id="e60c9-116">IMsRdpClient5:: GetErrorDescription (método)</span><span class="sxs-lookup"><span data-stu-id="e60c9-116">IMsRdpClient5::GetErrorDescription method</span></span>

<span data-ttu-id="e60c9-117">Recupera la descripción del error para los eventos de desconexión de la sesión.</span><span class="sxs-lookup"><span data-stu-id="e60c9-117">Retrieves the error description for the session disconnect events.</span></span>

## <a name="syntax"></a><span data-ttu-id="e60c9-118">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e60c9-118">Syntax</span></span>


```C++
HRESULT GetErrorDescription(
  [in]  UINT disconnectReason,
  [in]  UINT extendedDisconnectReason,
  [out] BSTR *pBstrErrorMsg
);
```



## <a name="parameters"></a><span data-ttu-id="e60c9-119">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e60c9-119">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e60c9-120">*disconnectReason* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e60c9-120">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e60c9-121">Motivo de la desconexión.</span><span class="sxs-lookup"><span data-stu-id="e60c9-121">The disconnect reason.</span></span>

</dd> <dt>

<span data-ttu-id="e60c9-122">*extendedDisconnectReason* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e60c9-122">*extendedDisconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e60c9-123">Proporciona información detallada sobre por qué se inició una desconexión.</span><span class="sxs-lookup"><span data-stu-id="e60c9-123">Provides detailed information about why a disconnect was initiated.</span></span>

</dd> <dt>

<span data-ttu-id="e60c9-124">*pBstrErrorMsg* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e60c9-124">*pBstrErrorMsg* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e60c9-125">Puntero a una variable **BSTR** que recibe el texto del mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="e60c9-125">A pointer to a **BSTR** variable that receives the error message text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e60c9-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e60c9-126">Return value</span></span>

<span data-ttu-id="e60c9-127">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e60c9-127">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e60c9-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e60c9-128">Requirements</span></span>



| <span data-ttu-id="e60c9-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e60c9-129">Requirement</span></span> | <span data-ttu-id="e60c9-130">Value</span><span class="sxs-lookup"><span data-stu-id="e60c9-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e60c9-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e60c9-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e60c9-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e60c9-132">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e60c9-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e60c9-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e60c9-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e60c9-134">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e60c9-135">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e60c9-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="e60c9-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e60c9-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e60c9-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e60c9-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e60c9-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e60c9-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e60c9-139">IID</span><span class="sxs-lookup"><span data-stu-id="e60c9-139">IID</span></span><br/>                      | <span data-ttu-id="e60c9-140">IID \_ IMsRdpClient5 se define como 4eb5335b-6429-477d-B922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="e60c9-140">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e60c9-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="e60c9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e60c9-142">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="e60c9-142">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="e60c9-143">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="e60c9-143">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="e60c9-144">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="e60c9-144">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="e60c9-145">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="e60c9-145">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="e60c9-146">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="e60c9-146">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="e60c9-147">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="e60c9-147">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





