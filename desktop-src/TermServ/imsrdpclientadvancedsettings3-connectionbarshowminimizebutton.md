---
title: Propiedad ConnectionBarShowMinimizeButton de IMsRdpClientAdvancedSettings3
description: Especifica si se va a mostrar el botón minimizar en la barra de conexión.
ms.assetid: 3ad89f25-f1ff-4bfc-ae86-09603058c9b5
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad ConnectionBarShowMinimizeButton
- Propiedad ConnectionBarShowMinimizeButton Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad ConnectionBarShowMinimizeButton
- Propiedad ConnectionBarShowMinimizeButton Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad ConnectionBarShowMinimizeButton
- Propiedad ConnectionBarShowMinimizeButton Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad ConnectionBarShowMinimizeButton
- Propiedad ConnectionBarShowMinimizeButton Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad ConnectionBarShowMinimizeButton
- Propiedad ConnectionBarShowMinimizeButton Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad ConnectionBarShowMinimizeButton
- Propiedad ConnectionBarShowMinimizeButton Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad ConnectionBarShowMinimizeButton
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings3.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings3.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowMinimizeButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc3cb600a853e4bc2dea7c693e676f992db85f48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801159"
---
# <a name="imsrdpclientadvancedsettings3connectionbarshowminimizebutton-property"></a><span data-ttu-id="6ef05-116">IMsRdpClientAdvancedSettings3:: ConnectionBarShowMinimizeButton (propiedad)</span><span class="sxs-lookup"><span data-stu-id="6ef05-116">IMsRdpClientAdvancedSettings3::ConnectionBarShowMinimizeButton property</span></span>

<span data-ttu-id="6ef05-117">Especifica si se va a mostrar el botón **minimizar** en la barra de conexión.</span><span class="sxs-lookup"><span data-stu-id="6ef05-117">Specifies whether to display the **Minimize** button on the connection bar.</span></span>

<span data-ttu-id="6ef05-118">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="6ef05-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ef05-119">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ef05-119">Syntax</span></span>


```C++
HRESULT put_ConnectionBarShowMinimizeButton(
  [in]  VARIANT_BOOL fShowMinimize
);

HRESULT get_ConnectionBarShowMinimizeButton(
  [out] VARIANT_BOOL *pfShowMinimize
);
```



## <a name="property-value"></a><span data-ttu-id="6ef05-120">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="6ef05-120">Property value</span></span>

<span data-ttu-id="6ef05-121">Establezca este parámetro en **Variant \_ true** para mostrar el botón **minimizar** y en **Variant \_ false** para deshabilitar la visualización del botón **minimizar** .</span><span class="sxs-lookup"><span data-stu-id="6ef05-121">Set this parameter to **VARIANT\_TRUE** to display the **Minimize** button, and to **VARIANT\_FALSE** to disable the display of the **Minimize** button.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6ef05-122">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="6ef05-122">Error codes</span></span>

<span data-ttu-id="6ef05-123">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="6ef05-123">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ef05-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ef05-124">Remarks</span></span>

<span data-ttu-id="6ef05-125">No se puede establecer esta propiedad mientras el control está conectado.</span><span class="sxs-lookup"><span data-stu-id="6ef05-125">This property cannot be set while the control is connected.</span></span>

<span data-ttu-id="6ef05-126">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6ef05-126">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ef05-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ef05-127">Requirements</span></span>



| <span data-ttu-id="6ef05-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ef05-128">Requirement</span></span> | <span data-ttu-id="6ef05-129">Value</span><span class="sxs-lookup"><span data-stu-id="6ef05-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ef05-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ef05-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6ef05-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ef05-131">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="6ef05-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ef05-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6ef05-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ef05-133">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="6ef05-134">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6ef05-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="6ef05-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ef05-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="6ef05-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6ef05-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ef05-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ef05-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="6ef05-138">IID</span><span class="sxs-lookup"><span data-stu-id="6ef05-138">IID</span></span><br/>                      | <span data-ttu-id="6ef05-139">IID \_ IMsRdpClientAdvancedSettings3 se define como 19cd856b-c542-4c53-ACEE-f127e3be1a59</span><span class="sxs-lookup"><span data-stu-id="6ef05-139">IID\_IMsRdpClientAdvancedSettings3 is defined as 19cd856b-c542-4c53-acee-f127e3be1a59</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6ef05-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ef05-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ef05-141">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="6ef05-141">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="6ef05-142">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="6ef05-142">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="6ef05-143">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="6ef05-143">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="6ef05-144">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="6ef05-144">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="6ef05-145">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="6ef05-145">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="6ef05-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="6ef05-146">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> </dl>

 

 





