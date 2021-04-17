---
description: El método Addtail (anexa un elemento al final de la lista.
ms.assetid: e365a23e-7447-42ec-b836-21dd68962db1
title: 'Método CGenericList. Addtail ((Wxlist. h): parámetro pObj'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CGenericList.AddTail
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f1e7cd3d8758107b9529114a75b3a90527937c6
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105670273"
---
# <a name="cgenericlistaddtail-method-wxlisth---pobj-parameter"></a><span data-ttu-id="b9841-103">Método CGenericList. Addtail ((Wxlist. h): parámetro pObj</span><span class="sxs-lookup"><span data-stu-id="b9841-103">CGenericList.AddTail method (Wxlist.h) - pObj parameter</span></span>

<span data-ttu-id="b9841-104">El `AddTail` método anexa un elemento al final de la lista.</span><span class="sxs-lookup"><span data-stu-id="b9841-104">The `AddTail` method appends an item to the end of the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9841-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9841-105">Syntax</span></span>


```C++
POSITION AddTail(
   OBJECT *pObj
);
```



## <a name="parameters"></a><span data-ttu-id="b9841-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b9841-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9841-107">*pObj*</span><span class="sxs-lookup"><span data-stu-id="b9841-107">*pObj*</span></span> 
</dt> <dd>

<span data-ttu-id="b9841-108">Puntero a un objeto de tipo **Object** (el tipo de plantilla).</span><span class="sxs-lookup"><span data-stu-id="b9841-108">Pointer to an object of type **OBJECT** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9841-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9841-109">Return value</span></span>

<span data-ttu-id="b9841-110">Devuelve un valor de posición para la nueva posición de la cola.</span><span class="sxs-lookup"><span data-stu-id="b9841-110">Returns a POSITION value for the new tail position.</span></span> <span data-ttu-id="b9841-111">Si se produce un error en el método, devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="b9841-111">If the method fails, it returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9841-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9841-112">Requirements</span></span>

| <span data-ttu-id="b9841-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9841-113">Requirement</span></span> | <span data-ttu-id="b9841-114">Value</span><span class="sxs-lookup"><span data-stu-id="b9841-114">Value</span></span> |
|-|-|
| <span data-ttu-id="b9841-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b9841-115">Header</span></span> | <span data-ttu-id="b9841-116">Wxlist. h (incluir streams. h)</span><span class="sxs-lookup"><span data-stu-id="b9841-116">Wxlist.h (include Streams.h)</span></span> |
| <span data-ttu-id="b9841-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b9841-117">Library</span></span>| <span data-ttu-id="b9841-118">Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración)</span><span class="sxs-lookup"><span data-stu-id="b9841-118">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="b9841-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9841-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9841-120">**Clase CGenericList**</span><span class="sxs-lookup"><span data-stu-id="b9841-120">**CGenericList Class**</span></span>](cgenericlist.md)
</dt> </dl>

 

 




