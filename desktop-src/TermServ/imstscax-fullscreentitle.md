---
title: Propiedad FullScreenTitle de IMsTscAx
description: Especifica el título de la ventana que se muestra cuando el control está en modo de pantalla completa.
ms.assetid: 441aea43-2d1c-44b7-a74f-e375e711fb4f
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad FullScreenTitle
- Propiedad FullScreenTitle Servicios de Escritorio remoto, interfaz IMsTscAx
- Servicios de Escritorio remoto de la interfaz IMsTscAx, propiedad FullScreenTitle
- Propiedad FullScreenTitle Servicios de Escritorio remoto, interfaz IMsRdpClient
- Servicios de Escritorio remoto de la interfaz IMsRdpClient, propiedad FullScreenTitle
- Propiedad FullScreenTitle Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Servicios de Escritorio remoto de la interfaz IMsRdpClient2, propiedad FullScreenTitle
- Propiedad FullScreenTitle Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Servicios de Escritorio remoto de la interfaz IMsRdpClient3, propiedad FullScreenTitle
- Propiedad FullScreenTitle Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Servicios de Escritorio remoto de la interfaz IMsRdpClient4, propiedad FullScreenTitle
- Propiedad FullScreenTitle Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad FullScreenTitle
- Propiedad FullScreenTitle Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad FullScreenTitle
- Propiedad FullScreenTitle Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad FullScreenTitle
- Propiedad FullScreenTitle Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad FullScreenTitle
- Propiedad FullScreenTitle Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad FullScreenTitle
topic_type:
- apiref
api_name:
- IMsTscAx.FullScreenTitle
- IMsTscAx.put_FullScreenTitle
- IMsRdpClient.FullScreenTitle
- IMsRdpClient.put_FullScreenTitle
- IMsRdpClient2.FullScreenTitle
- IMsRdpClient2.put_FullScreenTitle
- IMsRdpClient3.FullScreenTitle
- IMsRdpClient3.put_FullScreenTitle
- IMsRdpClient4.FullScreenTitle
- IMsRdpClient4.put_FullScreenTitle
- IMsRdpClient5.FullScreenTitle
- IMsRdpClient5.put_FullScreenTitle
- IMsRdpClient6.FullScreenTitle
- IMsRdpClient6.put_FullScreenTitle
- IMsRdpClient7.FullScreenTitle
- IMsRdpClient7.put_FullScreenTitle
- IMsRdpClient8.FullScreenTitle
- IMsRdpClient8.put_FullScreenTitle
- IMsRdpClient9.FullScreenTitle
- IMsRdpClient9.put_FullScreenTitle
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1384d1582f4f0089df55030c22471438575bd072
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150501"
---
# <a name="imstscaxfullscreentitle-property"></a><span data-ttu-id="007ed-124">IMsTscAx:: FullScreenTitle (propiedad)</span><span class="sxs-lookup"><span data-stu-id="007ed-124">IMsTscAx::FullScreenTitle property</span></span>

<span data-ttu-id="007ed-125">Especifica el título de la ventana que se muestra cuando el control está en modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="007ed-125">Specifies the window title displayed when the control is in full-screen mode.</span></span>

<span data-ttu-id="007ed-126">Esta propiedad es de solo escritura.</span><span class="sxs-lookup"><span data-stu-id="007ed-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="007ed-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="007ed-127">Syntax</span></span>


```C++
HRESULT put_FullScreenTitle(
  [in] BSTR fullScreenTitle
);
```



## <a name="property-value"></a><span data-ttu-id="007ed-128">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="007ed-128">Property value</span></span>

<span data-ttu-id="007ed-129">El título de la ventana.</span><span class="sxs-lookup"><span data-stu-id="007ed-129">The window title.</span></span> <span data-ttu-id="007ed-130">La longitud máxima de esta cadena es la \_ ruta de acceso Max-1 caracteres.</span><span class="sxs-lookup"><span data-stu-id="007ed-130">The maximum length of this string is MAX\_PATH-1 characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="007ed-131">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="007ed-131">Error codes</span></span>

<span data-ttu-id="007ed-132">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="007ed-132">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="007ed-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="007ed-133">Remarks</span></span>

<span data-ttu-id="007ed-134">Esta propiedad se usa para establecer el título de la ventana del control cuando la conexión se abre en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="007ed-134">This property is used to set the title of the control's window when the connection is opened in full-screen mode.</span></span> <span data-ttu-id="007ed-135">No utilice esta propiedad para el modo de pantalla completa controlado por contenedores.</span><span class="sxs-lookup"><span data-stu-id="007ed-135">Do not use this property for container-handled full-screen mode.</span></span> <span data-ttu-id="007ed-136">Cuando se llama al método [**IMsTscAdvancedSettings::p UT \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) , la ventana contenedor muestra el título de la ventana.</span><span class="sxs-lookup"><span data-stu-id="007ed-136">When the [**IMsTscAdvancedSettings::put\_ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) method is called, the container window displays the window title.</span></span>

<span data-ttu-id="007ed-137">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="007ed-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="007ed-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="007ed-138">Requirements</span></span>



| <span data-ttu-id="007ed-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="007ed-139">Requirement</span></span> | <span data-ttu-id="007ed-140">Value</span><span class="sxs-lookup"><span data-stu-id="007ed-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="007ed-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="007ed-141">Minimum supported client</span></span><br/> | <span data-ttu-id="007ed-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="007ed-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="007ed-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="007ed-143">Minimum supported server</span></span><br/> | <span data-ttu-id="007ed-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="007ed-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="007ed-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="007ed-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="007ed-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="007ed-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="007ed-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="007ed-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="007ed-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="007ed-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="007ed-149">IID</span><span class="sxs-lookup"><span data-stu-id="007ed-149">IID</span></span><br/>                      | <span data-ttu-id="007ed-150">IID \_ IMsTscAx se define como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="007ed-150">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="007ed-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="007ed-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="007ed-152">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="007ed-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="007ed-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="007ed-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="007ed-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="007ed-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="007ed-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="007ed-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="007ed-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="007ed-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="007ed-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="007ed-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="007ed-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="007ed-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="007ed-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="007ed-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="007ed-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="007ed-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="007ed-161">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="007ed-161">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





