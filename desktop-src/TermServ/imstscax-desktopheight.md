---
title: Propiedad DesktopHeight de IMsTscAx
description: Especifica el alto del control actual, en píxeles, en el escritorio remoto inicial.
ms.assetid: 7071053b-bdd1-408b-ab69-965c504fafb0
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DesktopHeight
- Propiedad DesktopHeight Servicios de Escritorio remoto, interfaz IMsTscAx
- Servicios de Escritorio remoto de la interfaz IMsTscAx, propiedad DesktopHeight
- Propiedad DesktopHeight Servicios de Escritorio remoto, interfaz IMsRdpClient
- Servicios de Escritorio remoto de la interfaz IMsRdpClient, propiedad DesktopHeight
- Propiedad DesktopHeight Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Servicios de Escritorio remoto de la interfaz IMsRdpClient2, propiedad DesktopHeight
- Propiedad DesktopHeight Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Servicios de Escritorio remoto de la interfaz IMsRdpClient3, propiedad DesktopHeight
- Propiedad DesktopHeight Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Servicios de Escritorio remoto de la interfaz IMsRdpClient4, propiedad DesktopHeight
- Propiedad DesktopHeight Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad DesktopHeight
- Propiedad DesktopHeight Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad DesktopHeight
- Propiedad DesktopHeight Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad DesktopHeight
- Propiedad DesktopHeight Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad DesktopHeight
- Propiedad DesktopHeight Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad DesktopHeight
topic_type:
- apiref
api_name:
- IMsTscAx.DesktopHeight
- IMsTscAx.get_DesktopHeight
- IMsTscAx.put_DesktopHeight
- IMsRdpClient.DesktopHeight
- IMsRdpClient.get_DesktopHeight
- IMsRdpClient.put_DesktopHeight
- IMsRdpClient2.DesktopHeight
- IMsRdpClient2.get_DesktopHeight
- IMsRdpClient2.put_DesktopHeight
- IMsRdpClient3.DesktopHeight
- IMsRdpClient3.get_DesktopHeight
- IMsRdpClient3.put_DesktopHeight
- IMsRdpClient4.DesktopHeight
- IMsRdpClient4.get_DesktopHeight
- IMsRdpClient4.put_DesktopHeight
- IMsRdpClient5.DesktopHeight
- IMsRdpClient5.get_DesktopHeight
- IMsRdpClient5.put_DesktopHeight
- IMsRdpClient6.DesktopHeight
- IMsRdpClient6.get_DesktopHeight
- IMsRdpClient6.put_DesktopHeight
- IMsRdpClient7.DesktopHeight
- IMsRdpClient7.get_DesktopHeight
- IMsRdpClient7.put_DesktopHeight
- IMsRdpClient8.DesktopHeight
- IMsRdpClient8.get_DesktopHeight
- IMsRdpClient8.put_DesktopHeight
- IMsRdpClient9.DesktopHeight
- IMsRdpClient9.get_DesktopHeight
- IMsRdpClient9.put_DesktopHeight
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb75467b35703420ce49fd99ea032b139d721505
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996677"
---
# <a name="imstscaxdesktopheight-property"></a><span data-ttu-id="52203-124">IMsTscAx::D propiedad esktopHeight</span><span class="sxs-lookup"><span data-stu-id="52203-124">IMsTscAx::DesktopHeight property</span></span>

<span data-ttu-id="52203-125">Especifica el alto del control actual, en píxeles, en el escritorio remoto inicial.</span><span class="sxs-lookup"><span data-stu-id="52203-125">Specifies the current control's height, in pixels, on the initial remote desktop.</span></span>

<span data-ttu-id="52203-126">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="52203-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="52203-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52203-127">Syntax</span></span>


