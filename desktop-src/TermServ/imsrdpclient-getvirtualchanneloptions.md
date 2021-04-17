---
title: IMsRdpClient GetVirtualChannelOptions, método
description: Recupera las opciones establecidas para un canal virtual.
ms.assetid: d2ec9fb2-c0dc-49f1-a86b-d7abca13a322
ms.tgt_platform: multiple
keywords:
- Método GetVirtualChannelOptions Servicios de Escritorio remoto
- Método GetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto, método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto, método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto, método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto, método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto, método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto, método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto, método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto, método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto, método GetVirtualChannelOptions
- Método GetVirtualChannelOptions Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto, método GetVirtualChannelOptions
topic_type:
- apiref
api_name:
- IMsRdpClient.GetVirtualChannelOptions
- IMsRdpClient2.GetVirtualChannelOptions
- IMsRdpClient3.GetVirtualChannelOptions
- IMsRdpClient4.GetVirtualChannelOptions
- IMsRdpClient5.GetVirtualChannelOptions
- IMsRdpClient6.GetVirtualChannelOptions
- IMsRdpClient7.GetVirtualChannelOptions
- IMsRdpClient8.GetVirtualChannelOptions
- IMsRdpClient9.GetVirtualChannelOptions
- IMsRdpClient10.GetVirtualChannelOptions
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71548002ebc67dae8dc1a49e8144da3de608afb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676934"
---
# <a name="imsrdpclientgetvirtualchanneloptions-method"></a><span data-ttu-id="fac00-124">IMsRdpClient:: GetVirtualChannelOptions (método)</span><span class="sxs-lookup"><span data-stu-id="fac00-124">IMsRdpClient::GetVirtualChannelOptions method</span></span>

<span data-ttu-id="fac00-125">Recupera las opciones establecidas para un canal virtual.</span><span class="sxs-lookup"><span data-stu-id="fac00-125">Retrieves the options set for a virtual channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="fac00-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fac00-126">Syntax</span></span>


```C++
HRESULT GetVirtualChannelOptions(
  [in]  BSTR ChanName,
  [out] LONG *pChanOptions
);
```



## <a name="parameters"></a><span data-ttu-id="fac00-127">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fac00-127">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fac00-128">*ChanName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fac00-128">*ChanName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fac00-129">El nombre de un canal virtual que se especificó en la llamada al método [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) .</span><span class="sxs-lookup"><span data-stu-id="fac00-129">The name of a virtual channel that was specified in the call to [**CreateVirtualChannels**](imstscax-createvirtualchannels.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="fac00-130">*pChanOptions* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="fac00-130">*pChanOptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fac00-131">Las opciones establecidas para el canal virtual especificado por el parámetro *ChanName* .</span><span class="sxs-lookup"><span data-stu-id="fac00-131">The options set for the virtual channel specified by the *ChanName* parameter.</span></span> <span data-ttu-id="fac00-132">Para obtener una descripción de las opciones posibles, consulte [**Channel \_ Def**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).</span><span class="sxs-lookup"><span data-stu-id="fac00-132">For a description of possible options, see [**CHANNEL\_DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fac00-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fac00-133">Return value</span></span>

<span data-ttu-id="fac00-134">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="fac00-134">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="fac00-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fac00-135">Remarks</span></span>

<span data-ttu-id="fac00-136">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="fac00-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fac00-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fac00-137">Requirements</span></span>



| <span data-ttu-id="fac00-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="fac00-138">Requirement</span></span> | <span data-ttu-id="fac00-139">Value</span><span class="sxs-lookup"><span data-stu-id="fac00-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fac00-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fac00-140">Minimum supported client</span></span><br/> | <span data-ttu-id="fac00-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fac00-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fac00-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fac00-142">Minimum supported server</span></span><br/> | <span data-ttu-id="fac00-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fac00-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fac00-144">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fac00-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="fac00-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fac00-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fac00-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fac00-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fac00-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fac00-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fac00-148">IID</span><span class="sxs-lookup"><span data-stu-id="fac00-148">IID</span></span><br/>                      | <span data-ttu-id="fac00-149">IID \_ IMsRdpClient se define como 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="fac00-149">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="fac00-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="fac00-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fac00-151">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="fac00-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="fac00-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="fac00-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="fac00-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="fac00-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="fac00-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="fac00-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="fac00-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="fac00-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="fac00-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="fac00-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="fac00-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="fac00-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="fac00-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="fac00-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="fac00-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="fac00-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="fac00-160">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="fac00-160">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="fac00-161">**DEF. de canal \_**</span><span class="sxs-lookup"><span data-stu-id="fac00-161">**CHANNEL\_DEF**</span></span>](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dt>

[<span data-ttu-id="fac00-162">**CreateVirtualChannels**</span><span class="sxs-lookup"><span data-stu-id="fac00-162">**CreateVirtualChannels**</span></span>](imstscax-createvirtualchannels.md)
</dt> <dt>

[<span data-ttu-id="fac00-163">**SetVirtualChannelOptions**</span><span class="sxs-lookup"><span data-stu-id="fac00-163">**SetVirtualChannelOptions**</span></span>](imsrdpclient-setvirtualchanneloptions.md)
</dt> </dl>

 

 





