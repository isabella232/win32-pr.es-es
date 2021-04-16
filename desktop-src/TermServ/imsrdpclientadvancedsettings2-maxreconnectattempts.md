---
title: Propiedad MaxReconnectAttempts de IMsRdpClientAdvancedSettings2
description: Especifica el número de veces que se intentará volver a conectar durante la reconexión automática.
ms.assetid: 24bfd3b6-d2de-4e46-8b5f-a4702c18a93c
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad MaxReconnectAttempts
- Propiedad MaxReconnectAttempts Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad MaxReconnectAttempts
- Propiedad MaxReconnectAttempts Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad MaxReconnectAttempts
- Propiedad MaxReconnectAttempts Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad MaxReconnectAttempts
- Propiedad MaxReconnectAttempts Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad MaxReconnectAttempts
- Propiedad MaxReconnectAttempts Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad MaxReconnectAttempts
- Propiedad MaxReconnectAttempts Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad MaxReconnectAttempts
- Propiedad MaxReconnectAttempts Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad MaxReconnectAttempts
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings2.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings2.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings3.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings4.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings5.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings6.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings7.put_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.get_MaxReconnectAttempts
- IMsRdpClientAdvancedSettings8.put_MaxReconnectAttempts
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 322796a2d6ca6a13476dad58af8c385b8bdfa1fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686070"
---
# <a name="imsrdpclientadvancedsettings2maxreconnectattempts-property"></a><span data-ttu-id="a8389-118">IMsRdpClientAdvancedSettings2:: MaxReconnectAttempts (propiedad)</span><span class="sxs-lookup"><span data-stu-id="a8389-118">IMsRdpClientAdvancedSettings2::MaxReconnectAttempts property</span></span>

<span data-ttu-id="a8389-119">Especifica el número de veces que se intentará volver a conectar durante la reconexión automática.</span><span class="sxs-lookup"><span data-stu-id="a8389-119">Specifies the number of times to try to reconnect during automatic reconnection.</span></span>

<span data-ttu-id="a8389-120">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="a8389-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8389-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8389-121">Syntax</span></span>


```C++
HRESULT put_MaxReconnectAttempts(
  [in]  LONG MaxReconnectAttempts
);

HRESULT get_MaxReconnectAttempts(
  [out] LONG *pMaxReconnectAttempts
);
```



## <a name="property-value"></a><span data-ttu-id="a8389-122">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="a8389-122">Property value</span></span>

<span data-ttu-id="a8389-123">El nuevo número de reintentos.</span><span class="sxs-lookup"><span data-stu-id="a8389-123">The new number of retries.</span></span> <span data-ttu-id="a8389-124">Los valores válidos son de 0 a 200, ambos incluidos.</span><span class="sxs-lookup"><span data-stu-id="a8389-124">The valid values are 0 to 200, inclusive.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a8389-125">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="a8389-125">Error codes</span></span>

<span data-ttu-id="a8389-126">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="a8389-126">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8389-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8389-127">Remarks</span></span>

<span data-ttu-id="a8389-128">No se puede establecer esta propiedad cuando el control está conectado.</span><span class="sxs-lookup"><span data-stu-id="a8389-128">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="a8389-129">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="a8389-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8389-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8389-130">Requirements</span></span>



| <span data-ttu-id="a8389-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8389-131">Requirement</span></span> | <span data-ttu-id="a8389-132">Value</span><span class="sxs-lookup"><span data-stu-id="a8389-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8389-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8389-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a8389-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8389-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="a8389-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8389-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a8389-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8389-136">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="a8389-137">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a8389-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="a8389-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8389-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a8389-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a8389-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8389-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8389-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="a8389-141">IID</span><span class="sxs-lookup"><span data-stu-id="a8389-141">IID</span></span><br/>                      | <span data-ttu-id="a8389-142">IID \_ IMsRdpClientAdvancedSettings2 se define como 9ac42117-2b76-4320-aa44-0e616ab8437b</span><span class="sxs-lookup"><span data-stu-id="a8389-142">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8389-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8389-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8389-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="a8389-144">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="a8389-145">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="a8389-145">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="a8389-146">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="a8389-146">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="a8389-147">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="a8389-147">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="a8389-148">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="a8389-148">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="a8389-149">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="a8389-149">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="a8389-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="a8389-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 





