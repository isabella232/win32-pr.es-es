---
description: El método RemoveHeadI quita el primer elemento de la lista.
ms.assetid: 7e448e32-ea31-4015-9219-1f990bf8763d
title: Método CBaseList. RemoveHeadI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveHeadI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d9b99dbac1d99587145aa2eba293ffa7ace959c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671227"
---
# <a name="cbaselistremoveheadi-method"></a><span data-ttu-id="229e4-103">CBaseList. RemoveHeadI, método</span><span class="sxs-lookup"><span data-stu-id="229e4-103">CBaseList.RemoveHeadI method</span></span>

<span data-ttu-id="229e4-104">El `RemoveHeadI` método quita el primer elemento de la lista.</span><span class="sxs-lookup"><span data-stu-id="229e4-104">The `RemoveHeadI` method removes the first item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="229e4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="229e4-105">Syntax</span></span>


```C++
void* RemoveHeadI();
```



## <a name="parameters"></a><span data-ttu-id="229e4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="229e4-106">Parameters</span></span>

<span data-ttu-id="229e4-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="229e4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="229e4-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="229e4-108">Return value</span></span>

<span data-ttu-id="229e4-109">Devuelve un puntero al elemento, o **null** si la lista está vacía.</span><span class="sxs-lookup"><span data-stu-id="229e4-109">Returns a pointer to the item, or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="229e4-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="229e4-110">Remarks</span></span>

<span data-ttu-id="229e4-111">Este método elimina el nodo de lista, pero no el elemento que contiene el nodo.</span><span class="sxs-lookup"><span data-stu-id="229e4-111">This method deletes the list node, but not the item that the node contains.</span></span>

## <a name="requirements"></a><span data-ttu-id="229e4-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="229e4-112">Requirements</span></span>



| <span data-ttu-id="229e4-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="229e4-113">Requirement</span></span> | <span data-ttu-id="229e4-114">Value</span><span class="sxs-lookup"><span data-stu-id="229e4-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="229e4-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="229e4-115">Header</span></span><br/>  | <dl> <span data-ttu-id="229e4-116"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="229e4-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="229e4-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="229e4-117">Library</span></span><br/> | <dl> <span data-ttu-id="229e4-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="229e4-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="229e4-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="229e4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="229e4-120">**Clase CBaseList**</span><span class="sxs-lookup"><span data-stu-id="229e4-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




