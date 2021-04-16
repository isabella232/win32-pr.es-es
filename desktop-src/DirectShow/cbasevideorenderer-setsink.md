---
description: El método SetSink establece el objeto IQualityControl que recibirá los mensajes de calidad.
ms.assetid: f5789781-1871-4fea-9d1f-bd1a21b70439
title: Método CBaseVideoRenderer. SetSink (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9658ab4a1099e7baaef0a3e1a0ae3c0d495e89e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679094"
---
# <a name="cbasevideorenderersetsink-method"></a><span data-ttu-id="0ee21-103">CBaseVideoRenderer. SetSink, método</span><span class="sxs-lookup"><span data-stu-id="0ee21-103">CBaseVideoRenderer.SetSink method</span></span>

<span data-ttu-id="0ee21-104">El `SetSink` método establece el objeto [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) que recibirá los mensajes de calidad.</span><span class="sxs-lookup"><span data-stu-id="0ee21-104">The `SetSink` method sets the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) object that will receive quality messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ee21-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ee21-105">Syntax</span></span>


```C++
HRESULT SetSink(
   IQualityControl *piqc
);
```



## <a name="parameters"></a><span data-ttu-id="0ee21-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ee21-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ee21-107">*piqc*</span><span class="sxs-lookup"><span data-stu-id="0ee21-107">*piqc*</span></span> 
</dt> <dd>

<span data-ttu-id="0ee21-108">Puntero al objeto [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) al que se deben enviar las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="0ee21-108">Pointer to the [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) object to which the notifications should be sent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ee21-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ee21-109">Return value</span></span>

<span data-ttu-id="0ee21-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0ee21-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ee21-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ee21-111">Remarks</span></span>

<span data-ttu-id="0ee21-112">Esta función miembro implementa el método [**IQualityControl:: SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) en el representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0ee21-112">This member function implements the [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) method on the video renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ee21-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ee21-113">Requirements</span></span>



| <span data-ttu-id="0ee21-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ee21-114">Requirement</span></span> | <span data-ttu-id="0ee21-115">Value</span><span class="sxs-lookup"><span data-stu-id="0ee21-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ee21-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ee21-116">Header</span></span><br/>  | <dl> <span data-ttu-id="0ee21-117"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ee21-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0ee21-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0ee21-118">Library</span></span><br/> | <dl> <span data-ttu-id="0ee21-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0ee21-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ee21-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ee21-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ee21-121">**Clase CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="0ee21-121">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




