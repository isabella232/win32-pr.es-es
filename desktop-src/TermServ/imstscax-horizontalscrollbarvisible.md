---
title: Propiedad HorizontalScrollBarVisible de IMsTscAx
description: Indica si el control ha mostrado una barra de desplazamiento horizontal.
ms.assetid: d3c22c5f-321f-476e-bcdb-224eb988a7bb
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad HorizontalScrollBarVisible
- Propiedad HorizontalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsTscAx
- Servicios de Escritorio remoto de la interfaz IMsTscAx, propiedad HorizontalScrollBarVisible
- Propiedad HorizontalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient
- Servicios de Escritorio remoto de la interfaz IMsRdpClient, propiedad HorizontalScrollBarVisible
- Propiedad HorizontalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient2
- Servicios de Escritorio remoto de la interfaz IMsRdpClient2, propiedad HorizontalScrollBarVisible
- Propiedad HorizontalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient3
- Servicios de Escritorio remoto de la interfaz IMsRdpClient3, propiedad HorizontalScrollBarVisible
- Propiedad HorizontalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient4
- Servicios de Escritorio remoto de la interfaz IMsRdpClient4, propiedad HorizontalScrollBarVisible
- Propiedad HorizontalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad HorizontalScrollBarVisible
- Propiedad HorizontalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad HorizontalScrollBarVisible
- Propiedad HorizontalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad HorizontalScrollBarVisible
- Propiedad HorizontalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad HorizontalScrollBarVisible
- Propiedad HorizontalScrollBarVisible Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad HorizontalScrollBarVisible
topic_type:
- apiref
api_name:
- IMsTscAx.HorizontalScrollBarVisible
- IMsTscAx.get_HorizontalScrollBarVisible
- IMsRdpClient.HorizontalScrollBarVisible
- IMsRdpClient.get_HorizontalScrollBarVisible
- IMsRdpClient2.HorizontalScrollBarVisible
- IMsRdpClient2.get_HorizontalScrollBarVisible
- IMsRdpClient3.HorizontalScrollBarVisible
- IMsRdpClient3.get_HorizontalScrollBarVisible
- IMsRdpClient4.HorizontalScrollBarVisible
- IMsRdpClient4.get_HorizontalScrollBarVisible
- IMsRdpClient5.HorizontalScrollBarVisible
- IMsRdpClient5.get_HorizontalScrollBarVisible
- IMsRdpClient6.HorizontalScrollBarVisible
- IMsRdpClient6.get_HorizontalScrollBarVisible
- IMsRdpClient7.HorizontalScrollBarVisible
- IMsRdpClient7.get_HorizontalScrollBarVisible
- IMsRdpClient8.HorizontalScrollBarVisible
- IMsRdpClient8.get_HorizontalScrollBarVisible
- IMsRdpClient9.HorizontalScrollBarVisible
- IMsRdpClient9.get_HorizontalScrollBarVisible
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08fa2abb97a28af013e5791bcbd643f3f479d5c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079298"
---
# <a name="imstscaxhorizontalscrollbarvisible-property"></a><span data-ttu-id="86ab3-124">IMsTscAx:: HorizontalScrollBarVisible (propiedad)</span><span class="sxs-lookup"><span data-stu-id="86ab3-124">IMsTscAx::HorizontalScrollBarVisible property</span></span>

<span data-ttu-id="86ab3-125">Indica si el control ha mostrado una barra de desplazamiento horizontal.</span><span class="sxs-lookup"><span data-stu-id="86ab3-125">Indicates whether the control has displayed a horizontal scroll bar.</span></span>

<span data-ttu-id="86ab3-126">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="86ab3-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="86ab3-127">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86ab3-127">Syntax</span></span>


```C++
HRESULT get_HorizontalScrollBarVisible(
  [out] BOOL *pfHScrollVisible
);
```



## <a name="property-value"></a><span data-ttu-id="86ab3-128">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="86ab3-128">Property value</span></span>

<span data-ttu-id="86ab3-129">El valor de este parámetro es **true** si la barra de desplazamiento horizontal está visible y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="86ab3-129">The value of this parameter is **TRUE** if the horizontal scroll bar is visible, and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="86ab3-130">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="86ab3-130">Error codes</span></span>

<span data-ttu-id="86ab3-131">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="86ab3-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="86ab3-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86ab3-132">Remarks</span></span>

<span data-ttu-id="86ab3-133">El control muestra automáticamente una barra de desplazamiento horizontal si el ancho del control es menor que el ancho del escritorio.</span><span class="sxs-lookup"><span data-stu-id="86ab3-133">The control automatically displays a horizontal scroll bar if the width of the control is less than the desktop width.</span></span>

<span data-ttu-id="86ab3-134">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="86ab3-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="86ab3-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86ab3-135">Requirements</span></span>



| <span data-ttu-id="86ab3-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="86ab3-136">Requirement</span></span> | <span data-ttu-id="86ab3-137">Value</span><span class="sxs-lookup"><span data-stu-id="86ab3-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="86ab3-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86ab3-138">Minimum supported client</span></span><br/> | <span data-ttu-id="86ab3-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86ab3-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="86ab3-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86ab3-140">Minimum supported server</span></span><br/> | <span data-ttu-id="86ab3-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86ab3-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="86ab3-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="86ab3-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="86ab3-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86ab3-143"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="86ab3-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="86ab3-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86ab3-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86ab3-145"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="86ab3-146">IID</span><span class="sxs-lookup"><span data-stu-id="86ab3-146">IID</span></span><br/>                      | <span data-ttu-id="86ab3-147">IID \_ IMsTscAx se define como 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="86ab3-147">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="86ab3-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="86ab3-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86ab3-149">**IMsRdpClient**</span><span class="sxs-lookup"><span data-stu-id="86ab3-149">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="86ab3-150">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="86ab3-150">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="86ab3-151">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="86ab3-151">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="86ab3-152">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="86ab3-152">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="86ab3-153">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="86ab3-153">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="86ab3-154">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="86ab3-154">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="86ab3-155">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="86ab3-155">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="86ab3-156">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="86ab3-156">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="86ab3-157">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="86ab3-157">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="86ab3-158">**IMsTscAx**</span><span class="sxs-lookup"><span data-stu-id="86ab3-158">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> <dt>

[<span data-ttu-id="86ab3-159">**VerticalScrollBarVisible**</span><span class="sxs-lookup"><span data-stu-id="86ab3-159">**VerticalScrollBarVisible**</span></span>](imstscax-verticalscrollbarvisible.md)
</dt> </dl>

 

 





