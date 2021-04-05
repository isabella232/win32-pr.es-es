---
title: IMsRdpClientNonScriptable NotifyRedirectDeviceChange, método
description: Notifica al módulo de redireccionamiento de dispositivos del Escritorio remoto control ActiveX que se ha producido un cambio de dispositivo en el sistema. Este método pasa \_ las notificaciones de WM DEVICECHANGE al control.
ms.assetid: 36323831-06e0-4e47-8a6c-06367119298f
ms.tgt_platform: multiple
keywords:
- Método NotifyRedirectDeviceChange Servicios de Escritorio remoto
- Método NotifyRedirectDeviceChange Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable
- Interfaz IMsRdpClientNonScriptable Servicios de Escritorio remoto, método NotifyRedirectDeviceChange
- Método NotifyRedirectDeviceChange Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable2
- Interfaz IMsRdpClientNonScriptable2 Servicios de Escritorio remoto, método NotifyRedirectDeviceChange
- Método NotifyRedirectDeviceChange Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Interfaz IMsRdpClientNonScriptable3 Servicios de Escritorio remoto, método NotifyRedirectDeviceChange
- Método NotifyRedirectDeviceChange Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Interfaz IMsRdpClientNonScriptable4 Servicios de Escritorio remoto, método NotifyRedirectDeviceChange
- Método NotifyRedirectDeviceChange Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Interfaz IMsRdpClientNonScriptable5 Servicios de Escritorio remoto, método NotifyRedirectDeviceChange
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable2.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable3.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable4.NotifyRedirectDeviceChange
- IMsRdpClientNonScriptable5.NotifyRedirectDeviceChange
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7357fcb5e31eeeb0de5791425b8d9fada4365ab8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997055"
---
# <a name="imsrdpclientnonscriptablenotifyredirectdevicechange-method"></a><span data-ttu-id="74509-115">IMsRdpClientNonScriptable:: NotifyRedirectDeviceChange (método)</span><span class="sxs-lookup"><span data-stu-id="74509-115">IMsRdpClientNonScriptable::NotifyRedirectDeviceChange method</span></span>

<span data-ttu-id="74509-116">Notifica al módulo de redireccionamiento de dispositivos del Escritorio remoto control ActiveX que se ha producido un cambio de dispositivo en el sistema.</span><span class="sxs-lookup"><span data-stu-id="74509-116">Notifies the device redirection module of the Remote Desktop ActiveX control that a device change has occurred on the system.</span></span> <span data-ttu-id="74509-117">Este método pasa las notificaciones de [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) al control.</span><span class="sxs-lookup"><span data-stu-id="74509-117">This method passes [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) notifications to the control.</span></span>

## <a name="syntax"></a><span data-ttu-id="74509-118">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="74509-118">Syntax</span></span>


