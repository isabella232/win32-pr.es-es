---
description: 'Método CMediaEvent.GetTypeInfoCount: recupera el número de interfaces de información de tipos proporcionadas por un objeto .'
ms.assetid: e16bc324-bb49-4df2-afeb-2c2cd1620693
title: Método CMediaEvent.GetTypeInfoCount (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9402ad973a08afed4d338cfdc7b5df7fb14b9f0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099123"
---
# <a name="cmediaeventgettypeinfocount-method"></a><span data-ttu-id="e9e52-103">Método CMediaEvent.GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="e9e52-103">CMediaEvent.GetTypeInfoCount method</span></span>

<span data-ttu-id="e9e52-104">Recupera el número de interfaces de información de tipo proporcionadas por un objeto .</span><span class="sxs-lookup"><span data-stu-id="e9e52-104">Retrieves the number of type-information interfaces provided by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9e52-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e9e52-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="e9e52-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e9e52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9e52-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="e9e52-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="e9e52-108">Puntero al número de interfaces de información de tipos que proporciona el objeto .</span><span class="sxs-lookup"><span data-stu-id="e9e52-108">Pointer to number of type-information interfaces that the object provides.</span></span> <span data-ttu-id="e9e52-109">Si el objeto proporciona información de tipo, este número es 1; De lo contrario, el número es 0.</span><span class="sxs-lookup"><span data-stu-id="e9e52-109">If the object provides type information, this number is 1; otherwise, the number is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9e52-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e9e52-110">Return value</span></span>

<span data-ttu-id="e9e52-111">Devuelve E \_ POINTER si *pctinfo* no es válido; de lo contrario, devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e9e52-111">Returns E\_POINTER if *pctinfo* is invalid; otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9e52-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9e52-112">Requirements</span></span>



| <span data-ttu-id="e9e52-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9e52-113">Requirement</span></span> | <span data-ttu-id="e9e52-114">Value</span><span class="sxs-lookup"><span data-stu-id="e9e52-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9e52-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9e52-115">Header</span></span><br/>  | <dl> <span data-ttu-id="e9e52-116"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9e52-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e9e52-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e9e52-117">Library</span></span><br/> | <dl> <span data-ttu-id="e9e52-118"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e9e52-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9e52-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e9e52-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9e52-120">**CMediaEvent (clase)**</span><span class="sxs-lookup"><span data-stu-id="e9e52-120">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




