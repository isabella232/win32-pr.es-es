---
title: Propiedad ConnectingText de IMsTscAx
description: Especifica el texto que aparece centrado en el control mientras el control se está conectando.
ms.assetid: 9bc82074-988f-491b-80e3-00c3f7ba437a
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad ConnectingText
- Propiedad ConnectingText Servicios de Escritorio remoto, interfaz IMsTscAx
- Servicios de Escritorio remoto de la interfaz IMsTscAx, propiedad ConnectingText
- Propiedad ConnectingText Servicios de Escritorio remoto, interfaz IMsRdpClient
- Servicios de Escritorio remoto de la interfaz IMsRdpClient, propiedad ConnectingText
- Propiedad ConnectingText Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Servicios de Escritorio remoto de la interfaz IMsRdpClient2, propiedad ConnectingText
- Propiedad ConnectingText Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Servicios de Escritorio remoto de la interfaz IMsRdpClient3, propiedad ConnectingText
- Propiedad ConnectingText Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Servicios de Escritorio remoto de la interfaz IMsRdpClient4, propiedad ConnectingText
- Propiedad ConnectingText Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad ConnectingText
- Propiedad ConnectingText Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad ConnectingText
- Propiedad ConnectingText Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad ConnectingText
- Propiedad ConnectingText Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad ConnectingText
- Propiedad ConnectingText Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad ConnectingText
topic_type:
- apiref
api_name:
- IMsTscAx.ConnectingText
- IMsTscAx.get_ConnectingText
- IMsTscAx.put_ConnectingText
- IMsRdpClient.ConnectingText
- IMsRdpClient.get_ConnectingText
- IMsRdpClient.put_ConnectingText
- IMsRdpClient2.ConnectingText
- IMsRdpClient2.get_ConnectingText
- IMsRdpClient2.put_ConnectingText
- IMsRdpClient3.ConnectingText
- IMsRdpClient3.get_ConnectingText
- IMsRdpClient3.put_ConnectingText
- IMsRdpClient4.ConnectingText
- IMsRdpClient4.get_ConnectingText
- IMsRdpClient4.put_ConnectingText
- IMsRdpClient5.ConnectingText
- IMsRdpClient5.get_ConnectingText
- IMsRdpClient5.put_ConnectingText
- IMsRdpClient6.ConnectingText
- IMsRdpClient6.get_ConnectingText
- IMsRdpClient6.put_ConnectingText
- IMsRdpClient7.ConnectingText
- IMsRdpClient7.get_ConnectingText
- IMsRdpClient7.put_ConnectingText
- IMsRdpClient8.ConnectingText
- IMsRdpClient8.get_ConnectingText
- IMsRdpClient8.put_ConnectingText
- IMsRdpClient9.ConnectingText
- IMsRdpClient9.get_ConnectingText
- IMsRdpClient9.put_ConnectingText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433da7d159f1fe5bf44114a0b76ed9b4d807046f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422474"
---
# <a name="imstscaxconnectingtext-property"></a><span data-ttu-id="0a4ff-124">IMsTscAx:: ConnectingText (propiedad)</span><span class="sxs-lookup"><span data-stu-id="0a4ff-124">IMsTscAx::ConnectingText property</span></span>

<span data-ttu-id="0a4ff-125">Especifica el texto que aparece centrado en el control mientras el control se está conectando.</span><span class="sxs-lookup"><span data-stu-id="0a4ff-125">Specifies the text that appears centered in the control while the control is connecting.</span></span>

<span data-ttu-id="0a4ff-126">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="0a4ff-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a4ff-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a4ff-127">Syntax</span></span>


```C++
HRESULT put_ConnectingText(
  [in]  BSTR newVal
);

HRESULT get_ConnectingText(
  [out] BSTR *pConnectingText
);
```



## <a name="property-value"></a><span data-ttu-id="0a4ff-128">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0a4ff-128">Property value</span></span>

