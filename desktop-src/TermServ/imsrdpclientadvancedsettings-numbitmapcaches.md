---
title: Propiedad NumBitmapCaches de IMsRdpClientAdvancedSettings
description: Esta propiedad no es compatible. | Propiedad NumBitmapCaches de IMsRdpClientAdvancedSettings
ms.assetid: a413b2c0-7661-415d-bc38-e8fd55006e8c
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad NumBitmapCaches
- Propiedad NumBitmapCaches Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad NumBitmapCaches
- Propiedad NumBitmapCaches Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad NumBitmapCaches
- Propiedad NumBitmapCaches Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad NumBitmapCaches
- Propiedad NumBitmapCaches Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad NumBitmapCaches
- Propiedad NumBitmapCaches Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad NumBitmapCaches
- Propiedad NumBitmapCaches Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad NumBitmapCaches
- Propiedad NumBitmapCaches Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad NumBitmapCaches
- Propiedad NumBitmapCaches Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad NumBitmapCaches
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.NumBitmapCaches
- IMsRdpClientAdvancedSettings.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings2.NumBitmapCaches
- IMsRdpClientAdvancedSettings2.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings2.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings3.NumBitmapCaches
- IMsRdpClientAdvancedSettings3.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings3.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings4.NumBitmapCaches
- IMsRdpClientAdvancedSettings4.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings4.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings5.NumBitmapCaches
- IMsRdpClientAdvancedSettings5.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings5.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings6.NumBitmapCaches
- IMsRdpClientAdvancedSettings6.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings6.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings7.NumBitmapCaches
- IMsRdpClientAdvancedSettings7.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings7.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings8.NumBitmapCaches
- IMsRdpClientAdvancedSettings8.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings8.put_NumBitmapCaches
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ae60423287da041e3f84b28d8d51388e9a4050b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678721"
---
# <a name="imsrdpclientadvancedsettingsnumbitmapcaches-property"></a><span data-ttu-id="b6099-121">IMsRdpClientAdvancedSettings:: NumBitmapCaches (propiedad)</span><span class="sxs-lookup"><span data-stu-id="b6099-121">IMsRdpClientAdvancedSettings::NumBitmapCaches property</span></span>

<span data-ttu-id="b6099-122">Esta propiedad no es compatible.</span><span class="sxs-lookup"><span data-stu-id="b6099-122">This property is not supported.</span></span>

<span data-ttu-id="b6099-123">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b6099-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6099-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6099-124">Syntax</span></span>


```C++
HRESULT put_NumBitmapCaches(
  [in]  LONG numBitmapCaches
);

HRESULT get_NumBitmapCaches(
  [out] LONG *pnumBitmapCaches
);
```



## <a name="property-value"></a><span data-ttu-id="b6099-125">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b6099-125">Property value</span></span>

<span data-ttu-id="b6099-126">El nuevo número de cachés.</span><span class="sxs-lookup"><span data-stu-id="b6099-126">The new number of caches.</span></span> <span data-ttu-id="b6099-127">El valor predeterminado es 3, lo que da como resultado el mejor rendimiento.</span><span class="sxs-lookup"><span data-stu-id="b6099-127">The default value is 3, which results in the best performance.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b6099-128">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="b6099-128">Error codes</span></span>

<span data-ttu-id="b6099-129">Devuelve **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="b6099-129">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6099-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6099-130">Remarks</span></span>

<span data-ttu-id="b6099-131">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="b6099-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6099-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6099-132">Requirements</span></span>



| <span data-ttu-id="b6099-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6099-133">Requirement</span></span> | <span data-ttu-id="b6099-134">Value</span><span class="sxs-lookup"><span data-stu-id="b6099-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6099-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6099-135">Minimum supported client</span></span><br/> | <span data-ttu-id="b6099-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b6099-136">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="b6099-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6099-137">Minimum supported server</span></span><br/> | <span data-ttu-id="b6099-138">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b6099-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="b6099-139">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="b6099-139">End of client support</span></span><br/>    | <span data-ttu-id="b6099-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b6099-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="b6099-141">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="b6099-141">End of server support</span></span><br/>    | <span data-ttu-id="b6099-142">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b6099-142">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="b6099-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b6099-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="b6099-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6099-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="b6099-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b6099-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6099-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6099-146"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="b6099-147">IID</span><span class="sxs-lookup"><span data-stu-id="b6099-147">IID</span></span><br/>                      | <span data-ttu-id="b6099-148">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="b6099-148">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b6099-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6099-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6099-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="b6099-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="b6099-151">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="b6099-151">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="b6099-152">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="b6099-152">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="b6099-153">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="b6099-153">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="b6099-154">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="b6099-154">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="b6099-155">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="b6099-155">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="b6099-156">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="b6099-156">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="b6099-157">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="b6099-157">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





