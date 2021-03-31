---
title: Propiedad del servidor IMsTscAx (Asptlb. h)
description: Especifica el nombre del servidor al que está conectado el control actual.
ms.assetid: 81118ddd-2662-47f5-8e9d-9c2a5056820b
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de propiedades de servidor
- Servicios de Escritorio remoto de propiedades de servidor, interfaz IMsTscAx
- Interfaz IMsTscAx Servicios de Escritorio remoto, propiedad de servidor
- Servicios de Escritorio remoto de propiedades de servidor, interfaz IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto, propiedad de servidor
- Servicios de Escritorio remoto de propiedades de servidor, interfaz IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto, propiedad de servidor
- Servicios de Escritorio remoto de propiedades de servidor, interfaz IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto, propiedad de servidor
- Servicios de Escritorio remoto de propiedades de servidor, interfaz IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto, propiedad de servidor
- Servicios de Escritorio remoto de propiedades de servidor, interfaz IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto, propiedad de servidor
- Servicios de Escritorio remoto de propiedades de servidor, interfaz IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto, propiedad de servidor
- Servicios de Escritorio remoto de propiedades de servidor, interfaz IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto, propiedad de servidor
- Servicios de Escritorio remoto de propiedades de servidor, interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto, propiedad de servidor
- Servicios de Escritorio remoto de propiedades de servidor, interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto, propiedad de servidor
topic_type:
- apiref
api_name:
- IMsTscAx.Server
- IMsTscAx.get_Server
- IMsTscAx.put_Server
- IMsRdpClient.Server
- IMsRdpClient.get_Server
- IMsRdpClient.put_Server
- IMsRdpClient2.Server
- IMsRdpClient2.get_Server
- IMsRdpClient2.put_Server
- IMsRdpClient3.Server
- IMsRdpClient3.get_Server
- IMsRdpClient3.put_Server
- IMsRdpClient4.Server
- IMsRdpClient4.get_Server
- IMsRdpClient4.put_Server
- IMsRdpClient5.Server
- IMsRdpClient5.get_Server
- IMsRdpClient5.put_Server
- IMsRdpClient6.Server
- IMsRdpClient6.get_Server
- IMsRdpClient6.put_Server
- IMsRdpClient7.Server
- IMsRdpClient7.get_Server
- IMsRdpClient7.put_Server
- IMsRdpClient8.Server
- IMsRdpClient8.get_Server
- IMsRdpClient8.put_Server
- IMsRdpClient9.Server
- IMsRdpClient9.get_Server
- IMsRdpClient9.put_Server
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b7be04c149e2ac10c1a3e905678bd2b5f663cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996013"
---
# <a name="imstscaxserver-property"></a><span data-ttu-id="4af59-124">IMsTscAx:: Server (propiedad)</span><span class="sxs-lookup"><span data-stu-id="4af59-124">IMsTscAx::Server property</span></span>

<span data-ttu-id="4af59-125">Especifica el nombre del servidor al que está conectado el control actual.</span><span class="sxs-lookup"><span data-stu-id="4af59-125">Specifies the name of the server to which the current control is connected.</span></span>

<span data-ttu-id="4af59-126">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="4af59-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4af59-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4af59-127">Syntax</span></span>


```C++
HRESULT put_Server(
  [in]  BSTR newVal
);

HRESULT get_Server(
  [out] BSTR *pServer
);
```



## <a name="property-value"></a><span data-ttu-id="4af59-128">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4af59-128">Property value</span></span>

<span data-ttu-id="4af59-129">Nombre del nuevo servidor.</span><span class="sxs-lookup"><span data-stu-id="4af59-129">The new server name.</span></span> <span data-ttu-id="4af59-130">Este parámetro puede ser un nombre DNS o una dirección IP.</span><span class="sxs-lookup"><span data-stu-id="4af59-130">This parameter can be a DNS name or IP address.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4af59-131">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="4af59-131">Error codes</span></span>

<span data-ttu-id="4af59-132">Si los métodos se realizan correctamente, se devuelve **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="4af59-132">If the methods succeed, **S\_OK** is returned.</span></span> <span data-ttu-id="4af59-133">Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="4af59-133">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="4af59-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4af59-134">Remarks</span></span>

<span data-ttu-id="4af59-135">Esta propiedad debe establecerse antes de llamar al método [**Connect**](imstscax-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="4af59-135">This property must be set before calling the [**Connect**](imstscax-connect.md) method.</span></span> <span data-ttu-id="4af59-136">Es la única propiedad que se debe establecer antes de la conexión.</span><span class="sxs-lookup"><span data-stu-id="4af59-136">It is the only property that must be set before connecting.</span></span>

<span data-ttu-id="4af59-137">Esta propiedad solo se puede establecer si el control no está en estado conectado.</span><span class="sxs-lookup"><span data-stu-id="4af59-137">This property can be set only if the control is not in the connected state.</span></span> <span data-ttu-id="4af59-138">Esta propiedad devuelve **E \_ produce un error** si se llama cuando el control está conectado.</span><span class="sxs-lookup"><span data-stu-id="4af59-138">This property returns **E\_FAIL** if it is called when the control is connected.</span></span> <span data-ttu-id="4af59-139">Puede comprobar el estado conectado mediante la propiedad [**conectado**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="4af59-139">You can check for the connected state by using the [**Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="4af59-140">Este método asigna la memoria necesaria para el búfer señalado por el parámetro *pServer* .</span><span class="sxs-lookup"><span data-stu-id="4af59-140">This method allocates the memory required for the buffer pointed to by the *pServer* parameter.</span></span> <span data-ttu-id="4af59-141">La llamada a aplicaciones de C/C++ debe liberar la memoria con una llamada a la función [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="4af59-141">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="4af59-142">Esto no es necesario para los clientes de scripting y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4af59-142">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="4af59-143">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="4af59-143">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4af59-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4af59-144">Requirements</span></span>



| <span data-ttu-id="4af59-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="4af59-145">Requirement</span></span> | <span data-ttu-id="4af59-146">Value</span><span class="sxs-lookup"><span data-stu-id="4af59-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4af59-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4af59-147">Minimum supported client</span></span><br/> | <span data-ttu-id="4af59-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4af59-148">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4af59-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4af59-149">Minimum supported server</span></span><br/> | <span data-ttu-id="4af59-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4af59-150">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4af59-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4af59-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="4af59-152"><dt>Asptlb. h</dt></span><span class="sxs-lookup"><span data-stu-id="4af59-152"><dt>Asptlb.h</dt></span></span> </dl>    |
| <span data-ttu-id="4af59-153">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4af59-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="4af59-154"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4af59-154"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4af59-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4af59-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4af59-156"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4af59-156"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4af59-157">IID</span><span class="sxs-lookup"><span data-stu-id="4af59-157">IID</span></span><br/>                      | <span data-ttu-id="4af59-158">IID \_ IMsTscAx se define como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="4af59-158">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="4af59-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="4af59-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4af59-160">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="4af59-160">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="4af59-161">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="4af59-161">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="4af59-162">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="4af59-162">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="4af59-163">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="4af59-163">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="4af59-164">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="4af59-164">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="4af59-165">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="4af59-165">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="4af59-166">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="4af59-166">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="4af59-167">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="4af59-167">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="4af59-168">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="4af59-168">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="4af59-169">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="4af59-169">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

