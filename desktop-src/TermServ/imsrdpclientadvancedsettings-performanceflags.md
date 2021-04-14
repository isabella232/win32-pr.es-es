---
title: Propiedad PerformanceFlags de IMsRdpClientAdvancedSettings
description: Especifica un conjunto de características que se pueden establecer en el servidor para mejorar el rendimiento.
ms.assetid: dbbc7c13-ad8a-461d-9d2e-c454bf4b9dea
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad PerformanceFlags
- Propiedad PerformanceFlags Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad PerformanceFlags
- Propiedad PerformanceFlags Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad PerformanceFlags
- Propiedad PerformanceFlags Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad PerformanceFlags
- Propiedad PerformanceFlags Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad PerformanceFlags
- Propiedad PerformanceFlags Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad PerformanceFlags
- Propiedad PerformanceFlags Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad PerformanceFlags
- Propiedad PerformanceFlags Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad PerformanceFlags
- Propiedad PerformanceFlags Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad PerformanceFlags
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.PerformanceFlags
- IMsRdpClientAdvancedSettings.get_PerformanceFlags
- IMsRdpClientAdvancedSettings.put_PerformanceFlags
- IMsRdpClientAdvancedSettings2.PerformanceFlags
- IMsRdpClientAdvancedSettings2.get_PerformanceFlags
- IMsRdpClientAdvancedSettings2.put_PerformanceFlags
- IMsRdpClientAdvancedSettings3.PerformanceFlags
- IMsRdpClientAdvancedSettings3.get_PerformanceFlags
- IMsRdpClientAdvancedSettings3.put_PerformanceFlags
- IMsRdpClientAdvancedSettings4.PerformanceFlags
- IMsRdpClientAdvancedSettings4.get_PerformanceFlags
- IMsRdpClientAdvancedSettings4.put_PerformanceFlags
- IMsRdpClientAdvancedSettings5.PerformanceFlags
- IMsRdpClientAdvancedSettings5.get_PerformanceFlags
- IMsRdpClientAdvancedSettings5.put_PerformanceFlags
- IMsRdpClientAdvancedSettings6.PerformanceFlags
- IMsRdpClientAdvancedSettings6.get_PerformanceFlags
- IMsRdpClientAdvancedSettings6.put_PerformanceFlags
- IMsRdpClientAdvancedSettings7.PerformanceFlags
- IMsRdpClientAdvancedSettings7.get_PerformanceFlags
- IMsRdpClientAdvancedSettings7.put_PerformanceFlags
- IMsRdpClientAdvancedSettings8.PerformanceFlags
- IMsRdpClientAdvancedSettings8.get_PerformanceFlags
- IMsRdpClientAdvancedSettings8.put_PerformanceFlags
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1731afc6d58cede5da055da8cacaf11c8712d3c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422134"
---
# <a name="imsrdpclientadvancedsettingsperformanceflags-property"></a><span data-ttu-id="9c4a9-120">IMsRdpClientAdvancedSettings::P propiedad erformanceFlags</span><span class="sxs-lookup"><span data-stu-id="9c4a9-120">IMsRdpClientAdvancedSettings::PerformanceFlags property</span></span>

<span data-ttu-id="9c4a9-121">Especifica un conjunto de características que se pueden establecer en el servidor para mejorar el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="9c4a9-121">Specifies a set of features that can be set at the server to improve performance.</span></span>

<span data-ttu-id="9c4a9-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="9c4a9-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c4a9-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c4a9-123">Syntax</span></span>


```C++
HRESULT put_PerformanceFlags(
  [in]  LONG DisableList = TS_PERF_DISABLE_NOTHING
);

HRESULT get_PerformanceFlags(
  [out] LONG *pDisableList
);
```



## <a name="property-value"></a><span data-ttu-id="9c4a9-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9c4a9-124">Property value</span></span>

