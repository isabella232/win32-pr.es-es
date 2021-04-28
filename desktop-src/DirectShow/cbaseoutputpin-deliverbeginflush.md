---
description: 'Método CBaseOutputPin.DeliverBeginFlush: el método DeliverBeginFlush solicita el pin de entrada conectado para iniciar una operación de vaciado.'
ms.assetid: 0d7c7bd7-2a7a-42a4-a0de-60205b62e49c
title: Método CBaseOutputPin.DeliverBeginFlush (Amfilter.h)
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
ms.openlocfilehash: 22dbd2bccf33d9f203d1505106184500b8cae3ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099523"
---
# <a name="cbaseoutputpindeliverbeginflush-method"></a><span data-ttu-id="a5cc7-103">Método CBaseOutputPin.DeliverBeginFlush</span><span class="sxs-lookup"><span data-stu-id="a5cc7-103">CBaseOutputPin.DeliverBeginFlush method</span></span>

<span data-ttu-id="a5cc7-104">El `DeliverBeginFlush` método solicita el pin de entrada conectado para iniciar una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="a5cc7-104">The `DeliverBeginFlush` method requests the connected input pin to begin a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5cc7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a5cc7-105">Syntax</span></span>


```C++
virtual HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="a5cc7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a5cc7-106">Parameters</span></span>

<span data-ttu-id="a5cc7-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a5cc7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a5cc7-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a5cc7-108">Return value</span></span>

<span data-ttu-id="a5cc7-109">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="a5cc7-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="a5cc7-110">Los valores posibles incluyen los enumerados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="a5cc7-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="a5cc7-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a5cc7-111">Return code</span></span>                                                                                           | <span data-ttu-id="a5cc7-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5cc7-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a5cc7-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a5cc7-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="a5cc7-114">Correcto.</span><span class="sxs-lookup"><span data-stu-id="a5cc7-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="a5cc7-115"><dt>**VFW \_ E \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="a5cc7-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="a5cc7-116">El pin no está conectado.</span><span class="sxs-lookup"><span data-stu-id="a5cc7-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a5cc7-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a5cc7-117">Remarks</span></span>

<span data-ttu-id="a5cc7-118">Este método llama al [**método IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) en el pin de entrada.</span><span class="sxs-lookup"><span data-stu-id="a5cc7-118">This method calls the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5cc7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5cc7-119">Requirements</span></span>



| <span data-ttu-id="a5cc7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5cc7-120">Requirement</span></span> | <span data-ttu-id="a5cc7-121">Value</span><span class="sxs-lookup"><span data-stu-id="a5cc7-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5cc7-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5cc7-122">Header</span></span><br/>  | <dl> <span data-ttu-id="a5cc7-123"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="a5cc7-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a5cc7-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a5cc7-124">Library</span></span><br/> | <dl> <span data-ttu-id="a5cc7-125"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a5cc7-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5cc7-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a5cc7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5cc7-127">**CBaseOutputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="a5cc7-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




