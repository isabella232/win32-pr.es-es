---
title: Propiedad HotKeyAltShiftTab de IMsRdpClientAdvancedSettings
description: Especifica el código de tecla virtual que se va a agregar a ALT para determinar el reemplazo de la tecla de cambio de teclas ALT + MAYÚS + TAB.
ms.assetid: da52f2fb-15cc-4d55-b26e-cf5465290889
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad HotKeyAltShiftTab
- Propiedad HotKeyAltShiftTab Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad HotKeyAltShiftTab
- Propiedad HotKeyAltShiftTab Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad HotKeyAltShiftTab
- Propiedad HotKeyAltShiftTab Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad HotKeyAltShiftTab
- Propiedad HotKeyAltShiftTab Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad HotKeyAltShiftTab
- Propiedad HotKeyAltShiftTab Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad HotKeyAltShiftTab
- Propiedad HotKeyAltShiftTab Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad HotKeyAltShiftTab
- Propiedad HotKeyAltShiftTab Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad HotKeyAltShiftTab
- Propiedad HotKeyAltShiftTab Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad HotKeyAltShiftTab
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings2.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings2.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings2.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings3.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings3.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings3.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings4.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings4.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings4.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings5.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings5.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings5.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings6.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings6.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings6.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings7.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings7.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings7.put_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings8.HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings8.get_HotKeyAltShiftTab
- IMsRdpClientAdvancedSettings8.put_HotKeyAltShiftTab
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9819ddcba3f9cb10450525467eb8accce958c2f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676673"
---
# <a name="imsrdpclientadvancedsettingshotkeyaltshifttab-property"></a><span data-ttu-id="56b7c-120">IMsRdpClientAdvancedSettings:: HotKeyAltShiftTab (propiedad)</span><span class="sxs-lookup"><span data-stu-id="56b7c-120">IMsRdpClientAdvancedSettings::HotKeyAltShiftTab property</span></span>

<span data-ttu-id="56b7c-121">Especifica el código de tecla virtual que se va a agregar a ALT para determinar el reemplazo de la tecla de cambio de teclas ALT + MAYÚS + TAB.</span><span class="sxs-lookup"><span data-stu-id="56b7c-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for ALT+SHIFT+TAB.</span></span>

<span data-ttu-id="56b7c-122">Esta propiedad solo es válida cuando la propiedad [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) no está habilitada.</span><span class="sxs-lookup"><span data-stu-id="56b7c-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="56b7c-123">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="56b7c-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="56b7c-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56b7c-124">Syntax</span></span>


```C++
HRESULT put_HotKeyAltShiftTab(
  [in]  LONG hotKeyAltShiftTab
);

HRESULT get_HotKeyAltShiftTab(
  [out] LONG *photKeyAltShiftTab
);
```



## <a name="property-value"></a><span data-ttu-id="56b7c-125">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="56b7c-125">Property value</span></span>

<span data-ttu-id="56b7c-126">El nuevo código de tecla virtual.</span><span class="sxs-lookup"><span data-stu-id="56b7c-126">The new virtual-key code.</span></span> <span data-ttu-id="56b7c-127">**VK \_ NEXT** es el valor predeterminado, con Alt + Av Pág como la secuencia resultante.</span><span class="sxs-lookup"><span data-stu-id="56b7c-127">**VK\_NEXT** is the default value, with ALT+PAGE DOWN as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="56b7c-128">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="56b7c-128">Error codes</span></span>

<span data-ttu-id="56b7c-129">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="56b7c-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="56b7c-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56b7c-130">Remarks</span></span>

<span data-ttu-id="56b7c-131">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="56b7c-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="56b7c-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56b7c-132">Requirements</span></span>



| <span data-ttu-id="56b7c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="56b7c-133">Requirement</span></span> | <span data-ttu-id="56b7c-134">Value</span><span class="sxs-lookup"><span data-stu-id="56b7c-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56b7c-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56b7c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="56b7c-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56b7c-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="56b7c-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56b7c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="56b7c-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56b7c-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="56b7c-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="56b7c-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="56b7c-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56b7c-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="56b7c-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="56b7c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56b7c-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56b7c-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="56b7c-143">IID</span><span class="sxs-lookup"><span data-stu-id="56b7c-143">IID</span></span><br/>                      | <span data-ttu-id="56b7c-144">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="56b7c-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="56b7c-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="56b7c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56b7c-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="56b7c-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="56b7c-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="56b7c-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="56b7c-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="56b7c-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="56b7c-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="56b7c-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="56b7c-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="56b7c-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="56b7c-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="56b7c-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="56b7c-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="56b7c-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="56b7c-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="56b7c-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





