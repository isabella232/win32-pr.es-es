---
title: Propiedad PortableSalt de IMsTscNonScriptable
description: Este propiedad ya no se admite.
ms.assetid: 1f123ec8-27b6-4637-9c57-fe32a224be8a
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad PortableSalt
- Propiedad PortableSalt Servicios de Escritorio remoto, interfaz IMsTscNonScriptable
- Servicios de Escritorio remoto de la interfaz IMsTscNonScriptable, propiedad PortableSalt
- Servicios de Escritorio remoto de la propiedad PortableSalt, objeto MsTscAx
- Servicios de Escritorio remoto de objeto MsTscAx, propiedad PortableSalt
- Propiedad PortableSalt Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable, propiedad PortableSalt
- Propiedad PortableSalt Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable2, propiedad PortableSalt
- Propiedad PortableSalt Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad PortableSalt
- Propiedad PortableSalt Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad PortableSalt
- Propiedad PortableSalt Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad PortableSalt
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.PortableSalt
- IMsTscNonScriptable.get_PortableSalt
- IMsTscNonScriptable.put_PortableSalt
- MsTscAx.PortableSalt
- IMsRdpClientNonScriptable.PortableSalt
- IMsRdpClientNonScriptable.get_PortableSalt
- IMsRdpClientNonScriptable.put_PortableSalt
- IMsRdpClientNonScriptable2.PortableSalt
- IMsRdpClientNonScriptable2.get_PortableSalt
- IMsRdpClientNonScriptable2.put_PortableSalt
- IMsRdpClientNonScriptable3.PortableSalt
- IMsRdpClientNonScriptable3.get_PortableSalt
- IMsRdpClientNonScriptable3.put_PortableSalt
- IMsRdpClientNonScriptable4.PortableSalt
- IMsRdpClientNonScriptable4.get_PortableSalt
- IMsRdpClientNonScriptable4.put_PortableSalt
- IMsRdpClientNonScriptable5.PortableSalt
- IMsRdpClientNonScriptable5.get_PortableSalt
- IMsRdpClientNonScriptable5.put_PortableSalt
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0162073b8361cc89f7ab2e33f60406c0db935bdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802941"
---
# <a name="imstscnonscriptableportablesalt-property"></a><span data-ttu-id="88094-118">IMsTscNonScriptable::P propiedad ortableSalt</span><span class="sxs-lookup"><span data-stu-id="88094-118">IMsTscNonScriptable::PortableSalt property</span></span>

<span data-ttu-id="88094-119">Este propiedad ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="88094-119">This property is no longer supported.</span></span>

<span data-ttu-id="88094-120">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="88094-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="88094-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88094-121">Syntax</span></span>


```C++
HRESULT put_PortableSalt(
  [in]  BSTR newPortableSalt
);

HRESULT get_PortableSalt(
  [out] BSTR *pPortableSalt
);
```



## <a name="property-value"></a><span data-ttu-id="88094-122">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="88094-122">Property value</span></span>

<span data-ttu-id="88094-123">La nueva parte de sal portátil para una contraseña codificada portátil.</span><span class="sxs-lookup"><span data-stu-id="88094-123">The new portable salt part for a portable encoded password.</span></span>

## <a name="error-codes"></a><span data-ttu-id="88094-124">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="88094-124">Error codes</span></span>

<span data-ttu-id="88094-125">Devuelve **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="88094-125">Returns **E\_NOTIMPL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="88094-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88094-126">Requirements</span></span>



| <span data-ttu-id="88094-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="88094-127">Requirement</span></span> | <span data-ttu-id="88094-128">Value</span><span class="sxs-lookup"><span data-stu-id="88094-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="88094-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88094-129">Minimum supported client</span></span><br/> | <span data-ttu-id="88094-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="88094-130">None supported</span></span><br/>                                                              |
| <span data-ttu-id="88094-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88094-131">Minimum supported server</span></span><br/> | <span data-ttu-id="88094-132">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="88094-132">None supported</span></span><br/>                                                              |
| <span data-ttu-id="88094-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="88094-133">End of client support</span></span><br/>    | <span data-ttu-id="88094-134">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="88094-134">None supported</span></span><br/>                                                              |
| <span data-ttu-id="88094-135">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="88094-135">End of server support</span></span><br/>    | <span data-ttu-id="88094-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="88094-136">None supported</span></span><br/>                                                              |
| <span data-ttu-id="88094-137">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="88094-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="88094-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88094-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="88094-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="88094-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88094-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88094-140"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="88094-141">IID</span><span class="sxs-lookup"><span data-stu-id="88094-141">IID</span></span><br/>                      | <span data-ttu-id="88094-142">IID \_ IMsTscNonScriptable se define como c1e6743a-41c1-4a74-832A-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="88094-142">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="88094-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="88094-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88094-144">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="88094-144">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="88094-145">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="88094-145">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="88094-146">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="88094-146">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="88094-147">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="88094-147">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="88094-148">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="88094-148">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="88094-149">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="88094-149">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="88094-150">**PortablePassword**</span><span class="sxs-lookup"><span data-stu-id="88094-150">**PortablePassword**</span></span>](imstscnonscriptable-portablepassword.md)
</dt> </dl>

 

 





