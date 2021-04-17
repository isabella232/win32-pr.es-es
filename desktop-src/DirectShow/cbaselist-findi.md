---
description: El método Findi recupera la primera posición que contiene el elemento especificado.
ms.assetid: a95fac19-0f93-4bb4-8e76-0da82745a1d2
title: Método CBaseList. Findi (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.FindI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2366f8c4c117b8550d91c84bffafb03393801088
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670938"
---
# <a name="cbaselistfindi-method"></a><span data-ttu-id="c91a3-103">CBaseList. Findi (método)</span><span class="sxs-lookup"><span data-stu-id="c91a3-103">CBaseList.FindI method</span></span>

<span data-ttu-id="c91a3-104">El `FindI` método recupera la primera posición que contiene el elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="c91a3-104">The `FindI` method retrieves the first position that holds the specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="c91a3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c91a3-105">Syntax</span></span>


```C++
POSITION FindI(
   void *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="c91a3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c91a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c91a3-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="c91a3-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="c91a3-108">Puntero al elemento.</span><span class="sxs-lookup"><span data-stu-id="c91a3-108">Pointer to the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c91a3-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c91a3-109">Return value</span></span>

<span data-ttu-id="c91a3-110">Devuelve un valor de posición o **null** si el elemento no está en la lista.</span><span class="sxs-lookup"><span data-stu-id="c91a3-110">Returns a POSITION value, or **NULL** if the item is not in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="c91a3-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c91a3-111">Requirements</span></span>



| <span data-ttu-id="c91a3-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="c91a3-112">Requirement</span></span> | <span data-ttu-id="c91a3-113">Value</span><span class="sxs-lookup"><span data-stu-id="c91a3-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c91a3-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c91a3-114">Header</span></span><br/>  | <dl> <span data-ttu-id="c91a3-115"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c91a3-115"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c91a3-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c91a3-116">Library</span></span><br/> | <dl> <span data-ttu-id="c91a3-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c91a3-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c91a3-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="c91a3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c91a3-119">**Clase CBaseList**</span><span class="sxs-lookup"><span data-stu-id="c91a3-119">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




