---
title: Propiedad AdvancedSettings de IMsTscAx
description: Recupera un puntero de la interfaz IMsTscAdvancedSettings.
ms.assetid: 1c0e2216-0c65-48ad-b0f6-3a766c8fa44e
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad AdvancedSettings
- Propiedad AdvancedSettings Servicios de Escritorio remoto, interfaz IMsTscAx
- Servicios de Escritorio remoto de la interfaz IMsTscAx, propiedad AdvancedSettings
- Propiedad AdvancedSettings Servicios de Escritorio remoto, interfaz IMsRdpClient
- Servicios de Escritorio remoto de la interfaz IMsRdpClient, propiedad AdvancedSettings
- Propiedad AdvancedSettings Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Servicios de Escritorio remoto de la interfaz IMsRdpClient2, propiedad AdvancedSettings
- Propiedad AdvancedSettings Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Servicios de Escritorio remoto de la interfaz IMsRdpClient3, propiedad AdvancedSettings
- Propiedad AdvancedSettings Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Servicios de Escritorio remoto de la interfaz IMsRdpClient4, propiedad AdvancedSettings
- Propiedad AdvancedSettings Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad AdvancedSettings
- Propiedad AdvancedSettings Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad AdvancedSettings
- Propiedad AdvancedSettings Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad AdvancedSettings
- Propiedad AdvancedSettings Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad AdvancedSettings
- Propiedad AdvancedSettings Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad AdvancedSettings
topic_type:
- apiref
api_name:
- IMsTscAx.AdvancedSettings
- IMsTscAx.get_AdvancedSettings
- IMsRdpClient.AdvancedSettings
- IMsRdpClient.get_AdvancedSettings
- IMsRdpClient2.AdvancedSettings
- IMsRdpClient2.get_AdvancedSettings
- IMsRdpClient3.AdvancedSettings
- IMsRdpClient3.get_AdvancedSettings
- IMsRdpClient4.AdvancedSettings
- IMsRdpClient4.get_AdvancedSettings
- IMsRdpClient5.AdvancedSettings
- IMsRdpClient5.get_AdvancedSettings
- IMsRdpClient6.AdvancedSettings
- IMsRdpClient6.get_AdvancedSettings
- IMsRdpClient7.AdvancedSettings
- IMsRdpClient7.get_AdvancedSettings
- IMsRdpClient8.AdvancedSettings
- IMsRdpClient8.get_AdvancedSettings
- IMsRdpClient9.AdvancedSettings
- IMsRdpClient9.get_AdvancedSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98bb6b1d581704a0638a47310004777f020ce9bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996384"
---
# <a name="imstscaxadvancedsettings-property"></a><span data-ttu-id="7e090-124">IMsTscAx:: AdvancedSettings (propiedad)</span><span class="sxs-lookup"><span data-stu-id="7e090-124">IMsTscAx::AdvancedSettings property</span></span>

<span data-ttu-id="7e090-125">Recupera un puntero de la interfaz [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="7e090-125">Retrieves an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span>

<span data-ttu-id="7e090-126">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7e090-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e090-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e090-127">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings(
  [out] IMsTscAdvancedSettings **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="7e090-128">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7e090-128">Property value</span></span>

<span data-ttu-id="7e090-129">Puntero a la interfaz [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="7e090-129">An [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7e090-130">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="7e090-130">Error codes</span></span>

<span data-ttu-id="7e090-131">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="7e090-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e090-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e090-132">Remarks</span></span>

<span data-ttu-id="7e090-133">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="7e090-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e090-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e090-134">Requirements</span></span>



| <span data-ttu-id="7e090-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e090-135">Requirement</span></span> | <span data-ttu-id="7e090-136">Value</span><span class="sxs-lookup"><span data-stu-id="7e090-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e090-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e090-137">Minimum supported client</span></span><br/> | <span data-ttu-id="7e090-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7e090-138">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7e090-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e090-139">Minimum supported server</span></span><br/> | <span data-ttu-id="7e090-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e090-140">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7e090-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7e090-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="7e090-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e090-142"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7e090-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7e090-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e090-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e090-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="7e090-145">IID</span><span class="sxs-lookup"><span data-stu-id="7e090-145">IID</span></span><br/>                      | <span data-ttu-id="7e090-146">IID \_ IMsTscAx se define como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="7e090-146">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="7e090-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e090-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e090-148">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="7e090-148">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="7e090-149">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="7e090-149">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="7e090-150">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="7e090-150">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="7e090-151">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="7e090-151">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="7e090-152">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="7e090-152">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="7e090-153">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="7e090-153">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="7e090-154">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="7e090-154">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="7e090-155">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="7e090-155">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="7e090-156">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="7e090-156">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="7e090-157">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="7e090-157">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





