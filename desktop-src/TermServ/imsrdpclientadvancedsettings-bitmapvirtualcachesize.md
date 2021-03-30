---
title: Propiedad BitmapVirtualCacheSize de IMsRdpClientAdvancedSettings
description: Especifica el tamaño, en megabytes, del archivo de caché de mapa de bits persistente que se va a usar para el color de 8 bits por píxel.
ms.assetid: 4efcabd2-8671-40a3-ad12-af0b2b6e495a
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad BitmapVirtualCacheSize
- Propiedad BitmapVirtualCacheSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad BitmapVirtualCacheSize
- Propiedad BitmapVirtualCacheSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad BitmapVirtualCacheSize
- Propiedad BitmapVirtualCacheSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad BitmapVirtualCacheSize
- Propiedad BitmapVirtualCacheSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad BitmapVirtualCacheSize
- Propiedad BitmapVirtualCacheSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad BitmapVirtualCacheSize
- Propiedad BitmapVirtualCacheSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad BitmapVirtualCacheSize
- Propiedad BitmapVirtualCacheSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad BitmapVirtualCacheSize
- Propiedad BitmapVirtualCacheSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad BitmapVirtualCacheSize
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings2.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings2.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings2.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings3.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings3.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings3.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings4.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings4.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings4.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings5.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCacheSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCacheSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb652c0f235cf7438b49e68a544188ac4622acad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079096"
---
# <a name="imsrdpclientadvancedsettingsbitmapvirtualcachesize-property"></a><span data-ttu-id="183f9-120">IMsRdpClientAdvancedSettings:: BitmapVirtualCacheSize (propiedad)</span><span class="sxs-lookup"><span data-stu-id="183f9-120">IMsRdpClientAdvancedSettings::BitmapVirtualCacheSize property</span></span>

<span data-ttu-id="183f9-121">Especifica el tamaño, en megabytes, del archivo de caché de mapa de bits persistente que se va a usar para el color de 8 bits por píxel.</span><span class="sxs-lookup"><span data-stu-id="183f9-121">Specifies the size, in megabytes, of the persistent bitmap cache file to use for 8-bits-per-pixel color.</span></span>

<span data-ttu-id="183f9-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="183f9-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="183f9-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="183f9-123">Syntax</span></span>


```C++
HRESULT put_BitmapVirtualCacheSize(
  [in]  LONG bitmapVirtualCacheSize
);

HRESULT get_BitmapVirtualCacheSize(
  [out] LONG *pbitmapVirtualCacheSize
);
```



## <a name="property-value"></a><span data-ttu-id="183f9-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="183f9-124">Property value</span></span>

<span data-ttu-id="183f9-125">Nuevo tamaño de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="183f9-125">The new cache size.</span></span> <span data-ttu-id="183f9-126">Los valores válidos son de 1 a 32, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="183f9-126">The valid values are 1 to 32 inclusive.</span></span> <span data-ttu-id="183f9-127">Tenga en cuenta que el tamaño máximo de todos los archivos de caché virtual es 128 MB.</span><span class="sxs-lookup"><span data-stu-id="183f9-127">Note that the maximum size for all virtual cache files is 128 MB.</span></span>

## <a name="error-codes"></a><span data-ttu-id="183f9-128">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="183f9-128">Error codes</span></span>

<span data-ttu-id="183f9-129">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="183f9-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="183f9-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="183f9-130">Remarks</span></span>

<span data-ttu-id="183f9-131">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="183f9-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="183f9-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="183f9-132">Requirements</span></span>



| <span data-ttu-id="183f9-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="183f9-133">Requirement</span></span> | <span data-ttu-id="183f9-134">Value</span><span class="sxs-lookup"><span data-stu-id="183f9-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="183f9-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="183f9-135">Minimum supported client</span></span><br/> | <span data-ttu-id="183f9-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="183f9-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="183f9-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="183f9-137">Minimum supported server</span></span><br/> | <span data-ttu-id="183f9-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="183f9-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="183f9-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="183f9-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="183f9-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="183f9-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="183f9-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="183f9-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="183f9-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="183f9-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="183f9-143">IID</span><span class="sxs-lookup"><span data-stu-id="183f9-143">IID</span></span><br/>                      | <span data-ttu-id="183f9-144">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="183f9-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="183f9-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="183f9-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="183f9-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="183f9-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="183f9-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="183f9-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="183f9-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="183f9-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="183f9-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="183f9-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="183f9-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="183f9-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="183f9-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="183f9-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="183f9-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="183f9-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="183f9-153">**BitmapVirtualCache16BppSize**</span><span class="sxs-lookup"><span data-stu-id="183f9-153">**BitmapVirtualCache16BppSize**</span></span>](imsrdpclientadvancedsettings-bitmapvirtualcache16bppsize.md)
</dt> <dt>

[<span data-ttu-id="183f9-154">**BitmapVirtualCache24BppSize**</span><span class="sxs-lookup"><span data-stu-id="183f9-154">**BitmapVirtualCache24BppSize**</span></span>](imsrdpclientadvancedsettings-bitmapvirtualcache24bppsize.md)
</dt> <dt>

[<span data-ttu-id="183f9-155">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="183f9-155">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





