---
title: Propiedad DisableCtrlAltDel de IMsRdpClientAdvancedSettings
description: Especifica si se debe mostrar la pantalla de explicación inicial de Winlogon.
ms.assetid: 79212472-105f-4e92-8065-f97819637d02
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DisableCtrlAltDel
- Propiedad DisableCtrlAltDel Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad DisableCtrlAltDel
- Propiedad DisableCtrlAltDel Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad DisableCtrlAltDel
- Propiedad DisableCtrlAltDel Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad DisableCtrlAltDel
- Propiedad DisableCtrlAltDel Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad DisableCtrlAltDel
- Propiedad DisableCtrlAltDel Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad DisableCtrlAltDel
- Propiedad DisableCtrlAltDel Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad DisableCtrlAltDel
- Propiedad DisableCtrlAltDel Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad DisableCtrlAltDel
- Propiedad DisableCtrlAltDel Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad DisableCtrlAltDel
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings2.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings3.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings4.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings5.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings6.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings7.put_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.get_DisableCtrlAltDel
- IMsRdpClientAdvancedSettings8.put_DisableCtrlAltDel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3380aa78c16c7e937637cc727fe81f054649f929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801568"
---
# <a name="imsrdpclientadvancedsettingsdisablectrlaltdel-property"></a><span data-ttu-id="3d1f1-120">IMsRdpClientAdvancedSettings::D propiedad isableCtrlAltDel</span><span class="sxs-lookup"><span data-stu-id="3d1f1-120">IMsRdpClientAdvancedSettings::DisableCtrlAltDel property</span></span>

<span data-ttu-id="3d1f1-121">Especifica si se debe mostrar la pantalla de explicación inicial de Winlogon.</span><span class="sxs-lookup"><span data-stu-id="3d1f1-121">Specifies if the initial explanatory screen in Winlogon should display.</span></span>

<span data-ttu-id="3d1f1-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="3d1f1-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d1f1-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d1f1-123">Syntax</span></span>


```C++
HRESULT put_DisableCtrlAltDel(
  [in]  LONG disableCtrlAltDel
);

HRESULT get_DisableCtrlAltDel(
  [out] LONG *pdisableCtrlAltDel
);
```



## <a name="property-value"></a><span data-ttu-id="3d1f1-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3d1f1-124">Property value</span></span>

<span data-ttu-id="3d1f1-125">Establezca este parámetro en 0 para deshabilitar la característica o un valor distinto de cero para habilitar la característica.</span><span class="sxs-lookup"><span data-stu-id="3d1f1-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3d1f1-126">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="3d1f1-126">Error codes</span></span>

<span data-ttu-id="3d1f1-127">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="3d1f1-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d1f1-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3d1f1-128">Remarks</span></span>

<span data-ttu-id="3d1f1-129">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="3d1f1-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3d1f1-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d1f1-130">Requirements</span></span>



| <span data-ttu-id="3d1f1-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d1f1-131">Requirement</span></span> | <span data-ttu-id="3d1f1-132">Value</span><span class="sxs-lookup"><span data-stu-id="3d1f1-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3d1f1-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d1f1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3d1f1-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d1f1-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="3d1f1-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d1f1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3d1f1-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d1f1-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="3d1f1-137">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3d1f1-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="3d1f1-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d1f1-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="3d1f1-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3d1f1-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d1f1-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d1f1-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="3d1f1-141">IID</span><span class="sxs-lookup"><span data-stu-id="3d1f1-141">IID</span></span><br/>                      | <span data-ttu-id="3d1f1-142">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="3d1f1-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3d1f1-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d1f1-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d1f1-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="3d1f1-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="3d1f1-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="3d1f1-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="3d1f1-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="3d1f1-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="3d1f1-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="3d1f1-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="3d1f1-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="3d1f1-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="3d1f1-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="3d1f1-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="3d1f1-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="3d1f1-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="3d1f1-151">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="3d1f1-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





