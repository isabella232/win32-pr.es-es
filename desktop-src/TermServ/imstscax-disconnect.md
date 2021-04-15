---
title: Método de desconexión IMsTscAx
description: Desconecta la conexión activa.
ms.assetid: 9fcffd45-b293-4650-be8f-1b0d01d592a2
ms.tgt_platform: multiple
keywords:
- Desconectar método Servicios de Escritorio remoto
- Método Disconnect Servicios de Escritorio remoto, interfaz IMsTscAx
- Interfaz IMsTscAx Servicios de Escritorio remoto, método Disconnect
- Método Disconnect Servicios de Escritorio remoto, interfaz IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto, método Disconnect
- Método Disconnect Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto, método Disconnect
- Método Disconnect Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto, método Disconnect
- Método Disconnect Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto, método Disconnect
- Método Disconnect Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto, método Disconnect
- Método Disconnect Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto, método Disconnect
- Método Disconnect Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto, método Disconnect
- Método Disconnect Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto, método Disconnect
- Método Disconnect Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto, método Disconnect
topic_type:
- apiref
api_name:
- IMsTscAx.Disconnect
- IMsRdpClient.Disconnect
- IMsRdpClient2.Disconnect
- IMsRdpClient3.Disconnect
- IMsRdpClient4.Disconnect
- IMsRdpClient5.Disconnect
- IMsRdpClient6.Disconnect
- IMsRdpClient7.Disconnect
- IMsRdpClient8.Disconnect
- IMsRdpClient9.Disconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d4f1545a8244209c0b4fa8267fcc8ce2a41e090
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534564"
---
# <a name="imstscaxdisconnect-method"></a><span data-ttu-id="205ed-124">IMsTscAx::D método Ulta</span><span class="sxs-lookup"><span data-stu-id="205ed-124">IMsTscAx::Disconnect method</span></span>

<span data-ttu-id="205ed-125">Desconecta la conexión activa.</span><span class="sxs-lookup"><span data-stu-id="205ed-125">Disconnects the active connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="205ed-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="205ed-126">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="205ed-127">Parámetros</span><span class="sxs-lookup"><span data-stu-id="205ed-127">Parameters</span></span>

<span data-ttu-id="205ed-128">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="205ed-128">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="205ed-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="205ed-129">Return value</span></span>

<span data-ttu-id="205ed-130">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="205ed-130">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="205ed-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="205ed-131">Remarks</span></span>

<span data-ttu-id="205ed-132">Este método devuelve un valor de error si se llama cuando el control no está conectado.</span><span class="sxs-lookup"><span data-stu-id="205ed-132">This method returns a failure error value if it is called when the control is not connected.</span></span>

<span data-ttu-id="205ed-133">También es posible desconectar el control cerrando la ventana principal.</span><span class="sxs-lookup"><span data-stu-id="205ed-133">It is also possible to disconnect the control by closing its main window.</span></span> <span data-ttu-id="205ed-134">Por ejemplo, si el control está hospedado en una página web, no es necesario llamar a este método antes de que se abandone la página; el cierre del control desencadena una desconexión.</span><span class="sxs-lookup"><span data-stu-id="205ed-134">For example, if the control is hosted in a webpage, it is not necessary to call this method before leaving the page; the closing of the control triggers a disconnection.</span></span>

<span data-ttu-id="205ed-135">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="205ed-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="205ed-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="205ed-136">Requirements</span></span>



| <span data-ttu-id="205ed-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="205ed-137">Requirement</span></span> | <span data-ttu-id="205ed-138">Value</span><span class="sxs-lookup"><span data-stu-id="205ed-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="205ed-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="205ed-139">Minimum supported client</span></span><br/> | <span data-ttu-id="205ed-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="205ed-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="205ed-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="205ed-141">Minimum supported server</span></span><br/> | <span data-ttu-id="205ed-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="205ed-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="205ed-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="205ed-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="205ed-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="205ed-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="205ed-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="205ed-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="205ed-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="205ed-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="205ed-147">IID</span><span class="sxs-lookup"><span data-stu-id="205ed-147">IID</span></span><br/>                      | <span data-ttu-id="205ed-148">IID \_ IMsTscAx se define como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="205ed-148">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="205ed-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="205ed-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="205ed-150">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="205ed-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="205ed-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="205ed-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="205ed-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="205ed-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="205ed-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="205ed-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="205ed-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="205ed-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="205ed-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="205ed-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="205ed-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="205ed-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="205ed-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="205ed-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="205ed-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="205ed-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="205ed-159">**Conectar**</span><span class="sxs-lookup"><span data-stu-id="205ed-159">**Connect**</span></span>](imstscax-connect.md)
</dt> <dt>

[<span data-ttu-id="205ed-160">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="205ed-160">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





