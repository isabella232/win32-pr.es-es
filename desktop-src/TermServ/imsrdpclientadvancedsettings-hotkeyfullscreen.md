---
title: Propiedad HotKeyFullScreen de IMsRdpClientAdvancedSettings
description: Especifica el código de tecla virtual que se va a agregar a CTRL + ALT para determinar el reemplazo de la tecla de cambio de teclas para cambiar al modo de pantalla completa.
ms.assetid: 75fda212-ec68-4b68-b7db-2bfcdee7a7de
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad HotKeyFullScreen
- Propiedad HotKeyFullScreen Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad HotKeyFullScreen
- Propiedad HotKeyFullScreen Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad HotKeyFullScreen
- Propiedad HotKeyFullScreen Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad HotKeyFullScreen
- Propiedad HotKeyFullScreen Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad HotKeyFullScreen
- Propiedad HotKeyFullScreen Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad HotKeyFullScreen
- Propiedad HotKeyFullScreen Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad HotKeyFullScreen
- Propiedad HotKeyFullScreen Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad HotKeyFullScreen
- Propiedad HotKeyFullScreen Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad HotKeyFullScreen
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.HotKeyFullScreen
- IMsRdpClientAdvancedSettings.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings2.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings3.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings4.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings5.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings6.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings7.put_HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.get_HotKeyFullScreen
- IMsRdpClientAdvancedSettings8.put_HotKeyFullScreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9c53dd0c6dff9e47b87ea8c8697c20b3613a14
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996017"
---
# <a name="imsrdpclientadvancedsettingshotkeyfullscreen-property"></a><span data-ttu-id="8db83-120">IMsRdpClientAdvancedSettings:: HotKeyFullScreen (propiedad)</span><span class="sxs-lookup"><span data-stu-id="8db83-120">IMsRdpClientAdvancedSettings::HotKeyFullScreen property</span></span>

<span data-ttu-id="8db83-121">Especifica el código de tecla virtual que se va a agregar a CTRL + ALT para determinar el reemplazo de la tecla de cambio de teclas para cambiar al modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="8db83-121">Specifies the virtual-key code to add to CTRL+ALT to determine the hotkey replacement for switching to full-screen mode.</span></span>

<span data-ttu-id="8db83-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="8db83-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8db83-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8db83-123">Syntax</span></span>


```C++
HRESULT put_HotKeyFullScreen(
  [in]  LONG hotKeyFullScreen
);

HRESULT get_HotKeyFullScreen(
  [out] LONG *photKeyFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="8db83-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8db83-124">Property value</span></span>

<span data-ttu-id="8db83-125">El nuevo código de tecla virtual.</span><span class="sxs-lookup"><span data-stu-id="8db83-125">The new virtual-key code.</span></span> <span data-ttu-id="8db83-126">**VK \_ CANCEL** es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="8db83-126">**VK\_CANCEL** is the default value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8db83-127">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="8db83-127">Error codes</span></span>

<span data-ttu-id="8db83-128">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="8db83-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="8db83-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8db83-129">Remarks</span></span>

<span data-ttu-id="8db83-130">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="8db83-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8db83-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8db83-131">Requirements</span></span>



| <span data-ttu-id="8db83-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="8db83-132">Requirement</span></span> | <span data-ttu-id="8db83-133">Value</span><span class="sxs-lookup"><span data-stu-id="8db83-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8db83-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8db83-134">Minimum supported client</span></span><br/> | <span data-ttu-id="8db83-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8db83-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="8db83-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8db83-136">Minimum supported server</span></span><br/> | <span data-ttu-id="8db83-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8db83-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="8db83-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8db83-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="8db83-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8db83-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="8db83-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8db83-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8db83-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8db83-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="8db83-142">IID</span><span class="sxs-lookup"><span data-stu-id="8db83-142">IID</span></span><br/>                      | <span data-ttu-id="8db83-143">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="8db83-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8db83-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="8db83-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8db83-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="8db83-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="8db83-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="8db83-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="8db83-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="8db83-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="8db83-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="8db83-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="8db83-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="8db83-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="8db83-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="8db83-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="8db83-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="8db83-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="8db83-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="8db83-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





