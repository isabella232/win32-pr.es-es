---
title: Propiedad AdvancedSettings5 de IMsRdpClient4
description: Recupera un puntero a una interfaz IMsRdpClientAdvancedSettings4.
ms.assetid: 2dd0cc5f-7822-485f-8b3f-12407af1e091
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad AdvancedSettings5
- Propiedad AdvancedSettings5 Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Servicios de Escritorio remoto de la interfaz IMsRdpClient4, propiedad AdvancedSettings5
- Propiedad AdvancedSettings5 Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad AdvancedSettings5
- Propiedad AdvancedSettings5 Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad AdvancedSettings5
- Propiedad AdvancedSettings5 Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad AdvancedSettings5
- Propiedad AdvancedSettings5 Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad AdvancedSettings5
- Propiedad AdvancedSettings5 Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad AdvancedSettings5
- Propiedad AdvancedSettings5 Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Servicios de Escritorio remoto de la interfaz IMsRdpClient10, propiedad AdvancedSettings5
topic_type:
- apiref
api_name:
- IMsRdpClient4.AdvancedSettings5
- IMsRdpClient4.get_AdvancedSettings5
- IMsRdpClient5.AdvancedSettings5
- IMsRdpClient5.get_AdvancedSettings5
- IMsRdpClient6.AdvancedSettings5
- IMsRdpClient6.get_AdvancedSettings5
- IMsRdpClient7.AdvancedSettings5
- IMsRdpClient7.get_AdvancedSettings5
- IMsRdpClient8.AdvancedSettings5
- IMsRdpClient8.get_AdvancedSettings5
- IMsRdpClient9.AdvancedSettings5
- IMsRdpClient9.get_AdvancedSettings5
- IMsRdpClient10.AdvancedSettings5
- IMsRdpClient10.get_AdvancedSettings5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ad96588b2109375aed23c1024ef925936cb3368
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535404"
---
# <a name="imsrdpclient4advancedsettings5-property"></a><span data-ttu-id="9cdd6-118">IMsRdpClient4:: AdvancedSettings5 (propiedad)</span><span class="sxs-lookup"><span data-stu-id="9cdd6-118">IMsRdpClient4::AdvancedSettings5 property</span></span>

<span data-ttu-id="9cdd6-119">Recupera un puntero a una interfaz [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) .</span><span class="sxs-lookup"><span data-stu-id="9cdd6-119">Retrieves a pointer to an [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) interface.</span></span>

<span data-ttu-id="9cdd6-120">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9cdd6-120">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cdd6-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9cdd6-121">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings5(
  [out] IMsRdpClientAdvancedSettings4 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="9cdd6-122">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9cdd6-122">Property value</span></span>

<span data-ttu-id="9cdd6-123">Puntero a la interfaz [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) .</span><span class="sxs-lookup"><span data-stu-id="9cdd6-123">A pointer to the [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) interface.</span></span> <span data-ttu-id="9cdd6-124">La interfaz se puede utilizar para establecer la configuración avanzada del control de cliente.</span><span class="sxs-lookup"><span data-stu-id="9cdd6-124">The interface can be used to set advanced settings for the client control.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9cdd6-125">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="9cdd6-125">Error codes</span></span>

<span data-ttu-id="9cdd6-126">Si el método se ejecuta correctamente, se devuelve **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="9cdd6-126">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="9cdd6-127">Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="9cdd6-127">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="9cdd6-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9cdd6-128">Remarks</span></span>

<span data-ttu-id="9cdd6-129">No se puede establecer esta propiedad cuando el control está conectado.</span><span class="sxs-lookup"><span data-stu-id="9cdd6-129">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="9cdd6-130">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="9cdd6-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9cdd6-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cdd6-131">Requirements</span></span>



| <span data-ttu-id="9cdd6-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cdd6-132">Requirement</span></span> | <span data-ttu-id="9cdd6-133">Value</span><span class="sxs-lookup"><span data-stu-id="9cdd6-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9cdd6-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9cdd6-134">Minimum supported client</span></span><br/> | <span data-ttu-id="9cdd6-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cdd6-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9cdd6-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9cdd6-136">Minimum supported server</span></span><br/> | <span data-ttu-id="9cdd6-137">Windows Server 2008, Windows Server 2008 con SP1</span><span class="sxs-lookup"><span data-stu-id="9cdd6-137">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="9cdd6-138">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9cdd6-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="9cdd6-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cdd6-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9cdd6-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9cdd6-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9cdd6-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9cdd6-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9cdd6-142">IID</span><span class="sxs-lookup"><span data-stu-id="9cdd6-142">IID</span></span><br/>                      | <span data-ttu-id="9cdd6-143">IMsRdpClient4 se define como 095E0738-D97D-488b-B9F6-DD0E8D66C0DE</span><span class="sxs-lookup"><span data-stu-id="9cdd6-143">IMsRdpClient4 is defined as 095E0738-D97D-488b-B9F6-DD0E8D66C0DE</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="9cdd6-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="9cdd6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cdd6-145">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="9cdd6-145">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="9cdd6-146">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="9cdd6-146">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="9cdd6-147">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="9cdd6-147">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="9cdd6-148">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="9cdd6-148">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="9cdd6-149">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="9cdd6-149">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="9cdd6-150">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="9cdd6-150">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="9cdd6-151">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="9cdd6-151">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





