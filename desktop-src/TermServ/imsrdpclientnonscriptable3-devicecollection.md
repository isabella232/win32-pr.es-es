---
title: Propiedad recopilación de IMsRdpClientNonScriptable3
description: Recupera la colección de objetos de dispositivo Plug and Play (PnP) que se van a redirigir.
ms.assetid: dd5fe4c7-58bf-4e7a-b066-59278419ea6f
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad recopilación
- Propiedad recopilación Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad recopilación
- Propiedad recopilación Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad recopilación
- Propiedad recopilación Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad recopilación
- Servicios de Escritorio remoto de la propiedad recopilación, objeto MsRdpClient5
- Servicios de Escritorio remoto de objeto MsRdpClient5, propiedad recopilación
- Servicios de Escritorio remoto de la propiedad recopilación, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad recopilación
- Servicios de Escritorio remoto de la propiedad recopilación, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad recopilación
- Servicios de Escritorio remoto de la propiedad recopilación, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad recopilación
- Servicios de Escritorio remoto de la propiedad recopilación, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad recopilación
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.DeviceCollection
- IMsRdpClientNonScriptable3.get_DeviceCollection
- IMsRdpClientNonScriptable4.DeviceCollection
- IMsRdpClientNonScriptable4.get_DeviceCollection
- IMsRdpClientNonScriptable5.DeviceCollection
- IMsRdpClientNonScriptable5.get_DeviceCollection
- MsRdpClient5.DeviceCollection
- MsRdpClient6.DeviceCollection
- MsRdpClient7.DeviceCollection
- MsRdpClient8.DeviceCollection
- MsRdpClient9.DeviceCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a545d2f4aaae2af68c14dd6531a2c57cf73711dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422073"
---
# <a name="imsrdpclientnonscriptable3devicecollection-property"></a><span data-ttu-id="75bd4-120">IMsRdpClientNonScriptable3::D propiedad eviceCollection</span><span class="sxs-lookup"><span data-stu-id="75bd4-120">IMsRdpClientNonScriptable3::DeviceCollection property</span></span>

<span data-ttu-id="75bd4-121">Recupera la colección de objetos de dispositivo Plug and Play (PnP) que se van a redirigir.</span><span class="sxs-lookup"><span data-stu-id="75bd4-121">Retrieves the collection of Plug and Play (PnP) device objects to be redirected.</span></span>

<span data-ttu-id="75bd4-122">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="75bd4-122">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="75bd4-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75bd4-123">Syntax</span></span>


```C++
HRESULT get_DeviceCollection(
  [out] IMSRdpDeviceCollection **ppDeviceCollection
);
```



## <a name="property-value"></a><span data-ttu-id="75bd4-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="75bd4-124">Property value</span></span>

<span data-ttu-id="75bd4-125">Recupera la colección de objetos de dispositivo PnP de tipo [**IMSRdpDevice**](imsrdpdevice.md).</span><span class="sxs-lookup"><span data-stu-id="75bd4-125">Retrieves the collection of PnP device objects of type [**IMSRdpDevice**](imsrdpdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="75bd4-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75bd4-126">Requirements</span></span>



| <span data-ttu-id="75bd4-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="75bd4-127">Requirement</span></span> | <span data-ttu-id="75bd4-128">Value</span><span class="sxs-lookup"><span data-stu-id="75bd4-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="75bd4-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75bd4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="75bd4-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75bd4-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="75bd4-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75bd4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="75bd4-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75bd4-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="75bd4-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="75bd4-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="75bd4-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75bd4-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="75bd4-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="75bd4-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75bd4-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75bd4-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="75bd4-137">IID</span><span class="sxs-lookup"><span data-stu-id="75bd4-137">IID</span></span><br/>                      | <span data-ttu-id="75bd4-138">IID \_ IMsRdpClientNonScriptable3 se define como b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="75bd4-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="75bd4-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="75bd4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75bd4-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="75bd4-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="75bd4-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="75bd4-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="75bd4-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="75bd4-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





