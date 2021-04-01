---
title: Propiedad SecuredSettings de IMsTscAx
description: Recupera un puntero de la interfaz IMsTscSecuredSettings.
ms.assetid: 64d4059b-e617-449d-a733-c19c1d281132
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad SecuredSettings
- Propiedad SecuredSettings Servicios de Escritorio remoto, interfaz IMsTscAx
- Servicios de Escritorio remoto de la interfaz IMsTscAx, propiedad SecuredSettings
- Propiedad SecuredSettings Servicios de Escritorio remoto, interfaz IMsRdpClient
- Servicios de Escritorio remoto de la interfaz IMsRdpClient, propiedad SecuredSettings
- Propiedad SecuredSettings Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Servicios de Escritorio remoto de la interfaz IMsRdpClient2, propiedad SecuredSettings
- Propiedad SecuredSettings Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Servicios de Escritorio remoto de la interfaz IMsRdpClient3, propiedad SecuredSettings
- Propiedad SecuredSettings Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Servicios de Escritorio remoto de la interfaz IMsRdpClient4, propiedad SecuredSettings
- Propiedad SecuredSettings Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad SecuredSettings
- Propiedad SecuredSettings Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad SecuredSettings
- Propiedad SecuredSettings Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad SecuredSettings
- Propiedad SecuredSettings Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad SecuredSettings
- Propiedad SecuredSettings Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad SecuredSettings
topic_type:
- apiref
api_name:
- IMsTscAx.SecuredSettings
- IMsTscAx.get_SecuredSettings
- IMsRdpClient.SecuredSettings
- IMsRdpClient.get_SecuredSettings
- IMsRdpClient2.SecuredSettings
- IMsRdpClient2.get_SecuredSettings
- IMsRdpClient3.SecuredSettings
- IMsRdpClient3.get_SecuredSettings
- IMsRdpClient4.SecuredSettings
- IMsRdpClient4.get_SecuredSettings
- IMsRdpClient5.SecuredSettings
- IMsRdpClient5.get_SecuredSettings
- IMsRdpClient6.SecuredSettings
- IMsRdpClient6.get_SecuredSettings
- IMsRdpClient7.SecuredSettings
- IMsRdpClient7.get_SecuredSettings
- IMsRdpClient8.SecuredSettings
- IMsRdpClient8.get_SecuredSettings
- IMsRdpClient9.SecuredSettings
- IMsRdpClient9.get_SecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6610448d822fe75082c225686dc6d809229a325f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150287"
---
# <a name="imstscaxsecuredsettings-property"></a><span data-ttu-id="ca154-124">IMsTscAx:: SecuredSettings (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ca154-124">IMsTscAx::SecuredSettings property</span></span>

<span data-ttu-id="ca154-125">Recupera un puntero de la interfaz [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="ca154-125">Retrieves an [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface pointer.</span></span>

<span data-ttu-id="ca154-126">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ca154-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca154-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ca154-127">Syntax</span></span>


```C++
HRESULT get_SecuredSettings(
  [out] IMsTscSecuredSettings **ppSecuredSettings
);
```



## <a name="property-value"></a><span data-ttu-id="ca154-128">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ca154-128">Property value</span></span>

<span data-ttu-id="ca154-129">Puntero a la interfaz [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="ca154-129">An [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ca154-130">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="ca154-130">Error codes</span></span>

<span data-ttu-id="ca154-131">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="ca154-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca154-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ca154-132">Remarks</span></span>

<span data-ttu-id="ca154-133">Si el control está hospedado en una página web y la zona de seguridad de la dirección URL de Internet Explorer actual no permite la recuperación de la dirección de la interfaz, este método devuelve **E \_ FAIL**.</span><span class="sxs-lookup"><span data-stu-id="ca154-133">If the control is hosted in a webpage and the current Internet Explorer URL security zone does not permit the retrieval of the interface address, this method returns **E\_FAIL**.</span></span>

<span data-ttu-id="ca154-134">Consulte [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) para obtener restricciones sobre la disponibilidad de la interfaz [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="ca154-134">Refer to [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md) for restrictions on the availability of the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface.</span></span>

<span data-ttu-id="ca154-135">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ca154-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca154-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca154-136">Requirements</span></span>



| <span data-ttu-id="ca154-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca154-137">Requirement</span></span> | <span data-ttu-id="ca154-138">Value</span><span class="sxs-lookup"><span data-stu-id="ca154-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca154-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca154-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ca154-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca154-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ca154-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca154-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ca154-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca154-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ca154-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ca154-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="ca154-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca154-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ca154-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ca154-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca154-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca154-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ca154-147">IID</span><span class="sxs-lookup"><span data-stu-id="ca154-147">IID</span></span><br/>                      | <span data-ttu-id="ca154-148">IID \_ IMsTscAx se define como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="ca154-148">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="ca154-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca154-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca154-150">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="ca154-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="ca154-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="ca154-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="ca154-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="ca154-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="ca154-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="ca154-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="ca154-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="ca154-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="ca154-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="ca154-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="ca154-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="ca154-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="ca154-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="ca154-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="ca154-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="ca154-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="ca154-159">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="ca154-159">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="ca154-160">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="ca154-160">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





