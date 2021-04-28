---
description: 'Método COutputQueue.BeginFlush: el método BeginFlush comienza una operación de vaciado.'
ms.assetid: d37b611e-742f-4bdf-bd72-a91cd1c473b3
title: Método COutputQueue.BeginFlush (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e7c6168daf766ec11e18e86673d9d25542b50462
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099033"
---
# <a name="coutputqueuebeginflush-method"></a><span data-ttu-id="79950-103">Método COutputQueue.BeginFlush</span><span class="sxs-lookup"><span data-stu-id="79950-103">COutputQueue.BeginFlush method</span></span>

<span data-ttu-id="79950-104">El `BeginFlush` método comienza una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="79950-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="79950-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="79950-105">Syntax</span></span>


```C++
void BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="79950-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="79950-106">Parameters</span></span>

<span data-ttu-id="79950-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="79950-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="79950-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79950-108">Return value</span></span>

<span data-ttu-id="79950-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="79950-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="79950-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="79950-110">Remarks</span></span>

<span data-ttu-id="79950-111">Este método establece la variable [**miembro COutputQueue::m \_ bFlushing**](coutputqueue-m-bflushing.md) en **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="79950-111">This method sets the [**COutputQueue::m\_bFlushing**](coutputqueue-m-bflushing.md) member variable to **TRUE**.</span></span> <span data-ttu-id="79950-112">Si el objeto usa un subproceso, el subproceso llama al método [**COutputQueue::FreeSamples**](coutputqueue-freesamples.md) para liberar los ejemplos pendientes.</span><span class="sxs-lookup"><span data-stu-id="79950-112">If the object is using a thread, the thread calls the [**COutputQueue::FreeSamples**](coutputqueue-freesamples.md) method to free any pending samples.</span></span> <span data-ttu-id="79950-113">De lo contrario, el objeto **llama a FreeSamples** durante [**el método COutputQueue::EndFlush.**](coutputqueue-endflush.md)</span><span class="sxs-lookup"><span data-stu-id="79950-113">Otherwise, the object calls **FreeSamples** during the [**COutputQueue::EndFlush**](coutputqueue-endflush.md) method.</span></span> <span data-ttu-id="79950-114">Este método también establece la variable [**miembro COutputQueue::m \_ hr**](coutputqueue-m-hr.md) en S FALSE, lo que hace que el objeto descarte \_ todos los ejemplos nuevos.</span><span class="sxs-lookup"><span data-stu-id="79950-114">This method also sets the [**COutputQueue::m\_hr**](coutputqueue-m-hr.md) member variable to S\_FALSE, which causes the object to discard all new samples.</span></span>

<span data-ttu-id="79950-115">El objeto pasa la notificación de vaciado de bajada llamando al [**método IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) en el pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="79950-115">The object passes the flush notification downstream by calling the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="79950-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79950-116">Requirements</span></span>



| <span data-ttu-id="79950-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="79950-117">Requirement</span></span> | <span data-ttu-id="79950-118">Value</span><span class="sxs-lookup"><span data-stu-id="79950-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79950-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="79950-119">Header</span></span><br/>  | <dl> <span data-ttu-id="79950-120"><dt>Outputq.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="79950-120"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="79950-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="79950-121">Library</span></span><br/> | <dl> <span data-ttu-id="79950-122"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="79950-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79950-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="79950-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79950-124">**COutputQueue (clase)**</span><span class="sxs-lookup"><span data-stu-id="79950-124">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




