---
description: El método SetAbortSignal establece una marca que indica si se debe detener la representación y rechazar más ejemplos.
ms.assetid: 2dbf3b4d-e285-4d17-a77c-01a16c09d148
title: Método CBaseRenderer. SetAbortSignal (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetAbortSignal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70527d5e43ccab4df7b2110a33df8d813bd16d28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671099"
---
# <a name="cbaserenderersetabortsignal-method"></a><span data-ttu-id="b2bef-103">CBaseRenderer. SetAbortSignal, método</span><span class="sxs-lookup"><span data-stu-id="b2bef-103">CBaseRenderer.SetAbortSignal method</span></span>

<span data-ttu-id="b2bef-104">El `SetAbortSignal` método establece una marca que indica si se debe detener la representación y rechazar más ejemplos.</span><span class="sxs-lookup"><span data-stu-id="b2bef-104">The `SetAbortSignal` method sets a flag which indicates whether to stop rendering and reject further samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2bef-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2bef-105">Syntax</span></span>


```C++
void SetAbortSignal(
   BOOL bAbort
);
```



## <a name="parameters"></a><span data-ttu-id="b2bef-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b2bef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2bef-107">*bAbort*</span><span class="sxs-lookup"><span data-stu-id="b2bef-107">*bAbort*</span></span> 
</dt> <dd>

<span data-ttu-id="b2bef-108">Valor booleano que indica si se va a detener la representación.</span><span class="sxs-lookup"><span data-stu-id="b2bef-108">Boolean value indicating whether to stop rendering.</span></span> <span data-ttu-id="b2bef-109">Si **es true**, el filtro no representará más muestras.</span><span class="sxs-lookup"><span data-stu-id="b2bef-109">If **TRUE**, the filter will not render any more samples.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2bef-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2bef-110">Return value</span></span>

<span data-ttu-id="b2bef-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b2bef-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2bef-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b2bef-112">Remarks</span></span>

<span data-ttu-id="b2bef-113">Este método establece la marca [**CBaseRenderer:: m \_ bAbort**](cbaserenderer-m-babort.md) .</span><span class="sxs-lookup"><span data-stu-id="b2bef-113">This method sets the [**CBaseRenderer::m\_bAbort**](cbaserenderer-m-babort.md) flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2bef-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2bef-114">Requirements</span></span>



| <span data-ttu-id="b2bef-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2bef-115">Requirement</span></span> | <span data-ttu-id="b2bef-116">Value</span><span class="sxs-lookup"><span data-stu-id="b2bef-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2bef-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2bef-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b2bef-118"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2bef-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b2bef-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b2bef-119">Library</span></span><br/> | <dl> <span data-ttu-id="b2bef-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b2bef-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2bef-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2bef-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2bef-122">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="b2bef-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




