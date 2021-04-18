---
title: Propiedad BitmapVirtualCache16BppSize de IMsRdpClientAdvancedSettings
description: Especifica el tamaño, en megabytes, del archivo de caché de mapa de bits persistente que se va a usar para los valores de color de alta densidad de 15 y 16 bits por píxel.
ms.assetid: f2558c88-d60f-4be3-9941-8e0e18bbb778
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad BitmapVirtualCache16BppSize
- Propiedad BitmapVirtualCache16BppSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad BitmapVirtualCache16BppSize
- Propiedad BitmapVirtualCache16BppSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad BitmapVirtualCache16BppSize
- Propiedad BitmapVirtualCache16BppSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad BitmapVirtualCache16BppSize
- Propiedad BitmapVirtualCache16BppSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad BitmapVirtualCache16BppSize
- Propiedad BitmapVirtualCache16BppSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad BitmapVirtualCache16BppSize
- Propiedad BitmapVirtualCache16BppSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad BitmapVirtualCache16BppSize
- Propiedad BitmapVirtualCache16BppSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad BitmapVirtualCache16BppSize
- Propiedad BitmapVirtualCache16BppSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad BitmapVirtualCache16BppSize
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings2.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings2.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings2.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings3.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings3.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings3.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings4.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings4.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings4.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings5.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCache16BppSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCache16BppSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5fd0a11a1cf3b313c1f6f2c12d1a73b61c6f45a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685856"
---
# <a name="imsrdpclientadvancedsettingsbitmapvirtualcache16bppsize-property"></a><span data-ttu-id="7662d-120">IMsRdpClientAdvancedSettings:: BitmapVirtualCache16BppSize (propiedad)</span><span class="sxs-lookup"><span data-stu-id="7662d-120">IMsRdpClientAdvancedSettings::BitmapVirtualCache16BppSize property</span></span>

<span data-ttu-id="7662d-121">Especifica el tamaño, en megabytes, del archivo de caché de mapa de bits persistente que se va a usar para los valores de color de alta densidad de 15 y 16 bits por píxel.</span><span class="sxs-lookup"><span data-stu-id="7662d-121">Specifies the size, in megabytes, of the persistent bitmap cache file to use for the 15 and 16 bits-per-pixel high-color settings.</span></span>

<span data-ttu-id="7662d-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="7662d-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7662d-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7662d-123">Syntax</span></span>


```C++
HRESULT put_BitmapVirtualCache16BppSize(
  [in]  LONG bitmapVirtualCache16BppSize
);

HRESULT get_BitmapVirtualCache16BppSize(
  [out] LONG *pbitmapVirtualCache16BppSize
);
```



## <a name="property-value"></a><span data-ttu-id="7662d-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7662d-124">Property value</span></span>

<span data-ttu-id="7662d-125">Nuevo tamaño de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="7662d-125">The new cache size.</span></span> <span data-ttu-id="7662d-126">Los valores válidos son de 1 a 32, ambos inclusive, y el valor predeterminado es 20.</span><span class="sxs-lookup"><span data-stu-id="7662d-126">The valid values are 1 to 32 inclusive, and the default value is 20.</span></span> <span data-ttu-id="7662d-127">Tenga en cuenta que el tamaño máximo de todos los archivos de caché virtual es 128 MB.</span><span class="sxs-lookup"><span data-stu-id="7662d-127">Note that the maximum size for all virtual cache files is 128 MB.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7662d-128">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="7662d-128">Error codes</span></span>

<span data-ttu-id="7662d-129">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="7662d-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="7662d-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7662d-130">Remarks</span></span>

<span data-ttu-id="7662d-131">Entre las propiedades relacionadas se incluyen las propiedades **BitmapVirtualCacheSize** y **BitmapVirtualCache24BppSize** .</span><span class="sxs-lookup"><span data-stu-id="7662d-131">Related properties include the **BitmapVirtualCacheSize** and **BitmapVirtualCache24BppSize** properties.</span></span>

<span data-ttu-id="7662d-132">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="7662d-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7662d-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7662d-133">Requirements</span></span>



| <span data-ttu-id="7662d-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="7662d-134">Requirement</span></span> | <span data-ttu-id="7662d-135">Value</span><span class="sxs-lookup"><span data-stu-id="7662d-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7662d-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7662d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7662d-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7662d-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="7662d-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7662d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7662d-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7662d-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="7662d-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7662d-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="7662d-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7662d-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="7662d-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7662d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7662d-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7662d-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="7662d-144">IID</span><span class="sxs-lookup"><span data-stu-id="7662d-144">IID</span></span><br/>                      | <span data-ttu-id="7662d-145">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="7662d-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7662d-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="7662d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7662d-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="7662d-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="7662d-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="7662d-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="7662d-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="7662d-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="7662d-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="7662d-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="7662d-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="7662d-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="7662d-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="7662d-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="7662d-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="7662d-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="7662d-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="7662d-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





