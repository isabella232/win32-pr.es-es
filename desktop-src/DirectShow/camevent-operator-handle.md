---
description: Recupera el identificador del evento. Este operador no se admite como un valor L.
ms.assetid: 9000d6d1-bbca-44ac-8808-0b3b827086c5
title: Método de identificador CAMEvent. Operator (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.operator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72193e89f415aabebfea4288fcdb986ccf8d73bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670707"
---
# <a name="cameventoperator-handle-method"></a><span data-ttu-id="38b4f-104">CAMEvent. Operator (método de identificador)</span><span class="sxs-lookup"><span data-stu-id="38b4f-104">CAMEvent.operator HANDLE method</span></span>

<span data-ttu-id="38b4f-105">Recupera el identificador del evento.</span><span class="sxs-lookup"><span data-stu-id="38b4f-105">Retrieves the event handle.</span></span> <span data-ttu-id="38b4f-106">Este operador no se admite como un valor L.</span><span class="sxs-lookup"><span data-stu-id="38b4f-106">This operator is not supported as an L-value.</span></span>

## <a name="syntax"></a><span data-ttu-id="38b4f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38b4f-107">Syntax</span></span>


```C++
 operator HANDLE() const;
```



## <a name="parameters"></a><span data-ttu-id="38b4f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="38b4f-108">Parameters</span></span>

<span data-ttu-id="38b4f-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="38b4f-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="38b4f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="38b4f-110">Return value</span></span>

<span data-ttu-id="38b4f-111">Devuelve la variable miembro [**CAMEvent:: m \_ hEvent**](camevent-m-hevent.md) .</span><span class="sxs-lookup"><span data-stu-id="38b4f-111">Returns the [**CAMEvent::m\_hEvent**](camevent-m-hevent.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="38b4f-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38b4f-112">Requirements</span></span>



| <span data-ttu-id="38b4f-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="38b4f-113">Requirement</span></span> | <span data-ttu-id="38b4f-114">Value</span><span class="sxs-lookup"><span data-stu-id="38b4f-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38b4f-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38b4f-115">Header</span></span><br/>  | <dl> <span data-ttu-id="38b4f-116"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="38b4f-116"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="38b4f-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="38b4f-117">Library</span></span><br/> | <dl> <span data-ttu-id="38b4f-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="38b4f-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38b4f-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="38b4f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38b4f-120">**Clase CAMEvent**</span><span class="sxs-lookup"><span data-stu-id="38b4f-120">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




