---
description: El método RemoveTailI quita el último elemento de la lista.
ms.assetid: 3e9f88a5-a681-4494-8977-d9a6ec62a849
title: Método CBaseList. RemoveTailI (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveTailI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17c4e151426b54667ea3b9e4cb88be9526e2054b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671326"
---
# <a name="cbaselistremovetaili-method"></a><span data-ttu-id="87adb-103">CBaseList. RemoveTailI, método</span><span class="sxs-lookup"><span data-stu-id="87adb-103">CBaseList.RemoveTailI method</span></span>

<span data-ttu-id="87adb-104">El `RemoveTailI` método quita el último elemento de la lista.</span><span class="sxs-lookup"><span data-stu-id="87adb-104">The `RemoveTailI` method removes the last item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="87adb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="87adb-105">Syntax</span></span>


```C++
void* RemoveTailI();
```



## <a name="parameters"></a><span data-ttu-id="87adb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="87adb-106">Parameters</span></span>

<span data-ttu-id="87adb-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="87adb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="87adb-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="87adb-108">Return value</span></span>

<span data-ttu-id="87adb-109">Devuelve un puntero al elemento, o **null** si la lista está vacía.</span><span class="sxs-lookup"><span data-stu-id="87adb-109">Returns a pointer to the item, or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="87adb-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="87adb-110">Remarks</span></span>

<span data-ttu-id="87adb-111">Este método elimina el nodo de lista, pero no el elemento contenido en el nodo.</span><span class="sxs-lookup"><span data-stu-id="87adb-111">This method deletes the list node, but not the item that is contained in the node.</span></span>

## <a name="requirements"></a><span data-ttu-id="87adb-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87adb-112">Requirements</span></span>



| <span data-ttu-id="87adb-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="87adb-113">Requirement</span></span> | <span data-ttu-id="87adb-114">Value</span><span class="sxs-lookup"><span data-stu-id="87adb-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87adb-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87adb-115">Header</span></span><br/>  | <dl> <span data-ttu-id="87adb-116"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87adb-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="87adb-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="87adb-117">Library</span></span><br/> | <dl> <span data-ttu-id="87adb-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="87adb-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87adb-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="87adb-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87adb-120">**Clase CBaseList**</span><span class="sxs-lookup"><span data-stu-id="87adb-120">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




