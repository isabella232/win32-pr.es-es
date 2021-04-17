---
title: Propiedad AcceleratorPassthrough de IMsRdpClientAdvancedSettings
description: Especifica si los aceleradores de teclado deben pasarse al servidor.
ms.assetid: ad0053bc-e3a9-4cd5-a409-fab3e24ffffa
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad AcceleratorPassthrough
- Propiedad AcceleratorPassthrough Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad AcceleratorPassthrough
- Propiedad AcceleratorPassthrough Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad AcceleratorPassthrough
- Propiedad AcceleratorPassthrough Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad AcceleratorPassthrough
- Propiedad AcceleratorPassthrough Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad AcceleratorPassthrough
- Propiedad AcceleratorPassthrough Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad AcceleratorPassthrough
- Propiedad AcceleratorPassthrough Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad AcceleratorPassthrough
- Propiedad AcceleratorPassthrough Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad AcceleratorPassthrough
- Propiedad AcceleratorPassthrough Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad AcceleratorPassthrough
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings2.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings2.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings2.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings3.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings3.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings3.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings4.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings4.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings4.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings5.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings5.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings5.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings6.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings6.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings6.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings7.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings7.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings7.put_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings8.AcceleratorPassthrough
- IMsRdpClientAdvancedSettings8.get_AcceleratorPassthrough
- IMsRdpClientAdvancedSettings8.put_AcceleratorPassthrough
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c252c5c0477f331b66cf65b93ed2cab844fb88e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676675"
---
# <a name="imsrdpclientadvancedsettingsacceleratorpassthrough-property"></a><span data-ttu-id="57d16-120">IMsRdpClientAdvancedSettings:: AcceleratorPassthrough (propiedad)</span><span class="sxs-lookup"><span data-stu-id="57d16-120">IMsRdpClientAdvancedSettings::AcceleratorPassthrough property</span></span>

<span data-ttu-id="57d16-121">Especifica si los aceleradores de teclado deben pasarse al servidor.</span><span class="sxs-lookup"><span data-stu-id="57d16-121">Specifies if keyboard accelerators should be passed to the server.</span></span>

<span data-ttu-id="57d16-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="57d16-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="57d16-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57d16-123">Syntax</span></span>


```C++
HRESULT put_AcceleratorPassthrough(
  [in]  LONG acceleratorPassthrough
);

HRESULT get_AcceleratorPassthrough(
  [out] LONG *pacceleratorPassthrough
);
```



## <a name="property-value"></a><span data-ttu-id="57d16-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="57d16-124">Property value</span></span>

<span data-ttu-id="57d16-125">Establezca este parámetro en 0 para deshabilitar la característica o un valor distinto de cero para habilitar la característica.</span><span class="sxs-lookup"><span data-stu-id="57d16-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span> <span data-ttu-id="57d16-126">El valor predeterminado es un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="57d16-126">The default is a nonzero value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="57d16-127">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="57d16-127">Error codes</span></span>

<span data-ttu-id="57d16-128">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="57d16-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="57d16-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57d16-129">Remarks</span></span>

<span data-ttu-id="57d16-130">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="57d16-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="57d16-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57d16-131">Requirements</span></span>



| <span data-ttu-id="57d16-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="57d16-132">Requirement</span></span> | <span data-ttu-id="57d16-133">Value</span><span class="sxs-lookup"><span data-stu-id="57d16-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57d16-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57d16-134">Minimum supported client</span></span><br/> | <span data-ttu-id="57d16-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57d16-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="57d16-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57d16-136">Minimum supported server</span></span><br/> | <span data-ttu-id="57d16-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57d16-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="57d16-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="57d16-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="57d16-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57d16-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="57d16-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="57d16-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57d16-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57d16-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="57d16-142">IID</span><span class="sxs-lookup"><span data-stu-id="57d16-142">IID</span></span><br/>                      | <span data-ttu-id="57d16-143">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="57d16-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="57d16-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="57d16-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57d16-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="57d16-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="57d16-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="57d16-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="57d16-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="57d16-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="57d16-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="57d16-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="57d16-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="57d16-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="57d16-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="57d16-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="57d16-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="57d16-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="57d16-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="57d16-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





