---
title: Propiedad ClearTextPassword de IMsRdpClientAdvancedSettings
description: Especifica la contraseña con la que se va a conectar. Para obtener más información, consulte la interfaz IMsTscNonScriptable.
ms.assetid: 9bb12dd6-f74c-488d-b6e5-4f96346610a1
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad ClearTextPassword
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.ClearTextPassword
- IMsRdpClientAdvancedSettings.put_ClearTextPassword
- IMsRdpClientAdvancedSettings2.ClearTextPassword
- IMsRdpClientAdvancedSettings2.put_ClearTextPassword
- IMsRdpClientAdvancedSettings3.ClearTextPassword
- IMsRdpClientAdvancedSettings3.put_ClearTextPassword
- IMsRdpClientAdvancedSettings4.ClearTextPassword
- IMsRdpClientAdvancedSettings4.put_ClearTextPassword
- IMsRdpClientAdvancedSettings5.ClearTextPassword
- IMsRdpClientAdvancedSettings5.put_ClearTextPassword
- IMsRdpClientAdvancedSettings6.ClearTextPassword
- IMsRdpClientAdvancedSettings6.put_ClearTextPassword
- IMsRdpClientAdvancedSettings7.ClearTextPassword
- IMsRdpClientAdvancedSettings7.put_ClearTextPassword
- IMsRdpClientAdvancedSettings8.ClearTextPassword
- IMsRdpClientAdvancedSettings8.put_ClearTextPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6943913193b2ecc9ed6ab31728d0274fb9ddd231
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490354"
---
# <a name="imsrdpclientadvancedsettingscleartextpassword-property"></a><span data-ttu-id="4bac6-121">IMsRdpClientAdvancedSettings:: ClearTextPassword (propiedad)</span><span class="sxs-lookup"><span data-stu-id="4bac6-121">IMsRdpClientAdvancedSettings::ClearTextPassword property</span></span>

<span data-ttu-id="4bac6-122">Especifica la contraseña con la que se va a conectar.</span><span class="sxs-lookup"><span data-stu-id="4bac6-122">Specifies the password with which to connect.</span></span> <span data-ttu-id="4bac6-123">Para obtener más información, consulte la interfaz [**IMsTscNonScriptable**](imstscnonscriptable-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="4bac6-123">For more information, see the [**IMsTscNonScriptable**](imstscnonscriptable-interface.md) interface.</span></span>

> [!Caution]  
> <span data-ttu-id="4bac6-124">Aunque el acceso con scripts a las contraseñas de texto no cifrado está disponible a través de esta propiedad, sigue siendo responsabilidad del desarrollador ejercitar cada precaución y mantener la seguridad al pasar contraseñas en sus aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="4bac6-124">Even though scriptable access to plaintext passwords is available through this property, it is still the responsibility of the developer to exercise every caution and maintain security when passing passwords in their applications.</span></span>

 

<span data-ttu-id="4bac6-125">Esta propiedad es de solo escritura.</span><span class="sxs-lookup"><span data-stu-id="4bac6-125">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bac6-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4bac6-126">Syntax</span></span>


```C++
HRESULT put_ClearTextPassword(
  [in] BSTR clearTextPassword
);
```



## <a name="property-value"></a><span data-ttu-id="4bac6-127">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4bac6-127">Property value</span></span>

<span data-ttu-id="4bac6-128">La contraseña nueva.</span><span class="sxs-lookup"><span data-stu-id="4bac6-128">The new password.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4bac6-129">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="4bac6-129">Error codes</span></span>

<span data-ttu-id="4bac6-130">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="4bac6-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bac6-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4bac6-131">Remarks</span></span>

<span data-ttu-id="4bac6-132">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="4bac6-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4bac6-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4bac6-133">Requirements</span></span>



| <span data-ttu-id="4bac6-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="4bac6-134">Requirement</span></span> | <span data-ttu-id="4bac6-135">Value</span><span class="sxs-lookup"><span data-stu-id="4bac6-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bac6-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bac6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4bac6-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4bac6-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="4bac6-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4bac6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4bac6-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4bac6-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="4bac6-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4bac6-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="4bac6-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bac6-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="4bac6-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4bac6-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bac6-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bac6-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="4bac6-144">IID</span><span class="sxs-lookup"><span data-stu-id="4bac6-144">IID</span></span><br/>                      | <span data-ttu-id="4bac6-145">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="4bac6-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4bac6-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="4bac6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bac6-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="4bac6-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="4bac6-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="4bac6-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="4bac6-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="4bac6-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="4bac6-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="4bac6-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="4bac6-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="4bac6-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="4bac6-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="4bac6-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="4bac6-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="4bac6-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="4bac6-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="4bac6-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





