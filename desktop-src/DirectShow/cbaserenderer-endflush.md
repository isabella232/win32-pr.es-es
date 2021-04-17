---
description: El método EndFlush finaliza una operación de vaciado.
ms.assetid: 4c30abbf-7351-4eee-af9a-9330f6d1aa08
title: Método CBaseRenderer. EndFlush (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bd565bfa21edb9945b901d8e315f3e1d1cd054f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671072"
---
# <a name="cbaserendererendflush-method"></a><span data-ttu-id="ab2a7-103">CBaseRenderer. EndFlush, método</span><span class="sxs-lookup"><span data-stu-id="ab2a7-103">CBaseRenderer.EndFlush method</span></span>

<span data-ttu-id="ab2a7-104">El `EndFlush` método finaliza una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="ab2a7-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab2a7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab2a7-105">Syntax</span></span>


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="ab2a7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab2a7-106">Parameters</span></span>

<span data-ttu-id="ab2a7-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ab2a7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ab2a7-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab2a7-108">Return value</span></span>

<span data-ttu-id="ab2a7-109">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="ab2a7-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab2a7-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab2a7-110">Remarks</span></span>

<span data-ttu-id="ab2a7-111">El PIN de entrada del filtro llama a este método cuando recibe una llamada al método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="ab2a7-111">The filter's input pin calls this method when it receives a call to the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab2a7-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab2a7-112">Requirements</span></span>



| <span data-ttu-id="ab2a7-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab2a7-113">Requirement</span></span> | <span data-ttu-id="ab2a7-114">Value</span><span class="sxs-lookup"><span data-stu-id="ab2a7-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab2a7-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab2a7-115">Header</span></span><br/>  | <dl> <span data-ttu-id="ab2a7-116"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab2a7-116"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ab2a7-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab2a7-117">Library</span></span><br/> | <dl> <span data-ttu-id="ab2a7-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ab2a7-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab2a7-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab2a7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab2a7-120">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="ab2a7-120">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




