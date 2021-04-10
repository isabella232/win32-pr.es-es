---
description: Los criterios de filtro que rigen la suscripción.
ms.assetid: cfc3ba9e-0566-45fd-917f-34842b8ff377
title: 'IEventSubscription2:: FilterCriteria (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSubscription2.FilterCriteria
- IEventSubscription2.get_FilterCriteria
- IEventSubscription2.put_FilterCriteria
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1443a89433cff91a298e8c390fce8f1f64b99f1b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153391"
---
# <a name="ieventsubscription2filtercriteria-property"></a><span data-ttu-id="58e0d-103">IEventSubscription2:: FilterCriteria (propiedad)</span><span class="sxs-lookup"><span data-stu-id="58e0d-103">IEventSubscription2::FilterCriteria property</span></span>

<span data-ttu-id="58e0d-104">Los criterios de filtro que rigen la suscripción.</span><span class="sxs-lookup"><span data-stu-id="58e0d-104">The filter criteria governing the subscription.</span></span>

<span data-ttu-id="58e0d-105">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="58e0d-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="58e0d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58e0d-106">Syntax</span></span>


```C++
HRESULT put_FilterCriteria(
  [in]          BSTR bstrFilterCriteria
);

HRESULT get_FilterCriteria(
  [out, retval] BSTR *pbstrFilterCriteria
);
```



## <a name="property-value"></a><span data-ttu-id="58e0d-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="58e0d-107">Property value</span></span>

<span data-ttu-id="58e0d-108">Los criterios de filtro o el CLSID para una clase que implementa [**IPublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter).</span><span class="sxs-lookup"><span data-stu-id="58e0d-108">The filter criteria or the CLSID for a class implementing [**IPublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter).</span></span>

## <a name="error-codes"></a><span data-ttu-id="58e0d-109">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="58e0d-109">Error codes</span></span>

<span data-ttu-id="58e0d-110">Este método puede devolver los valores devueltos estándar E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ inesperado, e \_ FAIL y S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="58e0d-110">This method can return the standard return values E\_INVALIDARG, E\_OUTOFMEMORY, E\_UNEXPECTED, E\_FAIL, and S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="58e0d-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58e0d-111">Requirements</span></span>



| <span data-ttu-id="58e0d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="58e0d-112">Requirement</span></span> | <span data-ttu-id="58e0d-113">Value</span><span class="sxs-lookup"><span data-stu-id="58e0d-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="58e0d-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58e0d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="58e0d-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="58e0d-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="58e0d-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="58e0d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="58e0d-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="58e0d-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="58e0d-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="58e0d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58e0d-119">**IEventSubscription2**</span><span class="sxs-lookup"><span data-stu-id="58e0d-119">**IEventSubscription2**</span></span>](ieventsubscription2.md)
</dt> </dl>

 

 




