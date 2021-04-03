---
description: El método AddHead agrega un elemento al principio de la lista.
ms.assetid: 8f0012b7-bbc2-407c-ae5a-9843c2f692dc
title: 'Método CGenericList. AddHead (Wxlist. h): parámetro pObj'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddHead
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62a32eb177c80d10a876a4b163c8a1609104fbea
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104083824"
---
# <a name="cgenericlistaddhead-method-wxlisth---pobj-parameter"></a><span data-ttu-id="65acd-103">Método CGenericList. AddHead (Wxlist. h): parámetro pObj</span><span class="sxs-lookup"><span data-stu-id="65acd-103">CGenericList.AddHead method (Wxlist.h) - pObj parameter</span></span>

<span data-ttu-id="65acd-104">El `AddHead` método agrega un elemento al principio de la lista.</span><span class="sxs-lookup"><span data-stu-id="65acd-104">The `AddHead` method adds an item to the front of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="65acd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65acd-105">Syntax</span></span>


```C++
POSITION AddHead(
   OBJECT *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="65acd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65acd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65acd-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="65acd-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="65acd-108">Puntero a un objeto de tipo **Object** (el tipo de plantilla).</span><span class="sxs-lookup"><span data-stu-id="65acd-108">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65acd-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65acd-109">Return value</span></span>

<span data-ttu-id="65acd-110">Devuelve un valor de posición que indica la nueva posición del encabezado.</span><span class="sxs-lookup"><span data-stu-id="65acd-110">Returns a POSITION value indicating the new head position.</span></span> <span data-ttu-id="65acd-111">Si se produce un error en el método, el valor devuelto es **null**.</span><span class="sxs-lookup"><span data-stu-id="65acd-111">If the method fails, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="65acd-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65acd-112">Requirements</span></span>

| <span data-ttu-id="65acd-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="65acd-113">Requirement</span></span> | <span data-ttu-id="65acd-114">Value</span><span class="sxs-lookup"><span data-stu-id="65acd-114">Value</span></span> |
|-|-|
| <span data-ttu-id="65acd-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65acd-115">Header</span></span> | <span data-ttu-id="65acd-116">Wxlist. h (incluir streams. h)</span><span class="sxs-lookup"><span data-stu-id="65acd-116">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="65acd-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="65acd-117">Library</span></span>| <span data-ttu-id="65acd-118">Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración)</span><span class="sxs-lookup"><span data-stu-id="65acd-118">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="65acd-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="65acd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65acd-120">**Clase CGenericList**</span><span class="sxs-lookup"><span data-stu-id="65acd-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




