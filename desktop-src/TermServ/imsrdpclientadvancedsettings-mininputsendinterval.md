---
title: Propiedad minInputSendInterval de IMsRdpClientAdvancedSettings
description: Especifica el intervalo mínimo, en milisegundos, entre el envío de eventos del mouse.
ms.assetid: d186c05f-0b45-47bd-8a8e-e1f9baf2bd75
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad minInputSendInterval
- propiedad minInputSendInterval Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad minInputSendInterval
- propiedad minInputSendInterval Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad minInputSendInterval
- propiedad minInputSendInterval Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad minInputSendInterval
- propiedad minInputSendInterval Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad minInputSendInterval
- propiedad minInputSendInterval Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad minInputSendInterval
- propiedad minInputSendInterval Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad minInputSendInterval
- propiedad minInputSendInterval Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad minInputSendInterval
- propiedad minInputSendInterval Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad minInputSendInterval
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.minInputSendInterval
- IMsRdpClientAdvancedSettings.get_minInputSendInterval
- IMsRdpClientAdvancedSettings.put_minInputSendInterval
- IMsRdpClientAdvancedSettings2.minInputSendInterval
- IMsRdpClientAdvancedSettings2.get_minInputSendInterval
- IMsRdpClientAdvancedSettings2.put_minInputSendInterval
- IMsRdpClientAdvancedSettings3.minInputSendInterval
- IMsRdpClientAdvancedSettings3.get_minInputSendInterval
- IMsRdpClientAdvancedSettings3.put_minInputSendInterval
- IMsRdpClientAdvancedSettings4.minInputSendInterval
- IMsRdpClientAdvancedSettings4.get_minInputSendInterval
- IMsRdpClientAdvancedSettings4.put_minInputSendInterval
- IMsRdpClientAdvancedSettings5.minInputSendInterval
- IMsRdpClientAdvancedSettings5.get_minInputSendInterval
- IMsRdpClientAdvancedSettings5.put_minInputSendInterval
- IMsRdpClientAdvancedSettings6.minInputSendInterval
- IMsRdpClientAdvancedSettings6.get_minInputSendInterval
- IMsRdpClientAdvancedSettings6.put_minInputSendInterval
- IMsRdpClientAdvancedSettings7.minInputSendInterval
- IMsRdpClientAdvancedSettings7.get_minInputSendInterval
- IMsRdpClientAdvancedSettings7.put_minInputSendInterval
- IMsRdpClientAdvancedSettings8.minInputSendInterval
- IMsRdpClientAdvancedSettings8.get_minInputSendInterval
- IMsRdpClientAdvancedSettings8.put_minInputSendInterval
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56070e2ba395c4b89dc9caa9e6e5181bb03d81ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422137"
---
# <a name="imsrdpclientadvancedsettingsmininputsendinterval-property"></a><span data-ttu-id="fabae-120">IMsRdpClientAdvancedSettings:: minInputSendInterval (propiedad)</span><span class="sxs-lookup"><span data-stu-id="fabae-120">IMsRdpClientAdvancedSettings::minInputSendInterval property</span></span>

<span data-ttu-id="fabae-121">Especifica el intervalo mínimo, en milisegundos, entre el envío de eventos del mouse.</span><span class="sxs-lookup"><span data-stu-id="fabae-121">Specifies the minimum interval, in milliseconds, between the sending of mouse events.</span></span>

<span data-ttu-id="fabae-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="fabae-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fabae-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fabae-123">Syntax</span></span>


```C++
HRESULT put_minInputSendInterval(
  [in]  LONG minInputSendInterval
);

HRESULT get_minInputSendInterval(
  [out] LONG *pminInputSendInterval
);
```



## <a name="property-value"></a><span data-ttu-id="fabae-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="fabae-124">Property value</span></span>

<span data-ttu-id="fabae-125">Nuevo intervalo, en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="fabae-125">The new interval, in milliseconds.</span></span> <span data-ttu-id="fabae-126">El valor predeterminado es 100.</span><span class="sxs-lookup"><span data-stu-id="fabae-126">The default value is 100.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fabae-127">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="fabae-127">Error codes</span></span>

<span data-ttu-id="fabae-128">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="fabae-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="fabae-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fabae-129">Remarks</span></span>

<span data-ttu-id="fabae-130">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="fabae-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fabae-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fabae-131">Requirements</span></span>



| <span data-ttu-id="fabae-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="fabae-132">Requirement</span></span> | <span data-ttu-id="fabae-133">Value</span><span class="sxs-lookup"><span data-stu-id="fabae-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fabae-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fabae-134">Minimum supported client</span></span><br/> | <span data-ttu-id="fabae-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fabae-135">Windows 7</span></span><br/>                                                                            |
| <span data-ttu-id="fabae-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fabae-136">Minimum supported server</span></span><br/> | <span data-ttu-id="fabae-137">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fabae-137">Windows Server 2008 R2</span></span><br/>                                                               |
| <span data-ttu-id="fabae-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fabae-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="fabae-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fabae-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="fabae-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fabae-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fabae-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fabae-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="fabae-142">IID</span><span class="sxs-lookup"><span data-stu-id="fabae-142">IID</span></span><br/>                      | <span data-ttu-id="fabae-143">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="fabae-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fabae-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="fabae-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fabae-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="fabae-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="fabae-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="fabae-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="fabae-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="fabae-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="fabae-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="fabae-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="fabae-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="fabae-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="fabae-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="fabae-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="fabae-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="fabae-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="fabae-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="fabae-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





