---
title: Propiedad DisplayConnectionBar de IMsRdpClientAdvancedSettings
description: Especifica si se va a utilizar la barra de conexión. El valor predeterminado es VARIANT \_ true, que habilita la propiedad.
ms.assetid: 251c0322-5589-423d-9694-004f847c173b
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DisplayConnectionBar
- Propiedad DisplayConnectionBar Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad DisplayConnectionBar
- Propiedad DisplayConnectionBar Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad DisplayConnectionBar
- Propiedad DisplayConnectionBar Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad DisplayConnectionBar
- Propiedad DisplayConnectionBar Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad DisplayConnectionBar
- Propiedad DisplayConnectionBar Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad DisplayConnectionBar
- Propiedad DisplayConnectionBar Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad DisplayConnectionBar
- Propiedad DisplayConnectionBar Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad DisplayConnectionBar
- Propiedad DisplayConnectionBar Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad DisplayConnectionBar
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DisplayConnectionBar
- IMsRdpClientAdvancedSettings.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings2.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings3.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings4.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings5.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings6.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings7.put_DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.get_DisplayConnectionBar
- IMsRdpClientAdvancedSettings8.put_DisplayConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39dd85d0c8fd578931ed9ca8b85ac7a5ca01981e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685932"
---
# <a name="imsrdpclientadvancedsettingsdisplayconnectionbar-property"></a><span data-ttu-id="786cb-121">IMsRdpClientAdvancedSettings::D propiedad isplayConnectionBar</span><span class="sxs-lookup"><span data-stu-id="786cb-121">IMsRdpClientAdvancedSettings::DisplayConnectionBar property</span></span>

<span data-ttu-id="786cb-122">Especifica si se va a utilizar la barra de conexión.</span><span class="sxs-lookup"><span data-stu-id="786cb-122">Specifies whether to use the connection bar.</span></span> <span data-ttu-id="786cb-123">El valor predeterminado es **Variant \_ true**, que habilita la propiedad.</span><span class="sxs-lookup"><span data-stu-id="786cb-123">The default value is **VARIANT\_TRUE**, which enables the property.</span></span> <span data-ttu-id="786cb-124">Al establecer esta propiedad en **Variant \_ false** en un entorno de scripting seguro se devuelve **E \_ FAIL**.</span><span class="sxs-lookup"><span data-stu-id="786cb-124">Setting this property to **VARIANT\_FALSE** in a safe scripting environment returns **E\_FAIL**.</span></span>

<span data-ttu-id="786cb-125">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="786cb-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="786cb-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="786cb-126">Syntax</span></span>


```C++
HRESULT put_DisplayConnectionBar(
  [in]  VARIANT_BOOL fDisplayConnectionBar
);

HRESULT get_DisplayConnectionBar(
  [out] VARIANT_BOOL *pfDisplayConnectionBar
);
```



## <a name="property-value"></a><span data-ttu-id="786cb-127">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="786cb-127">Property value</span></span>

<span data-ttu-id="786cb-128">Establezca este parámetro en **Variant \_ false** para deshabilitar la característica o la **variante \_ true** para habilitar la característica.</span><span class="sxs-lookup"><span data-stu-id="786cb-128">Set this parameter to **VARIANT\_FALSE** to disable the feature or **VARIANT\_TRUE** to enable the feature.</span></span> <span data-ttu-id="786cb-129">El valor predeterminado es **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="786cb-129">The default value is **VARIANT\_TRUE**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="786cb-130">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="786cb-130">Error codes</span></span>

<span data-ttu-id="786cb-131">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="786cb-131">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="786cb-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="786cb-132">Remarks</span></span>

<span data-ttu-id="786cb-133">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="786cb-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="786cb-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="786cb-134">Requirements</span></span>



| <span data-ttu-id="786cb-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="786cb-135">Requirement</span></span> | <span data-ttu-id="786cb-136">Value</span><span class="sxs-lookup"><span data-stu-id="786cb-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="786cb-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="786cb-137">Minimum supported client</span></span><br/> | <span data-ttu-id="786cb-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="786cb-138">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="786cb-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="786cb-139">Minimum supported server</span></span><br/> | <span data-ttu-id="786cb-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="786cb-140">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="786cb-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="786cb-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="786cb-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="786cb-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="786cb-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="786cb-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="786cb-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="786cb-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="786cb-145">IID</span><span class="sxs-lookup"><span data-stu-id="786cb-145">IID</span></span><br/>                      | <span data-ttu-id="786cb-146">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="786cb-146">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="786cb-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="786cb-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="786cb-148">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="786cb-148">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="786cb-149">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="786cb-149">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="786cb-150">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="786cb-150">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="786cb-151">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="786cb-151">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="786cb-152">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="786cb-152">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="786cb-153">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="786cb-153">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="786cb-154">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="786cb-154">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="786cb-155">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="786cb-155">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





