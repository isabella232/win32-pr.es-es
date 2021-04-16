---
title: Propiedad SmoothScroll de IMsRdpClientAdvancedSettings
description: Esta propiedad no es compatible. | Propiedad SmoothScroll de IMsRdpClientAdvancedSettings
ms.assetid: 7f1ce439-0b6e-4426-8dd6-3748509130e1
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad SmoothScroll
- Propiedad SmoothScroll Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad SmoothScroll
- Propiedad SmoothScroll Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad SmoothScroll
- Propiedad SmoothScroll Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad SmoothScroll
- Propiedad SmoothScroll Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad SmoothScroll
- Propiedad SmoothScroll Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad SmoothScroll
- Propiedad SmoothScroll Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad SmoothScroll
- Propiedad SmoothScroll Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad SmoothScroll
- Propiedad SmoothScroll Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad SmoothScroll
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.SmoothScroll
- IMsRdpClientAdvancedSettings.get_SmoothScroll
- IMsRdpClientAdvancedSettings.put_SmoothScroll
- IMsRdpClientAdvancedSettings2.SmoothScroll
- IMsRdpClientAdvancedSettings2.get_SmoothScroll
- IMsRdpClientAdvancedSettings2.put_SmoothScroll
- IMsRdpClientAdvancedSettings3.SmoothScroll
- IMsRdpClientAdvancedSettings3.get_SmoothScroll
- IMsRdpClientAdvancedSettings3.put_SmoothScroll
- IMsRdpClientAdvancedSettings4.SmoothScroll
- IMsRdpClientAdvancedSettings4.get_SmoothScroll
- IMsRdpClientAdvancedSettings4.put_SmoothScroll
- IMsRdpClientAdvancedSettings5.SmoothScroll
- IMsRdpClientAdvancedSettings5.get_SmoothScroll
- IMsRdpClientAdvancedSettings5.put_SmoothScroll
- IMsRdpClientAdvancedSettings6.SmoothScroll
- IMsRdpClientAdvancedSettings6.get_SmoothScroll
- IMsRdpClientAdvancedSettings6.put_SmoothScroll
- IMsRdpClientAdvancedSettings7.SmoothScroll
- IMsRdpClientAdvancedSettings7.get_SmoothScroll
- IMsRdpClientAdvancedSettings7.put_SmoothScroll
- IMsRdpClientAdvancedSettings8.SmoothScroll
- IMsRdpClientAdvancedSettings8.get_SmoothScroll
- IMsRdpClientAdvancedSettings8.put_SmoothScroll
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62be8fe85415792116c23b4e12d9ab56fb89e0f4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678723"
---
# <a name="imsrdpclientadvancedsettingssmoothscroll-property"></a><span data-ttu-id="104cc-121">IMsRdpClientAdvancedSettings:: SmoothScroll (propiedad)</span><span class="sxs-lookup"><span data-stu-id="104cc-121">IMsRdpClientAdvancedSettings::SmoothScroll property</span></span>

<span data-ttu-id="104cc-122">Esta propiedad no es compatible.</span><span class="sxs-lookup"><span data-stu-id="104cc-122">This property is not supported.</span></span>

<span data-ttu-id="104cc-123">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="104cc-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="104cc-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="104cc-124">Syntax</span></span>


```C++
HRESULT put_SmoothScroll(
  [in]  LONG smoothScroll
);

HRESULT get_SmoothScroll(
  [out] LONG *psmoothScroll
);
```



## <a name="property-value"></a><span data-ttu-id="104cc-125">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="104cc-125">Property value</span></span>

<span data-ttu-id="104cc-126">Establezca este parámetro en 0 para deshabilitar el desplazamiento suave o un valor distinto de cero para habilitar el desplazamiento suave.</span><span class="sxs-lookup"><span data-stu-id="104cc-126">Set this parameter to 0 to disable smooth scrolling or a nonzero value to enable smooth scrolling.</span></span>

## <a name="error-codes"></a><span data-ttu-id="104cc-127">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="104cc-127">Error codes</span></span>

<span data-ttu-id="104cc-128">Devuelve **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="104cc-128">Returns **S\_FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="104cc-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="104cc-129">Requirements</span></span>



| <span data-ttu-id="104cc-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="104cc-130">Requirement</span></span> | <span data-ttu-id="104cc-131">Value</span><span class="sxs-lookup"><span data-stu-id="104cc-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="104cc-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="104cc-132">Minimum supported client</span></span><br/> | <span data-ttu-id="104cc-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="104cc-133">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="104cc-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="104cc-134">Minimum supported server</span></span><br/> | <span data-ttu-id="104cc-135">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="104cc-135">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="104cc-136">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="104cc-136">End of client support</span></span><br/>    | <span data-ttu-id="104cc-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="104cc-137">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="104cc-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="104cc-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="104cc-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="104cc-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="104cc-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="104cc-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="104cc-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="104cc-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="104cc-142">IID</span><span class="sxs-lookup"><span data-stu-id="104cc-142">IID</span></span><br/>                      | <span data-ttu-id="104cc-143">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="104cc-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="104cc-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="104cc-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="104cc-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="104cc-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="104cc-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="104cc-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="104cc-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="104cc-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="104cc-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="104cc-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="104cc-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="104cc-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="104cc-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="104cc-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="104cc-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="104cc-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="104cc-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="104cc-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





