---
title: Propiedad PluginDlls de IMsTscAdvancedSettings
description: Especifica los nombres de los archivos dll de cliente de canal virtual que se van a cargar.
ms.assetid: 4b248fb8-200a-4ce0-8c8e-ce1692a80d88
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad PluginDlls
- Propiedad PluginDlls Servicios de Escritorio remoto, interfaz IMsTscAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsTscAdvancedSettings, propiedad PluginDlls
- Propiedad PluginDlls Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad PluginDlls
- Propiedad PluginDlls Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad PluginDlls
- Propiedad PluginDlls Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad PluginDlls
- Propiedad PluginDlls Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad PluginDlls
- Propiedad PluginDlls Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad PluginDlls
- Propiedad PluginDlls Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad PluginDlls
- Propiedad PluginDlls Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad PluginDlls
- Propiedad PluginDlls Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad PluginDlls
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.PluginDlls
- IMsTscAdvancedSettings.put_PluginDlls
- IMsRdpClientAdvancedSettings.PluginDlls
- IMsRdpClientAdvancedSettings.put_PluginDlls
- IMsRdpClientAdvancedSettings2.PluginDlls
- IMsRdpClientAdvancedSettings2.put_PluginDlls
- IMsRdpClientAdvancedSettings3.PluginDlls
- IMsRdpClientAdvancedSettings3.put_PluginDlls
- IMsRdpClientAdvancedSettings4.PluginDlls
- IMsRdpClientAdvancedSettings4.put_PluginDlls
- IMsRdpClientAdvancedSettings5.PluginDlls
- IMsRdpClientAdvancedSettings5.put_PluginDlls
- IMsRdpClientAdvancedSettings6.PluginDlls
- IMsRdpClientAdvancedSettings6.put_PluginDlls
- IMsRdpClientAdvancedSettings7.PluginDlls
- IMsRdpClientAdvancedSettings7.put_PluginDlls
- IMsRdpClientAdvancedSettings8.PluginDlls
- IMsRdpClientAdvancedSettings8.put_PluginDlls
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3ef2e518145ae34533477bcbefb92e15d9c8d94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490636"
---
# <a name="imstscadvancedsettingsplugindlls-property"></a><span data-ttu-id="c51bd-122">IMsTscAdvancedSettings::P propiedad luginDlls</span><span class="sxs-lookup"><span data-stu-id="c51bd-122">IMsTscAdvancedSettings::PluginDlls property</span></span>

<span data-ttu-id="c51bd-123">Especifica los nombres de los archivos dll de cliente de canal virtual que se van a cargar.</span><span class="sxs-lookup"><span data-stu-id="c51bd-123">Specifies the names of virtual channel client DLLs to be loaded.</span></span> <span data-ttu-id="c51bd-124">Los archivos dll de cliente de canal virtual también se conocen como archivos dll de complemento.</span><span class="sxs-lookup"><span data-stu-id="c51bd-124">Virtual channel client DLLs are also referred to as Plug-in DLLs.</span></span>

<span data-ttu-id="c51bd-125">Esta propiedad es de solo escritura.</span><span class="sxs-lookup"><span data-stu-id="c51bd-125">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c51bd-126">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c51bd-126">Syntax</span></span>


```C++
HRESULT put_PluginDlls(
  [in] BSTR PluginDlls
);
```



## <a name="property-value"></a><span data-ttu-id="c51bd-127">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c51bd-127">Property value</span></span>

<span data-ttu-id="c51bd-128">Lista separada por comas de los nombres de los archivos dll de cliente de canal virtual que se van a cargar.</span><span class="sxs-lookup"><span data-stu-id="c51bd-128">Comma-separated list of the names of the virtual channel client DLLs to be loaded.</span></span> <span data-ttu-id="c51bd-129">Los nombres de los archivos DLL solo deben contener caracteres alfanuméricos.</span><span class="sxs-lookup"><span data-stu-id="c51bd-129">The DLL names must contain only alphanumeric characters.</span></span> <span data-ttu-id="c51bd-130">Para obtener más información acerca del formato de estos nombres, consulte [registro del complemento de DVC](dvc-plug-in-registration.md).</span><span class="sxs-lookup"><span data-stu-id="c51bd-130">For more information about the format of these names, see [DVC plug-in registration](dvc-plug-in-registration.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="c51bd-131">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="c51bd-131">Error codes</span></span>

<span data-ttu-id="c51bd-132">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="c51bd-132">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c51bd-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c51bd-133">Remarks</span></span>

<span data-ttu-id="c51bd-134">Por motivos de seguridad, si el control se hospeda en una página web, la propiedad **PluginDlls** solo acepta una lista con nombre de archivos dll de cliente de canal virtual.</span><span class="sxs-lookup"><span data-stu-id="c51bd-134">For security reasons, if the control is hosted in a webpage the **PluginDlls** property only accepts a named list of virtual channel client DLLs.</span></span> <span data-ttu-id="c51bd-135">El control devuelve un error si se especifica un sistema de archivos o una ruta de acceso UNC.</span><span class="sxs-lookup"><span data-stu-id="c51bd-135">The control returns an error if a file system or UNC path is specified.</span></span>

<span data-ttu-id="c51bd-136">Los archivos dll de cliente de canal virtual a los que se tendrá acceso desde una página web deben instalarse en el directorio "% WinDir% \\ system32", ya que el control ActiveX escritorio remoto solo tiene acceso a los archivos dll de esa ubicación.</span><span class="sxs-lookup"><span data-stu-id="c51bd-136">Virtual channel client DLLs that will be accessed from a webpage must be installed in the "%WinDir%\\system32" directory because the Remote Desktop ActiveX control only accesses DLL files in that location.</span></span> <span data-ttu-id="c51bd-137">Si el control no está hospedado en una página web, esta restricción de seguridad no existe y las rutas de acceso completas se pueden usar para obtener acceso y cargar los archivos DLL del cliente del canal virtual ubicados en cualquier lugar del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="c51bd-137">If the control is not hosted in a webpage, this security restriction does not exist and full paths may be used to access and load virtual channel client DLLs located anywhere on the file system.</span></span>

<span data-ttu-id="c51bd-138">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="c51bd-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c51bd-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c51bd-139">Requirements</span></span>



| <span data-ttu-id="c51bd-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="c51bd-140">Requirement</span></span> | <span data-ttu-id="c51bd-141">Value</span><span class="sxs-lookup"><span data-stu-id="c51bd-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c51bd-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c51bd-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c51bd-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c51bd-143">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="c51bd-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c51bd-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c51bd-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c51bd-145">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="c51bd-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c51bd-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="c51bd-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c51bd-147"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="c51bd-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c51bd-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c51bd-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c51bd-149"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="c51bd-150">IID</span><span class="sxs-lookup"><span data-stu-id="c51bd-150">IID</span></span><br/>                      | <span data-ttu-id="c51bd-151">IID \_ IMsTscAdvancedSettings se define como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="c51bd-151">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c51bd-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="c51bd-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c51bd-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="c51bd-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="c51bd-154">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="c51bd-154">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="c51bd-155">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="c51bd-155">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="c51bd-156">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="c51bd-156">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="c51bd-157">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="c51bd-157">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="c51bd-158">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="c51bd-158">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="c51bd-159">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="c51bd-159">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="c51bd-160">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="c51bd-160">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="c51bd-161">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="c51bd-161">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





