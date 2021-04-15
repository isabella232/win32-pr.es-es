---
title: Propiedad overallConnectionTimeout de IMsRdpClientAdvancedSettings
description: Especifica la cantidad total de tiempo, en segundos, que el control de cliente espera a que se complete una conexión.
ms.assetid: 02fb24e1-b5e4-4d8e-a1c2-a9bd62a69bed
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad overallConnectionTimeout
- propiedad overallConnectionTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad overallConnectionTimeout
- propiedad overallConnectionTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad overallConnectionTimeout
- propiedad overallConnectionTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad overallConnectionTimeout
- propiedad overallConnectionTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad overallConnectionTimeout
- propiedad overallConnectionTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad overallConnectionTimeout
- propiedad overallConnectionTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad overallConnectionTimeout
- propiedad overallConnectionTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad overallConnectionTimeout
- propiedad overallConnectionTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad overallConnectionTimeout
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.overallConnectionTimeout
- IMsRdpClientAdvancedSettings.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings2.overallConnectionTimeout
- IMsRdpClientAdvancedSettings2.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings2.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings3.overallConnectionTimeout
- IMsRdpClientAdvancedSettings3.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings3.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings4.overallConnectionTimeout
- IMsRdpClientAdvancedSettings4.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings4.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings5.overallConnectionTimeout
- IMsRdpClientAdvancedSettings5.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings5.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings6.overallConnectionTimeout
- IMsRdpClientAdvancedSettings6.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings6.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings7.overallConnectionTimeout
- IMsRdpClientAdvancedSettings7.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings7.put_overallConnectionTimeout
- IMsRdpClientAdvancedSettings8.overallConnectionTimeout
- IMsRdpClientAdvancedSettings8.get_overallConnectionTimeout
- IMsRdpClientAdvancedSettings8.put_overallConnectionTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50de6687d3d5cbccb3f7fdab94eca5ba4f2331c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676670"
---
# <a name="imsrdpclientadvancedsettingsoverallconnectiontimeout-property"></a><span data-ttu-id="265d8-120">IMsRdpClientAdvancedSettings:: overallConnectionTimeout (propiedad)</span><span class="sxs-lookup"><span data-stu-id="265d8-120">IMsRdpClientAdvancedSettings::overallConnectionTimeout property</span></span>

<span data-ttu-id="265d8-121">Especifica la cantidad total de tiempo, en segundos, que el control de cliente espera a que se complete una conexión.</span><span class="sxs-lookup"><span data-stu-id="265d8-121">Specifies the total length of time, in seconds, that the client control waits for a connection to complete.</span></span>

<span data-ttu-id="265d8-122">Si transcurre el tiempo especificado antes de que se complete la conexión, el control se desconecta y llama al método [**IMsTscAxEvents:: OnDisconnection**](imstscaxevents-ondisconnected.md) .</span><span class="sxs-lookup"><span data-stu-id="265d8-122">If the specified time elapses before connection completes, the control disconnects and calls the [**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md) method.</span></span>

<span data-ttu-id="265d8-123">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="265d8-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="265d8-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="265d8-124">Syntax</span></span>


```C++
HRESULT put_overallConnectionTimeout(
  [in]  LONG overallConnectionTimeout
);

HRESULT get_overallConnectionTimeout(
  [out] LONG *poverallConnectionTimeout
);
```



## <a name="property-value"></a><span data-ttu-id="265d8-125">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="265d8-125">Property value</span></span>

<span data-ttu-id="265d8-126">La nueva hora, en segundos.</span><span class="sxs-lookup"><span data-stu-id="265d8-126">The new time, in seconds.</span></span> <span data-ttu-id="265d8-127">El valor máximo es 600, que representa 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="265d8-127">The maximum value is 600, which represents 10 minutes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="265d8-128">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="265d8-128">Error codes</span></span>

<span data-ttu-id="265d8-129">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="265d8-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="265d8-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="265d8-130">Remarks</span></span>

<span data-ttu-id="265d8-131">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="265d8-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="265d8-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="265d8-132">Requirements</span></span>



| <span data-ttu-id="265d8-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="265d8-133">Requirement</span></span> | <span data-ttu-id="265d8-134">Value</span><span class="sxs-lookup"><span data-stu-id="265d8-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="265d8-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="265d8-135">Minimum supported client</span></span><br/> | <span data-ttu-id="265d8-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="265d8-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="265d8-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="265d8-137">Minimum supported server</span></span><br/> | <span data-ttu-id="265d8-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="265d8-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="265d8-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="265d8-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="265d8-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="265d8-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="265d8-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="265d8-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="265d8-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="265d8-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="265d8-143">IID</span><span class="sxs-lookup"><span data-stu-id="265d8-143">IID</span></span><br/>                      | <span data-ttu-id="265d8-144">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="265d8-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="265d8-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="265d8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="265d8-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="265d8-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="265d8-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="265d8-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="265d8-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="265d8-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="265d8-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="265d8-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="265d8-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="265d8-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="265d8-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="265d8-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="265d8-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="265d8-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="265d8-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="265d8-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="265d8-154">**singleConnectionTimeout**</span><span class="sxs-lookup"><span data-stu-id="265d8-154">**singleConnectionTimeout**</span></span>](imsrdpclientadvancedsettings-singleconnectiontimeout.md)
</dt> </dl>

 

 





