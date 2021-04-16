---
title: Propiedad AdvancedSettings2 de IMsRdpClient
description: Recupera un puntero a la interfaz IMsRdpClientAdvancedSettings. La interfaz se puede utilizar para establecer la configuración avanzada del control de cliente.
ms.assetid: 207b625c-fc2b-41ad-9339-9f3c3b8eeab7
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad AdvancedSettings2
- Propiedad AdvancedSettings2 Servicios de Escritorio remoto, interfaz IMsRdpClient
- Servicios de Escritorio remoto de la interfaz IMsRdpClient, propiedad AdvancedSettings2
- Propiedad AdvancedSettings2 Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Servicios de Escritorio remoto de la interfaz IMsRdpClient2, propiedad AdvancedSettings2
- Propiedad AdvancedSettings2 Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Servicios de Escritorio remoto de la interfaz IMsRdpClient3, propiedad AdvancedSettings2
- Propiedad AdvancedSettings2 Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Servicios de Escritorio remoto de la interfaz IMsRdpClient4, propiedad AdvancedSettings2
- Propiedad AdvancedSettings2 Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad AdvancedSettings2
- Propiedad AdvancedSettings2 Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad AdvancedSettings2
- Propiedad AdvancedSettings2 Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad AdvancedSettings2
- Propiedad AdvancedSettings2 Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad AdvancedSettings2
- Propiedad AdvancedSettings2 Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad AdvancedSettings2
- Propiedad AdvancedSettings2 Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Servicios de Escritorio remoto de la interfaz IMsRdpClient10, propiedad AdvancedSettings2
topic_type:
- apiref
api_name:
- IMsRdpClient.AdvancedSettings2
- IMsRdpClient.get_AdvancedSettings2
- IMsRdpClient2.AdvancedSettings2
- IMsRdpClient2.get_AdvancedSettings2
- IMsRdpClient3.AdvancedSettings2
- IMsRdpClient3.get_AdvancedSettings2
- IMsRdpClient4.AdvancedSettings2
- IMsRdpClient4.get_AdvancedSettings2
- IMsRdpClient5.AdvancedSettings2
- IMsRdpClient5.get_AdvancedSettings2
- IMsRdpClient6.AdvancedSettings2
- IMsRdpClient6.get_AdvancedSettings2
- IMsRdpClient7.AdvancedSettings2
- IMsRdpClient7.get_AdvancedSettings2
- IMsRdpClient8.AdvancedSettings2
- IMsRdpClient8.get_AdvancedSettings2
- IMsRdpClient9.AdvancedSettings2
- IMsRdpClient9.get_AdvancedSettings2
- IMsRdpClient10.AdvancedSettings2
- IMsRdpClient10.get_AdvancedSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683d56d5e9501114b1e60635ca406b4509d2032b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686176"
---
# <a name="imsrdpclientadvancedsettings2-property"></a><span data-ttu-id="41292-125">IMsRdpClient:: AdvancedSettings2 (propiedad)</span><span class="sxs-lookup"><span data-stu-id="41292-125">IMsRdpClient::AdvancedSettings2 property</span></span>

<span data-ttu-id="41292-126">Recupera un puntero a la interfaz [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="41292-126">Retrieves a pointer to the [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) interface.</span></span> <span data-ttu-id="41292-127">La interfaz se puede utilizar para establecer la configuración avanzada del control de cliente.</span><span class="sxs-lookup"><span data-stu-id="41292-127">The interface can be used to set advanced settings for the client control.</span></span>

<span data-ttu-id="41292-128">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="41292-128">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="41292-129">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="41292-129">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings2(
  [out] IMsRdpClientAdvancedSettings **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="41292-130">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="41292-130">Property value</span></span>

<span data-ttu-id="41292-131">Puntero a la interfaz [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="41292-131">Pointer to the [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) interface.</span></span> <span data-ttu-id="41292-132">La interfaz se puede utilizar para establecer la configuración avanzada del control de cliente.</span><span class="sxs-lookup"><span data-stu-id="41292-132">The interface can be used to set advanced settings for the client control.</span></span>

## <a name="error-codes"></a><span data-ttu-id="41292-133">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="41292-133">Error codes</span></span>

<span data-ttu-id="41292-134">Si el método se ejecuta correctamente, se devuelve **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="41292-134">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="41292-135">Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="41292-135">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="41292-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="41292-136">Remarks</span></span>

<span data-ttu-id="41292-137">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="41292-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="41292-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41292-138">Requirements</span></span>



| <span data-ttu-id="41292-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="41292-139">Requirement</span></span> | <span data-ttu-id="41292-140">Value</span><span class="sxs-lookup"><span data-stu-id="41292-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="41292-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41292-141">Minimum supported client</span></span><br/> | <span data-ttu-id="41292-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="41292-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="41292-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41292-143">Minimum supported server</span></span><br/> | <span data-ttu-id="41292-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="41292-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="41292-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="41292-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="41292-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41292-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="41292-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="41292-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41292-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41292-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="41292-149">IID</span><span class="sxs-lookup"><span data-stu-id="41292-149">IID</span></span><br/>                      | <span data-ttu-id="41292-150">IID \_ IMsRdpClient se define como 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="41292-150">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="41292-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="41292-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41292-152">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="41292-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="41292-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="41292-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="41292-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="41292-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="41292-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="41292-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="41292-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="41292-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="41292-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="41292-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="41292-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="41292-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="41292-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="41292-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="41292-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="41292-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="41292-161">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="41292-161">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





