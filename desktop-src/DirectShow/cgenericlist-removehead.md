---
description: El método RemoveHead quita el primer elemento de la lista.
ms.assetid: 95902028-d2c2-4c16-9ca6-ef57174a9292
title: Método CGenericList. RemoveHead (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: da9267d6b3e0c3196b3a9d1e873f222649b66684
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660835"
---
# <a name="cgenericlistremovehead-method"></a><span data-ttu-id="b3c20-103">CGenericList. RemoveHead, método</span><span class="sxs-lookup"><span data-stu-id="b3c20-103">CGenericList.RemoveHead method</span></span>

<span data-ttu-id="b3c20-104">El `RemoveHead` método quita el primer elemento de la lista.</span><span class="sxs-lookup"><span data-stu-id="b3c20-104">The `RemoveHead` method removes the first item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3c20-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b3c20-105">Syntax</span></span>


```C++
OBJECT* RemoveHead();
```



## <a name="parameters"></a><span data-ttu-id="b3c20-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3c20-106">Parameters</span></span>

<span data-ttu-id="b3c20-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="b3c20-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b3c20-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3c20-108">Return value</span></span>

<span data-ttu-id="b3c20-109">Devuelve un puntero a un objeto de tipo **Object** (el tipo de plantilla) o **null** si la lista está vacía.</span><span class="sxs-lookup"><span data-stu-id="b3c20-109">Returns a pointer to an object of type **OBJECT** (the template type), or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3c20-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b3c20-110">Remarks</span></span>

<span data-ttu-id="b3c20-111">Este método elimina el nodo de lista, pero no el elemento que contiene el nodo.</span><span class="sxs-lookup"><span data-stu-id="b3c20-111">This method deletes the list node, but not the item that the node contains.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3c20-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3c20-112">Requirements</span></span>



| <span data-ttu-id="b3c20-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3c20-113">Requirement</span></span> | <span data-ttu-id="b3c20-114">Value</span><span class="sxs-lookup"><span data-stu-id="b3c20-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3c20-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3c20-115">Header</span></span><br/>  | <dl> <span data-ttu-id="b3c20-116"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b3c20-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b3c20-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b3c20-117">Library</span></span><br/> | <dl> <span data-ttu-id="b3c20-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b3c20-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3c20-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="b3c20-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3c20-120">**Clase CGenericList**</span><span class="sxs-lookup"><span data-stu-id="b3c20-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




