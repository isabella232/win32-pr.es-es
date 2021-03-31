---
title: Propiedad CanAutoReconnect de IMsRdpClientAdvancedSettings2
description: Especifica si el control de cliente puede volver a conectarse automáticamente a la sesión actual en caso de desconexión de red.
ms.assetid: 0a7ecf90-832b-4ec1-990b-7fe26ff134b1
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad CanAutoReconnect
- Propiedad CanAutoReconnect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad CanAutoReconnect
- Propiedad CanAutoReconnect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad CanAutoReconnect
- Propiedad CanAutoReconnect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad CanAutoReconnect
- Propiedad CanAutoReconnect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad CanAutoReconnect
- Propiedad CanAutoReconnect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad CanAutoReconnect
- Propiedad CanAutoReconnect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad CanAutoReconnect
- Propiedad CanAutoReconnect Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad CanAutoReconnect
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.CanAutoReconnect
- IMsRdpClientAdvancedSettings2.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings3.CanAutoReconnect
- IMsRdpClientAdvancedSettings3.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings4.CanAutoReconnect
- IMsRdpClientAdvancedSettings4.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings5.CanAutoReconnect
- IMsRdpClientAdvancedSettings5.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings6.CanAutoReconnect
- IMsRdpClientAdvancedSettings6.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings7.CanAutoReconnect
- IMsRdpClientAdvancedSettings7.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings8.CanAutoReconnect
- IMsRdpClientAdvancedSettings8.get_CanAutoReconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8c8f4113c39b79783978252136c50d2111ed0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905012"
---
# <a name="imsrdpclientadvancedsettings2canautoreconnect-property"></a><span data-ttu-id="88f39-118">IMsRdpClientAdvancedSettings2:: CanAutoReconnect (propiedad)</span><span class="sxs-lookup"><span data-stu-id="88f39-118">IMsRdpClientAdvancedSettings2::CanAutoReconnect property</span></span>

<span data-ttu-id="88f39-119">Especifica si el control de cliente puede volver a conectarse automáticamente a la sesión actual en caso de desconexión de red.</span><span class="sxs-lookup"><span data-stu-id="88f39-119">Specifies whether the client control is able to reconnect automatically to the current session in the event of a network disconnection.</span></span>

<span data-ttu-id="88f39-120">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="88f39-120">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="88f39-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="88f39-121">Syntax</span></span>


```C++
HRESULT get_CanAutoReconnect(
  [out] VARIANT_BOOL *pfCanAutoReconnect
);
```



## <a name="property-value"></a><span data-ttu-id="88f39-122">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="88f39-122">Property value</span></span>

<span data-ttu-id="88f39-123">Recibe la **variante \_ true** si el control puede volver a conectarse automáticamente y la **variante \_ false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="88f39-123">Receives **VARIANT\_TRUE** if the control is able to automatically reconnect, and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="88f39-124">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="88f39-124">Error codes</span></span>

<span data-ttu-id="88f39-125">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="88f39-125">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="88f39-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88f39-126">Remarks</span></span>

<span data-ttu-id="88f39-127">Entre las situaciones en las que la reconexión automática podría no estar habilitada se incluyen aquellas en las que un administrador usa la Directiva de grupo para deshabilitar reconexión automática del y los entornos heredados que no admiten la reconexión automática.</span><span class="sxs-lookup"><span data-stu-id="88f39-127">Situations in which automatic reconnection might not be enabled include those in which an administrator uses group policy to disable autoreconnection, and legacy environments that do not support automatic reconnection.</span></span>

<span data-ttu-id="88f39-128">No se puede establecer esta propiedad cuando el control está conectado.</span><span class="sxs-lookup"><span data-stu-id="88f39-128">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="88f39-129">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="88f39-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="88f39-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88f39-130">Requirements</span></span>



| <span data-ttu-id="88f39-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="88f39-131">Requirement</span></span> | <span data-ttu-id="88f39-132">Value</span><span class="sxs-lookup"><span data-stu-id="88f39-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88f39-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88f39-133">Minimum supported client</span></span><br/> | <span data-ttu-id="88f39-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88f39-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="88f39-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88f39-135">Minimum supported server</span></span><br/> | <span data-ttu-id="88f39-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88f39-136">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="88f39-137">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="88f39-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="88f39-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88f39-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="88f39-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="88f39-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="88f39-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88f39-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="88f39-141">IID</span><span class="sxs-lookup"><span data-stu-id="88f39-141">IID</span></span><br/>                      | <span data-ttu-id="88f39-142">IID \_ IMsRdpClientAdvancedSettings2 se define como 9ac42117-2b76-4320-aa44-0e616ab8437b</span><span class="sxs-lookup"><span data-stu-id="88f39-142">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="88f39-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="88f39-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88f39-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="88f39-144">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="88f39-145">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="88f39-145">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="88f39-146">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="88f39-146">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="88f39-147">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="88f39-147">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="88f39-148">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="88f39-148">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="88f39-149">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="88f39-149">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="88f39-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="88f39-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 





