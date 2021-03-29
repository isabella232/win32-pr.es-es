---
description: Recupera el número de interfaces de información de tipo proporcionado por un objeto.
ms.assetid: e16bc324-bb49-4df2-afeb-2c2cd1620693
title: Método CMediaEvent. GetTypeInfoCount (Ctlutil. h)
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
ms.openlocfilehash: 4de7a79251f2d25c1c55642050ad06513a1bfe6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679300"
---
# <a name="cmediaeventgettypeinfocount-method"></a><span data-ttu-id="cb5c1-103">CMediaEvent. GetTypeInfoCount, método</span><span class="sxs-lookup"><span data-stu-id="cb5c1-103">CMediaEvent.GetTypeInfoCount method</span></span>

<span data-ttu-id="cb5c1-104">Recupera el número de interfaces de información de tipo proporcionado por un objeto.</span><span class="sxs-lookup"><span data-stu-id="cb5c1-104">Retrieves the number of type-information interfaces provided by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb5c1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb5c1-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="cb5c1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb5c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb5c1-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="cb5c1-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="cb5c1-108">Puntero al número de interfaces de información de tipo que proporciona el objeto.</span><span class="sxs-lookup"><span data-stu-id="cb5c1-108">Pointer to number of type-information interfaces that the object provides.</span></span> <span data-ttu-id="cb5c1-109">Si el objeto proporciona información de tipo, este número es 1; de lo contrario, el número es 0.</span><span class="sxs-lookup"><span data-stu-id="cb5c1-109">If the object provides type information, this number is 1; otherwise, the number is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb5c1-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb5c1-110">Return value</span></span>

<span data-ttu-id="cb5c1-111">Devuelve el \_ puntero E si *pctinfo* no es válido; de lo contrario, devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cb5c1-111">Returns E\_POINTER if *pctinfo* is invalid; otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb5c1-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb5c1-112">Requirements</span></span>



| <span data-ttu-id="cb5c1-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb5c1-113">Requirement</span></span> | <span data-ttu-id="cb5c1-114">Value</span><span class="sxs-lookup"><span data-stu-id="cb5c1-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb5c1-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb5c1-115">Header</span></span><br/>  | <dl> <span data-ttu-id="cb5c1-116"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cb5c1-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cb5c1-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cb5c1-117">Library</span></span><br/> | <dl> <span data-ttu-id="cb5c1-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="cb5c1-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb5c1-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb5c1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb5c1-120">**Clase CMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="cb5c1-120">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




