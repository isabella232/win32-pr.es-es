---
description: El método AddBefore inserta un elemento antes de la posición especificada. Este método usa los parámetros ' p ' y ' pObj '.
ms.assetid: ec10fd08-6bb9-4357-830c-78b3d3a32e03
title: Método CGenericList. AddBefore (Wxlist. h)-p, parámetros pObj
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
ms.openlocfilehash: a79c0edb8938e3d3d5a89b4a84a418846b9f1986
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "104004000"
---
# <a name="cgenericlistaddbefore-method-wxlisth---p-pobj-parameters"></a><span data-ttu-id="95916-104">Método CGenericList. AddBefore (Wxlist. h)-p, parámetros pObj</span><span class="sxs-lookup"><span data-stu-id="95916-104">CGenericList.AddBefore method (Wxlist.h) - p, pObj parameters</span></span>

<span data-ttu-id="95916-105">El `AddBefore` método inserta un elemento antes de la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="95916-105">The `AddBefore` method inserts an item before the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="95916-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95916-106">Syntax</span></span>


```C++
POSITION AddBefore(
   POSITION p,
   OBJECT   *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="95916-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95916-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95916-108">*m*</span><span class="sxs-lookup"><span data-stu-id="95916-108">*p*</span></span> 
</dt> <dd>

<span data-ttu-id="95916-109">Posición antes de la que se va a insertar la lista.</span><span class="sxs-lookup"><span data-stu-id="95916-109">Position before which to insert the list.</span></span> <span data-ttu-id="95916-110">Si *p* es **null**, este método agrega el elemento al final de la lista.</span><span class="sxs-lookup"><span data-stu-id="95916-110">If *p* is **NULL**, this method adds the item to the tail of the list.</span></span>

</dd> <dt>

<span data-ttu-id="95916-111">*pObj*</span><span class="sxs-lookup"><span data-stu-id="95916-111">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="95916-112">Puntero a un objeto de tipo **Object** (el tipo de plantilla).</span><span class="sxs-lookup"><span data-stu-id="95916-112">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95916-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="95916-113">Return value</span></span>

<span data-ttu-id="95916-114">Devuelve el indicador de posición del elemento insertado.</span><span class="sxs-lookup"><span data-stu-id="95916-114">Returns the position indicator for the inserted item.</span></span>

## <a name="requirements"></a><span data-ttu-id="95916-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95916-115">Requirements</span></span>

| <span data-ttu-id="95916-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="95916-116">Requirement</span></span> | <span data-ttu-id="95916-117">Value</span><span class="sxs-lookup"><span data-stu-id="95916-117">Value</span></span> |
|-|-|
| <span data-ttu-id="95916-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="95916-118">Header</span></span> | <span data-ttu-id="95916-119">Wxlist. h (incluir streams. h)</span><span class="sxs-lookup"><span data-stu-id="95916-119">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="95916-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="95916-120">Library</span></span>| <span data-ttu-id="95916-121">Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración)</span><span class="sxs-lookup"><span data-stu-id="95916-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="95916-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="95916-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95916-123">**Clase CGenericList**</span><span class="sxs-lookup"><span data-stu-id="95916-123">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




