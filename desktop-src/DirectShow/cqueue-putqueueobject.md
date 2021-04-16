---
description: Coloca un elemento en la cola.
ms.assetid: 8ac41d80-e7d5-4b3f-9f09-c3d39c94c490
title: Método CQueue. PutQueueObject (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.PutQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5371c843bb348f50539535a3df9a0f6aed00893e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671419"
---
# <a name="cqueueputqueueobject-method"></a><span data-ttu-id="3fef5-103">CQueue. PutQueueObject, método</span><span class="sxs-lookup"><span data-stu-id="3fef5-103">CQueue.PutQueueObject method</span></span>

<span data-ttu-id="3fef5-104">Coloca un elemento en la cola.</span><span class="sxs-lookup"><span data-stu-id="3fef5-104">Puts an item onto the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fef5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3fef5-105">Syntax</span></span>


```C++
void PutQueueObject(
   T object
);
```



## <a name="parameters"></a><span data-ttu-id="3fef5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3fef5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fef5-107">*object*</span><span class="sxs-lookup"><span data-stu-id="3fef5-107">*object*</span></span> 
</dt> <dd>

<span data-ttu-id="3fef5-108">Objeto de tipo **T** (el tipo de plantilla).</span><span class="sxs-lookup"><span data-stu-id="3fef5-108">Object of type **T** (the template type).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fef5-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3fef5-109">Return value</span></span>

<span data-ttu-id="3fef5-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3fef5-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fef5-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3fef5-111">Remarks</span></span>

<span data-ttu-id="3fef5-112">Este método se bloquea hasta que haya espacio en la cola del elemento.</span><span class="sxs-lookup"><span data-stu-id="3fef5-112">This method blocks until there is space in the queue for the item.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fef5-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fef5-113">Requirements</span></span>



| <span data-ttu-id="3fef5-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fef5-114">Requirement</span></span> | <span data-ttu-id="3fef5-115">Value</span><span class="sxs-lookup"><span data-stu-id="3fef5-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fef5-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3fef5-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3fef5-117"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3fef5-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3fef5-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3fef5-118">Library</span></span><br/> | <dl> <span data-ttu-id="3fef5-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3fef5-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fef5-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="3fef5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fef5-121">**Clase CQueue**</span><span class="sxs-lookup"><span data-stu-id="3fef5-121">**CQueue Class**</span></span>](cqueue.md)
</dt> </dl>

 

 




