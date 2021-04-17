---
description: El método BeginFlush inicia una operación de vaciado.
ms.assetid: dc652394-c24e-4cea-ac28-30a1e6de205f
title: Método CBaseRenderer. BeginFlush (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e218e3b2d9c0cef8ce0fe052ad1b3c4b6f786858
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671082"
---
# <a name="cbaserendererbeginflush-method"></a><span data-ttu-id="4aae4-103">CBaseRenderer. BeginFlush, método</span><span class="sxs-lookup"><span data-stu-id="4aae4-103">CBaseRenderer.BeginFlush method</span></span>

<span data-ttu-id="4aae4-104">El `BeginFlush` método inicia una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="4aae4-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aae4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4aae4-105">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="4aae4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4aae4-106">Parameters</span></span>

<span data-ttu-id="4aae4-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="4aae4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4aae4-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4aae4-108">Return value</span></span>

<span data-ttu-id="4aae4-109">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="4aae4-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4aae4-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4aae4-110">Remarks</span></span>

<span data-ttu-id="4aae4-111">El PIN de entrada del filtro llama a este método cuando recibe una llamada al método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .</span><span class="sxs-lookup"><span data-stu-id="4aae4-111">The filter's input pin calls this method when it receives a call to the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span> <span data-ttu-id="4aae4-112">El filtro libera el subproceso de streaming y libera cualquier ejemplo que estaba manteniendo para su representación.</span><span class="sxs-lookup"><span data-stu-id="4aae4-112">The filter releases the streaming thread, and releases any sample that it was holding for rendering.</span></span>

## <a name="requirements"></a><span data-ttu-id="4aae4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4aae4-113">Requirements</span></span>



| <span data-ttu-id="4aae4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="4aae4-114">Requirement</span></span> | <span data-ttu-id="4aae4-115">Value</span><span class="sxs-lookup"><span data-stu-id="4aae4-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4aae4-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4aae4-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4aae4-117"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4aae4-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4aae4-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4aae4-118">Library</span></span><br/> | <dl> <span data-ttu-id="4aae4-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="4aae4-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aae4-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="4aae4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aae4-121">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="4aae4-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




