---
title: IMsTscAdvancedSettings propiedad IconIndex
description: Especifica el índice del icono dentro del archivo de icono actual.
ms.assetid: c29ae1a7-9c54-4e56-bb69-4e929e8a4e5c
ms.tgt_platform: multiple
keywords:
- Propiedad IconIndex Servicios de Escritorio remoto
- Propiedad IconIndex Servicios de Escritorio remoto, interfaz IMsTscAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsTscAdvancedSettings, propiedad IconIndex
- Propiedad IconIndex Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad IconIndex
- Propiedad IconIndex Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad IconIndex
- Propiedad IconIndex Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad IconIndex
- Propiedad IconIndex Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad IconIndex
- Propiedad IconIndex Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad IconIndex
- Propiedad IconIndex Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad IconIndex
- Propiedad IconIndex Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad IconIndex
- Propiedad IconIndex Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad IconIndex
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings.IconIndex
- IMsTscAdvancedSettings.put_IconIndex
- IMsRdpClientAdvancedSettings.IconIndex
- IMsRdpClientAdvancedSettings.put_IconIndex
- IMsRdpClientAdvancedSettings2.IconIndex
- IMsRdpClientAdvancedSettings2.put_IconIndex
- IMsRdpClientAdvancedSettings3.IconIndex
- IMsRdpClientAdvancedSettings3.put_IconIndex
- IMsRdpClientAdvancedSettings4.IconIndex
- IMsRdpClientAdvancedSettings4.put_IconIndex
- IMsRdpClientAdvancedSettings5.IconIndex
- IMsRdpClientAdvancedSettings5.put_IconIndex
- IMsRdpClientAdvancedSettings6.IconIndex
- IMsRdpClientAdvancedSettings6.put_IconIndex
- IMsRdpClientAdvancedSettings7.IconIndex
- IMsRdpClientAdvancedSettings7.put_IconIndex
- IMsRdpClientAdvancedSettings8.IconIndex
- IMsRdpClientAdvancedSettings8.put_IconIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3be56eab5dbe7f03155c6082e4e70fc4bd439253
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534137"
---
# <a name="imstscadvancedsettingsiconindex-property"></a><span data-ttu-id="e11b4-122">IMsTscAdvancedSettings:: IconIndex (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e11b4-122">IMsTscAdvancedSettings::IconIndex property</span></span>

<span data-ttu-id="e11b4-123">Especifica el índice del icono dentro del archivo de icono actual.</span><span class="sxs-lookup"><span data-stu-id="e11b4-123">Specifies the index of the icon within the current icon file.</span></span>

> [!Note]  
> <span data-ttu-id="e11b4-124">Esta propiedad no se admite en el control ActiveX (MsRdp. ocx).</span><span class="sxs-lookup"><span data-stu-id="e11b4-124">This property is not supported in the ActiveX control (MsRdp.ocx).</span></span> <span data-ttu-id="e11b4-125">Se admite en la biblioteca de MsTscAx.dll incluida en el cliente estándar (MsTsc.exe).</span><span class="sxs-lookup"><span data-stu-id="e11b4-125">It is supported in the MsTscAx.dll library included in the standard client (MsTsc.exe).</span></span>

 

<span data-ttu-id="e11b4-126">Esta propiedad es de solo escritura.</span><span class="sxs-lookup"><span data-stu-id="e11b4-126">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e11b4-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e11b4-127">Syntax</span></span>


```C++
HRESULT put_IconIndex(
  [in] LONG IconIndex
);
```



## <a name="property-value"></a><span data-ttu-id="e11b4-128">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e11b4-128">Property value</span></span>

<span data-ttu-id="e11b4-129">Índice del icono.</span><span class="sxs-lookup"><span data-stu-id="e11b4-129">The index of the icon.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e11b4-130">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="e11b4-130">Error codes</span></span>

<span data-ttu-id="e11b4-131">Devuelve **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="e11b4-131">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e11b4-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e11b4-132">Remarks</span></span>

<span data-ttu-id="e11b4-133">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e11b4-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e11b4-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e11b4-134">Requirements</span></span>



| <span data-ttu-id="e11b4-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e11b4-135">Requirement</span></span> | <span data-ttu-id="e11b4-136">Value</span><span class="sxs-lookup"><span data-stu-id="e11b4-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e11b4-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e11b4-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e11b4-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e11b4-138">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="e11b4-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e11b4-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e11b4-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e11b4-140">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="e11b4-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e11b4-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="e11b4-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e11b4-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="e11b4-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e11b4-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e11b4-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e11b4-144"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="e11b4-145">IID</span><span class="sxs-lookup"><span data-stu-id="e11b4-145">IID</span></span><br/>                      | <span data-ttu-id="e11b4-146">IID \_ IMsTscAdvancedSettings se define como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="e11b4-146">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e11b4-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="e11b4-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e11b4-148">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="e11b4-148">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="e11b4-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="e11b4-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="e11b4-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="e11b4-150">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="e11b4-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="e11b4-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="e11b4-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="e11b4-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="e11b4-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="e11b4-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="e11b4-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="e11b4-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="e11b4-155">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="e11b4-155">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="e11b4-156">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="e11b4-156">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

 





