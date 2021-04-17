---
description: El método Find recupera la primera posición que contiene el elemento especificado.
ms.assetid: 8e2a3e5d-96e6-4f40-8e2a-4dc8c21088cd
title: Método CGenericList. Find (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.Find
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a21f16e25d8a2ebba4494a850bc456a7b579f2a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660844"
---
# <a name="cgenericlistfind-method"></a><span data-ttu-id="40c99-103">CGenericList. Find (método)</span><span class="sxs-lookup"><span data-stu-id="40c99-103">CGenericList.Find method</span></span>

<span data-ttu-id="40c99-104">El `Find` método recupera la primera posición que contiene el elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="40c99-104">The `Find` method retrieves the first position that holds the specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="40c99-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="40c99-105">Syntax</span></span>


```C++
POSITION Find(
   OBJECT *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="40c99-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="40c99-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40c99-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="40c99-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="40c99-108">Puntero a un objeto de tipo **Object** (el tipo de plantilla).</span><span class="sxs-lookup"><span data-stu-id="40c99-108">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40c99-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="40c99-109">Return value</span></span>

<span data-ttu-id="40c99-110">Devuelve un valor de posición o **null** si el elemento no está en la lista.</span><span class="sxs-lookup"><span data-stu-id="40c99-110">Returns a POSITION value, or **NULL** if the item is not in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="40c99-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40c99-111">Requirements</span></span>



| <span data-ttu-id="40c99-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="40c99-112">Requirement</span></span> | <span data-ttu-id="40c99-113">Value</span><span class="sxs-lookup"><span data-stu-id="40c99-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40c99-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40c99-114">Header</span></span><br/>  | <dl> <span data-ttu-id="40c99-115"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="40c99-115"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="40c99-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="40c99-116">Library</span></span><br/> | <dl> <span data-ttu-id="40c99-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="40c99-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40c99-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="40c99-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40c99-119">**Clase CGenericList**</span><span class="sxs-lookup"><span data-stu-id="40c99-119">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




