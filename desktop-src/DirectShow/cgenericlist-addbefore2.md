---
description: El método AddBefore inserta una lista antes de la posición especificada. Este método usa los parámetros ' pos ' y ' plist '.
ms.assetid: 0fdb2a59-d9de-4dbb-8536-8e10726201d0
title: 'Método CGenericList. AddBefore (Wxlist. h): parámetros de pos y plist'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddBefore
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6aa6aa71b1738a815beee9cdc7c0f47118eb27f
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "103821586"
---
# <a name="cgenericlistaddbefore-method-wxlisth---pos-plist-parameters"></a><span data-ttu-id="ed1b2-104">Método CGenericList. AddBefore (Wxlist. h): parámetros de pos y plist</span><span class="sxs-lookup"><span data-stu-id="ed1b2-104">CGenericList.AddBefore method (Wxlist.h) - pos, pList parameters</span></span>

<span data-ttu-id="ed1b2-105">El `AddBefore` método inserta una lista antes de la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="ed1b2-105">The `AddBefore` method inserts a list before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed1b2-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ed1b2-106">Syntax</span></span>


```C++
BOOL AddBefore(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a><span data-ttu-id="ed1b2-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ed1b2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed1b2-108">*pos*</span><span class="sxs-lookup"><span data-stu-id="ed1b2-108">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="ed1b2-109">Posición en la que se va a insertar la lista.</span><span class="sxs-lookup"><span data-stu-id="ed1b2-109">Position to insert the list.</span></span> <span data-ttu-id="ed1b2-110">La lista se inserta antes de esta posición.</span><span class="sxs-lookup"><span data-stu-id="ed1b2-110">The list is inserted before this position.</span></span>

</dd> <dt>

<span data-ttu-id="ed1b2-111">*pList*</span><span class="sxs-lookup"><span data-stu-id="ed1b2-111">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="ed1b2-112">Puntero a la lista que se va a insertar.</span><span class="sxs-lookup"><span data-stu-id="ed1b2-112">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed1b2-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ed1b2-113">Return value</span></span>

<span data-ttu-id="ed1b2-114">Devuelve **true si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="ed1b2-114">Returns **TRUE** if successful.</span></span> <span data-ttu-id="ed1b2-115">De lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="ed1b2-115">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed1b2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed1b2-116">Requirements</span></span>

| <span data-ttu-id="ed1b2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed1b2-117">Requirement</span></span> | <span data-ttu-id="ed1b2-118">Value</span><span class="sxs-lookup"><span data-stu-id="ed1b2-118">Value</span></span> |
|-|-|
| <span data-ttu-id="ed1b2-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ed1b2-119">Header</span></span> | <span data-ttu-id="ed1b2-120">Wxlist. h (incluir streams. h)</span><span class="sxs-lookup"><span data-stu-id="ed1b2-120">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="ed1b2-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ed1b2-121">Library</span></span>| <span data-ttu-id="ed1b2-122">Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración)</span><span class="sxs-lookup"><span data-stu-id="ed1b2-122">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="ed1b2-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="ed1b2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed1b2-124">**Clase CGenericList**</span><span class="sxs-lookup"><span data-stu-id="ed1b2-124">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




