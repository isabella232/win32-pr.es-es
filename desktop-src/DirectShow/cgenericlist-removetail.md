---
description: El método RemoveTail quita el último elemento de la lista.
ms.assetid: 377af676-8042-430e-87a6-b41c00482a90
title: Método CGenericList. RemoveTail (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.RemoveTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7b98187c663f643acdce28b4f12ebc37b1d4c25
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660834"
---
# <a name="cgenericlistremovetail-method"></a><span data-ttu-id="8c510-103">CGenericList. RemoveTail, método</span><span class="sxs-lookup"><span data-stu-id="8c510-103">CGenericList.RemoveTail method</span></span>

<span data-ttu-id="8c510-104">El `RemoveTail` método quita el último elemento de la lista.</span><span class="sxs-lookup"><span data-stu-id="8c510-104">The `RemoveTail` method removes the last item in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c510-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c510-105">Syntax</span></span>


```C++
OBJECT* RemoveTail();
```



## <a name="parameters"></a><span data-ttu-id="8c510-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c510-106">Parameters</span></span>

<span data-ttu-id="8c510-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8c510-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c510-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c510-108">Return value</span></span>

<span data-ttu-id="8c510-109">Devuelve un puntero a un objeto de tipo **Object** (el tipo de plantilla) o **null** si la lista está vacía.</span><span class="sxs-lookup"><span data-stu-id="8c510-109">Returns a pointer to an object of type **OBJECT** (the template type), or **NULL** if the list is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c510-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c510-110">Remarks</span></span>

<span data-ttu-id="8c510-111">Este método elimina el nodo de lista, pero no el elemento contenido en el nodo.</span><span class="sxs-lookup"><span data-stu-id="8c510-111">This method deletes the list node, but not the item that is contained in the node.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c510-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c510-112">Requirements</span></span>



| <span data-ttu-id="8c510-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c510-113">Requirement</span></span> | <span data-ttu-id="8c510-114">Value</span><span class="sxs-lookup"><span data-stu-id="8c510-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c510-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c510-115">Header</span></span><br/>  | <dl> <span data-ttu-id="8c510-116"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c510-116"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="8c510-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8c510-117">Library</span></span><br/> | <dl> <span data-ttu-id="8c510-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="8c510-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c510-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c510-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c510-120">**Clase CGenericList**</span><span class="sxs-lookup"><span data-stu-id="8c510-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




