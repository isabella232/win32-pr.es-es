---
description: El método AddAfter inserta una lista después de la posición especificada y usa los parámetros ' pos ' y ' plist '.
ms.assetid: 99214667-8478-40e5-b55b-6ac47b1fb4d2
title: 'Método CGenericList. AddAfter (Wxlist. h): parámetros de pos y plist'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddAfter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6bbe26e98acc999f067a7b0e96c3716e7e0c0c0
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104548166"
---
# <a name="cgenericlistaddafter-method-wxlisth---pos-plist-parameters"></a><span data-ttu-id="39243-103">Método CGenericList. AddAfter (Wxlist. h): parámetros de pos y plist</span><span class="sxs-lookup"><span data-stu-id="39243-103">CGenericList.AddAfter method (Wxlist.h) - pos, plist parameters</span></span>

<span data-ttu-id="39243-104">El `AddAfter` método inserta una lista después de la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="39243-104">The `AddAfter` method inserts a list after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="39243-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39243-105">Syntax</span></span>


```C++
BOOL AddAfter(
   POSITION             pos,
   CGenericList<OBJECT> *pList
);
```



## <a name="parameters"></a><span data-ttu-id="39243-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39243-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39243-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="39243-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="39243-108">Posición en la que se va a insertar la lista.</span><span class="sxs-lookup"><span data-stu-id="39243-108">Position to insert the list.</span></span> <span data-ttu-id="39243-109">La lista se inserta después de esta posición.</span><span class="sxs-lookup"><span data-stu-id="39243-109">The list is inserted after this position.</span></span>

</dd> <dt>

<span data-ttu-id="39243-110">*pList*</span><span class="sxs-lookup"><span data-stu-id="39243-110">*pList*</span></span> 
</dt> <dd>

<span data-ttu-id="39243-111">Puntero a la lista que se va a insertar.</span><span class="sxs-lookup"><span data-stu-id="39243-111">Pointer to the list to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39243-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39243-112">Return value</span></span>

<span data-ttu-id="39243-113">Devuelve **true** si es correcto, o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="39243-113">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="39243-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39243-114">Requirements</span></span>

| <span data-ttu-id="39243-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="39243-115">Requirement</span></span> | <span data-ttu-id="39243-116">Value</span><span class="sxs-lookup"><span data-stu-id="39243-116">Value</span></span> |
|-|-|
| <span data-ttu-id="39243-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39243-117">Header</span></span> | <span data-ttu-id="39243-118">Wxlist. h (incluir streams. h)</span><span class="sxs-lookup"><span data-stu-id="39243-118">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="39243-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="39243-119">Library</span></span>| <span data-ttu-id="39243-120">Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración)</span><span class="sxs-lookup"><span data-stu-id="39243-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="39243-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="39243-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39243-122">**Clase CGenericList**</span><span class="sxs-lookup"><span data-stu-id="39243-122">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




