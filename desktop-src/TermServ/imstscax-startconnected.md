---
title: Propiedad StartConnected de IMsTscAx
description: Indica si el control establecerá la conexión del servidor de host de sesión Escritorio remoto de escritorio remoto (host de sesión de RD) inmediatamente al iniciar.
ms.assetid: cf2956c0-be4f-4f80-a14b-253ae8117824
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad StartConnected
- Propiedad StartConnected Servicios de Escritorio remoto, interfaz IMsTscAx
- Servicios de Escritorio remoto de la interfaz IMsTscAx, propiedad StartConnected
- Propiedad StartConnected Servicios de Escritorio remoto, interfaz IMsRdpClient
- Servicios de Escritorio remoto de la interfaz IMsRdpClient, propiedad StartConnected
- Propiedad StartConnected Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Servicios de Escritorio remoto de la interfaz IMsRdpClient2, propiedad StartConnected
- Propiedad StartConnected Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Servicios de Escritorio remoto de la interfaz IMsRdpClient3, propiedad StartConnected
- Propiedad StartConnected Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Servicios de Escritorio remoto de la interfaz IMsRdpClient4, propiedad StartConnected
- Propiedad StartConnected Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad StartConnected
- Propiedad StartConnected Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad StartConnected
- Propiedad StartConnected Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad StartConnected
- Propiedad StartConnected Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad StartConnected
- Propiedad StartConnected Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad StartConnected
topic_type:
- apiref
api_name:
- IMsTscAx.StartConnected
- IMsTscAx.get_StartConnected
- IMsTscAx.put_StartConnected
- IMsRdpClient.StartConnected
- IMsRdpClient.get_StartConnected
- IMsRdpClient.put_StartConnected
- IMsRdpClient2.StartConnected
- IMsRdpClient2.get_StartConnected
- IMsRdpClient2.put_StartConnected
- IMsRdpClient3.StartConnected
- IMsRdpClient3.get_StartConnected
- IMsRdpClient3.put_StartConnected
- IMsRdpClient4.StartConnected
- IMsRdpClient4.get_StartConnected
- IMsRdpClient4.put_StartConnected
- IMsRdpClient5.StartConnected
- IMsRdpClient5.get_StartConnected
- IMsRdpClient5.put_StartConnected
- IMsRdpClient6.StartConnected
- IMsRdpClient6.get_StartConnected
- IMsRdpClient6.put_StartConnected
- IMsRdpClient7.StartConnected
- IMsRdpClient7.get_StartConnected
- IMsRdpClient7.put_StartConnected
- IMsRdpClient8.StartConnected
- IMsRdpClient8.get_StartConnected
- IMsRdpClient8.put_StartConnected
- IMsRdpClient9.StartConnected
- IMsRdpClient9.get_StartConnected
- IMsRdpClient9.put_StartConnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09bda77a06723a6df63055374a3fc96cb80f7654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676595"
---
# <a name="imstscaxstartconnected-property"></a><span data-ttu-id="3b642-124">IMsTscAx:: StartConnected (propiedad)</span><span class="sxs-lookup"><span data-stu-id="3b642-124">IMsTscAx::StartConnected property</span></span>

<span data-ttu-id="3b642-125">Indica si el control establecerá la conexión del servidor de host de sesión Escritorio remoto de escritorio remoto (host de sesión de RD) inmediatamente al iniciar.</span><span class="sxs-lookup"><span data-stu-id="3b642-125">Indicates whether the control will establish the Remote Desktop Session Host (RD Session Host) server connection immediately upon startup.</span></span>

<span data-ttu-id="3b642-126">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="3b642-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b642-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b642-127">Syntax</span></span>


```C++
HRESULT put_StartConnected(
  [in]  BOOL fStartConnected
);

HRESULT get_StartConnected(
  [out] BOOL *pfStartConnected
);
```



## <a name="property-value"></a><span data-ttu-id="3b642-128">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3b642-128">Property value</span></span>

<span data-ttu-id="3b642-129">Establezca este parámetro en **true** si el control debe conectarse inmediatamente al iniciarse o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="3b642-129">Set this parameter to **TRUE** if the control should connect immediately on startup, or **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3b642-130">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="3b642-130">Error codes</span></span>

<span data-ttu-id="3b642-131">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="3b642-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b642-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b642-132">Remarks</span></span>

<span data-ttu-id="3b642-133">Esta propiedad es muy útil cuando las propiedades del control se establecen en la lista de parámetros de una <OBJECT> etiqueta, en lugar de mediante llamadas de script.</span><span class="sxs-lookup"><span data-stu-id="3b642-133">This property is most useful when the control properties are set in the parameter list of an <OBJECT> tag, rather than through script calls.</span></span>

<span data-ttu-id="3b642-134">Esta propiedad solo se puede usar si el nombre del servidor también se especifica mediante la propiedad del servidor.</span><span class="sxs-lookup"><span data-stu-id="3b642-134">This property can be used only if the server name is also specified using the server property.</span></span> <span data-ttu-id="3b642-135">Este parámetro debe establecerse antes de que se inicie el control, por ejemplo, si se incluye en la lista de parámetros de una <OBJECT> etiqueta al usar el control de una página web.</span><span class="sxs-lookup"><span data-stu-id="3b642-135">This parameter has to be set before the control starts up for example, by including it in the parameter list of an <OBJECT> tag when using the control from a webpage.</span></span>

<span data-ttu-id="3b642-136">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="3b642-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b642-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b642-137">Requirements</span></span>



| <span data-ttu-id="3b642-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b642-138">Requirement</span></span> | <span data-ttu-id="3b642-139">Value</span><span class="sxs-lookup"><span data-stu-id="3b642-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b642-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b642-140">Minimum supported client</span></span><br/> | <span data-ttu-id="3b642-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b642-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="3b642-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b642-142">Minimum supported server</span></span><br/> | <span data-ttu-id="3b642-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b642-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3b642-144">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3b642-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="3b642-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b642-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3b642-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3b642-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3b642-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b642-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="3b642-148">IID</span><span class="sxs-lookup"><span data-stu-id="3b642-148">IID</span></span><br/>                      | <span data-ttu-id="3b642-149">IID \_ IMsTscAx se define como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="3b642-149">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="3b642-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b642-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b642-151">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="3b642-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="3b642-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="3b642-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="3b642-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="3b642-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="3b642-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="3b642-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="3b642-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="3b642-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="3b642-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="3b642-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="3b642-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="3b642-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="3b642-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="3b642-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="3b642-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="3b642-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="3b642-160">Incrustar el control ActiveX Escritorio remoto en una página web</span><span class="sxs-lookup"><span data-stu-id="3b642-160">Embedding the Remote Desktop ActiveX Control in a Webpage</span></span>](embedding-the-remote-desktop-activex-control-in-a-web-page.md)
</dt> <dt>

[<span data-ttu-id="3b642-161">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="3b642-161">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





