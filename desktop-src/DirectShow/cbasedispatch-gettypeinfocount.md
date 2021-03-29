---
description: El método GetTypeInfoCount recupera el número de interfaces de información de tipo que proporciona el objeto.
ms.assetid: e09e6f6c-6ac8-4ce1-8ce1-ee5374d54183
title: Método CBaseDispatch. GetTypeInfoCount (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch.GetTypeInfoCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39c5b78181f5f26fb5f57831345bb6345a26da85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660579"
---
# <a name="cbasedispatchgettypeinfocount-method"></a><span data-ttu-id="cc961-103">CBaseDispatch. GetTypeInfoCount, método</span><span class="sxs-lookup"><span data-stu-id="cc961-103">CBaseDispatch.GetTypeInfoCount method</span></span>

<span data-ttu-id="cc961-104">El `GetTypeInfoCount` método recupera el número de interfaces de información de tipo que proporciona el objeto.</span><span class="sxs-lookup"><span data-stu-id="cc961-104">The `GetTypeInfoCount` method retrieves the number of type information interfaces the object provides.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc961-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc961-105">Syntax</span></span>


```C++
HRESULT GetTypeInfoCount(
   UINT *pctinfo
);
```



## <a name="parameters"></a><span data-ttu-id="cc961-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc961-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc961-107">*pctinfo*</span><span class="sxs-lookup"><span data-stu-id="cc961-107">*pctinfo*</span></span> 
</dt> <dd>

<span data-ttu-id="cc961-108">Puntero a una variable que recibe el número de interfaces de información de tipo proporcionado por el objeto.</span><span class="sxs-lookup"><span data-stu-id="cc961-108">Pointer to a variable that receives the number of type-information interfaces provided by the object.</span></span> <span data-ttu-id="cc961-109">Cuando el método devuelve, el valor es 1.</span><span class="sxs-lookup"><span data-stu-id="cc961-109">When the method returns, the value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc961-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc961-110">Return value</span></span>

<span data-ttu-id="cc961-111">Devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="cc961-111">Returns one of the following values.</span></span>



| <span data-ttu-id="cc961-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="cc961-112">Return code</span></span>                                                                               | <span data-ttu-id="cc961-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc961-113">Description</span></span>                           |
|-------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="cc961-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="cc961-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="cc961-115">Correcto.</span><span class="sxs-lookup"><span data-stu-id="cc961-115">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="cc961-116"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="cc961-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="cc961-117">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="cc961-117">**NULL** pointer argument.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cc961-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc961-118">Requirements</span></span>



| <span data-ttu-id="cc961-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc961-119">Requirement</span></span> | <span data-ttu-id="cc961-120">Value</span><span class="sxs-lookup"><span data-stu-id="cc961-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc961-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cc961-121">Header</span></span><br/>  | <dl> <span data-ttu-id="cc961-122"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc961-122"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cc961-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc961-123">Library</span></span><br/> | <dl> <span data-ttu-id="cc961-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="cc961-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc961-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="cc961-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc961-126">**Clase CBaseDispatch**</span><span class="sxs-lookup"><span data-stu-id="cc961-126">**CBaseDispatch Class**</span></span>](cbasedispatch.md)
</dt> </dl>

 

 




