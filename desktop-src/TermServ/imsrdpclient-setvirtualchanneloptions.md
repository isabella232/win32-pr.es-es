---
title: IMsRdpClient SetVirtualChannelOptions, método
description: Establece las opciones de canal virtual para el control ActiveX Escritorio remoto.
ms.assetid: c74c3917-5766-4d5b-8458-b051eb91cb28
ms.tgt_platform: multiple
keywords:
- Método SetVirtualChannelOptions Servicios de Escritorio remoto
- Método SetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto, método SetVirtualChannelOptions
- Método SetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto, método SetVirtualChannelOptions
topic_type:
- apiref
api_name:
- IMsRdpClient.SetVirtualChannelOptions
- IMsRdpClient2.SetVirtualChannelOptions
- IMsRdpClient3.SetVirtualChannelOptions
- IMsRdpClient4.SetVirtualChannelOptions
- IMsRdpClient5.SetVirtualChannelOptions
- IMsRdpClient6.SetVirtualChannelOptions
- IMsRdpClient7.SetVirtualChannelOptions
- IMsRdpClient8.SetVirtualChannelOptions
- IMsRdpClient9.SetVirtualChannelOptions
- IMsRdpClient10.SetVirtualChannelOptions
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10e727fd3486b9d1b31fb3a421ea6ff268949790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422085"
---
# <a name="imsrdpclientsetvirtualchanneloptions-method"></a><span data-ttu-id="3ecaf-124">IMsRdpClient:: SetVirtualChannelOptions (método)</span><span class="sxs-lookup"><span data-stu-id="3ecaf-124">IMsRdpClient::SetVirtualChannelOptions method</span></span>

<span data-ttu-id="3ecaf-125">Establece las opciones de canal virtual para el control ActiveX Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="3ecaf-125">Sets the virtual channel options for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="3ecaf-126">Llame a este método después de llamar al método [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) , pero antes de establecer una conexión con el método [**Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="3ecaf-126">Call this method after calling the [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method, but before establishing a connection with the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="3ecaf-127">Este método establece opciones adicionales en los canales virtuales creados con **CreateVirtualChannels**.</span><span class="sxs-lookup"><span data-stu-id="3ecaf-127">This method sets additional options on virtual channels that have been created with **CreateVirtualChannels**.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ecaf-128">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ecaf-128">Syntax</span></span>


```C++
HRESULT SetVirtualChannelOptions(
  [in] BSTR ChanName,
  [in] LONG chanOptions
);
```



## <a name="parameters"></a><span data-ttu-id="3ecaf-129">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3ecaf-129">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ecaf-130">*ChanName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3ecaf-130">*ChanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ecaf-131">Nombre del canal virtual que se especificó en la llamada al método [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) .</span><span class="sxs-lookup"><span data-stu-id="3ecaf-131">The name of the virtual channel that was specified in the call to the [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="3ecaf-132">*chanOptions* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3ecaf-132">*chanOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ecaf-133">Opciones que se van a establecer para el canal virtual especificado por el parámetro *ChanName* .</span><span class="sxs-lookup"><span data-stu-id="3ecaf-133">The options to set for the virtual channel specified by the *ChanName* parameter.</span></span> <span data-ttu-id="3ecaf-134">Para obtener una descripción de las opciones posibles, consulte [**Channel \_ Def**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).</span><span class="sxs-lookup"><span data-stu-id="3ecaf-134">For a description of possible options, see [**CHANNEL\_DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).</span></span> <span data-ttu-id="3ecaf-135">Para obtener más información, vea la sección Comentarios que se muestra más adelante.</span><span class="sxs-lookup"><span data-stu-id="3ecaf-135">For more information, see the following Remarks section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ecaf-136">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3ecaf-136">Return value</span></span>

<span data-ttu-id="3ecaf-137">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="3ecaf-137">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ecaf-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3ecaf-138">Remarks</span></span>

<span data-ttu-id="3ecaf-139">Un ejemplo del uso de este método sería declarar el canal como control remoto persistente mediante la configuración de **la \_ opción de canal \_ \_ \_ persistencia persistente de control remoto** .</span><span class="sxs-lookup"><span data-stu-id="3ecaf-139">An example of using this method would be to declare the channel as remote control persistent by setting the **CHANNEL\_OPTION\_REMOTE\_CONTROL\_PERSISTENT** flag.</span></span> <span data-ttu-id="3ecaf-140">Esto significa que el canal no se cerrará cuando un control remoto se conecte o desconecte de la sesión conectada al cliente.</span><span class="sxs-lookup"><span data-stu-id="3ecaf-140">This means that the channel would not be closed when a remote control connects to or disconnects from the session connected to the client.</span></span> <span data-ttu-id="3ecaf-141">Para obtener más información, consulte [Remote control remoto canales virtuales persistentes](remote-control-persistent-virtual-channels.md).</span><span class="sxs-lookup"><span data-stu-id="3ecaf-141">For more information, see [Remote Control Persistent Virtual Channels](remote-control-persistent-virtual-channels.md).</span></span>

<span data-ttu-id="3ecaf-142">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="3ecaf-142">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ecaf-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ecaf-143">Requirements</span></span>



| <span data-ttu-id="3ecaf-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ecaf-144">Requirement</span></span> | <span data-ttu-id="3ecaf-145">Value</span><span class="sxs-lookup"><span data-stu-id="3ecaf-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ecaf-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ecaf-146">Minimum supported client</span></span><br/> | <span data-ttu-id="3ecaf-147">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ecaf-147">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3ecaf-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ecaf-148">Minimum supported server</span></span><br/> | <span data-ttu-id="3ecaf-149">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ecaf-149">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3ecaf-150">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3ecaf-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="3ecaf-151"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ecaf-151"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3ecaf-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3ecaf-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ecaf-153"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ecaf-153"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3ecaf-154">IID</span><span class="sxs-lookup"><span data-stu-id="3ecaf-154">IID</span></span><br/>                      | <span data-ttu-id="3ecaf-155">IID \_ IMsRdpClient se define como 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="3ecaf-155">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="3ecaf-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ecaf-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ecaf-157">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="3ecaf-157">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="3ecaf-158">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="3ecaf-158">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="3ecaf-159">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="3ecaf-159">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="3ecaf-160">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="3ecaf-160">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="3ecaf-161">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="3ecaf-161">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="3ecaf-162">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="3ecaf-162">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="3ecaf-163">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="3ecaf-163">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="3ecaf-164">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="3ecaf-164">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="3ecaf-165">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="3ecaf-165">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="3ecaf-166">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="3ecaf-166">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="3ecaf-167">**DEF. de canal \_**</span><span class="sxs-lookup"><span data-stu-id="3ecaf-167">**CHANNEL\_DEF**</span></span>](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[<span data-ttu-id="3ecaf-168">**CreateVirtualChannels**</span><span class="sxs-lookup"><span data-stu-id="3ecaf-168">**CreateVirtualChannels**</span></span>](imstscax-createvirtualchannels.md)
</dt> <dt>

[<span data-ttu-id="3ecaf-169">**GetVirtualChannelOptions**</span><span class="sxs-lookup"><span data-stu-id="3ecaf-169">**GetVirtualChannelOptions**</span></span>](imsrdpclient-getvirtualchanneloptions.md)
</dt> </dl>

 

 





