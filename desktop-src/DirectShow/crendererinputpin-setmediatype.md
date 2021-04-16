---
description: 'El método SetMediaType establece el tipo de medio para la conexión. Este método invalida el método CBasePin:: SetMediaType.'
ms.assetid: b2668bb1-0739-413c-bea8-ec5541acfb3e
title: Método CRendererInputPin. SetMediaType (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca70878f8f6358a3297c22cbb9ac8e49ba0ce310
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671698"
---
# <a name="crendererinputpinsetmediatype-method"></a><span data-ttu-id="8ea7f-104">CRendererInputPin. SetMediaType, método</span><span class="sxs-lookup"><span data-stu-id="8ea7f-104">CRendererInputPin.SetMediaType method</span></span>

<span data-ttu-id="8ea7f-105">El `SetMediaType` método establece el tipo de medio para la conexión.</span><span class="sxs-lookup"><span data-stu-id="8ea7f-105">The `SetMediaType` method sets the media type for the connection.</span></span> <span data-ttu-id="8ea7f-106">Este método invalida el método [**CBasePin:: SetMediaType**](cbasepin-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="8ea7f-106">This method overrides the [**CBasePin::SetMediaType**](cbasepin-setmediatype.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ea7f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ea7f-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="8ea7f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ea7f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ea7f-109">*p.p.*</span><span class="sxs-lookup"><span data-stu-id="8ea7f-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="8ea7f-110">Puntero a un objeto [**CMediaType**](cmediatype.md) que especifica el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="8ea7f-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ea7f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ea7f-111">Return value</span></span>

<span data-ttu-id="8ea7f-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8ea7f-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ea7f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ea7f-113">Requirements</span></span>



| <span data-ttu-id="8ea7f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ea7f-114">Requirement</span></span> | <span data-ttu-id="8ea7f-115">Value</span><span class="sxs-lookup"><span data-stu-id="8ea7f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ea7f-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ea7f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="8ea7f-117"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ea7f-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8ea7f-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8ea7f-118">Library</span></span><br/> | <dl> <span data-ttu-id="8ea7f-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="8ea7f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ea7f-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ea7f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ea7f-121">**Clase CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="8ea7f-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