<span data-ttu-id="9c4a9-125">Nuevas marcas.</span><span class="sxs-lookup"><span data-stu-id="9c4a9-125">The new flags.</span></span> <span data-ttu-id="9c4a9-126">El valor predeterminado es 0 (el **rendimiento de TS no \_ \_ deshabilita \_ nada**).</span><span class="sxs-lookup"><span data-stu-id="9c4a9-126">The default is 0 (**TS\_PERF\_DISABLE\_NOTHING**.)</span></span>

<dt>

<span id="TS_PERF_DISABLE_NOTHING"></span><span id="ts_perf_disable_nothing"></span>

<span data-ttu-id="9c4a9-127"><span id="TS_PERF_DISABLE_NOTHING"></span><span id="ts_perf_disable_nothing"></span>**TS \_ PERF \_ deshabilitar \_ nada** (0x00000000)</span><span class="sxs-lookup"><span data-stu-id="9c4a9-127"><span id="TS_PERF_DISABLE_NOTHING"></span><span id="ts_perf_disable_nothing"></span>**TS\_PERF\_DISABLE\_NOTHING** (0x00000000)</span></span>


</dt> <dd>

<span data-ttu-id="9c4a9-128">No hay características deshabilitadas.</span><span class="sxs-lookup"><span data-stu-id="9c4a9-128">No features are disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_WALLPAPER"></span><span id="ts_perf_disable_wallpaper"></span>

<span data-ttu-id="9c4a9-129"><span id="TS_PERF_DISABLE_WALLPAPER"></span><span id="ts_perf_disable_wallpaper"></span>**TS \_ \_ \_ Papel tapiz de deshabilitación de rendimiento** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="9c4a9-129"><span id="TS_PERF_DISABLE_WALLPAPER"></span><span id="ts_perf_disable_wallpaper"></span>**TS\_PERF\_DISABLE\_WALLPAPER** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="9c4a9-130">No se muestra el papel tapiz en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="9c4a9-130">Wallpaper on the desktop is not displayed.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_FULLWINDOWDRAG"></span><span id="ts_perf_disable_fullwindowdrag"></span>

<span data-ttu-id="9c4a9-131"><span id="TS_PERF_DISABLE_FULLWINDOWDRAG"></span><span id="ts_perf_disable_fullwindowdrag"></span>**TS \_ \_Deshabilitar \_ FULLWINDOWDRAG de rendimiento** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="9c4a9-131"><span id="TS_PERF_DISABLE_FULLWINDOWDRAG"></span><span id="ts_perf_disable_fullwindowdrag"></span>**TS\_PERF\_DISABLE\_FULLWINDOWDRAG** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="9c4a9-132">La arrastre de la ventana completa está deshabilitada; solo se muestra el esquema de la ventana cuando se mueve la ventana.</span><span class="sxs-lookup"><span data-stu-id="9c4a9-132">Full-window drag is disabled; only the window outline is displayed when the window is moved.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_MENUANIMATIONS"></span><span id="ts_perf_disable_menuanimations"></span>

<span data-ttu-id="9c4a9-133"><span id="TS_PERF_DISABLE_MENUANIMATIONS"></span><span id="ts_perf_disable_menuanimations"></span>**TS \_ \_Deshabilitar \_ MENUANIMATIONS de rendimiento** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="9c4a9-133"><span id="TS_PERF_DISABLE_MENUANIMATIONS"></span><span id="ts_perf_disable_menuanimations"></span>**TS\_PERF\_DISABLE\_MENUANIMATIONS** (0x00000004)</span></span>


</dt> <dd>

<span data-ttu-id="9c4a9-134">Las animaciones de menú están deshabilitadas.</span><span class="sxs-lookup"><span data-stu-id="9c4a9-134">Menu animations are disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_THEMING"></span><span id="ts_perf_disable_theming"></span>

