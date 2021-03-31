---
title: Propiedad PinConnectionBar de IMsRdpClientAdvancedSettings
description: Especifica el estado de la barra de conexión de la interfaz de usuario.
ms.assetid: b1f9cb02-3ee3-4574-a874-2584b0d5b47e
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad PinConnectionBar
- Propiedad PinConnectionBar Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad PinConnectionBar
- Propiedad PinConnectionBar Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad PinConnectionBar
- Propiedad PinConnectionBar Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad PinConnectionBar
- Propiedad PinConnectionBar Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad PinConnectionBar
- Propiedad PinConnectionBar Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad PinConnectionBar
- Propiedad PinConnectionBar Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad PinConnectionBar
- Propiedad PinConnectionBar Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad PinConnectionBar
- Propiedad PinConnectionBar Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad PinConnectionBar
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.PinConnectionBar
- IMsRdpClientAdvancedSettings.get_PinConnectionBar
- IMsRdpClientAdvancedSettings.put_PinConnectionBar
- IMsRdpClientAdvancedSettings2.PinConnectionBar
- IMsRdpClientAdvancedSettings2.get_PinConnectionBar
- IMsRdpClientAdvancedSettings2.put_PinConnectionBar
- IMsRdpClientAdvancedSettings3.PinConnectionBar
- IMsRdpClientAdvancedSettings3.get_PinConnectionBar
- IMsRdpClientAdvancedSettings3.put_PinConnectionBar
- IMsRdpClientAdvancedSettings4.PinConnectionBar
- IMsRdpClientAdvancedSettings4.get_PinConnectionBar
- IMsRdpClientAdvancedSettings4.put_PinConnectionBar
- IMsRdpClientAdvancedSettings5.PinConnectionBar
- IMsRdpClientAdvancedSettings5.get_PinConnectionBar
- IMsRdpClientAdvancedSettings5.put_PinConnectionBar
- IMsRdpClientAdvancedSettings6.PinConnectionBar
- IMsRdpClientAdvancedSettings6.get_PinConnectionBar
- IMsRdpClientAdvancedSettings6.put_PinConnectionBar
- IMsRdpClientAdvancedSettings7.PinConnectionBar
- IMsRdpClientAdvancedSettings7.get_PinConnectionBar
- IMsRdpClientAdvancedSettings7.put_PinConnectionBar
- IMsRdpClientAdvancedSettings8.PinConnectionBar
- IMsRdpClientAdvancedSettings8.get_PinConnectionBar
- IMsRdpClientAdvancedSettings8.put_PinConnectionBar
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0da294d933026194d7307a7fa0a175575761809e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905014"
---
# <a name="imsrdpclientadvancedsettingspinconnectionbar-property"></a><span data-ttu-id="f48f8-120">IMsRdpClientAdvancedSettings::P propiedad inConnectionBar</span><span class="sxs-lookup"><span data-stu-id="f48f8-120">IMsRdpClientAdvancedSettings::PinConnectionBar property</span></span>

<span data-ttu-id="f48f8-121">Especifica el estado de la barra de conexión de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="f48f8-121">Specifies the state of the UI connection bar.</span></span>

<span data-ttu-id="f48f8-122">Esta propiedad devuelve **E \_ NOTIMPL** si el contenedor llama al método [**IObjectSafety:: SetInterfaceSafetyOptions**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768225(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="f48f8-122">This property returns **E\_NOTIMPL** if the container calls the [**IObjectSafety::SetInterfaceSafetyOptions**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768225(v=vs.85)) method.</span></span>

<span data-ttu-id="f48f8-123">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f48f8-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f48f8-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f48f8-124">Syntax</span></span>


```C++
HRESULT put_PinConnectionBar(
  [in]  VARIANT_BOOL fPinConnectionBar
);

HRESULT get_PinConnectionBar(
  [out] VARIANT_BOOL *pfPinConnectionBar
);
```



## <a name="property-value"></a><span data-ttu-id="f48f8-125">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f48f8-125">Property value</span></span>

<span data-ttu-id="f48f8-126">Al establecer esta propiedad en **Variant \_ true** , el estado se establece en "lowerd", es decir, no es visible para el usuario y no está disponible para la entrada.</span><span class="sxs-lookup"><span data-stu-id="f48f8-126">Setting this property to **VARIANT\_TRUE** sets the state to "lowered", that is, invisible to the user and unavailable for input.</span></span> <span data-ttu-id="f48f8-127">**Variante \_ FALSE** establece el estado en "generated" y disponible para los datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="f48f8-127">**VARIANT\_FALSE** sets the state to "raised" and available for user input.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f48f8-128">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="f48f8-128">Error codes</span></span>

<span data-ttu-id="f48f8-129">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="f48f8-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f48f8-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f48f8-130">Remarks</span></span>

<span data-ttu-id="f48f8-131">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f48f8-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f48f8-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f48f8-132">Requirements</span></span>



| <span data-ttu-id="f48f8-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f48f8-133">Requirement</span></span> | <span data-ttu-id="f48f8-134">Value</span><span class="sxs-lookup"><span data-stu-id="f48f8-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f48f8-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f48f8-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f48f8-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f48f8-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="f48f8-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f48f8-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f48f8-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f48f8-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="f48f8-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f48f8-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="f48f8-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f48f8-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f48f8-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f48f8-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f48f8-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f48f8-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f48f8-143">IID</span><span class="sxs-lookup"><span data-stu-id="f48f8-143">IID</span></span><br/>                      | <span data-ttu-id="f48f8-144">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="f48f8-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f48f8-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="f48f8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f48f8-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="f48f8-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="f48f8-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="f48f8-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="f48f8-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="f48f8-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="f48f8-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="f48f8-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="f48f8-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="f48f8-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="f48f8-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="f48f8-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="f48f8-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="f48f8-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="f48f8-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="f48f8-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

