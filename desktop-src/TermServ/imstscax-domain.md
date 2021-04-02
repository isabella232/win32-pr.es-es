---
title: Propiedad de dominio IMsTscAx
description: Especifica el dominio en el que el usuario actual inicia sesión.
ms.assetid: 5d9a2048-5f5d-43ca-a8b8-400dac7d7472
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de propiedad de dominio
- Propiedad de dominio Servicios de Escritorio remoto, interfaz IMsTscAx
- Servicios de Escritorio remoto de la interfaz IMsTscAx, propiedad del dominio
- Propiedad de dominio Servicios de Escritorio remoto, interfaz IMsRdpClient
- Servicios de Escritorio remoto de la interfaz IMsRdpClient, propiedad del dominio
- Propiedad de dominio Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Servicios de Escritorio remoto de la interfaz IMsRdpClient2, propiedad del dominio
- Propiedad de dominio Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Servicios de Escritorio remoto de la interfaz IMsRdpClient3, propiedad del dominio
- Propiedad de dominio Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Servicios de Escritorio remoto de la interfaz IMsRdpClient4, propiedad del dominio
- Propiedad de dominio Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad del dominio
- Propiedad de dominio Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad del dominio
- Propiedad de dominio Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad del dominio
- Propiedad de dominio Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad del dominio
- Propiedad de dominio Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad del dominio
topic_type:
- apiref
api_name:
- IMsTscAx.Domain
- IMsTscAx.get_Domain
- IMsTscAx.put_Domain
- IMsRdpClient.Domain
- IMsRdpClient.get_Domain
- IMsRdpClient.put_Domain
- IMsRdpClient2.Domain
- IMsRdpClient2.get_Domain
- IMsRdpClient2.put_Domain
- IMsRdpClient3.Domain
- IMsRdpClient3.get_Domain
- IMsRdpClient3.put_Domain
- IMsRdpClient4.Domain
- IMsRdpClient4.get_Domain
- IMsRdpClient4.put_Domain
- IMsRdpClient5.Domain
- IMsRdpClient5.get_Domain
- IMsRdpClient5.put_Domain
- IMsRdpClient6.Domain
- IMsRdpClient6.get_Domain
- IMsRdpClient6.put_Domain
- IMsRdpClient7.Domain
- IMsRdpClient7.get_Domain
- IMsRdpClient7.put_Domain
- IMsRdpClient8.Domain
- IMsRdpClient8.get_Domain
- IMsRdpClient8.put_Domain
- IMsRdpClient9.Domain
- IMsRdpClient9.get_Domain
- IMsRdpClient9.put_Domain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faf95c02de10fe8db38a53b75d4d20cf796020f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996987"
---
# <a name="imstscaxdomain-property"></a><span data-ttu-id="16228-124">IMsTscAx::D propiedad omain</span><span class="sxs-lookup"><span data-stu-id="16228-124">IMsTscAx::Domain property</span></span>

<span data-ttu-id="16228-125">Especifica el dominio en el que el usuario actual inicia sesión.</span><span class="sxs-lookup"><span data-stu-id="16228-125">Specifies the domain to which the current user logs on.</span></span>

<span data-ttu-id="16228-126">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="16228-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="16228-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="16228-127">Syntax</span></span>


```C++
HRESULT put_Domain(
  [in]  BSTR newVal
);

HRESULT get_Domain(
  [out] BSTR *pDomain
);
```



## <a name="property-value"></a><span data-ttu-id="16228-128">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="16228-128">Property value</span></span>

<span data-ttu-id="16228-129">El nuevo nombre de dominio.</span><span class="sxs-lookup"><span data-stu-id="16228-129">The new domain name.</span></span>

## <a name="error-codes"></a><span data-ttu-id="16228-130">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="16228-130">Error codes</span></span>

<span data-ttu-id="16228-131">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="16228-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="16228-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16228-132">Remarks</span></span>

<span data-ttu-id="16228-133">El establecimiento de la propiedad de **dominio** es opcional.</span><span class="sxs-lookup"><span data-stu-id="16228-133">Setting the **Domain** property is optional.</span></span> <span data-ttu-id="16228-134">Si no se establece, el usuario puede elegir un dominio cuando aparezca el cuadro de diálogo Inicio de sesión de Windows durante la conexión.</span><span class="sxs-lookup"><span data-stu-id="16228-134">If it is not set, the user can choose a domain when the Windows Logon dialog box appears during the connection.</span></span>

<span data-ttu-id="16228-135">El método **Get \_ Domain** asigna la memoria necesaria para el búfer señalado por el parámetro *pDomain* .</span><span class="sxs-lookup"><span data-stu-id="16228-135">The **get\_Domain** method allocates the memory required for the buffer pointed to by the *pDomain* parameter.</span></span> <span data-ttu-id="16228-136">La llamada a aplicaciones de C/C++ debe liberar la memoria con una llamada a la función [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="16228-136">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="16228-137">Esto no es necesario para los clientes de scripting y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="16228-137">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="16228-138">Esta propiedad solo se puede establecer si el control no está en estado conectado.</span><span class="sxs-lookup"><span data-stu-id="16228-138">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="16228-139">Devuelve **E \_ produce un error** si se llama cuando el control está conectado.</span><span class="sxs-lookup"><span data-stu-id="16228-139">It returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="16228-140">Puede comprobar si el control está conectado respondiendo a los eventos de conexión en [**IMsTscAxEvents**](imstscaxevents-interface.md) o examinando la propiedad [**Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="16228-140">You can check if the control is connected by responding to connection events in [**IMsTscAxEvents**](imstscaxevents-interface.md) or examining the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="16228-141">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="16228-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="16228-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16228-142">Requirements</span></span>



| <span data-ttu-id="16228-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="16228-143">Requirement</span></span> | <span data-ttu-id="16228-144">Value</span><span class="sxs-lookup"><span data-stu-id="16228-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16228-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16228-145">Minimum supported client</span></span><br/> | <span data-ttu-id="16228-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16228-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="16228-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="16228-147">Minimum supported server</span></span><br/> | <span data-ttu-id="16228-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16228-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="16228-149">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="16228-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="16228-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16228-150"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="16228-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="16228-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16228-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16228-152"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="16228-153">IID</span><span class="sxs-lookup"><span data-stu-id="16228-153">IID</span></span><br/>                      | <span data-ttu-id="16228-154">IID \_ IMsTscAx se define como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="16228-154">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="16228-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="16228-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16228-156">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="16228-156">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="16228-157">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="16228-157">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="16228-158">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="16228-158">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="16228-159">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="16228-159">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="16228-160">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="16228-160">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="16228-161">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="16228-161">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="16228-162">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="16228-162">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="16228-163">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="16228-163">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="16228-164">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="16228-164">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="16228-165">**Conectado**</span><span class="sxs-lookup"><span data-stu-id="16228-165">**Connected**</span></span>](imstscax-connected.md)
</dt> <dt>

[<span data-ttu-id="16228-166">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="16228-166">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="16228-167">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="16228-167">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