<span data-ttu-id="9c4a9-135"><span id="TS_PERF_DISABLE_THEMING"></span><span id="ts_perf_disable_theming"></span>**TS \_ \_Deshabilitar \_ la deshabilitación de rendimiento** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="9c4a9-135"><span id="TS_PERF_DISABLE_THEMING"></span><span id="ts_perf_disable_theming"></span>**TS\_PERF\_DISABLE\_THEMING** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="9c4a9-136">Los temas están deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="9c4a9-136">Themes are disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_ENABLE_ENHANCED_GRAPHICS"></span><span id="ts_perf_enable_enhanced_graphics"></span>

<span data-ttu-id="9c4a9-137"><span id="TS_PERF_ENABLE_ENHANCED_GRAPHICS"></span><span id="ts_perf_enable_enhanced_graphics"></span>**TS \_ \_Habilitar \_ gráficos mejorados** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="9c4a9-137"><span id="TS_PERF_ENABLE_ENHANCED_GRAPHICS"></span><span id="ts_perf_enable_enhanced_graphics"></span>**TS\_PERF\_ENABLE\_ENHANCED GRAPHICS** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="9c4a9-138">Habilitar gráficos mejorados.</span><span class="sxs-lookup"><span data-stu-id="9c4a9-138">Enable enhanced graphics.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_CURSOR_SHADOW"></span><span id="ts_perf_disable_cursor_shadow"></span>

<span data-ttu-id="9c4a9-139"><span id="TS_PERF_DISABLE_CURSOR_SHADOW"></span><span id="ts_perf_disable_cursor_shadow"></span>**TS \_ \_Sombra de \_ cursor \_ de deshabilitación de rendimiento** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="9c4a9-139"><span id="TS_PERF_DISABLE_CURSOR_SHADOW"></span><span id="ts_perf_disable_cursor_shadow"></span>**TS\_PERF\_DISABLE\_CURSOR\_SHADOW** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="9c4a9-140">No se muestra ninguna sombra para el cursor.</span><span class="sxs-lookup"><span data-stu-id="9c4a9-140">No shadow is displayed for the cursor.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_CURSORSETTINGS"></span><span id="ts_perf_disable_cursorsettings"></span>

<span data-ttu-id="9c4a9-141"><span id="TS_PERF_DISABLE_CURSORSETTINGS"></span><span id="ts_perf_disable_cursorsettings"></span>**TS \_ \_Deshabilitar \_ CURSORSETTINGS de rendimiento** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="9c4a9-141"><span id="TS_PERF_DISABLE_CURSORSETTINGS"></span><span id="ts_perf_disable_cursorsettings"></span>**TS\_PERF\_DISABLE\_CURSORSETTINGS** (0x00000040)</span></span>


</dt> <dd>

<span data-ttu-id="9c4a9-142">El parpadeo del cursor está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="9c4a9-142">Cursor blinking is disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_ENABLE_FONT_SMOOTHING"></span><span id="ts_perf_enable_font_smoothing"></span>

<span data-ttu-id="9c4a9-143"><span id="TS_PERF_ENABLE_FONT_SMOOTHING"></span><span id="ts_perf_enable_font_smoothing"></span>**TS \_ \_Habilitar el \_ \_ suavizado de fuentes** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="9c4a9-143"><span id="TS_PERF_ENABLE_FONT_SMOOTHING"></span><span id="ts_perf_enable_font_smoothing"></span>**TS\_PERF\_ENABLE\_FONT\_SMOOTHING** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="9c4a9-144">Habilitar el suavizado de fuentes.</span><span class="sxs-lookup"><span data-stu-id="9c4a9-144">Enable font smoothing.</span></span>

</dd> <dt>

<span id="TS_PERF_ENABLE_DESKTOP_COMPOSITION"></span><span id="ts_perf_enable_desktop_composition"></span>

<span data-ttu-id="9c4a9-145"><span id="TS_PERF_ENABLE_DESKTOP_COMPOSITION"></span><span id="ts_perf_enable_desktop_composition"></span>**TS \_ \_Habilitar la \_ \_ composición de escritorio** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="9c4a9-145"><span id="TS_PERF_ENABLE_DESKTOP_COMPOSITION"></span><span id="ts_perf_enable_desktop_composition"></span>**TS\_PERF\_ENABLE\_DESKTOP\_COMPOSITION** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="9c4a9-146">Habilitar composición de escritorio.</span><span class="sxs-lookup"><span data-stu-id="9c4a9-146">Enable desktop composition.</span></span>

