---
description: Se llama al método Receive cuando el objeto recibe un ejemplo multimedia del terminal de salida. La clase derivada debe implementar este método.
ms.assetid: ef45388b-b038-4838-b76b-dbbdc5388495
title: Método CPullPin. Receive (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a651822378b6a3c0754ecbd5ace4a5e464f014f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680831"
---
# <a name="cpullpinreceive-method"></a><span data-ttu-id="2f20f-104">CPullPin. Receive (método)</span><span class="sxs-lookup"><span data-stu-id="2f20f-104">CPullPin.Receive method</span></span>

<span data-ttu-id="2f20f-105">`Receive`Se llama al método cuando el objeto recibe un ejemplo multimedia del terminal de salida.</span><span class="sxs-lookup"><span data-stu-id="2f20f-105">The `Receive` method is called when the object receives a media sample from the output pin.</span></span> <span data-ttu-id="2f20f-106">La clase derivada debe implementar este método.</span><span class="sxs-lookup"><span data-stu-id="2f20f-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f20f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f20f-107">Syntax</span></span>


```C++
virtual HRESULT Receive(
   IMediaSample *pSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="2f20f-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f20f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f20f-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="2f20f-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="2f20f-110">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo multimedia.</span><span class="sxs-lookup"><span data-stu-id="2f20f-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f20f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f20f-111">Return value</span></span>

<span data-ttu-id="2f20f-112">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2f20f-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2f20f-113">Si se devuelve un valor distinto de S \_ OK, se detendrá el subproceso de extracción de datos.</span><span class="sxs-lookup"><span data-stu-id="2f20f-113">Returning a value other than S\_OK will stop the data-pulling thread.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f20f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f20f-114">Remarks</span></span>

<span data-ttu-id="2f20f-115">Se llama a este método siempre que llega un nuevo ejemplo del código PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="2f20f-115">This method is called whenever a new sample arrives from the output pin.</span></span> <span data-ttu-id="2f20f-116">Escriba este método de la misma manera que el método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .</span><span class="sxs-lookup"><span data-stu-id="2f20f-116">Write this method in the same manner as the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method.</span></span>

<span data-ttu-id="2f20f-117">Las marcas de tiempo del ejemplo especifican los desplazamientos de bytes con respecto a la posición inicial original que se especificó en el método [**CPullPin:: Seek**](cpullpin-seek.md) .</span><span class="sxs-lookup"><span data-stu-id="2f20f-117">The time stamps on the sample specify the byte offsets, relative to the original start position that was specified in [**CPullPin::Seek**](cpullpin-seek.md) method.</span></span>

<span data-ttu-id="2f20f-118">La posición inicial se redondea hacia abajo hasta el límite de alineación más cercano y la posición de detención se redondea al límite de alineación más cercano.</span><span class="sxs-lookup"><span data-stu-id="2f20f-118">The start position is rounded down to the nearest alignment boundary, and the stop position is rounded up to the nearest alignment boundary.</span></span> <span data-ttu-id="2f20f-119">Además, si la posición de detención supera la duración total, se usa la duración en su lugar.</span><span class="sxs-lookup"><span data-stu-id="2f20f-119">Also, if the stop position exceeds the total duration, the duration is used instead.</span></span>

<span data-ttu-id="2f20f-120">Todas las marcas de tiempo se proporcionan como un desplazamiento de bytes multiplicado por 10 millones, definidas como unidades de constantes.</span><span class="sxs-lookup"><span data-stu-id="2f20f-120">All time stamps are given as a byte offset multiplied by 10,000,000, defined as the constant UNITS.</span></span> <span data-ttu-id="2f20f-121">Por lo tanto, teóricamente un segundo es un byte.</span><span class="sxs-lookup"><span data-stu-id="2f20f-121">Thus, notionally one second is one byte.</span></span> <span data-ttu-id="2f20f-122">Para buscar los desplazamientos de bytes reales, llame a [**IMediaSample:: getTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) y divida los resultados por unidades.</span><span class="sxs-lookup"><span data-stu-id="2f20f-122">To find the actual byte offsets, call [**IMediaSample::GetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-gettime) and divide the results by UNITS.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f20f-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f20f-123">Requirements</span></span>



| <span data-ttu-id="2f20f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f20f-124">Requirement</span></span> | <span data-ttu-id="2f20f-125">Value</span><span class="sxs-lookup"><span data-stu-id="2f20f-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f20f-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f20f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="2f20f-127"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f20f-127"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="2f20f-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f20f-128">Library</span></span><br/> | <dl> <span data-ttu-id="2f20f-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2f20f-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f20f-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="2f20f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f20f-131">**Clase CPullPin**</span><span class="sxs-lookup"><span data-stu-id="2f20f-131">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




