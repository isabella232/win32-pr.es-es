---
title: Propiedad RedirectPorts de IMsRdpClientAdvancedSettings
description: Especifica si se permite la redirección de puertos locales (por ejemplo, COM y LPT).
ms.assetid: 85e1e40d-8da7-4333-ae96-2bfa44479267
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RedirectPorts
- Propiedad RedirectPorts Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad RedirectPorts
- Propiedad RedirectPorts Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad RedirectPorts
- Propiedad RedirectPorts Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad RedirectPorts
- Propiedad RedirectPorts Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad RedirectPorts
- Propiedad RedirectPorts Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad RedirectPorts
- Propiedad RedirectPorts Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad RedirectPorts
- Propiedad RedirectPorts Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad RedirectPorts
- Propiedad RedirectPorts Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad RedirectPorts
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectPorts
- IMsRdpClientAdvancedSettings.get_RedirectPorts
- IMsRdpClientAdvancedSettings.put_RedirectPorts
- IMsRdpClientAdvancedSettings2.RedirectPorts
- IMsRdpClientAdvancedSettings2.get_RedirectPorts
- IMsRdpClientAdvancedSettings2.put_RedirectPorts
- IMsRdpClientAdvancedSettings3.RedirectPorts
- IMsRdpClientAdvancedSettings3.get_RedirectPorts
- IMsRdpClientAdvancedSettings3.put_RedirectPorts
- IMsRdpClientAdvancedSettings4.RedirectPorts
- IMsRdpClientAdvancedSettings4.get_RedirectPorts
- IMsRdpClientAdvancedSettings4.put_RedirectPorts
- IMsRdpClientAdvancedSettings5.RedirectPorts
- IMsRdpClientAdvancedSettings5.get_RedirectPorts
- IMsRdpClientAdvancedSettings5.put_RedirectPorts
- IMsRdpClientAdvancedSettings6.RedirectPorts
- IMsRdpClientAdvancedSettings6.get_RedirectPorts
- IMsRdpClientAdvancedSettings6.put_RedirectPorts
- IMsRdpClientAdvancedSettings7.RedirectPorts
- IMsRdpClientAdvancedSettings7.get_RedirectPorts
- IMsRdpClientAdvancedSettings7.put_RedirectPorts
- IMsRdpClientAdvancedSettings8.RedirectPorts
- IMsRdpClientAdvancedSettings8.get_RedirectPorts
- IMsRdpClientAdvancedSettings8.put_RedirectPorts
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 714b26081bb4caadface283553b1dd3ebd91192d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995947"
---
# <a name="imsrdpclientadvancedsettingsredirectports-property"></a><span data-ttu-id="f7c45-120">IMsRdpClientAdvancedSettings:: RedirectPorts (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f7c45-120">IMsRdpClientAdvancedSettings::RedirectPorts property</span></span>

<span data-ttu-id="f7c45-121">Especifica si se permite la redirección de puertos locales (por ejemplo, COM y LPT).</span><span class="sxs-lookup"><span data-stu-id="f7c45-121">Specifies if redirection of local ports (for example, COM and LPT) is allowed.</span></span>

<span data-ttu-id="f7c45-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f7c45-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7c45-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f7c45-123">Syntax</span></span>


```C++
HRESULT put_RedirectPorts(
  [in]  VARIANT_BOOL redirectPorts
);

HRESULT get_RedirectPorts(
  [out] VARIANT_BOOL *predirectPorts
);
```



## <a name="property-value"></a><span data-ttu-id="f7c45-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f7c45-124">Property value</span></span>

<span data-ttu-id="f7c45-125">Establezca este parámetro en **Variant \_ true** para permitir el redireccionamiento o **Variant \_ false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f7c45-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span> <span data-ttu-id="f7c45-126">**Variante \_ TRUE** solicita al usuario que confirme que permite la redirección en el tiempo de conexión, por motivos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f7c45-126">**VARIANT\_TRUE** prompts the user to confirm allowing redirection at connection time, for security purposes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f7c45-127">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="f7c45-127">Error codes</span></span>

<span data-ttu-id="f7c45-128">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="f7c45-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7c45-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f7c45-129">Remarks</span></span>

<span data-ttu-id="f7c45-130">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f7c45-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7c45-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7c45-131">Requirements</span></span>



| <span data-ttu-id="f7c45-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7c45-132">Requirement</span></span> | <span data-ttu-id="f7c45-133">Value</span><span class="sxs-lookup"><span data-stu-id="f7c45-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7c45-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7c45-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f7c45-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7c45-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="f7c45-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7c45-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f7c45-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7c45-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="f7c45-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f7c45-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="f7c45-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7c45-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f7c45-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f7c45-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7c45-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7c45-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f7c45-142">IID</span><span class="sxs-lookup"><span data-stu-id="f7c45-142">IID</span></span><br/>                      | <span data-ttu-id="f7c45-143">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="f7c45-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f7c45-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7c45-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7c45-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="f7c45-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="f7c45-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="f7c45-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="f7c45-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="f7c45-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="f7c45-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="f7c45-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="f7c45-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="f7c45-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="f7c45-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="f7c45-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="f7c45-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="f7c45-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="f7c45-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="f7c45-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





