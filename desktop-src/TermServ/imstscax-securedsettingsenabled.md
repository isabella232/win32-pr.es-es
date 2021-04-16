---
title: Propiedad SecuredSettingsEnabled de IMsTscAx
description: Indica si la interfaz IMsTscSecuredSettings está disponible. Es decir, si la página web que contiene el control está actualmente en una de las zonas de seguridad de direcciones URL permitidas de Internet Explorer.
ms.assetid: 0747eab0-9d62-4c10-b02d-fc65ca2f752e
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad SecuredSettingsEnabled
- Propiedad SecuredSettingsEnabled Servicios de Escritorio remoto, interfaz IMsTscAx
- Servicios de Escritorio remoto de la interfaz IMsTscAx, propiedad SecuredSettingsEnabled
- Propiedad SecuredSettingsEnabled Servicios de Escritorio remoto, interfaz IMsRdpClient
- Servicios de Escritorio remoto de la interfaz IMsRdpClient, propiedad SecuredSettingsEnabled
- Propiedad SecuredSettingsEnabled Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Servicios de Escritorio remoto de la interfaz IMsRdpClient2, propiedad SecuredSettingsEnabled
- Propiedad SecuredSettingsEnabled Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Servicios de Escritorio remoto de la interfaz IMsRdpClient3, propiedad SecuredSettingsEnabled
- Propiedad SecuredSettingsEnabled Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Servicios de Escritorio remoto de la interfaz IMsRdpClient4, propiedad SecuredSettingsEnabled
- Propiedad SecuredSettingsEnabled Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad SecuredSettingsEnabled
- Propiedad SecuredSettingsEnabled Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad SecuredSettingsEnabled
- Propiedad SecuredSettingsEnabled Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad SecuredSettingsEnabled
- Propiedad SecuredSettingsEnabled Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad SecuredSettingsEnabled
- Propiedad SecuredSettingsEnabled Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad SecuredSettingsEnabled
topic_type:
- apiref
api_name:
- IMsTscAx.SecuredSettingsEnabled
- IMsTscAx.get_SecuredSettingsEnabled
- IMsRdpClient.SecuredSettingsEnabled
- IMsRdpClient.get_SecuredSettingsEnabled
- IMsRdpClient2.SecuredSettingsEnabled
- IMsRdpClient2.get_SecuredSettingsEnabled
- IMsRdpClient3.SecuredSettingsEnabled
- IMsRdpClient3.get_SecuredSettingsEnabled
- IMsRdpClient4.SecuredSettingsEnabled
- IMsRdpClient4.get_SecuredSettingsEnabled
- IMsRdpClient5.SecuredSettingsEnabled
- IMsRdpClient5.get_SecuredSettingsEnabled
- IMsRdpClient6.SecuredSettingsEnabled
- IMsRdpClient6.get_SecuredSettingsEnabled
- IMsRdpClient7.SecuredSettingsEnabled
- IMsRdpClient7.get_SecuredSettingsEnabled
- IMsRdpClient8.SecuredSettingsEnabled
- IMsRdpClient8.get_SecuredSettingsEnabled
- IMsRdpClient9.SecuredSettingsEnabled
- IMsRdpClient9.get_SecuredSettingsEnabled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de0601ac64ab0ca55f3d92ec460861a4347f70b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676928"
---
# <a name="imstscaxsecuredsettingsenabled-property"></a><span data-ttu-id="6c925-125">IMsTscAx:: SecuredSettingsEnabled (propiedad)</span><span class="sxs-lookup"><span data-stu-id="6c925-125">IMsTscAx::SecuredSettingsEnabled property</span></span>

<span data-ttu-id="6c925-126">Indica si la interfaz [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) está disponible.</span><span class="sxs-lookup"><span data-stu-id="6c925-126">Indicates whether the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface is available.</span></span> <span data-ttu-id="6c925-127">Es decir, si la página web que contiene el control está actualmente en una de las zonas de seguridad de direcciones URL permitidas de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="6c925-127">That is, whether the webpage containing the control is currently in one of the allowed Internet Explorer URL security zones.</span></span>

<span data-ttu-id="6c925-128">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6c925-128">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c925-129">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c925-129">Syntax</span></span>


```C++
HRESULT get_SecuredSettingsEnabled(
  [out] BOOL *pSecuredSettingsEnabled
);
```



## <a name="property-value"></a><span data-ttu-id="6c925-130">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="6c925-130">Property value</span></span>

<span data-ttu-id="6c925-131">El valor de este parámetro es **true** si la interfaz está disponible y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6c925-131">The value of this parameter is **TRUE** if the interface is available, and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6c925-132">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="6c925-132">Error codes</span></span>

<span data-ttu-id="6c925-133">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="6c925-133">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c925-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c925-134">Remarks</span></span>

<span data-ttu-id="6c925-135">Utilice este método para consultar si la interfaz [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) está disponible antes de recuperar la propiedad [**SecuredSettings**](imstscax-securedsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="6c925-135">Use this method to query whether the [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) interface is available before retrieving the [**SecuredSettings**](imstscax-securedsettings.md) property.</span></span>

<span data-ttu-id="6c925-136">Consulte [proporcionar seguridad de cliente RDP](providing-for-rdp-client-security.md) para obtener una lista de zonas de seguridad de direcciones URL restringidas.</span><span class="sxs-lookup"><span data-stu-id="6c925-136">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for a list of restricted URL security zones.</span></span>

<span data-ttu-id="6c925-137">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6c925-137">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c925-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c925-138">Requirements</span></span>



| <span data-ttu-id="6c925-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c925-139">Requirement</span></span> | <span data-ttu-id="6c925-140">Value</span><span class="sxs-lookup"><span data-stu-id="6c925-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c925-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c925-141">Minimum supported client</span></span><br/> | <span data-ttu-id="6c925-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c925-142">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6c925-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c925-143">Minimum supported server</span></span><br/> | <span data-ttu-id="6c925-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c925-144">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6c925-145">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6c925-145">Type library</span></span><br/>             | <dl> <span data-ttu-id="6c925-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c925-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6c925-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6c925-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c925-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c925-148"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="6c925-149">IID</span><span class="sxs-lookup"><span data-stu-id="6c925-149">IID</span></span><br/>                      | <span data-ttu-id="6c925-150">IID \_ IMsTscAx se define como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="6c925-150">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="6c925-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c925-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c925-152">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="6c925-152">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="6c925-153">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="6c925-153">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="6c925-154">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="6c925-154">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="6c925-155">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="6c925-155">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="6c925-156">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="6c925-156">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="6c925-157">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="6c925-157">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="6c925-158">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="6c925-158">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="6c925-159">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="6c925-159">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="6c925-160">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="6c925-160">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="6c925-161">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="6c925-161">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="6c925-162">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="6c925-162">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





