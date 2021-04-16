---
title: Propiedad PortablePassword de IMsTscNonScriptable
description: Esta propiedad ya no está disponible para su uso. | Propiedad PortablePassword de IMsTscNonScriptable
ms.assetid: 8d831ed3-1f4a-41a9-b283-507c5d9eea22
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad PortablePassword
- Propiedad PortablePassword Servicios de Escritorio remoto, interfaz IMsTscNonScriptable
- Servicios de Escritorio remoto de la interfaz IMsTscNonScriptable, propiedad PortablePassword
- Servicios de Escritorio remoto de la propiedad PortablePassword, objeto MsTscAx
- Servicios de Escritorio remoto de objeto MsTscAx, propiedad PortablePassword
- Propiedad PortablePassword Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable, propiedad PortablePassword
- Propiedad PortablePassword Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable2, propiedad PortablePassword
- Propiedad PortablePassword Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad PortablePassword
- Propiedad PortablePassword Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad PortablePassword
- Propiedad PortablePassword Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad PortablePassword
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.PortablePassword
- IMsTscNonScriptable.get_PortablePassword
- IMsTscNonScriptable.put_PortablePassword
- MsTscAx.PortablePassword
- IMsRdpClientNonScriptable.PortablePassword
- IMsRdpClientNonScriptable.get_PortablePassword
- IMsRdpClientNonScriptable.put_PortablePassword
- IMsRdpClientNonScriptable2.PortablePassword
- IMsRdpClientNonScriptable2.get_PortablePassword
- IMsRdpClientNonScriptable2.put_PortablePassword
- IMsRdpClientNonScriptable3.PortablePassword
- IMsRdpClientNonScriptable3.get_PortablePassword
- IMsRdpClientNonScriptable3.put_PortablePassword
- IMsRdpClientNonScriptable4.PortablePassword
- IMsRdpClientNonScriptable4.get_PortablePassword
- IMsRdpClientNonScriptable4.put_PortablePassword
- IMsRdpClientNonScriptable5.PortablePassword
- IMsRdpClientNonScriptable5.get_PortablePassword
- IMsRdpClientNonScriptable5.put_PortablePassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5259e83087287395e6114bb8ffe3eb7e859ab52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678699"
---
# <a name="imstscnonscriptableportablepassword-property"></a><span data-ttu-id="51fd0-119">IMsTscNonScriptable::P propiedad ortablePassword</span><span class="sxs-lookup"><span data-stu-id="51fd0-119">IMsTscNonScriptable::PortablePassword property</span></span>

<span data-ttu-id="51fd0-120">Esta propiedad ya no está disponible para su uso.</span><span class="sxs-lookup"><span data-stu-id="51fd0-120">This property is no longer available for use.</span></span>

<span data-ttu-id="51fd0-121">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="51fd0-121">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="51fd0-122">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51fd0-122">Syntax</span></span>


```C++
HRESULT put_PortablePassword(
  [in]  BSTR newPortablePassVal
);

HRESULT get_PortablePassword(
  [out] BSTR *pPortablePass
);
```



## <a name="property-value"></a><span data-ttu-id="51fd0-123">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="51fd0-123">Property value</span></span>

<span data-ttu-id="51fd0-124">La nueva parte de la contraseña, en formato codificado portable.</span><span class="sxs-lookup"><span data-stu-id="51fd0-124">The new password part, in portable encoded format.</span></span>

## <a name="error-codes"></a><span data-ttu-id="51fd0-125">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="51fd0-125">Error codes</span></span>

<span data-ttu-id="51fd0-126">Devuelve **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="51fd0-126">Returns **E\_NOTIMPL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="51fd0-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51fd0-127">Requirements</span></span>



| <span data-ttu-id="51fd0-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="51fd0-128">Requirement</span></span> | <span data-ttu-id="51fd0-129">Value</span><span class="sxs-lookup"><span data-stu-id="51fd0-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="51fd0-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51fd0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="51fd0-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="51fd0-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="51fd0-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51fd0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="51fd0-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="51fd0-133">None supported</span></span><br/>                                                              |
| <span data-ttu-id="51fd0-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="51fd0-134">End of client support</span></span><br/>    | <span data-ttu-id="51fd0-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="51fd0-135">None supported</span></span><br/>                                                              |
| <span data-ttu-id="51fd0-136">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="51fd0-136">End of server support</span></span><br/>    | <span data-ttu-id="51fd0-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="51fd0-137">None supported</span></span><br/>                                                              |
| <span data-ttu-id="51fd0-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="51fd0-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="51fd0-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51fd0-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="51fd0-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="51fd0-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51fd0-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51fd0-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="51fd0-142">IID</span><span class="sxs-lookup"><span data-stu-id="51fd0-142">IID</span></span><br/>                      | <span data-ttu-id="51fd0-143">IID \_ IMsTscNonScriptable se define como c1e6743a-41c1-4a74-832A-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="51fd0-143">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="51fd0-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="51fd0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51fd0-145">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="51fd0-145">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="51fd0-146">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="51fd0-146">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="51fd0-147">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="51fd0-147">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="51fd0-148">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="51fd0-148">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="51fd0-149">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="51fd0-149">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="51fd0-150">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="51fd0-150">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





