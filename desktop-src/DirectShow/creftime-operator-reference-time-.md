---
description: El operador de tiempo de referencia \_ () convierte el objeto en un \_ tipo de datos de hora de referencia.
ms.assetid: 36f51e03-a458-46e6-9657-977b263c127f
title: Método CRefTime. Operator REFERENCE_TIME (Reftime. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a3ceeeb00ba1de4f305f87ef3fe15e70a8d91457
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680398"
---
# <a name="creftimeoperator-reference_time-method"></a><span data-ttu-id="59cf8-103">Método CRefTime. Operator REFERENCE \_ Time</span><span class="sxs-lookup"><span data-stu-id="59cf8-103">CRefTime.operator REFERENCE\_TIME method</span></span>

<span data-ttu-id="59cf8-104">El `REFERENCE_TIME()` operador convierte el objeto en un tipo de datos de [**\_ hora de referencia**](reference-time.md) .</span><span class="sxs-lookup"><span data-stu-id="59cf8-104">The `REFERENCE_TIME()` operator casts the object to a [**REFERENCE\_TIME**](reference-time.md) data type.</span></span>

## <a name="syntax"></a><span data-ttu-id="59cf8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="59cf8-105">Syntax</span></span>


```C++
REFERENCE_TIME operator REFERENCE_TIME() const;
```



## <a name="parameters"></a><span data-ttu-id="59cf8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="59cf8-106">Parameters</span></span>

<span data-ttu-id="59cf8-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="59cf8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="59cf8-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="59cf8-108">Return value</span></span>

<span data-ttu-id="59cf8-109">Devuelve el valor de [**CRefTime:: m \_ hora**](creftime-m-time.md).</span><span class="sxs-lookup"><span data-stu-id="59cf8-109">Returns the value of [**CRefTime::m\_time**](creftime-m-time.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="59cf8-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="59cf8-110">Remarks</span></span>

<span data-ttu-id="59cf8-111">En el ejemplo siguiente se muestra cómo usar este operador de conversión:</span><span class="sxs-lookup"><span data-stu-id="59cf8-111">The following example shows how to use this cast operator:</span></span>


```C++
CRefTime cRT(1000);
REFERENCE_TIME rt = (REFERENCE_TIME)cRT;
```



## <a name="requirements"></a><span data-ttu-id="59cf8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59cf8-112">Requirements</span></span>



| <span data-ttu-id="59cf8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="59cf8-113">Requirement</span></span> | <span data-ttu-id="59cf8-114">Value</span><span class="sxs-lookup"><span data-stu-id="59cf8-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59cf8-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59cf8-115">Header</span></span><br/>  | <dl> <span data-ttu-id="59cf8-116"><dt>Reftime. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59cf8-116"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="59cf8-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="59cf8-117">Library</span></span><br/> | <dl> <span data-ttu-id="59cf8-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="59cf8-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