```C++
HRESULT NotifyRedirectDeviceChange(
  [in] WPARAM wParam,
  [in] LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="74509-119">Parámetros</span><span class="sxs-lookup"><span data-stu-id="74509-119">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74509-120">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74509-120">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74509-121">Especifica el evento de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74509-121">Specifies the device event.</span></span> <span data-ttu-id="74509-122">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="74509-122">This parameter can be one of the following values.</span></span>

<dt>

<span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>

<span data-ttu-id="74509-123"><span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>**DBT \_ CONFIGCHANGECANCELED**</span><span class="sxs-lookup"><span data-stu-id="74509-123"><span id="DBT_CONFIGCHANGECANCELED"></span><span id="dbt_configchangecanceled"></span>**DBT\_CONFIGCHANGECANCELED**</span></span>


</dt> <dd>

<span data-ttu-id="74509-124">Se ha cancelado una solicitud para cambiar la configuración actual (acoplar o desacoplar).</span><span class="sxs-lookup"><span data-stu-id="74509-124">A request to change the current configuration (dock or undock) has been canceled.</span></span>

</dd> <dt>

<span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>

<span data-ttu-id="74509-125"><span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>**DBT \_ CONFIGCHANGED**</span><span class="sxs-lookup"><span data-stu-id="74509-125"><span id="DBT_CONFIGCHANGED"></span><span id="dbt_configchanged"></span>**DBT\_CONFIGCHANGED**</span></span>


</dt> <dd>

<span data-ttu-id="74509-126">La configuración actual ha cambiado debido a un acoplamiento o desacoplamiento.</span><span class="sxs-lookup"><span data-stu-id="74509-126">The current configuration has changed due to a dock or undock.</span></span>

</dd> <dt>

<span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>

<span data-ttu-id="74509-127"><span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>**DBT \_ CUSTOMEVENT**</span><span class="sxs-lookup"><span data-stu-id="74509-127"><span id="DBT_CUSTOMEVENT"></span><span id="dbt_customevent"></span>**DBT\_CUSTOMEVENT**</span></span>


</dt> <dd>

<span data-ttu-id="74509-128">Se ha producido un evento personalizado.</span><span class="sxs-lookup"><span data-stu-id="74509-128">A custom event has occurred.</span></span>

</dd> <dt>

<span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>

<span data-ttu-id="74509-129"><span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>**DBT \_ DEVICEARRIVAL**</span><span class="sxs-lookup"><span data-stu-id="74509-129"><span id="DBT_DEVICEARRIVAL"></span><span id="dbt_devicearrival"></span>**DBT\_DEVICEARRIVAL**</span></span>


</dt> <dd>

<span data-ttu-id="74509-130">Se ha insertado un dispositivo y ahora está disponible.</span><span class="sxs-lookup"><span data-stu-id="74509-130">A device has been inserted and is now available.</span></span>

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>

<span data-ttu-id="74509-131"><span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>**DBT \_ DEVICEQUERYREMOVE**</span><span class="sxs-lookup"><span data-stu-id="74509-131"><span id="DBT_DEVICEQUERYREMOVE"></span><span id="dbt_devicequeryremove"></span>**DBT\_DEVICEQUERYREMOVE**</span></span>


</dt> <dd>

<span data-ttu-id="74509-132">Se solicita permiso para quitar un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74509-132">Permission is requested to remove a device.</span></span> <span data-ttu-id="74509-133">Cualquier aplicación puede denegar esta solicitud y cancelar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="74509-133">Any application can deny this request and cancel the removal.</span></span>

</dd> <dt>

<span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>

<span data-ttu-id="74509-134"><span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>**DBT \_ DEVICEQUERYREMOVEFAILED**</span><span class="sxs-lookup"><span data-stu-id="74509-134"><span id="DBT_DEVICEQUERYREMOVEFAILED"></span><span id="dbt_devicequeryremovefailed"></span>**DBT\_DEVICEQUERYREMOVEFAILED**</span></span>


</dt> <dd>

<span data-ttu-id="74509-135">Se canceló una solicitud para quitar un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74509-135">A request to remove a device has been canceled.</span></span>

</dd> <dt>

<span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>

<span data-ttu-id="74509-136"><span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>**DBT \_ DEVICEREMOVECOMPLETE**</span><span class="sxs-lookup"><span data-stu-id="74509-136"><span id="DBT_DEVICEREMOVECOMPLETE"></span><span id="dbt_deviceremovecomplete"></span>**DBT\_DEVICEREMOVECOMPLETE**</span></span>


</dt> <dd>

<span data-ttu-id="74509-137">Se ha quitado un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74509-137">A device has been removed.</span></span>

</dd> <dt>

<span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>

<span data-ttu-id="74509-138"><span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>**DBT \_ DEVICEREMOVEPENDING**</span><span class="sxs-lookup"><span data-stu-id="74509-138"><span id="DBT_DEVICEREMOVEPENDING"></span><span id="dbt_deviceremovepending"></span>**DBT\_DEVICEREMOVEPENDING**</span></span>


</dt> <dd>

<span data-ttu-id="74509-139">Un dispositivo está a punto de quitarse.</span><span class="sxs-lookup"><span data-stu-id="74509-139">A device is about to be removed.</span></span> <span data-ttu-id="74509-140">No se puede denegar la eliminación.</span><span class="sxs-lookup"><span data-stu-id="74509-140">The removal cannot be denied.</span></span>

</dd> <dt>

<span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>

<span data-ttu-id="74509-141"><span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>**DBT \_ DEVICETYPESPECIFIC**</span><span class="sxs-lookup"><span data-stu-id="74509-141"><span id="DBT_DEVICETYPESPECIFIC"></span><span id="dbt_devicetypespecific"></span>**DBT\_DEVICETYPESPECIFIC**</span></span>


</dt> <dd>

<span data-ttu-id="74509-142">Se ha producido un evento específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="74509-142">A device-specific event has occurred.</span></span>

</dd> <dt>

<span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>

<span data-ttu-id="74509-143"><span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>**DBT \_ DEVNODES \_ Changed**</span><span class="sxs-lookup"><span data-stu-id="74509-143"><span id="DBT_DEVNODES_CHANGED"></span><span id="dbt_devnodes_changed"></span>**DBT\_DEVNODES\_CHANGED**</span></span>


</dt> <dd>

<span data-ttu-id="74509-144">Se ha agregado o quitado un dispositivo del sistema.</span><span class="sxs-lookup"><span data-stu-id="74509-144">A device has been added to or removed from the system.</span></span>

</dd> <dt>

<span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>

<span data-ttu-id="74509-145"><span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>**DBT \_ QUERYCHANGECONFIG**</span><span class="sxs-lookup"><span data-stu-id="74509-145"><span id="DBT_QUERYCHANGECONFIG"></span><span id="dbt_querychangeconfig"></span>**DBT\_QUERYCHANGECONFIG**</span></span>


</dt> <dd>

<span data-ttu-id="74509-146">Se solicita permiso para cambiar la configuración actual (acoplar o desacoplar).</span><span class="sxs-lookup"><span data-stu-id="74509-146">Permission is requested to change the current configuration (dock or undock).</span></span>

</dd> <dt>

<span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>

<span data-ttu-id="74509-147"><span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>**DBT \_ USERDEFINED**</span><span class="sxs-lookup"><span data-stu-id="74509-147"><span id="DBT_USERDEFINED"></span><span id="dbt_userdefined"></span>**DBT\_USERDEFINED**</span></span>


</dt> <dd>

<span data-ttu-id="74509-148">El significado de este mensaje está definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="74509-148">The meaning of this message is user-defined.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="74509-149">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="74509-149">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74509-150">Puntero a una estructura que contiene datos específicos del evento.</span><span class="sxs-lookup"><span data-stu-id="74509-150">Pointer to a structure that contains event-specific data.</span></span> <span data-ttu-id="74509-151">Su formato depende del valor del parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="74509-151">Its format depends on the value of the *wParam* parameter.</span></span> <span data-ttu-id="74509-152">Para obtener más información, consulte la documentación de cada evento.</span><span class="sxs-lookup"><span data-stu-id="74509-152">For more information, refer to the documentation for each event.</span></span> <span data-ttu-id="74509-153">Para obtener más información, consulte [tipos de eventos de dispositivo](/windows/desktop/DevIO/device-event-types).</span><span class="sxs-lookup"><span data-stu-id="74509-153">For more information, see [Device Event Types](/windows/desktop/DevIO/device-event-types).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74509-154">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="74509-154">Return value</span></span>

<span data-ttu-id="74509-155">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="74509-155">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="74509-156">Observaciones</span><span class="sxs-lookup"><span data-stu-id="74509-156">Remarks</span></span>

<span data-ttu-id="74509-157">Una aplicación contenedora que permita la adición o eliminación dinámica de dispositivos debe procesar el mensaje de [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) en su ventana de nivel superior y reenviar el mensaje al control mediante el método **NotifyRedirectDeviceChange** .</span><span class="sxs-lookup"><span data-stu-id="74509-157">A container application that allows dynamic addition or removal of devices should process the [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) message in its top level window and forward the message to the control using the **NotifyRedirectDeviceChange** method.</span></span> <span data-ttu-id="74509-158">Un ejemplo de cambio dinámico de un dispositivo es cuando se agrega o se quita una unidad de disco redirigida mientras el sistema se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="74509-158">An example of a dynamic device change is when a redirected disk drive is added or removed while the system is running.</span></span>

<span data-ttu-id="74509-159">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="74509-159">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74509-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74509-160">Requirements</span></span>



| <span data-ttu-id="74509-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="74509-161">Requirement</span></span> | <span data-ttu-id="74509-162">Value</span><span class="sxs-lookup"><span data-stu-id="74509-162">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="74509-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74509-163">Minimum supported client</span></span><br/> | <span data-ttu-id="74509-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="74509-164">Windows Vista</span></span><br/>                                                                     |
| <span data-ttu-id="74509-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="74509-165">Minimum supported server</span></span><br/> | <span data-ttu-id="74509-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74509-166">Windows Server 2008</span></span><br/>                                                               |
| <span data-ttu-id="74509-167">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="74509-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="74509-168"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74509-168"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="74509-169">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="74509-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74509-170"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74509-170"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="74509-171">IID</span><span class="sxs-lookup"><span data-stu-id="74509-171">IID</span></span><br/>                      | <span data-ttu-id="74509-172">IID \_ IMsRdpClientNonScriptable se define como 2f079c4c-87b2-4afd-97ab-20cdb43038ae</span><span class="sxs-lookup"><span data-stu-id="74509-172">IID\_IMsRdpClientNonScriptable is defined as 2f079c4c-87b2-4afd-97ab-20cdb43038ae</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="74509-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="74509-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74509-174">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="74509-174">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="74509-175">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="74509-175">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="74509-176">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="74509-176">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="74509-177">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="74509-177">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="74509-178">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="74509-178">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> </dl>

 

