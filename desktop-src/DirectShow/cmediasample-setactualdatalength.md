---
description: 'El método SetActualDataLength establece la longitud de los datos válidos en el búfer. Este método implementa el método IMediaSample:: SetActualDataLength.'
ms.assetid: a80a67ef-e490-4874-a123-f2d193cec4d7
title: Método CMediaSample. SetActualDataLength (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetActualDataLength
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 825b02f43195424f9ceb5ecd23c4dcf26727ef8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670531"
---
# <a name="cmediasamplesetactualdatalength-method"></a><span data-ttu-id="eb3dd-104">CMediaSample. SetActualDataLength, método</span><span class="sxs-lookup"><span data-stu-id="eb3dd-104">CMediaSample.SetActualDataLength method</span></span>

<span data-ttu-id="eb3dd-105">El `SetActualDataLength` método establece la longitud de los datos válidos en el búfer.</span><span class="sxs-lookup"><span data-stu-id="eb3dd-105">The `SetActualDataLength` method sets the length of the valid data in the buffer.</span></span> <span data-ttu-id="eb3dd-106">Este método implementa el método [**IMediaSample:: SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) .</span><span class="sxs-lookup"><span data-stu-id="eb3dd-106">This method implements the [**IMediaSample::SetActualDataLength**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setactualdatalength) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb3dd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb3dd-107">Syntax</span></span>


```C++
HRESULT SetActualDataLength(
   long lLen
);
```



## <a name="parameters"></a><span data-ttu-id="eb3dd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eb3dd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb3dd-109">*lLen*</span><span class="sxs-lookup"><span data-stu-id="eb3dd-109">*lLen*</span></span> 
</dt> <dd>

<span data-ttu-id="eb3dd-110">Longitud de los datos válidos, en bytes.</span><span class="sxs-lookup"><span data-stu-id="eb3dd-110">Length of the valid data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb3dd-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eb3dd-111">Return value</span></span>

<span data-ttu-id="eb3dd-112">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="eb3dd-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="eb3dd-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="eb3dd-113">Return code</span></span>                                                                                             | <span data-ttu-id="eb3dd-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb3dd-114">Description</span></span>                                                 |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="eb3dd-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="eb3dd-115"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="eb3dd-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="eb3dd-116">Success.</span></span><br/>                                         |
| <dl> <span data-ttu-id="eb3dd-117"><dt>**desbordamiento de búfer de VFW \_ E \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="eb3dd-117"><dt>**VFW\_E\_BUFFER\_OVERFLOW**</dt></span></span> </dl> | <span data-ttu-id="eb3dd-118">*lLen* es mayor que el tamaño de búfer asignado.</span><span class="sxs-lookup"><span data-stu-id="eb3dd-118">*lLen* is larger than the allocated buffer size.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eb3dd-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eb3dd-119">Remarks</span></span>

<span data-ttu-id="eb3dd-120">Este método establece la variable miembro [**CMediaSample:: m \_ lActual**](cmediasample-m-lactual.md) .</span><span class="sxs-lookup"><span data-stu-id="eb3dd-120">This method sets the [**CMediaSample::m\_lActual**](cmediasample-m-lactual.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb3dd-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb3dd-121">Requirements</span></span>



| <span data-ttu-id="eb3dd-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb3dd-122">Requirement</span></span> | <span data-ttu-id="eb3dd-123">Value</span><span class="sxs-lookup"><span data-stu-id="eb3dd-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb3dd-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eb3dd-124">Header</span></span><br/>  | <dl> <span data-ttu-id="eb3dd-125"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb3dd-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="eb3dd-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eb3dd-126">Library</span></span><br/> | <dl> <span data-ttu-id="eb3dd-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="eb3dd-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb3dd-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb3dd-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb3dd-129">**Clase CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="eb3dd-129">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




