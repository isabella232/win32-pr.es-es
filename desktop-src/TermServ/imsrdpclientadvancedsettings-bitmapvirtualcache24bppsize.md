---
title: Propiedad BitmapVirtualCache24BppSize de IMsRdpClientAdvancedSettings
description: Especifica el tamaño, en megabytes, del archivo de caché de mapa de bits persistente que se va a usar para la configuración de alto color de 24 bits por píxel.
ms.assetid: 5891c90d-f463-4f27-b212-351ebf21ae00
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad BitmapVirtualCache24BppSize
- Propiedad BitmapVirtualCache24BppSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad BitmapVirtualCache24BppSize
- Propiedad BitmapVirtualCache24BppSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad BitmapVirtualCache24BppSize
- Propiedad BitmapVirtualCache24BppSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad BitmapVirtualCache24BppSize
- Propiedad BitmapVirtualCache24BppSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad BitmapVirtualCache24BppSize
- Propiedad BitmapVirtualCache24BppSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad BitmapVirtualCache24BppSize
- Propiedad BitmapVirtualCache24BppSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad BitmapVirtualCache24BppSize
- Propiedad BitmapVirtualCache24BppSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad BitmapVirtualCache24BppSize
- Propiedad BitmapVirtualCache24BppSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad BitmapVirtualCache24BppSize
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings2.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings2.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings2.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings3.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings3.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings3.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings4.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings4.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings4.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings5.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings5.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings5.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings6.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings6.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings6.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings7.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings7.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings7.put_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings8.BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings8.get_BitmapVirtualCache24BppSize
- IMsRdpClientAdvancedSettings8.put_BitmapVirtualCache24BppSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0fc31954ff191f795146e3894b0394b29484fb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676977"
---
# <a name="imsrdpclientadvancedsettingsbitmapvirtualcache24bppsize-property"></a><span data-ttu-id="0a0b6-120">IMsRdpClientAdvancedSettings:: BitmapVirtualCache24BppSize (propiedad)</span><span class="sxs-lookup"><span data-stu-id="0a0b6-120">IMsRdpClientAdvancedSettings::BitmapVirtualCache24BppSize property</span></span>

<span data-ttu-id="0a0b6-121">Especifica el tamaño, en megabytes, del archivo de caché de mapa de bits persistente que se va a usar para la configuración de alto color de 24 bits por píxel.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-121">Specifies the size, in megabytes, of the persistent bitmap cache file to use for the 24 bits-per-pixel high-color setting.</span></span>

<span data-ttu-id="0a0b6-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a0b6-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a0b6-123">Syntax</span></span>


```C++
HRESULT put_BitmapVirtualCache24BppSize(
  [in]  LONG bitmapVirtualCache24BppSize
);

HRESULT get_BitmapVirtualCache24BppSize(
  [out] LONG *pbitmapVirtualCache24BppSize
);
```



## <a name="property-value"></a><span data-ttu-id="0a0b6-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0a0b6-124">Property value</span></span>

<span data-ttu-id="0a0b6-125">Nuevo tamaño de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-125">The new cache size.</span></span> <span data-ttu-id="0a0b6-126">Los valores válidos son de 1 a 32, ambos inclusive, y el valor predeterminado es 30.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-126">The valid values are 1 to 32 inclusive, and the default value is 30.</span></span> <span data-ttu-id="0a0b6-127">Tenga en cuenta que el tamaño máximo de todos los archivos de caché virtual es 128 MB.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-127">Note that the maximum size for all virtual cache files is 128 MB.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0a0b6-128">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="0a0b6-128">Error codes</span></span>

<span data-ttu-id="0a0b6-129">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="0a0b6-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a0b6-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0a0b6-130">Remarks</span></span>

<span data-ttu-id="0a0b6-131">Entre las propiedades relacionadas se incluyen las propiedades **BitmapVirtualCacheSize** y **BitmapVirtualCache16BppSize** .</span><span class="sxs-lookup"><span data-stu-id="0a0b6-131">Related properties include the **BitmapVirtualCacheSize** and **BitmapVirtualCache16BppSize** properties.</span></span>

<span data-ttu-id="0a0b6-132">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="0a0b6-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a0b6-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a0b6-133">Requirements</span></span>



| <span data-ttu-id="0a0b6-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a0b6-134">Requirement</span></span> | <span data-ttu-id="0a0b6-135">Value</span><span class="sxs-lookup"><span data-stu-id="0a0b6-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a0b6-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a0b6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="0a0b6-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0a0b6-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="0a0b6-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a0b6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="0a0b6-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0a0b6-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="0a0b6-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0a0b6-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="0a0b6-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a0b6-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="0a0b6-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0a0b6-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a0b6-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a0b6-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="0a0b6-144">IID</span><span class="sxs-lookup"><span data-stu-id="0a0b6-144">IID</span></span><br/>                      | <span data-ttu-id="0a0b6-145">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="0a0b6-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0a0b6-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a0b6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a0b6-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="0a0b6-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="0a0b6-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="0a0b6-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="0a0b6-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="0a0b6-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="0a0b6-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="0a0b6-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="0a0b6-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="0a0b6-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="0a0b6-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="0a0b6-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="0a0b6-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="0a0b6-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="0a0b6-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="0a0b6-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





