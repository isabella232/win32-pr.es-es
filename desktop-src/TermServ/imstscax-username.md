---
title: Propiedad de nombre de usuario IMsTscAx
description: Especifica la credencial de inicio de sesión del nombre de usuario.
ms.assetid: 9be25003-b9aa-41bb-a5a9-512546175114
ms.tgt_platform: multiple
keywords:
- Propiedad UserName Servicios de Escritorio remoto
- Propiedad UserName Servicios de Escritorio remoto, interfaz IMsTscAx
- Servicios de Escritorio remoto de la interfaz IMsTscAx, propiedad UserName
- Propiedad UserName Servicios de Escritorio remoto, interfaz IMsRdpClient
- Servicios de Escritorio remoto de la interfaz IMsRdpClient, propiedad UserName
- Propiedad UserName Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Servicios de Escritorio remoto de la interfaz IMsRdpClient2, propiedad UserName
- Propiedad UserName Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Servicios de Escritorio remoto de la interfaz IMsRdpClient3, propiedad UserName
- Propiedad UserName Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Servicios de Escritorio remoto de la interfaz IMsRdpClient4, propiedad UserName
- Propiedad UserName Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad UserName
- Propiedad UserName Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad UserName
- Propiedad UserName Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad UserName
- Propiedad UserName Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad UserName
- Propiedad UserName Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad UserName
topic_type:
- apiref
api_name:
- IMsTscAx.UserName
- IMsTscAx.get_UserName
- IMsTscAx.put_UserName
- IMsRdpClient.UserName
- IMsRdpClient.get_UserName
- IMsRdpClient.put_UserName
- IMsRdpClient2.UserName
- IMsRdpClient2.get_UserName
- IMsRdpClient2.put_UserName
- IMsRdpClient3.UserName
- IMsRdpClient3.get_UserName
- IMsRdpClient3.put_UserName
- IMsRdpClient4.UserName
- IMsRdpClient4.get_UserName
- IMsRdpClient4.put_UserName
- IMsRdpClient5.UserName
- IMsRdpClient5.get_UserName
- IMsRdpClient5.put_UserName
- IMsRdpClient6.UserName
- IMsRdpClient6.get_UserName
- IMsRdpClient6.put_UserName
- IMsRdpClient7.UserName
- IMsRdpClient7.get_UserName
- IMsRdpClient7.put_UserName
- IMsRdpClient8.UserName
- IMsRdpClient8.get_UserName
- IMsRdpClient8.put_UserName
- IMsRdpClient9.UserName
- IMsRdpClient9.get_UserName
- IMsRdpClient9.put_UserName
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a94a7f7d9fe5d6532de55f36a50094205fe1d4ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492922"
---
# <a name="imstscaxusername-property"></a><span data-ttu-id="955d6-124">IMsTscAx:: UserName (propiedad)</span><span class="sxs-lookup"><span data-stu-id="955d6-124">IMsTscAx::UserName property</span></span>

<span data-ttu-id="955d6-125">Especifica la credencial de inicio de sesión del nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="955d6-125">Specifies the user name logon credential.</span></span>

<span data-ttu-id="955d6-126">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="955d6-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="955d6-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="955d6-127">Syntax</span></span>


```C++
HRESULT put_UserName(
  [in]  BSTR newVal
);

HRESULT get_UserName(
  [out] BSTR *pUserName
);
```



## <a name="property-value"></a><span data-ttu-id="955d6-128">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="955d6-128">Property value</span></span>

<span data-ttu-id="955d6-129">El nuevo nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="955d6-129">The new user name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="955d6-130">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="955d6-130">Error codes</span></span>

<span data-ttu-id="955d6-131">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="955d6-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="955d6-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="955d6-132">Remarks</span></span>

<span data-ttu-id="955d6-133">El establecimiento de la propiedad **username** es opcional.</span><span class="sxs-lookup"><span data-stu-id="955d6-133">Setting the **UserName** property is optional.</span></span> <span data-ttu-id="955d6-134">Si no se especifica, el usuario puede proporcionar un nombre de usuario cuando aparece el cuadro de diálogo Inicio de sesión de Windows durante la conexión.</span><span class="sxs-lookup"><span data-stu-id="955d6-134">If it is not specified, the user can provide a user name when the Windows Logon dialog box appears during connection.</span></span>

<span data-ttu-id="955d6-135">Esta propiedad solo se puede establecer si el control no está en estado conectado.</span><span class="sxs-lookup"><span data-stu-id="955d6-135">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="955d6-136">Devuelve **E \_ produce un error** si se llama cuando el control está conectado.</span><span class="sxs-lookup"><span data-stu-id="955d6-136">It returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="955d6-137">Puede comprobar si el control está conectado respondiendo a los eventos de conexión en [**IMsTscAxEvents**](imstscaxevents-interface.md) o examinando la propiedad [**Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="955d6-137">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="955d6-138">El método **Get \_ username** Property asigna la memoria necesaria para el búfer señalado por el parámetro *pVersion* .</span><span class="sxs-lookup"><span data-stu-id="955d6-138">The **get\_UserName** property method allocates the memory required for the buffer pointed to by the *pVersion* parameter.</span></span> <span data-ttu-id="955d6-139">La llamada a aplicaciones de C/C++ debe liberar la memoria con una llamada a la función [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="955d6-139">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="955d6-140">Esto no es necesario para los clientes de scripting y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="955d6-140">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="955d6-141">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="955d6-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="955d6-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="955d6-142">Requirements</span></span>



| <span data-ttu-id="955d6-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="955d6-143">Requirement</span></span> | <span data-ttu-id="955d6-144">Value</span><span class="sxs-lookup"><span data-stu-id="955d6-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="955d6-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="955d6-145">Minimum supported client</span></span><br/> | <span data-ttu-id="955d6-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="955d6-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="955d6-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="955d6-147">Minimum supported server</span></span><br/> | <span data-ttu-id="955d6-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="955d6-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="955d6-149">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="955d6-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="955d6-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="955d6-150"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="955d6-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="955d6-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="955d6-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="955d6-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="955d6-153">IID</span><span class="sxs-lookup"><span data-stu-id="955d6-153">IID</span></span><br/>                      | <span data-ttu-id="955d6-154">IID \_ IMsTscAx se define como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="955d6-154">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="955d6-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="955d6-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="955d6-156">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="955d6-156">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="955d6-157">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="955d6-157">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="955d6-158">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="955d6-158">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="955d6-159">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="955d6-159">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="955d6-160">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="955d6-160">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="955d6-161">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="955d6-161">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="955d6-162">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="955d6-162">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="955d6-163">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="955d6-163">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="955d6-164">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="955d6-164">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="955d6-165">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="955d6-165">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

