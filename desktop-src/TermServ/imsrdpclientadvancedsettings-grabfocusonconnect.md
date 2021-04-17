---
title: Propiedad GrabFocusOnConnect de IMsRdpClientAdvancedSettings
description: Especifica si el control de cliente debe tener el foco mientras se conecta.
ms.assetid: c67fc284-6e07-4749-84bf-70c0ae4d1b2b
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad GrabFocusOnConnect
- Propiedad GrabFocusOnConnect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad GrabFocusOnConnect
- Propiedad GrabFocusOnConnect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad GrabFocusOnConnect
- Propiedad GrabFocusOnConnect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad GrabFocusOnConnect
- Propiedad GrabFocusOnConnect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad GrabFocusOnConnect
- Propiedad GrabFocusOnConnect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad GrabFocusOnConnect
- Propiedad GrabFocusOnConnect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad GrabFocusOnConnect
- Propiedad GrabFocusOnConnect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad GrabFocusOnConnect
- Propiedad GrabFocusOnConnect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad GrabFocusOnConnect
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings2.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings3.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings4.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings5.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings6.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings7.put_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.get_GrabFocusOnConnect
- IMsRdpClientAdvancedSettings8.put_GrabFocusOnConnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e7fb04c00bd7aaaf4de1252d961206ffee0e6b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676931"
---
# <a name="imsrdpclientadvancedsettingsgrabfocusonconnect-property"></a><span data-ttu-id="ba8d4-120">IMsRdpClientAdvancedSettings:: GrabFocusOnConnect (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ba8d4-120">IMsRdpClientAdvancedSettings::GrabFocusOnConnect property</span></span>

<span data-ttu-id="ba8d4-121">Especifica si el control de cliente debe tener el foco mientras se conecta.</span><span class="sxs-lookup"><span data-stu-id="ba8d4-121">Specifies if the client control should have the focus while connecting.</span></span> <span data-ttu-id="ba8d4-122">El control no intentará captar el foco de una ventana que se ejecuta en un proceso diferente.</span><span class="sxs-lookup"><span data-stu-id="ba8d4-122">The control will not attempt to grab focus from a window running in a different process.</span></span>

<span data-ttu-id="ba8d4-123">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ba8d4-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba8d4-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba8d4-124">Syntax</span></span>


```C++
HRESULT put_GrabFocusOnConnect(
  [in]  VARIANT_BOOL fGrabFocusOnConnect
);

HRESULT get_GrabFocusOnConnect(
  [out] VARIANT_BOOL pfGrabFocusOnConnect
);
```



## <a name="property-value"></a><span data-ttu-id="ba8d4-125">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ba8d4-125">Property value</span></span>

<span data-ttu-id="ba8d4-126">Establezca este parámetro en **Variant \_ false** para deshabilitar la característica o la **variante \_ true** para habilitar la característica.</span><span class="sxs-lookup"><span data-stu-id="ba8d4-126">Set this parameter to **VARIANT\_FALSE** to disable the feature or **VARIANT\_TRUE** to enable the feature.</span></span> <span data-ttu-id="ba8d4-127">Al establecer esta propiedad en **Variant \_ false** , se impide que el control capte el foco al conectarse.</span><span class="sxs-lookup"><span data-stu-id="ba8d4-127">Setting this property to **VARIANT\_FALSE** prevents the control from grabbing focus when connecting.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ba8d4-128">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="ba8d4-128">Error codes</span></span>

<span data-ttu-id="ba8d4-129">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="ba8d4-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba8d4-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ba8d4-130">Remarks</span></span>

<span data-ttu-id="ba8d4-131">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ba8d4-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ba8d4-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba8d4-132">Requirements</span></span>



| <span data-ttu-id="ba8d4-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba8d4-133">Requirement</span></span> | <span data-ttu-id="ba8d4-134">Value</span><span class="sxs-lookup"><span data-stu-id="ba8d4-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba8d4-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba8d4-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ba8d4-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba8d4-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="ba8d4-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba8d4-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ba8d4-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba8d4-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="ba8d4-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ba8d4-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="ba8d4-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba8d4-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ba8d4-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ba8d4-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba8d4-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba8d4-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ba8d4-143">IID</span><span class="sxs-lookup"><span data-stu-id="ba8d4-143">IID</span></span><br/>                      | <span data-ttu-id="ba8d4-144">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="ba8d4-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ba8d4-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba8d4-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba8d4-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="ba8d4-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="ba8d4-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="ba8d4-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="ba8d4-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="ba8d4-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="ba8d4-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="ba8d4-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="ba8d4-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ba8d4-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="ba8d4-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ba8d4-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ba8d4-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ba8d4-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ba8d4-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="ba8d4-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





