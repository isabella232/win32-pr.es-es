---
description: El operador asigna una nueva hora de referencia y usa el parámetro ' RT [Ref] '.
ms.assetid: e3a005c0-95d5-41e0-80bb-e70399a50dca
title: COARefTime. Operator = Method (Ctlutil. h)-RT [Ref] parámetro
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bad1e0d7ee63fe9bcfa7fc1664a7349e787d9927
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/19/2021
ms.locfileid: "105678861"
---
# <a name="coareftimeoperator-method-ctlutilh---rt-ref-parameter"></a><span data-ttu-id="499f2-103">COARefTime. Operator = Method (Ctlutil. h)-RT [Ref] parámetro</span><span class="sxs-lookup"><span data-stu-id="499f2-103">COARefTime.operator= method (Ctlutil.h) - rt [ref] parameter</span></span>

<span data-ttu-id="499f2-104">Este operador asigna una nueva hora de referencia.</span><span class="sxs-lookup"><span data-stu-id="499f2-104">This operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="499f2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="499f2-105">Syntax</span></span>


```C++
COARefTime& operator=(
  [ref] const REFERENCE_TIME &rt
);
```



## <a name="parameters"></a><span data-ttu-id="499f2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="499f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="499f2-107">*RT* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="499f2-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="499f2-108">Referencia a un valor de [**\_ tiempo de referencia**](reference-time.md) que especifica el nuevo tiempo de referencia en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="499f2-108">Reference to a [**REFERENCE\_TIME**](reference-time.md) value that specifies the new reference time in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="499f2-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="499f2-109">Return value</span></span>

<span data-ttu-id="499f2-110">Devuelve una referencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="499f2-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="499f2-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="499f2-111">Requirements</span></span>

| <span data-ttu-id="499f2-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="499f2-112">Requirement</span></span>                    | <span data-ttu-id="499f2-113">Value</span><span class="sxs-lookup"><span data-stu-id="499f2-113">Value</span></span>                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="499f2-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="499f2-114">Header</span></span>  | <span data-ttu-id="499f2-115">Ctlutil. h (incluir streams. h)</span><span class="sxs-lookup"><span data-stu-id="499f2-115">Ctlutil.h (include Streams.h)</span></span>                                                                                   |
| <span data-ttu-id="499f2-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="499f2-116">Library</span></span> | <span data-ttu-id="499f2-117">Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración)</span><span class="sxs-lookup"><span data-stu-id="499f2-117">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="499f2-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="499f2-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="499f2-119">**Clase COARefTime**</span><span class="sxs-lookup"><span data-stu-id="499f2-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




