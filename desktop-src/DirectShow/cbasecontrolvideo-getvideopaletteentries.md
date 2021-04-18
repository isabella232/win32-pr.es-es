---
description: El método GetVideoPaletteEntries recupera un intervalo de entradas de la paleta para el vídeo.
ms.assetid: 7ac12e28-daa7-4d6c-9983-401971e6704d
title: Método CBaseControlVideo. GetVideoPaletteEntries (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetVideoPaletteEntries
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fa354922e57436c0d9e3e18924dcf31afe1629e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690844"
---
# <a name="cbasecontrolvideogetvideopaletteentries-method"></a><span data-ttu-id="afe72-103">CBaseControlVideo. GetVideoPaletteEntries, método</span><span class="sxs-lookup"><span data-stu-id="afe72-103">CBaseControlVideo.GetVideoPaletteEntries method</span></span>

<span data-ttu-id="afe72-104">El `GetVideoPaletteEntries` método recupera un intervalo de entradas de la paleta para el vídeo.</span><span class="sxs-lookup"><span data-stu-id="afe72-104">The `GetVideoPaletteEntries` method retrieves a range of palette entries for the video.</span></span>

## <a name="syntax"></a><span data-ttu-id="afe72-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="afe72-105">Syntax</span></span>


```C++
HRESULT GetVideoPaletteEntries(
   long StartIndex,
   long Entries,
   long *pRetrieved,
   long *pPalette
);
```



## <a name="parameters"></a><span data-ttu-id="afe72-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="afe72-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afe72-107">*Super*</span><span class="sxs-lookup"><span data-stu-id="afe72-107">*StartIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="afe72-108">Entrada de la paleta de inicio de base cero.</span><span class="sxs-lookup"><span data-stu-id="afe72-108">Zero-based start palette entry.</span></span>

</dd> <dt>

<span data-ttu-id="afe72-109">*Entradas*</span><span class="sxs-lookup"><span data-stu-id="afe72-109">*Entries*</span></span> 
</dt> <dd>

<span data-ttu-id="afe72-110">Número de entradas necesarias.</span><span class="sxs-lookup"><span data-stu-id="afe72-110">Number of entries required.</span></span>

</dd> <dt>

<span data-ttu-id="afe72-111">*pRetrieved*</span><span class="sxs-lookup"><span data-stu-id="afe72-111">*pRetrieved*</span></span> 
</dt> <dd>

<span data-ttu-id="afe72-112">Puntero al número de colores obtenidos.</span><span class="sxs-lookup"><span data-stu-id="afe72-112">Pointer to the number of colors obtained.</span></span>

</dd> <dt>

<span data-ttu-id="afe72-113">*pPalette*</span><span class="sxs-lookup"><span data-stu-id="afe72-113">*pPalette*</span></span> 
</dt> <dd>

<span data-ttu-id="afe72-114">Puntero en el búfer de salida para los colores.</span><span class="sxs-lookup"><span data-stu-id="afe72-114">Pointer to output buffer for colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afe72-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="afe72-115">Return value</span></span>

<span data-ttu-id="afe72-116">Devuelve NoError si se realiza correctamente, VFW \_ e \_ no hay ninguna \_ paleta \_ disponible si los ejemplos de vídeo no tienen paleta de colores, e \_ OUTOFMEMORY si no hay suficiente memoria disponible, e \_ INVALIDARG si *StartIndex* no es válido o S \_ false si no hay colores en la paleta.</span><span class="sxs-lookup"><span data-stu-id="afe72-116">Returns NOERROR if successful, VFW\_E\_NO\_PALETTE\_AVAILABLE if the video samples has no color palette, E\_OUTOFMEMORY if there is not enough memory available, E\_INVALIDARG if *StartIndex* is invalid, or S\_FALSE if there are no colors in the palette.</span></span>

## <a name="remarks"></a><span data-ttu-id="afe72-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="afe72-117">Remarks</span></span>

<span data-ttu-id="afe72-118">Esta función miembro devuelve la paleta actual del vídeo como una matriz asignada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="afe72-118">This member function returns the current palette of the video as an array allocated by the user.</span></span> <span data-ttu-id="afe72-119">Para mantener la coherencia, use los miembros de la estructura de Win32 **PALETTEENTRY** para devolver los colores, en lugar de los miembros de la estructura **RGBQUAD** (aunque el parámetro es un **valor Long**).</span><span class="sxs-lookup"><span data-stu-id="afe72-119">To remain consistent, use the members in the Win32 **PALETTEENTRY** structure to return the colors, rather than the members in the **RGBQUAD** structure (although the parameter is a **LONG**).</span></span> <span data-ttu-id="afe72-120">El autor de la llamada asigna la memoria, por lo que basta con copiar cada uno de ellos a su vez.</span><span class="sxs-lookup"><span data-stu-id="afe72-120">The memory is allocated by the caller, so simply copy each in turn.</span></span> <span data-ttu-id="afe72-121">Determine que el número de entradas solicitadas y el desplazamiento de la posición de inicio son válidos.</span><span class="sxs-lookup"><span data-stu-id="afe72-121">Determine that the number of entries requested and the start position offset are both valid.</span></span> <span data-ttu-id="afe72-122">Si el número de entradas se evalúa como cero, se devuelve un \_ código S false.</span><span class="sxs-lookup"><span data-stu-id="afe72-122">If the number of entries evaluates to zero, return an S\_FALSE code.</span></span>

## <a name="requirements"></a><span data-ttu-id="afe72-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="afe72-123">Requirements</span></span>



| <span data-ttu-id="afe72-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="afe72-124">Requirement</span></span> | <span data-ttu-id="afe72-125">Value</span><span class="sxs-lookup"><span data-stu-id="afe72-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afe72-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="afe72-126">Header</span></span><br/>  | <dl> <span data-ttu-id="afe72-127"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="afe72-127"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="afe72-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="afe72-128">Library</span></span><br/> | <dl> <span data-ttu-id="afe72-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="afe72-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afe72-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="afe72-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afe72-131">**Clase CBaseControlVideo**</span><span class="sxs-lookup"><span data-stu-id="afe72-131">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




