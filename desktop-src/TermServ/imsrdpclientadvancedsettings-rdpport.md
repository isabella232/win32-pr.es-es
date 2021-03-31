---
title: Propiedad RDPPort de IMsRdpClientAdvancedSettings
description: Especifica el puerto de conexión.
ms.assetid: 15be7ef8-8ed2-46e0-8cc5-d5cf1642b79e
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RDPPort
- Propiedad RDPPort Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad RDPPort
- Propiedad RDPPort Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad RDPPort
- Propiedad RDPPort Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad RDPPort
- Propiedad RDPPort Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad RDPPort
- Propiedad RDPPort Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad RDPPort
- Propiedad RDPPort Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad RDPPort
- Propiedad RDPPort Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad RDPPort
- Propiedad RDPPort Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad RDPPort
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RDPPort
- IMsRdpClientAdvancedSettings.get_RDPPort
- IMsRdpClientAdvancedSettings.put_RDPPort
- IMsRdpClientAdvancedSettings2.RDPPort
- IMsRdpClientAdvancedSettings2.get_RDPPort
- IMsRdpClientAdvancedSettings2.put_RDPPort
- IMsRdpClientAdvancedSettings3.RDPPort
- IMsRdpClientAdvancedSettings3.get_RDPPort
- IMsRdpClientAdvancedSettings3.put_RDPPort
- IMsRdpClientAdvancedSettings4.RDPPort
- IMsRdpClientAdvancedSettings4.get_RDPPort
- IMsRdpClientAdvancedSettings4.put_RDPPort
- IMsRdpClientAdvancedSettings5.RDPPort
- IMsRdpClientAdvancedSettings5.get_RDPPort
- IMsRdpClientAdvancedSettings5.put_RDPPort
- IMsRdpClientAdvancedSettings6.RDPPort
- IMsRdpClientAdvancedSettings6.get_RDPPort
- IMsRdpClientAdvancedSettings6.put_RDPPort
- IMsRdpClientAdvancedSettings7.RDPPort
- IMsRdpClientAdvancedSettings7.get_RDPPort
- IMsRdpClientAdvancedSettings7.put_RDPPort
- IMsRdpClientAdvancedSettings8.RDPPort
- IMsRdpClientAdvancedSettings8.get_RDPPort
- IMsRdpClientAdvancedSettings8.put_RDPPort
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c8eafb3521d6338a0a2d469c813ff7ffa447a20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151117"
---
# <a name="imsrdpclientadvancedsettingsrdpport-property"></a><span data-ttu-id="718c5-120">IMsRdpClientAdvancedSettings:: RDPPort (propiedad)</span><span class="sxs-lookup"><span data-stu-id="718c5-120">IMsRdpClientAdvancedSettings::RDPPort property</span></span>

<span data-ttu-id="718c5-121">Especifica el puerto de conexión.</span><span class="sxs-lookup"><span data-stu-id="718c5-121">Specifies the connection port.</span></span>

<span data-ttu-id="718c5-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="718c5-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="718c5-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="718c5-123">Syntax</span></span>


```C++
HRESULT put_RDPPort(
  [in]  LONG rdpPort
);

HRESULT get_RDPPort(
  [out] LONG *prdpPort
);
```



## <a name="property-value"></a><span data-ttu-id="718c5-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="718c5-124">Property value</span></span>

<span data-ttu-id="718c5-125">El nuevo puerto.</span><span class="sxs-lookup"><span data-stu-id="718c5-125">The new port.</span></span> <span data-ttu-id="718c5-126">El valor predeterminado es 3389.</span><span class="sxs-lookup"><span data-stu-id="718c5-126">The default value is 3389.</span></span>

## <a name="error-codes"></a><span data-ttu-id="718c5-127">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="718c5-127">Error codes</span></span>

<span data-ttu-id="718c5-128">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="718c5-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="718c5-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="718c5-129">Remarks</span></span>

<span data-ttu-id="718c5-130">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="718c5-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="718c5-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="718c5-131">Requirements</span></span>



| <span data-ttu-id="718c5-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="718c5-132">Requirement</span></span> | <span data-ttu-id="718c5-133">Value</span><span class="sxs-lookup"><span data-stu-id="718c5-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="718c5-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="718c5-134">Minimum supported client</span></span><br/> | <span data-ttu-id="718c5-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="718c5-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="718c5-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="718c5-136">Minimum supported server</span></span><br/> | <span data-ttu-id="718c5-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="718c5-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="718c5-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="718c5-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="718c5-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="718c5-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="718c5-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="718c5-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="718c5-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="718c5-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="718c5-142">IID</span><span class="sxs-lookup"><span data-stu-id="718c5-142">IID</span></span><br/>                      | <span data-ttu-id="718c5-143">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="718c5-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="718c5-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="718c5-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="718c5-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="718c5-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="718c5-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="718c5-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="718c5-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="718c5-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="718c5-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="718c5-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="718c5-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="718c5-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="718c5-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="718c5-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="718c5-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="718c5-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="718c5-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="718c5-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





