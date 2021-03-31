---
title: Propiedad DoubleClickDetect de IMsRdpClientAdvancedSettings
description: Especifica si el cliente identifica los dos clics para el servidor.
ms.assetid: 39e76bef-3d12-406d-a074-8c084fbe9ccc
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DoubleClickDetect
- Propiedad DoubleClickDetect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad DoubleClickDetect
- Propiedad DoubleClickDetect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad DoubleClickDetect
- Propiedad DoubleClickDetect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad DoubleClickDetect
- Propiedad DoubleClickDetect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad DoubleClickDetect
- Propiedad DoubleClickDetect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad DoubleClickDetect
- Propiedad DoubleClickDetect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad DoubleClickDetect
- Propiedad DoubleClickDetect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad DoubleClickDetect
- Propiedad DoubleClickDetect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad DoubleClickDetect
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DoubleClickDetect
- IMsRdpClientAdvancedSettings.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings2.DoubleClickDetect
- IMsRdpClientAdvancedSettings2.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings2.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings3.DoubleClickDetect
- IMsRdpClientAdvancedSettings3.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings3.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings4.DoubleClickDetect
- IMsRdpClientAdvancedSettings4.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings4.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings5.DoubleClickDetect
- IMsRdpClientAdvancedSettings5.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings5.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings6.DoubleClickDetect
- IMsRdpClientAdvancedSettings6.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings6.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings7.DoubleClickDetect
- IMsRdpClientAdvancedSettings7.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings7.put_DoubleClickDetect
- IMsRdpClientAdvancedSettings8.DoubleClickDetect
- IMsRdpClientAdvancedSettings8.get_DoubleClickDetect
- IMsRdpClientAdvancedSettings8.put_DoubleClickDetect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd771614a80d909e0e7a748ab7256a5310084deb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151015"
---
# <a name="imsrdpclientadvancedsettingsdoubleclickdetect-property"></a><span data-ttu-id="bcf62-120">IMsRdpClientAdvancedSettings::D propiedad oubleClickDetect</span><span class="sxs-lookup"><span data-stu-id="bcf62-120">IMsRdpClientAdvancedSettings::DoubleClickDetect property</span></span>

<span data-ttu-id="bcf62-121">Especifica si el cliente identifica los dos clics para el servidor.</span><span class="sxs-lookup"><span data-stu-id="bcf62-121">Specifies if the client identifies double-clicks for the server.</span></span>

<span data-ttu-id="bcf62-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="bcf62-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcf62-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bcf62-123">Syntax</span></span>


```C++
HRESULT put_DoubleClickDetect(
  [in]  LONG doubleClickDetect
);

HRESULT get_DoubleClickDetect(
  [out] LONG *pdoubleClickDetect
);
```



## <a name="property-value"></a><span data-ttu-id="bcf62-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="bcf62-124">Property value</span></span>

<span data-ttu-id="bcf62-125">Establezca este parámetro en 0 para deshabilitar la característica o un valor distinto de cero para habilitar la característica.</span><span class="sxs-lookup"><span data-stu-id="bcf62-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bcf62-126">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="bcf62-126">Error codes</span></span>

<span data-ttu-id="bcf62-127">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="bcf62-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcf62-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bcf62-128">Remarks</span></span>

<span data-ttu-id="bcf62-129">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="bcf62-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bcf62-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcf62-130">Requirements</span></span>



| <span data-ttu-id="bcf62-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcf62-131">Requirement</span></span> | <span data-ttu-id="bcf62-132">Value</span><span class="sxs-lookup"><span data-stu-id="bcf62-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcf62-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bcf62-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bcf62-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bcf62-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="bcf62-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bcf62-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bcf62-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bcf62-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="bcf62-137">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="bcf62-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="bcf62-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcf62-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="bcf62-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bcf62-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcf62-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcf62-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="bcf62-141">IID</span><span class="sxs-lookup"><span data-stu-id="bcf62-141">IID</span></span><br/>                      | <span data-ttu-id="bcf62-142">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="bcf62-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bcf62-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="bcf62-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcf62-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="bcf62-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="bcf62-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="bcf62-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="bcf62-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="bcf62-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="bcf62-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="bcf62-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="bcf62-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="bcf62-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="bcf62-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="bcf62-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="bcf62-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="bcf62-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="bcf62-151">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="bcf62-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





