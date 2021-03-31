---
title: Propiedad MsRdpClientShell de IMsRdpClient5
description: Recupera la interfaz de configuración de cliente con scripts IMsRdpClientShell.
ms.assetid: cc56cec4-779d-4b51-8e94-ae0dd9bae997
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad MsRdpClientShell
- Propiedad MsRdpClientShell Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad MsRdpClientShell
- Propiedad MsRdpClientShell Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad MsRdpClientShell
- Propiedad MsRdpClientShell Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad MsRdpClientShell
- Propiedad MsRdpClientShell Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad MsRdpClientShell
- Propiedad MsRdpClientShell Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad MsRdpClientShell
- Propiedad MsRdpClientShell Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Servicios de Escritorio remoto de la interfaz IMsRdpClient10, propiedad MsRdpClientShell
topic_type:
- apiref
api_name:
- IMsRdpClient5.MsRdpClientShell
- IMsRdpClient5.get_MsRdpClientShell
- IMsRdpClient6.MsRdpClientShell
- IMsRdpClient6.get_MsRdpClientShell
- IMsRdpClient7.MsRdpClientShell
- IMsRdpClient7.get_MsRdpClientShell
- IMsRdpClient8.MsRdpClientShell
- IMsRdpClient8.get_MsRdpClientShell
- IMsRdpClient9.MsRdpClientShell
- IMsRdpClient9.get_MsRdpClientShell
- IMsRdpClient10.MsRdpClientShell
- IMsRdpClient10.get_MsRdpClientShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46129dc4736b50e8b6a650cc7a59f9b238da56e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151118"
---
# <a name="imsrdpclient5msrdpclientshell-property"></a><span data-ttu-id="0b703-116">IMsRdpClient5:: MsRdpClientShell (propiedad)</span><span class="sxs-lookup"><span data-stu-id="0b703-116">IMsRdpClient5::MsRdpClientShell property</span></span>

<span data-ttu-id="0b703-117">Recupera la interfaz de configuración de cliente con scripts [**IMsRdpClientShell**](imsrdpclientshell.md).</span><span class="sxs-lookup"><span data-stu-id="0b703-117">Retrieves the scriptable client setting interface [**IMsRdpClientShell**](imsrdpclientshell.md).</span></span>

<span data-ttu-id="0b703-118">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0b703-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b703-119">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b703-119">Syntax</span></span>


```C++
HRESULT get_MsRdpClientShell(
  [out] IMsRdpClientShell **ppLauncher
);
```



## <a name="property-value"></a><span data-ttu-id="0b703-120">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="0b703-120">Property value</span></span>

<span data-ttu-id="0b703-121">Puntero a la interfaz [**IMsRdpClientShell**](imsrdpclientshell.md) .</span><span class="sxs-lookup"><span data-stu-id="0b703-121">An [**IMsRdpClientShell**](imsrdpclientshell.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b703-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b703-122">Requirements</span></span>



| <span data-ttu-id="0b703-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b703-123">Requirement</span></span> | <span data-ttu-id="0b703-124">Value</span><span class="sxs-lookup"><span data-stu-id="0b703-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b703-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b703-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0b703-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b703-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0b703-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b703-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0b703-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b703-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0b703-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="0b703-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="0b703-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b703-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0b703-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0b703-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b703-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b703-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="0b703-133">IID</span><span class="sxs-lookup"><span data-stu-id="0b703-133">IID</span></span><br/>                      | <span data-ttu-id="0b703-134">IID \_ IMsRdpClient5 se define como 4eb5335b-6429-477d-B922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="0b703-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0b703-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b703-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b703-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="0b703-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="0b703-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="0b703-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="0b703-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="0b703-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="0b703-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="0b703-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="0b703-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="0b703-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="0b703-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="0b703-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





