---
description: La clase CImageDisplay es una clase auxiliar para que los representadores de vídeo GDI administren el formato de presentación.
ms.assetid: c9221e5c-30c6-489a-89d7-132203314dc8
title: Clase CImageDisplay (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5a7cbb28c53d8ff357d4e5174d24f92ba2d0cad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681008"
---
# <a name="cimagedisplay-class"></a><span data-ttu-id="56144-103">Clase CImageDisplay</span><span class="sxs-lookup"><span data-stu-id="56144-103">CImageDisplay class</span></span>

![cimagedisplayclasshierarchy](images/wutil06.png)

<span data-ttu-id="56144-105">La `CImageDisplay` clase es una clase auxiliar para que los representadores de vídeo GDI administren el formato de presentación.</span><span class="sxs-lookup"><span data-stu-id="56144-105">The `CImageDisplay` class is a helper class for GDI video renderers to manage the display format.</span></span> <span data-ttu-id="56144-106">El objeto almacena una estructura de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) que describe el modo de presentación actual, que se inicializa en el método de constructor del objeto.</span><span class="sxs-lookup"><span data-stu-id="56144-106">The object stores a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure that describes the current display mode, which is initialized in the object's constructor method.</span></span> <span data-ttu-id="56144-107">El método **CheckMediaType** del objeto comprueba si un tipo de medio propuesto se puede representar de forma eficaz mediante GDI.</span><span class="sxs-lookup"><span data-stu-id="56144-107">The object's **CheckMediaType** method checks whether a proposed media type can be rendered efficiently using GDI.</span></span>



