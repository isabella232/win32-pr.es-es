---
description: GUID de partición del suscriptor.
ms.assetid: 0b2411d3-cdc1-492c-a54f-ca3d3bd8b953
title: 'IEventSubscription3:: SubscriberPartitionID (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.SubscriberPartitionID
- IEventSubscription3.get_SubscriberPartitionID
- IEventSubscription3.put_SubscriberPartitionID
api_type:
- COM
api_location: ''
ms.openlocfilehash: b09c41ac1b3a90c3275daf7afa0cd90fe2bb905c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275090"
---
# <a name="ieventsubscription3subscriberpartitionid-property"></a><span data-ttu-id="8765b-103">IEventSubscription3:: SubscriberPartitionID (propiedad)</span><span class="sxs-lookup"><span data-stu-id="8765b-103">IEventSubscription3::SubscriberPartitionID property</span></span>

<span data-ttu-id="8765b-104">GUID de partición del suscriptor.</span><span class="sxs-lookup"><span data-stu-id="8765b-104">The partition GUID of the subscriber.</span></span>

<span data-ttu-id="8765b-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="8765b-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8765b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8765b-106">Syntax</span></span>


```C++
HRESULT put_SubscriberPartitionID(
  [in]          BSTR bstrSubscriberPartitionID
);

HRESULT get_SubscriberPartitionID(
  [out, retval] BSTR *pbstrSubscriberPartitionID
);
```



## <a name="property-value"></a><span data-ttu-id="8765b-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8765b-107">Property value</span></span>

<span data-ttu-id="8765b-108">Cadena que contiene el GUID de la partición del suscriptor.</span><span class="sxs-lookup"><span data-stu-id="8765b-108">A string containing the GUID of the subscriber partition.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8765b-109">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="8765b-109">Error codes</span></span>

<span data-ttu-id="8765b-110">Este método puede devolver los valores devueltos estándar E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inesperado, e \_ FAIL y S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8765b-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="8765b-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8765b-111">Requirements</span></span>



| <span data-ttu-id="8765b-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="8765b-112">Requirement</span></span> | <span data-ttu-id="8765b-113">Value</span><span class="sxs-lookup"><span data-stu-id="8765b-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="8765b-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8765b-114">Minimum supported client</span></span><br/> | <span data-ttu-id="8765b-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8765b-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8765b-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8765b-116">Minimum supported server</span></span><br/> | <span data-ttu-id="8765b-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8765b-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="8765b-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="8765b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8765b-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="8765b-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




