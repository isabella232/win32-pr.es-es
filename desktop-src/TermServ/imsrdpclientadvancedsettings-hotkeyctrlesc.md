---
title: Propiedad HotKeyCtrlEsc de IMsRdpClientAdvancedSettings
description: Especifica el código de la clave virtual que se va a agregar a la tecla ALT para determinar el reemplazo de la tecla de cambio para CTRL + ESC.
ms.assetid: 55d20a97-ce6e-4394-bfdf-c5bc880e7e2f
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad HotKeyCtrlEsc
- Propiedad HotKeyCtrlEsc Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad HotKeyCtrlEsc
- Propiedad HotKeyCtrlEsc Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad HotKeyCtrlEsc
- Propiedad HotKeyCtrlEsc Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad HotKeyCtrlEsc
- Propiedad HotKeyCtrlEsc Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad HotKeyCtrlEsc
- Propiedad HotKeyCtrlEsc Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad HotKeyCtrlEsc
- Propiedad HotKeyCtrlEsc Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad HotKeyCtrlEsc
- Propiedad HotKeyCtrlEsc Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad HotKeyCtrlEsc
- Propiedad HotKeyCtrlEsc Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad HotKeyCtrlEsc
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings2.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings2.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings2.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings3.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings3.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings3.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings4.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings4.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings4.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings5.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings5.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings5.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings6.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings6.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings6.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings7.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings7.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings7.put_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings8.HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings8.get_HotKeyCtrlEsc
- IMsRdpClientAdvancedSettings8.put_HotKeyCtrlEsc
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1a806430e8b93503c7cdc0fef04ba3f0a59b20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676738"
---
# <a name="imsrdpclientadvancedsettingshotkeyctrlesc-property"></a><span data-ttu-id="1f1ce-120">IMsRdpClientAdvancedSettings:: HotKeyCtrlEsc (propiedad)</span><span class="sxs-lookup"><span data-stu-id="1f1ce-120">IMsRdpClientAdvancedSettings::HotKeyCtrlEsc property</span></span>

<span data-ttu-id="1f1ce-121">Especifica el código de la clave virtual que se va a agregar a la tecla ALT para determinar el reemplazo de la tecla de cambio para CTRL + ESC.</span><span class="sxs-lookup"><span data-stu-id="1f1ce-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for CTRL+ESC.</span></span>

<span data-ttu-id="1f1ce-122">Esta propiedad solo es válida cuando la propiedad [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) no está habilitada.</span><span class="sxs-lookup"><span data-stu-id="1f1ce-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="1f1ce-123">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="1f1ce-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f1ce-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1f1ce-124">Syntax</span></span>


```C++
HRESULT put_HotKeyCtrlEsc(
  [in]  LONG hotKeyCtrlEsc
);

HRESULT get_HotKeyCtrlEsc(
  [out] LONG *photKeyCtrlEsc
);
```



## <a name="property-value"></a><span data-ttu-id="1f1ce-125">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="1f1ce-125">Property value</span></span>

<span data-ttu-id="1f1ce-126">El nuevo código de tecla virtual.</span><span class="sxs-lookup"><span data-stu-id="1f1ce-126">The new virtual-key code.</span></span> <span data-ttu-id="1f1ce-127">**VK \_ Inicio** es el valor predeterminado, con Alt + Inicio como la secuencia resultante.</span><span class="sxs-lookup"><span data-stu-id="1f1ce-127">**VK\_HOME** is the default value, with ALT+HOME as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1f1ce-128">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="1f1ce-128">Error codes</span></span>

<span data-ttu-id="1f1ce-129">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="1f1ce-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f1ce-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1f1ce-130">Remarks</span></span>

<span data-ttu-id="1f1ce-131">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="1f1ce-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1f1ce-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f1ce-132">Requirements</span></span>



| <span data-ttu-id="1f1ce-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f1ce-133">Requirement</span></span> | <span data-ttu-id="1f1ce-134">Value</span><span class="sxs-lookup"><span data-stu-id="1f1ce-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f1ce-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f1ce-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1f1ce-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f1ce-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="1f1ce-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f1ce-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1f1ce-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f1ce-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="1f1ce-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1f1ce-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="1f1ce-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f1ce-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="1f1ce-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1f1ce-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f1ce-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f1ce-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="1f1ce-143">IID</span><span class="sxs-lookup"><span data-stu-id="1f1ce-143">IID</span></span><br/>                      | <span data-ttu-id="1f1ce-144">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="1f1ce-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1f1ce-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="1f1ce-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f1ce-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="1f1ce-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="1f1ce-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="1f1ce-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="1f1ce-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="1f1ce-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="1f1ce-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="1f1ce-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="1f1ce-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="1f1ce-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="1f1ce-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="1f1ce-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="1f1ce-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="1f1ce-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="1f1ce-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="1f1ce-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





