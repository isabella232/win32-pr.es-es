---
title: Propiedad shutdownTimeout de IMsRdpClientAdvancedSettings
description: Especifica el período de tiempo, en segundos, que se esperará a que el servidor responda a una solicitud de desconexión.
ms.assetid: 3fa935dc-d4b0-433b-ab67-a644fcf09006
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad shutdownTimeout
- propiedad shutdownTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad shutdownTimeout
- propiedad shutdownTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad shutdownTimeout
- propiedad shutdownTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad shutdownTimeout
- propiedad shutdownTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad shutdownTimeout
- propiedad shutdownTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad shutdownTimeout
- propiedad shutdownTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad shutdownTimeout
- propiedad shutdownTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad shutdownTimeout
- propiedad shutdownTimeout Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad shutdownTimeout
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.shutdownTimeout
- IMsRdpClientAdvancedSettings.get_shutdownTimeout
- IMsRdpClientAdvancedSettings.put_shutdownTimeout
- IMsRdpClientAdvancedSettings2.shutdownTimeout
- IMsRdpClientAdvancedSettings2.get_shutdownTimeout
- IMsRdpClientAdvancedSettings2.put_shutdownTimeout
- IMsRdpClientAdvancedSettings3.shutdownTimeout
- IMsRdpClientAdvancedSettings3.get_shutdownTimeout
- IMsRdpClientAdvancedSettings3.put_shutdownTimeout
- IMsRdpClientAdvancedSettings4.shutdownTimeout
- IMsRdpClientAdvancedSettings4.get_shutdownTimeout
- IMsRdpClientAdvancedSettings4.put_shutdownTimeout
- IMsRdpClientAdvancedSettings5.shutdownTimeout
- IMsRdpClientAdvancedSettings5.get_shutdownTimeout
- IMsRdpClientAdvancedSettings5.put_shutdownTimeout
- IMsRdpClientAdvancedSettings6.shutdownTimeout
- IMsRdpClientAdvancedSettings6.get_shutdownTimeout
- IMsRdpClientAdvancedSettings6.put_shutdownTimeout
- IMsRdpClientAdvancedSettings7.shutdownTimeout
- IMsRdpClientAdvancedSettings7.get_shutdownTimeout
- IMsRdpClientAdvancedSettings7.put_shutdownTimeout
- IMsRdpClientAdvancedSettings8.shutdownTimeout
- IMsRdpClientAdvancedSettings8.get_shutdownTimeout
- IMsRdpClientAdvancedSettings8.put_shutdownTimeout
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 868a011a0ce484f5bb2dd7d1ec610f4e3a436898
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104421931"
---
# <a name="imsrdpclientadvancedsettingsshutdowntimeout-property"></a><span data-ttu-id="ae6f8-120">IMsRdpClientAdvancedSettings:: shutdownTimeout (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ae6f8-120">IMsRdpClientAdvancedSettings::shutdownTimeout property</span></span>

<span data-ttu-id="ae6f8-121">Especifica el período de tiempo, en segundos, que se esperará a que el servidor responda a una solicitud de desconexión.</span><span class="sxs-lookup"><span data-stu-id="ae6f8-121">Specifies the length of time, in seconds, to wait for the server to respond to a disconnection request.</span></span>

<span data-ttu-id="ae6f8-122">Si el servidor no responde dentro del tiempo especificado, el control de cliente se desconecta.</span><span class="sxs-lookup"><span data-stu-id="ae6f8-122">If the server does not reply within the specified time, the client control disconnects.</span></span>

<span data-ttu-id="ae6f8-123">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ae6f8-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae6f8-124">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae6f8-124">Syntax</span></span>


```C++
HRESULT put_shutdownTimeout(
  [in]  LONG shutdownTimeout
);

HRESULT get_shutdownTimeout(
  [out] LONG *pshutdownTimeout
);
```



## <a name="property-value"></a><span data-ttu-id="ae6f8-125">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ae6f8-125">Property value</span></span>

<span data-ttu-id="ae6f8-126">La nueva hora, en segundos.</span><span class="sxs-lookup"><span data-stu-id="ae6f8-126">The new time, in seconds.</span></span> <span data-ttu-id="ae6f8-127">El valor predeterminado de la propiedad es 10.</span><span class="sxs-lookup"><span data-stu-id="ae6f8-127">The default value of the property is 10.</span></span> <span data-ttu-id="ae6f8-128">El valor máximo es 600, que representa 10 minutos.</span><span class="sxs-lookup"><span data-stu-id="ae6f8-128">The maximum value is 600, which represents 10 minutes.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ae6f8-129">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="ae6f8-129">Error codes</span></span>

<span data-ttu-id="ae6f8-130">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="ae6f8-130">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae6f8-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ae6f8-131">Remarks</span></span>

<span data-ttu-id="ae6f8-132">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="ae6f8-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae6f8-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae6f8-133">Requirements</span></span>



| <span data-ttu-id="ae6f8-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae6f8-134">Requirement</span></span> | <span data-ttu-id="ae6f8-135">Value</span><span class="sxs-lookup"><span data-stu-id="ae6f8-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae6f8-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae6f8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ae6f8-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ae6f8-137">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="ae6f8-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae6f8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ae6f8-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ae6f8-139">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="ae6f8-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ae6f8-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="ae6f8-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae6f8-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ae6f8-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ae6f8-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae6f8-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae6f8-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="ae6f8-144">IID</span><span class="sxs-lookup"><span data-stu-id="ae6f8-144">IID</span></span><br/>                      | <span data-ttu-id="ae6f8-145">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="ae6f8-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ae6f8-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae6f8-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae6f8-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="ae6f8-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="ae6f8-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="ae6f8-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="ae6f8-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="ae6f8-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="ae6f8-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="ae6f8-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="ae6f8-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="ae6f8-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="ae6f8-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="ae6f8-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="ae6f8-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="ae6f8-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="ae6f8-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="ae6f8-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





