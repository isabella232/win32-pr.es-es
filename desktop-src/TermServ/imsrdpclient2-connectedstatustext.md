---
title: Propiedad ConnectedStatusText de IMsRdpClient2
description: Contiene el texto que se muestra en el área cliente del control mientras el control está en estado conectado.
ms.assetid: c3d8433b-2fb0-413d-88a3-667149f858ba
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad ConnectedStatusText
- Propiedad ConnectedStatusText Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Servicios de Escritorio remoto de la interfaz IMsRdpClient2, propiedad ConnectedStatusText
- Propiedad ConnectedStatusText Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Servicios de Escritorio remoto de la interfaz IMsRdpClient3, propiedad ConnectedStatusText
- Propiedad ConnectedStatusText Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Servicios de Escritorio remoto de la interfaz IMsRdpClient4, propiedad ConnectedStatusText
- Propiedad ConnectedStatusText Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad ConnectedStatusText
- Propiedad ConnectedStatusText Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad ConnectedStatusText
- Propiedad ConnectedStatusText Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad ConnectedStatusText
- Propiedad ConnectedStatusText Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad ConnectedStatusText
- Propiedad ConnectedStatusText Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad ConnectedStatusText
- Propiedad ConnectedStatusText Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Servicios de Escritorio remoto de la interfaz IMsRdpClient10, propiedad ConnectedStatusText
topic_type:
- apiref
api_name:
- IMsRdpClient2.ConnectedStatusText
- IMsRdpClient2.get_ConnectedStatusText
- IMsRdpClient2.put_ConnectedStatusText
- IMsRdpClient3.ConnectedStatusText
- IMsRdpClient3.get_ConnectedStatusText
- IMsRdpClient3.put_ConnectedStatusText
- IMsRdpClient4.ConnectedStatusText
- IMsRdpClient4.get_ConnectedStatusText
- IMsRdpClient4.put_ConnectedStatusText
- IMsRdpClient5.ConnectedStatusText
- IMsRdpClient5.get_ConnectedStatusText
- IMsRdpClient5.put_ConnectedStatusText
- IMsRdpClient6.ConnectedStatusText
- IMsRdpClient6.get_ConnectedStatusText
- IMsRdpClient6.put_ConnectedStatusText
- IMsRdpClient7.ConnectedStatusText
- IMsRdpClient7.get_ConnectedStatusText
- IMsRdpClient7.put_ConnectedStatusText
- IMsRdpClient8.ConnectedStatusText
- IMsRdpClient8.get_ConnectedStatusText
- IMsRdpClient8.put_ConnectedStatusText
- IMsRdpClient9.ConnectedStatusText
- IMsRdpClient9.get_ConnectedStatusText
- IMsRdpClient9.put_ConnectedStatusText
- IMsRdpClient10.ConnectedStatusText
- IMsRdpClient10.get_ConnectedStatusText
- IMsRdpClient10.put_ConnectedStatusText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd6ee2ac155aa3fc4873ee1a5eb890774b50978
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685903"
---
# <a name="imsrdpclient2connectedstatustext-property"></a><span data-ttu-id="45b8e-122">IMsRdpClient2:: ConnectedStatusText (propiedad)</span><span class="sxs-lookup"><span data-stu-id="45b8e-122">IMsRdpClient2::ConnectedStatusText property</span></span>

<span data-ttu-id="45b8e-123">Contiene el texto que se muestra en el área cliente del control mientras el control está en estado conectado.</span><span class="sxs-lookup"><span data-stu-id="45b8e-123">Contains the text that is displayed in the client area of the control while the control is in the connected state.</span></span>

<span data-ttu-id="45b8e-124">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="45b8e-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="45b8e-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45b8e-125">Syntax</span></span>


```C++
HRESULT put_ConnectedStatusText(
  [in]  BSTR newVal
);

HRESULT get_ConnectedStatusText(
  [out] BSTR *pConnectedStatusText
);
```



## <a name="property-value"></a><span data-ttu-id="45b8e-126">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="45b8e-126">Property value</span></span>

