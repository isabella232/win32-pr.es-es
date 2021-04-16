---
title: Propiedad MinutesToIdleTimeout de IMsRdpClientAdvancedSettings
description: Especifica el período de tiempo máximo, en minutos, que el cliente debe permanecer conectado sin intervención del usuario. Si transcurre el tiempo especificado, el control llama al método OnIdleTimeoutNotification de IMsTscAxEvents.
ms.assetid: 709238ea-45f8-4bdc-9bbe-019d54ca27bf
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad MinutesToIdleTimeout
- Propiedad MinutesToIdleTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad MinutesToIdleTimeout
- Propiedad MinutesToIdleTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad MinutesToIdleTimeout
- Propiedad MinutesToIdleTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad MinutesToIdleTimeout
- Propiedad MinutesToIdleTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad MinutesToIdleTimeout
- Propiedad MinutesToIdleTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad MinutesToIdleTimeout
- Propiedad MinutesToIdleTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad MinutesToIdleTimeout
- Propiedad MinutesToIdleTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad MinutesToIdleTimeout
- Propiedad MinutesToIdleTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad MinutesToIdleTimeout
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings2.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings3.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings4.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings5.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings6.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings7.put_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.get_MinutesToIdleTimeout
- IMsRdpClientAdvancedSettings8.put_MinutesToIdleTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5e42258ed670ac0323723cafe7b2792f8c5bd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685930"
---
# <a name="imsrdpclientadvancedsettingsminutestoidletimeout-property"></a><span data-ttu-id="4f672-121">IMsRdpClientAdvancedSettings:: MinutesToIdleTimeout (propiedad)</span><span class="sxs-lookup"><span data-stu-id="4f672-121">IMsRdpClientAdvancedSettings::MinutesToIdleTimeout property</span></span>

<span data-ttu-id="4f672-122">Especifica el período de tiempo máximo, en minutos, que el cliente debe permanecer conectado sin intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="4f672-122">Specifies the maximum length of time, in minutes, that the client should remain connected without user input.</span></span> <span data-ttu-id="4f672-123">Si transcurre el tiempo especificado, el control llama al método [**IMsTscAxEvents:: OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="4f672-123">If the specified time elapses, the control calls the [**IMsTscAxEvents::OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md) method.</span></span>

<span data-ttu-id="4f672-124">Puede usar esta propiedad en una situación en la que necesite desconectar una sesión inactiva; por ejemplo, en un entorno de quiosco.</span><span class="sxs-lookup"><span data-stu-id="4f672-124">You can use this property in a situation where you need to disconnect an idle session; for example, in a kiosk environment.</span></span>

<span data-ttu-id="4f672-125">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="4f672-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f672-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f672-126">Syntax</span></span>


```C++
HRESULT put_MinutesToIdleTimeout(
  [in]  LONG minutesToIdleTimeout
);

HRESULT get_MinutesToIdleTimeout(
  [out] LONG *pminutesToIdleTimeout
);
```



## <a name="property-value"></a><span data-ttu-id="4f672-127">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4f672-127">Property value</span></span>

<span data-ttu-id="4f672-128">La nueva hora, en minutos.</span><span class="sxs-lookup"><span data-stu-id="4f672-128">The new time, in minutes.</span></span> <span data-ttu-id="4f672-129">El valor predeterminado es cero, lo que deshabilita la característica.</span><span class="sxs-lookup"><span data-stu-id="4f672-129">The default value is zero, which disables the feature.</span></span> <span data-ttu-id="4f672-130">El valor máximo es 240, que representa 4 horas.</span><span class="sxs-lookup"><span data-stu-id="4f672-130">The maximum value is 240, which represents 4 hours.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4f672-131">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="4f672-131">Error codes</span></span>

<span data-ttu-id="4f672-132">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="4f672-132">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f672-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f672-133">Remarks</span></span>

<span data-ttu-id="4f672-134">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="4f672-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f672-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f672-135">Requirements</span></span>



| <span data-ttu-id="4f672-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f672-136">Requirement</span></span> | <span data-ttu-id="4f672-137">Value</span><span class="sxs-lookup"><span data-stu-id="4f672-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f672-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f672-138">Minimum supported client</span></span><br/> | <span data-ttu-id="4f672-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f672-139">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="4f672-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f672-140">Minimum supported server</span></span><br/> | <span data-ttu-id="4f672-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f672-141">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="4f672-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4f672-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="4f672-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f672-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="4f672-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4f672-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f672-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f672-145"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="4f672-146">IID</span><span class="sxs-lookup"><span data-stu-id="4f672-146">IID</span></span><br/>                      | <span data-ttu-id="4f672-147">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="4f672-147">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4f672-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f672-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f672-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="4f672-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="4f672-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="4f672-150">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="4f672-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="4f672-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="4f672-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="4f672-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="4f672-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="4f672-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="4f672-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="4f672-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="4f672-155">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="4f672-155">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="4f672-156">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="4f672-156">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





