---
title: Propiedad keepAliveInterval de IMsRdpClientAdvancedSettings
description: Especifica un intervalo, en milisegundos, en el que el cliente envía mensajes persistentes al servidor.
ms.assetid: 0d1b7d8f-f81c-4591-bb08-adab307e87fe
ms.tgt_platform: multiple
keywords:
- propiedad keepAliveInterval Servicios de Escritorio remoto
- propiedad keepAliveInterval Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad keepAliveInterval
- propiedad keepAliveInterval Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad keepAliveInterval
- propiedad keepAliveInterval Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad keepAliveInterval
- propiedad keepAliveInterval Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad keepAliveInterval
- propiedad keepAliveInterval Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad keepAliveInterval
- propiedad keepAliveInterval Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad keepAliveInterval
- propiedad keepAliveInterval Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad keepAliveInterval
- propiedad keepAliveInterval Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad keepAliveInterval
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.keepAliveInterval
- IMsRdpClientAdvancedSettings.get_keepAliveInterval
- IMsRdpClientAdvancedSettings.put_keepAliveInterval
- IMsRdpClientAdvancedSettings2.keepAliveInterval
- IMsRdpClientAdvancedSettings2.get_keepAliveInterval
- IMsRdpClientAdvancedSettings2.put_keepAliveInterval
- IMsRdpClientAdvancedSettings3.keepAliveInterval
- IMsRdpClientAdvancedSettings3.get_keepAliveInterval
- IMsRdpClientAdvancedSettings3.put_keepAliveInterval
- IMsRdpClientAdvancedSettings4.keepAliveInterval
- IMsRdpClientAdvancedSettings4.get_keepAliveInterval
- IMsRdpClientAdvancedSettings4.put_keepAliveInterval
- IMsRdpClientAdvancedSettings5.keepAliveInterval
- IMsRdpClientAdvancedSettings5.get_keepAliveInterval
- IMsRdpClientAdvancedSettings5.put_keepAliveInterval
- IMsRdpClientAdvancedSettings6.keepAliveInterval
- IMsRdpClientAdvancedSettings6.get_keepAliveInterval
- IMsRdpClientAdvancedSettings6.put_keepAliveInterval
- IMsRdpClientAdvancedSettings7.keepAliveInterval
- IMsRdpClientAdvancedSettings7.get_keepAliveInterval
- IMsRdpClientAdvancedSettings7.put_keepAliveInterval
- IMsRdpClientAdvancedSettings8.keepAliveInterval
- IMsRdpClientAdvancedSettings8.get_keepAliveInterval
- IMsRdpClientAdvancedSettings8.put_keepAliveInterval
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d15412b5b1803aadcffa08a8617742e0c90b1a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422139"
---
# <a name="imsrdpclientadvancedsettingskeepaliveinterval-property"></a><span data-ttu-id="e1fd4-120">IMsRdpClientAdvancedSettings:: keepAliveInterval (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e1fd4-120">IMsRdpClientAdvancedSettings::keepAliveInterval property</span></span>

<span data-ttu-id="e1fd4-121">Especifica un intervalo, en milisegundos, en el que el cliente envía mensajes persistentes al servidor.</span><span class="sxs-lookup"><span data-stu-id="e1fd4-121">Specifies an interval, in milliseconds, at which the client sends keep-alive messages to the server.</span></span>

<span data-ttu-id="e1fd4-122">Una configuración de directiva de grupo que especifica si se permiten conexiones de cliente persistentes al servidor puede invalidar esta configuración de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e1fd4-122">A group policy setting that specifies whether persistent client connections to the server are allowed can override this property setting.</span></span>

<span data-ttu-id="e1fd4-123">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e1fd4-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1fd4-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1fd4-124">Syntax</span></span>


```C++
HRESULT put_keepAliveInterval(
  [in]  LONG keepAliveInterval
);

HRESULT get_keepAliveInterval(
  [out] LONG *pkeepAliveInterval
);
```



## <a name="property-value"></a><span data-ttu-id="e1fd4-125">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e1fd4-125">Property value</span></span>

<span data-ttu-id="e1fd4-126">Nuevo intervalo, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="e1fd4-126">The new interval, in milliseconds.</span></span> <span data-ttu-id="e1fd4-127">El valor predeterminado de la propiedad es cero, lo que deshabilita los mensajes persistentes.</span><span class="sxs-lookup"><span data-stu-id="e1fd4-127">The default value of the property is zero, which disables keep-alive messages.</span></span> <span data-ttu-id="e1fd4-128">El valor mínimo válido de esta propiedad es 10.000, que representa 10 segundos.</span><span class="sxs-lookup"><span data-stu-id="e1fd4-128">The minimum valid value of this property is 10,000, which represents 10 seconds.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e1fd4-129">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="e1fd4-129">Error codes</span></span>

<span data-ttu-id="e1fd4-130">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="e1fd4-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1fd4-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1fd4-131">Remarks</span></span>

<span data-ttu-id="e1fd4-132">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e1fd4-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1fd4-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1fd4-133">Requirements</span></span>



| <span data-ttu-id="e1fd4-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1fd4-134">Requirement</span></span> | <span data-ttu-id="e1fd4-135">Value</span><span class="sxs-lookup"><span data-stu-id="e1fd4-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1fd4-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1fd4-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e1fd4-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1fd4-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="e1fd4-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e1fd4-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e1fd4-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e1fd4-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="e1fd4-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e1fd4-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="e1fd4-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1fd4-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="e1fd4-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e1fd4-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1fd4-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1fd4-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="e1fd4-144">IID</span><span class="sxs-lookup"><span data-stu-id="e1fd4-144">IID</span></span><br/>                      | <span data-ttu-id="e1fd4-145">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="e1fd4-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e1fd4-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1fd4-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1fd4-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="e1fd4-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="e1fd4-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="e1fd4-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="e1fd4-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="e1fd4-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="e1fd4-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="e1fd4-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="e1fd4-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="e1fd4-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="e1fd4-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="e1fd4-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="e1fd4-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="e1fd4-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="e1fd4-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="e1fd4-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





