---
title: Propiedad SmartSizing de IMsRdpClientAdvancedSettings
description: Especifica si la presentación se debe escalar para ajustarse al área cliente del control. Tenga en cuenta que las barras de desplazamiento no aparecen cuando la propiedad SmartSizing está habilitada.
ms.assetid: d0b93129-5f84-49c5-bf8c-048075ac1481
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad SmartSizing
- Propiedad SmartSizing Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad SmartSizing
- Propiedad SmartSizing Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad SmartSizing
- Propiedad SmartSizing Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad SmartSizing
- Propiedad SmartSizing Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad SmartSizing
- Propiedad SmartSizing Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad SmartSizing
- Propiedad SmartSizing Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad SmartSizing
- Propiedad SmartSizing Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad SmartSizing
- Propiedad SmartSizing Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad SmartSizing
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.SmartSizing
- IMsRdpClientAdvancedSettings.get_SmartSizing
- IMsRdpClientAdvancedSettings.put_SmartSizing
- IMsRdpClientAdvancedSettings2.SmartSizing
- IMsRdpClientAdvancedSettings2.get_SmartSizing
- IMsRdpClientAdvancedSettings2.put_SmartSizing
- IMsRdpClientAdvancedSettings3.SmartSizing
- IMsRdpClientAdvancedSettings3.get_SmartSizing
- IMsRdpClientAdvancedSettings3.put_SmartSizing
- IMsRdpClientAdvancedSettings4.SmartSizing
- IMsRdpClientAdvancedSettings4.get_SmartSizing
- IMsRdpClientAdvancedSettings4.put_SmartSizing
- IMsRdpClientAdvancedSettings5.SmartSizing
- IMsRdpClientAdvancedSettings5.get_SmartSizing
- IMsRdpClientAdvancedSettings5.put_SmartSizing
- IMsRdpClientAdvancedSettings6.SmartSizing
- IMsRdpClientAdvancedSettings6.get_SmartSizing
- IMsRdpClientAdvancedSettings6.put_SmartSizing
- IMsRdpClientAdvancedSettings7.SmartSizing
- IMsRdpClientAdvancedSettings7.get_SmartSizing
- IMsRdpClientAdvancedSettings7.put_SmartSizing
- IMsRdpClientAdvancedSettings8.SmartSizing
- IMsRdpClientAdvancedSettings8.get_SmartSizing
- IMsRdpClientAdvancedSettings8.put_SmartSizing
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ec2a825725e01d876b9e8658f215de6595f32f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421929"
---
# <a name="imsrdpclientadvancedsettingssmartsizing-property"></a><span data-ttu-id="f9715-121">IMsRdpClientAdvancedSettings:: SmartSizing (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f9715-121">IMsRdpClientAdvancedSettings::SmartSizing property</span></span>

<span data-ttu-id="f9715-122">Especifica si la presentación se debe escalar para ajustarse al área cliente del control.</span><span class="sxs-lookup"><span data-stu-id="f9715-122">Specifies if the display should be scaled to fit the client area of the control.</span></span> <span data-ttu-id="f9715-123">Tenga en cuenta que las barras de desplazamiento no aparecen cuando la propiedad **SmartSizing** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="f9715-123">Note that scroll bars do not appear when the **SmartSizing** property is enabled.</span></span>

<span data-ttu-id="f9715-124">A diferencia de la mayoría de las demás propiedades, esta propiedad se puede establecer cuando el control está conectado.</span><span class="sxs-lookup"><span data-stu-id="f9715-124">Unlike most other properties, this property can be set when the control is connected.</span></span>

<span data-ttu-id="f9715-125">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f9715-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9715-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9715-126">Syntax</span></span>


```C++
HRESULT put_SmartSizing(
  [in]  VARIANT_BOOL fSmartSizing
);

HRESULT get_SmartSizing(
  [out] VARIANT_BOOL *pfSmartSizing
);
```



## <a name="property-value"></a><span data-ttu-id="f9715-127">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f9715-127">Property value</span></span>

<span data-ttu-id="f9715-128">Establezca este parámetro en **Variant \_ false** para deshabilitar la característica o la **variante \_ true** para habilitar la característica.</span><span class="sxs-lookup"><span data-stu-id="f9715-128">Set this parameter to **VARIANT\_FALSE** to disable the feature or **VARIANT\_TRUE** to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f9715-129">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="f9715-129">Error codes</span></span>

<span data-ttu-id="f9715-130">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="f9715-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9715-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9715-131">Remarks</span></span>

<span data-ttu-id="f9715-132">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f9715-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9715-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9715-133">Requirements</span></span>



| <span data-ttu-id="f9715-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9715-134">Requirement</span></span> | <span data-ttu-id="f9715-135">Value</span><span class="sxs-lookup"><span data-stu-id="f9715-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9715-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9715-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f9715-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9715-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="f9715-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f9715-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f9715-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9715-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="f9715-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f9715-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="f9715-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9715-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f9715-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f9715-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9715-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9715-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f9715-144">IID</span><span class="sxs-lookup"><span data-stu-id="f9715-144">IID</span></span><br/>                      | <span data-ttu-id="f9715-145">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="f9715-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9715-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9715-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9715-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="f9715-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="f9715-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="f9715-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="f9715-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="f9715-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="f9715-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="f9715-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="f9715-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="f9715-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="f9715-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="f9715-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="f9715-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="f9715-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="f9715-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="f9715-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





