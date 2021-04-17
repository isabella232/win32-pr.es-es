---
title: Propiedad HotKeyAltTab de IMsRdpClientAdvancedSettings
description: Especifica el código de tecla virtual que se va a agregar a ALT para determinar el reemplazo de la tecla de cambio de teclas ALT + TAB.
ms.assetid: d7066fb4-f53f-4e55-ba12-fb4078ece144
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad HotKeyAltTab
- Propiedad HotKeyAltTab Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad HotKeyAltTab
- Propiedad HotKeyAltTab Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad HotKeyAltTab
- Propiedad HotKeyAltTab Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad HotKeyAltTab
- Propiedad HotKeyAltTab Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad HotKeyAltTab
- Propiedad HotKeyAltTab Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad HotKeyAltTab
- Propiedad HotKeyAltTab Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad HotKeyAltTab
- Propiedad HotKeyAltTab Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad HotKeyAltTab
- Propiedad HotKeyAltTab Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad HotKeyAltTab
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltTab
- IMsRdpClientAdvancedSettings.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings2.HotKeyAltTab
- IMsRdpClientAdvancedSettings2.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings2.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings3.HotKeyAltTab
- IMsRdpClientAdvancedSettings3.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings3.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings4.HotKeyAltTab
- IMsRdpClientAdvancedSettings4.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings4.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings5.HotKeyAltTab
- IMsRdpClientAdvancedSettings5.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings5.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings6.HotKeyAltTab
- IMsRdpClientAdvancedSettings6.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings6.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings7.HotKeyAltTab
- IMsRdpClientAdvancedSettings7.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings7.put_HotKeyAltTab
- IMsRdpClientAdvancedSettings8.HotKeyAltTab
- IMsRdpClientAdvancedSettings8.get_HotKeyAltTab
- IMsRdpClientAdvancedSettings8.put_HotKeyAltTab
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eec7834a95b83ec43553d0ced1e056860cfb5abe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422140"
---
# <a name="imsrdpclientadvancedsettingshotkeyalttab-property"></a><span data-ttu-id="f6aa5-120">IMsRdpClientAdvancedSettings:: HotKeyAltTab (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f6aa5-120">IMsRdpClientAdvancedSettings::HotKeyAltTab property</span></span>

<span data-ttu-id="f6aa5-121">Especifica el código de tecla virtual que se va a agregar a ALT para determinar el reemplazo de la tecla de cambio de teclas ALT + TAB.</span><span class="sxs-lookup"><span data-stu-id="f6aa5-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for ALT+TAB.</span></span>

<span data-ttu-id="f6aa5-122">Esta propiedad solo es válida cuando la propiedad [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) no está habilitada.</span><span class="sxs-lookup"><span data-stu-id="f6aa5-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="f6aa5-123">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="f6aa5-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6aa5-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6aa5-124">Syntax</span></span>


```C++
HRESULT put_HotKeyAltTab(
  [in]  LONG hotKeyAltTab
);

HRESULT get_HotKeyAltTab(
  [out] LONG *photKeyAltTab
);
```



## <a name="property-value"></a><span data-ttu-id="f6aa5-125">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f6aa5-125">Property value</span></span>

<span data-ttu-id="f6aa5-126">El nuevo código de tecla virtual.</span><span class="sxs-lookup"><span data-stu-id="f6aa5-126">The new virtual-key code.</span></span> <span data-ttu-id="f6aa5-127">**VK \_ ANTES** es el valor predeterminado, con Alt + Re Pág como la secuencia resultante.</span><span class="sxs-lookup"><span data-stu-id="f6aa5-127">**VK\_PRIOR** is the default value, with ALT+PAGE UP as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f6aa5-128">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="f6aa5-128">Error codes</span></span>

<span data-ttu-id="f6aa5-129">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="f6aa5-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6aa5-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6aa5-130">Remarks</span></span>

<span data-ttu-id="f6aa5-131">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f6aa5-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6aa5-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6aa5-132">Requirements</span></span>



| <span data-ttu-id="f6aa5-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6aa5-133">Requirement</span></span> | <span data-ttu-id="f6aa5-134">Value</span><span class="sxs-lookup"><span data-stu-id="f6aa5-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6aa5-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6aa5-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f6aa5-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f6aa5-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="f6aa5-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6aa5-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f6aa5-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f6aa5-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="f6aa5-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f6aa5-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="f6aa5-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6aa5-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f6aa5-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f6aa5-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6aa5-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6aa5-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="f6aa5-143">IID</span><span class="sxs-lookup"><span data-stu-id="f6aa5-143">IID</span></span><br/>                      | <span data-ttu-id="f6aa5-144">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="f6aa5-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f6aa5-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6aa5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6aa5-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="f6aa5-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="f6aa5-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="f6aa5-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="f6aa5-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="f6aa5-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="f6aa5-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="f6aa5-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="f6aa5-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="f6aa5-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="f6aa5-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="f6aa5-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="f6aa5-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="f6aa5-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="f6aa5-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="f6aa5-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





