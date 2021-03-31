---
title: Propiedad RemoteProgram2 de IMsRdpClient7
description: Recupera un objeto que admite la interfaz ITSRemoteProgram2.
ms.assetid: fabdc933-c941-487f-9e49-c20a39e0c86e
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RemoteProgram2
- Propiedad RemoteProgram2 Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad RemoteProgram2
- Propiedad RemoteProgram2 Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad RemoteProgram2
- Propiedad RemoteProgram2 Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad RemoteProgram2
- Propiedad RemoteProgram2 Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Servicios de Escritorio remoto de la interfaz IMsRdpClient10, propiedad RemoteProgram2
topic_type:
- apiref
api_name:
- IMsRdpClient7.RemoteProgram2
- IMsRdpClient7.get_RemoteProgram2
- IMsRdpClient8.RemoteProgram2
- IMsRdpClient8.get_RemoteProgram2
- IMsRdpClient9.RemoteProgram2
- IMsRdpClient9.get_RemoteProgram2
- IMsRdpClient10.RemoteProgram2
- IMsRdpClient10.get_RemoteProgram2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1572aada1384a7edfe88b198826050927ae3cff5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996079"
---
# <a name="imsrdpclient7remoteprogram2-property"></a><span data-ttu-id="37d48-112">IMsRdpClient7:: RemoteProgram2 (propiedad)</span><span class="sxs-lookup"><span data-stu-id="37d48-112">IMsRdpClient7::RemoteProgram2 property</span></span>

<span data-ttu-id="37d48-113">Recupera un objeto que admite la interfaz [**ITSRemoteProgram2**](itsremoteprogram2.md) .</span><span class="sxs-lookup"><span data-stu-id="37d48-113">Retrieves an object that supports the [**ITSRemoteProgram2**](itsremoteprogram2.md) interface.</span></span>

<span data-ttu-id="37d48-114">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="37d48-114">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="37d48-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37d48-115">Syntax</span></span>


```C++
HRESULT get_RemoteProgram2(
  [out, retval] ITSRemoteProgram2 **ppRemoteProgram
);
```



## <a name="property-value"></a><span data-ttu-id="37d48-116">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="37d48-116">Property value</span></span>

<span data-ttu-id="37d48-117">Dirección de un puntero de interfaz [**ITSRemoteProgram2**](itsremoteprogram2.md) que recibe el objeto.</span><span class="sxs-lookup"><span data-stu-id="37d48-117">The address of an [**ITSRemoteProgram2**](itsremoteprogram2.md) interface pointer that receives the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="37d48-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37d48-118">Requirements</span></span>



| <span data-ttu-id="37d48-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="37d48-119">Requirement</span></span> | <span data-ttu-id="37d48-120">Value</span><span class="sxs-lookup"><span data-stu-id="37d48-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="37d48-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37d48-121">Minimum supported client</span></span><br/> | <span data-ttu-id="37d48-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="37d48-122">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="37d48-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37d48-123">Minimum supported server</span></span><br/> | <span data-ttu-id="37d48-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="37d48-124">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="37d48-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="37d48-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="37d48-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37d48-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="37d48-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="37d48-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37d48-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37d48-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="37d48-129">IID</span><span class="sxs-lookup"><span data-stu-id="37d48-129">IID</span></span><br/>                      | <span data-ttu-id="37d48-130">IID \_ IMsRdpClient7 se define como b2a5b5ce-3461-444A-91d4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="37d48-130">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="37d48-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="37d48-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37d48-132">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="37d48-132">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="37d48-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="37d48-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="37d48-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="37d48-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="37d48-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="37d48-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





