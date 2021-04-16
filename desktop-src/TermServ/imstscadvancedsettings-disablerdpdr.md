---
title: Propiedad DisableRdpdr de IMsTscAdvancedSettings
description: Especifica si está habilitada la redirección de la impresora y del portapapeles.
ms.assetid: 63e0e024-4792-4efe-a6c5-d122f8adcb0a
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DisableRdpdr
- Propiedad DisableRdpdr Servicios de Escritorio remoto, interfaz IMsTscAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsTscAdvancedSettings, propiedad DisableRdpdr
- Propiedad DisableRdpdr Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad DisableRdpdr
- Propiedad DisableRdpdr Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad DisableRdpdr
- Propiedad DisableRdpdr Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad DisableRdpdr
- Propiedad DisableRdpdr Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad DisableRdpdr
- Propiedad DisableRdpdr Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad DisableRdpdr
- Propiedad DisableRdpdr Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad DisableRdpdr
- Propiedad DisableRdpdr Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad DisableRdpdr
- Propiedad DisableRdpdr Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad DisableRdpdr
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.DisableRdpdr
- IMsTscAdvancedSettings.get_DisableRdpdr
- IMsTscAdvancedSettings.put_DisableRdpdr
- IMsRdpClientAdvancedSettings.DisableRdpdr
- IMsRdpClientAdvancedSettings.get_DisableRdpdr
- IMsRdpClientAdvancedSettings.put_DisableRdpdr
- IMsRdpClientAdvancedSettings2.DisableRdpdr
- IMsRdpClientAdvancedSettings2.get_DisableRdpdr
- IMsRdpClientAdvancedSettings2.put_DisableRdpdr
- IMsRdpClientAdvancedSettings3.DisableRdpdr
- IMsRdpClientAdvancedSettings3.get_DisableRdpdr
- IMsRdpClientAdvancedSettings3.put_DisableRdpdr
- IMsRdpClientAdvancedSettings4.DisableRdpdr
- IMsRdpClientAdvancedSettings4.get_DisableRdpdr
- IMsRdpClientAdvancedSettings4.put_DisableRdpdr
- IMsRdpClientAdvancedSettings5.DisableRdpdr
- IMsRdpClientAdvancedSettings5.get_DisableRdpdr
- IMsRdpClientAdvancedSettings5.put_DisableRdpdr
- IMsRdpClientAdvancedSettings6.DisableRdpdr
- IMsRdpClientAdvancedSettings6.get_DisableRdpdr
- IMsRdpClientAdvancedSettings6.put_DisableRdpdr
- IMsRdpClientAdvancedSettings7.DisableRdpdr
- IMsRdpClientAdvancedSettings7.get_DisableRdpdr
- IMsRdpClientAdvancedSettings7.put_DisableRdpdr
- IMsRdpClientAdvancedSettings8.DisableRdpdr
- IMsRdpClientAdvancedSettings8.get_DisableRdpdr
- IMsRdpClientAdvancedSettings8.put_DisableRdpdr
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0747f37cd5e85c62946c9b8e3a1587f736dd8af9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686025"
---
# <a name="imstscadvancedsettingsdisablerdpdr-property"></a><span data-ttu-id="7483e-122">IMsTscAdvancedSettings::D propiedad isableRdpdr</span><span class="sxs-lookup"><span data-stu-id="7483e-122">IMsTscAdvancedSettings::DisableRdpdr property</span></span>

<span data-ttu-id="7483e-123">Especifica si está habilitada la redirección de la impresora y del portapapeles.</span><span class="sxs-lookup"><span data-stu-id="7483e-123">Specifies whether printer and clipboard redirection is enabled.</span></span>

<span data-ttu-id="7483e-124">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="7483e-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7483e-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7483e-125">Syntax</span></span>


```C++
HRESULT put_DisableRdpdr(
  [in]  BOOL DisableRdpdr
);

HRESULT get_DisableRdpdr(
  [out] BOOL *pDisableRdpdr
);
```



## <a name="property-value"></a><span data-ttu-id="7483e-126">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7483e-126">Property value</span></span>

<span data-ttu-id="7483e-127">Establezca este parámetro en **true** para deshabilitar la redirección o en **false** para habilitar la redirección.</span><span class="sxs-lookup"><span data-stu-id="7483e-127">Set this parameter to **TRUE** to disable redirection or **FALSE** to enable redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7483e-128">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="7483e-128">Error codes</span></span>

<span data-ttu-id="7483e-129">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="7483e-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="7483e-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7483e-130">Remarks</span></span>

<span data-ttu-id="7483e-131">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="7483e-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7483e-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7483e-132">Requirements</span></span>



| <span data-ttu-id="7483e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="7483e-133">Requirement</span></span> | <span data-ttu-id="7483e-134">Value</span><span class="sxs-lookup"><span data-stu-id="7483e-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7483e-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7483e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="7483e-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7483e-136">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="7483e-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7483e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="7483e-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7483e-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="7483e-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7483e-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="7483e-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7483e-140"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="7483e-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7483e-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7483e-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7483e-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="7483e-143">IID</span><span class="sxs-lookup"><span data-stu-id="7483e-143">IID</span></span><br/>                      | <span data-ttu-id="7483e-144">IID \_ IMsTscAdvancedSettings se define como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="7483e-144">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7483e-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="7483e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7483e-146">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="7483e-146">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="7483e-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="7483e-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="7483e-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="7483e-148">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="7483e-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="7483e-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="7483e-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="7483e-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="7483e-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="7483e-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="7483e-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="7483e-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="7483e-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="7483e-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="7483e-154">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="7483e-154">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





