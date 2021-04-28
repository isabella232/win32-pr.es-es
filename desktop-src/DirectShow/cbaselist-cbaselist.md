---
description: 'Constructor CBaseList.CBaseList(TCHAR \* , INT): método constructor.'
ms.assetid: 2d48cb66-45d2-4d2d-ba7e-ae759b6d2aa4
title: Constructor CBaseList.CBaseList(TCHAR*, INT) (Wxlist.h)
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
ms.openlocfilehash: cf745e22ffccb342d945a024760f8c72fdb35ce9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099643"
---
# <a name="cbaselistcbaselisttchar-int-constructor"></a><span data-ttu-id="1e807-103">Constructor CBaseList.CBaseList(TCHAR, \* INT)</span><span class="sxs-lookup"><span data-stu-id="1e807-103">CBaseList.CBaseList(TCHAR\*, INT) constructor</span></span>

<span data-ttu-id="1e807-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="1e807-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e807-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e807-105">Syntax</span></span>


```C++
CBaseList(
   TCHAR *pName,
   INT   iItems
);
```



## <a name="parameters"></a><span data-ttu-id="1e807-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e807-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e807-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="1e807-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="1e807-108">Puntero al nombre de la lista.</span><span class="sxs-lookup"><span data-stu-id="1e807-108">Pointer to the name of the list.</span></span>

</dd> <dt>

<span data-ttu-id="1e807-109">*iItems*</span><span class="sxs-lookup"><span data-stu-id="1e807-109">*iItems*</span></span> 
</dt> <dd>

<span data-ttu-id="1e807-110">Tamaño de la caché del nodo.</span><span class="sxs-lookup"><span data-stu-id="1e807-110">Size of the node cache.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1e807-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1e807-111">Remarks</span></span>

<span data-ttu-id="1e807-112">Para mejorar la eficacia, `CBaseList` la clase mantiene una caché de nodos de lista.</span><span class="sxs-lookup"><span data-stu-id="1e807-112">For efficiency, the `CBaseList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="1e807-113">Si sabe aproximadamente cuántos elementos contendrán la lista, use esta versión del constructor.</span><span class="sxs-lookup"><span data-stu-id="1e807-113">If you know approximately how many items the list will hold, use this version of the constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e807-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e807-114">Requirements</span></span>



| <span data-ttu-id="1e807-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e807-115">Requirement</span></span> | <span data-ttu-id="1e807-116">Value</span><span class="sxs-lookup"><span data-stu-id="1e807-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e807-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1e807-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1e807-118"><dt>Wxlist.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="1e807-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1e807-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1e807-119">Library</span></span><br/> | <dl> <span data-ttu-id="1e807-120"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1e807-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e807-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="1e807-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e807-122">**CBaseList (clase)**</span><span class="sxs-lookup"><span data-stu-id="1e807-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




