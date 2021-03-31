---
title: Propiedad de versión de IMsTscAx
description: Especifica el número de versión del control actual.
ms.assetid: 91ddeb4c-9d61-41e7-af96-95b0c4884682
ms.tgt_platform: multiple
keywords:
- Propiedad versión Servicios de Escritorio remoto
- Propiedad version Servicios de Escritorio remoto, interfaz IMsTscAx
- Interfaz IMsTscAx Servicios de Escritorio remoto, propiedad version
- Propiedad version Servicios de Escritorio remoto, interfaz IMsRdpClient
- Interfaz IMsRdpClient Servicios de Escritorio remoto, propiedad version
- Propiedad version Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Interfaz IMsRdpClient2 Servicios de Escritorio remoto, propiedad version
- Propiedad version Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto, propiedad version
- Propiedad version Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto, propiedad version
- Propiedad version Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Interfaz IMsRdpClient5 Servicios de Escritorio remoto, propiedad version
- Propiedad version Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto, propiedad version
- Propiedad version Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Interfaz IMsRdpClient7 Servicios de Escritorio remoto, propiedad version
- Propiedad version Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto, propiedad version
- Propiedad version Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto, propiedad version
topic_type:
- apiref
api_name:
- IMsTscAx.Version
- IMsTscAx.get_Version
- IMsRdpClient.Version
- IMsRdpClient.get_Version
- IMsRdpClient2.Version
- IMsRdpClient2.get_Version
- IMsRdpClient3.Version
- IMsRdpClient3.get_Version
- IMsRdpClient4.Version
- IMsRdpClient4.get_Version
- IMsRdpClient5.Version
- IMsRdpClient5.get_Version
- IMsRdpClient6.Version
- IMsRdpClient6.get_Version
- IMsRdpClient7.Version
- IMsRdpClient7.get_Version
- IMsRdpClient8.Version
- IMsRdpClient8.get_Version
- IMsRdpClient9.Version
- IMsRdpClient9.get_Version
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff25f274d1f076c9c4119648ccb9cc6d82f43b33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490630"
---
# <a name="imstscaxversion-property"></a><span data-ttu-id="683ec-124">IMsTscAx:: version (propiedad)</span><span class="sxs-lookup"><span data-stu-id="683ec-124">IMsTscAx::Version property</span></span>

<span data-ttu-id="683ec-125">Especifica el número de versión del control actual.</span><span class="sxs-lookup"><span data-stu-id="683ec-125">Specifies the version number of the current control.</span></span>

<span data-ttu-id="683ec-126">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="683ec-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="683ec-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="683ec-127">Syntax</span></span>


```C++
HRESULT get_Version(
  [out] BSTR *pVersion
);
```



## <a name="property-value"></a><span data-ttu-id="683ec-128">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="683ec-128">Property value</span></span>

<span data-ttu-id="683ec-129">El número de versión.</span><span class="sxs-lookup"><span data-stu-id="683ec-129">The version number.</span></span>

## <a name="error-codes"></a><span data-ttu-id="683ec-130">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="683ec-130">Error codes</span></span>

<span data-ttu-id="683ec-131">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="683ec-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="683ec-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="683ec-132">Remarks</span></span>

<span data-ttu-id="683ec-133">Este método asigna la memoria necesaria para el búfer señalado por el parámetro *pVersion* .</span><span class="sxs-lookup"><span data-stu-id="683ec-133">This method allocates the memory required for the buffer pointed to by the *pVersion* parameter.</span></span> <span data-ttu-id="683ec-134">La llamada a aplicaciones de C/C++ debe liberar la memoria con una llamada a la función [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .</span><span class="sxs-lookup"><span data-stu-id="683ec-134">Calling C/C++ applications must free the memory with a call to the [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) function.</span></span> <span data-ttu-id="683ec-135">Esto no es necesario para los clientes de scripting y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="683ec-135">This is not required for Visual Basic and scripting clients.</span></span>

<span data-ttu-id="683ec-136">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="683ec-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="683ec-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="683ec-137">Requirements</span></span>



| <span data-ttu-id="683ec-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="683ec-138">Requirement</span></span> | <span data-ttu-id="683ec-139">Value</span><span class="sxs-lookup"><span data-stu-id="683ec-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="683ec-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="683ec-140">Minimum supported client</span></span><br/> | <span data-ttu-id="683ec-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="683ec-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="683ec-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="683ec-142">Minimum supported server</span></span><br/> | <span data-ttu-id="683ec-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="683ec-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="683ec-144">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="683ec-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="683ec-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="683ec-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="683ec-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="683ec-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="683ec-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="683ec-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="683ec-148">IID</span><span class="sxs-lookup"><span data-stu-id="683ec-148">IID</span></span><br/>                      | <span data-ttu-id="683ec-149">IID \_ IMsTscAx se define como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="683ec-149">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="683ec-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="683ec-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="683ec-151">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="683ec-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="683ec-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="683ec-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="683ec-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="683ec-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="683ec-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="683ec-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="683ec-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="683ec-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="683ec-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="683ec-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="683ec-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="683ec-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="683ec-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="683ec-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="683ec-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="683ec-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="683ec-160">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="683ec-160">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

