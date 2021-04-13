---
title: Propiedad singleConnectionTimeout de IMsRdpClientAdvancedSettings
description: Especifica el período de tiempo máximo, en segundos, que el control de cliente espera para una conexión a una dirección IP.
ms.assetid: 57fb2397-8229-4446-88fd-e75cb96c7ac5
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad singleConnectionTimeout
- propiedad singleConnectionTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad singleConnectionTimeout
- propiedad singleConnectionTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad singleConnectionTimeout
- propiedad singleConnectionTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad singleConnectionTimeout
- propiedad singleConnectionTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad singleConnectionTimeout
- propiedad singleConnectionTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad singleConnectionTimeout
- propiedad singleConnectionTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad singleConnectionTimeout
- propiedad singleConnectionTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad singleConnectionTimeout
- propiedad singleConnectionTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad singleConnectionTimeout
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.singleConnectionTimeout
- IMsRdpClientAdvancedSettings.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings2.singleConnectionTimeout
- IMsRdpClientAdvancedSettings2.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings2.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings3.singleConnectionTimeout
- IMsRdpClientAdvancedSettings3.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings3.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings4.singleConnectionTimeout
- IMsRdpClientAdvancedSettings4.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings4.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings5.singleConnectionTimeout
- IMsRdpClientAdvancedSettings5.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings5.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings6.singleConnectionTimeout
- IMsRdpClientAdvancedSettings6.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings6.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings7.singleConnectionTimeout
- IMsRdpClientAdvancedSettings7.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings7.put_singleConnectionTimeout
- IMsRdpClientAdvancedSettings8.singleConnectionTimeout
- IMsRdpClientAdvancedSettings8.get_singleConnectionTimeout
- IMsRdpClientAdvancedSettings8.put_singleConnectionTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55a0d2eb34235c874b4408e5e4c6f0a349a1ab93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421930"
---
# <a name="imsrdpclientadvancedsettingssingleconnectiontimeout-property"></a><span data-ttu-id="58835-120">IMsRdpClientAdvancedSettings:: singleConnectionTimeout (propiedad)</span><span class="sxs-lookup"><span data-stu-id="58835-120">IMsRdpClientAdvancedSettings::singleConnectionTimeout property</span></span>

<span data-ttu-id="58835-121">Especifica el período de tiempo máximo, en segundos, que el control de cliente espera para una conexión a una dirección IP.</span><span class="sxs-lookup"><span data-stu-id="58835-121">Specifies the maximum length of time, in seconds, that the client control waits for a connection to an IP address.</span></span>

<span data-ttu-id="58835-122">Durante la conexión, es posible que el control intente conectarse a varias direcciones IP.</span><span class="sxs-lookup"><span data-stu-id="58835-122">During connection, the control may attempt to connect to multiple IP addresses.</span></span>

<span data-ttu-id="58835-123">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="58835-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="58835-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58835-124">Syntax</span></span>


```C++
HRESULT put_singleConnectionTimeout(
  [in]  LONG singleConnectionTimeout
);

HRESULT get_singleConnectionTimeout(
  [out] LONG *psingleConnectionTimeout
);
```



## <a name="property-value"></a><span data-ttu-id="58835-125">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="58835-125">Property value</span></span>

<span data-ttu-id="58835-126">La nueva hora, en segundos.</span><span class="sxs-lookup"><span data-stu-id="58835-126">The new time, in seconds.</span></span> <span data-ttu-id="58835-127">El valor máximo es 600.</span><span class="sxs-lookup"><span data-stu-id="58835-127">The maximum value is 600.</span></span>

## <a name="error-codes"></a><span data-ttu-id="58835-128">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="58835-128">Error codes</span></span>

<span data-ttu-id="58835-129">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="58835-129">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="58835-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="58835-130">Remarks</span></span>

<span data-ttu-id="58835-131">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="58835-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="58835-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58835-132">Requirements</span></span>



| <span data-ttu-id="58835-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="58835-133">Requirement</span></span> | <span data-ttu-id="58835-134">Value</span><span class="sxs-lookup"><span data-stu-id="58835-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58835-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58835-135">Minimum supported client</span></span><br/> | <span data-ttu-id="58835-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58835-136">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="58835-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58835-137">Minimum supported server</span></span><br/> | <span data-ttu-id="58835-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58835-138">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="58835-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="58835-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="58835-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58835-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="58835-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="58835-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58835-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58835-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="58835-143">IID</span><span class="sxs-lookup"><span data-stu-id="58835-143">IID</span></span><br/>                      | <span data-ttu-id="58835-144">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="58835-144">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="58835-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="58835-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58835-146">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="58835-146">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="58835-147">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="58835-147">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="58835-148">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="58835-148">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="58835-149">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="58835-149">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="58835-150">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="58835-150">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="58835-151">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="58835-151">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="58835-152">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="58835-152">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="58835-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="58835-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="58835-154">**overallConnectionTimeout**</span><span class="sxs-lookup"><span data-stu-id="58835-154">**overallConnectionTimeout**</span></span>](imsrdpclientadvancedsettings-overallconnectiontimeout.md)
</dt> </dl>

 

 





