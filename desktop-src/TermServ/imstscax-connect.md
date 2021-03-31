---
title: Método de conexión de IMsTscAx
description: Inicia una conexión utilizando las propiedades establecidas actualmente en el control.
ms.assetid: 9bcbdc13-6c66-4737-82a4-98329f173743
ms.tgt_platform: multiple
keywords:
- Método Connect Servicios de Escritorio remoto
- Método Connect Servicios de Escritorio remoto, interfaz IMsTscAx
- Interfaz IMsTscAx Servicios de Escritorio remoto, método Connect
- Método Connect Servicios de Escritorio remoto, interfaz IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto, método Connect
- Método Connect Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto, método Connect
- Método Connect Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto, método Connect
- Método Connect Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto, método Connect
- Método Connect Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto, método Connect
- Método Connect Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto, método Connect
- Método Connect Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto, método Connect
- Método Connect Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto, método Connect
- Método Connect Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto, método Connect
topic_type:
- apiref
api_name:
- IMsTscAx.Connect
- IMsRdpClient.Connect
- IMsRdpClient2.Connect
- IMsRdpClient3.Connect
- IMsRdpClient4.Connect
- IMsRdpClient5.Connect
- IMsRdpClient6.Connect
- IMsRdpClient7.Connect
- IMsRdpClient8.Connect
- IMsRdpClient9.Connect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c267b24c3dd27dd875d895674d98e1350f757c82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996137"
---
# <a name="imstscaxconnect-method"></a><span data-ttu-id="e08f8-124">IMsTscAx:: Connect (método)</span><span class="sxs-lookup"><span data-stu-id="e08f8-124">IMsTscAx::Connect method</span></span>

<span data-ttu-id="e08f8-125">Inicia una conexión utilizando las propiedades establecidas actualmente en el control.</span><span class="sxs-lookup"><span data-stu-id="e08f8-125">Initiates a connection using the properties currently set on the control.</span></span>

## <a name="syntax"></a><span data-ttu-id="e08f8-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e08f8-126">Syntax</span></span>


```C++
HRESULT Connect();
```



## <a name="parameters"></a><span data-ttu-id="e08f8-127">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e08f8-127">Parameters</span></span>

<span data-ttu-id="e08f8-128">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e08f8-128">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e08f8-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e08f8-129">Return value</span></span>

<span data-ttu-id="e08f8-130">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="e08f8-130">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e08f8-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e08f8-131">Remarks</span></span>

<span data-ttu-id="e08f8-132">La única propiedad obligatoria es el nombre del servidor.</span><span class="sxs-lookup"><span data-stu-id="e08f8-132">The only required property is the server name.</span></span> <span data-ttu-id="e08f8-133">Consulte la propiedad del [**servidor**](imstscax-server.md) .</span><span class="sxs-lookup"><span data-stu-id="e08f8-133">Refer to the [**Server**](imstscax-server.md) property.</span></span>

<span data-ttu-id="e08f8-134">El control se conecta de forma asincrónica, por lo que un valor devuelto de una llamada de conexión solo indica que la conexión se ha iniciado correctamente, no que se ha completado.</span><span class="sxs-lookup"><span data-stu-id="e08f8-134">The control connects asynchronously, so a return from a Connect call indicates only that the connection has been initiated successfully, not that it has been completed.</span></span> <span data-ttu-id="e08f8-135">Debe responder a los eventos de la interfaz [**IMsTscAxEvents**](imstscaxevents-interface.md) para determinar cuándo se ha conectado correctamente el control (o se ha desconectado).</span><span class="sxs-lookup"><span data-stu-id="e08f8-135">You should respond to events on the [**IMsTscAxEvents**](imstscaxevents-interface.md) interface to determine when the control has successfully connected (or has been disconnected.)</span></span>

<span data-ttu-id="e08f8-136">Este método devuelve **E \_ producirá un error** si se llama mientras el control ya está conectado o en el estado de conexión.</span><span class="sxs-lookup"><span data-stu-id="e08f8-136">This method returns **E\_FAIL** if it is called while the control is already connected or in the connecting state.</span></span>

<span data-ttu-id="e08f8-137">Después de llamar a **Connect** , la mayoría de las propiedades del control ya no se pueden establecer hasta que el control vuelva al estado desconectado.</span><span class="sxs-lookup"><span data-stu-id="e08f8-137">After **Connect** has been called, most of the control properties can no longer be set until the control returns to the disconnected state.</span></span>

<span data-ttu-id="e08f8-138">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e08f8-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e08f8-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e08f8-139">Requirements</span></span>



| <span data-ttu-id="e08f8-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="e08f8-140">Requirement</span></span> | <span data-ttu-id="e08f8-141">Value</span><span class="sxs-lookup"><span data-stu-id="e08f8-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e08f8-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e08f8-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e08f8-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e08f8-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e08f8-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e08f8-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e08f8-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e08f8-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e08f8-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e08f8-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="e08f8-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e08f8-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e08f8-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e08f8-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e08f8-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e08f8-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e08f8-150">IID</span><span class="sxs-lookup"><span data-stu-id="e08f8-150">IID</span></span><br/>                      | <span data-ttu-id="e08f8-151">IID \_ IMsTscAx se define como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="e08f8-151">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="e08f8-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="e08f8-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e08f8-153">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="e08f8-153">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="e08f8-154">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="e08f8-154">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="e08f8-155">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="e08f8-155">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="e08f8-156">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="e08f8-156">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="e08f8-157">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="e08f8-157">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="e08f8-158">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="e08f8-158">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="e08f8-159">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="e08f8-159">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="e08f8-160">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="e08f8-160">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="e08f8-161">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="e08f8-161">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="e08f8-162">**Desconectar**</span><span class="sxs-lookup"><span data-stu-id="e08f8-162">**Disconnect**</span></span>](imstscax-disconnect.md)
</dt> <dt>

[<span data-ttu-id="e08f8-163">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="e08f8-163">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





