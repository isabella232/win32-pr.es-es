---
title: Propiedad RedirectDynamicDrives de IMsRdpClientNonScriptable3
description: Especifica o recupera si las unidades de Plug and Play conectadas dinámicamente (PnP) que se enumeran mientras están en una sesión están disponibles para la redirección.
ms.assetid: 11eb19fc-9711-4293-8054-f7975dadb492
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RedirectDynamicDrives
- Propiedad RedirectDynamicDrives Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad RedirectDynamicDrives
- Propiedad RedirectDynamicDrives Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad RedirectDynamicDrives
- Propiedad RedirectDynamicDrives Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad RedirectDynamicDrives
- Servicios de Escritorio remoto de la propiedad RedirectDynamicDrives, objeto MsRdpClient5
- Servicios de Escritorio remoto de objeto MsRdpClient5, propiedad RedirectDynamicDrives
- Servicios de Escritorio remoto de la propiedad RedirectDynamicDrives, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad RedirectDynamicDrives
- Servicios de Escritorio remoto de la propiedad RedirectDynamicDrives, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad RedirectDynamicDrives
- Servicios de Escritorio remoto de la propiedad RedirectDynamicDrives, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad RedirectDynamicDrives
- Servicios de Escritorio remoto de la propiedad RedirectDynamicDrives, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad RedirectDynamicDrives
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.RedirectDynamicDrives
- IMsRdpClientNonScriptable3.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable3.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.RedirectDynamicDrives
- IMsRdpClientNonScriptable4.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.RedirectDynamicDrives
- IMsRdpClientNonScriptable5.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.put_RedirectDynamicDrives
- MsRdpClient5.RedirectDynamicDrives
- MsRdpClient6.RedirectDynamicDrives
- MsRdpClient7.RedirectDynamicDrives
- MsRdpClient8.RedirectDynamicDrives
- MsRdpClient9.RedirectDynamicDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b19c0e6e20f7f73481f6f2ecbc50ab0eda512ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803884"
---
# <a name="imsrdpclientnonscriptable3redirectdynamicdrives-property"></a><span data-ttu-id="5ce22-120">IMsRdpClientNonScriptable3:: RedirectDynamicDrives (propiedad)</span><span class="sxs-lookup"><span data-stu-id="5ce22-120">IMsRdpClientNonScriptable3::RedirectDynamicDrives property</span></span>

<span data-ttu-id="5ce22-121">Especifica o recupera si las unidades de Plug and Play conectadas dinámicamente (PnP) que se enumeran mientras están en una sesión están disponibles para la redirección.</span><span class="sxs-lookup"><span data-stu-id="5ce22-121">Specifies or retrieves whether dynamically attached Plug and Play (PnP) drives that are enumerated while in a session are available for redirection.</span></span>

<span data-ttu-id="5ce22-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5ce22-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ce22-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ce22-123">Syntax</span></span>


```C++
HRESULT put_RedirectDynamicDrives(
  [in]  VARIANT_BOOL fRedirectDynamicDrives
);

HRESULT get_RedirectDynamicDrives(
  [out] VARIANT_BOOL *pfRedirectDynamicDrives
);
```



## <a name="property-value"></a><span data-ttu-id="5ce22-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5ce22-124">Property value</span></span>

<span data-ttu-id="5ce22-125">Especifica si las unidades PnP conectadas dinámicamente que se enumeran mientras están en una sesión están disponibles para la redirección.</span><span class="sxs-lookup"><span data-stu-id="5ce22-125">Specifies whether dynamically attached PnP drives that are enumerated while in a session are available for redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ce22-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ce22-126">Requirements</span></span>



| <span data-ttu-id="5ce22-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ce22-127">Requirement</span></span> | <span data-ttu-id="5ce22-128">Value</span><span class="sxs-lookup"><span data-stu-id="5ce22-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ce22-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ce22-129">Minimum supported client</span></span><br/> | <span data-ttu-id="5ce22-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ce22-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="5ce22-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ce22-131">Minimum supported server</span></span><br/> | <span data-ttu-id="5ce22-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ce22-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="5ce22-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5ce22-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="5ce22-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ce22-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="5ce22-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5ce22-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ce22-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ce22-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="5ce22-137">IID</span><span class="sxs-lookup"><span data-stu-id="5ce22-137">IID</span></span><br/>                      | <span data-ttu-id="5ce22-138">IID \_ IMsRdpClientNonScriptable3 se define como b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="5ce22-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5ce22-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ce22-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ce22-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="5ce22-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="5ce22-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="5ce22-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="5ce22-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="5ce22-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





