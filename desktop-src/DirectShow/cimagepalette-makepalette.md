---
description: El método MakePalette crea una paleta lógica a partir de la tabla de colores en un formato de vídeo.
ms.assetid: f158e529-d683-4210-818d-21a834fc7683
title: Método CImagePalette. MakePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.MakePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 20c4484b2666b25b5d713ede450a9a5a99f93348
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679037"
---
# <a name="cimagepalettemakepalette-method"></a><span data-ttu-id="9e687-103">CImagePalette. MakePalette, método</span><span class="sxs-lookup"><span data-stu-id="9e687-103">CImagePalette.MakePalette method</span></span>

<span data-ttu-id="9e687-104">El `MakePalette` método crea una paleta lógica a partir de la tabla de colores en un formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9e687-104">The `MakePalette` method creates a logical palette from the color table in a video format.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e687-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9e687-105">Syntax</span></span>


```C++
HPALETTE MakePalette(
   const VIDEOINFOHEADER *pVideoInfo,
         LPSTR           szDevice
);
```



## <a name="parameters"></a><span data-ttu-id="9e687-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9e687-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e687-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="9e687-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="9e687-108">Puntero a una estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) que contiene la tabla de colores.</span><span class="sxs-lookup"><span data-stu-id="9e687-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure that contains the color table.</span></span>

</dd> <dt>

<span data-ttu-id="9e687-109">*szDevice*</span><span class="sxs-lookup"><span data-stu-id="9e687-109">*szDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="9e687-110">Puntero a una cadena que contiene el nombre del dispositivo de pantalla, devuelto por la función **EnumDisplayDevices** de GDI.</span><span class="sxs-lookup"><span data-stu-id="9e687-110">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="9e687-111">Para usar el dispositivo de pantalla principal, establezca este parámetro en **null**.</span><span class="sxs-lookup"><span data-stu-id="9e687-111">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e687-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9e687-112">Return value</span></span>

<span data-ttu-id="9e687-113">Si se realiza correctamente, devuelve un identificador a la paleta.</span><span class="sxs-lookup"><span data-stu-id="9e687-113">If successful, returns a handle to the palette.</span></span> <span data-ttu-id="9e687-114">De lo contrario, devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="9e687-114">Otherwise, returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e687-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e687-115">Requirements</span></span>



| <span data-ttu-id="9e687-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e687-116">Requirement</span></span> | <span data-ttu-id="9e687-117">Value</span><span class="sxs-lookup"><span data-stu-id="9e687-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e687-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e687-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9e687-119"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e687-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9e687-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9e687-120">Library</span></span><br/> | <dl> <span data-ttu-id="9e687-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9e687-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e687-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e687-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e687-123">**Clase CImagePalette**</span><span class="sxs-lookup"><span data-stu-id="9e687-123">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




