---
title: Propiedad PromptForCredsOnClient de IMsRdpClientNonScriptable4
description: Especifica si el control de cliente muestra un cuadro de diálogo que solicita las credenciales.
ms.assetid: 426676be-0150-4a33-acd0-26423966f32a
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad PromptForCredsOnClient
- Propiedad PromptForCredsOnClient Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad PromptForCredsOnClient
- Propiedad PromptForCredsOnClient Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad PromptForCredsOnClient
- Servicios de Escritorio remoto de la propiedad PromptForCredsOnClient, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad PromptForCredsOnClient
- Servicios de Escritorio remoto de la propiedad PromptForCredsOnClient, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad PromptForCredsOnClient
- Servicios de Escritorio remoto de la propiedad PromptForCredsOnClient, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad PromptForCredsOnClient
- Servicios de Escritorio remoto de la propiedad PromptForCredsOnClient, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad PromptForCredsOnClient
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PromptForCredsOnClient
- IMsRdpClientNonScriptable4.get_PromptForCredsOnClient
- IMsRdpClientNonScriptable4.put_PromptForCredsOnClient
- IMsRdpClientNonScriptable5.PromptForCredsOnClient
- IMsRdpClientNonScriptable5.get_PromptForCredsOnClient
- IMsRdpClientNonScriptable5.put_PromptForCredsOnClient
- MsRdpClient6.PromptForCredsOnClient
- MsRdpClient7.PromptForCredsOnClient
- MsRdpClient8.PromptForCredsOnClient
- MsRdpClient9.PromptForCredsOnClient
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6443c503e107bb2edb164a17beedddb1bbbc88a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422431"
---
# <a name="imsrdpclientnonscriptable4promptforcredsonclient-property"></a><span data-ttu-id="c1d4e-116">IMsRdpClientNonScriptable4::P propiedad romptForCredsOnClient</span><span class="sxs-lookup"><span data-stu-id="c1d4e-116">IMsRdpClientNonScriptable4::PromptForCredsOnClient property</span></span>

<span data-ttu-id="c1d4e-117">Especifica si el control de cliente muestra un cuadro de diálogo que solicita las credenciales.</span><span class="sxs-lookup"><span data-stu-id="c1d4e-117">Specifies whether the client control displays a dialog box that prompts for credentials.</span></span>

<span data-ttu-id="c1d4e-118">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="c1d4e-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1d4e-119">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c1d4e-119">Syntax</span></span>


```C++
HRESULT put_PromptForCredsOnClient(
  [in]  VARIANT_BOOL fPromptForCredsOnClient
);

HRESULT get_PromptForCredsOnClient(
  [out] VARIANT_BOOL *pfPromptForCredsOnClient
);
```



## <a name="property-value"></a><span data-ttu-id="c1d4e-120">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c1d4e-120">Property value</span></span>

<span data-ttu-id="c1d4e-121">Establece si el control de cliente muestra un cuadro de diálogo que solicita las credenciales.</span><span class="sxs-lookup"><span data-stu-id="c1d4e-121">Sets whether the client control displays a dialog box that prompts for credentials.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c1d4e-122">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="c1d4e-122">Error codes</span></span>

<span data-ttu-id="c1d4e-123">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="c1d4e-123">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1d4e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1d4e-124">Requirements</span></span>



| <span data-ttu-id="c1d4e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1d4e-125">Requirement</span></span> | <span data-ttu-id="c1d4e-126">Value</span><span class="sxs-lookup"><span data-stu-id="c1d4e-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1d4e-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1d4e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c1d4e-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c1d4e-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="c1d4e-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c1d4e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c1d4e-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c1d4e-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="c1d4e-131">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c1d4e-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="c1d4e-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1d4e-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="c1d4e-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c1d4e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1d4e-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c1d4e-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="c1d4e-135">IID</span><span class="sxs-lookup"><span data-stu-id="c1d4e-135">IID</span></span><br/>                      | <span data-ttu-id="c1d4e-136">IMsRdpClientNonScriptable4 se define como f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="c1d4e-136">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c1d4e-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="c1d4e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1d4e-138">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="c1d4e-138">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="c1d4e-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="c1d4e-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





