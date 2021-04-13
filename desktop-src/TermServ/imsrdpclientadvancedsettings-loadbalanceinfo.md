---
title: Propiedad LoadBalanceInfo de IMsRdpClientAdvancedSettings
description: Especifica la cookie de equilibrio de carga que se colocará en el paquete de solicitud de conexión X. 224 en la secuencia de conexión del Protocolo de servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto).
ms.assetid: 25f12a2e-00a2-42a8-afd3-81efcd94da94
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad LoadBalanceInfo
- Propiedad LoadBalanceInfo Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad LoadBalanceInfo
- Propiedad LoadBalanceInfo Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad LoadBalanceInfo
- Propiedad LoadBalanceInfo Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad LoadBalanceInfo
- Propiedad LoadBalanceInfo Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad LoadBalanceInfo
- Propiedad LoadBalanceInfo Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad LoadBalanceInfo
- Propiedad LoadBalanceInfo Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad LoadBalanceInfo
- Propiedad LoadBalanceInfo Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad LoadBalanceInfo
- Propiedad LoadBalanceInfo Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad LoadBalanceInfo
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.LoadBalanceInfo
- IMsRdpClientAdvancedSettings.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.put_LoadBalanceInfo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a12112eb2a18d38993e905f8d36175f1ab15f58a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422138"
---
# <a name="imsrdpclientadvancedsettingsloadbalanceinfo-property"></a><span data-ttu-id="d676d-120">IMsRdpClientAdvancedSettings:: LoadBalanceInfo (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d676d-120">IMsRdpClientAdvancedSettings::LoadBalanceInfo property</span></span>

<span data-ttu-id="d676d-121">Especifica la cookie de equilibrio de carga que se colocará en el paquete de solicitud de conexión X. 224 en la secuencia de conexión del Protocolo de servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="d676d-121">Specifies the load balancing cookie that will be placed in the X.224 Connection Request packet in the Remote Desktop Session Host (RD Session Host) server protocol connection sequence.</span></span>

<span data-ttu-id="d676d-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d676d-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d676d-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d676d-123">Syntax</span></span>


```C++
HRESULT put_LoadBalanceInfo(
  [in]  BSTR newLBInfo
);

HRESULT get_LoadBalanceInfo(
  [out] BSTR *pLBInfo
);
```



## <a name="property-value"></a><span data-ttu-id="d676d-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d676d-124">Property value</span></span>

<span data-ttu-id="d676d-125">Puntero a la nueva cookie.</span><span class="sxs-lookup"><span data-stu-id="d676d-125">Pointer to the new cookie.</span></span> <span data-ttu-id="d676d-126">Para obtener más información, vea la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="d676d-126">For more information, see the remarks section.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d676d-127">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="d676d-127">Error codes</span></span>

<span data-ttu-id="d676d-128">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="d676d-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d676d-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d676d-129">Remarks</span></span>

<span data-ttu-id="d676d-130">Los enrutadores de equilibrio de carga usan la información de equilibrio de carga para elegir el mejor servidor para el cliente cuando se usan granjas de servidores host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d676d-130">The load balancing information is used by load balancing routers to choose the best server for the client when using farms of RD Session Host servers.</span></span> <span data-ttu-id="d676d-131">El propio servidor host de sesión de escritorio remoto no usa esta información y lo descartará.</span><span class="sxs-lookup"><span data-stu-id="d676d-131">The RD Session Host server itself does not use this information and will discard it.</span></span>

<span data-ttu-id="d676d-132">La cookie utiliza la sintaxis siguiente, que distingue entre mayúsculas y minúsculas:</span><span class="sxs-lookup"><span data-stu-id="d676d-132">The cookie uses the following, case-sensitive, syntax:</span></span>

<span data-ttu-id="d676d-133">**Cookie: MSTS =**_IpAddressAndPortNumber_*_\\ r \\ n_*</span><span class="sxs-lookup"><span data-stu-id="d676d-133">**Cookie: msts=**_IpAddressAndPortNumber_*_\\r\\n_*</span></span>

<span data-ttu-id="d676d-134">Donde *IpAddressAndPortNumber* es la dirección IP y el número de puerto, en el orden de bytes de la red.</span><span class="sxs-lookup"><span data-stu-id="d676d-134">Where *IpAddressAndPortNumber* is the IP address and port number, in network byte order.</span></span>

<span data-ttu-id="d676d-135">Por ejemplo, la cookie usada para tener acceso a la dirección IP de 172.31.249.216, el número de Puerto 3389 es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="d676d-135">For example, the cookie used to access the IP address of 172.31.249.216, port number 3389 is as follows:</span></span>

<span data-ttu-id="d676d-136">**Cookie: MSTS = 3640205228.15629.0000 \\ r \\ n**</span><span class="sxs-lookup"><span data-stu-id="d676d-136">**Cookie: msts=3640205228.15629.0000\\r\\n**</span></span>

<span data-ttu-id="d676d-137">Los cuatro últimos ceros son opcionales y están reservados.</span><span class="sxs-lookup"><span data-stu-id="d676d-137">The final four zeros are optional and are reserved.</span></span> <span data-ttu-id="d676d-138">El último punto decimal es obligatorio, al igual que el retorno de carro y el avance de carro finales.</span><span class="sxs-lookup"><span data-stu-id="d676d-138">The final decimal point is required, as are the trailing carriage return and linefeed.</span></span> <span data-ttu-id="d676d-139">La longitud de la cadena, en caracteres, debe ser un múltiplo par de 2, por lo que debe agregar un espacio si es necesario.</span><span class="sxs-lookup"><span data-stu-id="d676d-139">The length of the string, in characters, must be an even multiple of 2, so add a space if necessary.</span></span>

<span data-ttu-id="d676d-140">Si no se proporciona ninguna cookie, el valor predeterminado es **Cookie: mstshash =**_username_*_\\ r \\ n_*.</span><span class="sxs-lookup"><span data-stu-id="d676d-140">If no cookie is supplied, the default is **Cookie: mstshash=**_UserName_*_\\r\\n_*.</span></span>

<span data-ttu-id="d676d-141">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d676d-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d676d-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d676d-142">Requirements</span></span>



| <span data-ttu-id="d676d-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="d676d-143">Requirement</span></span> | <span data-ttu-id="d676d-144">Value</span><span class="sxs-lookup"><span data-stu-id="d676d-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d676d-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d676d-145">Minimum supported client</span></span><br/> | <span data-ttu-id="d676d-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d676d-146">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="d676d-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d676d-147">Minimum supported server</span></span><br/> | <span data-ttu-id="d676d-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d676d-148">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="d676d-149">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d676d-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="d676d-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d676d-150"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d676d-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d676d-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d676d-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d676d-152"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="d676d-153">IID</span><span class="sxs-lookup"><span data-stu-id="d676d-153">IID</span></span><br/>                      | <span data-ttu-id="d676d-154">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="d676d-154">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d676d-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="d676d-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d676d-156">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="d676d-156">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="d676d-157">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="d676d-157">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="d676d-158">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="d676d-158">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="d676d-159">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="d676d-159">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="d676d-160">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="d676d-160">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="d676d-161">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="d676d-161">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="d676d-162">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="d676d-162">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="d676d-163">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="d676d-163">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





