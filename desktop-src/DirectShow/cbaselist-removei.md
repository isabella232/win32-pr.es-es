---
description: El método removei quita el elemento en la posición especificada.
ms.assetid: 6a6d54ce-7ab3-48dd-8d5d-1315816bcbb9
title: Método CBaseList. removei (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.RemoveI
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4511a9867f61596572c959a3d763eb56d862311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671327"
---
# <a name="cbaselistremovei-method"></a><span data-ttu-id="84c73-103">CBaseList. Remove (método)</span><span class="sxs-lookup"><span data-stu-id="84c73-103">CBaseList.RemoveI method</span></span>

<span data-ttu-id="84c73-104">El `RemoveI` método quita el elemento en la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="84c73-104">The `RemoveI` method removes the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="84c73-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="84c73-105">Syntax</span></span>


```C++
void* RemoveI(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="84c73-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="84c73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84c73-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="84c73-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="84c73-108">Valor de posición que indica el elemento que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="84c73-108">POSITION value indicating the item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84c73-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="84c73-109">Return value</span></span>

<span data-ttu-id="84c73-110">Devuelve un puntero al elemento.</span><span class="sxs-lookup"><span data-stu-id="84c73-110">Returns a pointer to the item.</span></span>

## <a name="remarks"></a><span data-ttu-id="84c73-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="84c73-111">Remarks</span></span>

<span data-ttu-id="84c73-112">Este método elimina el nodo de la lista, pero no elimina el elemento contenido en ese nodo.</span><span class="sxs-lookup"><span data-stu-id="84c73-112">This method deletes the node from the list, but does not delete the item contained in that node.</span></span>

<span data-ttu-id="84c73-113">Si *pos* es **null**, el método devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="84c73-113">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="84c73-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84c73-114">Requirements</span></span>



| <span data-ttu-id="84c73-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="84c73-115">Requirement</span></span> | <span data-ttu-id="84c73-116">Value</span><span class="sxs-lookup"><span data-stu-id="84c73-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84c73-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="84c73-117">Header</span></span><br/>  | <dl> <span data-ttu-id="84c73-118"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="84c73-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="84c73-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="84c73-119">Library</span></span><br/> | <dl> <span data-ttu-id="84c73-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="84c73-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84c73-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="84c73-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84c73-122">**Clase CBaseList**</span><span class="sxs-lookup"><span data-stu-id="84c73-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




