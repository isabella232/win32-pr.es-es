---
description: Se llama al método SetMediaType cuando se establece el tipo de medio del PIN.
ms.assetid: 91d88523-006e-49fe-92f3-92825fbb323b
title: Método CBaseRenderer. SetMediaType (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ccb364545df514e098811ff6135e0c8cf72a329
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671674"
---
# <a name="cbaserenderersetmediatype-method"></a><span data-ttu-id="29195-103">CBaseRenderer. SetMediaType, método</span><span class="sxs-lookup"><span data-stu-id="29195-103">CBaseRenderer.SetMediaType method</span></span>

<span data-ttu-id="29195-104">`SetMediaType`Se llama al método cuando se establece el tipo de medio del PIN.</span><span class="sxs-lookup"><span data-stu-id="29195-104">The `SetMediaType` method is called when the pin's media type is set.</span></span>

## <a name="syntax"></a><span data-ttu-id="29195-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29195-105">Syntax</span></span>


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="29195-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="29195-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29195-107">*p.p.*</span><span class="sxs-lookup"><span data-stu-id="29195-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="29195-108">Puntero a un objeto [**CMediaType**](cmediatype.md) que especifica el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="29195-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29195-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="29195-109">Return value</span></span>

<span data-ttu-id="29195-110">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="29195-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="29195-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="29195-111">Remarks</span></span>

<span data-ttu-id="29195-112">El PIN de entrada llama a este método desde su propio método [**CRendererInputPin:: SetMediaType**](crendererinputpin-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="29195-112">The input pin calls this method from its own [**CRendererInputPin::SetMediaType**](crendererinputpin-setmediatype.md) method.</span></span> <span data-ttu-id="29195-113">Este método no hace nada en la clase base.</span><span class="sxs-lookup"><span data-stu-id="29195-113">This method does nothing in the base class.</span></span>

## <a name="requirements"></a><span data-ttu-id="29195-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29195-114">Requirements</span></span>



| <span data-ttu-id="29195-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="29195-115">Requirement</span></span> | <span data-ttu-id="29195-116">Value</span><span class="sxs-lookup"><span data-stu-id="29195-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29195-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="29195-117">Header</span></span><br/>  | <dl> <span data-ttu-id="29195-118"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29195-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="29195-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="29195-119">Library</span></span><br/> | <dl> <span data-ttu-id="29195-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="29195-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29195-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="29195-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29195-122">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="29195-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