</dd> <dt>

<span id="TS_PERF_DEFAULT_NONPERFCLIENT_SETTING"></span><span id="ts_perf_default_nonperfclient_setting"></span>

<span data-ttu-id="9c4a9-147"><span id="TS_PERF_DEFAULT_NONPERFCLIENT_SETTING"></span><span id="ts_perf_default_nonperfclient_setting"></span>**TS \_ \_Configuración de \_ NONPERFCLIENT \_ predeterminada de rendimiento** (0x40000000)</span><span class="sxs-lookup"><span data-stu-id="9c4a9-147"><span id="TS_PERF_DEFAULT_NONPERFCLIENT_SETTING"></span><span id="ts_perf_default_nonperfclient_setting"></span>**TS\_PERF\_DEFAULT\_NONPERFCLIENT\_SETTING** (0x40000000)</span></span>


</dt> <dd>

<span data-ttu-id="9c4a9-148">Se establece internamente para los clientes que no tienen en cuenta esta configuración.</span><span class="sxs-lookup"><span data-stu-id="9c4a9-148">Set internally for clients not aware of this setting.</span></span>

</dd> <dt>

<span id="TS_PERF_RESERVED1"></span><span id="ts_perf_reserved1"></span>

<span data-ttu-id="9c4a9-149"><span id="TS_PERF_RESERVED1"></span><span id="ts_perf_reserved1"></span>**TS \_ RENDIMIENTO \_ RESERVED1** (0x80000000)</span><span class="sxs-lookup"><span data-stu-id="9c4a9-149"><span id="TS_PERF_RESERVED1"></span><span id="ts_perf_reserved1"></span>**TS\_PERF\_RESERVED1** (0x80000000)</span></span>


</dt> <dd>

<span data-ttu-id="9c4a9-150">Reservada y usada internamente por el cliente.</span><span class="sxs-lookup"><span data-stu-id="9c4a9-150">Reserved and used internally by the client.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="9c4a9-151">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="9c4a9-151">Error codes</span></span>

<span data-ttu-id="9c4a9-152">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="9c4a9-152">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c4a9-153">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c4a9-153">Remarks</span></span>

<span data-ttu-id="9c4a9-154">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9c4a9-154">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c4a9-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c4a9-155">Requirements</span></span>



| <span data-ttu-id="9c4a9-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c4a9-156">Requirement</span></span> | <span data-ttu-id="9c4a9-157">Value</span><span class="sxs-lookup"><span data-stu-id="9c4a9-157">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c4a9-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c4a9-158">Minimum supported client</span></span><br/> | <span data-ttu-id="9c4a9-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c4a9-159">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="9c4a9-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c4a9-160">Minimum supported server</span></span><br/> | <span data-ttu-id="9c4a9-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c4a9-161">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="9c4a9-162">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9c4a9-162">Type library</span></span><br/>             | <dl> <span data-ttu-id="9c4a9-163"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c4a9-163"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="9c4a9-164">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9c4a9-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c4a9-165"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c4a9-165"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="9c4a9-166">IID</span><span class="sxs-lookup"><span data-stu-id="9c4a9-166">IID</span></span><br/>                      | <span data-ttu-id="9c4a9-167">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="9c4a9-167">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9c4a9-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c4a9-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c4a9-169">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="9c4a9-169">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="9c4a9-170">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="9c4a9-170">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="9c4a9-171">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="9c4a9-171">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="9c4a9-172">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="9c4a9-172">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="9c4a9-173">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="9c4a9-173">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="9c4a9-174">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="9c4a9-174">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="9c4a9-175">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="9c4a9-175">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="9c4a9-176">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="9c4a9-176">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





