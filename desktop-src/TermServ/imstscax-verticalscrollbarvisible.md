---
title: Propiedad VerticalScrollBarVisible de IMsTscAx
description: Indica si el control muestra una barra de desplazamiento vertical.
ms.assetid: b31e2db3-b367-4900-a2c6-51fd794341c2
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad VerticalScrollBarVisible
- Propiedad VerticalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsTscAx
- Servicios de Escritorio remoto de la interfaz IMsTscAx, propiedad VerticalScrollBarVisible
- Propiedad VerticalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient
- Servicios de Escritorio remoto de la interfaz IMsRdpClient, propiedad VerticalScrollBarVisible
- Propiedad VerticalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Servicios de Escritorio remoto de la interfaz IMsRdpClient2, propiedad VerticalScrollBarVisible
- Propiedad VerticalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Servicios de Escritorio remoto de la interfaz IMsRdpClient3, propiedad VerticalScrollBarVisible
- Propiedad VerticalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Servicios de Escritorio remoto de la interfaz IMsRdpClient4, propiedad VerticalScrollBarVisible
- Propiedad VerticalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad VerticalScrollBarVisible
- Propiedad VerticalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad VerticalScrollBarVisible
- Propiedad VerticalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad VerticalScrollBarVisible
- Propiedad VerticalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad VerticalScrollBarVisible
- Propiedad VerticalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad VerticalScrollBarVisible
topic_type:
- apiref
api_name:
- IMsTscAx.VerticalScrollBarVisible
- IMsTscAx.get_VerticalScrollBarVisible
- IMsRdpClient.VerticalScrollBarVisible
- IMsRdpClient.get_VerticalScrollBarVisible
- IMsRdpClient2.VerticalScrollBarVisible
- IMsRdpClient2.get_VerticalScrollBarVisible
- IMsRdpClient3.VerticalScrollBarVisible
- IMsRdpClient3.get_VerticalScrollBarVisible
- IMsRdpClient4.VerticalScrollBarVisible
- IMsRdpClient4.get_VerticalScrollBarVisible
- IMsRdpClient5.VerticalScrollBarVisible
- IMsRdpClient5.get_VerticalScrollBarVisible
- IMsRdpClient6.VerticalScrollBarVisible
- IMsRdpClient6.get_VerticalScrollBarVisible
- IMsRdpClient7.VerticalScrollBarVisible
- IMsRdpClient7.get_VerticalScrollBarVisible
- IMsRdpClient8.VerticalScrollBarVisible
- IMsRdpClient8.get_VerticalScrollBarVisible
- IMsRdpClient9.VerticalScrollBarVisible
- IMsRdpClient9.get_VerticalScrollBarVisible
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1365a0ab6d4a1411d78496cf157f3bc49fe5db15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489670"
---
# <a name="imstscaxverticalscrollbarvisible-property"></a><span data-ttu-id="1c093-124">IMsTscAx:: VerticalScrollBarVisible (propiedad)</span><span class="sxs-lookup"><span data-stu-id="1c093-124">IMsTscAx::VerticalScrollBarVisible property</span></span>

<span data-ttu-id="1c093-125">Indica si el control muestra una barra de desplazamiento vertical.</span><span class="sxs-lookup"><span data-stu-id="1c093-125">Indicates whether the control displays a vertical scroll bar.</span></span>

<span data-ttu-id="1c093-126">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1c093-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c093-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c093-127">Syntax</span></span>


```C++
HRESULT get_VerticalScrollBarVisible(
  [out] BOOL *pfVScrollVisible
);
```



## <a name="property-value"></a><span data-ttu-id="1c093-128">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="1c093-128">Property value</span></span>

<span data-ttu-id="1c093-129">El valor de este parámetro es **true** si la barra de desplazamiento vertical está visible y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="1c093-129">The value of this parameter is **TRUE** if the vertical scroll bar is visible, and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1c093-130">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="1c093-130">Error codes</span></span>

<span data-ttu-id="1c093-131">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="1c093-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c093-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1c093-132">Remarks</span></span>

<span data-ttu-id="1c093-133">El control muestra automáticamente una barra de desplazamiento vertical si el alto del control actual es menor que el alto del escritorio.</span><span class="sxs-lookup"><span data-stu-id="1c093-133">The control automatically displays a vertical scroll bar if the height of the current control is less than the height of the desktop.</span></span>

<span data-ttu-id="1c093-134">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="1c093-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1c093-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c093-135">Requirements</span></span>



| <span data-ttu-id="1c093-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c093-136">Requirement</span></span> | <span data-ttu-id="1c093-137">Value</span><span class="sxs-lookup"><span data-stu-id="1c093-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c093-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c093-138">Minimum supported client</span></span><br/> | <span data-ttu-id="1c093-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c093-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1c093-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c093-140">Minimum supported server</span></span><br/> | <span data-ttu-id="1c093-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c093-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1c093-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1c093-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="1c093-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c093-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1c093-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1c093-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c093-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c093-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="1c093-146">IID</span><span class="sxs-lookup"><span data-stu-id="1c093-146">IID</span></span><br/>                      | <span data-ttu-id="1c093-147">IID \_ IMsTscAx se define como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="1c093-147">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="1c093-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c093-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c093-149">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="1c093-149">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="1c093-150">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="1c093-150">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="1c093-151">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="1c093-151">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="1c093-152">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="1c093-152">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="1c093-153">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="1c093-153">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="1c093-154">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="1c093-154">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="1c093-155">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="1c093-155">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="1c093-156">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="1c093-156">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="1c093-157">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="1c093-157">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="1c093-158">**HorizontalScrollBarVisible**</span><span class="sxs-lookup"><span data-stu-id="1c093-158">**HorizontalScrollBarVisible**</span></span>](imstscax-horizontalscrollbarvisible.md)
</dt> <dt>

[<span data-ttu-id="1c093-159">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="1c093-159">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





