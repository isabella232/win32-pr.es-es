---
description: La función ConvertVideoInfoToVideoInfo2 convierte un tipo de medio que usa VIDEOINFOHEADER en uno que utiliza VIDEOINFOHEADER2.
ms.assetid: d938bfc0-a5ae-475b-b183-56ff39b4bae1
title: Función ConvertVideoInfoToVideoInfo2 (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConvertVideoInfoToVideoInfo2
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54611c83c30ad65a806a077dc51c933a9f881636
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678879"
---
# <a name="convertvideoinfotovideoinfo2-function"></a><span data-ttu-id="4aedd-103">ConvertVideoInfoToVideoInfo2 función)</span><span class="sxs-lookup"><span data-stu-id="4aedd-103">ConvertVideoInfoToVideoInfo2 function</span></span>

<span data-ttu-id="4aedd-104">La `ConvertVideoInfoToVideoInfo2` función convierte un tipo de medio que usa [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) en uno que usa [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span><span class="sxs-lookup"><span data-stu-id="4aedd-104">The `ConvertVideoInfoToVideoInfo2` function converts a media type that uses [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) to one that uses [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span></span>

## <a name="syntax"></a><span data-ttu-id="4aedd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4aedd-105">Syntax</span></span>


```C++
HRESULT STDAPI ConvertVideoInfoToVideoInfo2(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="4aedd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4aedd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4aedd-107">*p.p.*</span><span class="sxs-lookup"><span data-stu-id="4aedd-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="4aedd-108">Puntero a la estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="4aedd-108">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to convert.</span></span> <span data-ttu-id="4aedd-109">La estructura debe tener el formato de tipo de formato \_ videoinfo.</span><span class="sxs-lookup"><span data-stu-id="4aedd-109">The structure must have format type FORMAT\_VideoInfo.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4aedd-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4aedd-110">Return value</span></span>

<span data-ttu-id="4aedd-111">Devuelve S \_ OK o E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="4aedd-111">Returns S\_OK or E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="4aedd-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4aedd-112">Remarks</span></span>

<span data-ttu-id="4aedd-113">Esta función asigna una nueva estructura **VIDEOINFOHEADER2** , copia los miembros de la estructura **VIDEOINFOHEADER** en ella y reemplaza la estructura anterior por la nueva estructura en el bloque de formato del tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="4aedd-113">This function allocates a new **VIDEOINFOHEADER2** structure, copies the members of the **VIDEOINFOHEADER** structure into it, and replaces the old structure with the new structure in the format block of the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="4aedd-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4aedd-114">Requirements</span></span>



| <span data-ttu-id="4aedd-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4aedd-115">Requirement</span></span> | <span data-ttu-id="4aedd-116">Value</span><span class="sxs-lookup"><span data-stu-id="4aedd-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4aedd-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4aedd-117">Header</span></span><br/>  | <dl> <span data-ttu-id="4aedd-118"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4aedd-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4aedd-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4aedd-119">Library</span></span><br/> | <dl> <span data-ttu-id="4aedd-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="4aedd-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aedd-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="4aedd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aedd-122">Funciones de vídeo e imagen</span><span class="sxs-lookup"><span data-stu-id="4aedd-122">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




