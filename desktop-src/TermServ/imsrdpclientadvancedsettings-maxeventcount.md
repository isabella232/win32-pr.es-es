---
title: Propiedad maxEventCount de IMsRdpClientAdvancedSettings
description: Esta propiedad no es compatible. | Propiedad maxEventCount de IMsRdpClientAdvancedSettings
ms.assetid: d7b5951d-8cc3-48b4-af1b-1f547afbc6ae
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad maxEventCount
- propiedad maxEventCount Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad maxEventCount
- propiedad maxEventCount Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad maxEventCount
- propiedad maxEventCount Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad maxEventCount
- propiedad maxEventCount Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad maxEventCount
- propiedad maxEventCount Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad maxEventCount
- propiedad maxEventCount Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad maxEventCount
- propiedad maxEventCount Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad maxEventCount
- propiedad maxEventCount Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad maxEventCount
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.maxEventCount
- IMsRdpClientAdvancedSettings.get_maxEventCount
- IMsRdpClientAdvancedSettings.put_maxEventCount
- IMsRdpClientAdvancedSettings2.maxEventCount
- IMsRdpClientAdvancedSettings2.get_maxEventCount
- IMsRdpClientAdvancedSettings2.put_maxEventCount
- IMsRdpClientAdvancedSettings3.maxEventCount
- IMsRdpClientAdvancedSettings3.get_maxEventCount
- IMsRdpClientAdvancedSettings3.put_maxEventCount
- IMsRdpClientAdvancedSettings4.maxEventCount
- IMsRdpClientAdvancedSettings4.get_maxEventCount
- IMsRdpClientAdvancedSettings4.put_maxEventCount
- IMsRdpClientAdvancedSettings5.maxEventCount
- IMsRdpClientAdvancedSettings5.get_maxEventCount
- IMsRdpClientAdvancedSettings5.put_maxEventCount
- IMsRdpClientAdvancedSettings6.maxEventCount
- IMsRdpClientAdvancedSettings6.get_maxEventCount
- IMsRdpClientAdvancedSettings6.put_maxEventCount
- IMsRdpClientAdvancedSettings7.maxEventCount
- IMsRdpClientAdvancedSettings7.get_maxEventCount
- IMsRdpClientAdvancedSettings7.put_maxEventCount
- IMsRdpClientAdvancedSettings8.maxEventCount
- IMsRdpClientAdvancedSettings8.get_maxEventCount
- IMsRdpClientAdvancedSettings8.put_maxEventCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb305d4a81b3c4dd9eb53dceab5a4e685c57c060
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914394"
---
# <a name="imsrdpclientadvancedsettingsmaxeventcount-property"></a><span data-ttu-id="380cc-121">IMsRdpClientAdvancedSettings:: maxEventCount (propiedad)</span><span class="sxs-lookup"><span data-stu-id="380cc-121">IMsRdpClientAdvancedSettings::maxEventCount property</span></span>

<span data-ttu-id="380cc-122">Esta propiedad no es compatible.</span><span class="sxs-lookup"><span data-stu-id="380cc-122">This property is not supported.</span></span>

<span data-ttu-id="380cc-123">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="380cc-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="380cc-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="380cc-124">Syntax</span></span>


```C++
HRESULT put_maxEventCount(
  [in]  LONG maxEventCount
);

HRESULT get_maxEventCount(
  [out] LONG pmaxEventCount
);
```



## <a name="property-value"></a><span data-ttu-id="380cc-125">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="380cc-125">Property value</span></span>

<span data-ttu-id="380cc-126">Nuevo recuento de eventos.</span><span class="sxs-lookup"><span data-stu-id="380cc-126">The new event count.</span></span> <span data-ttu-id="380cc-127">El valor predeterminado es 100.</span><span class="sxs-lookup"><span data-stu-id="380cc-127">The default is 100.</span></span>

## <a name="error-codes"></a><span data-ttu-id="380cc-128">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="380cc-128">Error codes</span></span>

<span data-ttu-id="380cc-129">Devuelve **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="380cc-129">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="380cc-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="380cc-130">Remarks</span></span>

<span data-ttu-id="380cc-131">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="380cc-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="380cc-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="380cc-132">Requirements</span></span>



| <span data-ttu-id="380cc-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="380cc-133">Requirement</span></span> | <span data-ttu-id="380cc-134">Value</span><span class="sxs-lookup"><span data-stu-id="380cc-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="380cc-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="380cc-135">Minimum supported client</span></span><br/> | <span data-ttu-id="380cc-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="380cc-136">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="380cc-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="380cc-137">Minimum supported server</span></span><br/> | <span data-ttu-id="380cc-138">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="380cc-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="380cc-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="380cc-139">End of client support</span></span><br/>    | <span data-ttu-id="380cc-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="380cc-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="380cc-141">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="380cc-141">End of server support</span></span><br/>    | <span data-ttu-id="380cc-142">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="380cc-142">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="380cc-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="380cc-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="380cc-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="380cc-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="380cc-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="380cc-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="380cc-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="380cc-146"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="380cc-147">IID</span><span class="sxs-lookup"><span data-stu-id="380cc-147">IID</span></span><br/>                      | <span data-ttu-id="380cc-148">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="380cc-148">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="380cc-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="380cc-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="380cc-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="380cc-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="380cc-151">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="380cc-151">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="380cc-152">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="380cc-152">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="380cc-153">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="380cc-153">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="380cc-154">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="380cc-154">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="380cc-155">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="380cc-155">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="380cc-156">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="380cc-156">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="380cc-157">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="380cc-157">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





