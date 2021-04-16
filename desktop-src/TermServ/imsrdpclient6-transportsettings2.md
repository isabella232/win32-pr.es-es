---
title: Propiedad TransportSettings2 de IMsRdpClient6
description: Recupera la interfaz IMsRdpClientTransportSettings2.
ms.assetid: 5cd3c745-b360-43fb-b780-c526ed539db0
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad TransportSettings2
- Propiedad TransportSettings2 Servicios de Escritorio remoto, interfaz IMsRdpClient6
- Servicios de Escritorio remoto de la interfaz IMsRdpClient6, propiedad TransportSettings2
- Propiedad TransportSettings2 Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad TransportSettings2
- Propiedad TransportSettings2 Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad TransportSettings2
- Propiedad TransportSettings2 Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad TransportSettings2
- Propiedad TransportSettings2 Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Servicios de Escritorio remoto de la interfaz IMsRdpClient10, propiedad TransportSettings2
topic_type:
- apiref
api_name:
- IMsRdpClient6.TransportSettings2
- IMsRdpClient6.get_TransportSettings2
- IMsRdpClient7.TransportSettings2
- IMsRdpClient7.get_TransportSettings2
- IMsRdpClient8.TransportSettings2
- IMsRdpClient8.get_TransportSettings2
- IMsRdpClient9.TransportSettings2
- IMsRdpClient9.get_TransportSettings2
- IMsRdpClient10.TransportSettings2
- IMsRdpClient10.get_TransportSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ba11975e0e065e0cfcce91eb22402153acf236
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685902"
---
# <a name="imsrdpclient6transportsettings2-property"></a><span data-ttu-id="97d51-114">IMsRdpClient6:: TransportSettings2 (propiedad)</span><span class="sxs-lookup"><span data-stu-id="97d51-114">IMsRdpClient6::TransportSettings2 property</span></span>

<span data-ttu-id="97d51-115">Recupera la interfaz [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="97d51-115">Retrieves the [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) interface.</span></span>

<span data-ttu-id="97d51-116">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="97d51-116">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="97d51-117">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="97d51-117">Syntax</span></span>


```C++
HRESULT get_TransportSettings2(
  [out] IMsRdpClientTransportSettings2 **ppXportSet2
);
```



## <a name="property-value"></a><span data-ttu-id="97d51-118">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="97d51-118">Property value</span></span>

<span data-ttu-id="97d51-119">Puntero a la interfaz [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="97d51-119">An [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="97d51-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97d51-120">Requirements</span></span>



| <span data-ttu-id="97d51-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="97d51-121">Requirement</span></span> | <span data-ttu-id="97d51-122">Value</span><span class="sxs-lookup"><span data-stu-id="97d51-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97d51-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97d51-123">Minimum supported client</span></span><br/> | <span data-ttu-id="97d51-124">Windows Vista con SP1</span><span class="sxs-lookup"><span data-stu-id="97d51-124">Windows Vista with SP1</span></span><br/>                                                      |
| <span data-ttu-id="97d51-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97d51-125">Minimum supported server</span></span><br/> | <span data-ttu-id="97d51-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97d51-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="97d51-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="97d51-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="97d51-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97d51-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="97d51-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="97d51-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97d51-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97d51-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="97d51-131">IID</span><span class="sxs-lookup"><span data-stu-id="97d51-131">IID</span></span><br/>                      | <span data-ttu-id="97d51-132">IID \_ IMsRdpClient6 se define como d43b7d80-8517-4b6d-9eac-96ad6800d7f2</span><span class="sxs-lookup"><span data-stu-id="97d51-132">IID\_IMsRdpClient6 is defined as d43b7d80-8517-4b6d-9eac-96ad6800d7f2</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="97d51-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="97d51-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97d51-134">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="97d51-134">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="97d51-135">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="97d51-135">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="97d51-136">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="97d51-136">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="97d51-137">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="97d51-137">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="97d51-138">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="97d51-138">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





