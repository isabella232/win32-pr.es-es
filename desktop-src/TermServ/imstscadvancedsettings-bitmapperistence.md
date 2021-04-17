---
title: Propiedad BitmapPeristence de IMsTscAdvancedSettings
description: Especifica si está habilitado el almacenamiento en caché de mapas de bits.
ms.assetid: 8cabeae8-26bc-4d33-82cc-47bb201d79b6
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad BitmapPeristence
- Propiedad BitmapPeristence Servicios de Escritorio remoto, interfaz IMsTscAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsTscAdvancedSettings, propiedad BitmapPeristence
- Propiedad BitmapPeristence Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad BitmapPeristence
- Propiedad BitmapPeristence Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad BitmapPeristence
- Propiedad BitmapPeristence Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad BitmapPeristence
- Propiedad BitmapPeristence Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad BitmapPeristence
- Propiedad BitmapPeristence Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad BitmapPeristence
- Propiedad BitmapPeristence Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad BitmapPeristence
- Propiedad BitmapPeristence Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad BitmapPeristence
- Propiedad BitmapPeristence Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad BitmapPeristence
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.BitmapPeristence
- IMsTscAdvancedSettings.get_BitmapPeristence
- IMsTscAdvancedSettings.put_BitmapPeristence
- IMsRdpClientAdvancedSettings.BitmapPeristence
- IMsRdpClientAdvancedSettings.get_BitmapPeristence
- IMsRdpClientAdvancedSettings.put_BitmapPeristence
- IMsRdpClientAdvancedSettings2.BitmapPeristence
- IMsRdpClientAdvancedSettings2.get_BitmapPeristence
- IMsRdpClientAdvancedSettings2.put_BitmapPeristence
- IMsRdpClientAdvancedSettings3.BitmapPeristence
- IMsRdpClientAdvancedSettings3.get_BitmapPeristence
- IMsRdpClientAdvancedSettings3.put_BitmapPeristence
- IMsRdpClientAdvancedSettings4.BitmapPeristence
- IMsRdpClientAdvancedSettings4.get_BitmapPeristence
- IMsRdpClientAdvancedSettings4.put_BitmapPeristence
- IMsRdpClientAdvancedSettings5.BitmapPeristence
- IMsRdpClientAdvancedSettings5.get_BitmapPeristence
- IMsRdpClientAdvancedSettings5.put_BitmapPeristence
- IMsRdpClientAdvancedSettings6.BitmapPeristence
- IMsRdpClientAdvancedSettings6.get_BitmapPeristence
- IMsRdpClientAdvancedSettings6.put_BitmapPeristence
- IMsRdpClientAdvancedSettings7.BitmapPeristence
- IMsRdpClientAdvancedSettings7.get_BitmapPeristence
- IMsRdpClientAdvancedSettings7.put_BitmapPeristence
- IMsRdpClientAdvancedSettings8.BitmapPeristence
- IMsRdpClientAdvancedSettings8.get_BitmapPeristence
- IMsRdpClientAdvancedSettings8.put_BitmapPeristence
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a543d24b200d8fa484939d5ffeabfeeac0b5f73f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492923"
---
# <a name="imstscadvancedsettingsbitmapperistence-property"></a><span data-ttu-id="ef875-122">IMsTscAdvancedSettings:: BitmapPeristence (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ef875-122">IMsTscAdvancedSettings::BitmapPeristence property</span></span>

<span data-ttu-id="ef875-123">Especifica si está habilitado el almacenamiento en caché de mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="ef875-123">Specifies whether bitmap caching is enabled.</span></span> <span data-ttu-id="ef875-124">El almacenamiento en caché persistente puede mejorar el rendimiento pero requiere espacio adicional en disco.</span><span class="sxs-lookup"><span data-stu-id="ef875-124">Persistent caching can improve performance but requires additional disk space.</span></span>

> [!Note]  
> <span data-ttu-id="ef875-125">El error ortográfico en el nombre de la propiedad y su parámetro está en la versión de lanzamiento del control.</span><span class="sxs-lookup"><span data-stu-id="ef875-125">The spelling error in the name of the property and its parameter is in the released version of the control.</span></span>

 

<span data-ttu-id="ef875-126">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ef875-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef875-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ef875-127">Syntax</span></span>


```C++
HRESULT put_BitmapPeristence(
  [in]  LONG bitmapPeristence
);

HRESULT get_BitmapPeristence(
  [out] LONG *pbitmapPeristence
);
```



## <a name="property-value"></a><span data-ttu-id="ef875-128">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ef875-128">Property value</span></span>

<span data-ttu-id="ef875-129">Establezca este parámetro en 0 para deshabilitar el almacenamiento en caché o un valor distinto de cero para habilitar el almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="ef875-129">Set this parameter to 0 to disable caching or a nonzero value to enable caching.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ef875-130">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="ef875-130">Error codes</span></span>

<span data-ttu-id="ef875-131">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="ef875-131">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef875-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef875-132">Remarks</span></span>

<span data-ttu-id="ef875-133">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ef875-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef875-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef875-134">Requirements</span></span>



| <span data-ttu-id="ef875-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef875-135">Requirement</span></span> | <span data-ttu-id="ef875-136">Value</span><span class="sxs-lookup"><span data-stu-id="ef875-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef875-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef875-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ef875-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ef875-138">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="ef875-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef875-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ef875-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ef875-140">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="ef875-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ef875-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="ef875-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef875-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="ef875-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ef875-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef875-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef875-144"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="ef875-145">IID</span><span class="sxs-lookup"><span data-stu-id="ef875-145">IID</span></span><br/>                      | <span data-ttu-id="ef875-146">IID \_ IMsTscAdvancedSettings se define como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="ef875-146">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ef875-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef875-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef875-148">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="ef875-148">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="ef875-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="ef875-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="ef875-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="ef875-150">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="ef875-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="ef875-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="ef875-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="ef875-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="ef875-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ef875-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="ef875-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ef875-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ef875-155">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ef875-155">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ef875-156">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="ef875-156">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





