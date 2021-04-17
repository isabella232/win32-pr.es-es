---
description: El método PreparePalette configura una paleta basándose en un tipo de medio del filtro propietario.
ms.assetid: cb012391-39ab-4ad1-aeb7-ec25010ac64a
title: Método CImagePalette. PreparePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.PreparePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9b09804b2ee6ad9fbda394a7fb8f9f188b46453
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670493"
---
# <a name="cimagepalettepreparepalette-method"></a><span data-ttu-id="a2141-103">CImagePalette. PreparePalette, método</span><span class="sxs-lookup"><span data-stu-id="a2141-103">CImagePalette.PreparePalette method</span></span>

<span data-ttu-id="a2141-104">El `PreparePalette` método configura una paleta, basándose en un tipo de medio del filtro propietario.</span><span class="sxs-lookup"><span data-stu-id="a2141-104">The `PreparePalette` method sets up a palette, based on a media type from the owning filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2141-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a2141-105">Syntax</span></span>


```C++
HRESULT PreparePalette(
   const CMediaType *pmtNew,
   const CMediaType *pmtOld,
         LPSTR      szDevice
);
```



## <a name="parameters"></a><span data-ttu-id="a2141-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a2141-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2141-107">*pmtNew*</span><span class="sxs-lookup"><span data-stu-id="a2141-107">*pmtNew*</span></span> 
</dt> <dd>

<span data-ttu-id="a2141-108">Puntero al nuevo tipo de archivo multimedia.</span><span class="sxs-lookup"><span data-stu-id="a2141-108">Pointer to the new media type.</span></span> <span data-ttu-id="a2141-109">El bloque de formato debe ser una estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="a2141-109">The format block must be a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a2141-110">*pmtOld*</span><span class="sxs-lookup"><span data-stu-id="a2141-110">*pmtOld*</span></span> 
</dt> <dd>

<span data-ttu-id="a2141-111">Puntero al tipo de medio anterior.</span><span class="sxs-lookup"><span data-stu-id="a2141-111">Pointer to the old media type.</span></span> <span data-ttu-id="a2141-112">Si el tipo de medio se establece por primera vez, este parámetro puede ser un tipo vacío sin bloque de formato.</span><span class="sxs-lookup"><span data-stu-id="a2141-112">If the media type is being set for the first time, this parameter can be an empty type with no format block.</span></span> <span data-ttu-id="a2141-113">De lo contrario, el bloque de formato debe ser una estructura **VIDEOINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="a2141-113">Otherwise, the format block must be a **VIDEOINFOHEADER** structure.</span></span>

</dd> <dt>

<span data-ttu-id="a2141-114">*szDevice*</span><span class="sxs-lookup"><span data-stu-id="a2141-114">*szDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="a2141-115">Puntero a una cadena que contiene el nombre del dispositivo de pantalla, devuelto por la función **EnumDisplayDevices** de GDI.</span><span class="sxs-lookup"><span data-stu-id="a2141-115">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="a2141-116">Para usar el dispositivo de pantalla principal, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="a2141-116">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2141-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2141-117">Return value</span></span>

<span data-ttu-id="a2141-118">Devuelve S \_ OK si se actualizó la paleta o S \_ false si no ha cambiado la paleta.</span><span class="sxs-lookup"><span data-stu-id="a2141-118">Returns S\_OK if the palette was updated, or S\_FALSE if the palette did not change.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2141-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2141-119">Remarks</span></span>

<span data-ttu-id="a2141-120">Si es necesario actualizar la paleta, este método realiza las acciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="a2141-120">If the palette needs to be updated, this method performs the following actions:</span></span>

-   <span data-ttu-id="a2141-121">Llama a [**CImagePalette:: MakePalette**](cimagepalette-makepalette.md) para crear una nueva paleta lógica.</span><span class="sxs-lookup"><span data-stu-id="a2141-121">Calls [**CImagePalette::MakePalette**](cimagepalette-makepalette.md) to create a new logical palette.</span></span>
-   <span data-ttu-id="a2141-122">Envía un evento de la [**paleta de EC \_ \_ cambiada**](ec-palette-changed.md) al administrador de gráficos de filtro.</span><span class="sxs-lookup"><span data-stu-id="a2141-122">Sends an [**EC\_PALETTE\_CHANGED**](ec-palette-changed.md) event to the Filter Graph Manager.</span></span>
-   <span data-ttu-id="a2141-123">Llama a [**CBaseWindow:: SetPalette**](cbasewindow-setpalette.md) en el objeto **CBaseWindow** .</span><span class="sxs-lookup"><span data-stu-id="a2141-123">Calls [**CBaseWindow::SetPalette**](cbasewindow-setpalette.md) on the **CBaseWindow** object.</span></span>
-   <span data-ttu-id="a2141-124">Llama a [**CDrawImage:: IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md) en el objeto **CDrawImage** .</span><span class="sxs-lookup"><span data-stu-id="a2141-124">Calls [**CDrawImage::IncrementPaletteVersion**](cdrawimage-incrementpaletteversion.md) on the **CDrawImage** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2141-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2141-125">Requirements</span></span>



| <span data-ttu-id="a2141-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2141-126">Requirement</span></span> | <span data-ttu-id="a2141-127">Value</span><span class="sxs-lookup"><span data-stu-id="a2141-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2141-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2141-128">Header</span></span><br/>  | <dl> <span data-ttu-id="a2141-129"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2141-129"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a2141-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a2141-130">Library</span></span><br/> | <dl> <span data-ttu-id="a2141-131"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a2141-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2141-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2141-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2141-133">**Clase CImagePalette**</span><span class="sxs-lookup"><span data-stu-id="a2141-133">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




