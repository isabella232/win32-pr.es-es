---
title: Propiedad IMsRdpClient ColorDepth
description: Profundidad de color (en bits por píxel) de la conexión del control.
ms.assetid: 9ba4d8fe-20cd-40e9-a71a-0dce0ddd29fc
ms.tgt_platform: multiple
keywords:
- Propiedad ColorDepth Servicios de Escritorio remoto
- Propiedad ColorDepth Servicios de Escritorio remoto, interfaz IMsRdpClient
- IMsRdpClient interface Servicios de Escritorio remoto, ColorDepth (propiedad)
- Propiedad ColorDepth Servicios de Escritorio remoto, interfaz IMsRdpClient2
- IMsRdpClient2 interface Servicios de Escritorio remoto, ColorDepth (propiedad)
- Propiedad ColorDepth Servicios de Escritorio remoto, interfaz IMsRdpClient3
- IMsRdpClient3 interface Servicios de Escritorio remoto, ColorDepth (propiedad)
- Propiedad ColorDepth Servicios de Escritorio remoto, interfaz IMsRdpClient4
- IMsRdpClient4 interface Servicios de Escritorio remoto, ColorDepth (propiedad)
- Propiedad ColorDepth Servicios de Escritorio remoto, interfaz IMsRdpClient5
- IMsRdpClient5 interface Servicios de Escritorio remoto, ColorDepth (propiedad)
- Propiedad ColorDepth Servicios de Escritorio remoto, interfaz IMsRdpClient6
- IMsRdpClient6 interface Servicios de Escritorio remoto, ColorDepth (propiedad)
- Propiedad ColorDepth Servicios de Escritorio remoto, interfaz IMsRdpClient7
- IMsRdpClient7 interface Servicios de Escritorio remoto, ColorDepth (propiedad)
- Propiedad ColorDepth Servicios de Escritorio remoto, interfaz IMsRdpClient8
- IMsRdpClient8 interface Servicios de Escritorio remoto, ColorDepth (propiedad)
- Propiedad ColorDepth Servicios de Escritorio remoto, interfaz IMsRdpClient9
- IMsRdpClient9 interface Servicios de Escritorio remoto, ColorDepth (propiedad)
- Propiedad ColorDepth Servicios de Escritorio remoto, interfaz IMsRdpClient10
- IMsRdpClient10 interface Servicios de Escritorio remoto, ColorDepth (propiedad)
topic_type:
- apiref
api_name:
- IMsRdpClient.ColorDepth
- IMsRdpClient.get_ColorDepth
- IMsRdpClient.put_ColorDepth
- IMsRdpClient2.ColorDepth
- IMsRdpClient2.get_ColorDepth
- IMsRdpClient2.put_ColorDepth
- IMsRdpClient3.ColorDepth
- IMsRdpClient3.get_ColorDepth
- IMsRdpClient3.put_ColorDepth
- IMsRdpClient4.ColorDepth
- IMsRdpClient4.get_ColorDepth
- IMsRdpClient4.put_ColorDepth
- IMsRdpClient5.ColorDepth
- IMsRdpClient5.get_ColorDepth
- IMsRdpClient5.put_ColorDepth
- IMsRdpClient6.ColorDepth
- IMsRdpClient6.get_ColorDepth
- IMsRdpClient6.put_ColorDepth
- IMsRdpClient7.ColorDepth
- IMsRdpClient7.get_ColorDepth
- IMsRdpClient7.put_ColorDepth
- IMsRdpClient8.ColorDepth
- IMsRdpClient8.get_ColorDepth
- IMsRdpClient8.put_ColorDepth
- IMsRdpClient9.ColorDepth
- IMsRdpClient9.get_ColorDepth
- IMsRdpClient9.put_ColorDepth
- IMsRdpClient10.ColorDepth
- IMsRdpClient10.get_ColorDepth
- IMsRdpClient10.put_ColorDepth
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5099deff3913d23173a466245cbf08fd5b95a6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151018"
---
# <a name="imsrdpclientcolordepth-property"></a><span data-ttu-id="8ba4b-124">IMsRdpClient:: ColorDepth (propiedad)</span><span class="sxs-lookup"><span data-stu-id="8ba4b-124">IMsRdpClient::ColorDepth property</span></span>

<span data-ttu-id="8ba4b-125">Profundidad de color (en bits por píxel) de la conexión del control.</span><span class="sxs-lookup"><span data-stu-id="8ba4b-125">The color depth (in bits per pixel) for the control's connection.</span></span>

<span data-ttu-id="8ba4b-126">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="8ba4b-126">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ba4b-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ba4b-127">Syntax</span></span>


```C++
HRESULT put_ColorDepth(
  [in]  LONG colorDepth
);

HRESULT get_ColorDepth(
  [out] LONG pcolorDepth
);
```



## <a name="property-value"></a><span data-ttu-id="8ba4b-128">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8ba4b-128">Property value</span></span>

<span data-ttu-id="8ba4b-129">Profundidad de color.</span><span class="sxs-lookup"><span data-stu-id="8ba4b-129">The color depth.</span></span> <span data-ttu-id="8ba4b-130">Los valores son 8, 15, 16, 24 y 32 bits por píxel.</span><span class="sxs-lookup"><span data-stu-id="8ba4b-130">Values include 8, 15, 16, 24, and 32 bits per pixel.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8ba4b-131">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="8ba4b-131">Error codes</span></span>

<span data-ttu-id="8ba4b-132">Si los métodos se realizan correctamente, se devuelve **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="8ba4b-132">If the methods succeed, **S\_OK** is returned.</span></span> <span data-ttu-id="8ba4b-133">Cualquier otro valor **HRESULT** indica que se produjo un error en la llamada.</span><span class="sxs-lookup"><span data-stu-id="8ba4b-133">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ba4b-134">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ba4b-134">Remarks</span></span>

<span data-ttu-id="8ba4b-135">No se puede establecer esta propiedad cuando el control está conectado.</span><span class="sxs-lookup"><span data-stu-id="8ba4b-135">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="8ba4b-136">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="8ba4b-136">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ba4b-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ba4b-137">Requirements</span></span>



| <span data-ttu-id="8ba4b-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ba4b-138">Requirement</span></span> | <span data-ttu-id="8ba4b-139">Value</span><span class="sxs-lookup"><span data-stu-id="8ba4b-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ba4b-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ba4b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="8ba4b-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8ba4b-141">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8ba4b-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ba4b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="8ba4b-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8ba4b-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8ba4b-144">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8ba4b-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="8ba4b-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ba4b-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8ba4b-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8ba4b-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ba4b-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ba4b-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8ba4b-148">IID</span><span class="sxs-lookup"><span data-stu-id="8ba4b-148">IID</span></span><br/>                      | <span data-ttu-id="8ba4b-149">IID \_ IMsRdpClient se define como 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span><span class="sxs-lookup"><span data-stu-id="8ba4b-149">IID\_IMsRdpClient is defined as 92b4a539-7115-4b7c-a5a9-e5d9efc2780a</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="8ba4b-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ba4b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ba4b-151">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="8ba4b-151">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="8ba4b-152">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="8ba4b-152">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="8ba4b-153">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="8ba4b-153">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="8ba4b-154">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="8ba4b-154">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="8ba4b-155">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="8ba4b-155">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="8ba4b-156">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="8ba4b-156">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="8ba4b-157">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="8ba4b-157">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="8ba4b-158">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="8ba4b-158">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="8ba4b-159">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="8ba4b-159">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="8ba4b-160">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="8ba4b-160">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





