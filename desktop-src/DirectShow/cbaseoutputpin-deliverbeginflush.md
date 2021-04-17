---
description: El método DeliverBeginFlush solicita la clavija de entrada conectada para iniciar una operación de vaciado.
ms.assetid: 0d7c7bd7-2a7a-42a4-a0de-60205b62e49c
title: Método CBaseOutputPin. DeliverBeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverBeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dad764ceaa6cc57c8c5b7ee288859926b6c63f02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661197"
---
# <a name="cbaseoutputpindeliverbeginflush-method"></a><span data-ttu-id="e6eef-103">CBaseOutputPin. DeliverBeginFlush, método</span><span class="sxs-lookup"><span data-stu-id="e6eef-103">CBaseOutputPin.DeliverBeginFlush method</span></span>

<span data-ttu-id="e6eef-104">El `DeliverBeginFlush` método solicita la clavija de entrada conectada para iniciar una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="e6eef-104">The `DeliverBeginFlush` method requests the connected input pin to begin a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6eef-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6eef-105">Syntax</span></span>


```C++
virtual HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="e6eef-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6eef-106">Parameters</span></span>

<span data-ttu-id="e6eef-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="e6eef-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e6eef-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6eef-108">Return value</span></span>

<span data-ttu-id="e6eef-109">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e6eef-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e6eef-110">Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e6eef-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="e6eef-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="e6eef-111">Return code</span></span>                                                                                           | <span data-ttu-id="e6eef-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6eef-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e6eef-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="e6eef-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="e6eef-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="e6eef-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="e6eef-115"><dt>**VFW \_ E \_ no \_ conectada**</dt></span><span class="sxs-lookup"><span data-stu-id="e6eef-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="e6eef-116">El PIN no está conectado.</span><span class="sxs-lookup"><span data-stu-id="e6eef-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e6eef-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6eef-117">Remarks</span></span>

<span data-ttu-id="e6eef-118">Este método llama al método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) en el PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="e6eef-118">This method calls the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6eef-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6eef-119">Requirements</span></span>



| <span data-ttu-id="e6eef-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6eef-120">Requirement</span></span> | <span data-ttu-id="e6eef-121">Value</span><span class="sxs-lookup"><span data-stu-id="e6eef-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6eef-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6eef-122">Header</span></span><br/>  | <dl> <span data-ttu-id="e6eef-123"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6eef-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e6eef-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6eef-124">Library</span></span><br/> | <dl> <span data-ttu-id="e6eef-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e6eef-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6eef-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6eef-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6eef-127">**Clase CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="e6eef-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




