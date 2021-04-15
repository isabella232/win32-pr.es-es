---
description: El método FindPinNumber recupera el número de un PIN especificado en el filtro.
ms.assetid: c9366fcc-7b13-4e43-883e-6003c32fadec
title: CSource. FindPinNumber (método) (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPinNumber
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a71c65efd97c48eed58fb7d0b5aa8fcc2f178e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689997"
---
# <a name="csourcefindpinnumber-method"></a><span data-ttu-id="6e74e-103">CSource. FindPinNumber, método</span><span class="sxs-lookup"><span data-stu-id="6e74e-103">CSource.FindPinNumber method</span></span>

<span data-ttu-id="6e74e-104">El `FindPinNumber` método recupera el número de un PIN especificado en el filtro.</span><span class="sxs-lookup"><span data-stu-id="6e74e-104">The `FindPinNumber` method retrieves the number of a specified pin on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e74e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e74e-105">Syntax</span></span>


```C++
int FindPinNumber(
   IPin *iPin
);
```



## <a name="parameters"></a><span data-ttu-id="6e74e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e74e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e74e-107">*iPin*</span><span class="sxs-lookup"><span data-stu-id="6e74e-107">*iPin*</span></span> 
</dt> <dd>

<span data-ttu-id="6e74e-108">Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN.</span><span class="sxs-lookup"><span data-stu-id="6e74e-108">Pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e74e-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e74e-109">Return value</span></span>

<span data-ttu-id="6e74e-110">Devuelve el número de PIN o 1 si no se encuentra el PIN en este filtro.</span><span class="sxs-lookup"><span data-stu-id="6e74e-110">Returns the pin number, or  1 if the pin is not found on this filter.</span></span> <span data-ttu-id="6e74e-111">El primer pin tiene el número cero.</span><span class="sxs-lookup"><span data-stu-id="6e74e-111">The first pin is numbered zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e74e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e74e-112">Requirements</span></span>



| <span data-ttu-id="6e74e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e74e-113">Requirement</span></span> | <span data-ttu-id="6e74e-114">Value</span><span class="sxs-lookup"><span data-stu-id="6e74e-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e74e-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e74e-115">Header</span></span><br/>  | <dl> <span data-ttu-id="6e74e-116"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6e74e-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6e74e-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6e74e-117">Library</span></span><br/> | <dl> <span data-ttu-id="6e74e-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6e74e-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e74e-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e74e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e74e-120">**Clase CSource**</span><span class="sxs-lookup"><span data-stu-id="6e74e-120">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




