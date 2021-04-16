---
title: Propiedad DesktopWidth de IMsTscAx
description: Especifica el ancho del control actual, en píxeles, en el escritorio remoto inicial.
ms.assetid: 3b349f6c-d068-4047-b8b5-29d022894729
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DesktopWidth
- Propiedad DesktopWidth Servicios de Escritorio remoto, interfaz IMsTscAx
- Servicios de Escritorio remoto de la interfaz IMsTscAx, propiedad DesktopWidth
- Propiedad DesktopWidth Servicios de Escritorio remoto, interfaz IMsRdpClient
- Servicios de Escritorio remoto de la interfaz IMsRdpClient, propiedad DesktopWidth
- Propiedad DesktopWidth Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Servicios de Escritorio remoto de la interfaz IMsRdpClient2, propiedad DesktopWidth
- Propiedad DesktopWidth Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Servicios de Escritorio remoto de la interfaz IMsRdpClient3, propiedad DesktopWidth
- Propiedad DesktopWidth Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Servicios de Escritorio remoto de la interfaz IMsRdpClient4, propiedad DesktopWidth
- Propiedad DesktopWidth Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad DesktopWidth
- Propiedad DesktopWidth Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad DesktopWidth
- Propiedad DesktopWidth Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad DesktopWidth
- Propiedad DesktopWidth Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad DesktopWidth
- Propiedad DesktopWidth Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad DesktopWidth
topic_type:
- apiref
api_name:
- IMsTscAx.DesktopWidth
- IMsTscAx.get_DesktopWidth
- IMsTscAx.put_DesktopWidth
- IMsRdpClient.DesktopWidth
- IMsRdpClient.get_DesktopWidth
- IMsRdpClient.put_DesktopWidth
- IMsRdpClient2.DesktopWidth
- IMsRdpClient2.get_DesktopWidth
- IMsRdpClient2.put_DesktopWidth
- IMsRdpClient3.DesktopWidth
- IMsRdpClient3.get_DesktopWidth
- IMsRdpClient3.put_DesktopWidth
- IMsRdpClient4.DesktopWidth
- IMsRdpClient4.get_DesktopWidth
- IMsRdpClient4.put_DesktopWidth
- IMsRdpClient5.DesktopWidth
- IMsRdpClient5.get_DesktopWidth
- IMsRdpClient5.put_DesktopWidth
- IMsRdpClient6.DesktopWidth
- IMsRdpClient6.get_DesktopWidth
- IMsRdpClient6.put_DesktopWidth
- IMsRdpClient7.DesktopWidth
- IMsRdpClient7.get_DesktopWidth
- IMsRdpClient7.put_DesktopWidth
- IMsRdpClient8.DesktopWidth
- IMsRdpClient8.get_DesktopWidth
- IMsRdpClient8.put_DesktopWidth
- IMsRdpClient9.DesktopWidth
- IMsRdpClient9.get_DesktopWidth
- IMsRdpClient9.put_DesktopWidth
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16cd1391c6aeb27d9ec0f87317b06e9084337fbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534132"
---
# <a name="imstscaxdesktopwidth-property"></a><span data-ttu-id="65606-124">IMsTscAx::D propiedad esktopWidth</span><span class="sxs-lookup"><span data-stu-id="65606-124">IMsTscAx::DesktopWidth property</span></span>

<span data-ttu-id="65606-125">Especifica el ancho del control actual, en píxeles, en el escritorio remoto inicial.</span><span class="sxs-lookup"><span data-stu-id="65606-125">Specifies the current control's width, in pixels, on the initial remote desktop.</span></span>

<span data-ttu-id="65606-126">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="65606-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="65606-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65606-127">Syntax</span></span>


