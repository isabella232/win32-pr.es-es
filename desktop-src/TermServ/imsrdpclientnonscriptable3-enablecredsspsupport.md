---
title: Propiedad EnableCredSspSupport de IMsRdpClientNonScriptable3
description: Especifica o recupera si el proveedor de servicios de seguridad de credenciales (CredSSP) está habilitado para esta conexión.
ms.assetid: 770da50b-2a93-4274-9b6f-c24c13f08549
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad EnableCredSspSupport
- Propiedad EnableCredSspSupport Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad EnableCredSspSupport
- Propiedad EnableCredSspSupport Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad EnableCredSspSupport
- Propiedad EnableCredSspSupport Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad EnableCredSspSupport
- Servicios de Escritorio remoto de la propiedad EnableCredSspSupport, objeto MsRdpClient5
- Servicios de Escritorio remoto de objeto MsRdpClient5, propiedad EnableCredSspSupport
- Servicios de Escritorio remoto de la propiedad EnableCredSspSupport, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad EnableCredSspSupport
- Servicios de Escritorio remoto de la propiedad EnableCredSspSupport, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad EnableCredSspSupport
- Servicios de Escritorio remoto de la propiedad EnableCredSspSupport, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad EnableCredSspSupport
- Servicios de Escritorio remoto de la propiedad EnableCredSspSupport, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad EnableCredSspSupport
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.EnableCredSspSupport
- IMsRdpClientNonScriptable3.get_EnableCredSspSupport
- IMsRdpClientNonScriptable3.put_EnableCredSspSupport
- IMsRdpClientNonScriptable4.EnableCredSspSupport
- IMsRdpClientNonScriptable4.get_EnableCredSspSupport
- IMsRdpClientNonScriptable4.put_EnableCredSspSupport
- IMsRdpClientNonScriptable5.EnableCredSspSupport
- IMsRdpClientNonScriptable5.get_EnableCredSspSupport
- IMsRdpClientNonScriptable5.put_EnableCredSspSupport
- MsRdpClient5.EnableCredSspSupport
- MsRdpClient6.EnableCredSspSupport
- MsRdpClient7.EnableCredSspSupport
- MsRdpClient8.EnableCredSspSupport
- MsRdpClient9.EnableCredSspSupport
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2330b800d15f95a7b59a01735de971dd4b212d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150220"
---
# <a name="imsrdpclientnonscriptable3enablecredsspsupport-property"></a><span data-ttu-id="2f022-120">IMsRdpClientNonScriptable3:: EnableCredSspSupport (propiedad)</span><span class="sxs-lookup"><span data-stu-id="2f022-120">IMsRdpClientNonScriptable3::EnableCredSspSupport property</span></span>

<span data-ttu-id="2f022-121">Especifica o recupera si el proveedor de servicios de seguridad de credenciales (CredSSP) está habilitado para esta conexión.</span><span class="sxs-lookup"><span data-stu-id="2f022-121">Specifies or retrieves whether the Credential Security Service Provider (CredSSP) is enabled for this connection.</span></span>

<span data-ttu-id="2f022-122">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="2f022-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f022-123">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f022-123">Syntax</span></span>


```C++
HRESULT put_EnableCredSspSupport(
  [in]  VARIANT_BOOL fEnableSupport
);

HRESULT get_EnableCredSspSupport(
  [out] VARIANT_BOOL *pfEnableSupport
);
```



## <a name="property-value"></a><span data-ttu-id="2f022-124">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2f022-124">Property value</span></span>

<span data-ttu-id="2f022-125">Especifica si CredSSP está habilitado para esta conexión.</span><span class="sxs-lookup"><span data-stu-id="2f022-125">Specifies whether CredSSP is enabled for this connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f022-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f022-126">Requirements</span></span>



| <span data-ttu-id="2f022-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f022-127">Requirement</span></span> | <span data-ttu-id="2f022-128">Value</span><span class="sxs-lookup"><span data-stu-id="2f022-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f022-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f022-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2f022-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f022-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="2f022-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f022-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2f022-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f022-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="2f022-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2f022-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="2f022-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f022-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="2f022-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2f022-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f022-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f022-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="2f022-137">IID</span><span class="sxs-lookup"><span data-stu-id="2f022-137">IID</span></span><br/>                      | <span data-ttu-id="2f022-138">IID \_ IMsRdpClientNonScriptable3 se define como b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="2f022-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2f022-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f022-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f022-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="2f022-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="2f022-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="2f022-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="2f022-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="2f022-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





