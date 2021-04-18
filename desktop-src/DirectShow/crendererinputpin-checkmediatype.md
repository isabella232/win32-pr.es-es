---
description: 'El método CheckMediaType determina si el PIN acepta un tipo de medio específico. Este método invalida el método CBasePin:: CheckMediaType.'
ms.assetid: 618c6f2e-2a15-43dd-811e-898dad0de226
title: Método CRendererInputPin. CheckMediaType (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5d3229d1431e45a6177c454f94bf9873aaceaca5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660659"
---
# <a name="crendererinputpincheckmediatype-method"></a><span data-ttu-id="6c45f-104">CRendererInputPin. CheckMediaType, método</span><span class="sxs-lookup"><span data-stu-id="6c45f-104">CRendererInputPin.CheckMediaType method</span></span>

<span data-ttu-id="6c45f-105">El `CheckMediaType` método determina si el PIN acepta un tipo de medio específico.</span><span class="sxs-lookup"><span data-stu-id="6c45f-105">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span> <span data-ttu-id="6c45f-106">Este método invalida el método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="6c45f-106">This method overrides the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c45f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c45f-107">Syntax</span></span>


```C++
HRESULT CheckMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="6c45f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c45f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c45f-109">*p.p.*</span><span class="sxs-lookup"><span data-stu-id="6c45f-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="6c45f-110">Puntero a un objeto de tipo de medio que contiene el tipo de medio propuesto.</span><span class="sxs-lookup"><span data-stu-id="6c45f-110">Pointer to a media type object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c45f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c45f-111">Return value</span></span>

<span data-ttu-id="6c45f-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6c45f-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c45f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c45f-113">Requirements</span></span>



| <span data-ttu-id="6c45f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c45f-114">Requirement</span></span> | <span data-ttu-id="6c45f-115">Value</span><span class="sxs-lookup"><span data-stu-id="6c45f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c45f-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c45f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6c45f-117"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c45f-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6c45f-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6c45f-118">Library</span></span><br/> | <dl> <span data-ttu-id="6c45f-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6c45f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c45f-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c45f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c45f-121">**Clase CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="6c45f-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




