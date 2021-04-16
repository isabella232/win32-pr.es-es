---
description: El método DeliverEndFlush solicita que el PIN de entrada conectado finalice una operación de vaciado.
ms.assetid: 9f1fd76c-dba7-41c5-b098-9735e4f2571b
title: Método CBaseOutputPin. DeliverEndFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb9b92947f2452b8755109c4b83cb21afa119461
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671508"
---
# <a name="cbaseoutputpindeliverendflush-method"></a><span data-ttu-id="bd046-103">CBaseOutputPin. DeliverEndFlush, método</span><span class="sxs-lookup"><span data-stu-id="bd046-103">CBaseOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="bd046-104">El `DeliverEndFlush` método solicita el PIN de entrada conectado para finalizar una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="bd046-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd046-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd046-105">Syntax</span></span>


```C++
virtual HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="bd046-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd046-106">Parameters</span></span>

<span data-ttu-id="bd046-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="bd046-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bd046-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd046-108">Return value</span></span>

<span data-ttu-id="bd046-109">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bd046-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="bd046-110">Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="bd046-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="bd046-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="bd046-111">Return code</span></span>                                                                                           | <span data-ttu-id="bd046-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="bd046-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="bd046-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="bd046-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="bd046-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="bd046-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="bd046-115"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="bd046-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="bd046-116">El PIN no está conectado.</span><span class="sxs-lookup"><span data-stu-id="bd046-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bd046-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bd046-117">Remarks</span></span>

<span data-ttu-id="bd046-118">Este método llama al método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) en el PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="bd046-118">This method calls the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd046-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd046-119">Requirements</span></span>



| <span data-ttu-id="bd046-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd046-120">Requirement</span></span> | <span data-ttu-id="bd046-121">Value</span><span class="sxs-lookup"><span data-stu-id="bd046-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd046-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd046-122">Header</span></span><br/>  | <dl> <span data-ttu-id="bd046-123"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bd046-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bd046-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bd046-124">Library</span></span><br/> | <dl> <span data-ttu-id="bd046-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="bd046-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd046-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd046-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd046-127">**Clase CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="bd046-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




