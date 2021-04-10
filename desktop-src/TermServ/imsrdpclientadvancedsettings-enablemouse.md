---
title: Propiedad EnableMouse de IMsRdpClientAdvancedSettings
description: Esta propiedad no es compatible. | Propiedad EnableMouse de IMsRdpClientAdvancedSettings
ms.assetid: 4f60fdfc-e1b9-4ac2-98e4-49331b072883
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad EnableMouse
- Propiedad EnableMouse Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad EnableMouse
- Propiedad EnableMouse Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad EnableMouse
- Propiedad EnableMouse Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad EnableMouse
- Propiedad EnableMouse Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad EnableMouse
- Propiedad EnableMouse Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad EnableMouse
- Propiedad EnableMouse Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad EnableMouse
- Propiedad EnableMouse Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad EnableMouse
- Propiedad EnableMouse Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad EnableMouse
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.EnableMouse
- IMsRdpClientAdvancedSettings.get_EnableMouse
- IMsRdpClientAdvancedSettings.put_EnableMouse
- IMsRdpClientAdvancedSettings2.EnableMouse
- IMsRdpClientAdvancedSettings2.get_EnableMouse
- IMsRdpClientAdvancedSettings2.put_EnableMouse
- IMsRdpClientAdvancedSettings3.EnableMouse
- IMsRdpClientAdvancedSettings3.get_EnableMouse
- IMsRdpClientAdvancedSettings3.put_EnableMouse
- IMsRdpClientAdvancedSettings4.EnableMouse
- IMsRdpClientAdvancedSettings4.get_EnableMouse
- IMsRdpClientAdvancedSettings4.put_EnableMouse
- IMsRdpClientAdvancedSettings5.EnableMouse
- IMsRdpClientAdvancedSettings5.get_EnableMouse
- IMsRdpClientAdvancedSettings5.put_EnableMouse
- IMsRdpClientAdvancedSettings6.EnableMouse
- IMsRdpClientAdvancedSettings6.get_EnableMouse
- IMsRdpClientAdvancedSettings6.put_EnableMouse
- IMsRdpClientAdvancedSettings7.EnableMouse
- IMsRdpClientAdvancedSettings7.get_EnableMouse
- IMsRdpClientAdvancedSettings7.put_EnableMouse
- IMsRdpClientAdvancedSettings8.EnableMouse
- IMsRdpClientAdvancedSettings8.get_EnableMouse
- IMsRdpClientAdvancedSettings8.put_EnableMouse
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0495ba7b48e431efe5746f40b353b5c1ad701d6a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104003502"
---
# <a name="imsrdpclientadvancedsettingsenablemouse-property"></a><span data-ttu-id="44720-121">IMsRdpClientAdvancedSettings:: EnableMouse (propiedad)</span><span class="sxs-lookup"><span data-stu-id="44720-121">IMsRdpClientAdvancedSettings::EnableMouse property</span></span>

<span data-ttu-id="44720-122">Esta propiedad no es compatible.</span><span class="sxs-lookup"><span data-stu-id="44720-122">This property is not supported.</span></span>

<span data-ttu-id="44720-123">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="44720-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="44720-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44720-124">Syntax</span></span>


```C++
HRESULT put_EnableMouse(
  [in]  LONG enableMouse
);

HRESULT get_EnableMouse(
  [out] LONG *penableMouse
);
```



## <a name="property-value"></a><span data-ttu-id="44720-125">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="44720-125">Property value</span></span>

<span data-ttu-id="44720-126">Establezca este parámetro en 0 para deshabilitar la característica o un valor distinto de cero para habilitar la característica.</span><span class="sxs-lookup"><span data-stu-id="44720-126">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="44720-127">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="44720-127">Error codes</span></span>

<span data-ttu-id="44720-128">Devuelve **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="44720-128">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="44720-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44720-129">Remarks</span></span>

<span data-ttu-id="44720-130">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="44720-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="44720-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44720-131">Requirements</span></span>



| <span data-ttu-id="44720-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="44720-132">Requirement</span></span> | <span data-ttu-id="44720-133">Value</span><span class="sxs-lookup"><span data-stu-id="44720-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44720-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44720-134">Minimum supported client</span></span><br/> | <span data-ttu-id="44720-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="44720-135">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="44720-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44720-136">Minimum supported server</span></span><br/> | <span data-ttu-id="44720-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="44720-137">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="44720-138">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="44720-138">End of client support</span></span><br/>    | <span data-ttu-id="44720-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="44720-139">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="44720-140">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="44720-140">End of server support</span></span><br/>    | <span data-ttu-id="44720-141">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="44720-141">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="44720-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="44720-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="44720-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44720-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="44720-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="44720-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44720-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44720-145"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="44720-146">IID</span><span class="sxs-lookup"><span data-stu-id="44720-146">IID</span></span><br/>                      | <span data-ttu-id="44720-147">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="44720-147">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="44720-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="44720-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44720-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="44720-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="44720-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="44720-150">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="44720-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="44720-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="44720-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="44720-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="44720-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="44720-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="44720-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="44720-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="44720-155">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="44720-155">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="44720-156">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="44720-156">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