| <span data-ttu-id="56144-108">Variables de miembro protegidas</span><span class="sxs-lookup"><span data-stu-id="56144-108">Protected Member Variables</span></span>                                       | <span data-ttu-id="56144-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="56144-109">Description</span></span>                                                                            |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="56144-110">**m \_ Mostrar**</span><span class="sxs-lookup"><span data-stu-id="56144-110">**m\_Display**</span></span>](cimagedisplay-m-display.md)                    | <span data-ttu-id="56144-111">Estructura de **videoinfo** que describe el formato de presentación actual.</span><span class="sxs-lookup"><span data-stu-id="56144-111">**VIDEOINFO** structure that describes the current display format.</span></span>                     |
| <span data-ttu-id="56144-112">Métodos protegidos</span><span class="sxs-lookup"><span data-stu-id="56144-112">Protected Methods</span></span>                                                | <span data-ttu-id="56144-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="56144-113">Description</span></span>                                                                            |
| [<span data-ttu-id="56144-114">**CheckBitFields**</span><span class="sxs-lookup"><span data-stu-id="56144-114">**CheckBitFields**</span></span>](cimagedisplay-checkbitfields.md)           | <span data-ttu-id="56144-115">Valida las máscaras de color de una estructura de **videoinfo** .</span><span class="sxs-lookup"><span data-stu-id="56144-115">Validates the color masks in a **VIDEOINFO** structure.</span></span>                                |
| [<span data-ttu-id="56144-116">**CountPrefixBits**</span><span class="sxs-lookup"><span data-stu-id="56144-116">**CountPrefixBits**</span></span>](cimagedisplay-countprefixbits.md)         | <span data-ttu-id="56144-117">Calcula el número de bits cero al principio de un campo de bits especificado.</span><span class="sxs-lookup"><span data-stu-id="56144-117">Calculates the number of zero bits at the start of a specified bit field.</span></span>              |
| [<span data-ttu-id="56144-118">**CountSetBits**</span><span class="sxs-lookup"><span data-stu-id="56144-118">**CountSetBits**</span></span>](cimagedisplay-countsetbits.md)               | <span data-ttu-id="56144-119">Devuelve el número de bits establecidos en 1 en un campo de bits especificado.</span><span class="sxs-lookup"><span data-stu-id="56144-119">Returns the number of bits set to 1 in a specified bit field.</span></span>                          |
| <span data-ttu-id="56144-120">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="56144-120">Public Methods</span></span>                                                   | <span data-ttu-id="56144-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="56144-121">Description</span></span>                                                                            |
| [<span data-ttu-id="56144-122">**CheckHeaderValidity**</span><span class="sxs-lookup"><span data-stu-id="56144-122">**CheckHeaderValidity**</span></span>](cimagedisplay-checkheadervalidity.md) | <span data-ttu-id="56144-123">Valida una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="56144-123">Validates a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>                    |
| [<span data-ttu-id="56144-124">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="56144-124">**CheckMediaType**</span></span>](cimagedisplay-checkmediatype.md)           | <span data-ttu-id="56144-125">Determina si un tipo de medio propuesto es compatible con el formato de presentación.</span><span class="sxs-lookup"><span data-stu-id="56144-125">Determines whether a proposed media type is compatible with the display format.</span></span>        |
| [<span data-ttu-id="56144-126">**CheckPaletteHeader**</span><span class="sxs-lookup"><span data-stu-id="56144-126">**CheckPaletteHeader**</span></span>](cimagedisplay-checkpaletteheader.md)   | <span data-ttu-id="56144-127">Valida las entradas de la paleta en una estructura de **videoinfo** .</span><span class="sxs-lookup"><span data-stu-id="56144-127">Validates the palette entries in a **VIDEOINFO** structure.</span></span>                            |
| [<span data-ttu-id="56144-128">**CheckVideoType**</span><span class="sxs-lookup"><span data-stu-id="56144-128">**CheckVideoType**</span></span>](cimagedisplay-checkvideotype.md)           | <span data-ttu-id="56144-129">Comprueba si un formato de **videoinfo** especificado es compatible con el formato de presentación.</span><span class="sxs-lookup"><span data-stu-id="56144-129">Checks whether a specified **VIDEOINFO** format is compatible with the display format.</span></span> |
| [<span data-ttu-id="56144-130">**CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="56144-130">**CImageDisplay**</span></span>](cimagedisplay-cimagedisplay.md)             | <span data-ttu-id="56144-131">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="56144-131">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="56144-132">**GetBitMasks**</span><span class="sxs-lookup"><span data-stu-id="56144-132">**GetBitMasks**</span></span>](cimagedisplay-getbitmasks.md)                 | <span data-ttu-id="56144-133">Recupera las máscaras de color para un formato de **videoinfo** especificado.</span><span class="sxs-lookup"><span data-stu-id="56144-133">Retrieves the color masks for a specified **VIDEOINFO** format.</span></span>                        |
| [<span data-ttu-id="56144-134">**GetColourMask**</span><span class="sxs-lookup"><span data-stu-id="56144-134">**GetColourMask**</span></span>](cimagedisplay-getcolourmask.md)             | <span data-ttu-id="56144-135">Recupera las máscaras de color para el formato de presentación actual.</span><span class="sxs-lookup"><span data-stu-id="56144-135">Retrieves the color masks for the current display format.</span></span>                              |
| [<span data-ttu-id="56144-136">**GetDisplayDepth**</span><span class="sxs-lookup"><span data-stu-id="56144-136">**GetDisplayDepth**</span></span>](cimagedisplay-getdisplaydepth.md)         | <span data-ttu-id="56144-137">Recupera la profundidad de bits del modo de presentación actual.</span><span class="sxs-lookup"><span data-stu-id="56144-137">Retrieves the bit depth of the current display mode.</span></span>                                   |
| [<span data-ttu-id="56144-138">**GetDisplayFormat**</span><span class="sxs-lookup"><span data-stu-id="56144-138">**GetDisplayFormat**</span></span>](cimagedisplay-getdisplayformat.md)       | <span data-ttu-id="56144-139">Recupera un formato de vídeo que describe el modo de presentación actual.</span><span class="sxs-lookup"><span data-stu-id="56144-139">Retrieves a video format that describes the current display mode.</span></span>                      |
| [<span data-ttu-id="56144-140">**IsPalettised**</span><span class="sxs-lookup"><span data-stu-id="56144-140">**IsPalettised**</span></span>](cimagedisplay-ispalettised.md)               | <span data-ttu-id="56144-141">Retermines si el formato de presentación actual es de paleta.</span><span class="sxs-lookup"><span data-stu-id="56144-141">Retermines whether the current display format is palettized.</span></span>                           |
| [<span data-ttu-id="56144-142">**RefreshDisplayType**</span><span class="sxs-lookup"><span data-stu-id="56144-142">**RefreshDisplayType**</span></span>](cimagedisplay-refreshdisplaytype.md)   | <span data-ttu-id="56144-143">Actualiza el formato de vídeo del objeto para que coincida con la presentación especificada.</span><span class="sxs-lookup"><span data-stu-id="56144-143">Updates the object's video format to match the specified display</span></span>                       |



 

## <a name="requirements"></a><span data-ttu-id="56144-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56144-144">Requirements</span></span>



| <span data-ttu-id="56144-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="56144-145">Requirement</span></span> | <span data-ttu-id="56144-146">Value</span><span class="sxs-lookup"><span data-stu-id="56144-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56144-147">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56144-147">Header</span></span><br/>  | <dl> <span data-ttu-id="56144-148"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56144-148"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="56144-149">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="56144-149">Library</span></span><br/> | <dl> <span data-ttu-id="56144-150"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="56144-150"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




