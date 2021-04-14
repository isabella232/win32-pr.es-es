---
title: Propiedad BitmapPersistence de IMsRdpClientAdvancedSettings
description: Especifica si se debe usar el almacenamiento en caché de mapas de bits persistente. El almacenamiento en caché persistente puede mejorar el rendimiento pero requiere espacio adicional en disco.
ms.assetid: ffaa9277-9dd7-4b2a-9de5-009b7e8766bc
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad BitmapPersistence
- Propiedad BitmapPersistence Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad BitmapPersistence
- Propiedad BitmapPersistence Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad BitmapPersistence
- Propiedad BitmapPersistence Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad BitmapPersistence
- Propiedad BitmapPersistence Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad BitmapPersistence
- Propiedad BitmapPersistence Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad BitmapPersistence
- Propiedad BitmapPersistence Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad BitmapPersistence
- Propiedad BitmapPersistence Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad BitmapPersistence
- Propiedad BitmapPersistence Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad BitmapPersistence
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapPersistence
- IMsRdpClientAdvancedSettings.get_BitmapPersistence
- IMsRdpClientAdvancedSettings.put_BitmapPersistence
- IMsRdpClientAdvancedSettings2.BitmapPersistence
- IMsRdpClientAdvancedSettings2.get_BitmapPersistence
- IMsRdpClientAdvancedSettings2.put_BitmapPersistence
- IMsRdpClientAdvancedSettings3.BitmapPersistence
- IMsRdpClientAdvancedSettings3.get_BitmapPersistence
- IMsRdpClientAdvancedSettings3.put_BitmapPersistence
- IMsRdpClientAdvancedSettings4.BitmapPersistence
- IMsRdpClientAdvancedSettings4.get_BitmapPersistence
- IMsRdpClientAdvancedSettings4.put_BitmapPersistence
- IMsRdpClientAdvancedSettings5.BitmapPersistence
- IMsRdpClientAdvancedSettings5.get_BitmapPersistence
- IMsRdpClientAdvancedSettings5.put_BitmapPersistence
- IMsRdpClientAdvancedSettings6.BitmapPersistence
- IMsRdpClientAdvancedSettings6.get_BitmapPersistence
- IMsRdpClientAdvancedSettings6.put_BitmapPersistence
- IMsRdpClientAdvancedSettings7.BitmapPersistence
- IMsRdpClientAdvancedSettings7.get_BitmapPersistence
- IMsRdpClientAdvancedSettings7.put_BitmapPersistence
- IMsRdpClientAdvancedSettings8.BitmapPersistence
- IMsRdpClientAdvancedSettings8.get_BitmapPersistence
- IMsRdpClientAdvancedSettings8.put_BitmapPersistence
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65795b5217c785befe0db6ac529d5760a6211d4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422145"
---
# <a name="imsrdpclientadvancedsettingsbitmappersistence-property"></a><span data-ttu-id="2c134-121">IMsRdpClientAdvancedSettings:: BitmapPersistence (propiedad)</span><span class="sxs-lookup"><span data-stu-id="2c134-121">IMsRdpClientAdvancedSettings::BitmapPersistence property</span></span>

<span data-ttu-id="2c134-122">Especifica si se debe usar el almacenamiento en caché de mapas de bits persistente.</span><span class="sxs-lookup"><span data-stu-id="2c134-122">Specifies if persistent bitmap caching should be used.</span></span> <span data-ttu-id="2c134-123">El almacenamiento en caché persistente puede mejorar el rendimiento pero requiere espacio adicional en disco.</span><span class="sxs-lookup"><span data-stu-id="2c134-123">Persistent caching can improve performance but requires additional disk space.</span></span>

<span data-ttu-id="2c134-124">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="2c134-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c134-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2c134-125">Syntax</span></span>


```C++
HRESULT put_BitmapPersistence(
  [in]  LONG bitmapPeristence
);

HRESULT get_BitmapPersistence(
  [out] LONG *pbitmapPeristence
);
```



## <a name="property-value"></a><span data-ttu-id="2c134-126">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2c134-126">Property value</span></span>

<span data-ttu-id="2c134-127">Establezca este parámetro en 0 para deshabilitar el almacenamiento en caché o un valor distinto de cero para habilitar el almacenamiento en caché.</span><span class="sxs-lookup"><span data-stu-id="2c134-127">Set this parameter to 0 to disable caching or a nonzero value to enable caching.</span></span>

> [!Note]  
> <span data-ttu-id="2c134-128">El error ortográfico en el nombre del parámetro está en la versión de lanzamiento del control.</span><span class="sxs-lookup"><span data-stu-id="2c134-128">The spelling error in the name of the parameter is in the released version of the control.</span></span>

 

## <a name="error-codes"></a><span data-ttu-id="2c134-129">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="2c134-129">Error codes</span></span>

<span data-ttu-id="2c134-130">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="2c134-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c134-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2c134-131">Remarks</span></span>

<span data-ttu-id="2c134-132">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="2c134-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c134-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c134-133">Requirements</span></span>



| <span data-ttu-id="2c134-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c134-134">Requirement</span></span> | <span data-ttu-id="2c134-135">Value</span><span class="sxs-lookup"><span data-stu-id="2c134-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c134-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c134-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2c134-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c134-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="2c134-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2c134-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2c134-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c134-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="2c134-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2c134-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="2c134-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c134-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="2c134-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2c134-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c134-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c134-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="2c134-144">IID</span><span class="sxs-lookup"><span data-stu-id="2c134-144">IID</span></span><br/>                      | <span data-ttu-id="2c134-145">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="2c134-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2c134-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c134-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c134-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="2c134-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="2c134-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="2c134-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="2c134-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="2c134-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="2c134-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="2c134-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="2c134-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="2c134-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="2c134-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="2c134-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="2c134-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="2c134-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="2c134-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="2c134-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





