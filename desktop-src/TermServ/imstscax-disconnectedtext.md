---
title: Propiedad DisconnectedText de IMsTscAx
description: Especifica el texto que aparece centrado en el control antes de que se termine una conexión.
ms.assetid: ec7efe7a-8fb9-4c45-8e16-78951365de13
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DisconnectedText
- Propiedad DisconnectedText Servicios de Escritorio remoto, interfaz IMsTscAx
- Servicios de Escritorio remoto de la interfaz IMsTscAx, propiedad DisconnectedText
- Propiedad DisconnectedText Servicios de Escritorio remoto, interfaz IMsRdpClient
- Servicios de Escritorio remoto de la interfaz IMsRdpClient, propiedad DisconnectedText
- Propiedad DisconnectedText Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Servicios de Escritorio remoto de la interfaz IMsRdpClient2, propiedad DisconnectedText
- Propiedad DisconnectedText Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Servicios de Escritorio remoto de la interfaz IMsRdpClient3, propiedad DisconnectedText
- Propiedad DisconnectedText Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Servicios de Escritorio remoto de la interfaz IMsRdpClient4, propiedad DisconnectedText
- Propiedad DisconnectedText Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad DisconnectedText
- Propiedad DisconnectedText Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad DisconnectedText
- Propiedad DisconnectedText Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad DisconnectedText
- Propiedad DisconnectedText Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad DisconnectedText
- Propiedad DisconnectedText Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad DisconnectedText
topic_type:
- apiref
api_name:
- IMsTscAx.DisconnectedText
- IMsTscAx.get_DisconnectedText
- IMsTscAx.put_DisconnectedText
- IMsRdpClient.DisconnectedText
- IMsRdpClient.get_DisconnectedText
- IMsRdpClient.put_DisconnectedText
- IMsRdpClient2.DisconnectedText
- IMsRdpClient2.get_DisconnectedText
- IMsRdpClient2.put_DisconnectedText
- IMsRdpClient3.DisconnectedText
- IMsRdpClient3.get_DisconnectedText
- IMsRdpClient3.put_DisconnectedText
- IMsRdpClient4.DisconnectedText
- IMsRdpClient4.get_DisconnectedText
- IMsRdpClient4.put_DisconnectedText
- IMsRdpClient5.DisconnectedText
- IMsRdpClient5.get_DisconnectedText
- IMsRdpClient5.put_DisconnectedText
- IMsRdpClient6.DisconnectedText
- IMsRdpClient6.get_DisconnectedText
- IMsRdpClient6.put_DisconnectedText
- IMsRdpClient7.DisconnectedText
- IMsRdpClient7.get_DisconnectedText
- IMsRdpClient7.put_DisconnectedText
- IMsRdpClient8.DisconnectedText
- IMsRdpClient8.get_DisconnectedText
- IMsRdpClient8.put_DisconnectedText
- IMsRdpClient9.DisconnectedText
- IMsRdpClient9.get_DisconnectedText
- IMsRdpClient9.put_DisconnectedText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4768e639cbfb1543e06c03f2d9e6566d0adb147e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802744"
---
# <a name="imstscaxdisconnectedtext-property"></a><span data-ttu-id="f02a1-124">IMsTscAx::D propiedad isconnectedText</span><span class="sxs-lookup"><span data-stu-id="f02a1-124">IMsTscAx::DisconnectedText property</span></span>

<span data-ttu-id="f02a1-125">Especifica el texto que aparece centrado en el control antes de que se termine una conexión.</span><span class="sxs-lookup"><span data-stu-id="f02a1-125">Specifies the text that appears centered in the control before a connection is terminated.</span></span>

<span data-ttu-id="f02a1-126">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f02a1-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f02a1-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f02a1-127">Syntax</span></span>


```C++
HRESULT put_DisconnectedText(
  [in]  BSTR newVal
);

HRESULT get_DisconnectedText(
  [out] BSTR *pDisconnectedText
);
```



## <a name="property-value"></a><span data-ttu-id="f02a1-128">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f02a1-128">Property value</span></span>

<span data-ttu-id="f02a1-129">Nuevo texto que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="f02a1-129">The new display text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f02a1-130">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="f02a1-130">Error codes</span></span>

<span data-ttu-id="f02a1-131">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="f02a1-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f02a1-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f02a1-132">Remarks</span></span>

<span data-ttu-id="f02a1-133">El establecimiento de la propiedad **DisconnectedText** es opcional.</span><span class="sxs-lookup"><span data-stu-id="f02a1-133">Setting the **DisconnectedText** property is optional.</span></span> <span data-ttu-id="f02a1-134">Si no se especifica, el control aparece en blanco antes de que se establezca una conexión.</span><span class="sxs-lookup"><span data-stu-id="f02a1-134">If it is not specified the control appears blank before a connection is established.</span></span>

<span data-ttu-id="f02a1-135">Esta propiedad solo se puede establecer si el control no está en estado conectado.</span><span class="sxs-lookup"><span data-stu-id="f02a1-135">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="f02a1-136">El método devuelve **E \_ producirá un error** si se llama después de que se haya conectado el control.</span><span class="sxs-lookup"><span data-stu-id="f02a1-136">The method returns **E\_FAIL** if it is called after the control is connected.</span></span> <span data-ttu-id="f02a1-137">Puede comprobar si el control está conectado respondiendo a los eventos de conexión en [**IMsTscAxEvents**](imstscaxevents-interface.md) o examinando la propiedad [**Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="f02a1-137">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="f02a1-138">Este método asigna la memoria necesaria para el búfer señalado por el parámetro *pDisconnectedText* .</span><span class="sxs-lookup"><span data-stu-id="f02a1-138">This method allocates the memory required for the buffer pointed to by the *pDisconnectedText* parameter.</span></span> <span data-ttu-id="f02a1-139">La llamada a aplicaciones de C/C++ debe liberar la memoria con una llamada a la función [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="f02a1-139">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="f02a1-140">Esto no es necesario para los clientes de scripting y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f02a1-140">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="f02a1-141">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f02a1-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f02a1-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f02a1-142">Requirements</span></span>



| <span data-ttu-id="f02a1-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="f02a1-143">Requirement</span></span> | <span data-ttu-id="f02a1-144">Value</span><span class="sxs-lookup"><span data-stu-id="f02a1-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f02a1-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f02a1-145">Minimum supported client</span></span><br/> | <span data-ttu-id="f02a1-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f02a1-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f02a1-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f02a1-147">Minimum supported server</span></span><br/> | <span data-ttu-id="f02a1-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f02a1-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f02a1-149">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f02a1-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="f02a1-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f02a1-150"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f02a1-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f02a1-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f02a1-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f02a1-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f02a1-153">IID</span><span class="sxs-lookup"><span data-stu-id="f02a1-153">IID</span></span><br/>                      | <span data-ttu-id="f02a1-154">IID \_ IMsTscAx se define como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="f02a1-154">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="f02a1-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="f02a1-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f02a1-156">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="f02a1-156">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="f02a1-157">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="f02a1-157">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="f02a1-158">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="f02a1-158">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="f02a1-159">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="f02a1-159">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="f02a1-160">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="f02a1-160">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="f02a1-161">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="f02a1-161">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="f02a1-162">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="f02a1-162">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="f02a1-163">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="f02a1-163">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="f02a1-164">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="f02a1-164">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="f02a1-165">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="f02a1-165">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