<span data-ttu-id="0a4ff-129">Nuevo texto que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="0a4ff-129">The new display text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0a4ff-130">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="0a4ff-130">Error codes</span></span>

<span data-ttu-id="0a4ff-131">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="0a4ff-131">Return **S\_OK** if successful.</span></span>

<span data-ttu-id="0a4ff-132">Devuelve un **valor HRESULT** distinto de cero si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="0a4ff-132">Return a nonzero **HRESULT** if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a4ff-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0a4ff-133">Remarks</span></span>

<span data-ttu-id="0a4ff-134">Un ejemplo de texto de conexión es "conectando con el servidor...".</span><span class="sxs-lookup"><span data-stu-id="0a4ff-134">An example of connection text is "Connecting to server ...".</span></span>

<span data-ttu-id="0a4ff-135">El establecimiento de la propiedad **ConnectingText** es opcional.</span><span class="sxs-lookup"><span data-stu-id="0a4ff-135">Setting the **ConnectingText** property is optional.</span></span> <span data-ttu-id="0a4ff-136">Si no se establece, el control aparece en blanco antes de que se establezca una conexión.</span><span class="sxs-lookup"><span data-stu-id="0a4ff-136">If it is not set, the control appears blank before a connection is established.</span></span>

<span data-ttu-id="0a4ff-137">Esta propiedad solo se puede establecer si el control no está en estado conectado.</span><span class="sxs-lookup"><span data-stu-id="0a4ff-137">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="0a4ff-138">Devuelve **E \_ produce un error** si se llama cuando el control está conectado.</span><span class="sxs-lookup"><span data-stu-id="0a4ff-138">It returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="0a4ff-139">Puede comprobar si el control está conectado respondiendo a los eventos de conexión en [**IMsTscAxEvents**](imstscaxevents-interface.md) o examinando la propiedad [**Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="0a4ff-139">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="0a4ff-140">El método de propiedad **Get \_ ConnectingText** asigna la memoria necesaria para el búfer señalado por el parámetro *pConnectingText* .</span><span class="sxs-lookup"><span data-stu-id="0a4ff-140">The **get\_ConnectingText** property method allocates the memory required for the buffer pointed to by the *pConnectingText* parameter.</span></span> <span data-ttu-id="0a4ff-141">La llamada a aplicaciones de C/C++ debe liberar la memoria con una llamada a la función [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="0a4ff-141">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="0a4ff-142">Esto no es necesario para los clientes de scripting y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0a4ff-142">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="0a4ff-143">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0a4ff-143">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a4ff-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a4ff-144">Requirements</span></span>



| <span data-ttu-id="0a4ff-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a4ff-145">Requirement</span></span> | <span data-ttu-id="0a4ff-146">Value</span><span class="sxs-lookup"><span data-stu-id="0a4ff-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a4ff-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a4ff-147">Minimum supported client</span></span><br/> | <span data-ttu-id="0a4ff-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a4ff-148">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0a4ff-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a4ff-149">Minimum supported server</span></span><br/> | <span data-ttu-id="0a4ff-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a4ff-150">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0a4ff-151">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0a4ff-151">Type library</span></span><br/>             | <dl> <span data-ttu-id="0a4ff-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a4ff-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0a4ff-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0a4ff-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a4ff-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a4ff-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0a4ff-155">IID</span><span class="sxs-lookup"><span data-stu-id="0a4ff-155">IID</span></span><br/>                      | <span data-ttu-id="0a4ff-156">IID \_ IMsTscAx se define como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="0a4ff-156">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="0a4ff-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a4ff-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a4ff-158">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="0a4ff-158">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="0a4ff-159">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="0a4ff-159">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="0a4ff-160">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="0a4ff-160">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="0a4ff-161">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="0a4ff-161">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="0a4ff-162">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="0a4ff-162">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="0a4ff-163">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="0a4ff-163">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="0a4ff-164">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="0a4ff-164">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="0a4ff-165">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="0a4ff-165">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="0a4ff-166">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="0a4ff-166">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="0a4ff-167">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="0a4ff-167">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