<span data-ttu-id="45b8e-127">La propiedad **ConnectedStatusText** contiene el texto que se muestra en el área cliente del control mientras el control está en estado conectado.</span><span class="sxs-lookup"><span data-stu-id="45b8e-127">The **ConnectedStatusText** property contains the text that is displayed in the client area of the control while the control is in the connected state.</span></span>

## <a name="error-codes"></a><span data-ttu-id="45b8e-128">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="45b8e-128">Error codes</span></span>

<span data-ttu-id="45b8e-129">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="45b8e-129">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="45b8e-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45b8e-130">Remarks</span></span>

<span data-ttu-id="45b8e-131">Texto que se va a mostrar en el área cliente del control mientras el control está en estado conectado.</span><span class="sxs-lookup"><span data-stu-id="45b8e-131">Text to display in the client area of the control while the control is in the connected state.</span></span> <span data-ttu-id="45b8e-132">Este es el texto que es visible, por ejemplo, cuando el usuario cambia el control al modo de pantalla completa en un explorador Web, un escenario que deja una parte del control hospedado en el explorador.</span><span class="sxs-lookup"><span data-stu-id="45b8e-132">This is the text that is visible, for example, when the user switches the control to the full-screen mode in a web browser, a scenario that leaves a portion of the control hosted in the browser.</span></span>

<span data-ttu-id="45b8e-133">El método **Get \_ ConnectedStatusText** asigna la memoria necesaria para el búfer señalado por el parámetro *pConnectedStatusText* .</span><span class="sxs-lookup"><span data-stu-id="45b8e-133">The **get\_ConnectedStatusText** method allocates the memory required for the buffer pointed to by the *pConnectedStatusText* parameter.</span></span> <span data-ttu-id="45b8e-134">La llamada a aplicaciones de C/C++ debe liberar la memoria con una llamada a la función [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="45b8e-134">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="45b8e-135">Esto no es necesario para los clientes de scripting y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="45b8e-135">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="45b8e-136">No se puede establecer esta propiedad cuando el control está conectado.</span><span class="sxs-lookup"><span data-stu-id="45b8e-136">This property cannot be set when the control is connected.</span></span> <span data-ttu-id="45b8e-137">Puede comprobar si el control está conectado llamando al método [**IMsTscAx:: get \_ Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="45b8e-137">You can check if the control is connected by calling the [**IMsTscAx::get\_Connected**](imstscax-connected.md) method.</span></span>

<span data-ttu-id="45b8e-138">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="45b8e-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="45b8e-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45b8e-139">Requirements</span></span>



| <span data-ttu-id="45b8e-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="45b8e-140">Requirement</span></span> | <span data-ttu-id="45b8e-141">Value</span><span class="sxs-lookup"><span data-stu-id="45b8e-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="45b8e-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45b8e-142">Minimum supported client</span></span><br/> | <span data-ttu-id="45b8e-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="45b8e-143">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="45b8e-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45b8e-144">Minimum supported server</span></span><br/> | <span data-ttu-id="45b8e-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="45b8e-145">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="45b8e-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="45b8e-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="45b8e-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45b8e-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="45b8e-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="45b8e-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45b8e-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45b8e-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="45b8e-150">IID</span><span class="sxs-lookup"><span data-stu-id="45b8e-150">IID</span></span><br/>                      | <span data-ttu-id="45b8e-151">IID \_ IMsRdpClient2 se define como e7e17dc4-3b71-4ba7-a8e6-281ffadca28f</span><span class="sxs-lookup"><span data-stu-id="45b8e-151">IID\_IMsRdpClient2 is defined as e7e17dc4-3b71-4ba7-a8e6-281ffadca28f</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="45b8e-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="45b8e-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45b8e-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="45b8e-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="45b8e-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="45b8e-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="45b8e-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="45b8e-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="45b8e-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="45b8e-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="45b8e-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="45b8e-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="45b8e-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="45b8e-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="45b8e-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="45b8e-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="45b8e-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="45b8e-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="45b8e-161">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="45b8e-161">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

