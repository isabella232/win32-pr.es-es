---
title: Propiedad ConnectionBarShowRestoreButton de IMsRdpClientAdvancedSettings3
description: Especifica si se va a mostrar el botón restaurar en la barra de conexión.
ms.assetid: a56c3c05-d253-404a-bf49-9c1d804802e0
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad ConnectionBarShowRestoreButton
- Propiedad ConnectionBarShowRestoreButton Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad ConnectionBarShowRestoreButton
- Propiedad ConnectionBarShowRestoreButton Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad ConnectionBarShowRestoreButton
- Propiedad ConnectionBarShowRestoreButton Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad ConnectionBarShowRestoreButton
- Propiedad ConnectionBarShowRestoreButton Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad ConnectionBarShowRestoreButton
- Propiedad ConnectionBarShowRestoreButton Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad ConnectionBarShowRestoreButton
- Propiedad ConnectionBarShowRestoreButton Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad ConnectionBarShowRestoreButton
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings3.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings3.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowRestoreButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae83ecde31461eff9c553782b8bfa3ae760fb54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422003"
---
# <a name="imsrdpclientadvancedsettings3connectionbarshowrestorebutton-property"></a><span data-ttu-id="653c6-116">IMsRdpClientAdvancedSettings3:: ConnectionBarShowRestoreButton (propiedad)</span><span class="sxs-lookup"><span data-stu-id="653c6-116">IMsRdpClientAdvancedSettings3::ConnectionBarShowRestoreButton property</span></span>

<span data-ttu-id="653c6-117">Especifica si se va a mostrar el botón **restaurar** en la barra de conexión.</span><span class="sxs-lookup"><span data-stu-id="653c6-117">Specifies whether to display the **Restore** button on the connection bar.</span></span>

<span data-ttu-id="653c6-118">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="653c6-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="653c6-119">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="653c6-119">Syntax</span></span>


```C++
HRESULT put_ConnectionBarShowRestoreButton(
  [in]  VARIANT_BOOL fShowRestore
);

HRESULT get_ConnectionBarShowRestoreButton(
  [out] VARIANT_BOOL *pfShowRestore
);
```



## <a name="property-value"></a><span data-ttu-id="653c6-120">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="653c6-120">Property value</span></span>

<span data-ttu-id="653c6-121">Establézcalo en **Variant \_ true** para mostrar el botón **restaurar** y en **Variant \_ false** para deshabilitar la visualización del botón **restaurar** .</span><span class="sxs-lookup"><span data-stu-id="653c6-121">Set to **VARIANT\_TRUE** to display the **Restore** button, and to **VARIANT\_FALSE** to disable the display of the **Restore** button.</span></span>

## <a name="error-codes"></a><span data-ttu-id="653c6-122">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="653c6-122">Error codes</span></span>

<span data-ttu-id="653c6-123">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="653c6-123">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="653c6-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="653c6-124">Remarks</span></span>

<span data-ttu-id="653c6-125">No se puede establecer esta propiedad mientras el control está conectado.</span><span class="sxs-lookup"><span data-stu-id="653c6-125">This property cannot be set while the control is connected.</span></span>

<span data-ttu-id="653c6-126">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="653c6-126">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="653c6-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="653c6-127">Requirements</span></span>



| <span data-ttu-id="653c6-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="653c6-128">Requirement</span></span> | <span data-ttu-id="653c6-129">Value</span><span class="sxs-lookup"><span data-stu-id="653c6-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="653c6-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="653c6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="653c6-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="653c6-131">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="653c6-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="653c6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="653c6-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="653c6-133">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="653c6-134">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="653c6-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="653c6-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="653c6-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="653c6-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="653c6-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="653c6-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="653c6-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="653c6-138">IID</span><span class="sxs-lookup"><span data-stu-id="653c6-138">IID</span></span><br/>                      | <span data-ttu-id="653c6-139">IID \_ IMsRdpClientAdvancedSettings3 se define como 19cd856b-c542-4c53-ACEE-f127e3be1a59</span><span class="sxs-lookup"><span data-stu-id="653c6-139">IID\_IMsRdpClientAdvancedSettings3 is defined as 19cd856b-c542-4c53-acee-f127e3be1a59</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="653c6-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="653c6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="653c6-141">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="653c6-141">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="653c6-142">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="653c6-142">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="653c6-143">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="653c6-143">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="653c6-144">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="653c6-144">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="653c6-145">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="653c6-145">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="653c6-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="653c6-146">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> </dl>

 

 





