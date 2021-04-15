---
description: El método DisplaySampleTimes dibuja las marcas de tiempo de un ejemplo multimedia en la parte superior de la imagen de vídeo.
ms.assetid: 3741dc74-5311-4cb1-9e6b-4a8bf6113477
title: Método CDrawImage. DisplaySampleTimes (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DisplaySampleTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9988aaedf9a1c01c83412cdbe9e00533556c9b15
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661397"
---
# <a name="cdrawimagedisplaysampletimes-method"></a><span data-ttu-id="e6feb-103">CDrawImage. DisplaySampleTimes, método</span><span class="sxs-lookup"><span data-stu-id="e6feb-103">CDrawImage.DisplaySampleTimes method</span></span>

<span data-ttu-id="e6feb-104">El `DisplaySampleTimes` método dibuja las marcas de tiempo de un ejemplo multimedia en la parte superior de la imagen de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e6feb-104">The `DisplaySampleTimes` method draws the time stamps of a media sample on top of the video image.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6feb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e6feb-105">Syntax</span></span>


```C++
void DisplaySampleTimes(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="e6feb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e6feb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6feb-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="e6feb-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="e6feb-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e6feb-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6feb-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e6feb-109">Return value</span></span>

<span data-ttu-id="e6feb-110">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="e6feb-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6feb-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e6feb-111">Remarks</span></span>

<span data-ttu-id="e6feb-112">Solo se llama a este método en las compilaciones de depuración.</span><span class="sxs-lookup"><span data-stu-id="e6feb-112">This method is called only in debug builds.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6feb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6feb-113">Requirements</span></span>



| <span data-ttu-id="e6feb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6feb-114">Requirement</span></span> | <span data-ttu-id="e6feb-115">Value</span><span class="sxs-lookup"><span data-stu-id="e6feb-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6feb-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6feb-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e6feb-117"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6feb-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e6feb-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6feb-118">Library</span></span><br/> | <dl> <span data-ttu-id="e6feb-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e6feb-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6feb-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="e6feb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6feb-121">**Clase CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="e6feb-121">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




