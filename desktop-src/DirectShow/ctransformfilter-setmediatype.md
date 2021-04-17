---
description: Se llama al método SetMediaType cuando el tipo de medio se establece en uno de los PIN del filtro.
ms.assetid: 3e505036-7fa6-42cf-a683-3a39a43d209d
title: Método CTransformFilter. SetMediaType (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 86e9eac76ccc178659935511d75b1676a136a1c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680817"
---
# <a name="ctransformfiltersetmediatype-method"></a><span data-ttu-id="fbed2-103">CTransformFilter. SetMediaType, método</span><span class="sxs-lookup"><span data-stu-id="fbed2-103">CTransformFilter.SetMediaType method</span></span>

<span data-ttu-id="fbed2-104">`SetMediaType`Se llama al método cuando el tipo de medio se establece en uno de los PIN del filtro.</span><span class="sxs-lookup"><span data-stu-id="fbed2-104">The `SetMediaType` method is called when the media type is set on one of the filter's pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbed2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fbed2-105">Syntax</span></span>


```C++
virtual HRESULT SetMediaType(
         PIN_DIRECTION direction,
   const CMediaType    *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="fbed2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fbed2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbed2-107">*direction*</span><span class="sxs-lookup"><span data-stu-id="fbed2-107">*direction*</span></span> 
</dt> <dd>

<span data-ttu-id="fbed2-108">Miembro del tipo enumerado de [**\_ dirección del PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) , que especifica un PIN en el filtro (entrada o salida).</span><span class="sxs-lookup"><span data-stu-id="fbed2-108">Member of the [**PIN\_DIRECTION**](/windows/win32/api/strmif/ne-strmif-pin_direction) enumerated type, specifying a pin on the filter (input or output).</span></span>

</dd> <dt>

<span data-ttu-id="fbed2-109">*p.p.*</span><span class="sxs-lookup"><span data-stu-id="fbed2-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="fbed2-110">Puntero a un objeto [**CMediaType**](cmediatype.md) que especifica el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="fbed2-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbed2-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fbed2-111">Return value</span></span>

<span data-ttu-id="fbed2-112">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="fbed2-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbed2-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fbed2-113">Remarks</span></span>

<span data-ttu-id="fbed2-114">Los métodos [**CTransformInputPin:: SetMediaType**](ctransforminputpin-setmediatype.md) y [**CTransformOutputPin:: SetMediaType**](ctransformoutputpin-setmediatype.md) llaman a este método cuando se establece el tipo de medio de un PIN.</span><span class="sxs-lookup"><span data-stu-id="fbed2-114">The [**CTransformInputPin::SetMediaType**](ctransforminputpin-setmediatype.md) and [**CTransformOutputPin::SetMediaType**](ctransformoutputpin-setmediatype.md) methods call this method when a pin's media type is set.</span></span> <span data-ttu-id="fbed2-115">Este método no hace nada en la clase base, pero la clase derivada puede invalidarlo.</span><span class="sxs-lookup"><span data-stu-id="fbed2-115">This method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbed2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbed2-116">Requirements</span></span>



| <span data-ttu-id="fbed2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbed2-117">Requirement</span></span> | <span data-ttu-id="fbed2-118">Value</span><span class="sxs-lookup"><span data-stu-id="fbed2-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbed2-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fbed2-119">Header</span></span><br/>  | <dl> <span data-ttu-id="fbed2-120"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fbed2-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fbed2-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fbed2-121">Library</span></span><br/> | <dl> <span data-ttu-id="fbed2-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="fbed2-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbed2-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="fbed2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbed2-124">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="fbed2-124">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




