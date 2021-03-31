---
title: Propiedad IMsRdpClient FullScreen
description: Determina si el control de cliente está en modo de pantalla completa.
ms.assetid: 64fe2835-c00e-4d21-812d-dcf160147d93
ms.tgt_platform: multiple
keywords:
- Propiedad FullScreen Servicios de Escritorio remoto
- Propiedad FullScreen Servicios de Escritorio remoto, interfaz IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto, propiedad FullScreen
- Propiedad FullScreen Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto, propiedad FullScreen
- Propiedad FullScreen Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto, propiedad FullScreen
- Propiedad FullScreen Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto, propiedad FullScreen
- Propiedad FullScreen Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto, propiedad FullScreen
- Propiedad FullScreen Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto, propiedad FullScreen
- Propiedad FullScreen Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto, propiedad FullScreen
- Propiedad FullScreen Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto, propiedad FullScreen
- Propiedad FullScreen Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto, propiedad FullScreen
- Propiedad FullScreen Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto, propiedad FullScreen
topic_type:
- apiref
api_name:
- IMsRdpClient.FullScreen
- IMsRdpClient.get_FullScreen
- IMsRdpClient.put_FullScreen
- IMsRdpClient2.FullScreen
- IMsRdpClient2.get_FullScreen
- IMsRdpClient2.put_FullScreen
- IMsRdpClient3.FullScreen
- IMsRdpClient3.get_FullScreen
- IMsRdpClient3.put_FullScreen
- IMsRdpClient4.FullScreen
- IMsRdpClient4.get_FullScreen
- IMsRdpClient4.put_FullScreen
- IMsRdpClient5.FullScreen
- IMsRdpClient5.get_FullScreen
- IMsRdpClient5.put_FullScreen
- IMsRdpClient6.FullScreen
- IMsRdpClient6.get_FullScreen
- IMsRdpClient6.put_FullScreen
- IMsRdpClient7.FullScreen
- IMsRdpClient7.get_FullScreen
- IMsRdpClient7.put_FullScreen
- IMsRdpClient8.FullScreen
- IMsRdpClient8.get_FullScreen
- IMsRdpClient8.put_FullScreen
- IMsRdpClient9.FullScreen
- IMsRdpClient9.get_FullScreen
- IMsRdpClient9.put_FullScreen
- IMsRdpClient10.FullScreen
- IMsRdpClient10.get_FullScreen
- IMsRdpClient10.put_FullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1adbc8e11d2cc4fb4a8071372777a01d81b5edad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151017"
---
# <a name="imsrdpclientfullscreen-property"></a><span data-ttu-id="3ed1e-124">IMsRdpClient:: FullScreen (propiedad)</span><span class="sxs-lookup"><span data-stu-id="3ed1e-124">IMsRdpClient::FullScreen property</span></span>

<span data-ttu-id="3ed1e-125">Determina si el control de cliente está en modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="3ed1e-125">Determines whether the client control is in full-screen mode.</span></span>

<span data-ttu-id="3ed1e-126">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="3ed1e-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ed1e-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ed1e-127">Syntax</span></span>


```C++
HRESULT put_FullScreen(
  [in]  VARIANT_BOOL fFullScreen
);

HRESULT get_FullScreen(
  [out] VARIANT_BOOL *pfFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="3ed1e-128">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3ed1e-128">Property value</span></span>

<span data-ttu-id="3ed1e-129">**True** para entrar en el modo de pantalla completa, **false** para salir del modo de pantalla completa y volver al modo de ventana.</span><span class="sxs-lookup"><span data-stu-id="3ed1e-129">**True** to enter full-screen mode, **False** to leave full-screen mode and return to window mode.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3ed1e-130">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="3ed1e-130">Error codes</span></span>

<span data-ttu-id="3ed1e-131">Si los métodos se realizan correctamente, se devuelve **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="3ed1e-131">If the methods succeed, **S\_OK** is returned.</span></span> <span data-ttu-id="3ed1e-132">Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="3ed1e-132">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ed1e-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3ed1e-133">Remarks</span></span>

<span data-ttu-id="3ed1e-134">Puede establecer esta propiedad cuando el control está conectado.</span><span class="sxs-lookup"><span data-stu-id="3ed1e-134">You can set this property when the control is connected.</span></span>

<span data-ttu-id="3ed1e-135">Debe llamar al método [**IMsRdpClientNonScriptable3::p UT \_ ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) antes de llamar al método de [**\_ pantalla completa IMsTscSecuredSettings::p UT**](imstscsecuredsettings-fullscreen.md) o al método de **\_ pantalla completa IMsRdpClient::p UT** .</span><span class="sxs-lookup"><span data-stu-id="3ed1e-135">You must call the [**IMsRdpClientNonScriptable3::put\_ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) method before you call the [**IMsTscSecuredSettings::put\_Fullscreen**](imstscsecuredsettings-fullscreen.md) method or the **IMsRdpClient::put\_Fullscreen** method.</span></span>

<span data-ttu-id="3ed1e-136">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="3ed1e-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ed1e-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ed1e-137">Requirements</span></span>



| <span data-ttu-id="3ed1e-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ed1e-138">Requirement</span></span> | <span data-ttu-id="3ed1e-139">Value</span><span class="sxs-lookup"><span data-stu-id="3ed1e-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ed1e-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ed1e-140">Minimum supported client</span></span><br/> | <span data-ttu-id="3ed1e-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3ed1e-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3ed1e-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ed1e-142">Minimum supported server</span></span><br/> | <span data-ttu-id="3ed1e-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3ed1e-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3ed1e-144">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3ed1e-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="3ed1e-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ed1e-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3ed1e-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3ed1e-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ed1e-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ed1e-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3ed1e-148">IID</span><span class="sxs-lookup"><span data-stu-id="3ed1e-148">IID</span></span><br/>                      | <span data-ttu-id="3ed1e-149">IID \_ IMsRdpClient se define como 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="3ed1e-149">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="3ed1e-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="3ed1e-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ed1e-151">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="3ed1e-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="3ed1e-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="3ed1e-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="3ed1e-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="3ed1e-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="3ed1e-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="3ed1e-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="3ed1e-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="3ed1e-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="3ed1e-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="3ed1e-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="3ed1e-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="3ed1e-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="3ed1e-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="3ed1e-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="3ed1e-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="3ed1e-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="3ed1e-160">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="3ed1e-160">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





