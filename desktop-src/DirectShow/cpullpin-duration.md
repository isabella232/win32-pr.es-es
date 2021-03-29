---
description: El método Duration recupera la duración de la secuencia.
ms.assetid: 82fbd7f5-36dc-4e81-9ce5-9ee28adf73ef
title: Método CPullPin. Duration (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Duration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ecd05478f67934368aa6d1de84ae32a209ddcad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680835"
---
# <a name="cpullpinduration-method"></a><span data-ttu-id="c5525-103">CPullPin. Duration (método)</span><span class="sxs-lookup"><span data-stu-id="c5525-103">CPullPin.Duration method</span></span>

<span data-ttu-id="c5525-104">El `Duration` método recupera la duración de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="c5525-104">The `Duration` method retrieves the duration of the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5525-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c5525-105">Syntax</span></span>


```C++
HRESULT Duration(
   REFERENCE_TIME *ptDuration
);
```



## <a name="parameters"></a><span data-ttu-id="c5525-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c5525-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5525-107">*ptDuration*</span><span class="sxs-lookup"><span data-stu-id="c5525-107">*ptDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="c5525-108">Puntero a una variable que recibe la duración, en bytes multiplicada por 10 millones.</span><span class="sxs-lookup"><span data-stu-id="c5525-108">Pointer to a variable that receives the duration, in bytes multiplied by 10,000,000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5525-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c5525-109">Return value</span></span>

<span data-ttu-id="c5525-110">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="c5525-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5525-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c5525-111">Remarks</span></span>

<span data-ttu-id="c5525-112">La duración es indeterminada hasta que se llama al método [**CPullPin:: Connect**](cpullpin-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="c5525-112">The duration is indeterminate until the [**CPullPin::Connect**](cpullpin-connect.md) method is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5525-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5525-113">Requirements</span></span>



| <span data-ttu-id="c5525-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5525-114">Requirement</span></span> | <span data-ttu-id="c5525-115">Value</span><span class="sxs-lookup"><span data-stu-id="c5525-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5525-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c5525-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c5525-117"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5525-117"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="c5525-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c5525-118">Library</span></span><br/> | <dl> <span data-ttu-id="c5525-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c5525-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5525-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="c5525-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5525-121">**Clase CPullPin**</span><span class="sxs-lookup"><span data-stu-id="c5525-121">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




