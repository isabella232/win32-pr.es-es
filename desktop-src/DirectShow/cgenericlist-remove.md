---
description: El método Remove quita el elemento en la posición especificada.
ms.assetid: a7b8f6fb-f13a-4c24-aa18-463446602e29
title: Método CGenericList. Remove (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d5fc3d0cd76cd78c83fa210d8b91ba97b93b92f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660836"
---
# <a name="cgenericlistremove-method"></a><span data-ttu-id="f7d8d-103">CGenericList. Remove (método)</span><span class="sxs-lookup"><span data-stu-id="f7d8d-103">CGenericList.Remove method</span></span>

<span data-ttu-id="f7d8d-104">El `Remove` método quita el elemento en la posición especificada.</span><span class="sxs-lookup"><span data-stu-id="f7d8d-104">The `Remove` method removes the item at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7d8d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f7d8d-105">Syntax</span></span>


```C++
OBJECT* Remove(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="f7d8d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f7d8d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7d8d-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="f7d8d-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="f7d8d-108">Valor de posición que indica el elemento que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="f7d8d-108">POSITION value indicating the item to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7d8d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f7d8d-109">Return value</span></span>

<span data-ttu-id="f7d8d-110">Devuelve un puntero a un objeto de tipo **Object** (el tipo de plantilla).</span><span class="sxs-lookup"><span data-stu-id="f7d8d-110">Returns a pointer to an object of type **OBJECT** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="f7d8d-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f7d8d-111">Remarks</span></span>

<span data-ttu-id="f7d8d-112">Este método elimina el nodo de la lista, pero no elimina el elemento contenido en ese nodo.</span><span class="sxs-lookup"><span data-stu-id="f7d8d-112">This method deletes the node from the list, but does not delete the item contained in that node.</span></span>

<span data-ttu-id="f7d8d-113">Si *pos* es **null**, el método devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="f7d8d-113">If *pos* is **NULL**, the method returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7d8d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7d8d-114">Requirements</span></span>



| <span data-ttu-id="f7d8d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7d8d-115">Requirement</span></span> | <span data-ttu-id="f7d8d-116">Value</span><span class="sxs-lookup"><span data-stu-id="f7d8d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7d8d-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f7d8d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f7d8d-118"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f7d8d-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f7d8d-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f7d8d-119">Library</span></span><br/> | <dl> <span data-ttu-id="f7d8d-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f7d8d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7d8d-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7d8d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7d8d-122">**Clase CGenericList**</span><span class="sxs-lookup"><span data-stu-id="f7d8d-122">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




