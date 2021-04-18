---
description: 'El método SetMediaType establece el tipo de medio para el ejemplo. Este método implementa el método IMediaSample:: SetMediaType.'
ms.assetid: 4423cc1e-d6e1-49e7-9cc1-1a1d71a3497b
title: Método CMediaSample. SetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f46fc4e8c348b1d03d19e815f658e0f637b8f880
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679074"
---
# <a name="cmediasamplesetmediatype-method"></a><span data-ttu-id="f821e-104">CMediaSample. SetMediaType, método</span><span class="sxs-lookup"><span data-stu-id="f821e-104">CMediaSample.SetMediaType method</span></span>

<span data-ttu-id="f821e-105">El `SetMediaType` método establece el tipo de medio para el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f821e-105">The `SetMediaType` method sets the media type for the sample.</span></span> <span data-ttu-id="f821e-106">Este método implementa el método [**IMediaSample:: SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) .</span><span class="sxs-lookup"><span data-stu-id="f821e-106">This method implements the [**IMediaSample::SetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setmediatype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f821e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f821e-107">Syntax</span></span>


```C++
HRESULT SetMediaType(
   AM_MEDIA_TYPE *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="f821e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f821e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f821e-109">*pMediaType*</span><span class="sxs-lookup"><span data-stu-id="f821e-109">*pMediaType*</span></span> 
</dt> <dd>

<span data-ttu-id="f821e-110">Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="f821e-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f821e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f821e-111">Return value</span></span>

<span data-ttu-id="f821e-112">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f821e-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="f821e-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f821e-113">Return code</span></span>                                                                                   | <span data-ttu-id="f821e-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f821e-114">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="f821e-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f821e-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f821e-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="f821e-116">Success</span></span><br/>             |
| <dl> <span data-ttu-id="f821e-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f821e-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f821e-118">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="f821e-118">Insufficient memory</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f821e-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f821e-119">Remarks</span></span>

<span data-ttu-id="f821e-120">Este método establece la variable miembro [**CMediaSample:: m \_ pMediaType**](cmediasample-m-pmediatype.md) , que especifica el tipo de medio y la variable miembro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) , que especifica si el tipo de medio ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="f821e-120">This method sets the [**CMediaSample::m\_pMediaType**](cmediasample-m-pmediatype.md) member variable, which specifies the media type, and the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies whether the media type has changed.</span></span>

<span data-ttu-id="f821e-121">Este método realiza una copia de la \_ estructura de tipo de medio am \_ .</span><span class="sxs-lookup"><span data-stu-id="f821e-121">This method makes a copy of the AM\_MEDIA\_TYPE structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="f821e-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f821e-122">Requirements</span></span>



| <span data-ttu-id="f821e-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f821e-123">Requirement</span></span> | <span data-ttu-id="f821e-124">Value</span><span class="sxs-lookup"><span data-stu-id="f821e-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f821e-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f821e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f821e-126"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f821e-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f821e-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f821e-127">Library</span></span><br/> | <dl> <span data-ttu-id="f821e-128"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f821e-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f821e-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="f821e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f821e-130">**Clase CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="f821e-130">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




