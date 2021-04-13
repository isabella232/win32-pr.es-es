---
title: Propiedad HotKeyAltEsc de IMsRdpClientAdvancedSettings
description: Especifica el código de tecla virtual que se va a agregar a ALT para determinar el reemplazo de la tecla de cambio para ALT + ESC.
ms.assetid: 17cae4ca-8e97-4713-bb4e-ac9a9876c16c
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad HotKeyAltEsc
- Propiedad HotKeyAltEsc Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad HotKeyAltEsc
- Propiedad HotKeyAltEsc Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad HotKeyAltEsc
- Propiedad HotKeyAltEsc Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad HotKeyAltEsc
- Propiedad HotKeyAltEsc Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad HotKeyAltEsc
- Propiedad HotKeyAltEsc Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad HotKeyAltEsc
- Propiedad HotKeyAltEsc Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad HotKeyAltEsc
- Propiedad HotKeyAltEsc Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad HotKeyAltEsc
- Propiedad HotKeyAltEsc Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad HotKeyAltEsc
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltEsc
- IMsRdpClientAdvancedSettings.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings2.HotKeyAltEsc
- IMsRdpClientAdvancedSettings2.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings2.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings3.HotKeyAltEsc
- IMsRdpClientAdvancedSettings3.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings3.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings4.HotKeyAltEsc
- IMsRdpClientAdvancedSettings4.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings4.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings5.HotKeyAltEsc
- IMsRdpClientAdvancedSettings5.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings5.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings6.HotKeyAltEsc
- IMsRdpClientAdvancedSettings6.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings6.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings7.HotKeyAltEsc
- IMsRdpClientAdvancedSettings7.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings7.put_HotKeyAltEsc
- IMsRdpClientAdvancedSettings8.HotKeyAltEsc
- IMsRdpClientAdvancedSettings8.get_HotKeyAltEsc
- IMsRdpClientAdvancedSettings8.put_HotKeyAltEsc
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b661a91a0204177525063629825c478b40b4c29e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493192"
---
# <a name="imsrdpclientadvancedsettingshotkeyaltesc-property"></a><span data-ttu-id="e7497-120">IMsRdpClientAdvancedSettings:: HotKeyAltEsc (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e7497-120">IMsRdpClientAdvancedSettings::HotKeyAltEsc property</span></span>

<span data-ttu-id="e7497-121">Especifica el código de tecla virtual que se va a agregar a ALT para determinar el reemplazo de la tecla de cambio para ALT + ESC.</span><span class="sxs-lookup"><span data-stu-id="e7497-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for ALT+ESC.</span></span>

<span data-ttu-id="e7497-122">Esta propiedad solo es válida cuando la propiedad [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) no está habilitada.</span><span class="sxs-lookup"><span data-stu-id="e7497-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="e7497-123">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="e7497-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7497-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e7497-124">Syntax</span></span>


```C++
HRESULT put_HotKeyAltEsc(
  [in]  LONG hotKeyAltEsc
);

HRESULT get_HotKeyAltEsc(
  [out] LONG *photKeyAltEsc
);
```



## <a name="property-value"></a><span data-ttu-id="e7497-125">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e7497-125">Property value</span></span>

<span data-ttu-id="e7497-126">El nuevo código de tecla virtual.</span><span class="sxs-lookup"><span data-stu-id="e7497-126">The new virtual-key code.</span></span> <span data-ttu-id="e7497-127">**VK \_ INSERT** es el valor predeterminado, con Alt + Insert como la secuencia resultante.</span><span class="sxs-lookup"><span data-stu-id="e7497-127">**VK\_INSERT** is the default value, with ALT+INSERT as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e7497-128">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="e7497-128">Error codes</span></span>

<span data-ttu-id="e7497-129">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="e7497-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7497-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7497-130">Remarks</span></span>

<span data-ttu-id="e7497-131">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e7497-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7497-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7497-132">Requirements</span></span>



| <span data-ttu-id="e7497-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7497-133">Requirement</span></span> | <span data-ttu-id="e7497-134">Value</span><span class="sxs-lookup"><span data-stu-id="e7497-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7497-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7497-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e7497-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e7497-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="e7497-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7497-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e7497-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7497-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="e7497-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e7497-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="e7497-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7497-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="e7497-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e7497-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7497-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7497-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="e7497-143">IID</span><span class="sxs-lookup"><span data-stu-id="e7497-143">IID</span></span><br/>                      | <span data-ttu-id="e7497-144">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="e7497-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e7497-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7497-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7497-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="e7497-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="e7497-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="e7497-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="e7497-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="e7497-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="e7497-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="e7497-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="e7497-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="e7497-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="e7497-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="e7497-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="e7497-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="e7497-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="e7497-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="e7497-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





