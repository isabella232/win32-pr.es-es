---
title: IMsTscAx CreateVirtualChannels, método
description: Crea un objeto de canal virtual del lado cliente para cada nombre de canal virtual especificado.
ms.assetid: 3afd2f1c-abd5-4f85-93fb-6d1173f09b07
ms.tgt_platform: multiple
keywords:
- Método CreateVirtualChannels Servicios de Escritorio remoto
- Método CreateVirtualChannels Servicios de Escritorio remoto, interfaz IMsTscAx
- Interfaz IMsTscAx Servicios de Escritorio remoto, método CreateVirtualChannels
- Método CreateVirtualChannels Servicios de Escritorio remoto, interfaz IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto, método CreateVirtualChannels
- Método CreateVirtualChannels Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto, método CreateVirtualChannels
- Método CreateVirtualChannels Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto, método CreateVirtualChannels
- Método CreateVirtualChannels Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto, método CreateVirtualChannels
- Método CreateVirtualChannels Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto, método CreateVirtualChannels
- Método CreateVirtualChannels Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto, método CreateVirtualChannels
- Método CreateVirtualChannels Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto, método CreateVirtualChannels
- Método CreateVirtualChannels Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto, método CreateVirtualChannels
- Método CreateVirtualChannels Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto, método CreateVirtualChannels
topic_type:
- apiref
api_name:
- IMsTscAx.CreateVirtualChannels
- IMsRdpClient.CreateVirtualChannels
- IMsRdpClient2.CreateVirtualChannels
- IMsRdpClient3.CreateVirtualChannels
- IMsRdpClient4.CreateVirtualChannels
- IMsRdpClient5.CreateVirtualChannels
- IMsRdpClient6.CreateVirtualChannels
- IMsRdpClient7.CreateVirtualChannels
- IMsRdpClient8.CreateVirtualChannels
- IMsRdpClient9.CreateVirtualChannels
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d59c185763ddd3685e5e566f88e26a6aa6211b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491626"
---
# <a name="imstscaxcreatevirtualchannels-method"></a><span data-ttu-id="11f69-124">IMsTscAx:: CreateVirtualChannels (método)</span><span class="sxs-lookup"><span data-stu-id="11f69-124">IMsTscAx::CreateVirtualChannels method</span></span>

<span data-ttu-id="11f69-125">Crea un objeto de canal virtual del lado cliente para cada nombre de canal virtual especificado.</span><span class="sxs-lookup"><span data-stu-id="11f69-125">Creates a client-side virtual channel object for each specified virtual channel name.</span></span>

## <a name="syntax"></a><span data-ttu-id="11f69-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="11f69-126">Syntax</span></span>


```C++
HRESULT CreateVirtualChannels(
  [in] BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="11f69-127">Parámetros</span><span class="sxs-lookup"><span data-stu-id="11f69-127">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11f69-128">*newVal* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="11f69-128">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11f69-129">Lista separada por comas de nombres de canal virtual válidos.</span><span class="sxs-lookup"><span data-stu-id="11f69-129">A comma-separated list of valid virtual channel names.</span></span> <span data-ttu-id="11f69-130">La longitud de cada nombre en esta lista puede ser un mínimo de uno y un máximo de siete caracteres alfabéticos.</span><span class="sxs-lookup"><span data-stu-id="11f69-130">The length of each name in this list can be a minimum of one and a maximum of seven alphabetical characters.</span></span> <span data-ttu-id="11f69-131">La longitud de la cadena completa puede ser un mínimo de 1 y un máximo de 300 caracteres alfabéticos.</span><span class="sxs-lookup"><span data-stu-id="11f69-131">The length of the entire string can be a minimum of one and a maximum of 300 alphabetical characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11f69-132">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="11f69-132">Return value</span></span>

<span data-ttu-id="11f69-133">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="11f69-133">Returns **S\_OK** if successful.</span></span> <span data-ttu-id="11f69-134">Devuelve **E \_ INVALIDARG** si el parámetro que se pasa no cumple los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="11f69-134">Returns **E\_INVALIDARG** if the parameter that is passed does not meet the criteria that is specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="11f69-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="11f69-135">Remarks</span></span>

<span data-ttu-id="11f69-136">Llame a este método antes de llamar al método [**Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="11f69-136">Call this method before calling the [**Connect**](imstscax-connect.md) method.</span></span>

<span data-ttu-id="11f69-137">Consulte [registro de cliente de canal virtual](virtual-channel-client-registration.md) para obtener información sobre las restricciones de nomenclatura de canal virtual.</span><span class="sxs-lookup"><span data-stu-id="11f69-137">Refer to [Virtual Channel Client Registration](virtual-channel-client-registration.md) for information about virtual channel naming restrictions.</span></span>

<span data-ttu-id="11f69-138">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="11f69-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="11f69-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11f69-139">Requirements</span></span>



| <span data-ttu-id="11f69-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="11f69-140">Requirement</span></span> | <span data-ttu-id="11f69-141">Value</span><span class="sxs-lookup"><span data-stu-id="11f69-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11f69-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11f69-142">Minimum supported client</span></span><br/> | <span data-ttu-id="11f69-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="11f69-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="11f69-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11f69-144">Minimum supported server</span></span><br/> | <span data-ttu-id="11f69-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="11f69-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="11f69-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="11f69-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="11f69-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11f69-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="11f69-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="11f69-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11f69-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11f69-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="11f69-150">IID</span><span class="sxs-lookup"><span data-stu-id="11f69-150">IID</span></span><br/>                      | <span data-ttu-id="11f69-151">IID \_ IMsTscAx se define como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="11f69-151">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="11f69-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="11f69-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11f69-153">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="11f69-153">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="11f69-154">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="11f69-154">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="11f69-155">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="11f69-155">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="11f69-156">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="11f69-156">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="11f69-157">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="11f69-157">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="11f69-158">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="11f69-158">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="11f69-159">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="11f69-159">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="11f69-160">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="11f69-160">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="11f69-161">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="11f69-161">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="11f69-162">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="11f69-162">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





