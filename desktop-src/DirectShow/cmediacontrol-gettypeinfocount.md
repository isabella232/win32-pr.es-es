---
description: Recupera el número de interfaces de información de tipo proporcionado por un objeto.
ms.assetid: 29575325-8f97-4f39-8272-86a917d9144f
title: Método CMediaControl. GetTypeInfoCount (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2454e503a045a02db20c0dc457b6367f6d3b427
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671522"
---
# <a name="cmediacontrolgettypeinfocount-method"></a><span data-ttu-id="4c8a8-103">CMediaControl. GetTypeInfoCount, método</span><span class="sxs-lookup"><span data-stu-id="4c8a8-103">CMediaControl.GetTypeInfoCount method</span></span>

<span data-ttu-id="4c8a8-104">Recupera el número de interfaces de información de tipo proporcionado por un objeto.</span><span class="sxs-lookup"><span data-stu-id="4c8a8-104">Retrieves the number of type-information interfaces provided by an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c8a8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4c8a8-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="4c8a8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c8a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c8a8-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="4c8a8-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="4c8a8-108">Puntero al número de interfaces de información de tipo que proporciona el objeto.</span><span class="sxs-lookup"><span data-stu-id="4c8a8-108">Pointer to the number of type-information interfaces that the object provides.</span></span> <span data-ttu-id="4c8a8-109">Si el objeto proporciona información de tipo, este número es 1; de lo contrario, el número es 0.</span><span class="sxs-lookup"><span data-stu-id="4c8a8-109">If the object provides type information, this number is 1; otherwise, the number is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c8a8-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c8a8-110">Return value</span></span>

<span data-ttu-id="4c8a8-111">Devuelve el \_ puntero E si *pctinfo* no es válido; de lo contrario, devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4c8a8-111">Returns E\_POINTER if *pctinfo* is invalid; otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c8a8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c8a8-112">Requirements</span></span>



| <span data-ttu-id="4c8a8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c8a8-113">Requirement</span></span> | <span data-ttu-id="4c8a8-114">Value</span><span class="sxs-lookup"><span data-stu-id="4c8a8-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c8a8-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4c8a8-115">Header</span></span><br/>  | <dl> <span data-ttu-id="4c8a8-116"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4c8a8-116"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4c8a8-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4c8a8-117">Library</span></span><br/> | <dl> <span data-ttu-id="4c8a8-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="4c8a8-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c8a8-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c8a8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c8a8-120">**Clase CMediaControl**</span><span class="sxs-lookup"><span data-stu-id="4c8a8-120">**CMediaControl Class**</span></span>](cmediacontrol.md)
</dt> </dl>

 

 




