---
description: GUID de la aplicación del suscriptor.
ms.assetid: 46c91cae-ca31-4eac-baa8-d36910917f0f
title: 'IEventSubscription3:: SubscriberApplicationID (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription3.SubscriberApplicationID
- IEventSubscription3.get_SubscriberApplicationID
- IEventSubscription3.put_SubscriberApplicationID
api_type:
- COM
api_location: ''
ms.openlocfilehash: c2e726d97821a7a7143f4971a4918227235adb9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274925"
---
# <a name="ieventsubscription3subscriberapplicationid-property"></a><span data-ttu-id="4f5d4-103">IEventSubscription3:: SubscriberApplicationID (propiedad)</span><span class="sxs-lookup"><span data-stu-id="4f5d4-103">IEventSubscription3::SubscriberApplicationID property</span></span>

<span data-ttu-id="4f5d4-104">GUID de la aplicación del suscriptor.</span><span class="sxs-lookup"><span data-stu-id="4f5d4-104">The application GUID of the subscriber.</span></span>

<span data-ttu-id="4f5d4-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="4f5d4-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f5d4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f5d4-106">Syntax</span></span>


```C++
HRESULT put_SubscriberApplicationID(
  [in]          BSTR bstrSubscriberApplicationID
);

HRESULT get_SubscriberApplicationID(
  [out, retval] BSTR *pbstrSubscriberApplicationID
);
```



## <a name="property-value"></a><span data-ttu-id="4f5d4-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4f5d4-107">Property value</span></span>

<span data-ttu-id="4f5d4-108">Cadena que contiene el GUID de la aplicación del suscriptor.</span><span class="sxs-lookup"><span data-stu-id="4f5d4-108">A string containing the GUID of the subscriber application.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4f5d4-109">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="4f5d4-109">Error codes</span></span>

<span data-ttu-id="4f5d4-110">Este método puede devolver los valores devueltos estándar E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inesperado, e \_ FAIL y S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4f5d4-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f5d4-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f5d4-111">Requirements</span></span>



| <span data-ttu-id="4f5d4-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f5d4-112">Requirement</span></span> | <span data-ttu-id="4f5d4-113">Value</span><span class="sxs-lookup"><span data-stu-id="4f5d4-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4f5d4-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f5d4-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4f5d4-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="4f5d4-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4f5d4-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f5d4-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4f5d4-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="4f5d4-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4f5d4-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f5d4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f5d4-119">**IEventSubscription3**</span><span class="sxs-lookup"><span data-stu-id="4f5d4-119">**IEventSubscription3**</span></span>](ieventsubscription3.md)
</dt> </dl>

 

 




