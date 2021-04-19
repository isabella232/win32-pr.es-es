---
title: Propiedad DedicatedTerminal de IMsRdpClientAdvancedSettings
description: Esta propiedad no es compatible. | Propiedad DedicatedTerminal de IMsRdpClientAdvancedSettings
ms.assetid: 40d54c88-dcac-4e7d-b389-a65caeb6960e
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DedicatedTerminal
- Propiedad DedicatedTerminal Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad DedicatedTerminal
- Propiedad DedicatedTerminal Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad DedicatedTerminal
- Propiedad DedicatedTerminal Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad DedicatedTerminal
- Propiedad DedicatedTerminal Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad DedicatedTerminal
- Propiedad DedicatedTerminal Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad DedicatedTerminal
- Propiedad DedicatedTerminal Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad DedicatedTerminal
- Propiedad DedicatedTerminal Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad DedicatedTerminal
- Propiedad DedicatedTerminal Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad DedicatedTerminal
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DedicatedTerminal
- IMsRdpClientAdvancedSettings.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings2.DedicatedTerminal
- IMsRdpClientAdvancedSettings2.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings2.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings3.DedicatedTerminal
- IMsRdpClientAdvancedSettings3.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings3.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings4.DedicatedTerminal
- IMsRdpClientAdvancedSettings4.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings4.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings5.DedicatedTerminal
- IMsRdpClientAdvancedSettings5.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings5.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings6.DedicatedTerminal
- IMsRdpClientAdvancedSettings6.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings6.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings7.DedicatedTerminal
- IMsRdpClientAdvancedSettings7.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings7.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings8.DedicatedTerminal
- IMsRdpClientAdvancedSettings8.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings8.put_DedicatedTerminal
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee005439b38e21c5ed05d035545cc5600993cd5c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689793"
---
# <a name="imsrdpclientadvancedsettingsdedicatedterminal-property"></a><span data-ttu-id="81b95-121">IMsRdpClientAdvancedSettings::D propiedad edicatedTerminal</span><span class="sxs-lookup"><span data-stu-id="81b95-121">IMsRdpClientAdvancedSettings::DedicatedTerminal property</span></span>

<span data-ttu-id="81b95-122">Esta propiedad no es compatible.</span><span class="sxs-lookup"><span data-stu-id="81b95-122">This property is not supported.</span></span>

<span data-ttu-id="81b95-123">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="81b95-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="81b95-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="81b95-124">Syntax</span></span>


```C++
HRESULT put_DedicatedTerminal(
  [in]  LONG dedicatedTerminal
);

HRESULT get_DedicatedTerminal(
  [out] LONG *pdedicatedTerminal
);
```



## <a name="property-value"></a><span data-ttu-id="81b95-125">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="81b95-125">Property value</span></span>

<span data-ttu-id="81b95-126">Establezca este parámetro en 0 para deshabilitar la característica o un valor distinto de cero para habilitar la característica.</span><span class="sxs-lookup"><span data-stu-id="81b95-126">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="81b95-127">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="81b95-127">Error codes</span></span>

<span data-ttu-id="81b95-128">Devuelve **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="81b95-128">Returns **S\_FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="81b95-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81b95-129">Requirements</span></span>



| <span data-ttu-id="81b95-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="81b95-130">Requirement</span></span> | <span data-ttu-id="81b95-131">Value</span><span class="sxs-lookup"><span data-stu-id="81b95-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81b95-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81b95-132">Minimum supported client</span></span><br/> | <span data-ttu-id="81b95-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="81b95-133">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="81b95-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="81b95-134">Minimum supported server</span></span><br/> | <span data-ttu-id="81b95-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="81b95-135">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="81b95-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="81b95-136">End of client support</span></span><br/>    | <span data-ttu-id="81b95-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="81b95-137">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="81b95-138">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="81b95-138">End of server support</span></span><br/>    | <span data-ttu-id="81b95-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="81b95-139">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="81b95-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="81b95-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="81b95-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81b95-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="81b95-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="81b95-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81b95-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81b95-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="81b95-144">IID</span><span class="sxs-lookup"><span data-stu-id="81b95-144">IID</span></span><br/>                      | <span data-ttu-id="81b95-145">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="81b95-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="81b95-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="81b95-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81b95-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="81b95-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="81b95-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="81b95-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="81b95-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="81b95-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="81b95-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="81b95-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="81b95-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="81b95-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="81b95-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="81b95-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="81b95-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="81b95-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="81b95-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="81b95-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





