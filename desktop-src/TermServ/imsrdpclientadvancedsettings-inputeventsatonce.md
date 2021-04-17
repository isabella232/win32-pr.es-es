---
title: Propiedad InputEventsAtOnce de IMsRdpClientAdvancedSettings
description: Esta propiedad no es compatible. | Propiedad InputEventsAtOnce de IMsRdpClientAdvancedSettings
ms.assetid: 2f24b2cd-136d-4bde-9808-e5cb02bd7ce8
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad InputEventsAtOnce
- Propiedad InputEventsAtOnce Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad InputEventsAtOnce
- Propiedad InputEventsAtOnce Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad InputEventsAtOnce
- Propiedad InputEventsAtOnce Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad InputEventsAtOnce
- Propiedad InputEventsAtOnce Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad InputEventsAtOnce
- Propiedad InputEventsAtOnce Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad InputEventsAtOnce
- Propiedad InputEventsAtOnce Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad InputEventsAtOnce
- Propiedad InputEventsAtOnce Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad InputEventsAtOnce
- Propiedad InputEventsAtOnce Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad InputEventsAtOnce
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.InputEventsAtOnce
- IMsRdpClientAdvancedSettings.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings2.InputEventsAtOnce
- IMsRdpClientAdvancedSettings2.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings2.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings3.InputEventsAtOnce
- IMsRdpClientAdvancedSettings3.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings3.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings4.InputEventsAtOnce
- IMsRdpClientAdvancedSettings4.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings4.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings5.InputEventsAtOnce
- IMsRdpClientAdvancedSettings5.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings5.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings6.InputEventsAtOnce
- IMsRdpClientAdvancedSettings6.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings6.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings7.InputEventsAtOnce
- IMsRdpClientAdvancedSettings7.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings7.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings8.InputEventsAtOnce
- IMsRdpClientAdvancedSettings8.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings8.put_InputEventsAtOnce
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 999d00cb706e4fdd4cf0c9ed606c33de4a81e8d6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689784"
---
# <a name="imsrdpclientadvancedsettingsinputeventsatonce-property"></a><span data-ttu-id="9dd0b-121">IMsRdpClientAdvancedSettings:: InputEventsAtOnce (propiedad)</span><span class="sxs-lookup"><span data-stu-id="9dd0b-121">IMsRdpClientAdvancedSettings::InputEventsAtOnce property</span></span>

<span data-ttu-id="9dd0b-122">Esta propiedad no es compatible.</span><span class="sxs-lookup"><span data-stu-id="9dd0b-122">This property is not supported.</span></span>

<span data-ttu-id="9dd0b-123">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="9dd0b-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dd0b-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9dd0b-124">Syntax</span></span>


```C++
HRESULT put_InputEventsAtOnce(
  [in]  LONG inputEventsAtOnce
);

HRESULT get_InputEventsAtOnce(
  [out] LONG *pinputEventsAtOnce
);
```



## <a name="property-value"></a><span data-ttu-id="9dd0b-125">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9dd0b-125">Property value</span></span>

<span data-ttu-id="9dd0b-126">Nuevo número de eventos de entrada.</span><span class="sxs-lookup"><span data-stu-id="9dd0b-126">The new number of input events.</span></span> <span data-ttu-id="9dd0b-127">El valor predeterminado es 10.</span><span class="sxs-lookup"><span data-stu-id="9dd0b-127">The default is 10.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9dd0b-128">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="9dd0b-128">Error codes</span></span>

<span data-ttu-id="9dd0b-129">Devuelve **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="9dd0b-129">Returns **S\_FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9dd0b-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9dd0b-130">Requirements</span></span>



| <span data-ttu-id="9dd0b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dd0b-131">Requirement</span></span> | <span data-ttu-id="9dd0b-132">Value</span><span class="sxs-lookup"><span data-stu-id="9dd0b-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dd0b-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9dd0b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9dd0b-134">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9dd0b-134">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="9dd0b-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9dd0b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9dd0b-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9dd0b-136">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="9dd0b-137">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="9dd0b-137">End of client support</span></span><br/>    | <span data-ttu-id="9dd0b-138">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9dd0b-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="9dd0b-139">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="9dd0b-139">End of server support</span></span><br/>    | <span data-ttu-id="9dd0b-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9dd0b-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="9dd0b-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9dd0b-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="9dd0b-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9dd0b-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="9dd0b-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9dd0b-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9dd0b-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9dd0b-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="9dd0b-145">IID</span><span class="sxs-lookup"><span data-stu-id="9dd0b-145">IID</span></span><br/>                      | <span data-ttu-id="9dd0b-146">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="9dd0b-146">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9dd0b-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="9dd0b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dd0b-148">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="9dd0b-148">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="9dd0b-149">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="9dd0b-149">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="9dd0b-150">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="9dd0b-150">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="9dd0b-151">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="9dd0b-151">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="9dd0b-152">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="9dd0b-152">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="9dd0b-153">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="9dd0b-153">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="9dd0b-154">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="9dd0b-154">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="9dd0b-155">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="9dd0b-155">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





