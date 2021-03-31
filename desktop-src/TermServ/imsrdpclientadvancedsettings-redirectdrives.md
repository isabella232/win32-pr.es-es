---
title: Propiedad RedirectDrives de IMsRdpClientAdvancedSettings
description: Especifica si se permite la redirección de unidades de disco.
ms.assetid: 5ed4cd28-4a1f-4d3b-9f9d-bf44a8483209
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RedirectDrives
- Propiedad RedirectDrives Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad RedirectDrives
- Propiedad RedirectDrives Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad RedirectDrives
- Propiedad RedirectDrives Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad RedirectDrives
- Propiedad RedirectDrives Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad RedirectDrives
- Propiedad RedirectDrives Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad RedirectDrives
- Propiedad RedirectDrives Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad RedirectDrives
- Propiedad RedirectDrives Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad RedirectDrives
- Propiedad RedirectDrives Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad RedirectDrives
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectDrives
- IMsRdpClientAdvancedSettings.get_RedirectDrives
- IMsRdpClientAdvancedSettings.put_RedirectDrives
- IMsRdpClientAdvancedSettings2.RedirectDrives
- IMsRdpClientAdvancedSettings2.get_RedirectDrives
- IMsRdpClientAdvancedSettings2.put_RedirectDrives
- IMsRdpClientAdvancedSettings3.RedirectDrives
- IMsRdpClientAdvancedSettings3.get_RedirectDrives
- IMsRdpClientAdvancedSettings3.put_RedirectDrives
- IMsRdpClientAdvancedSettings4.RedirectDrives
- IMsRdpClientAdvancedSettings4.get_RedirectDrives
- IMsRdpClientAdvancedSettings4.put_RedirectDrives
- IMsRdpClientAdvancedSettings5.RedirectDrives
- IMsRdpClientAdvancedSettings5.get_RedirectDrives
- IMsRdpClientAdvancedSettings5.put_RedirectDrives
- IMsRdpClientAdvancedSettings6.RedirectDrives
- IMsRdpClientAdvancedSettings6.get_RedirectDrives
- IMsRdpClientAdvancedSettings6.put_RedirectDrives
- IMsRdpClientAdvancedSettings7.RedirectDrives
- IMsRdpClientAdvancedSettings7.get_RedirectDrives
- IMsRdpClientAdvancedSettings7.put_RedirectDrives
- IMsRdpClientAdvancedSettings8.RedirectDrives
- IMsRdpClientAdvancedSettings8.get_RedirectDrives
- IMsRdpClientAdvancedSettings8.put_RedirectDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c83d24ae4ea4dae2760c1e468f4fa8b326a94c38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803890"
---
# <a name="imsrdpclientadvancedsettingsredirectdrives-property"></a><span data-ttu-id="cde74-120">IMsRdpClientAdvancedSettings:: RedirectDrives (propiedad)</span><span class="sxs-lookup"><span data-stu-id="cde74-120">IMsRdpClientAdvancedSettings::RedirectDrives property</span></span>

<span data-ttu-id="cde74-121">Especifica si se permite la redirección de unidades de disco.</span><span class="sxs-lookup"><span data-stu-id="cde74-121">Specifies if redirection of disk drives is allowed.</span></span>

<span data-ttu-id="cde74-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="cde74-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cde74-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cde74-123">Syntax</span></span>


```C++
HRESULT put_RedirectDrives(
  [in]  VARIANT_BOOL redirectDrives
);

HRESULT get_RedirectDrives(
  [out] VARIANT_BOOL *predirectDrives
);
```



## <a name="property-value"></a><span data-ttu-id="cde74-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="cde74-124">Property value</span></span>

<span data-ttu-id="cde74-125">Establezca este parámetro en **Variant \_ true** para permitir el redireccionamiento o **Variant \_ false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="cde74-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="cde74-126">**Variante \_ TRUE** solicita al usuario que confirme que permite la redirección en el tiempo de conexión, por motivos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="cde74-126">**VARIANT\_TRUE** prompts the user to confirm allowing redirection at connection time, for security purposes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cde74-127">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="cde74-127">Error codes</span></span>

<span data-ttu-id="cde74-128">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="cde74-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="cde74-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cde74-129">Remarks</span></span>

<span data-ttu-id="cde74-130">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="cde74-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cde74-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cde74-131">Requirements</span></span>



| <span data-ttu-id="cde74-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="cde74-132">Requirement</span></span> | <span data-ttu-id="cde74-133">Value</span><span class="sxs-lookup"><span data-stu-id="cde74-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cde74-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cde74-134">Minimum supported client</span></span><br/> | <span data-ttu-id="cde74-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cde74-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="cde74-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cde74-136">Minimum supported server</span></span><br/> | <span data-ttu-id="cde74-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cde74-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="cde74-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="cde74-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="cde74-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cde74-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="cde74-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cde74-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cde74-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cde74-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="cde74-142">IID</span><span class="sxs-lookup"><span data-stu-id="cde74-142">IID</span></span><br/>                      | <span data-ttu-id="cde74-143">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="cde74-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cde74-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="cde74-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cde74-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="cde74-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="cde74-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="cde74-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="cde74-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="cde74-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="cde74-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="cde74-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="cde74-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="cde74-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="cde74-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="cde74-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="cde74-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="cde74-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="cde74-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="cde74-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





