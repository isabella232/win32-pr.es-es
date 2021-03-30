---
title: Propiedad RedirectPrinters de IMsRdpClientAdvancedSettings
description: Especifica si se permite la redirección de impresoras.
ms.assetid: 7d4f28a7-a99d-4d0b-ab51-832a78881900
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RedirectPrinters
- Propiedad RedirectPrinters Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad RedirectPrinters
- Propiedad RedirectPrinters Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad RedirectPrinters
- Propiedad RedirectPrinters Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad RedirectPrinters
- Propiedad RedirectPrinters Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad RedirectPrinters
- Propiedad RedirectPrinters Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad RedirectPrinters
- Propiedad RedirectPrinters Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad RedirectPrinters
- Propiedad RedirectPrinters Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad RedirectPrinters
- Propiedad RedirectPrinters Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad RedirectPrinters
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectPrinters
- IMsRdpClientAdvancedSettings.get_RedirectPrinters
- IMsRdpClientAdvancedSettings.put_RedirectPrinters
- IMsRdpClientAdvancedSettings2.RedirectPrinters
- IMsRdpClientAdvancedSettings2.get_RedirectPrinters
- IMsRdpClientAdvancedSettings2.put_RedirectPrinters
- IMsRdpClientAdvancedSettings3.RedirectPrinters
- IMsRdpClientAdvancedSettings3.get_RedirectPrinters
- IMsRdpClientAdvancedSettings3.put_RedirectPrinters
- IMsRdpClientAdvancedSettings4.RedirectPrinters
- IMsRdpClientAdvancedSettings4.get_RedirectPrinters
- IMsRdpClientAdvancedSettings4.put_RedirectPrinters
- IMsRdpClientAdvancedSettings5.RedirectPrinters
- IMsRdpClientAdvancedSettings5.get_RedirectPrinters
- IMsRdpClientAdvancedSettings5.put_RedirectPrinters
- IMsRdpClientAdvancedSettings6.RedirectPrinters
- IMsRdpClientAdvancedSettings6.get_RedirectPrinters
- IMsRdpClientAdvancedSettings6.put_RedirectPrinters
- IMsRdpClientAdvancedSettings7.RedirectPrinters
- IMsRdpClientAdvancedSettings7.get_RedirectPrinters
- IMsRdpClientAdvancedSettings7.put_RedirectPrinters
- IMsRdpClientAdvancedSettings8.RedirectPrinters
- IMsRdpClientAdvancedSettings8.get_RedirectPrinters
- IMsRdpClientAdvancedSettings8.put_RedirectPrinters
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94fecc3b6f72b8706168c75d220d78fc49340752
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801166"
---
# <a name="imsrdpclientadvancedsettingsredirectprinters-property"></a><span data-ttu-id="972c6-120">IMsRdpClientAdvancedSettings:: RedirectPrinters (propiedad)</span><span class="sxs-lookup"><span data-stu-id="972c6-120">IMsRdpClientAdvancedSettings::RedirectPrinters property</span></span>

<span data-ttu-id="972c6-121">Especifica si se permite la redirección de impresoras.</span><span class="sxs-lookup"><span data-stu-id="972c6-121">Specifies if redirection of printers is allowed.</span></span>

<span data-ttu-id="972c6-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="972c6-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="972c6-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="972c6-123">Syntax</span></span>


```C++
HRESULT put_RedirectPrinters(
  [in]  VARIANT_BOOL redirectPrinters
);

HRESULT get_RedirectPrinters(
  [out] VARIANT_BOOL *predirectPrinters
);
```



## <a name="property-value"></a><span data-ttu-id="972c6-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="972c6-124">Property value</span></span>

<span data-ttu-id="972c6-125">Establezca este parámetro en **Variant \_ true** para permitir el redireccionamiento o **Variant \_ false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="972c6-125">Set this parameter to **VARIANT\_TRUE** to allow redirection or **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="972c6-126">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="972c6-126">Error codes</span></span>

<span data-ttu-id="972c6-127">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="972c6-127">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="972c6-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="972c6-128">Remarks</span></span>

<span data-ttu-id="972c6-129">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="972c6-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="972c6-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="972c6-130">Requirements</span></span>



| <span data-ttu-id="972c6-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="972c6-131">Requirement</span></span> | <span data-ttu-id="972c6-132">Value</span><span class="sxs-lookup"><span data-stu-id="972c6-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="972c6-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="972c6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="972c6-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="972c6-134">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="972c6-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="972c6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="972c6-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="972c6-136">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="972c6-137">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="972c6-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="972c6-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="972c6-138"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="972c6-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="972c6-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="972c6-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="972c6-140"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="972c6-141">IID</span><span class="sxs-lookup"><span data-stu-id="972c6-141">IID</span></span><br/>                      | <span data-ttu-id="972c6-142">IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="972c6-142">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="972c6-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="972c6-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="972c6-144">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="972c6-144">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="972c6-145">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="972c6-145">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="972c6-146">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="972c6-146">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="972c6-147">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="972c6-147">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="972c6-148">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="972c6-148">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="972c6-149">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="972c6-149">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="972c6-150">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="972c6-150">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="972c6-151">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="972c6-151">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





