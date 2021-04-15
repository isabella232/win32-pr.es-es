---
title: Propiedad ShadowBitmap de IMsRdpClientAdvancedSettings
description: Especifica si se deben usar los mapas de bits de sombra.
ms.assetid: b329e367-7579-466d-877a-16253f85e5a2
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad ShadowBitmap
- Propiedad ShadowBitmap Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad ShadowBitmap
- Propiedad ShadowBitmap Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad ShadowBitmap
- Propiedad ShadowBitmap Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad ShadowBitmap
- Propiedad ShadowBitmap Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad ShadowBitmap
- Propiedad ShadowBitmap Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad ShadowBitmap
- Propiedad ShadowBitmap Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad ShadowBitmap
- Propiedad ShadowBitmap Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad ShadowBitmap
- Propiedad ShadowBitmap Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad ShadowBitmap
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.ShadowBitmap
- IMsRdpClientAdvancedSettings.get_ShadowBitmap
- IMsRdpClientAdvancedSettings.put_ShadowBitmap
- IMsRdpClientAdvancedSettings2.ShadowBitmap
- IMsRdpClientAdvancedSettings2.get_ShadowBitmap
- IMsRdpClientAdvancedSettings2.put_ShadowBitmap
- IMsRdpClientAdvancedSettings3.ShadowBitmap
- IMsRdpClientAdvancedSettings3.get_ShadowBitmap
- IMsRdpClientAdvancedSettings3.put_ShadowBitmap
- IMsRdpClientAdvancedSettings4.ShadowBitmap
- IMsRdpClientAdvancedSettings4.get_ShadowBitmap
- IMsRdpClientAdvancedSettings4.put_ShadowBitmap
- IMsRdpClientAdvancedSettings5.ShadowBitmap
- IMsRdpClientAdvancedSettings5.get_ShadowBitmap
- IMsRdpClientAdvancedSettings5.put_ShadowBitmap
- IMsRdpClientAdvancedSettings6.ShadowBitmap
- IMsRdpClientAdvancedSettings6.get_ShadowBitmap
- IMsRdpClientAdvancedSettings6.put_ShadowBitmap
- IMsRdpClientAdvancedSettings7.ShadowBitmap
- IMsRdpClientAdvancedSettings7.get_ShadowBitmap
- IMsRdpClientAdvancedSettings7.put_ShadowBitmap
- IMsRdpClientAdvancedSettings8.ShadowBitmap
- IMsRdpClientAdvancedSettings8.get_ShadowBitmap
- IMsRdpClientAdvancedSettings8.put_ShadowBitmap
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc6c43862b498fe5828d2746666c5e414de4c71e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489124"
---
# <a name="imsrdpclientadvancedsettingsshadowbitmap-property"></a><span data-ttu-id="8ba83-120">IMsRdpClientAdvancedSettings:: ShadowBitmap (propiedad)</span><span class="sxs-lookup"><span data-stu-id="8ba83-120">IMsRdpClientAdvancedSettings::ShadowBitmap property</span></span>

<span data-ttu-id="8ba83-121">\[Esta propiedad no es compatible.</span><span class="sxs-lookup"><span data-stu-id="8ba83-121">\[This property is not supported.</span></span> <span data-ttu-id="8ba83-122">A partir de Windows Server 2008 y Windows 7, las llamadas a **ShadowBitmap** siempre devuelven **S \_ false**.\]</span><span class="sxs-lookup"><span data-stu-id="8ba83-122">Starting with Windows Server 2008 and Windows 7, calls to **ShadowBitmap** always return **S\_FALSE**.\]</span></span>

<span data-ttu-id="8ba83-123">Especifica si se deben usar los mapas de bits de sombra.</span><span class="sxs-lookup"><span data-stu-id="8ba83-123">Specifies if shadow bitmaps should be used.</span></span>

<span data-ttu-id="8ba83-124">Los mapas de bits de sombra siempre están deshabilitados en el modo de pantalla completa, por lo que esta propiedad no tiene ningún efecto en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="8ba83-124">Shadow bitmaps are always disabled in full-screen mode, therefore this property has no effect when in full-screen mode.</span></span>

<span data-ttu-id="8ba83-125">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="8ba83-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ba83-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ba83-126">Syntax</span></span>


```C++
HRESULT put_ShadowBitmap(
  [in]  LONG shadowBitmap
);

HRESULT get_ShadowBitmap(
  [out] LONG *pshadowBitmap
);
```



## <a name="property-value"></a><span data-ttu-id="8ba83-127">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8ba83-127">Property value</span></span>

<span data-ttu-id="8ba83-128">Establezca este parámetro en 0 para deshabilitar la característica o un valor distinto de cero para habilitar la característica.</span><span class="sxs-lookup"><span data-stu-id="8ba83-128">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span> <span data-ttu-id="8ba83-129">La deshabilitación de esta característica normalmente mejora el rendimiento, pero puede producir artefactos al pintar pantallas.</span><span class="sxs-lookup"><span data-stu-id="8ba83-129">Disabling this feature typically improves performance but can result in artifacts when painting screens.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ba83-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ba83-130">Remarks</span></span>

<span data-ttu-id="8ba83-131">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="8ba83-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ba83-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ba83-132">Requirements</span></span>



| <span data-ttu-id="8ba83-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ba83-133">Requirement</span></span> | <span data-ttu-id="8ba83-134">Value</span><span class="sxs-lookup"><span data-stu-id="8ba83-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ba83-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ba83-135">Minimum supported client</span></span><br/> | <span data-ttu-id="8ba83-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8ba83-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="8ba83-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ba83-137">Minimum supported server</span></span><br/> | <span data-ttu-id="8ba83-138">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8ba83-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="8ba83-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="8ba83-139">End of client support</span></span><br/>    | <span data-ttu-id="8ba83-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8ba83-140">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="8ba83-141">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="8ba83-141">End of server support</span></span><br/>    | <span data-ttu-id="8ba83-142">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="8ba83-142">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="8ba83-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8ba83-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="8ba83-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ba83-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="8ba83-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8ba83-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ba83-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ba83-146"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="8ba83-147">IID</span><span class="sxs-lookup"><span data-stu-id="8ba83-147">IID</span></span><br/>                      | <span data-ttu-id="8ba83-148">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="8ba83-148">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8ba83-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ba83-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ba83-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="8ba83-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="8ba83-151">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="8ba83-151">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="8ba83-152">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="8ba83-152">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="8ba83-153">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="8ba83-153">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="8ba83-154">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="8ba83-154">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="8ba83-155">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="8ba83-155">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="8ba83-156">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="8ba83-156">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="8ba83-157">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="8ba83-157">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