```C++
HRESULT put_DesktopWidth(
  [in]  LONG newVal
);

HRESULT get_DesktopWidth(
  [out] LONG *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="65606-128">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="65606-128">Property value</span></span>

<span data-ttu-id="65606-129">Nuevo ancho, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="65606-129">The new width, in pixels.</span></span>

## <a name="error-codes"></a><span data-ttu-id="65606-130">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="65606-130">Error codes</span></span>

<span data-ttu-id="65606-131">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="65606-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="65606-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="65606-132">Remarks</span></span>

<span data-ttu-id="65606-133">Establecer la propiedad **DesktopWidth** es opcional, pero debe establecerse antes de llamar al método [**Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="65606-133">Setting the **DesktopWidth** property is optional, but it must be set before calling the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="65606-134">Si no se especifica un ancho de escritorio o se establece en cero, el ancho del escritorio se establece en el ancho del control.</span><span class="sxs-lookup"><span data-stu-id="65606-134">If a desktop width is not specified, or is set to zero, the desktop width is set to the width of the control.</span></span> <span data-ttu-id="65606-135">Los valores mínimo y máximo dependen de la versión del sistema operativo del cliente Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="65606-135">The minimum and maximum values are dependent upon the operating system version of the Remote Desktop client.</span></span>

<dl> <dt>

<span data-ttu-id="65606-136"><span id="_"></span>Windows 8/Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="65606-136"><span id="_"></span>Windows 8/Windows Server 2012</span></span>
</dt> <dd>

<span data-ttu-id="65606-137">200 como mínimo, 8192 como máximo</span><span class="sxs-lookup"><span data-stu-id="65606-137">200 minimum, 8192 maximum</span></span>

</dd> <dt>

<span data-ttu-id="65606-138"><span id="_"></span>Windows 7/Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65606-138"><span id="_"></span>Windows 7/Windows Server 2008</span></span>
</dt> <dd>

<span data-ttu-id="65606-139">200 como mínimo, 2048 como máximo</span><span class="sxs-lookup"><span data-stu-id="65606-139">200 minimum, 2048 maximum</span></span>

</dd> <dt>

<span data-ttu-id="65606-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65606-140">Windows Vista</span></span>
</dt> <dd>

<span data-ttu-id="65606-141">200 como mínimo, 1200 como máximo</span><span class="sxs-lookup"><span data-stu-id="65606-141">200 minimum, 1200 maximum</span></span>

</dd> </dl>

<span data-ttu-id="65606-142">Una vez establecida una conexión, los cambios en el ancho del control no cambian el ancho del escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="65606-142">After a connection is established, any changes to the control's width do not change the width of the remote desktop.</span></span> <span data-ttu-id="65606-143">En su lugar, el control muestra barras de desplazamiento o centra el escritorio remoto, según corresponda.</span><span class="sxs-lookup"><span data-stu-id="65606-143">Instead, the control brings up scroll bars or centers the remote desktop, as appropriate.</span></span> <span data-ttu-id="65606-144">Para cambiar el tamaño del escritorio de una conexión activa, utilice el método [**IMsRdpClient8:: reconnect**](imsrdpclient8-reconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="65606-144">To change the desktop size of an active connection, use the [**IMsRdpClient8::Reconnect**](imsrdpclient8-reconnect.md) method.</span></span>

<span data-ttu-id="65606-145">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="65606-145">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="65606-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65606-146">Requirements</span></span>



| <span data-ttu-id="65606-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="65606-147">Requirement</span></span> | <span data-ttu-id="65606-148">Value</span><span class="sxs-lookup"><span data-stu-id="65606-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="65606-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65606-149">Minimum supported client</span></span><br/> | <span data-ttu-id="65606-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="65606-150">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="65606-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65606-151">Minimum supported server</span></span><br/> | <span data-ttu-id="65606-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="65606-152">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="65606-153">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="65606-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="65606-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65606-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="65606-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="65606-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65606-156"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65606-156"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="65606-157">IID</span><span class="sxs-lookup"><span data-stu-id="65606-157">IID</span></span><br/>                      | <span data-ttu-id="65606-158">IID \_ IMsTscAx se define como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="65606-158">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="65606-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="65606-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65606-160">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="65606-160">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="65606-161">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="65606-161">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="65606-162">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="65606-162">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="65606-163">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="65606-163">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="65606-164">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="65606-164">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="65606-165">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="65606-165">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="65606-166">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="65606-166">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="65606-167">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="65606-167">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="65606-168">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="65606-168">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="65606-169">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="65606-169">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





