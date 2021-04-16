---
title: Propiedad BinaryPassword de IMsTscNonScriptable
description: Esta propiedad ya no está disponible para su uso. | Propiedad BinaryPassword de IMsTscNonScriptable
ms.assetid: b3be7323-a75f-4ec2-9d58-e8ff3338d6ff
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad BinaryPassword
- Propiedad BinaryPassword Servicios de Escritorio remoto, interfaz IMsTscNonScriptable
- Servicios de Escritorio remoto de la interfaz IMsTscNonScriptable, propiedad BinaryPassword
- Servicios de Escritorio remoto de la propiedad BinaryPassword, objeto MsTscAx
- Servicios de Escritorio remoto de objeto MsTscAx, propiedad BinaryPassword
- Propiedad BinaryPassword Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable, propiedad BinaryPassword
- Propiedad BinaryPassword Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable2, propiedad BinaryPassword
- Propiedad BinaryPassword Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad BinaryPassword
- Propiedad BinaryPassword Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad BinaryPassword
- Propiedad BinaryPassword Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad BinaryPassword
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.BinaryPassword
- IMsTscNonScriptable.get_BinaryPassword
- IMsTscNonScriptable.put_BinaryPassword
- MsTscAx.BinaryPassword
- IMsRdpClientNonScriptable.BinaryPassword
- IMsRdpClientNonScriptable.get_BinaryPassword
- IMsRdpClientNonScriptable.put_BinaryPassword
- IMsRdpClientNonScriptable2.BinaryPassword
- IMsRdpClientNonScriptable2.get_BinaryPassword
- IMsRdpClientNonScriptable2.put_BinaryPassword
- IMsRdpClientNonScriptable3.BinaryPassword
- IMsRdpClientNonScriptable3.get_BinaryPassword
- IMsRdpClientNonScriptable3.put_BinaryPassword
- IMsRdpClientNonScriptable4.BinaryPassword
- IMsRdpClientNonScriptable4.get_BinaryPassword
- IMsRdpClientNonScriptable4.put_BinaryPassword
- IMsRdpClientNonScriptable5.BinaryPassword
- IMsRdpClientNonScriptable5.get_BinaryPassword
- IMsRdpClientNonScriptable5.put_BinaryPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d6eab2a3902968ef4d4c953a8da8b9c884a497
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689739"
---
# <a name="imstscnonscriptablebinarypassword-property"></a><span data-ttu-id="28d9f-119">IMsTscNonScriptable:: BinaryPassword (propiedad)</span><span class="sxs-lookup"><span data-stu-id="28d9f-119">IMsTscNonScriptable::BinaryPassword property</span></span>

<span data-ttu-id="28d9f-120">Esta propiedad ya no está disponible para su uso.</span><span class="sxs-lookup"><span data-stu-id="28d9f-120">This property is no longer available for use.</span></span>

<span data-ttu-id="28d9f-121">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="28d9f-121">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="28d9f-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28d9f-122">Syntax</span></span>


```C++
HRESULT put_BinaryPassword(
  [in]  BSTR newPassword
);

HRESULT get_BinaryPassword(
  [out] BSTR *pBinaryPassword
);
```



## <a name="property-value"></a><span data-ttu-id="28d9f-123">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="28d9f-123">Property value</span></span>

<span data-ttu-id="28d9f-124">La nueva parte de la contraseña, en formato codificado binario.</span><span class="sxs-lookup"><span data-stu-id="28d9f-124">The new password part, in binary encoded format.</span></span>

## <a name="error-codes"></a><span data-ttu-id="28d9f-125">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="28d9f-125">Error codes</span></span>

<span data-ttu-id="28d9f-126">Devuelve **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="28d9f-126">Returns **E\_NOTIMPL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="28d9f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28d9f-127">Requirements</span></span>



| <span data-ttu-id="28d9f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="28d9f-128">Requirement</span></span> | <span data-ttu-id="28d9f-129">Value</span><span class="sxs-lookup"><span data-stu-id="28d9f-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28d9f-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28d9f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="28d9f-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="28d9f-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="28d9f-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="28d9f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="28d9f-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="28d9f-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="28d9f-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="28d9f-134">End of client support</span></span><br/>    | <span data-ttu-id="28d9f-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="28d9f-135">None supported</span></span><br/>                                                              |
| <span data-ttu-id="28d9f-136">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="28d9f-136">End of server support</span></span><br/>    | <span data-ttu-id="28d9f-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="28d9f-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="28d9f-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="28d9f-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="28d9f-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28d9f-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="28d9f-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="28d9f-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28d9f-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28d9f-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="28d9f-142">IID</span><span class="sxs-lookup"><span data-stu-id="28d9f-142">IID</span></span><br/>                      | <span data-ttu-id="28d9f-143">IID \_ IMsTscNonScriptable se define como c1e6743a-41c1-4a74-832A-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="28d9f-143">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="28d9f-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="28d9f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28d9f-145">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="28d9f-145">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="28d9f-146">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="28d9f-146">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="28d9f-147">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="28d9f-147">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="28d9f-148">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="28d9f-148">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="28d9f-149">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="28d9f-149">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="28d9f-150">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="28d9f-150">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





