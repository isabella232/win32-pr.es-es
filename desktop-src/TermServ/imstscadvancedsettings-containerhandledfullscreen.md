---
title: Propiedad ContainerHandledFullScreen de IMsTscAdvancedSettings
description: Especifica si está habilitado el modo de pantalla completa controlado por contenedores.
ms.assetid: 67679323-4a74-4d91-abd0-607415295f3d
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad ContainerHandledFullScreen
- Propiedad ContainerHandledFullScreen Servicios de Escritorio remoto, interfaz IMsTscAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsTscAdvancedSettings, propiedad ContainerHandledFullScreen
- Propiedad ContainerHandledFullScreen Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad ContainerHandledFullScreen
- Propiedad ContainerHandledFullScreen Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad ContainerHandledFullScreen
- Propiedad ContainerHandledFullScreen Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad ContainerHandledFullScreen
- Propiedad ContainerHandledFullScreen Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad ContainerHandledFullScreen
- Propiedad ContainerHandledFullScreen Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad ContainerHandledFullScreen
- Propiedad ContainerHandledFullScreen Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad ContainerHandledFullScreen
- Propiedad ContainerHandledFullScreen Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad ContainerHandledFullScreen
- Propiedad ContainerHandledFullScreen Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad ContainerHandledFullScreen
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.ContainerHandledFullScreen
- IMsTscAdvancedSettings.get_ContainerHandledFullScreen
- IMsTscAdvancedSettings.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings2.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings3.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings4.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings5.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings6.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings7.put_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.get_ContainerHandledFullScreen
- IMsRdpClientAdvancedSettings8.put_ContainerHandledFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a7442ce16e2ff30ca2d9b3bd529d37382d1df41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422428"
---
# <a name="imstscadvancedsettingscontainerhandledfullscreen-property"></a><span data-ttu-id="c8e02-122">IMsTscAdvancedSettings:: ContainerHandledFullScreen (propiedad)</span><span class="sxs-lookup"><span data-stu-id="c8e02-122">IMsTscAdvancedSettings::ContainerHandledFullScreen property</span></span>

<span data-ttu-id="c8e02-123">Especifica si está habilitado el modo de pantalla completa controlado por contenedores.</span><span class="sxs-lookup"><span data-stu-id="c8e02-123">Specifies whether the container-handled full-screen mode is enabled.</span></span>

> [!Note]  
> <span data-ttu-id="c8e02-124">El valor de la propiedad **ContainerHandledFullScreen** no tiene ningún efecto cuando el control ActiveX escritorio remoto es seguro para el scripting y devuelve **S \_ false** cuando se realiza un intento de cambiar el valor.</span><span class="sxs-lookup"><span data-stu-id="c8e02-124">The value of the **ContainerHandledFullScreen** property has no effect when the Remote Desktop ActiveX control is safe for scripting, and returns **S\_FALSE** when an attempt is made to change the value.</span></span>

 

<span data-ttu-id="c8e02-125">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="c8e02-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8e02-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8e02-126">Syntax</span></span>


```C++
HRESULT put_ContainerHandledFullScreen(
  [in]  BOOL ContainerHandledFullScreen
);

HRESULT get_ContainerHandledFullScreen(
  [out] BOOL *pContainerHandledFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="c8e02-127">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c8e02-127">Property value</span></span>

<span data-ttu-id="c8e02-128">Establezca este parámetro en **true** para habilitar el modo u otro valor para deshabilitar el modo.</span><span class="sxs-lookup"><span data-stu-id="c8e02-128">Set this parameter to **TRUE** to enable the mode or another value to disable the mode.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c8e02-129">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="c8e02-129">Error codes</span></span>

<span data-ttu-id="c8e02-130">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="c8e02-130">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="c8e02-131">Devuelve **S \_ false** si no se admite.</span><span class="sxs-lookup"><span data-stu-id="c8e02-131">Returns **S\_FALSE** if not supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8e02-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8e02-132">Remarks</span></span>

<span data-ttu-id="c8e02-133">Cuando este modo está habilitado, el contenedor actual procesa el modificador dentro y fuera del modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="c8e02-133">When this mode is enabled, the current container processes the switch into and out of full-screen mode.</span></span> <span data-ttu-id="c8e02-134">Este método solo se debe usar si el contenedor actual necesita un control extensivo sobre el comportamiento del modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="c8e02-134">This method should be used only if the current container needs extensive control over full-screen mode behavior.</span></span> <span data-ttu-id="c8e02-135">Cuando se establece esta propiedad, el control no entra o sale del modo de pantalla completa en respuesta a la combinación de teclas de método abreviado del modo de pantalla completa (CTRL + ALT + inter); en su lugar, se llama a los eventos [**IMsTscAxEvents:: OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md) y [**IMsTscAxEvents:: OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md) .</span><span class="sxs-lookup"><span data-stu-id="c8e02-135">When this property is set, the control does not enter or leave full-screen mode in response to the full-screen mode shortcut key combination (CTRL+ALT+BREAK); instead, the [**IMsTscAxEvents::OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md) and [**IMsTscAxEvents::OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md) events are called.</span></span> <span data-ttu-id="c8e02-136">Vea [**IMsTscAxEvents**](imstscaxevents-interface.md) para obtener más información sobre estos eventos.</span><span class="sxs-lookup"><span data-stu-id="c8e02-136">See [**IMsTscAxEvents**](imstscaxevents-interface.md) for more information about these events.</span></span>

<span data-ttu-id="c8e02-137">La mayoría de las aplicaciones contenedoras no tendrán que usar el modo de pantalla completa controlado por contenedores.</span><span class="sxs-lookup"><span data-stu-id="c8e02-137">Most container applications will not need to use container-handled full-screen mode.</span></span>

<span data-ttu-id="c8e02-138">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c8e02-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c8e02-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8e02-139">Requirements</span></span>



| <span data-ttu-id="c8e02-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8e02-140">Requirement</span></span> | <span data-ttu-id="c8e02-141">Value</span><span class="sxs-lookup"><span data-stu-id="c8e02-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8e02-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8e02-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c8e02-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8e02-143">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="c8e02-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8e02-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c8e02-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8e02-145">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="c8e02-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c8e02-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="c8e02-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8e02-147"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="c8e02-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c8e02-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8e02-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8e02-149"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="c8e02-150">IID</span><span class="sxs-lookup"><span data-stu-id="c8e02-150">IID</span></span><br/>                      | <span data-ttu-id="c8e02-151">IID \_ IMsTscAdvancedSettings se define como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="c8e02-151">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c8e02-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8e02-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8e02-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="c8e02-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="c8e02-154">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="c8e02-154">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="c8e02-155">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="c8e02-155">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="c8e02-156">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="c8e02-156">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="c8e02-157">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="c8e02-157">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="c8e02-158">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="c8e02-158">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="c8e02-159">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="c8e02-159">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="c8e02-160">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="c8e02-160">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="c8e02-161">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="c8e02-161">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





