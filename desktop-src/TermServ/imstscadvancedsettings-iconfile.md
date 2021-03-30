---
title: Propiedad IconFile de IMsTscAdvancedSettings
description: Especifica el nombre del archivo que contiene los datos de icono a los que se tendrá acceso al mostrar el cliente en modo de pantalla completa.
ms.assetid: 2b6ac2ad-9745-4b80-a415-4840cd8aa8b3
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad IconFile
- Propiedad IconFile Servicios de Escritorio remoto, interfaz IMsTscAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsTscAdvancedSettings, propiedad IconFile
- Propiedad IconFile Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad IconFile
- Propiedad IconFile Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad IconFile
- Propiedad IconFile Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad IconFile
- Propiedad IconFile Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad IconFile
- Propiedad IconFile Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad IconFile
- Propiedad IconFile Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad IconFile
- Propiedad IconFile Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad IconFile
- Propiedad IconFile Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad IconFile
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.IconFile
- IMsTscAdvancedSettings.put_IconFile
- IMsRdpClientAdvancedSettings.IconFile
- IMsRdpClientAdvancedSettings.put_IconFile
- IMsRdpClientAdvancedSettings2.IconFile
- IMsRdpClientAdvancedSettings2.put_IconFile
- IMsRdpClientAdvancedSettings3.IconFile
- IMsRdpClientAdvancedSettings3.put_IconFile
- IMsRdpClientAdvancedSettings4.IconFile
- IMsRdpClientAdvancedSettings4.put_IconFile
- IMsRdpClientAdvancedSettings5.IconFile
- IMsRdpClientAdvancedSettings5.put_IconFile
- IMsRdpClientAdvancedSettings6.IconFile
- IMsRdpClientAdvancedSettings6.put_IconFile
- IMsRdpClientAdvancedSettings7.IconFile
- IMsRdpClientAdvancedSettings7.put_IconFile
- IMsRdpClientAdvancedSettings8.IconFile
- IMsRdpClientAdvancedSettings8.put_IconFile
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d8f996e70873d5584bb80bbf4f40f71a7deae8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802281"
---
# <a name="imstscadvancedsettingsiconfile-property"></a><span data-ttu-id="e8588-122">IMsTscAdvancedSettings:: IconFile (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e8588-122">IMsTscAdvancedSettings::IconFile property</span></span>

<span data-ttu-id="e8588-123">Especifica el nombre del archivo que contiene los datos de icono a los que se tendrá acceso al mostrar el cliente en modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="e8588-123">Specifies the name of the file containing icon data that will be accessed when displaying the client in full-screen mode.</span></span>

> [!Note]  
> <span data-ttu-id="e8588-124">Esta propiedad no se admite en el control ActiveX (MsRdp. ocx).</span><span class="sxs-lookup"><span data-stu-id="e8588-124">This property is not supported in the ActiveX control (MsRdp.ocx).</span></span> <span data-ttu-id="e8588-125">Se admite en la biblioteca de MsTscAx.dll incluida en el cliente estándar (MsTsc.exe).</span><span class="sxs-lookup"><span data-stu-id="e8588-125">It is supported in the MsTscAx.dll library included in the standard client (MsTsc.exe).</span></span>

 

<span data-ttu-id="e8588-126">Esta propiedad es de solo escritura.</span><span class="sxs-lookup"><span data-stu-id="e8588-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8588-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8588-127">Syntax</span></span>


```C++
HRESULT put_IconFile(
  [in] BSTR IconFile
);
```



## <a name="property-value"></a><span data-ttu-id="e8588-128">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e8588-128">Property value</span></span>

<span data-ttu-id="e8588-129">La ruta de acceso completa del archivo de icono o un archivo que contiene datos de icono, como un archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="e8588-129">The fully qualified path of icon file or a file containing icon data, such as a DLL.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e8588-130">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="e8588-130">Error codes</span></span>

<span data-ttu-id="e8588-131">Devuelve **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="e8588-131">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8588-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e8588-132">Remarks</span></span>

<span data-ttu-id="e8588-133">La extensión de nombre de archivo de un archivo de icono es ". ico".</span><span class="sxs-lookup"><span data-stu-id="e8588-133">The file name extension of an icon file is ".ico".</span></span>

<span data-ttu-id="e8588-134">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e8588-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8588-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8588-135">Requirements</span></span>



| <span data-ttu-id="e8588-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8588-136">Requirement</span></span> | <span data-ttu-id="e8588-137">Value</span><span class="sxs-lookup"><span data-stu-id="e8588-137">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8588-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8588-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e8588-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8588-139">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="e8588-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8588-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e8588-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8588-141">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="e8588-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e8588-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="e8588-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8588-143"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="e8588-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e8588-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8588-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8588-145"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="e8588-146">IID</span><span class="sxs-lookup"><span data-stu-id="e8588-146">IID</span></span><br/>                      | <span data-ttu-id="e8588-147">IID \_ IMsTscAdvancedSettings se define como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="e8588-147">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e8588-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="e8588-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8588-149">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="e8588-149">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="e8588-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="e8588-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="e8588-151">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="e8588-151">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="e8588-152">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="e8588-152">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="e8588-153">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="e8588-153">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="e8588-154">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="e8588-154">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="e8588-155">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="e8588-155">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="e8588-156">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="e8588-156">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="e8588-157">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="e8588-157">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





