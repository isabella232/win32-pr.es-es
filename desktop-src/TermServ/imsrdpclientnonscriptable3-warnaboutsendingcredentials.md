---
title: Propiedad WarnAboutSendingCredentials de IMsRdpClientNonScriptable3
description: Especifica o recupera si el cuadro de diálogo Advertencia de seguridad debe incluir una advertencia sobre el envío de credenciales al servidor remoto antes de iniciar una sesión.
ms.assetid: b97baef5-4a51-4e5c-bd53-10cff175533c
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad WarnAboutSendingCredentials
- Propiedad WarnAboutSendingCredentials Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad WarnAboutSendingCredentials
- Propiedad WarnAboutSendingCredentials Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad WarnAboutSendingCredentials
- Propiedad WarnAboutSendingCredentials Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad WarnAboutSendingCredentials
- Servicios de Escritorio remoto de la propiedad WarnAboutSendingCredentials, objeto MsRdpClient5
- Servicios de Escritorio remoto de objeto MsRdpClient5, propiedad WarnAboutSendingCredentials
- Servicios de Escritorio remoto de la propiedad WarnAboutSendingCredentials, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad WarnAboutSendingCredentials
- Servicios de Escritorio remoto de la propiedad WarnAboutSendingCredentials, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad WarnAboutSendingCredentials
- Servicios de Escritorio remoto de la propiedad WarnAboutSendingCredentials, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad WarnAboutSendingCredentials
- Servicios de Escritorio remoto de la propiedad WarnAboutSendingCredentials, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad WarnAboutSendingCredentials
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable3.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable3.put_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.put_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.put_WarnAboutSendingCredentials
- MsRdpClient5.WarnAboutSendingCredentials
- MsRdpClient6.WarnAboutSendingCredentials
- MsRdpClient7.WarnAboutSendingCredentials
- MsRdpClient8.WarnAboutSendingCredentials
- MsRdpClient9.WarnAboutSendingCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29d9d2fcfe158f5a0bb6812002bfcc160f1c9009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685926"
---
# <a name="imsrdpclientnonscriptable3warnaboutsendingcredentials-property"></a><span data-ttu-id="7adc5-120">IMsRdpClientNonScriptable3:: WarnAboutSendingCredentials (propiedad)</span><span class="sxs-lookup"><span data-stu-id="7adc5-120">IMsRdpClientNonScriptable3::WarnAboutSendingCredentials property</span></span>

<span data-ttu-id="7adc5-121">Especifica o recupera si el cuadro de diálogo Advertencia de seguridad debe incluir una advertencia sobre el envío de credenciales al servidor remoto antes de iniciar una sesión.</span><span class="sxs-lookup"><span data-stu-id="7adc5-121">Specifies or retrieves whether the security warning dialog box should include a warning about sending credentials to the remote server before starting a session.</span></span>

<span data-ttu-id="7adc5-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="7adc5-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7adc5-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7adc5-123">Syntax</span></span>


```C++
HRESULT put_WarnAboutSendingCredentials(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutSendingCredentials(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a><span data-ttu-id="7adc5-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7adc5-124">Property value</span></span>

<span data-ttu-id="7adc5-125">Especifica si el cuadro de diálogo Advertencia de seguridad debe incluir una advertencia sobre el envío de credenciales al servidor remoto antes de iniciar una sesión.</span><span class="sxs-lookup"><span data-stu-id="7adc5-125">Specifies whether the security warning dialog box should include a warning about sending credentials to the remote server before starting a session.</span></span>

## <a name="requirements"></a><span data-ttu-id="7adc5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7adc5-126">Requirements</span></span>



| <span data-ttu-id="7adc5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="7adc5-127">Requirement</span></span> | <span data-ttu-id="7adc5-128">Value</span><span class="sxs-lookup"><span data-stu-id="7adc5-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7adc5-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7adc5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7adc5-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7adc5-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="7adc5-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7adc5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7adc5-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7adc5-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="7adc5-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7adc5-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="7adc5-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7adc5-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="7adc5-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7adc5-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7adc5-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7adc5-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="7adc5-137">IID</span><span class="sxs-lookup"><span data-stu-id="7adc5-137">IID</span></span><br/>                      | <span data-ttu-id="7adc5-138">IID \_ IMsRdpClientNonScriptable3 se define como b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="7adc5-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7adc5-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="7adc5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7adc5-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="7adc5-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="7adc5-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="7adc5-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="7adc5-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="7adc5-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





