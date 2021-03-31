---
title: Propiedad RedirectDynamicDevices de IMsRdpClientNonScriptable3
description: Especifica o recupera si los dispositivos Plug and Play conectados dinámicamente (PnP) que se enumeran mientras están en una sesión están disponibles para la redirección.
ms.assetid: 8cc5d6a4-108b-4505-8937-f6e790a5c2ba
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RedirectDynamicDevices
- Propiedad RedirectDynamicDevices Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad RedirectDynamicDevices
- Propiedad RedirectDynamicDevices Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad RedirectDynamicDevices
- Propiedad RedirectDynamicDevices Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad RedirectDynamicDevices
- Servicios de Escritorio remoto de la propiedad RedirectDynamicDevices, objeto MsRdpClient5
- Servicios de Escritorio remoto de objeto MsRdpClient5, propiedad RedirectDynamicDevices
- Servicios de Escritorio remoto de la propiedad RedirectDynamicDevices, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad RedirectDynamicDevices
- Servicios de Escritorio remoto de la propiedad RedirectDynamicDevices, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad RedirectDynamicDevices
- Servicios de Escritorio remoto de la propiedad RedirectDynamicDevices, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad RedirectDynamicDevices
- Servicios de Escritorio remoto de la propiedad RedirectDynamicDevices, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad RedirectDynamicDevices
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.RedirectDynamicDevices
- IMsRdpClientNonScriptable3.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable3.put_RedirectDynamicDevices
- IMsRdpClientNonScriptable4.RedirectDynamicDevices
- IMsRdpClientNonScriptable4.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable4.put_RedirectDynamicDevices
- IMsRdpClientNonScriptable5.RedirectDynamicDevices
- IMsRdpClientNonScriptable5.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable5.put_RedirectDynamicDevices
- MsRdpClient5.RedirectDynamicDevices
- MsRdpClient6.RedirectDynamicDevices
- MsRdpClient7.RedirectDynamicDevices
- MsRdpClient8.RedirectDynamicDevices
- MsRdpClient9.RedirectDynamicDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75224d26034e606a7a46943a02845280a092c3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801448"
---
# <a name="imsrdpclientnonscriptable3redirectdynamicdevices-property"></a><span data-ttu-id="5b8ec-120">IMsRdpClientNonScriptable3:: RedirectDynamicDevices (propiedad)</span><span class="sxs-lookup"><span data-stu-id="5b8ec-120">IMsRdpClientNonScriptable3::RedirectDynamicDevices property</span></span>

<span data-ttu-id="5b8ec-121">Especifica o recupera si los dispositivos Plug and Play conectados dinámicamente (PnP) que se enumeran mientras están en una sesión están disponibles para la redirección.</span><span class="sxs-lookup"><span data-stu-id="5b8ec-121">Specifies or retrieves whether dynamically attached Plug and Play (PnP) devices that are enumerated while in a session are available for redirection.</span></span>

<span data-ttu-id="5b8ec-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5b8ec-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b8ec-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b8ec-123">Syntax</span></span>


```C++
HRESULT put_RedirectDynamicDevices(
  [in]  VARIANT_BOOL fRedirectDynamicDevices
);

HRESULT get_RedirectDynamicDevices(
  [out] VARIANT_BOOL *pfRedirectDynamicDevices
);
```



## <a name="property-value"></a><span data-ttu-id="5b8ec-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5b8ec-124">Property value</span></span>

<span data-ttu-id="5b8ec-125">Especifica si los dispositivos PnP conectados dinámicamente que se enumeran mientras están en una sesión están disponibles para la redirección.</span><span class="sxs-lookup"><span data-stu-id="5b8ec-125">Specifies whether dynamically attached PnP devices that are enumerated while in a session are available for redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b8ec-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b8ec-126">Requirements</span></span>



| <span data-ttu-id="5b8ec-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b8ec-127">Requirement</span></span> | <span data-ttu-id="5b8ec-128">Value</span><span class="sxs-lookup"><span data-stu-id="5b8ec-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b8ec-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b8ec-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5b8ec-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b8ec-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="5b8ec-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5b8ec-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5b8ec-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b8ec-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="5b8ec-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5b8ec-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="5b8ec-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b8ec-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="5b8ec-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5b8ec-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b8ec-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b8ec-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="5b8ec-137">IID</span><span class="sxs-lookup"><span data-stu-id="5b8ec-137">IID</span></span><br/>                      | <span data-ttu-id="5b8ec-138">IID \_ IMsRdpClientNonScriptable3 se define como b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="5b8ec-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5b8ec-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b8ec-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b8ec-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="5b8ec-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="5b8ec-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="5b8ec-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="5b8ec-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="5b8ec-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





