---
title: Propiedad IMsRdpClientNonScriptable3 PromptForCredentials (Wuapi. h)
description: Especifica o recupera si el cuadro de diálogo solicitar credenciales está habilitado para la conexión.
ms.assetid: 252ec5bd-bd52-40d4-ae48-b2c00c0720c0
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad PromptForCredentials
- Propiedad PromptForCredentials Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad PromptForCredentials
- Propiedad PromptForCredentials Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad PromptForCredentials
- Propiedad PromptForCredentials Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad PromptForCredentials
- Servicios de Escritorio remoto de la propiedad PromptForCredentials, objeto MsRdpClient5
- Servicios de Escritorio remoto de objeto MsRdpClient5, propiedad PromptForCredentials
- Servicios de Escritorio remoto de la propiedad PromptForCredentials, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad PromptForCredentials
- Servicios de Escritorio remoto de la propiedad PromptForCredentials, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad PromptForCredentials
- Servicios de Escritorio remoto de la propiedad PromptForCredentials, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad PromptForCredentials
- Servicios de Escritorio remoto de la propiedad PromptForCredentials, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad PromptForCredentials
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.PromptForCredentials
- IMsRdpClientNonScriptable3.get_PromptForCredentials
- IMsRdpClientNonScriptable3.put_PromptForCredentials
- IMsRdpClientNonScriptable4.PromptForCredentials
- IMsRdpClientNonScriptable4.get_PromptForCredentials
- IMsRdpClientNonScriptable4.put_PromptForCredentials
- IMsRdpClientNonScriptable5.PromptForCredentials
- IMsRdpClientNonScriptable5.get_PromptForCredentials
- IMsRdpClientNonScriptable5.put_PromptForCredentials
- MsRdpClient5.PromptForCredentials
- MsRdpClient6.PromptForCredentials
- MsRdpClient7.PromptForCredentials
- MsRdpClient8.PromptForCredentials
- MsRdpClient9.PromptForCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62f913937c9a2ff01d4aabeaba48dcbdc8ddb21d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359672"
---
# <a name="imsrdpclientnonscriptable3promptforcredentials-property"></a><span data-ttu-id="ddf0e-120">IMsRdpClientNonScriptable3::P propiedad romptForCredentials</span><span class="sxs-lookup"><span data-stu-id="ddf0e-120">IMsRdpClientNonScriptable3::PromptForCredentials property</span></span>

<span data-ttu-id="ddf0e-121">Especifica o recupera si el cuadro de diálogo solicitar credenciales está habilitado para la conexión.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-121">Specifies or retrieves whether the prompt for credentials dialog is enabled for the connection.</span></span>

<span data-ttu-id="ddf0e-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddf0e-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ddf0e-123">Syntax</span></span>


```C++
HRESULT put_PromptForCredentials(
  [in]  VARIANT_BOOL fPrompt
);

HRESULT get_PromptForCredentials(
  [out] VARIANT_BOOL *pfPrompt
);
```



## <a name="property-value"></a><span data-ttu-id="ddf0e-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ddf0e-124">Property value</span></span>

<span data-ttu-id="ddf0e-125">Especifica si el cuadro de diálogo solicitar credenciales está habilitado para la conexión.</span><span class="sxs-lookup"><span data-stu-id="ddf0e-125">Specifies whether the prompt for credentials dialog is enabled for the connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ddf0e-126">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="ddf0e-126">Error codes</span></span>

## <a name="requirements"></a><span data-ttu-id="ddf0e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddf0e-127">Requirements</span></span>



| <span data-ttu-id="ddf0e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddf0e-128">Requirement</span></span> | <span data-ttu-id="ddf0e-129">Value</span><span class="sxs-lookup"><span data-stu-id="ddf0e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddf0e-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddf0e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ddf0e-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ddf0e-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="ddf0e-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddf0e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ddf0e-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ddf0e-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="ddf0e-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ddf0e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ddf0e-135"><dt>Wuapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddf0e-135"><dt>Wuapi.h</dt></span></span> </dl>            |
| <span data-ttu-id="ddf0e-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ddf0e-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="ddf0e-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddf0e-137"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="ddf0e-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ddf0e-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddf0e-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddf0e-139"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="ddf0e-140">IID</span><span class="sxs-lookup"><span data-stu-id="ddf0e-140">IID</span></span><br/>                      | <span data-ttu-id="ddf0e-141">IID \_ IMsRdpClientNonScriptable3 se define como b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="ddf0e-141">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ddf0e-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddf0e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddf0e-143">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="ddf0e-143">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="ddf0e-144">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="ddf0e-144">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="ddf0e-145">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="ddf0e-145">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





