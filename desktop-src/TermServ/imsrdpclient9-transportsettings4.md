---
title: Propiedad TransportSettings4 de IMsRdpClient9
description: Recupera un objeto que admite la interfaz IMsRdpClientTransportSettings4.
ms.assetid: 808259b9-a1a4-4611-8602-b6877013c4f6
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad TransportSettings4
- Propiedad TransportSettings4 Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Servicios de Escritorio remoto de la interfaz IMsRdpClient9, propiedad TransportSettings4
- Propiedad TransportSettings4 Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Servicios de Escritorio remoto de la interfaz IMsRdpClient10, propiedad TransportSettings4
topic_type:
- apiref
api_name:
- IMsRdpClient9.TransportSettings4
- IMsRdpClient9.get_TransportSettings4
- IMsRdpClient10.TransportSettings4
- IMsRdpClient10.get_TransportSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 765d2ad5a50e0608e4c11731742debbaede51737
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359674"
---
# <a name="imsrdpclient9transportsettings4-property"></a><span data-ttu-id="65a79-108">IMsRdpClient9:: TransportSettings4 (propiedad)</span><span class="sxs-lookup"><span data-stu-id="65a79-108">IMsRdpClient9::TransportSettings4 property</span></span>

<span data-ttu-id="65a79-109">Recupera un objeto que admite la interfaz [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) .</span><span class="sxs-lookup"><span data-stu-id="65a79-109">Retrieves an object that supports the [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) interface.</span></span>

<span data-ttu-id="65a79-110">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="65a79-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="65a79-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65a79-111">Syntax</span></span>


```C++
HRESULT get_TransportSettings4(
  [out, retval] IMsRdpClientTransportSettings4 **ppXportSet4
);
```



## <a name="property-value"></a><span data-ttu-id="65a79-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="65a79-112">Property value</span></span>

<span data-ttu-id="65a79-113">Devuelve un puntero de la interfaz [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) .</span><span class="sxs-lookup"><span data-stu-id="65a79-113">Returns an [**IMsRdpClientTransportSettings4**](imsrdpclienttransportsettings4.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="65a79-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65a79-114">Requirements</span></span>



| <span data-ttu-id="65a79-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="65a79-115">Requirement</span></span> | <span data-ttu-id="65a79-116">Value</span><span class="sxs-lookup"><span data-stu-id="65a79-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65a79-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65a79-117">Minimum supported client</span></span><br/> | <span data-ttu-id="65a79-118">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="65a79-118">Windows 8.1</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="65a79-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="65a79-119">Minimum supported server</span></span><br/> | <span data-ttu-id="65a79-120">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="65a79-120">Windows Server 2012 R2</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="65a79-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="65a79-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="65a79-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65a79-122"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="65a79-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="65a79-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65a79-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65a79-124"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="65a79-125">IID</span><span class="sxs-lookup"><span data-stu-id="65a79-125">IID</span></span><br/>                      | <span data-ttu-id="65a79-126">CLSID \_ MsRdpClient9 se define como 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="65a79-126">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="65a79-127">CLSID \_ MsRdpClient9NotSafeForScripting se define como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="65a79-127">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> <span data-ttu-id="65a79-128">IID \_ IMsRdpClient9 se define como 28904001-04B6-436C-A55B-0AF1A0883DC9</span><span class="sxs-lookup"><span data-stu-id="65a79-128">IID\_IMsRdpClient9 is defined as 28904001-04B6-436C-A55B-0AF1A0883DC9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="65a79-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="65a79-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65a79-130">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="65a79-130">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="65a79-131">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="65a79-131">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





