---
title: Propiedad AdvancedSettings4 de IMsRdpClient3
description: Recupera un puntero a la interfaz IMsRdpClientAdvancedSettings3.
ms.assetid: 30935099-7f33-4745-8a31-f9a28ab78b63
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad AdvancedSettings4
- Propiedad AdvancedSettings4 Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Servicios de Escritorio remoto de la interfaz IMsRdpClient3, propiedad AdvancedSettings4
- Propiedad AdvancedSettings4 Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Servicios de Escritorio remoto de la interfaz IMsRdpClient4, propiedad AdvancedSettings4
- Propiedad AdvancedSettings4 Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad AdvancedSettings4
- Propiedad AdvancedSettings4 Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad AdvancedSettings4
- Propiedad AdvancedSettings4 Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad AdvancedSettings4
- Propiedad AdvancedSettings4 Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad AdvancedSettings4
- Propiedad AdvancedSettings4 Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad AdvancedSettings4
- Propiedad AdvancedSettings4 Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Servicios de Escritorio remoto de la interfaz IMsRdpClient10, propiedad AdvancedSettings4
topic_type:
- apiref
api_name:
- IMsRdpClient3.AdvancedSettings4
- IMsRdpClient3.get_AdvancedSettings4
- IMsRdpClient4.AdvancedSettings4
- IMsRdpClient4.get_AdvancedSettings4
- IMsRdpClient5.AdvancedSettings4
- IMsRdpClient5.get_AdvancedSettings4
- IMsRdpClient6.AdvancedSettings4
- IMsRdpClient6.get_AdvancedSettings4
- IMsRdpClient7.AdvancedSettings4
- IMsRdpClient7.get_AdvancedSettings4
- IMsRdpClient8.AdvancedSettings4
- IMsRdpClient8.get_AdvancedSettings4
- IMsRdpClient9.AdvancedSettings4
- IMsRdpClient9.get_AdvancedSettings4
- IMsRdpClient10.AdvancedSettings4
- IMsRdpClient10.get_AdvancedSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7a229c28b645e7920212a04cc44ca5a9ce42be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905068"
---
# <a name="imsrdpclient3advancedsettings4-property"></a><span data-ttu-id="4ebe7-120">IMsRdpClient3:: AdvancedSettings4 (propiedad)</span><span class="sxs-lookup"><span data-stu-id="4ebe7-120">IMsRdpClient3::AdvancedSettings4 property</span></span>

<span data-ttu-id="4ebe7-121">Recupera un puntero a la interfaz [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) .</span><span class="sxs-lookup"><span data-stu-id="4ebe7-121">Retrieves a pointer to the [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) interface.</span></span>

<span data-ttu-id="4ebe7-122">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4ebe7-122">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ebe7-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ebe7-123">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings4(
  [out] IMsRdpClientAdvancedSettings3 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="4ebe7-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4ebe7-124">Property value</span></span>

<span data-ttu-id="4ebe7-125">Puntero a la interfaz [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) .</span><span class="sxs-lookup"><span data-stu-id="4ebe7-125">Pointer to the [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) interface.</span></span> <span data-ttu-id="4ebe7-126">La interfaz se puede utilizar para establecer la configuración avanzada del control de cliente.</span><span class="sxs-lookup"><span data-stu-id="4ebe7-126">The interface can be used to set advanced settings for the client control.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4ebe7-127">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="4ebe7-127">Error codes</span></span>

<span data-ttu-id="4ebe7-128">Si el método se ejecuta correctamente, se devuelve **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="4ebe7-128">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="4ebe7-129">Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="4ebe7-129">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ebe7-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ebe7-130">Remarks</span></span>

<span data-ttu-id="4ebe7-131">No se puede establecer esta propiedad cuando el control está conectado.</span><span class="sxs-lookup"><span data-stu-id="4ebe7-131">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="4ebe7-132">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="4ebe7-132">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4ebe7-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ebe7-133">Requirements</span></span>



| <span data-ttu-id="4ebe7-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ebe7-134">Requirement</span></span> | <span data-ttu-id="4ebe7-135">Value</span><span class="sxs-lookup"><span data-stu-id="4ebe7-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ebe7-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ebe7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4ebe7-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ebe7-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4ebe7-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4ebe7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4ebe7-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ebe7-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4ebe7-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="4ebe7-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="4ebe7-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ebe7-141"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4ebe7-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4ebe7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ebe7-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ebe7-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4ebe7-144">IID</span><span class="sxs-lookup"><span data-stu-id="4ebe7-144">IID</span></span><br/>                      | <span data-ttu-id="4ebe7-145">IID \_ IMsRdpClient3 se define como 91b7cbc5-a72e-4fa0-9300-d647d7e897ff</span><span class="sxs-lookup"><span data-stu-id="4ebe7-145">IID\_IMsRdpClient3 is defined as 91b7cbc5-a72e-4fa0-9300-d647d7e897ff</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4ebe7-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ebe7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ebe7-147">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="4ebe7-147">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="4ebe7-148">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="4ebe7-148">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="4ebe7-149">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="4ebe7-149">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="4ebe7-150">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="4ebe7-150">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="4ebe7-151">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="4ebe7-151">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="4ebe7-152">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="4ebe7-152">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="4ebe7-153">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="4ebe7-153">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="4ebe7-154">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="4ebe7-154">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





