---
title: Propiedad conectada a IMsTscAx (Tsvirtualchannels. h)
description: Recupera el estado de conexión del control actual.
ms.assetid: f6f65ef6-d321-4362-b192-1ea5ffd2b712
ms.tgt_platform: multiple
keywords:
- Propiedad conectada Servicios de Escritorio remoto
- Propiedad conectada Servicios de Escritorio remoto, interfaz IMsTscAx
- Servicios de Escritorio remoto de la interfaz IMsTscAx, propiedad conectada
- Propiedad conectada Servicios de Escritorio remoto, interfaz IMsRdpClient
- Servicios de Escritorio remoto de la interfaz IMsRdpClient, propiedad conectada
- Propiedad conectada Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Servicios de Escritorio remoto de la interfaz IMsRdpClient2, propiedad conectada
- Propiedad conectada Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Servicios de Escritorio remoto de la interfaz IMsRdpClient3, propiedad conectada
- Propiedad conectada Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Servicios de Escritorio remoto de la interfaz IMsRdpClient4, propiedad conectada
- Propiedad conectada Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad conectada
- Propiedad conectada Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad conectada
- Propiedad conectada Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad conectada
- Propiedad conectada Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad conectada
- Propiedad conectada Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad conectada
topic_type:
- apiref
api_name:
- IMsTscAx.Connected
- IMsTscAx.get_Connected
- IMsRdpClient.Connected
- IMsRdpClient.get_Connected
- IMsRdpClient2.Connected
- IMsRdpClient2.get_Connected
- IMsRdpClient3.Connected
- IMsRdpClient3.get_Connected
- IMsRdpClient4.Connected
- IMsRdpClient4.get_Connected
- IMsRdpClient5.Connected
- IMsRdpClient5.get_Connected
- IMsRdpClient6.Connected
- IMsRdpClient6.get_Connected
- IMsRdpClient7.Connected
- IMsRdpClient7.get_Connected
- IMsRdpClient8.Connected
- IMsRdpClient8.get_Connected
- IMsRdpClient9.Connected
- IMsRdpClient9.get_Connected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 883ba670ab9a6b5d4e4a065c35f263734929ba02
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686238"
---
# <a name="imstscaxconnected-property"></a><span data-ttu-id="5a573-124">IMsTscAx:: Connected (propiedad)</span><span class="sxs-lookup"><span data-stu-id="5a573-124">IMsTscAx::Connected property</span></span>

<span data-ttu-id="5a573-125">Recupera el estado de conexión del control actual.</span><span class="sxs-lookup"><span data-stu-id="5a573-125">Retrieves the connection state of the current control.</span></span>

<span data-ttu-id="5a573-126">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5a573-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a573-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a573-127">Syntax</span></span>


```C++
HRESULT get_Connected(
  [out] short *pIsConnected
);
```



## <a name="property-value"></a><span data-ttu-id="5a573-128">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5a573-128">Property value</span></span>

<span data-ttu-id="5a573-129">Indica el estado de conexión del control.</span><span class="sxs-lookup"><span data-stu-id="5a573-129">Indicates the connection state of the control.</span></span> <span data-ttu-id="5a573-130">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5a573-130">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="5a573-131">0</span><span class="sxs-lookup"><span data-stu-id="5a573-131">0</span></span>
</dt> <dd>

<span data-ttu-id="5a573-132">El control no está conectado.</span><span class="sxs-lookup"><span data-stu-id="5a573-132">The control is not connected.</span></span>

</dd> <dt>

<span data-ttu-id="5a573-133">1</span><span class="sxs-lookup"><span data-stu-id="5a573-133">1</span></span>
</dt> <dd>

<span data-ttu-id="5a573-134">El control está conectado.</span><span class="sxs-lookup"><span data-stu-id="5a573-134">The control is connected.</span></span>

</dd> <dt>

<span data-ttu-id="5a573-135">2</span><span class="sxs-lookup"><span data-stu-id="5a573-135">2</span></span>
</dt> <dd>

<span data-ttu-id="5a573-136">El control está estableciendo una conexión.</span><span class="sxs-lookup"><span data-stu-id="5a573-136">The control is establishing a connection.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="5a573-137">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="5a573-137">Error codes</span></span>

<span data-ttu-id="5a573-138">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="5a573-138">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a573-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a573-139">Remarks</span></span>

<span data-ttu-id="5a573-140">La mejor manera de determinar el estado de conexión del control es responder a los eventos de conexión en [**IMsTscAxEvents**](imstscaxevents-interface.md).</span><span class="sxs-lookup"><span data-stu-id="5a573-140">The preferred way to determine the control's connection state is to respond to the connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md).</span></span>

<span data-ttu-id="5a573-141">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="5a573-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a573-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a573-142">Requirements</span></span>



| <span data-ttu-id="5a573-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a573-143">Requirement</span></span> | <span data-ttu-id="5a573-144">Value</span><span class="sxs-lookup"><span data-stu-id="5a573-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a573-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a573-145">Minimum supported client</span></span><br/> | <span data-ttu-id="5a573-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5a573-146">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="5a573-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a573-147">Minimum supported server</span></span><br/> | <span data-ttu-id="5a573-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5a573-148">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="5a573-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5a573-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a573-150"><dt>Tsvirtualchannels. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a573-150"><dt>Tsvirtualchannels.h</dt></span></span> </dl> |
| <span data-ttu-id="5a573-151">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5a573-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="5a573-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a573-152"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="5a573-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5a573-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a573-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a573-154"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="5a573-155">IID</span><span class="sxs-lookup"><span data-stu-id="5a573-155">IID</span></span><br/>                      | <span data-ttu-id="5a573-156">IID \_ IMsTscAx se define como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="5a573-156">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="5a573-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a573-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a573-158">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="5a573-158">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="5a573-159">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="5a573-159">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="5a573-160">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="5a573-160">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="5a573-161">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="5a573-161">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="5a573-162">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="5a573-162">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="5a573-163">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="5a573-163">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="5a573-164">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="5a573-164">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="5a573-165">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="5a573-165">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="5a573-166">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="5a573-166">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="5a573-167">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="5a573-167">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





