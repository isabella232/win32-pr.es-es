---
description: El método AddAfter inserta un elemento después de la posición especificada y usa los parámetros ' p ' y ' pObj '.
ms.assetid: 3e1f27c5-3e04-424a-8fe3-9bfde4e3824b
title: Método CGenericList. AddAfter (Wxlist. h)-p, parámetros pObj
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
ms.openlocfilehash: fbb9553310a8ba817f90464d90226eb36371505e
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104362830"
---
# <a name="cgenericlistaddafter-method-wxlisth---p-pobj-parameters"></a><span data-ttu-id="bba51-103">Método CGenericList. AddAfter (Wxlist. h)-p, parámetros pObj</span><span class="sxs-lookup"><span data-stu-id="bba51-103">CGenericList.AddAfter method (Wxlist.h) - p, pObj parameters</span></span>

<span data-ttu-id="bba51-104">El `AddAfter` método inserta un elemento después de la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="bba51-104">The `AddAfter` method inserts an item after the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="bba51-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bba51-105">Syntax</span></span>


```C++
POSITION AddAfter(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="bba51-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bba51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bba51-107">*m*</span><span class="sxs-lookup"><span data-stu-id="bba51-107">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="bba51-108">Posición detrás de la que se va a agregar el elemento.</span><span class="sxs-lookup"><span data-stu-id="bba51-108">Position after which to add the item.</span></span> <span data-ttu-id="bba51-109">Si *p* es **null**, el método agrega el elemento al encabezado de la lista.</span><span class="sxs-lookup"><span data-stu-id="bba51-109">If *p* is **NULL**, the method adds the item to the head of the list.</span></span>

</dd> <dt>

<span data-ttu-id="bba51-110">*pObj*</span><span class="sxs-lookup"><span data-stu-id="bba51-110">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="bba51-111">Puntero a un objeto de tipo **Object** (el tipo de plantilla).</span><span class="sxs-lookup"><span data-stu-id="bba51-111">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bba51-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bba51-112">Return value</span></span>

<span data-ttu-id="bba51-113">Devuelve el indicador de posición del elemento insertado.</span><span class="sxs-lookup"><span data-stu-id="bba51-113">Returns the position indicator of the inserted item.</span></span>

## <a name="requirements"></a><span data-ttu-id="bba51-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bba51-114">Requirements</span></span>

| <span data-ttu-id="bba51-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bba51-115">Requirement</span></span> | <span data-ttu-id="bba51-116">Value</span><span class="sxs-lookup"><span data-stu-id="bba51-116">Value</span></span> |
|-|-|
| <span data-ttu-id="bba51-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bba51-117">Header</span></span> | <span data-ttu-id="bba51-118">Wxlist. h (incluir streams. h)</span><span class="sxs-lookup"><span data-stu-id="bba51-118">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="bba51-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bba51-119">Library</span></span>| <span data-ttu-id="bba51-120">Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración)</span><span class="sxs-lookup"><span data-stu-id="bba51-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="bba51-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="bba51-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bba51-122">**Clase CGenericList**</span><span class="sxs-lookup"><span data-stu-id="bba51-122">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




