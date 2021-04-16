---
title: Propiedad EnableAutoReconnect de IMsRdpClientAdvancedSettings2
description: Especifica si se habilita el control de cliente para que se vuelva a conectar automáticamente a una sesión en caso de desconexión de la red.
ms.assetid: 9d820f78-bf7f-479a-ae6f-be0f0abe549c
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad EnableAutoReconnect
- Propiedad EnableAutoReconnect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad EnableAutoReconnect
- Propiedad EnableAutoReconnect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad EnableAutoReconnect
- Propiedad EnableAutoReconnect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad EnableAutoReconnect
- Propiedad EnableAutoReconnect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad EnableAutoReconnect
- Propiedad EnableAutoReconnect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad EnableAutoReconnect
- Propiedad EnableAutoReconnect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad EnableAutoReconnect
- Propiedad EnableAutoReconnect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad EnableAutoReconnect
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.EnableAutoReconnect
- IMsRdpClientAdvancedSettings2.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings2.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings3.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings4.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings5.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings6.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings7.put_EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.get_EnableAutoReconnect
- IMsRdpClientAdvancedSettings8.put_EnableAutoReconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f8d4a1345395b5b5843872df256fe7a113094e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686071"
---
# <a name="imsrdpclientadvancedsettings2enableautoreconnect-property"></a><span data-ttu-id="434ae-118">IMsRdpClientAdvancedSettings2:: EnableAutoReconnect (propiedad)</span><span class="sxs-lookup"><span data-stu-id="434ae-118">IMsRdpClientAdvancedSettings2::EnableAutoReconnect property</span></span>

<span data-ttu-id="434ae-119">Especifica si se habilita el control de cliente para que se vuelva a conectar automáticamente a una sesión en caso de desconexión de la red.</span><span class="sxs-lookup"><span data-stu-id="434ae-119">Specifies whether to enable the client control to reconnect automatically to a session in the event of a network disconnection.</span></span>

<span data-ttu-id="434ae-120">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="434ae-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="434ae-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="434ae-121">Syntax</span></span>


```C++
HRESULT put_EnableAutoReconnect(
  [in]  VARIANT_BOOL fEnableAutoReconnect
);

HRESULT get_EnableAutoReconnect(
  [out] VARIANT_BOOL *pfEnableAutoReconnect
);
```



## <a name="property-value"></a><span data-ttu-id="434ae-122">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="434ae-122">Property value</span></span>

<span data-ttu-id="434ae-123">Establézcalo en **Variant \_ true** para habilitar la reconexión automática y en **Variant \_ false** para deshabilitarla.</span><span class="sxs-lookup"><span data-stu-id="434ae-123">Set to **VARIANT\_TRUE** to enable automatic reconnection, and to **VARIANT\_FALSE** to disable it.</span></span> <span data-ttu-id="434ae-124">El valor predeterminado es **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="434ae-124">The default is **VARIANT\_TRUE**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="434ae-125">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="434ae-125">Error codes</span></span>

<span data-ttu-id="434ae-126">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="434ae-126">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="434ae-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="434ae-127">Remarks</span></span>

<span data-ttu-id="434ae-128">No se puede establecer esta propiedad cuando el control está conectado.</span><span class="sxs-lookup"><span data-stu-id="434ae-128">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="434ae-129">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="434ae-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="434ae-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="434ae-130">Requirements</span></span>



| <span data-ttu-id="434ae-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="434ae-131">Requirement</span></span> | <span data-ttu-id="434ae-132">Value</span><span class="sxs-lookup"><span data-stu-id="434ae-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="434ae-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="434ae-133">Minimum supported client</span></span><br/> | <span data-ttu-id="434ae-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="434ae-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="434ae-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="434ae-135">Minimum supported server</span></span><br/> | <span data-ttu-id="434ae-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="434ae-136">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="434ae-137">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="434ae-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="434ae-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="434ae-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="434ae-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="434ae-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="434ae-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="434ae-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="434ae-141">IID</span><span class="sxs-lookup"><span data-stu-id="434ae-141">IID</span></span><br/>                      | <span data-ttu-id="434ae-142">IID \_ IMsRdpClientAdvancedSettings2 se define como 9ac42117-2b76-4320-aa44-0e616ab8437b</span><span class="sxs-lookup"><span data-stu-id="434ae-142">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="434ae-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="434ae-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="434ae-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="434ae-144">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="434ae-145">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="434ae-145">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="434ae-146">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="434ae-146">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="434ae-147">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="434ae-147">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="434ae-148">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="434ae-148">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="434ae-149">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="434ae-149">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="434ae-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="434ae-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 





