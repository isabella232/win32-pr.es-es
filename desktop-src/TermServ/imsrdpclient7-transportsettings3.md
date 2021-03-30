---
title: Propiedad TransportSettings3 de IMsRdpClient7
description: Recupera un objeto que admite la interfaz IMsRdpClientTransportSettings3.
ms.assetid: d11f0943-241e-44cd-a98c-595916ab0718
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad TransportSettings3
- Propiedad TransportSettings3 Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad TransportSettings3
- Propiedad TransportSettings3 Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad TransportSettings3
- Propiedad TransportSettings3 Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad TransportSettings3
- Propiedad TransportSettings3 Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Servicios de Escritorio remoto de la interfaz IMsRdpClient10, propiedad TransportSettings3
topic_type:
- apiref
api_name:
- IMsRdpClient7.TransportSettings3
- IMsRdpClient7.get_TransportSettings3
- IMsRdpClient8.TransportSettings3
- IMsRdpClient8.get_TransportSettings3
- IMsRdpClient9.TransportSettings3
- IMsRdpClient9.get_TransportSettings3
- IMsRdpClient10.TransportSettings3
- IMsRdpClient10.get_TransportSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c60b58f8f2438de0d43f69ce0b3bb73607e7551
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801573"
---
# <a name="imsrdpclient7transportsettings3-property"></a><span data-ttu-id="229f4-112">IMsRdpClient7:: TransportSettings3 (propiedad)</span><span class="sxs-lookup"><span data-stu-id="229f4-112">IMsRdpClient7::TransportSettings3 property</span></span>

<span data-ttu-id="229f4-113">Recupera un objeto que admite la interfaz [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) .</span><span class="sxs-lookup"><span data-stu-id="229f4-113">Retrieves an object that supports the [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) interface.</span></span>

<span data-ttu-id="229f4-114">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="229f4-114">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="229f4-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="229f4-115">Syntax</span></span>


```C++
HRESULT get_TransportSettings3(
  [out, retval] IMsRdpClientTransportSettings3 **ppXportSet3
);
```



## <a name="property-value"></a><span data-ttu-id="229f4-116">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="229f4-116">Property value</span></span>

<span data-ttu-id="229f4-117">Dirección de un puntero de interfaz [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) que recibe el objeto.</span><span class="sxs-lookup"><span data-stu-id="229f4-117">The address of an [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) interface pointer that receives the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="229f4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="229f4-118">Requirements</span></span>



| <span data-ttu-id="229f4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="229f4-119">Requirement</span></span> | <span data-ttu-id="229f4-120">Value</span><span class="sxs-lookup"><span data-stu-id="229f4-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="229f4-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="229f4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="229f4-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="229f4-122">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="229f4-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="229f4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="229f4-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="229f4-124">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="229f4-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="229f4-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="229f4-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="229f4-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="229f4-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="229f4-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="229f4-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="229f4-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="229f4-129">IID</span><span class="sxs-lookup"><span data-stu-id="229f4-129">IID</span></span><br/>                      | <span data-ttu-id="229f4-130">IID \_ IMsRdpClient7 se define como b2a5b5ce-3461-444A-91d4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="229f4-130">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="229f4-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="229f4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="229f4-132">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="229f4-132">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="229f4-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="229f4-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="229f4-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="229f4-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="229f4-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="229f4-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





