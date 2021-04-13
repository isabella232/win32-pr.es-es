---
title: Propiedad ExtendedDisconnectReason de IMsRdpClient
description: Contiene información extendida sobre el motivo del control para la desconexión.
ms.assetid: 5729992f-6695-44c0-8cf0-0d6b4cbddb62
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad ExtendedDisconnectReason
- Propiedad ExtendedDisconnectReason Servicios de Escritorio remoto, interfaz IMsRdpClient
- Servicios de Escritorio remoto de la interfaz IMsRdpClient, propiedad ExtendedDisconnectReason
- Propiedad ExtendedDisconnectReason Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Servicios de Escritorio remoto de la interfaz IMsRdpClient2, propiedad ExtendedDisconnectReason
- Propiedad ExtendedDisconnectReason Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Servicios de Escritorio remoto de la interfaz IMsRdpClient3, propiedad ExtendedDisconnectReason
- Propiedad ExtendedDisconnectReason Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Servicios de Escritorio remoto de la interfaz IMsRdpClient4, propiedad ExtendedDisconnectReason
- Propiedad ExtendedDisconnectReason Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad ExtendedDisconnectReason
- Propiedad ExtendedDisconnectReason Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad ExtendedDisconnectReason
- Propiedad ExtendedDisconnectReason Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad ExtendedDisconnectReason
- Propiedad ExtendedDisconnectReason Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad ExtendedDisconnectReason
- Propiedad ExtendedDisconnectReason Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad ExtendedDisconnectReason
- Propiedad ExtendedDisconnectReason Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Servicios de Escritorio remoto de la interfaz IMsRdpClient10, propiedad ExtendedDisconnectReason
topic_type:
- apiref
api_name:
- IMsRdpClient.ExtendedDisconnectReason
- IMsRdpClient.get_ExtendedDisconnectReason
- IMsRdpClient2.ExtendedDisconnectReason
- IMsRdpClient2.get_ExtendedDisconnectReason
- IMsRdpClient3.ExtendedDisconnectReason
- IMsRdpClient3.get_ExtendedDisconnectReason
- IMsRdpClient4.ExtendedDisconnectReason
- IMsRdpClient4.get_ExtendedDisconnectReason
- IMsRdpClient5.ExtendedDisconnectReason
- IMsRdpClient5.get_ExtendedDisconnectReason
- IMsRdpClient6.ExtendedDisconnectReason
- IMsRdpClient6.get_ExtendedDisconnectReason
- IMsRdpClient7.ExtendedDisconnectReason
- IMsRdpClient7.get_ExtendedDisconnectReason
- IMsRdpClient8.ExtendedDisconnectReason
- IMsRdpClient8.get_ExtendedDisconnectReason
- IMsRdpClient9.ExtendedDisconnectReason
- IMsRdpClient9.get_ExtendedDisconnectReason
- IMsRdpClient10.ExtendedDisconnectReason
- IMsRdpClient10.get_ExtendedDisconnectReason
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94c2612b231e24aaec855b6ebd1f9a0498b63c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535224"
---
# <a name="imsrdpclientextendeddisconnectreason-property"></a><span data-ttu-id="53ce7-124">IMsRdpClient:: ExtendedDisconnectReason (propiedad)</span><span class="sxs-lookup"><span data-stu-id="53ce7-124">IMsRdpClient::ExtendedDisconnectReason property</span></span>

<span data-ttu-id="53ce7-125">Contiene información extendida sobre el motivo del control para la desconexión.</span><span class="sxs-lookup"><span data-stu-id="53ce7-125">Contains extended information about the control's reason for disconnection.</span></span>

<span data-ttu-id="53ce7-126">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="53ce7-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="53ce7-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53ce7-127">Syntax</span></span>


```C++
HRESULT get_ExtendedDisconnectReason(
  [out] ExtendedDisconnectReasonCode *pExtendedDisconnectReason
);
```



## <a name="property-value"></a><span data-ttu-id="53ce7-128">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="53ce7-128">Property value</span></span>

<span data-ttu-id="53ce7-129">Puntero al valor de [**ExtendedDisconnectReasonCode**](extendeddisconnectreasoncode.md) que indica el motivo de la desconexión del cliente.</span><span class="sxs-lookup"><span data-stu-id="53ce7-129">Pointer to the [**ExtendedDisconnectReasonCode**](extendeddisconnectreasoncode.md) value indicating the reason for disconnection of the client.</span></span>

## <a name="error-codes"></a><span data-ttu-id="53ce7-130">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="53ce7-130">Error codes</span></span>

<span data-ttu-id="53ce7-131">Si el método se ejecuta correctamente, se devuelve **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="53ce7-131">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="53ce7-132">Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="53ce7-132">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="53ce7-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53ce7-133">Remarks</span></span>

<span data-ttu-id="53ce7-134">Normalmente, se llama a este método en el controlador de eventos [**IMsTscAxEvents:: OnDisconnection**](imstscaxevents-ondisconnected.md) para recuperar información adicional sobre el evento de desconexión.</span><span class="sxs-lookup"><span data-stu-id="53ce7-134">Typically this method is called in the [**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md) event handler to retrieve additional information about the disconnection event.</span></span>

<span data-ttu-id="53ce7-135">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="53ce7-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="53ce7-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53ce7-136">Requirements</span></span>



| <span data-ttu-id="53ce7-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="53ce7-137">Requirement</span></span> | <span data-ttu-id="53ce7-138">Value</span><span class="sxs-lookup"><span data-stu-id="53ce7-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53ce7-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53ce7-139">Minimum supported client</span></span><br/> | <span data-ttu-id="53ce7-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53ce7-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="53ce7-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53ce7-141">Minimum supported server</span></span><br/> | <span data-ttu-id="53ce7-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53ce7-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="53ce7-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="53ce7-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="53ce7-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53ce7-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="53ce7-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="53ce7-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53ce7-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53ce7-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="53ce7-147">IID</span><span class="sxs-lookup"><span data-stu-id="53ce7-147">IID</span></span><br/>                      | <span data-ttu-id="53ce7-148">IID \_ IMsRdpClient se define como 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="53ce7-148">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="53ce7-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="53ce7-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53ce7-150">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="53ce7-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="53ce7-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="53ce7-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="53ce7-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="53ce7-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="53ce7-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="53ce7-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="53ce7-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="53ce7-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="53ce7-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="53ce7-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="53ce7-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="53ce7-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="53ce7-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="53ce7-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="53ce7-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="53ce7-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="53ce7-159">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="53ce7-159">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="53ce7-160">**IMsTscAxEvents:: OnDisconnection**</span><span class="sxs-lookup"><span data-stu-id="53ce7-160">**IMsTscAxEvents::OnDisconnected**</span></span>](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

 





