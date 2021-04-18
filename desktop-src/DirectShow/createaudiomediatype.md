---
description: La función CreateAudioMediaType Inicializa un tipo de archivo multimedia a partir de una estructura WAVEFORMATEX.
ms.assetid: 2571b7b4-86e9-443f-a99d-9ba48f469522
title: Función CreateAudioMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateAudioMediaType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef4e525762d4b6928e6a9095fad34f3f4f2e96fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680862"
---
# <a name="createaudiomediatype-function"></a><span data-ttu-id="a416a-103">CreateAudioMediaType función)</span><span class="sxs-lookup"><span data-stu-id="a416a-103">CreateAudioMediaType function</span></span>

<span data-ttu-id="a416a-104">La función **CreateAudioMediaType** Inicializa un tipo de archivo multimedia a partir de una estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a416a-104">The **CreateAudioMediaType** function initializes a media type from a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a416a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a416a-105">Syntax</span></span>


```C++
HRESULT STDAPI CreateAudioMediaType(
   const WAVEFORMATEX  *pwfx,
         AM_MEDIA_TYPE *pmt,
         BOOL          bSetFormat
);
```



## <a name="parameters"></a><span data-ttu-id="a416a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a416a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a416a-107">*pwfx*</span><span class="sxs-lookup"><span data-stu-id="a416a-107">*pwfx*</span></span> 
</dt> <dd>

<span data-ttu-id="a416a-108">Puntero a la estructura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) proporcionada.</span><span class="sxs-lookup"><span data-stu-id="a416a-108">Pointer to the supplied [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a416a-109">*p.p.*</span><span class="sxs-lookup"><span data-stu-id="a416a-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="a416a-110">Puntero a la estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que se va a inicializar.</span><span class="sxs-lookup"><span data-stu-id="a416a-110">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to initialize.</span></span>

</dd> <dt>

<span data-ttu-id="a416a-111">*bSetFormat*</span><span class="sxs-lookup"><span data-stu-id="a416a-111">*bSetFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="a416a-112">Marca que indica si se debe inicializar el bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="a416a-112">Flag indicating whether to initialize the format block.</span></span> <span data-ttu-id="a416a-113">Especifique **true** para inicializarlo o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a416a-113">Specify **TRUE** to initialize it, or **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a416a-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a416a-114">Return value</span></span>

<span data-ttu-id="a416a-115">Devuelve E \_ OUTOFMEMORY si no se pudo asignar memoria para los datos de formato; \_En caso contrario, es correcto.</span><span class="sxs-lookup"><span data-stu-id="a416a-115">Returns E\_OUTOFMEMORY if memory could not be allocated for the format data; S\_OK otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a416a-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a416a-116">Remarks</span></span>

<span data-ttu-id="a416a-117">Si el parámetro *bSetFormat* es **true**, el método asigna la memoria para el bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="a416a-117">If the *bSetFormat* parameter is **TRUE**, the method allocates the memory for the format block.</span></span> <span data-ttu-id="a416a-118">Si el parámetro *PMT* ya contiene un bloque de formato asignado, se producirá una fuga de memoria.</span><span class="sxs-lookup"><span data-stu-id="a416a-118">If the *pmt* parameter already contains an allocated format block, a memory leak will occur.</span></span> <span data-ttu-id="a416a-119">Para evitar una pérdida de memoria, llame a [**FreeMediaType**](freemediatype.md) antes de llamar a esta función.</span><span class="sxs-lookup"><span data-stu-id="a416a-119">To avoid a memory leak, call [**FreeMediaType**](freemediatype.md) before calling this function.</span></span> <span data-ttu-id="a416a-120">Cuando el método vuelva, llame de nuevo a **FreeMediaType** para liberar el bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="a416a-120">After the method returns, call **FreeMediaType** again to free the format block.</span></span>

## <a name="requirements"></a><span data-ttu-id="a416a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a416a-121">Requirements</span></span>



| <span data-ttu-id="a416a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a416a-122">Requirement</span></span> | <span data-ttu-id="a416a-123">Value</span><span class="sxs-lookup"><span data-stu-id="a416a-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a416a-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a416a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a416a-125"><dt>Mtype. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a416a-125"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="a416a-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a416a-126">Library</span></span><br/> | <dl> <span data-ttu-id="a416a-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a416a-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a416a-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="a416a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a416a-129">**Funciones de tipo de medio**</span><span class="sxs-lookup"><span data-stu-id="a416a-129">**Media Type Functions**</span></span>](media-type-functions.md)
</dt> </dl>

 

