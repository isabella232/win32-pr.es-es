---
title: Propiedad CipherStrength de IMsTscAx
description: Recupera la intensidad máxima de cifrado del control actual.
ms.assetid: 94efe3e5-4074-4187-b58a-b812f37f3622
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad CipherStrength
- Propiedad CipherStrength Servicios de Escritorio remoto, interfaz IMsTscAx
- Servicios de Escritorio remoto de la interfaz IMsTscAx, propiedad CipherStrength
- Propiedad CipherStrength Servicios de Escritorio remoto, interfaz IMsRdpClient
- Servicios de Escritorio remoto de la interfaz IMsRdpClient, propiedad CipherStrength
- Propiedad CipherStrength Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Servicios de Escritorio remoto de la interfaz IMsRdpClient2, propiedad CipherStrength
- Propiedad CipherStrength Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Servicios de Escritorio remoto de la interfaz IMsRdpClient3, propiedad CipherStrength
- Propiedad CipherStrength Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Servicios de Escritorio remoto de la interfaz IMsRdpClient4, propiedad CipherStrength
- Propiedad CipherStrength Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad CipherStrength
- Propiedad CipherStrength Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad CipherStrength
- Propiedad CipherStrength Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad CipherStrength
- Propiedad CipherStrength Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad CipherStrength
- Propiedad CipherStrength Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad CipherStrength
topic_type:
- apiref
api_name:
- IMsTscAx.CipherStrength
- IMsTscAx.get_CipherStrength
- IMsRdpClient.CipherStrength
- IMsRdpClient.get_CipherStrength
- IMsRdpClient2.CipherStrength
- IMsRdpClient2.get_CipherStrength
- IMsRdpClient3.CipherStrength
- IMsRdpClient3.get_CipherStrength
- IMsRdpClient4.CipherStrength
- IMsRdpClient4.get_CipherStrength
- IMsRdpClient5.CipherStrength
- IMsRdpClient5.get_CipherStrength
- IMsRdpClient6.CipherStrength
- IMsRdpClient6.get_CipherStrength
- IMsRdpClient7.CipherStrength
- IMsRdpClient7.get_CipherStrength
- IMsRdpClient8.CipherStrength
- IMsRdpClient8.get_CipherStrength
- IMsRdpClient9.CipherStrength
- IMsRdpClient9.get_CipherStrength
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401cf3796d349aaa6764eae46a371a9d485f763c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422000"
---
# <a name="imstscaxcipherstrength-property"></a><span data-ttu-id="174a1-124">IMsTscAx:: CipherStrength (propiedad)</span><span class="sxs-lookup"><span data-stu-id="174a1-124">IMsTscAx::CipherStrength property</span></span>

<span data-ttu-id="174a1-125">Recupera la intensidad máxima de cifrado del control actual.</span><span class="sxs-lookup"><span data-stu-id="174a1-125">Retrieves the maximum encryption strength of the current control.</span></span>

<span data-ttu-id="174a1-126">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="174a1-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="174a1-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="174a1-127">Syntax</span></span>


```C++
HRESULT get_CipherStrength(
  [out] LONG *pCipherStrength
);
```



## <a name="property-value"></a><span data-ttu-id="174a1-128">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="174a1-128">Property value</span></span>

<span data-ttu-id="174a1-129">La intensidad de cifrado.</span><span class="sxs-lookup"><span data-stu-id="174a1-129">The encryption strength.</span></span>

## <a name="error-codes"></a><span data-ttu-id="174a1-130">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="174a1-130">Error codes</span></span>

<span data-ttu-id="174a1-131">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="174a1-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="174a1-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="174a1-132">Remarks</span></span>

<span data-ttu-id="174a1-133">Por Conexión web a Escritorio remoto, la intensidad de cifrado siempre es 128 porque el control ActiveX Escritorio remoto admite el cifrado hasta 128 bits inclusive.</span><span class="sxs-lookup"><span data-stu-id="174a1-133">For Remote Desktop Web Connection, the cipher strength is always 128 because the Remote Desktop ActiveX control supports encryption up to and including 128 bits.</span></span> <span data-ttu-id="174a1-134">El control de 128 bits todavía puede conectarse al cifrado de 56 bits Escritorio remoto los servidores host de sesión de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="174a1-134">The 128-bit control can still connect to 56 bit encryption Remote Desktop Session Host (RD Session Host) servers.</span></span>

<span data-ttu-id="174a1-135">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="174a1-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="174a1-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="174a1-136">Requirements</span></span>



| <span data-ttu-id="174a1-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="174a1-137">Requirement</span></span> | <span data-ttu-id="174a1-138">Value</span><span class="sxs-lookup"><span data-stu-id="174a1-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="174a1-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="174a1-139">Minimum supported client</span></span><br/> | <span data-ttu-id="174a1-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="174a1-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="174a1-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="174a1-141">Minimum supported server</span></span><br/> | <span data-ttu-id="174a1-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="174a1-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="174a1-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="174a1-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="174a1-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="174a1-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="174a1-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="174a1-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="174a1-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="174a1-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="174a1-147">IID</span><span class="sxs-lookup"><span data-stu-id="174a1-147">IID</span></span><br/>                      | <span data-ttu-id="174a1-148">IID \_ IMsTscAx se define como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="174a1-148">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="174a1-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="174a1-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="174a1-150">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="174a1-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="174a1-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="174a1-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="174a1-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="174a1-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="174a1-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="174a1-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="174a1-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="174a1-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="174a1-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="174a1-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="174a1-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="174a1-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="174a1-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="174a1-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="174a1-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="174a1-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="174a1-159">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="174a1-159">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





