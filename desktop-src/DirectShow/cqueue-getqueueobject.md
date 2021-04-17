---
description: Recupera el siguiente elemento de la cola.
ms.assetid: 406ae640-5903-427d-91f9-8b01beb1aaa7
title: Método CQueue. GetQueueObject (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue.GetQueueObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3ae68c0564c7f76f38e91b7d27c8c3deb5ef2b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680866"
---
# <a name="cqueuegetqueueobject-method"></a><span data-ttu-id="9460c-103">CQueue. GetQueueObject, método</span><span class="sxs-lookup"><span data-stu-id="9460c-103">CQueue.GetQueueObject method</span></span>

<span data-ttu-id="9460c-104">Recupera el siguiente elemento de la cola.</span><span class="sxs-lookup"><span data-stu-id="9460c-104">Retrieves the next item from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="9460c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9460c-105">Syntax</span></span>


```C++
T GetQueueObject();
```



## <a name="parameters"></a><span data-ttu-id="9460c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9460c-106">Parameters</span></span>

<span data-ttu-id="9460c-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9460c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9460c-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9460c-108">Return value</span></span>

<span data-ttu-id="9460c-109">Devuelve un objeto de tipo **T** (el tipo de plantilla).</span><span class="sxs-lookup"><span data-stu-id="9460c-109">Returns an object of type **T** (the template type).</span></span>

## <a name="remarks"></a><span data-ttu-id="9460c-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9460c-110">Remarks</span></span>

<span data-ttu-id="9460c-111">Este método se bloquea hasta que un elemento esté disponible en la cola.</span><span class="sxs-lookup"><span data-stu-id="9460c-111">This method blocks until an item is available on the queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="9460c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9460c-112">Requirements</span></span>



| <span data-ttu-id="9460c-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9460c-113">Requirement</span></span> | <span data-ttu-id="9460c-114">Value</span><span class="sxs-lookup"><span data-stu-id="9460c-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9460c-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9460c-115">Header</span></span><br/>  | <dl> <span data-ttu-id="9460c-116"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9460c-116"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9460c-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9460c-117">Library</span></span><br/> | <dl> <span data-ttu-id="9460c-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9460c-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9460c-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="9460c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9460c-120">**Clase CQueue**</span><span class="sxs-lookup"><span data-stu-id="9460c-120">**CQueue Class**</span></span>](cqueue.md)
</dt> </dl>

 

 




