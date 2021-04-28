---
description: 'Método CBaseRenderer.GetPin: el método GetPin recupera un pin.'
ms.assetid: 665e1aaf-4491-4241-94c6-6ea356d7a665
title: Método CBaseRenderer.GetPin (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b7c30767b7cba68931bc1ddde4905c9b7bc2bc29
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119893"
---
# <a name="cbaserenderergetpin-method"></a><span data-ttu-id="2f6e0-103">Método CBaseRenderer.GetPin</span><span class="sxs-lookup"><span data-stu-id="2f6e0-103">CBaseRenderer.GetPin method</span></span>

<span data-ttu-id="2f6e0-104">El `GetPin` método recupera un pin.</span><span class="sxs-lookup"><span data-stu-id="2f6e0-104">The `GetPin` method retrieves a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f6e0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f6e0-105">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="2f6e0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f6e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f6e0-107">*n*</span><span class="sxs-lookup"><span data-stu-id="2f6e0-107">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="2f6e0-108">Número del pin especificado.</span><span class="sxs-lookup"><span data-stu-id="2f6e0-108">Number of the specified pin.</span></span> <span data-ttu-id="2f6e0-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="2f6e0-109">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f6e0-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f6e0-110">Return value</span></span>

<span data-ttu-id="2f6e0-111">Devuelve el [**puntero CBaseRenderer::m \_ pInputPin.**](cbaserenderer-m-pinputpin.md)</span><span class="sxs-lookup"><span data-stu-id="2f6e0-111">Returns the [**CBaseRenderer::m\_pInputPin**](cbaserenderer-m-pinputpin.md) pointer.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f6e0-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2f6e0-112">Remarks</span></span>

<span data-ttu-id="2f6e0-113">Este método implementa el [**método CBaseFilter::GetPin,**](cbasefilter-getpin.md) que es virtual puro en la **clase CBaseFilter.**</span><span class="sxs-lookup"><span data-stu-id="2f6e0-113">This method implements the [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method, which is pure virtual in the **CBaseFilter** class.</span></span> <span data-ttu-id="2f6e0-114">El filtro admite exactamente un pin (el pin de entrada).</span><span class="sxs-lookup"><span data-stu-id="2f6e0-114">The filter supports exactly one pin (the input pin).</span></span> <span data-ttu-id="2f6e0-115">La primera vez que se llama a este método, crea el pin como un nuevo [**objeto CRendererInputPin.**](crendererinputpin.md)</span><span class="sxs-lookup"><span data-stu-id="2f6e0-115">The first time this method is called, it creates the pin as a new [**CRendererInputPin**](crendererinputpin.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f6e0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f6e0-116">Requirements</span></span>



| <span data-ttu-id="2f6e0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f6e0-117">Requirement</span></span> | <span data-ttu-id="2f6e0-118">Value</span><span class="sxs-lookup"><span data-stu-id="2f6e0-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f6e0-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f6e0-119">Header</span></span><br/>  | <dl> <span data-ttu-id="2f6e0-120"><dt>Renbase.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f6e0-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2f6e0-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f6e0-121">Library</span></span><br/> | <dl> <span data-ttu-id="2f6e0-122"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2f6e0-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f6e0-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2f6e0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f6e0-124">**CBaseRenderer (clase)**</span><span class="sxs-lookup"><span data-stu-id="2f6e0-124">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




