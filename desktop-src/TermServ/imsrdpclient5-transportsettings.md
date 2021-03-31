---
title: Propiedad TransportSettings de IMsRdpClient5
description: Recupera lo que se pasó a través de un script a la interfaz IMsRdpClientTransportSettings.
ms.assetid: 38f5a735-55c7-425a-835b-22f6e0900d57
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad TransportSettings
- Propiedad TransportSettings Servicios de Escritorio remoto, interfaz IMsRdpClient5
- Servicios de Escritorio remoto de la interfaz IMsRdpClient5, propiedad TransportSettings
- Propiedad TransportSettings Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad TransportSettings
- Propiedad TransportSettings Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad TransportSettings
- Propiedad TransportSettings Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad TransportSettings
- Propiedad TransportSettings Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad TransportSettings
- Propiedad TransportSettings Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Servicios de Escritorio remoto de la interfaz IMsRdpClient10, propiedad TransportSettings
topic_type:
- apiref
api_name:
- IMsRdpClient5.TransportSettings
- IMsRdpClient5.get_TransportSettings
- IMsRdpClient6.TransportSettings
- IMsRdpClient6.get_TransportSettings
- IMsRdpClient7.TransportSettings
- IMsRdpClient7.get_TransportSettings
- IMsRdpClient8.TransportSettings
- IMsRdpClient8.get_TransportSettings
- IMsRdpClient9.TransportSettings
- IMsRdpClient9.get_TransportSettings
- IMsRdpClient10.TransportSettings
- IMsRdpClient10.get_TransportSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 077ed94253c0ebadeed775e54c4db2ae6cbacf13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150035"
---
# <a name="imsrdpclient5transportsettings-property"></a><span data-ttu-id="35bd4-116">IMsRdpClient5:: TransportSettings (propiedad)</span><span class="sxs-lookup"><span data-stu-id="35bd4-116">IMsRdpClient5::TransportSettings property</span></span>

<span data-ttu-id="35bd4-117">Recupera lo que se pasó a través de un script a la interfaz [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="35bd4-117">Retrieves what was passed through a script to the [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) interface.</span></span>

<span data-ttu-id="35bd4-118">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="35bd4-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="35bd4-119">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35bd4-119">Syntax</span></span>


```C++
HRESULT get_TransportSettings(
  [out] IMsRdpClientTransportSettings **ppXportSet
);
```



## <a name="property-value"></a><span data-ttu-id="35bd4-120">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="35bd4-120">Property value</span></span>

<span data-ttu-id="35bd4-121">Puntero a la interfaz [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="35bd4-121">An [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="35bd4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35bd4-122">Requirements</span></span>



| <span data-ttu-id="35bd4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="35bd4-123">Requirement</span></span> | <span data-ttu-id="35bd4-124">Value</span><span class="sxs-lookup"><span data-stu-id="35bd4-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="35bd4-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35bd4-125">Minimum supported client</span></span><br/> | <span data-ttu-id="35bd4-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35bd4-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="35bd4-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35bd4-127">Minimum supported server</span></span><br/> | <span data-ttu-id="35bd4-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35bd4-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="35bd4-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="35bd4-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="35bd4-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35bd4-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="35bd4-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="35bd4-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35bd4-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35bd4-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="35bd4-133">IID</span><span class="sxs-lookup"><span data-stu-id="35bd4-133">IID</span></span><br/>                      | <span data-ttu-id="35bd4-134">IID \_ IMsRdpClient5 se define como 4eb5335b-6429-477d-B922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="35bd4-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="35bd4-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="35bd4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35bd4-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="35bd4-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="35bd4-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="35bd4-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="35bd4-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="35bd4-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="35bd4-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="35bd4-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="35bd4-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="35bd4-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="35bd4-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="35bd4-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





