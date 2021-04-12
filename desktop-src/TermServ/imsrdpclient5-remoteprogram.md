---
title: Propiedad RemoteProgram de IMsRdpClient5
description: Recupera un objeto que admite la interfaz ITSRemoteProgram.
ms.assetid: 013f613b-af7b-4cc5-be1f-d45833806e3b
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RemoteProgram
- Propiedad RemoteProgram Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad RemoteProgram
- Propiedad RemoteProgram Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad RemoteProgram
- Propiedad RemoteProgram Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad RemoteProgram
- Propiedad RemoteProgram Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad RemoteProgram
- Propiedad RemoteProgram Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad RemoteProgram
- Propiedad RemoteProgram Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Servicios de Escritorio remoto de la interfaz IMsRdpClient10, propiedad RemoteProgram
topic_type:
- apiref
api_name:
- IMsRdpClient5.RemoteProgram
- IMsRdpClient5.get_RemoteProgram
- IMsRdpClient6.RemoteProgram
- IMsRdpClient6.get_RemoteProgram
- IMsRdpClient7.RemoteProgram
- IMsRdpClient7.get_RemoteProgram
- IMsRdpClient8.RemoteProgram
- IMsRdpClient8.get_RemoteProgram
- IMsRdpClient9.RemoteProgram
- IMsRdpClient9.get_RemoteProgram
- IMsRdpClient10.RemoteProgram
- IMsRdpClient10.get_RemoteProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 267e367af090a7fd70e9482406104fd0403d63f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489682"
---
# <a name="imsrdpclient5remoteprogram-property"></a><span data-ttu-id="d0556-116">IMsRdpClient5:: RemoteProgram (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d0556-116">IMsRdpClient5::RemoteProgram property</span></span>

<span data-ttu-id="d0556-117">Recupera un objeto que admite la interfaz [**ITSRemoteProgram**](itsremoteprogram.md) .</span><span class="sxs-lookup"><span data-stu-id="d0556-117">Retrieves an object that supports the [**ITSRemoteProgram**](itsremoteprogram.md) interface.</span></span>

<span data-ttu-id="d0556-118">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d0556-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0556-119">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0556-119">Syntax</span></span>


```C++
HRESULT get_RemoteProgram(
  [out] ITSRemoteProgram **ppRemoteProgram
);
```



## <a name="property-value"></a><span data-ttu-id="d0556-120">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d0556-120">Property value</span></span>

<span data-ttu-id="d0556-121">Puntero a la interfaz [**ITSRemoteProgram**](itsremoteprogram.md) .</span><span class="sxs-lookup"><span data-stu-id="d0556-121">An [**ITSRemoteProgram**](itsremoteprogram.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0556-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0556-122">Requirements</span></span>



| <span data-ttu-id="d0556-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0556-123">Requirement</span></span> | <span data-ttu-id="d0556-124">Value</span><span class="sxs-lookup"><span data-stu-id="d0556-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0556-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0556-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d0556-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0556-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d0556-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0556-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d0556-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0556-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d0556-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d0556-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="d0556-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0556-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d0556-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d0556-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0556-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0556-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="d0556-133">IID</span><span class="sxs-lookup"><span data-stu-id="d0556-133">IID</span></span><br/>                      | <span data-ttu-id="d0556-134">IID \_ IMsRdpClient5 se define como 4eb5335b-6429-477d-B922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="d0556-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d0556-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0556-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0556-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="d0556-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="d0556-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="d0556-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="d0556-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="d0556-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="d0556-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="d0556-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="d0556-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="d0556-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="d0556-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="d0556-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





