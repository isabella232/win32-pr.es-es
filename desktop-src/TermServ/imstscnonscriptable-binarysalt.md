---
title: Propiedad BinarySalt de IMsTscNonScriptable
description: Esta propiedad ya no está disponible para su uso. | Propiedad BinarySalt de IMsTscNonScriptable
ms.assetid: 7af2e5be-9ddb-46ab-947c-f79ab890d7bc
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad BinarySalt
- Propiedad BinarySalt Servicios de Escritorio remoto, interfaz IMsTscNonScriptable
- Servicios de Escritorio remoto de la interfaz IMsTscNonScriptable, propiedad BinarySalt
- Servicios de Escritorio remoto de la propiedad BinarySalt, objeto MsTscAx
- Servicios de Escritorio remoto de objeto MsTscAx, propiedad BinarySalt
- Propiedad BinarySalt Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable, propiedad BinarySalt
- Propiedad BinarySalt Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable2, propiedad BinarySalt
- Propiedad BinarySalt Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad BinarySalt
- Propiedad BinarySalt Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad BinarySalt
- Propiedad BinarySalt Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad BinarySalt
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.BinarySalt
- IMsTscNonScriptable.get_BinarySalt
- IMsTscNonScriptable.put_BinarySalt
- MsTscAx.BinarySalt
- IMsRdpClientNonScriptable.BinarySalt
- IMsRdpClientNonScriptable.get_BinarySalt
- IMsRdpClientNonScriptable.put_BinarySalt
- IMsRdpClientNonScriptable2.BinarySalt
- IMsRdpClientNonScriptable2.get_BinarySalt
- IMsRdpClientNonScriptable2.put_BinarySalt
- IMsRdpClientNonScriptable3.BinarySalt
- IMsRdpClientNonScriptable3.get_BinarySalt
- IMsRdpClientNonScriptable3.put_BinarySalt
- IMsRdpClientNonScriptable4.BinarySalt
- IMsRdpClientNonScriptable4.get_BinarySalt
- IMsRdpClientNonScriptable4.put_BinarySalt
- IMsRdpClientNonScriptable5.BinarySalt
- IMsRdpClientNonScriptable5.get_BinarySalt
- IMsRdpClientNonScriptable5.put_BinarySalt
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eb13ccb79a9cf2c309a32772a73b393756c7bdd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678691"
---
# <a name="imstscnonscriptablebinarysalt-property"></a><span data-ttu-id="b2299-119">IMsTscNonScriptable:: BinarySalt (propiedad)</span><span class="sxs-lookup"><span data-stu-id="b2299-119">IMsTscNonScriptable::BinarySalt property</span></span>

<span data-ttu-id="b2299-120">Esta propiedad ya no está disponible para su uso.</span><span class="sxs-lookup"><span data-stu-id="b2299-120">This property is no longer available for use.</span></span>

<span data-ttu-id="b2299-121">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b2299-121">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2299-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2299-122">Syntax</span></span>


```C++
HRESULT put_BinarySalt(
  [in]  BSTR newSalt
);

HRESULT get_BinarySalt(
  [out] BSTR *pSalt
);
```



## <a name="property-value"></a><span data-ttu-id="b2299-123">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b2299-123">Property value</span></span>

<span data-ttu-id="b2299-124">La nueva parte de sal binaria para una contraseña codificada binaria.</span><span class="sxs-lookup"><span data-stu-id="b2299-124">The new binary salt part for a binary encoded password.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b2299-125">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="b2299-125">Error codes</span></span>

<span data-ttu-id="b2299-126">Devuelve **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="b2299-126">Returns **E\_NOTIMPL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2299-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2299-127">Requirements</span></span>



| <span data-ttu-id="b2299-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2299-128">Requirement</span></span> | <span data-ttu-id="b2299-129">Value</span><span class="sxs-lookup"><span data-stu-id="b2299-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b2299-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2299-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b2299-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b2299-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b2299-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2299-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b2299-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b2299-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b2299-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b2299-134">End of client support</span></span><br/>    | <span data-ttu-id="b2299-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b2299-135">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b2299-136">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="b2299-136">End of server support</span></span><br/>    | <span data-ttu-id="b2299-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b2299-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="b2299-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b2299-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="b2299-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2299-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b2299-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b2299-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2299-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2299-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b2299-142">IID</span><span class="sxs-lookup"><span data-stu-id="b2299-142">IID</span></span><br/>                      | <span data-ttu-id="b2299-143">IID \_ IMsTscNonScriptable se define como c1e6743a-41c1-4a74-832A-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="b2299-143">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b2299-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2299-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2299-145">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="b2299-145">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="b2299-146">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="b2299-146">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="b2299-147">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="b2299-147">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="b2299-148">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="b2299-148">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="b2299-149">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="b2299-149">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="b2299-150">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="b2299-150">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





