---
description: El método EndFlush finaliza una operación de vaciado.
ms.assetid: ebb6beec-84e2-49a7-9771-bbd191faada7
title: Método CTransformFilter. EndFlush (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 348675f1369ec9b0deb5415ad14a864a8befef73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660622"
---
# <a name="ctransformfilterendflush-method"></a><span data-ttu-id="de104-103">CTransformFilter. EndFlush, método</span><span class="sxs-lookup"><span data-stu-id="de104-103">CTransformFilter.EndFlush method</span></span>

<span data-ttu-id="de104-104">El `EndFlush` método finaliza una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="de104-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="de104-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="de104-105">Syntax</span></span>


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="de104-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="de104-106">Parameters</span></span>

<span data-ttu-id="de104-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="de104-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="de104-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="de104-108">Return value</span></span>

<span data-ttu-id="de104-109">Devuelve S \_ OK u otro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="de104-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="de104-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de104-110">Remarks</span></span>

<span data-ttu-id="de104-111">Al final de una operación de vaciado, el método [**CTransformInputPin:: EndFlush**](ctransforminputpin-endflush.md) del PIN de entrada llama a este método.</span><span class="sxs-lookup"><span data-stu-id="de104-111">At the end of a flush operation, the input pin's [**CTransformInputPin::EndFlush**](ctransforminputpin-endflush.md) method calls this method.</span></span> <span data-ttu-id="de104-112">Este método pasa la `EndFlush` llamada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="de104-112">This method passes the `EndFlush` call downstream.</span></span>

<span data-ttu-id="de104-113">Si la clase derivada utiliza un subproceso de trabajo para proporcionar ejemplos, debe descartar todos los datos en cola antes de enviar la `EndFlush` llamada de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="de104-113">If the derived class uses a worker thread to deliver samples, it must discard any queued data before sending the `EndFlush` call downstream.</span></span> <span data-ttu-id="de104-114">Para obtener más información, vea [flujo de datos para desarrolladores de filtros](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="de104-114">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="de104-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de104-115">Requirements</span></span>



| <span data-ttu-id="de104-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="de104-116">Requirement</span></span> | <span data-ttu-id="de104-117">Value</span><span class="sxs-lookup"><span data-stu-id="de104-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de104-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="de104-118">Header</span></span><br/>  | <dl> <span data-ttu-id="de104-119"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de104-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="de104-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="de104-120">Library</span></span><br/> | <dl> <span data-ttu-id="de104-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="de104-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de104-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="de104-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de104-123">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="de104-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




