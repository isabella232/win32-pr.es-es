---
title: Propiedad HotKeyAltSpace de IMsRdpClientAdvancedSettings
description: Especifica el código de la clave virtual que se va a agregar a la tecla ALT para determinar el reemplazo de la tecla ALT + espacio.
ms.assetid: 943935e9-a6f1-496e-895c-e993755e25cc
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad HotKeyAltSpace
- Propiedad HotKeyAltSpace Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad HotKeyAltSpace
- Propiedad HotKeyAltSpace Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad HotKeyAltSpace
- Propiedad HotKeyAltSpace Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad HotKeyAltSpace
- Propiedad HotKeyAltSpace Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad HotKeyAltSpace
- Propiedad HotKeyAltSpace Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad HotKeyAltSpace
- Propiedad HotKeyAltSpace Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad HotKeyAltSpace
- Propiedad HotKeyAltSpace Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad HotKeyAltSpace
- Propiedad HotKeyAltSpace Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad HotKeyAltSpace
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyAltSpace
- IMsRdpClientAdvancedSettings.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings2.HotKeyAltSpace
- IMsRdpClientAdvancedSettings2.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings2.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings3.HotKeyAltSpace
- IMsRdpClientAdvancedSettings3.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings3.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings4.HotKeyAltSpace
- IMsRdpClientAdvancedSettings4.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings4.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings5.HotKeyAltSpace
- IMsRdpClientAdvancedSettings5.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings5.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings6.HotKeyAltSpace
- IMsRdpClientAdvancedSettings6.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings6.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings7.HotKeyAltSpace
- IMsRdpClientAdvancedSettings7.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings7.put_HotKeyAltSpace
- IMsRdpClientAdvancedSettings8.HotKeyAltSpace
- IMsRdpClientAdvancedSettings8.get_HotKeyAltSpace
- IMsRdpClientAdvancedSettings8.put_HotKeyAltSpace
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6b257bd04171f8bff22bbe91ee7310fafe89c13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996313"
---
# <a name="imsrdpclientadvancedsettingshotkeyaltspace-property"></a><span data-ttu-id="fbf56-120">IMsRdpClientAdvancedSettings:: HotKeyAltSpace (propiedad)</span><span class="sxs-lookup"><span data-stu-id="fbf56-120">IMsRdpClientAdvancedSettings::HotKeyAltSpace property</span></span>

<span data-ttu-id="fbf56-121">Especifica el código de la clave virtual que se va a agregar a la tecla ALT para determinar el reemplazo de la tecla ALT + espacio.</span><span class="sxs-lookup"><span data-stu-id="fbf56-121">Specifies the virtual-key code to add to ALT to determine the hotkey replacement for ALT+SPACE.</span></span>

<span data-ttu-id="fbf56-122">Esta propiedad solo es válida cuando la propiedad [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) no está habilitada.</span><span class="sxs-lookup"><span data-stu-id="fbf56-122">This property is valid only when the [**KeyboardHookMode**](imsrdpclientsecuredsettings-keyboardhookmode.md) property is not enabled.</span></span>

<span data-ttu-id="fbf56-123">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="fbf56-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbf56-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fbf56-124">Syntax</span></span>


```C++
HRESULT put_HotKeyAltSpace(
  [in]  LONG hotKeyAltSpace
);

HRESULT get_HotKeyAltSpace(
  [out] LONG *photKeyAltSpace
);
```



## <a name="property-value"></a><span data-ttu-id="fbf56-125">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="fbf56-125">Property value</span></span>

<span data-ttu-id="fbf56-126">El nuevo código de tecla virtual.</span><span class="sxs-lookup"><span data-stu-id="fbf56-126">The new virtual-key code.</span></span> <span data-ttu-id="fbf56-127">**VK \_ DELETE** es el valor predeterminado, con Alt + Delete como la secuencia resultante.</span><span class="sxs-lookup"><span data-stu-id="fbf56-127">**VK\_DELETE** is the default, with ALT+DELETE as the resulting sequence.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fbf56-128">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="fbf56-128">Error codes</span></span>

<span data-ttu-id="fbf56-129">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="fbf56-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbf56-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fbf56-130">Remarks</span></span>

<span data-ttu-id="fbf56-131">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="fbf56-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fbf56-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbf56-132">Requirements</span></span>



| <span data-ttu-id="fbf56-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbf56-133">Requirement</span></span> | <span data-ttu-id="fbf56-134">Value</span><span class="sxs-lookup"><span data-stu-id="fbf56-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbf56-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbf56-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fbf56-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fbf56-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="fbf56-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbf56-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fbf56-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fbf56-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="fbf56-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fbf56-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="fbf56-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbf56-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="fbf56-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fbf56-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbf56-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbf56-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="fbf56-143">IID</span><span class="sxs-lookup"><span data-stu-id="fbf56-143">IID</span></span><br/>                      | <span data-ttu-id="fbf56-144">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="fbf56-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fbf56-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="fbf56-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbf56-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="fbf56-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="fbf56-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="fbf56-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="fbf56-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="fbf56-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="fbf56-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="fbf56-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="fbf56-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="fbf56-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="fbf56-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="fbf56-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="fbf56-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="fbf56-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="fbf56-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="fbf56-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





