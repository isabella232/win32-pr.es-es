---
title: Propiedad EnableWindowsKey de IMsRdpClientAdvancedSettings
description: Especifica si la clave de Windows se puede usar en la sesión remota.
ms.assetid: fcf0460d-3cd1-4da4-8009-0b1256adf312
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad EnableWindowsKey
- Propiedad EnableWindowsKey Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad EnableWindowsKey
- Propiedad EnableWindowsKey Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad EnableWindowsKey
- Propiedad EnableWindowsKey Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad EnableWindowsKey
- Propiedad EnableWindowsKey Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad EnableWindowsKey
- Propiedad EnableWindowsKey Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad EnableWindowsKey
- Propiedad EnableWindowsKey Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad EnableWindowsKey
- Propiedad EnableWindowsKey Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad EnableWindowsKey
- Propiedad EnableWindowsKey Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad EnableWindowsKey
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.EnableWindowsKey
- IMsRdpClientAdvancedSettings.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings2.EnableWindowsKey
- IMsRdpClientAdvancedSettings2.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings2.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings3.EnableWindowsKey
- IMsRdpClientAdvancedSettings3.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings3.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings4.EnableWindowsKey
- IMsRdpClientAdvancedSettings4.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings4.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings5.EnableWindowsKey
- IMsRdpClientAdvancedSettings5.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings5.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings6.EnableWindowsKey
- IMsRdpClientAdvancedSettings6.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings6.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings7.EnableWindowsKey
- IMsRdpClientAdvancedSettings7.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings7.put_EnableWindowsKey
- IMsRdpClientAdvancedSettings8.EnableWindowsKey
- IMsRdpClientAdvancedSettings8.get_EnableWindowsKey
- IMsRdpClientAdvancedSettings8.put_EnableWindowsKey
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e31571e44d6b391250c32268750b25a76105eb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803625"
---
# <a name="imsrdpclientadvancedsettingsenablewindowskey-property"></a><span data-ttu-id="6b660-120">IMsRdpClientAdvancedSettings:: EnableWindowsKey (propiedad)</span><span class="sxs-lookup"><span data-stu-id="6b660-120">IMsRdpClientAdvancedSettings::EnableWindowsKey property</span></span>

<span data-ttu-id="6b660-121">Especifica si la clave de Windows se puede usar en la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="6b660-121">Specifies if the Windows key can be used in the remote session.</span></span>

<span data-ttu-id="6b660-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="6b660-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b660-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6b660-123">Syntax</span></span>


```C++
HRESULT put_EnableWindowsKey(
  [in]  LONG enableWindowsKey
);

HRESULT get_EnableWindowsKey(
  [out] LONG *penableWindowsKey
);
```



## <a name="property-value"></a><span data-ttu-id="6b660-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="6b660-124">Property value</span></span>

<span data-ttu-id="6b660-125">Establezca este parámetro en 0 para deshabilitar la característica o un valor distinto de cero para habilitar la característica.</span><span class="sxs-lookup"><span data-stu-id="6b660-125">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6b660-126">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="6b660-126">Error codes</span></span>

<span data-ttu-id="6b660-127">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="6b660-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b660-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6b660-128">Remarks</span></span>

<span data-ttu-id="6b660-129">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6b660-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b660-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b660-130">Requirements</span></span>



| <span data-ttu-id="6b660-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b660-131">Requirement</span></span> | <span data-ttu-id="6b660-132">Value</span><span class="sxs-lookup"><span data-stu-id="6b660-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b660-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b660-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6b660-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b660-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="6b660-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b660-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6b660-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b660-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="6b660-137">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6b660-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="6b660-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b660-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="6b660-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6b660-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b660-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b660-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="6b660-141">IID</span><span class="sxs-lookup"><span data-stu-id="6b660-141">IID</span></span><br/>                      | <span data-ttu-id="6b660-142">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="6b660-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6b660-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b660-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b660-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="6b660-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="6b660-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="6b660-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="6b660-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="6b660-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="6b660-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="6b660-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="6b660-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="6b660-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="6b660-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="6b660-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="6b660-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="6b660-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="6b660-151">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="6b660-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





