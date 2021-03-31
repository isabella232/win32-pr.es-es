---
title: Propiedad ClearTextPassword de IMsTscNonScriptable
description: Establece la Escritorio remoto contraseña del control ActiveX en formato de texto simple.
ms.assetid: 93d35b10-5c92-4ab7-a32a-328ba6fcf16b
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto, interfaz IMsTscNonScriptable
- Servicios de Escritorio remoto de la interfaz IMsTscNonScriptable, propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable, propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable2, propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad ClearTextPassword
- Propiedad ClearTextPassword Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad ClearTextPassword
- Servicios de Escritorio remoto de la propiedad ClearTextPassword, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad ClearTextPassword
- Servicios de Escritorio remoto de la propiedad ClearTextPassword, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad ClearTextPassword
- Servicios de Escritorio remoto de la propiedad ClearTextPassword, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad ClearTextPassword
- Servicios de Escritorio remoto de la propiedad ClearTextPassword, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad ClearTextPassword
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ClearTextPassword
- IMsTscNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable.ClearTextPassword
- IMsRdpClientNonScriptable.put_ClearTextPassword
- IMsRdpClientNonScriptable2.ClearTextPassword
- IMsRdpClientNonScriptable2.put_ClearTextPassword
- IMsRdpClientNonScriptable3.ClearTextPassword
- IMsRdpClientNonScriptable3.put_ClearTextPassword
- IMsRdpClientNonScriptable4.ClearTextPassword
- IMsRdpClientNonScriptable4.put_ClearTextPassword
- IMsRdpClientNonScriptable5.ClearTextPassword
- IMsRdpClientNonScriptable5.put_ClearTextPassword
- MsRdpClient6.ClearTextPassword
- MsRdpClient7.ClearTextPassword
- MsRdpClient8.ClearTextPassword
- MsRdpClient9.ClearTextPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aad33d7d85c6a5c331efe8383815e079150fb65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803794"
---
# <a name="imstscnonscriptablecleartextpassword-property"></a><span data-ttu-id="d34eb-124">IMsTscNonScriptable:: ClearTextPassword (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d34eb-124">IMsTscNonScriptable::ClearTextPassword property</span></span>

<span data-ttu-id="d34eb-125">Establece la Escritorio remoto contraseña del control ActiveX en formato de texto simple.</span><span class="sxs-lookup"><span data-stu-id="d34eb-125">Sets the Remote Desktop ActiveX control password in plaintext format.</span></span>

<span data-ttu-id="d34eb-126">Esta propiedad es de solo escritura.</span><span class="sxs-lookup"><span data-stu-id="d34eb-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d34eb-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d34eb-127">Syntax</span></span>


```C++
HRESULT put_ClearTextPassword(
  [in] BSTR newClearTextPass
);
```



## <a name="property-value"></a><span data-ttu-id="d34eb-128">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d34eb-128">Property value</span></span>

<span data-ttu-id="d34eb-129">Contraseña que se va a usar para conectarse, especificada en formato de texto simple.</span><span class="sxs-lookup"><span data-stu-id="d34eb-129">The password to be used to connect, specified in plaintext format.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d34eb-130">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="d34eb-130">Error codes</span></span>

<span data-ttu-id="d34eb-131">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="d34eb-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d34eb-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d34eb-132">Remarks</span></span>

<span data-ttu-id="d34eb-133">La contraseña se pasa al servidor en el canal de comunicaciones RDP cifrado de forma segura.</span><span class="sxs-lookup"><span data-stu-id="d34eb-133">The password is passed to the server in the safely encrypted RDP communications channel.</span></span> <span data-ttu-id="d34eb-134">Después de establecer una contraseña de texto sin formato, no se puede recuperar en formato de texto no cifrado.</span><span class="sxs-lookup"><span data-stu-id="d34eb-134">After a plaintext password is set, it cannot be retrieved in plaintext format.</span></span>

