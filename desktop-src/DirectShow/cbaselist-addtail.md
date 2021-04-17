---
description: El método Addtail (anexa otra lista al final de esta lista.
ms.assetid: 996523cd-d9ba-406a-afdf-494d328dc9dd
title: Método CBaseList. Addtail ((Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36d42f0b80703457032e5dde37f6d1549da089c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670940"
---
# <a name="cbaselistaddtail-method"></a><span data-ttu-id="87531-103">CBaseList. Addtail (, método</span><span class="sxs-lookup"><span data-stu-id="87531-103">CBaseList.AddTail method</span></span>

<span data-ttu-id="87531-104">El `AddTail` método anexa otra lista al final de esta lista.</span><span class="sxs-lookup"><span data-stu-id="87531-104">The `AddTail` method appends another list to the end of this list.</span></span>

## <a name="syntax"></a><span data-ttu-id="87531-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="87531-105">Syntax</span></span>


```C++
BOOL AddTail(
   CBaseList *pList
);
```



## <a name="parameters"></a><span data-ttu-id="87531-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="87531-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87531-107">*pList*</span><span class="sxs-lookup"><span data-stu-id="87531-107">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="87531-108">Puntero a la lista que se va a anexar.</span><span class="sxs-lookup"><span data-stu-id="87531-108">Pointer to the list to append.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87531-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="87531-109">Return value</span></span>

<span data-ttu-id="87531-110">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="87531-110">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="87531-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="87531-111">Remarks</span></span>

<span data-ttu-id="87531-112">Si se produce un error en el método, es posible que algunos elementos se hayan agregado a la lista.</span><span class="sxs-lookup"><span data-stu-id="87531-112">If the method fails, some items may have been added to the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="87531-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87531-113">Requirements</span></span>



| <span data-ttu-id="87531-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="87531-114">Requirement</span></span> | <span data-ttu-id="87531-115">Value</span><span class="sxs-lookup"><span data-stu-id="87531-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87531-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="87531-116">Header</span></span><br/>  | <dl> <span data-ttu-id="87531-117"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87531-117"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="87531-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="87531-118">Library</span></span><br/> | <dl> <span data-ttu-id="87531-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="87531-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87531-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="87531-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87531-121">**Clase CBaseList**</span><span class="sxs-lookup"><span data-stu-id="87531-121">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




