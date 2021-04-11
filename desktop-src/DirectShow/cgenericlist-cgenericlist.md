---
description: Obtenga información sobre el método de constructor para CGenericList. CGenericList (Wxlist. h). Este método usa los parámetros ' pName ' y ' iItems '.
ms.assetid: 2258ecd6-7594-4ff8-961b-9e5e1ae9ff82
title: Constructor CGenericList. CGenericList (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.CGenericList
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77a3dd932872b9d96c754ac5b1db184dcf99cf03
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104362839"
---
# <a name="cgenericlistcgenericlist-constructor-wxlisth---pname-iitems-parameters"></a><span data-ttu-id="b84da-104">Constructor CGenericList. CGenericList (Wxlist. h): parámetros pName, iItems</span><span class="sxs-lookup"><span data-stu-id="b84da-104">CGenericList.CGenericList constructor (Wxlist.h) - pName, iItems parameters</span></span>

<span data-ttu-id="b84da-105">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="b84da-105">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b84da-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b84da-106">Syntax</span></span>


```C++
CGenericList(
   TCHAR *pName,
   INT   iItems,
   BOOL  bLock,
   BOOL  bAlert
);
```



## <a name="parameters"></a><span data-ttu-id="b84da-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b84da-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b84da-108">*pName*</span><span class="sxs-lookup"><span data-stu-id="b84da-108">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="b84da-109">Puntero al nombre de la lista.</span><span class="sxs-lookup"><span data-stu-id="b84da-109">Pointer to the name of the list.</span></span>

</dd> <dt>

<span data-ttu-id="b84da-110">*iItems*</span><span class="sxs-lookup"><span data-stu-id="b84da-110">*iItems*</span></span> 
</dt> <dd>

<span data-ttu-id="b84da-111">Tamaño de la memoria caché de nodo.</span><span class="sxs-lookup"><span data-stu-id="b84da-111">Size of the node cache.</span></span>

</dd> <dt>

<span data-ttu-id="b84da-112">*Sin*</span><span class="sxs-lookup"><span data-stu-id="b84da-112">*bLock*</span></span> 
</dt> <dd>

<span data-ttu-id="b84da-113">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b84da-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="b84da-114">*bAlert*</span><span class="sxs-lookup"><span data-stu-id="b84da-114">*bAlert*</span></span> 
</dt> <dd>

<span data-ttu-id="b84da-115">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b84da-115">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b84da-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b84da-116">Remarks</span></span>

<span data-ttu-id="b84da-117">Por motivos de eficacia, la `CGenericList` clase mantiene una memoria caché de nodos de lista.</span><span class="sxs-lookup"><span data-stu-id="b84da-117">For efficiency, the `CGenericList` class maintains a cache of list nodes.</span></span> <span data-ttu-id="b84da-118">Si conoce aproximadamente el número de elementos que contendrá la lista, use esta versión del constructor.</span><span class="sxs-lookup"><span data-stu-id="b84da-118">If you know approximately how many items the list will hold, use this version of the constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="b84da-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b84da-119">Requirements</span></span>

| <span data-ttu-id="b84da-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b84da-120">Requirement</span></span> | <span data-ttu-id="b84da-121">Value</span><span class="sxs-lookup"><span data-stu-id="b84da-121">Value</span></span> |
|-|-|
| <span data-ttu-id="b84da-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b84da-122">Header</span></span> | <span data-ttu-id="b84da-123">Wxlist. h (incluir streams. h)</span><span class="sxs-lookup"><span data-stu-id="b84da-123">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="b84da-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b84da-124">Library</span></span>| <span data-ttu-id="b84da-125">Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración)</span><span class="sxs-lookup"><span data-stu-id="b84da-125">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="b84da-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="b84da-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b84da-127">**Clase CGenericList**</span><span class="sxs-lookup"><span data-stu-id="b84da-127">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




