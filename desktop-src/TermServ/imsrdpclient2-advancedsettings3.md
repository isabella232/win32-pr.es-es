---
title: Propiedad AdvancedSettings3 de IMsRdpClient2
description: Recupera un puntero a la interfaz IMsRdpClientAdvancedSettings2. La interfaz se puede utilizar para establecer la configuración avanzada del control de cliente.
ms.assetid: 69353bfa-973e-4c6a-8f7e-1b9514be2539
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad AdvancedSettings3
- Propiedad AdvancedSettings3 Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Servicios de Escritorio remoto de la interfaz IMsRdpClient2, propiedad AdvancedSettings3
- Propiedad AdvancedSettings3 Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Servicios de Escritorio remoto de la interfaz IMsRdpClient3, propiedad AdvancedSettings3
- Propiedad AdvancedSettings3 Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Servicios de Escritorio remoto de la interfaz IMsRdpClient4, propiedad AdvancedSettings3
- Propiedad AdvancedSettings3 Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad AdvancedSettings3
- Propiedad AdvancedSettings3 Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad AdvancedSettings3
- Propiedad AdvancedSettings3 Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad AdvancedSettings3
- Propiedad AdvancedSettings3 Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad AdvancedSettings3
- Propiedad AdvancedSettings3 Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad AdvancedSettings3
- Propiedad AdvancedSettings3 Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Servicios de Escritorio remoto de la interfaz IMsRdpClient10, propiedad AdvancedSettings3
topic_type:
- apiref
api_name:
- IMsRdpClient2.AdvancedSettings3
- IMsRdpClient2.get_AdvancedSettings3
- IMsRdpClient3.AdvancedSettings3
- IMsRdpClient3.get_AdvancedSettings3
- IMsRdpClient4.AdvancedSettings3
- IMsRdpClient4.get_AdvancedSettings3
- IMsRdpClient5.AdvancedSettings3
- IMsRdpClient5.get_AdvancedSettings3
- IMsRdpClient6.AdvancedSettings3
- IMsRdpClient6.get_AdvancedSettings3
- IMsRdpClient7.AdvancedSettings3
- IMsRdpClient7.get_AdvancedSettings3
- IMsRdpClient8.AdvancedSettings3
- IMsRdpClient8.get_AdvancedSettings3
- IMsRdpClient9.AdvancedSettings3
- IMsRdpClient9.get_AdvancedSettings3
- IMsRdpClient10.AdvancedSettings3
- IMsRdpClient10.get_AdvancedSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf16d56eaff321d313e3a27eb6dd774ef67e13ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359761"
---
# <a name="imsrdpclient2advancedsettings3-property"></a><span data-ttu-id="e627f-123">IMsRdpClient2:: AdvancedSettings3 (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e627f-123">IMsRdpClient2::AdvancedSettings3 property</span></span>

<span data-ttu-id="e627f-124">Recupera un puntero a la interfaz [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="e627f-124">Retrieves a pointer to the [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) interface.</span></span> <span data-ttu-id="e627f-125">La interfaz se puede utilizar para establecer la configuración avanzada del control de cliente.</span><span class="sxs-lookup"><span data-stu-id="e627f-125">The interface can be used to set advanced settings for the client control.</span></span>

<span data-ttu-id="e627f-126">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e627f-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e627f-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e627f-127">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings3(
  [out] IMsRdpClientAdvancedSettings2 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="e627f-128">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e627f-128">Property value</span></span>

<span data-ttu-id="e627f-129">Recupera un puntero a la interfaz [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="e627f-129">Retrieves a pointer to the [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) interface.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e627f-130">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="e627f-130">Error codes</span></span>

<span data-ttu-id="e627f-131">Si el método se ejecuta correctamente, se devuelve **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="e627f-131">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="e627f-132">Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="e627f-132">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="e627f-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e627f-133">Remarks</span></span>

<span data-ttu-id="e627f-134">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e627f-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e627f-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e627f-135">Requirements</span></span>



| <span data-ttu-id="e627f-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="e627f-136">Requirement</span></span> | <span data-ttu-id="e627f-137">Value</span><span class="sxs-lookup"><span data-stu-id="e627f-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e627f-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e627f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e627f-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e627f-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e627f-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e627f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e627f-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e627f-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e627f-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e627f-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="e627f-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e627f-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e627f-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e627f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e627f-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e627f-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e627f-146">IID</span><span class="sxs-lookup"><span data-stu-id="e627f-146">IID</span></span><br/>                      | <span data-ttu-id="e627f-147">IID \_ IMsRdpClient2 se define como e7e17dc4-3b71-4ba7-a8e6-281ffadca28f</span><span class="sxs-lookup"><span data-stu-id="e627f-147">IID\_IMsRdpClient2 is defined as e7e17dc4-3b71-4ba7-a8e6-281ffadca28f</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e627f-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="e627f-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e627f-149">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="e627f-149">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="e627f-150">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="e627f-150">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="e627f-151">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="e627f-151">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="e627f-152">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="e627f-152">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="e627f-153">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="e627f-153">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="e627f-154">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="e627f-154">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="e627f-155">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="e627f-155">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="e627f-156">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="e627f-156">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="e627f-157">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="e627f-157">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





