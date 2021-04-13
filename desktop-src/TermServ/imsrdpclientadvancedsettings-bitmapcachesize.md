---
title: Propiedad BitmapCacheSize de IMsRdpClientAdvancedSettings
description: Tamaño, en kilobytes, del archivo de caché de mapa de bits utilizado para los mapas de bits de 8 bits por píxel.
ms.assetid: a2a4b739-0fa3-4a76-87ae-3cba913b7703
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad BitmapCacheSize
- Propiedad BitmapCacheSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad BitmapCacheSize
- Propiedad BitmapCacheSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad BitmapCacheSize
- Propiedad BitmapCacheSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad BitmapCacheSize
- Propiedad BitmapCacheSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad BitmapCacheSize
- Propiedad BitmapCacheSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad BitmapCacheSize
- Propiedad BitmapCacheSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad BitmapCacheSize
- Propiedad BitmapCacheSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad BitmapCacheSize
- Propiedad BitmapCacheSize Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad BitmapCacheSize
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.BitmapCacheSize
- IMsRdpClientAdvancedSettings.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings2.BitmapCacheSize
- IMsRdpClientAdvancedSettings2.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings2.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings3.BitmapCacheSize
- IMsRdpClientAdvancedSettings3.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings3.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings4.BitmapCacheSize
- IMsRdpClientAdvancedSettings4.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings4.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings5.BitmapCacheSize
- IMsRdpClientAdvancedSettings5.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings5.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings6.BitmapCacheSize
- IMsRdpClientAdvancedSettings6.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings6.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings7.BitmapCacheSize
- IMsRdpClientAdvancedSettings7.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings7.put_BitmapCacheSize
- IMsRdpClientAdvancedSettings8.BitmapCacheSize
- IMsRdpClientAdvancedSettings8.get_BitmapCacheSize
- IMsRdpClientAdvancedSettings8.put_BitmapCacheSize
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a38376bb0b06bd4efea36d3c4cad4e4aec0f35b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422146"
---
# <a name="imsrdpclientadvancedsettingsbitmapcachesize-property"></a><span data-ttu-id="c56be-120">IMsRdpClientAdvancedSettings:: BitmapCacheSize (propiedad)</span><span class="sxs-lookup"><span data-stu-id="c56be-120">IMsRdpClientAdvancedSettings::BitmapCacheSize property</span></span>

<span data-ttu-id="c56be-121">Tamaño, en kilobytes, del archivo de caché de mapa de bits utilizado para los mapas de bits de 8 bits por píxel.</span><span class="sxs-lookup"><span data-stu-id="c56be-121">The size, in kilobytes, of the bitmap cache file used for 8-bits-per-pixel bitmaps.</span></span>

<span data-ttu-id="c56be-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="c56be-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c56be-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c56be-123">Syntax</span></span>


```C++
HRESULT put_BitmapCacheSize(
  [in]  LONG bitmapCacheSize
);

HRESULT get_BitmapCacheSize(
  [out] LONG *pbitmapCacheSize
);
```



## <a name="property-value"></a><span data-ttu-id="c56be-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c56be-124">Property value</span></span>

<span data-ttu-id="c56be-125">Nuevo tamaño de la memoria caché, en kilobytes.</span><span class="sxs-lookup"><span data-stu-id="c56be-125">The new cache size, in kilobytes.</span></span> <span data-ttu-id="c56be-126">Los valores numéricos válidos van de 1 a 32, ambos inclusive.</span><span class="sxs-lookup"><span data-stu-id="c56be-126">The valid numeric values are 1 to 32 inclusive.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c56be-127">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="c56be-127">Error codes</span></span>

<span data-ttu-id="c56be-128">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="c56be-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c56be-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c56be-129">Remarks</span></span>

<span data-ttu-id="c56be-130">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c56be-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c56be-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c56be-131">Requirements</span></span>



| <span data-ttu-id="c56be-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="c56be-132">Requirement</span></span> | <span data-ttu-id="c56be-133">Value</span><span class="sxs-lookup"><span data-stu-id="c56be-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c56be-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c56be-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c56be-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c56be-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="c56be-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c56be-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c56be-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c56be-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="c56be-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c56be-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="c56be-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c56be-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="c56be-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c56be-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c56be-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c56be-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="c56be-142">IID</span><span class="sxs-lookup"><span data-stu-id="c56be-142">IID</span></span><br/>                      | <span data-ttu-id="c56be-143">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="c56be-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c56be-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="c56be-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c56be-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="c56be-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="c56be-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="c56be-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="c56be-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="c56be-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="c56be-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="c56be-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="c56be-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="c56be-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="c56be-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="c56be-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="c56be-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="c56be-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="c56be-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="c56be-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





