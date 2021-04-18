---
description: Método de constructor.
ms.assetid: 2d48cb66-45d2-4d2d-ba7e-ae759b6d2aa4
title: Constructor CBaseList. CBaseList (TCHAR *, INT) (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.CBaseList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9c947c8ffa6b61f919d03470b386ffa82945f3b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670939"
---
# <a name="cbaselistcbaselisttchar-int-constructor"></a><span data-ttu-id="1075d-103">Constructor CBaseList. CBaseList (TCHAR \* , int)</span><span class="sxs-lookup"><span data-stu-id="1075d-103">CBaseList.CBaseList(TCHAR\*, INT) constructor</span></span>

<span data-ttu-id="1075d-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="1075d-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1075d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1075d-105">Syntax</span></span>


```C++
CBaseList(
   TCHAR *pName,
   INT   iItems
);
```



## <a name="parameters"></a><span data-ttu-id="1075d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1075d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1075d-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="1075d-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="1075d-108">Puntero al nombre de la lista.</span><span class="sxs-lookup"><span data-stu-id="1075d-108">Pointer to the name of the list.</span></span>

</dd> <dt>

<span data-ttu-id="1075d-109">*iItems*</span><span class="sxs-lookup"><span data-stu-id="1075d-109">*iItems*</span></span> 
</dt> <dd>

<span data-ttu-id="1075d-110">Tamaño de la memoria caché de nodo.</span><span class="sxs-lookup"><span data-stu-id="1075d-110">Size of the node cache.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1075d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1075d-111">Remarks</span></span>

<span data-ttu-id="1075d-112">Por motivos de eficacia, la `CBaseList` clase mantiene una memoria caché de nodos de lista.</span><span class="sxs-lookup"><span data-stu-id="1075d-112">For efficiency, the `CBaseList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="1075d-113">Si conoce aproximadamente el número de elementos que contendrá la lista, use esta versión del constructor.</span><span class="sxs-lookup"><span data-stu-id="1075d-113">If you know approximately how many items the list will hold, use this version of the constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="1075d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1075d-114">Requirements</span></span>



| <span data-ttu-id="1075d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1075d-115">Requirement</span></span> | <span data-ttu-id="1075d-116">Value</span><span class="sxs-lookup"><span data-stu-id="1075d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1075d-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1075d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1075d-118"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1075d-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1075d-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1075d-119">Library</span></span><br/> | <dl> <span data-ttu-id="1075d-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1075d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1075d-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="1075d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1075d-122">**Clase CBaseList**</span><span class="sxs-lookup"><span data-stu-id="1075d-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




