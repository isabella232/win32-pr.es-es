---
description: El método InitializeOutputSample recupera un nuevo ejemplo de salida y lo inicializa.
ms.assetid: a4f8f514-cf1a-4f8f-ac17-17378705c2ea
title: CTransformFilter.Inimétodo tializeOutputSample (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.InitializeOutputSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: efe7e62936c6feb1984a339a67783cdbc1e4f124
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661034"
---
# <a name="ctransformfilterinitializeoutputsample-method"></a><span data-ttu-id="3350c-103">CTransformFilter.Inimétodo tializeOutputSample</span><span class="sxs-lookup"><span data-stu-id="3350c-103">CTransformFilter.InitializeOutputSample method</span></span>

<span data-ttu-id="3350c-104">El `InitializeOutputSample` método recupera un nuevo ejemplo de salida y lo inicializa.</span><span class="sxs-lookup"><span data-stu-id="3350c-104">The `InitializeOutputSample` method retrieves a new output sample and initializes it.</span></span>

## <a name="syntax"></a><span data-ttu-id="3350c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3350c-105">Syntax</span></span>


```C++
HRESULT InitializeOutputSample(
   IMediaSample *pSample,
   IMediaSample **ppOutSample
);
```



## <a name="parameters"></a><span data-ttu-id="3350c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3350c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3350c-107">*pSample*</span><span class="sxs-lookup"><span data-stu-id="3350c-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="3350c-108">Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del ejemplo de entrada.</span><span class="sxs-lookup"><span data-stu-id="3350c-108">Pointer to the input sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> <dt>

<span data-ttu-id="3350c-109">*ppOutSample*</span><span class="sxs-lookup"><span data-stu-id="3350c-109">*ppOutSample*</span></span> 
</dt> <dd>

<span data-ttu-id="3350c-110">Recibe un puntero a la interfaz **IMediaSample** del ejemplo de salida.</span><span class="sxs-lookup"><span data-stu-id="3350c-110">Receives a pointer to the output sample's **IMediaSample** interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3350c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3350c-111">Return value</span></span>

<span data-ttu-id="3350c-112">Devuelve S \_ OK u otro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3350c-112">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3350c-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3350c-113">Remarks</span></span>

<span data-ttu-id="3350c-114">El método [**CTransformFilter:: Receive**](ctransformfilter-receive.md) llama a este método para preparar el ejemplo de salida.</span><span class="sxs-lookup"><span data-stu-id="3350c-114">This method is called by the [**CTransformFilter::Receive**](ctransformfilter-receive.md) method to prepare the output sample.</span></span> <span data-ttu-id="3350c-115">Por lo general, no es necesario llamar a este método en la clase derivada, a menos que se invalide el método **Receive** .</span><span class="sxs-lookup"><span data-stu-id="3350c-115">Generally you do not have to call this method in your derived class, unless you override the **Receive** method.</span></span>

<span data-ttu-id="3350c-116">Este método recupera un nuevo ejemplo del asignador del terminal de salida.</span><span class="sxs-lookup"><span data-stu-id="3350c-116">This method retrieves a new sample from the output pin's allocator.</span></span> <span data-ttu-id="3350c-117">Después, copia las propiedades de ejemplo del ejemplo de entrada en el ejemplo de salida.</span><span class="sxs-lookup"><span data-stu-id="3350c-117">Then it copies the sample properties from the input sample to the output sample.</span></span> <span data-ttu-id="3350c-118">Las propiedades de ejemplo se definen en la estructura de [**\_ \_ propiedades AM SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .</span><span class="sxs-lookup"><span data-stu-id="3350c-118">The sample properties are defined in the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3350c-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3350c-119">Requirements</span></span>



| <span data-ttu-id="3350c-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3350c-120">Requirement</span></span> | <span data-ttu-id="3350c-121">Value</span><span class="sxs-lookup"><span data-stu-id="3350c-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3350c-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3350c-122">Header</span></span><br/>  | <dl> <span data-ttu-id="3350c-123"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3350c-123"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3350c-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3350c-124">Library</span></span><br/> | <dl> <span data-ttu-id="3350c-125"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3350c-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3350c-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="3350c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3350c-127">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="3350c-127">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




