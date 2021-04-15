---
title: Propiedad RedirectSmartCards de IMsRdpClientAdvancedSettings
description: Especifica si se permite la redirección de tarjetas inteligentes.
ms.assetid: 53b6b483-ccba-41eb-a417-241a4430958e
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RedirectSmartCards
- Propiedad RedirectSmartCards Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad RedirectSmartCards
- Propiedad RedirectSmartCards Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad RedirectSmartCards
- Propiedad RedirectSmartCards Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad RedirectSmartCards
- Propiedad RedirectSmartCards Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad RedirectSmartCards
- Propiedad RedirectSmartCards Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad RedirectSmartCards
- Propiedad RedirectSmartCards Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad RedirectSmartCards
- Propiedad RedirectSmartCards Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad RedirectSmartCards
- Propiedad RedirectSmartCards Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad RedirectSmartCards
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectSmartCards
- IMsRdpClientAdvancedSettings.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings2.RedirectSmartCards
- IMsRdpClientAdvancedSettings2.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings2.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings3.RedirectSmartCards
- IMsRdpClientAdvancedSettings3.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings3.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings4.RedirectSmartCards
- IMsRdpClientAdvancedSettings4.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings4.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings5.RedirectSmartCards
- IMsRdpClientAdvancedSettings5.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings5.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings6.RedirectSmartCards
- IMsRdpClientAdvancedSettings6.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings6.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings7.RedirectSmartCards
- IMsRdpClientAdvancedSettings7.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings7.put_RedirectSmartCards
- IMsRdpClientAdvancedSettings8.RedirectSmartCards
- IMsRdpClientAdvancedSettings8.get_RedirectSmartCards
- IMsRdpClientAdvancedSettings8.put_RedirectSmartCards
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ba58a492ede5371c0f43d996f46ed7a898df7f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676561"
---
# <a name="imsrdpclientadvancedsettingsredirectsmartcards-property"></a><span data-ttu-id="1384c-120">IMsRdpClientAdvancedSettings:: RedirectSmartCards (propiedad)</span><span class="sxs-lookup"><span data-stu-id="1384c-120">IMsRdpClientAdvancedSettings::RedirectSmartCards property</span></span>

<span data-ttu-id="1384c-121">Especifica si se permite la redirección de tarjetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="1384c-121">Specifies if redirection of smart cards is allowed.</span></span>

<span data-ttu-id="1384c-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="1384c-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1384c-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1384c-123">Syntax</span></span>


```C++
HRESULT put_RedirectSmartCards(
  [in]  VARIANT_BOOL redirectSmartCards
);

HRESULT get_RedirectSmartCards(
  [out] VARIANT_BOOL *predirectSmartCards
);
```



## <a name="property-value"></a><span data-ttu-id="1384c-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="1384c-124">Property value</span></span>

<span data-ttu-id="1384c-125">Establezca este parámetro en **Variant \_ true** para permitir el redireccionamiento o **Variant \_ false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1384c-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="1384c-126">**Variante \_ TRUE** solicita al usuario que confirme que permite la redirección en el tiempo de conexión, por motivos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="1384c-126">**VARIANT\_TRUE** prompts the user to confirm allowing redirection at connection time, for security purposes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1384c-127">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="1384c-127">Error codes</span></span>

<span data-ttu-id="1384c-128">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="1384c-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="1384c-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1384c-129">Remarks</span></span>

<span data-ttu-id="1384c-130">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="1384c-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1384c-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1384c-131">Requirements</span></span>



| <span data-ttu-id="1384c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1384c-132">Requirement</span></span> | <span data-ttu-id="1384c-133">Value</span><span class="sxs-lookup"><span data-stu-id="1384c-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1384c-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1384c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1384c-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1384c-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="1384c-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1384c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1384c-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1384c-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="1384c-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1384c-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="1384c-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1384c-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="1384c-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1384c-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1384c-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1384c-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="1384c-142">IID</span><span class="sxs-lookup"><span data-stu-id="1384c-142">IID</span></span><br/>                      | <span data-ttu-id="1384c-143">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="1384c-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1384c-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="1384c-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1384c-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="1384c-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="1384c-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="1384c-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="1384c-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="1384c-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="1384c-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="1384c-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="1384c-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="1384c-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="1384c-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="1384c-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="1384c-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="1384c-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="1384c-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="1384c-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





