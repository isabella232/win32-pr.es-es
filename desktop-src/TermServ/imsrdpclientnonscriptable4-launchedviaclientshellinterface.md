---
title: Propiedad LaunchedViaClientShellInterface de IMsRdpClientNonScriptable4
description: Especifica si el usuario inició el control de cliente mediante la interfaz de acceso web de Escritorio remoto (acceso web de escritorio remoto).
ms.assetid: bf72c375-0eec-49c7-9f9a-c7545a95bdce
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad LaunchedViaClientShellInterface
- Propiedad LaunchedViaClientShellInterface Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad LaunchedViaClientShellInterface
- Propiedad LaunchedViaClientShellInterface Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad LaunchedViaClientShellInterface
- Servicios de Escritorio remoto de la propiedad LaunchedViaClientShellInterface, objeto MsRdpClient5
- Servicios de Escritorio remoto de objeto MsRdpClient5, propiedad LaunchedViaClientShellInterface
- Servicios de Escritorio remoto de la propiedad LaunchedViaClientShellInterface, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad LaunchedViaClientShellInterface
- Servicios de Escritorio remoto de la propiedad LaunchedViaClientShellInterface, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad LaunchedViaClientShellInterface
- Servicios de Escritorio remoto de la propiedad LaunchedViaClientShellInterface, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad LaunchedViaClientShellInterface
- Servicios de Escritorio remoto de la propiedad LaunchedViaClientShellInterface, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad LaunchedViaClientShellInterface
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable4.get_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable4.put_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.get_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.put_LaunchedViaClientShellInterface
- MsRdpClient5.LaunchedViaClientShellInterface
- MsRdpClient6.LaunchedViaClientShellInterface
- MsRdpClient7.LaunchedViaClientShellInterface
- MsRdpClient8.LaunchedViaClientShellInterface
- MsRdpClient9.LaunchedViaClientShellInterface
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d5854a4e75be455035fd9a123418bd486932379
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996596"
---
# <a name="imsrdpclientnonscriptable4launchedviaclientshellinterface-property"></a><span data-ttu-id="046b4-118">IMsRdpClientNonScriptable4:: LaunchedViaClientShellInterface (propiedad)</span><span class="sxs-lookup"><span data-stu-id="046b4-118">IMsRdpClientNonScriptable4::LaunchedViaClientShellInterface property</span></span>

<span data-ttu-id="046b4-119">Especifica si el usuario inició el control de cliente mediante la interfaz de acceso web de Escritorio remoto (acceso web de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="046b4-119">Specifies whether the user launched the client control by using the Remote Desktop Web Access (RD Web Access) interface.</span></span>

<span data-ttu-id="046b4-120">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="046b4-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="046b4-121">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="046b4-121">Syntax</span></span>


```C++
HRESULT put_LaunchedViaClientShellInterface(
  [in]  VARIANT_BOOL fLaunchedViaClientShellInterface
);

HRESULT get_LaunchedViaClientShellInterface(
  [out]  VARIANT_BOOL *pfLaunchedViaClientShellInterface
);
```



## <a name="property-value"></a><span data-ttu-id="046b4-122">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="046b4-122">Property value</span></span>

<span data-ttu-id="046b4-123">Establece la propiedad **LaunchedViaClientShellInterface** .</span><span class="sxs-lookup"><span data-stu-id="046b4-123">Sets the **LaunchedViaClientShellInterface** property.</span></span>

## <a name="error-codes"></a><span data-ttu-id="046b4-124">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="046b4-124">Error codes</span></span>

<span data-ttu-id="046b4-125">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="046b4-125">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="046b4-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="046b4-126">Requirements</span></span>



| <span data-ttu-id="046b4-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="046b4-127">Requirement</span></span> | <span data-ttu-id="046b4-128">Value</span><span class="sxs-lookup"><span data-stu-id="046b4-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="046b4-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="046b4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="046b4-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="046b4-130">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="046b4-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="046b4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="046b4-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="046b4-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="046b4-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="046b4-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="046b4-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="046b4-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="046b4-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="046b4-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="046b4-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="046b4-136"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="046b4-137">IID</span><span class="sxs-lookup"><span data-stu-id="046b4-137">IID</span></span><br/>                      | <span data-ttu-id="046b4-138">IMsRdpClientNonScriptable4 se define como f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="046b4-138">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="046b4-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="046b4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="046b4-140">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="046b4-140">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="046b4-141">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="046b4-141">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