<span data-ttu-id="d34eb-135">La propiedad **ClearTextPassword** solo se puede establecer cuando el control ActiveX escritorio remoto no está en estado conectado.</span><span class="sxs-lookup"><span data-stu-id="d34eb-135">The **ClearTextPassword** property can only be set when the Remote Desktop ActiveX control is not in the connected state.</span></span> <span data-ttu-id="d34eb-136">Si se establece esta propiedad, se producirá un error si el control está conectado.</span><span class="sxs-lookup"><span data-stu-id="d34eb-136">Setting this property fails if the control is connected.</span></span> <span data-ttu-id="d34eb-137">Para comprobar el estado conectado, recupere la propiedad [**IMsTscAx:: Connected**](imstscax-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="d34eb-137">To check for the connected state, retrieve the [**IMsTscAx::Connected**](imstscax-connected.md) property.</span></span>

<span data-ttu-id="d34eb-138">También puede llamar a este método para establecer una contraseña de texto no cifrado antes de convertirla en una contraseña codificada portable o en una contraseña codificada binaria (no portable).</span><span class="sxs-lookup"><span data-stu-id="d34eb-138">You can also call this method to set a plaintext password before converting it to either a portable encoded password or to a binary (nonportable) encoded password.</span></span> <span data-ttu-id="d34eb-139">Sin embargo, tenga en cuenta que las contraseñas codificadas no se deben considerar cifradas de forma segura.</span><span class="sxs-lookup"><span data-stu-id="d34eb-139">Note however that encoded passwords should not be considered securely encrypted.</span></span>

<span data-ttu-id="d34eb-140">Si llama primero a este método para establecer una contraseña en formato de texto simple, puede convertir la contraseña al formato codificado.</span><span class="sxs-lookup"><span data-stu-id="d34eb-140">If you first call this method to set a password in plaintext format, you can then convert the password to encoded format.</span></span>

<span data-ttu-id="d34eb-141">**Para convertir una contraseña de texto no cifrado en formato codificado**</span><span class="sxs-lookup"><span data-stu-id="d34eb-141">**To convert a plaintext password to encoded format**</span></span>

1.  <span data-ttu-id="d34eb-142">Establezca la contraseña en formato de texto no cifrado en la propiedad **ClearTextPassword** .</span><span class="sxs-lookup"><span data-stu-id="d34eb-142">Set the password in plaintext format in the **ClearTextPassword** property.</span></span>
2.  <span data-ttu-id="d34eb-143">Para recuperar la contraseña en formato codificado binario (no portable), recupere la propiedad [**BinaryPassword**](imstscnonscriptable-binarypassword.md) y las propiedades [**BinarySalt**](imstscnonscriptable-binarysalt.md) .</span><span class="sxs-lookup"><span data-stu-id="d34eb-143">To retrieve the password in binary (nonportable) encoded format, retrieve the [**BinaryPassword**](imstscnonscriptable-binarypassword.md) property and the [**BinarySalt**](imstscnonscriptable-binarysalt.md) properties.</span></span> <span data-ttu-id="d34eb-144">Tanto la parte de la contraseña codificada como la parte del valor Salt son necesarias para establecer una contraseña en formato codificado binario.</span><span class="sxs-lookup"><span data-stu-id="d34eb-144">Both the encoded password part and the salt part are required to set a password in binary encoded format.</span></span>
3.  <span data-ttu-id="d34eb-145">Para recuperar la contraseña en formato codificado portable, recupere el método [**PortablePassword**](imstscnonscriptable-portablepassword.md) y las propiedades [**PortableSalt**](imstscnonscriptable-portablesalt.md) .</span><span class="sxs-lookup"><span data-stu-id="d34eb-145">To retrieve the password in portable encoded format, retrieve the [**PortablePassword**](imstscnonscriptable-portablepassword.md) method and the [**PortableSalt**](imstscnonscriptable-portablesalt.md) properties.</span></span> <span data-ttu-id="d34eb-146">Ambas partes son necesarias para establecer una contraseña en formato codificado portátil.</span><span class="sxs-lookup"><span data-stu-id="d34eb-146">Both parts are required to set a password in portable encoded format.</span></span>

<span data-ttu-id="d34eb-147">Después de seguir los tres pasos anteriores, puede establecer la contraseña en formato codificado estableciendo las propiedades [**BinaryPassword**](imstscnonscriptable-binarypassword.md) y [**BinarySalt**](imstscnonscriptable-binarysalt.md) , o [**PortablePassword**](imstscnonscriptable-portablepassword.md) y [**PortableSalt**](imstscnonscriptable-portablesalt.md) .</span><span class="sxs-lookup"><span data-stu-id="d34eb-147">After following the preceding three steps, you can set the password in encoded format by setting the [**BinaryPassword**](imstscnonscriptable-binarypassword.md) and [**BinarySalt**](imstscnonscriptable-binarysalt.md) properties, or [**PortablePassword**](imstscnonscriptable-portablepassword.md) and [**PortableSalt**](imstscnonscriptable-portablesalt.md) properties.</span></span> <span data-ttu-id="d34eb-148">Ambas partes son obligatorias.</span><span class="sxs-lookup"><span data-stu-id="d34eb-148">Both parts are required.</span></span>

<span data-ttu-id="d34eb-149">Para habilitar el inicio de sesión automático, también debe establecer las propiedades de [**nombre de usuario**](imstscax-username.md) y [**dominio**](imstscax-domain.md) .</span><span class="sxs-lookup"><span data-stu-id="d34eb-149">To enable automatic logon, you must also set the [**UserName**](imstscax-username.md) and [**Domain**](imstscax-domain.md) properties.</span></span> <span data-ttu-id="d34eb-150">Si la contraseña no puede autenticar al usuario, el cuadro de diálogo de inicio de sesión de Windows se muestra en el servidor para pedir la contraseña al usuario.</span><span class="sxs-lookup"><span data-stu-id="d34eb-150">If the password fails to authenticate the user, the Windows Logon dialog box is displayed at the server to prompt the user for the password.</span></span>

<span data-ttu-id="d34eb-151">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d34eb-151">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d34eb-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d34eb-152">Requirements</span></span>



| <span data-ttu-id="d34eb-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="d34eb-153">Requirement</span></span> | <span data-ttu-id="d34eb-154">Value</span><span class="sxs-lookup"><span data-stu-id="d34eb-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d34eb-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d34eb-155">Minimum supported client</span></span><br/> | <span data-ttu-id="d34eb-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d34eb-156">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d34eb-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d34eb-157">Minimum supported server</span></span><br/> | <span data-ttu-id="d34eb-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d34eb-158">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d34eb-159">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d34eb-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="d34eb-160"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d34eb-160"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d34eb-161">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d34eb-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d34eb-162"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d34eb-162"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d34eb-163">IID</span><span class="sxs-lookup"><span data-stu-id="d34eb-163">IID</span></span><br/>                      | <span data-ttu-id="d34eb-164">IID \_ IMsTscNonScriptable se define como c1e6743a-41c1-4a74-832A-0dd06c1c7a0e</span><span class="sxs-lookup"><span data-stu-id="d34eb-164">IID\_IMsTscNonScriptable is defined as c1e6743a-41c1-4a74-832a-0dd06c1c7a0e</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d34eb-165">Vea también</span><span class="sxs-lookup"><span data-stu-id="d34eb-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d34eb-166">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="d34eb-166">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="d34eb-167">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="d34eb-167">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="d34eb-168">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="d34eb-168">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="d34eb-169">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="d34eb-169">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="d34eb-170">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="d34eb-170">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="d34eb-171">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="d34eb-171">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





