---
description: El método Transform transforma una muestra de entrada para generar un ejemplo de salida.
ms.assetid: 30ef8c0c-e834-481a-93ff-d06e6fa1ddeb
title: Método CTransformFilter. Transform (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Transform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8498a9a6ce266e0646dbbdcb4f322c093d6e0cc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679361"
---
# <a name="ctransformfiltertransform-method"></a><span data-ttu-id="2f0de-103">CTransformFilter. Transform (método)</span><span class="sxs-lookup"><span data-stu-id="2f0de-103">CTransformFilter.Transform method</span></span>

<span data-ttu-id="2f0de-104">El `Transform` método transforma una muestra de entrada para generar un ejemplo de salida.</span><span class="sxs-lookup"><span data-stu-id="2f0de-104">The `Transform` method transforms an input sample to produce an output sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f0de-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f0de-105">Syntax</span></span>


```C++
virtual HRESULT Transform(
   IMediaSample *pIn,
   IMediaSample *pOut
);
```



## <a name="parameters"></a><span data-ttu-id="2f0de-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f0de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f0de-107">*Agujas*</span><span class="sxs-lookup"><span data-stu-id="2f0de-107">*pIn*</span></span> 
</dt> <dd>

<span data-ttu-id="2f0de-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo de entrada.</span><span class="sxs-lookup"><span data-stu-id="2f0de-108">Pointer to the input sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="2f0de-109">*pOut*</span><span class="sxs-lookup"><span data-stu-id="2f0de-109">*pOut*</span></span> 
</dt> <dd>

<span data-ttu-id="2f0de-110">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo de salida.</span><span class="sxs-lookup"><span data-stu-id="2f0de-110">Pointer to the output sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f0de-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f0de-111">Return value</span></span>

<span data-ttu-id="2f0de-112">La clase base devuelve E \_ inesperada.</span><span class="sxs-lookup"><span data-stu-id="2f0de-112">The base class returns E\_UNEXPECTED.</span></span>

<span data-ttu-id="2f0de-113">La clase derivada debe devolver un valor **HRESULT** , que indica que se ha realizado correctamente o se ha producido un error.</span><span class="sxs-lookup"><span data-stu-id="2f0de-113">The derived class should return an **HRESULT** value, indicating success or failure.</span></span> <span data-ttu-id="2f0de-114">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="2f0de-114">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="2f0de-115">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2f0de-115">Return code</span></span>                                                                             | <span data-ttu-id="2f0de-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f0de-116">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="2f0de-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="2f0de-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="2f0de-118">No entregue este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="2f0de-118">Do not deliver this sample.</span></span><br/> |
| <dl> <span data-ttu-id="2f0de-119"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="2f0de-119"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="2f0de-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="2f0de-120">Success.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="2f0de-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f0de-121">Remarks</span></span>

<span data-ttu-id="2f0de-122">Invalide este método para generar datos de salida.</span><span class="sxs-lookup"><span data-stu-id="2f0de-122">Override this method to produce output data.</span></span> <span data-ttu-id="2f0de-123">Lea los datos de entrada del ejemplo especificado por el parámetro *pIn* y escriba los datos nuevos en el ejemplo especificado por el parámetro *pOut* .</span><span class="sxs-lookup"><span data-stu-id="2f0de-123">Read the input data from the sample specified by the *pIn* parameter, and write the new data into the sample specified by the *pOut* parameter.</span></span>

<span data-ttu-id="2f0de-124">Antes de que el filtro llame a este método, copia las propiedades de la muestra de entrada en el ejemplo de salida.</span><span class="sxs-lookup"><span data-stu-id="2f0de-124">Before the filter calls this method, it copies the properties from the input sample to the output sample.</span></span> <span data-ttu-id="2f0de-125">El `Transform` método debe establecer las propiedades que difieren entre los dos ejemplos, mediante métodos **IMediaSample** o la interfaz [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) (si está disponible).</span><span class="sxs-lookup"><span data-stu-id="2f0de-125">The `Transform` method should set any properties that differ between the two samples, using **IMediaSample** methods or the [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) interface (if available).</span></span>

<span data-ttu-id="2f0de-126">Si el filtro no debe proporcionar este ejemplo (por ejemplo, para admitir el control de calidad), el método debe devolver S \_ false.</span><span class="sxs-lookup"><span data-stu-id="2f0de-126">If the filter should not deliver this sample (for example, to support quality control), the method should return S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f0de-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f0de-127">Requirements</span></span>



| <span data-ttu-id="2f0de-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f0de-128">Requirement</span></span> | <span data-ttu-id="2f0de-129">Value</span><span class="sxs-lookup"><span data-stu-id="2f0de-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f0de-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f0de-130">Header</span></span><br/>  | <dl> <span data-ttu-id="2f0de-131"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f0de-131"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2f0de-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f0de-132">Library</span></span><br/> | <dl> <span data-ttu-id="2f0de-133"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2f0de-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f0de-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f0de-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f0de-135">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="2f0de-135">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




