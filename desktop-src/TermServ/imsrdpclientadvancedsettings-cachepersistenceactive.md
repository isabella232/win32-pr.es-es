---
title: Propiedad CachePersistenceActive de IMsRdpClientAdvancedSettings
description: Especifica si se debe usar el almacenamiento en caché de mapas de bits persistente. El almacenamiento en caché persistente puede mejorar el rendimiento pero requiere espacio adicional en disco.
ms.assetid: 5eb986c4-98dd-426f-8d55-d3a9a526e1b2
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad CachePersistenceActive
- Propiedad CachePersistenceActive Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad CachePersistenceActive
- Propiedad CachePersistenceActive Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad CachePersistenceActive
- Propiedad CachePersistenceActive Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad CachePersistenceActive
- Propiedad CachePersistenceActive Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad CachePersistenceActive
- Propiedad CachePersistenceActive Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad CachePersistenceActive
- Propiedad CachePersistenceActive Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad CachePersistenceActive
- Propiedad CachePersistenceActive Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad CachePersistenceActive
- Propiedad CachePersistenceActive Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad CachePersistenceActive
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.CachePersistenceActive
- IMsRdpClientAdvancedSettings.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings2.CachePersistenceActive
- IMsRdpClientAdvancedSettings2.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings2.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings3.CachePersistenceActive
- IMsRdpClientAdvancedSettings3.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings3.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings4.CachePersistenceActive
- IMsRdpClientAdvancedSettings4.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings4.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings5.CachePersistenceActive
- IMsRdpClientAdvancedSettings5.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings5.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings6.CachePersistenceActive
- IMsRdpClientAdvancedSettings6.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings6.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings7.CachePersistenceActive
- IMsRdpClientAdvancedSettings7.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings7.put_CachePersistenceActive
- IMsRdpClientAdvancedSettings8.CachePersistenceActive
- IMsRdpClientAdvancedSettings8.get_CachePersistenceActive
- IMsRdpClientAdvancedSettings8.put_CachePersistenceActive
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb34e90cc028e95c750a444d53f42c9c0ab77400
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676978"
---
# <a name="imsrdpclientadvancedsettingscachepersistenceactive-property"></a><span data-ttu-id="c5fae-121">IMsRdpClientAdvancedSettings:: CachePersistenceActive (propiedad)</span><span class="sxs-lookup"><span data-stu-id="c5fae-121">IMsRdpClientAdvancedSettings::CachePersistenceActive property</span></span>

<span data-ttu-id="c5fae-122">Especifica si se debe usar el almacenamiento en caché de mapas de bits persistente.</span><span class="sxs-lookup"><span data-stu-id="c5fae-122">Specifies whether persistent bitmap caching should be used.</span></span> <span data-ttu-id="c5fae-123">El almacenamiento en caché persistente puede mejorar el rendimiento pero requiere espacio adicional en disco.</span><span class="sxs-lookup"><span data-stu-id="c5fae-123">Persistent caching can improve performance but requires additional disk space.</span></span>

<span data-ttu-id="c5fae-124">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="c5fae-124">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5fae-125">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5fae-125">Syntax</span></span>


```C++
HRESULT put_CachePersistenceActive(
  [in]  LONG cachePersistenceActive
);

HRESULT get_CachePersistenceActive(
  [out] LONG *pcachePersistenceActive
);
```



## <a name="property-value"></a><span data-ttu-id="c5fae-126">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c5fae-126">Property value</span></span>

<span data-ttu-id="c5fae-127">Establezca este parámetro en 0 para deshabilitar la característica o un valor distinto de cero para habilitar la característica.</span><span class="sxs-lookup"><span data-stu-id="c5fae-127">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c5fae-128">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="c5fae-128">Error codes</span></span>

<span data-ttu-id="c5fae-129">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="c5fae-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5fae-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5fae-130">Remarks</span></span>

<span data-ttu-id="c5fae-131">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c5fae-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5fae-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5fae-132">Requirements</span></span>



| <span data-ttu-id="c5fae-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5fae-133">Requirement</span></span> | <span data-ttu-id="c5fae-134">Value</span><span class="sxs-lookup"><span data-stu-id="c5fae-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5fae-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5fae-135">Minimum supported client</span></span><br/> | <span data-ttu-id="c5fae-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c5fae-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="c5fae-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c5fae-137">Minimum supported server</span></span><br/> | <span data-ttu-id="c5fae-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5fae-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="c5fae-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c5fae-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="c5fae-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5fae-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="c5fae-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c5fae-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5fae-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5fae-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="c5fae-143">IID</span><span class="sxs-lookup"><span data-stu-id="c5fae-143">IID</span></span><br/>                      | <span data-ttu-id="c5fae-144">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="c5fae-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c5fae-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5fae-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5fae-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="c5fae-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="c5fae-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="c5fae-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="c5fae-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="c5fae-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="c5fae-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="c5fae-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="c5fae-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="c5fae-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="c5fae-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="c5fae-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="c5fae-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="c5fae-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="c5fae-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="c5fae-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





