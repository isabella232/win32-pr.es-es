---
title: Propiedad SecuredSettings2 de IMsRdpClient
description: Recupera un puntero a la interfaz IMsRdpClientSecuredSettings. Esta interfaz se puede usar para establecer la configuración segura para el control de cliente.
ms.assetid: f570a3f6-70ae-45fd-ba20-75c9f4d2f5ca
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad SecuredSettings2
- Propiedad SecuredSettings2 Servicios de Escritorio remoto, interfaz IMsRdpClient
- Servicios de Escritorio remoto de la interfaz IMsRdpClient, propiedad SecuredSettings2
- Propiedad SecuredSettings2 Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Servicios de Escritorio remoto de la interfaz IMsRdpClient2, propiedad SecuredSettings2
- Propiedad SecuredSettings2 Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Servicios de Escritorio remoto de la interfaz IMsRdpClient3, propiedad SecuredSettings2
- Propiedad SecuredSettings2 Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Servicios de Escritorio remoto de la interfaz IMsRdpClient4, propiedad SecuredSettings2
- Propiedad SecuredSettings2 Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad SecuredSettings2
- Propiedad SecuredSettings2 Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad SecuredSettings2
- Propiedad SecuredSettings2 Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad SecuredSettings2
- Propiedad SecuredSettings2 Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad SecuredSettings2
- Propiedad SecuredSettings2 Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad SecuredSettings2
- Propiedad SecuredSettings2 Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Servicios de Escritorio remoto de la interfaz IMsRdpClient10, propiedad SecuredSettings2
topic_type:
- apiref
api_name:
- IMsRdpClient.SecuredSettings2
- IMsRdpClient.get_SecuredSettings2
- IMsRdpClient2.SecuredSettings2
- IMsRdpClient2.get_SecuredSettings2
- IMsRdpClient3.SecuredSettings2
- IMsRdpClient3.get_SecuredSettings2
- IMsRdpClient4.SecuredSettings2
- IMsRdpClient4.get_SecuredSettings2
- IMsRdpClient5.SecuredSettings2
- IMsRdpClient5.get_SecuredSettings2
- IMsRdpClient6.SecuredSettings2
- IMsRdpClient6.get_SecuredSettings2
- IMsRdpClient7.SecuredSettings2
- IMsRdpClient7.get_SecuredSettings2
- IMsRdpClient8.SecuredSettings2
- IMsRdpClient8.get_SecuredSettings2
- IMsRdpClient9.SecuredSettings2
- IMsRdpClient9.get_SecuredSettings2
- IMsRdpClient10.SecuredSettings2
- IMsRdpClient10.get_SecuredSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39e26d9d7a7b2ac776166c251e5a2ab9923297f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533753"
---
# <a name="imsrdpclientsecuredsettings2-property"></a><span data-ttu-id="7581e-125">IMsRdpClient:: SecuredSettings2 (propiedad)</span><span class="sxs-lookup"><span data-stu-id="7581e-125">IMsRdpClient::SecuredSettings2 property</span></span>

<span data-ttu-id="7581e-126">Recupera un puntero a la interfaz [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="7581e-126">Retrieves a pointer to the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface.</span></span> <span data-ttu-id="7581e-127">Esta interfaz se puede usar para establecer la configuración segura para el control de cliente.</span><span class="sxs-lookup"><span data-stu-id="7581e-127">This interface can be used to set secured settings for the client control.</span></span>

<span data-ttu-id="7581e-128">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7581e-128">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7581e-129">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7581e-129">Syntax</span></span>


```C++
HRESULT get_SecuredSettings2(
  [out] IMsRdpClientSecuredSettings **ppSecuredSettings
);
```



## <a name="property-value"></a><span data-ttu-id="7581e-130">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7581e-130">Property value</span></span>

<span data-ttu-id="7581e-131">Puntero a la interfaz [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="7581e-131">An [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7581e-132">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="7581e-132">Error codes</span></span>

<span data-ttu-id="7581e-133">Si el método se ejecuta correctamente, se devuelve **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="7581e-133">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="7581e-134">Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="7581e-134">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="7581e-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7581e-135">Remarks</span></span>

<span data-ttu-id="7581e-136">Para obtener más información, consulte la interfaz [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) y [proporcione la seguridad del cliente RDP](providing-for-rdp-client-security.md).</span><span class="sxs-lookup"><span data-stu-id="7581e-136">For more information, see the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface, and [Providing for RDP Client Security](providing-for-rdp-client-security.md).</span></span>

<span data-ttu-id="7581e-137">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="7581e-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7581e-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7581e-138">Requirements</span></span>



| <span data-ttu-id="7581e-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="7581e-139">Requirement</span></span> | <span data-ttu-id="7581e-140">Value</span><span class="sxs-lookup"><span data-stu-id="7581e-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7581e-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7581e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="7581e-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7581e-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7581e-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7581e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="7581e-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7581e-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7581e-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7581e-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="7581e-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7581e-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7581e-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7581e-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7581e-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7581e-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7581e-149">IID</span><span class="sxs-lookup"><span data-stu-id="7581e-149">IID</span></span><br/>                      | <span data-ttu-id="7581e-150">IID \_ IMsRdpClient se define como 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="7581e-150">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="7581e-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="7581e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7581e-152">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="7581e-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="7581e-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="7581e-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="7581e-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="7581e-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="7581e-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="7581e-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="7581e-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="7581e-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="7581e-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="7581e-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="7581e-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="7581e-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="7581e-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="7581e-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="7581e-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="7581e-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="7581e-161">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="7581e-161">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





