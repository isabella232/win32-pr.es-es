---
title: Propiedad HotKeyCtrlAltDel de IMsRdpClientAdvancedSettings
description: Especifica el código de tecla virtual que se va a agregar a CTRL + ALT para determinar el reemplazo de la tecla de método abreviado para CTRL + ALT + SUPR, también denominado secuencia de atención segura (SAS).
ms.assetid: bce55cdb-4444-4291-b443-9bc1b3743e23
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad HotKeyCtrlAltDel
- Propiedad HotKeyCtrlAltDel Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad HotKeyCtrlAltDel
- Propiedad HotKeyCtrlAltDel Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad HotKeyCtrlAltDel
- Propiedad HotKeyCtrlAltDel Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad HotKeyCtrlAltDel
- Propiedad HotKeyCtrlAltDel Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad HotKeyCtrlAltDel
- Propiedad HotKeyCtrlAltDel Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad HotKeyCtrlAltDel
- Propiedad HotKeyCtrlAltDel Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad HotKeyCtrlAltDel
- Propiedad HotKeyCtrlAltDel Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad HotKeyCtrlAltDel
- Propiedad HotKeyCtrlAltDel Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad HotKeyCtrlAltDel
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings2.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings3.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings4.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings5.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings6.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings7.put_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.get_HotKeyCtrlAltDel
- IMsRdpClientAdvancedSettings8.put_HotKeyCtrlAltDel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00fa4c1f963841d0c1ea0375cdf11913b28d0286
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422004"
---
# <a name="imsrdpclientadvancedsettingshotkeyctrlaltdel-property"></a><span data-ttu-id="ecae6-120">IMsRdpClientAdvancedSettings:: HotKeyCtrlAltDel (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ecae6-120">IMsRdpClientAdvancedSettings::HotKeyCtrlAltDel property</span></span>

<span data-ttu-id="ecae6-121">Especifica el código de tecla virtual que se va a agregar a CTRL + ALT para determinar el reemplazo de la tecla de método abreviado para CTRL + ALT + SUPR, también denominado secuencia de atención segura (SAS).</span><span class="sxs-lookup"><span data-stu-id="ecae6-121">Specifies the virtual-key code to add to CTRL+ALT to determine the hotkey replacement for CTRL+ALT+DELETE, also called the secure attention sequence (SAS).</span></span>

> [!Note]  
> <span data-ttu-id="ecae6-122">CTRL + ALT + SUPR nunca se redirige al servidor remoto, incluso cuando la propiedad [KeyboardHookMode](imsrdpclientsecuredsettings-keyboardhookmode.md) está habilitada; CTRL + ALT + SUPR es la secuencia SAS local.</span><span class="sxs-lookup"><span data-stu-id="ecae6-122">CTRL+ALT+DELETE is never redirected to the remote server, even when the [KeyboardHookMode](imsrdpclientsecuredsettings-keyboardhookmode.md) property is enabled; CTRL+ALT+DELETE is the local SAS sequence.</span></span>

 

<span data-ttu-id="ecae6-123">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ecae6-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecae6-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ecae6-124">Syntax</span></span>


```C++
HRESULT put_HotKeyCtrlAltDel(
  [in]  LONG hotKeyCtrlAltDel
);

HRESULT get_HotKeyCtrlAltDel(
  [out] LONG *photKeyCtrlAltDel
);
```



## <a name="property-value"></a><span data-ttu-id="ecae6-125">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ecae6-125">Property value</span></span>

<span data-ttu-id="ecae6-126">El nuevo código de tecla virtual.</span><span class="sxs-lookup"><span data-stu-id="ecae6-126">The new virtual-key code.</span></span> <span data-ttu-id="ecae6-127">**VK \_ END** es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ecae6-127">**VK\_END** is the default.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ecae6-128">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="ecae6-128">Error codes</span></span>

<span data-ttu-id="ecae6-129">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="ecae6-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecae6-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ecae6-130">Remarks</span></span>

<span data-ttu-id="ecae6-131">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ecae6-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ecae6-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecae6-132">Requirements</span></span>



| <span data-ttu-id="ecae6-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecae6-133">Requirement</span></span> | <span data-ttu-id="ecae6-134">Value</span><span class="sxs-lookup"><span data-stu-id="ecae6-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecae6-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecae6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ecae6-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ecae6-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="ecae6-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecae6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ecae6-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ecae6-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="ecae6-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ecae6-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="ecae6-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecae6-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ecae6-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ecae6-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ecae6-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ecae6-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ecae6-143">IID</span><span class="sxs-lookup"><span data-stu-id="ecae6-143">IID</span></span><br/>                      | <span data-ttu-id="ecae6-144">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="ecae6-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ecae6-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="ecae6-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecae6-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="ecae6-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="ecae6-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="ecae6-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="ecae6-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="ecae6-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="ecae6-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="ecae6-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="ecae6-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ecae6-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="ecae6-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ecae6-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ecae6-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ecae6-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ecae6-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="ecae6-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





