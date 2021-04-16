---
description: El método CRendererInputPin es un método de constructor.
ms.assetid: 272f864e-d6a8-4a9e-b72f-892147db9970
title: Constructor CRendererInputPin. CRendererInputPin (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CRendererInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6888b234b87a48fc89f70c0db36122cbf7289ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671705"
---
# <a name="crendererinputpincrendererinputpin-constructor"></a><span data-ttu-id="2f388-103">Constructor CRendererInputPin. CRendererInputPin</span><span class="sxs-lookup"><span data-stu-id="2f388-103">CRendererInputPin.CRendererInputPin constructor</span></span>

<span data-ttu-id="2f388-104">El `CRendererInputPin` método es un método de constructor.</span><span class="sxs-lookup"><span data-stu-id="2f388-104">The `CRendererInputPin` method is a constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f388-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f388-105">Syntax</span></span>


```C++
CRendererInputPin(
   CBaseRenderer *pRenderer,
   HRESULT       *phr,
   LPCWSTR       Name
);
```



## <a name="parameters"></a><span data-ttu-id="2f388-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f388-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f388-107">*pRenderer*</span><span class="sxs-lookup"><span data-stu-id="2f388-107">*pRenderer*</span></span> 
</dt> <dd>

<span data-ttu-id="2f388-108">Puntero al objeto [**CBaseRenderer**](cbaserenderer.md) que implementa el filtro.</span><span class="sxs-lookup"><span data-stu-id="2f388-108">Pointer to the [**CBaseRenderer**](cbaserenderer.md) object that implements the filter.</span></span>

</dd> <dt>

<span data-ttu-id="2f388-109">*phr*</span><span class="sxs-lookup"><span data-stu-id="2f388-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="2f388-110">Puntero a una variable que recibe un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2f388-110">Pointer to a variable that receives an **HRESULT** value.</span></span>

</dd> <dt>

<span data-ttu-id="2f388-111">*Nombre*</span><span class="sxs-lookup"><span data-stu-id="2f388-111">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="2f388-112">Puntero a una cadena de caracteres anchos que contiene el identificador del PIN.</span><span class="sxs-lookup"><span data-stu-id="2f388-112">Pointer to a wide-character string containing the pin identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f388-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f388-113">Requirements</span></span>



| <span data-ttu-id="2f388-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f388-114">Requirement</span></span> | <span data-ttu-id="2f388-115">Value</span><span class="sxs-lookup"><span data-stu-id="2f388-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f388-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f388-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2f388-117"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f388-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2f388-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f388-118">Library</span></span><br/> | <dl> <span data-ttu-id="2f388-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2f388-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f388-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f388-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f388-121">**Clase CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="2f388-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




