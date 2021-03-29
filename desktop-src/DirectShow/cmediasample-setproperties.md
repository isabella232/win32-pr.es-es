---
description: 'El método SetProperties establece las propiedades del ejemplo. Este método implementa el método IMediaSample2:: SetProperties.'
ms.assetid: 639aedf5-0c21-4578-b336-91859e40f3be
title: Método CMediaSample. SetProperties (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c5e6ef3c3839825586bf47259cf44783d167f503
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678999"
---
# <a name="cmediasamplesetproperties-method"></a><span data-ttu-id="b665e-104">CMediaSample. SetProperties (método)</span><span class="sxs-lookup"><span data-stu-id="b665e-104">CMediaSample.SetProperties method</span></span>

<span data-ttu-id="b665e-105">El `SetProperties` método establece las propiedades del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b665e-105">The `SetProperties` method sets the properties of the sample.</span></span> <span data-ttu-id="b665e-106">Este método implementa el método [**IMediaSample2:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties) .</span><span class="sxs-lookup"><span data-stu-id="b665e-106">This method implements the [**IMediaSample2::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-setproperties) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b665e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b665e-107">Syntax</span></span>


```C++
HRESULT SetProperties(
         DWORD cbProperties,
   const BYTE  *pbProperties
);
```



## <a name="parameters"></a><span data-ttu-id="b665e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b665e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b665e-109">*cbProperties*</span><span class="sxs-lookup"><span data-stu-id="b665e-109">*cbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="b665e-110">Longitud de los datos de propiedad que se van a establecer, en bytes.</span><span class="sxs-lookup"><span data-stu-id="b665e-110">Length of property data to set, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b665e-111">*pbProperties*</span><span class="sxs-lookup"><span data-stu-id="b665e-111">*pbProperties*</span></span> 
</dt> <dd>

<span data-ttu-id="b665e-112">Puntero a un búfer de tamaño *cbProperties*.</span><span class="sxs-lookup"><span data-stu-id="b665e-112">Pointer to a buffer of size *cbProperties*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b665e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b665e-113">Return value</span></span>

<span data-ttu-id="b665e-114">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="b665e-114">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="b665e-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="b665e-115">Return code</span></span>                                                                                   | <span data-ttu-id="b665e-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="b665e-116">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="b665e-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="b665e-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b665e-118">Correcto</span><span class="sxs-lookup"><span data-stu-id="b665e-118">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="b665e-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="b665e-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="b665e-120">Argumento no válido</span><span class="sxs-lookup"><span data-stu-id="b665e-120">Invalid argument</span></span><br/>          |
| <dl> <span data-ttu-id="b665e-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b665e-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b665e-122">Memoria insuficiente</span><span class="sxs-lookup"><span data-stu-id="b665e-122">Insufficient memory</span></span><br/>       |
| <dl> <span data-ttu-id="b665e-123"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="b665e-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b665e-124">Argumento de puntero **nulo**</span><span class="sxs-lookup"><span data-stu-id="b665e-124">**NULL** pointer argument</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b665e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b665e-125">Requirements</span></span>



| <span data-ttu-id="b665e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b665e-126">Requirement</span></span> | <span data-ttu-id="b665e-127">Value</span><span class="sxs-lookup"><span data-stu-id="b665e-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b665e-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b665e-128">Header</span></span><br/>  | <dl> <span data-ttu-id="b665e-129"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b665e-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b665e-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b665e-130">Library</span></span><br/> | <dl> <span data-ttu-id="b665e-131"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b665e-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b665e-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="b665e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b665e-133">**Clase CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="b665e-133">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




