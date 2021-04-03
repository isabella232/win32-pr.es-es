---
description: Moniker de suscriptores.
ms.assetid: d33d8c80-3251-4ec7-9cf3-d0b60d91ed5a
title: Propiedad IEventSubscription2SubscriberMoniker
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2.SubscriberMoniker
- IEventSubscription2.get_SubscriberMoniker
- IEventSubscription2.put_SubscriberMoniker
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9496a3046b4bb0e99a88322892e557588a92aab8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807376"
---
# <a name="ieventsubscription2subscribermoniker-property"></a><span data-ttu-id="b4a11-103">IEventSubscription2:: SubscriberMoniker (propiedad)</span><span class="sxs-lookup"><span data-stu-id="b4a11-103">IEventSubscription2::SubscriberMoniker property</span></span>

<span data-ttu-id="b4a11-104">Moniker del suscriptor.</span><span class="sxs-lookup"><span data-stu-id="b4a11-104">The subscriber's moniker.</span></span>

<span data-ttu-id="b4a11-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b4a11-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4a11-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4a11-106">Syntax</span></span>


```C++
HRESULT put_SubscriberMoniker(
  [in]          BSTR bstrMoniker
);

HRESULT get_SubscriberMoniker(
  [out, retval] BSTR *pbstrMoniker
);
```



## <a name="property-value"></a><span data-ttu-id="b4a11-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b4a11-107">Property value</span></span>

<span data-ttu-id="b4a11-108">Cadena de moniker que especifica el suscriptor.</span><span class="sxs-lookup"><span data-stu-id="b4a11-108">A moniker string specifying the subscriber.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b4a11-109">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="b4a11-109">Error codes</span></span>

<span data-ttu-id="b4a11-110">Este método puede devolver los valores devueltos estándar E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inesperado, e \_ FAIL y S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b4a11-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4a11-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4a11-111">Requirements</span></span>



| <span data-ttu-id="b4a11-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4a11-112">Requirement</span></span> | <span data-ttu-id="b4a11-113">Value</span><span class="sxs-lookup"><span data-stu-id="b4a11-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="b4a11-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4a11-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b4a11-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b4a11-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="b4a11-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4a11-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b4a11-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b4a11-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="b4a11-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4a11-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4a11-119">**IEventSubscription2**</span><span class="sxs-lookup"><span data-stu-id="b4a11-119">**IEventSubscription2**</span></span>](ieventsubscription2.md)
</dt> </dl>

 

 




