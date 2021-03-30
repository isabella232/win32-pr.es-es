---
title: Propiedad allowBackgroundInput de IMsTscAdvancedSettings
description: Especifica si está habilitado el modo de entrada en segundo plano.
ms.assetid: 2b57ebe9-3aad-400c-bcfb-d01c759b453d
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad allowBackgroundInput
- propiedad allowBackgroundInput Servicios de Escritorio remoto, interfaz IMsTscAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsTscAdvancedSettings, propiedad allowBackgroundInput
- propiedad allowBackgroundInput Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad allowBackgroundInput
- propiedad allowBackgroundInput Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad allowBackgroundInput
- propiedad allowBackgroundInput Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad allowBackgroundInput
- propiedad allowBackgroundInput Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad allowBackgroundInput
- propiedad allowBackgroundInput Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad allowBackgroundInput
- propiedad allowBackgroundInput Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad allowBackgroundInput
- propiedad allowBackgroundInput Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad allowBackgroundInput
- propiedad allowBackgroundInput Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad allowBackgroundInput
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.allowBackgroundInput
- IMsTscAdvancedSettings.get_allowBackgroundInput
- IMsTscAdvancedSettings.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings.allowBackgroundInput
- IMsRdpClientAdvancedSettings.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings2.allowBackgroundInput
- IMsRdpClientAdvancedSettings2.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings2.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings3.allowBackgroundInput
- IMsRdpClientAdvancedSettings3.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings3.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings4.allowBackgroundInput
- IMsRdpClientAdvancedSettings4.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings4.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings5.allowBackgroundInput
- IMsRdpClientAdvancedSettings5.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings5.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings6.allowBackgroundInput
- IMsRdpClientAdvancedSettings6.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings6.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings7.allowBackgroundInput
- IMsRdpClientAdvancedSettings7.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings7.put_allowBackgroundInput
- IMsRdpClientAdvancedSettings8.allowBackgroundInput
- IMsRdpClientAdvancedSettings8.get_allowBackgroundInput
- IMsRdpClientAdvancedSettings8.put_allowBackgroundInput
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 938725ea1aa3d774d5993be695ac8568963897fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422607"
---
# <a name="imstscadvancedsettingsallowbackgroundinput-property"></a><span data-ttu-id="18797-122">IMsTscAdvancedSettings:: allowBackgroundInput (propiedad)</span><span class="sxs-lookup"><span data-stu-id="18797-122">IMsTscAdvancedSettings::allowBackgroundInput property</span></span>

<span data-ttu-id="18797-123">Especifica si está habilitado el modo de entrada en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="18797-123">Specifies whether background input mode is enabled.</span></span> <span data-ttu-id="18797-124">Cuando la entrada en segundo plano está habilitada, el cliente puede aceptar la entrada cuando el cliente no tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="18797-124">When background input is enabled the client can accept input when the client does not have focus.</span></span>

<span data-ttu-id="18797-125">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="18797-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="18797-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="18797-126">Syntax</span></span>


```C++
HRESULT put_allowBackgroundInput(
  [in]  LONG allowBackgroundInput
);

HRESULT get_allowBackgroundInput(
  [out] LONG *pallowBackgroundInput
);
```



## <a name="property-value"></a><span data-ttu-id="18797-127">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="18797-127">Property value</span></span>

<span data-ttu-id="18797-128">Establezca este parámetro en 0 para deshabilitar el modo de entrada en segundo plano o un valor distinto de cero para habilitar el modo de entrada en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="18797-128">Set this parameter to 0 to disable background input mode or a nonzero value to enable background input mode.</span></span>

## <a name="error-codes"></a><span data-ttu-id="18797-129">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="18797-129">Error codes</span></span>

<span data-ttu-id="18797-130">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="18797-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="18797-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18797-131">Remarks</span></span>

<span data-ttu-id="18797-132">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="18797-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="18797-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18797-133">Requirements</span></span>



| <span data-ttu-id="18797-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="18797-134">Requirement</span></span> | <span data-ttu-id="18797-135">Value</span><span class="sxs-lookup"><span data-stu-id="18797-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="18797-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18797-136">Minimum supported client</span></span><br/> | <span data-ttu-id="18797-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18797-137">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="18797-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="18797-138">Minimum supported server</span></span><br/> | <span data-ttu-id="18797-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18797-139">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="18797-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="18797-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="18797-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18797-141"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="18797-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="18797-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18797-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18797-143"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="18797-144">IID</span><span class="sxs-lookup"><span data-stu-id="18797-144">IID</span></span><br/>                      | <span data-ttu-id="18797-145">IID \_ IMsTscAdvancedSettings se define como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="18797-145">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="18797-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="18797-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18797-147">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="18797-147">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="18797-148">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="18797-148">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="18797-149">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="18797-149">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="18797-150">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="18797-150">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="18797-151">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="18797-151">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="18797-152">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="18797-152">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="18797-153">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="18797-153">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="18797-154">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="18797-154">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="18797-155">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="18797-155">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





