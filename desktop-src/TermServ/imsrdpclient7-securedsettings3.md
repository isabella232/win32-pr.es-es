---
title: Propiedad SecuredSettings3 de IMsRdpClient7
description: Recupera un objeto que admite la interfaz IMsRdpClientSecuredSettings2.
ms.assetid: 500ce7ed-bd86-434c-baf8-f30dd667dca3
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad SecuredSettings3
- Propiedad SecuredSettings3 Servicios de Escritorio remoto, interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, propiedad SecuredSettings3
- Propiedad SecuredSettings3 Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Servicios de Escritorio remoto de la interfaz IMsRdpClient8, propiedad SecuredSettings3
- Propiedad SecuredSettings3 Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad SecuredSettings3
- Propiedad SecuredSettings3 Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Servicios de Escritorio remoto de la interfaz IMsRdpClient10, propiedad SecuredSettings3
topic_type:
- apiref
api_name:
- IMsRdpClient7.SecuredSettings3
- IMsRdpClient7.get_SecuredSettings3
- IMsRdpClient8.SecuredSettings3
- IMsRdpClient8.get_SecuredSettings3
- IMsRdpClient9.SecuredSettings3
- IMsRdpClient9.get_SecuredSettings3
- IMsRdpClient10.SecuredSettings3
- IMsRdpClient10.get_SecuredSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 219e3373a6ecb2f5b963a82800f4415f7de64534
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422079"
---
# <a name="imsrdpclient7securedsettings3-property"></a><span data-ttu-id="ae6ca-112">IMsRdpClient7:: SecuredSettings3 (propiedad)</span><span class="sxs-lookup"><span data-stu-id="ae6ca-112">IMsRdpClient7::SecuredSettings3 property</span></span>

<span data-ttu-id="ae6ca-113">Recupera un objeto que admite la interfaz [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="ae6ca-113">Retrieves an object that supports the [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) interface.</span></span>

<span data-ttu-id="ae6ca-114">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ae6ca-114">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae6ca-115">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae6ca-115">Syntax</span></span>


```C++
HRESULT get_SecuredSettings3(
  [out] IMsRdpClientSecuredSettings2 **ppSecuredSettings
);
```



## <a name="property-value"></a><span data-ttu-id="ae6ca-116">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ae6ca-116">Property value</span></span>

<span data-ttu-id="ae6ca-117">Dirección de un puntero de interfaz [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) que recibe el objeto.</span><span class="sxs-lookup"><span data-stu-id="ae6ca-117">The address of an [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) interface pointer that receives the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae6ca-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae6ca-118">Requirements</span></span>



| <span data-ttu-id="ae6ca-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae6ca-119">Requirement</span></span> | <span data-ttu-id="ae6ca-120">Value</span><span class="sxs-lookup"><span data-stu-id="ae6ca-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae6ca-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae6ca-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ae6ca-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ae6ca-122">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="ae6ca-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae6ca-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ae6ca-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ae6ca-124">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="ae6ca-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ae6ca-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="ae6ca-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae6ca-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ae6ca-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ae6ca-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae6ca-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae6ca-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ae6ca-129">IID</span><span class="sxs-lookup"><span data-stu-id="ae6ca-129">IID</span></span><br/>                      | <span data-ttu-id="ae6ca-130">IID \_ IMsRdpClient7 se define como b2a5b5ce-3461-444A-91d4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="ae6ca-130">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ae6ca-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae6ca-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae6ca-132">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="ae6ca-132">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="ae6ca-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="ae6ca-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="ae6ca-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="ae6ca-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="ae6ca-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="ae6ca-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





