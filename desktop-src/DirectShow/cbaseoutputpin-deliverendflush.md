---
description: 'Método CBaseOutputPin.DeliverEndFlush: el método DeliverEndFlush solicita el pin de entrada conectado para finalizar una operación de vaciado.'
ms.assetid: 9f1fd76c-dba7-41c5-b098-9735e4f2571b
title: Método CBaseOutputPin.DeliverEndFlush (Amfilter.h)
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
ms.openlocfilehash: 5f3fd5c1bc686ee5c0b4ff0cd1285a5114b93049
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096183"
---
# <a name="cbaseoutputpindeliverendflush-method"></a><span data-ttu-id="d3f69-103">Método CBaseOutputPin.DeliverEndFlush</span><span class="sxs-lookup"><span data-stu-id="d3f69-103">CBaseOutputPin.DeliverEndFlush method</span></span>

<span data-ttu-id="d3f69-104">El `DeliverEndFlush` método solicita el pin de entrada conectado para finalizar una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="d3f69-104">The `DeliverEndFlush` method requests the connected input pin to end a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3f69-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3f69-105">Syntax</span></span>


```C++
virtual HRESULT DeliverEndFlush();
```



## <a name="parameters"></a><span data-ttu-id="d3f69-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d3f69-106">Parameters</span></span>

<span data-ttu-id="d3f69-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d3f69-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d3f69-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d3f69-108">Return value</span></span>

<span data-ttu-id="d3f69-109">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="d3f69-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d3f69-110">Los valores posibles incluyen los enumerados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="d3f69-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="d3f69-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d3f69-111">Return code</span></span>                                                                                           | <span data-ttu-id="d3f69-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3f69-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d3f69-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d3f69-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="d3f69-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="d3f69-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="d3f69-115"><dt>**VFW \_ E \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="d3f69-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="d3f69-116">El pin no está conectado.</span><span class="sxs-lookup"><span data-stu-id="d3f69-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d3f69-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d3f69-117">Remarks</span></span>

<span data-ttu-id="d3f69-118">Este método llama al [**método IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) en el pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="d3f69-118">This method calls the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3f69-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3f69-119">Requirements</span></span>



| <span data-ttu-id="d3f69-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3f69-120">Requirement</span></span> | <span data-ttu-id="d3f69-121">Value</span><span class="sxs-lookup"><span data-stu-id="d3f69-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3f69-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d3f69-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d3f69-123"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="d3f69-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d3f69-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d3f69-124">Library</span></span><br/> | <dl> <span data-ttu-id="d3f69-125"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d3f69-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3f69-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d3f69-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3f69-127">**CBaseOutputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="d3f69-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




