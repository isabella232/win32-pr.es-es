---
description: El método GetPin recupera un PIN.
ms.assetid: 665e1aaf-4491-4241-94c6-6ea356d7a665
title: Método CBaseRenderer. GetPin (Renbase. h)
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
ms.openlocfilehash: 6b67b926e0af604e0a25ea7c09b417baf3647fde
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660284"
---
# <a name="cbaserenderergetpin-method"></a><span data-ttu-id="05f41-103">CBaseRenderer. GetPin, método</span><span class="sxs-lookup"><span data-stu-id="05f41-103">CBaseRenderer.GetPin method</span></span>

<span data-ttu-id="05f41-104">El `GetPin` método recupera un PIN.</span><span class="sxs-lookup"><span data-stu-id="05f41-104">The `GetPin` method retrieves a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="05f41-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="05f41-105">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="05f41-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="05f41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05f41-107">*n*</span><span class="sxs-lookup"><span data-stu-id="05f41-107">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="05f41-108">Número del PIN especificado.</span><span class="sxs-lookup"><span data-stu-id="05f41-108">Number of the specified pin.</span></span> <span data-ttu-id="05f41-109">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="05f41-109">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05f41-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="05f41-110">Return value</span></span>

<span data-ttu-id="05f41-111">Devuelve el puntero [**CBaseRenderer:: m \_ pInputPin**](cbaserenderer-m-pinputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="05f41-111">Returns the [**CBaseRenderer::m\_pInputPin**](cbaserenderer-m-pinputpin.md) pointer.</span></span>

## <a name="remarks"></a><span data-ttu-id="05f41-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="05f41-112">Remarks</span></span>

<span data-ttu-id="05f41-113">Este método implementa el método [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) , que es virtual puro en la clase **CBaseFilter** .</span><span class="sxs-lookup"><span data-stu-id="05f41-113">This method implements the [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method, which is pure virtual in the **CBaseFilter** class.</span></span> <span data-ttu-id="05f41-114">El filtro admite exactamente un PIN (el PIN de entrada).</span><span class="sxs-lookup"><span data-stu-id="05f41-114">The filter supports exactly one pin (the input pin).</span></span> <span data-ttu-id="05f41-115">La primera vez que se llama a este método, se crea el PIN como un nuevo objeto [**CRendererInputPin**](crendererinputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="05f41-115">The first time this method is called, it creates the pin as a new [**CRendererInputPin**](crendererinputpin.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="05f41-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05f41-116">Requirements</span></span>



| <span data-ttu-id="05f41-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="05f41-117">Requirement</span></span> | <span data-ttu-id="05f41-118">Value</span><span class="sxs-lookup"><span data-stu-id="05f41-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05f41-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="05f41-119">Header</span></span><br/>  | <dl> <span data-ttu-id="05f41-120"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05f41-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="05f41-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="05f41-121">Library</span></span><br/> | <dl> <span data-ttu-id="05f41-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="05f41-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05f41-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="05f41-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05f41-124">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="05f41-124">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