```C++
HRESULT put_DesktopHeight(
  [in]  LONG newVal
);

HRESULT get_DesktopHeight(
  [out] LONG *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="52203-128">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="52203-128">Property value</span></span>

<span data-ttu-id="52203-129">Nuevo alto, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="52203-129">The new height, in pixels.</span></span>

## <a name="error-codes"></a><span data-ttu-id="52203-130">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="52203-130">Error codes</span></span>

<span data-ttu-id="52203-131">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="52203-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="52203-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52203-132">Remarks</span></span>

<span data-ttu-id="52203-133">Establecer la propiedad **DesktopHeight** es opcional, pero debe establecerse antes de llamar al método [**Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="52203-133">Setting the **DesktopHeight** property is optional, but it must be set before calling the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="52203-134">Si no se especifica un alto de escritorio o se establece en cero, el alto del escritorio se establece en el alto del control.</span><span class="sxs-lookup"><span data-stu-id="52203-134">If a desktop height is not specified, or is set to zero, the desktop height is set to the height of the control.</span></span> <span data-ttu-id="52203-135">Los valores mínimo y máximo dependen de la versión del sistema operativo del cliente Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="52203-135">The minimum and maximum values are dependent upon the operating system version of the Remote Desktop client.</span></span>

<dl> <dt>

<span data-ttu-id="52203-136"><span id="_"></span>Windows 8/Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="52203-136"><span id="_"></span>Windows 8/Windows Server 2012</span></span>
</dt> <dd>

<span data-ttu-id="52203-137">200 como mínimo, 8192 como máximo</span><span class="sxs-lookup"><span data-stu-id="52203-137">200 minimum, 8192 maximum</span></span>

</dd> <dt>

<span data-ttu-id="52203-138"><span id="_"></span>Windows 7/Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52203-138"><span id="_"></span>Windows 7/Windows Server 2008</span></span>
</dt> <dd>

<span data-ttu-id="52203-139">200 como mínimo, 2048 como máximo</span><span class="sxs-lookup"><span data-stu-id="52203-139">200 minimum, 2048 maximum</span></span>

</dd> <dt>

<span data-ttu-id="52203-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52203-140">Windows Vista</span></span>
</dt> <dd>

<span data-ttu-id="52203-141">200 como mínimo, 1200 como máximo</span><span class="sxs-lookup"><span data-stu-id="52203-141">200 minimum, 1200 maximum</span></span>

</dd> </dl>

<span data-ttu-id="52203-142">Una vez establecida una conexión, los cambios en el alto del control no cambian el alto del escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="52203-142">After a connection is established, any changes to the control's height do not change the height of the remote desktop.</span></span> <span data-ttu-id="52203-143">En su lugar, el control muestra barras de desplazamiento o centra el escritorio remoto, según corresponda.</span><span class="sxs-lookup"><span data-stu-id="52203-143">Instead, the control brings up scroll bars or centers the remote desktop, as appropriate.</span></span> <span data-ttu-id="52203-144">Para cambiar el tamaño del escritorio de una conexión activa, utilice el método [**IMsRdpClient8:: reconnect**](imsrdpclient8-reconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="52203-144">To change the desktop size of an active connection, use the [**IMsRdpClient8::Reconnect**](imsrdpclient8-reconnect.md) method.</span></span>

<span data-ttu-id="52203-145">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="52203-145">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="52203-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52203-146">Requirements</span></span>



| <span data-ttu-id="52203-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="52203-147">Requirement</span></span> | <span data-ttu-id="52203-148">Value</span><span class="sxs-lookup"><span data-stu-id="52203-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52203-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52203-149">Minimum supported client</span></span><br/> | <span data-ttu-id="52203-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52203-150">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="52203-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="52203-151">Minimum supported server</span></span><br/> | <span data-ttu-id="52203-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52203-152">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="52203-153">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="52203-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="52203-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52203-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="52203-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="52203-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52203-156"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52203-156"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="52203-157">IID</span><span class="sxs-lookup"><span data-stu-id="52203-157">IID</span></span><br/>                      | <span data-ttu-id="52203-158">IID \_ IMsTscAx se define como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="52203-158">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="52203-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="52203-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52203-160">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="52203-160">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="52203-161">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="52203-161">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="52203-162">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="52203-162">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="52203-163">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="52203-163">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="52203-164">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="52203-164">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="52203-165">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="52203-165">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="52203-166">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="52203-166">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="52203-167">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="52203-167">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="52203-168">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="52203-168">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="52203-169">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="52203-169">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





