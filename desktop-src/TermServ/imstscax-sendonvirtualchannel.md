---
title: IMsTscAx SendOnVirtualChannel, método
description: Envía datos al servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto) a través de un canal virtual que se creó anteriormente mediante el método CreateVirtualChannels.
ms.assetid: 795ef508-bdf7-4897-84b1-931615262293
ms.tgt_platform: multiple
keywords:
- Método SendOnVirtualChannel Servicios de Escritorio remoto
- Método SendOnVirtualChannel Servicios de Escritorio remoto, interfaz IMsTscAx
- Interfaz IMsTscAx Servicios de Escritorio remoto, método SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto, interfaz IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto, método SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto, método SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto, método SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto, método SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto, método SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto, método SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto, método SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto, método SendOnVirtualChannel
- Método SendOnVirtualChannel Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto, método SendOnVirtualChannel
topic_type:
- apiref
api_name:
- IMsTscAx.SendOnVirtualChannel
- IMsRdpClient.SendOnVirtualChannel
- IMsRdpClient2.SendOnVirtualChannel
- IMsRdpClient3.SendOnVirtualChannel
- IMsRdpClient4.SendOnVirtualChannel
- IMsRdpClient5.SendOnVirtualChannel
- IMsRdpClient6.SendOnVirtualChannel
- IMsRdpClient7.SendOnVirtualChannel
- IMsRdpClient8.SendOnVirtualChannel
- IMsRdpClient9.SendOnVirtualChannel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1371ae17978601a3194f755dd364d9227b8fc28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489503"
---
# <a name="imstscaxsendonvirtualchannel-method"></a><span data-ttu-id="aa725-124">IMsTscAx:: SendOnVirtualChannel (método)</span><span class="sxs-lookup"><span data-stu-id="aa725-124">IMsTscAx::SendOnVirtualChannel method</span></span>

<span data-ttu-id="aa725-125">Envía datos al servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto) a través de un canal virtual que se creó anteriormente mediante el método [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) .</span><span class="sxs-lookup"><span data-stu-id="aa725-125">Sends data to the Remote Desktop Session Host (RD Session Host) server over a virtual channel that was created previously by using the [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa725-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aa725-126">Syntax</span></span>


```C++
HRESULT SendOnVirtualChannel(
  [in] BSTR ChanName,
  [in] BSTR ChanData
);
```



## <a name="parameters"></a><span data-ttu-id="aa725-127">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aa725-127">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa725-128">*ChanName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aa725-128">*ChanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa725-129">Nombre del canal virtual que se especificó en la llamada a [**CreateVirtualChannels**](imstscax-createvirtualchannels.md).</span><span class="sxs-lookup"><span data-stu-id="aa725-129">The virtual channel name that was specified in the call to [**CreateVirtualChannels**](imstscax-createvirtualchannels.md).</span></span>

</dd> <dt>

<span data-ttu-id="aa725-130">*ChanData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aa725-130">*ChanData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa725-131">Los datos que se van a enviar a través del canal virtual, en forma de **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="aa725-131">The data to send over the virtual channel, in **BSTR** form.</span></span> <span data-ttu-id="aa725-132">No hay ninguna restricción de que estos datos deban ser cadenas terminadas en NULL.</span><span class="sxs-lookup"><span data-stu-id="aa725-132">There is no restriction that this data must be null-terminated strings.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa725-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aa725-133">Return value</span></span>

<span data-ttu-id="aa725-134">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="aa725-134">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa725-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa725-135">Remarks</span></span>

<span data-ttu-id="aa725-136">Consulte [registro de cliente de canal virtual](virtual-channel-client-registration.md) para obtener información sobre las restricciones de nomenclatura de canal virtual.</span><span class="sxs-lookup"><span data-stu-id="aa725-136">Refer to [Virtual Channel Client Registration](virtual-channel-client-registration.md) for information about virtual channel naming restrictions.</span></span>

<span data-ttu-id="aa725-137">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="aa725-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aa725-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa725-138">Requirements</span></span>



| <span data-ttu-id="aa725-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa725-139">Requirement</span></span> | <span data-ttu-id="aa725-140">Value</span><span class="sxs-lookup"><span data-stu-id="aa725-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa725-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa725-141">Minimum supported client</span></span><br/> | <span data-ttu-id="aa725-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa725-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="aa725-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aa725-143">Minimum supported server</span></span><br/> | <span data-ttu-id="aa725-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa725-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="aa725-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="aa725-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="aa725-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa725-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="aa725-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aa725-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa725-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa725-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="aa725-149">IID</span><span class="sxs-lookup"><span data-stu-id="aa725-149">IID</span></span><br/>                      | <span data-ttu-id="aa725-150">IID \_ IMsTscAx se define como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="aa725-150">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="aa725-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="aa725-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa725-152">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="aa725-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="aa725-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="aa725-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="aa725-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="aa725-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="aa725-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="aa725-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="aa725-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="aa725-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="aa725-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="aa725-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="aa725-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="aa725-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="aa725-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="aa725-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="aa725-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="aa725-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="aa725-161">**CreateVirtualChannels**</span><span class="sxs-lookup"><span data-stu-id="aa725-161">**CreateVirtualChannels**</span></span>](imstscax-createvirtualchannels.md)
</dt> <dt>

[<span data-ttu-id="aa725-162">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="aa725-162">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





