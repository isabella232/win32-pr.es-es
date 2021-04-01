---
title: IMsTscAdvancedSettings propiedad Compress
description: Especifica si está habilitada la compresión.
ms.assetid: 274774b3-0442-4a46-95f8-7857f885bfdb
ms.tgt_platform: multiple
keywords:
- Propiedad Compress Servicios de Escritorio remoto
- Propiedad Compress Servicios de Escritorio remoto, interfaz IMsTscAdvancedSettings
- Interfaz IMsTscAdvancedSettings Servicios de Escritorio remoto, propiedad Compress
- Propiedad Compress Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Interfaz IMsRdpClientAdvancedSettings Servicios de Escritorio remoto, propiedad Compress
- Propiedad Compress Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Interfaz IMsRdpClientAdvancedSettings2 Servicios de Escritorio remoto, propiedad Compress
- Propiedad Compress Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Interfaz IMsRdpClientAdvancedSettings3 Servicios de Escritorio remoto, propiedad Compress
- Propiedad Compress Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Interfaz IMsRdpClientAdvancedSettings4 Servicios de Escritorio remoto, propiedad Compress
- Propiedad Compress Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Interfaz IMsRdpClientAdvancedSettings5 Servicios de Escritorio remoto, propiedad Compress
- Propiedad Compress Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Interfaz IMsRdpClientAdvancedSettings6 Servicios de Escritorio remoto, propiedad Compress
- Propiedad Compress Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Interfaz IMsRdpClientAdvancedSettings7 Servicios de Escritorio remoto, propiedad Compress
- Propiedad Compress Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Interfaz IMsRdpClientAdvancedSettings8 Servicios de Escritorio remoto, propiedad Compress
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.Compress
- IMsTscAdvancedSettings.get_Compress
- IMsTscAdvancedSettings.put_Compress
- IMsRdpClientAdvancedSettings.Compress
- IMsRdpClientAdvancedSettings.get_Compress
- IMsRdpClientAdvancedSettings.put_Compress
- IMsRdpClientAdvancedSettings2.Compress
- IMsRdpClientAdvancedSettings2.get_Compress
- IMsRdpClientAdvancedSettings2.put_Compress
- IMsRdpClientAdvancedSettings3.Compress
- IMsRdpClientAdvancedSettings3.get_Compress
- IMsRdpClientAdvancedSettings3.put_Compress
- IMsRdpClientAdvancedSettings4.Compress
- IMsRdpClientAdvancedSettings4.get_Compress
- IMsRdpClientAdvancedSettings4.put_Compress
- IMsRdpClientAdvancedSettings5.Compress
- IMsRdpClientAdvancedSettings5.get_Compress
- IMsRdpClientAdvancedSettings5.put_Compress
- IMsRdpClientAdvancedSettings6.Compress
- IMsRdpClientAdvancedSettings6.get_Compress
- IMsRdpClientAdvancedSettings6.put_Compress
- IMsRdpClientAdvancedSettings7.Compress
- IMsRdpClientAdvancedSettings7.get_Compress
- IMsRdpClientAdvancedSettings7.put_Compress
- IMsRdpClientAdvancedSettings8.Compress
- IMsRdpClientAdvancedSettings8.get_Compress
- IMsRdpClientAdvancedSettings8.put_Compress
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c588784d9b06bd2e8e1605a96c8aa9fd157c10eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996594"
---
# <a name="imstscadvancedsettingscompress-property"></a><span data-ttu-id="a02c0-122">IMsTscAdvancedSettings:: compress (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a02c0-122">IMsTscAdvancedSettings::Compress property</span></span>

<span data-ttu-id="a02c0-123">Especifica si está habilitada la compresión.</span><span class="sxs-lookup"><span data-stu-id="a02c0-123">Specifies whether compression is enabled.</span></span>

<span data-ttu-id="a02c0-124">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a02c0-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a02c0-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a02c0-125">Syntax</span></span>


```C++
HRESULT put_Compress(
  [in]  LONG compress
);

HRESULT get_Compress(
  [out] LONG *pcompress
);
```



## <a name="property-value"></a><span data-ttu-id="a02c0-126">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a02c0-126">Property value</span></span>

<span data-ttu-id="a02c0-127">Establezca este parámetro en 0 para deshabilitar la compresión o un valor distinto de cero para habilitar la compresión.</span><span class="sxs-lookup"><span data-stu-id="a02c0-127">Set this parameter to 0 to disable compression or a nonzero value to enable compression.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a02c0-128">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="a02c0-128">Error codes</span></span>

<span data-ttu-id="a02c0-129">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="a02c0-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a02c0-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a02c0-130">Remarks</span></span>

<span data-ttu-id="a02c0-131">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a02c0-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a02c0-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a02c0-132">Requirements</span></span>



| <span data-ttu-id="a02c0-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a02c0-133">Requirement</span></span> | <span data-ttu-id="a02c0-134">Value</span><span class="sxs-lookup"><span data-stu-id="a02c0-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a02c0-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a02c0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="a02c0-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a02c0-136">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="a02c0-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a02c0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="a02c0-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a02c0-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="a02c0-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a02c0-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="a02c0-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a02c0-140"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="a02c0-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a02c0-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a02c0-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a02c0-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="a02c0-143">IID</span><span class="sxs-lookup"><span data-stu-id="a02c0-143">IID</span></span><br/>                      | <span data-ttu-id="a02c0-144">IID \_ IMsTscAdvancedSettings se define como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="a02c0-144">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a02c0-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="a02c0-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a02c0-146">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="a02c0-146">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="a02c0-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="a02c0-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="a02c0-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="a02c0-148">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="a02c0-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="a02c0-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="a02c0-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="a02c0-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="a02c0-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="a02c0-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="a02c0-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="a02c0-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="a02c0-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="a02c0-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="a02c0-154">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="a02c0-154">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





