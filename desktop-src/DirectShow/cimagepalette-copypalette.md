---
description: El método CopyPalette copia la paleta de cualquier estructura de videoinfo en cualquier estructura de videoinformación de paleta.
ms.assetid: ea06b40b-3f96-4c11-921c-52f3a44e0a30
title: Método CImagePalette. CopyPalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette.CopyPalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b429c5fd4d3d0e0e28cd0662fbee0a1ac926ddc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671543"
---
# <a name="cimagepalettecopypalette-method"></a><span data-ttu-id="1933f-103">CImagePalette. CopyPalette, método</span><span class="sxs-lookup"><span data-stu-id="1933f-103">CImagePalette.CopyPalette method</span></span>

<span data-ttu-id="1933f-104">El `CopyPalette` método copia la paleta de cualquier estructura de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) en cualquier estructura de **videoinformación** de paleta.</span><span class="sxs-lookup"><span data-stu-id="1933f-104">The `CopyPalette` method copies the palette from any [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure to any palettized **VIDEOINFO** structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="1933f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1933f-105">Syntax</span></span>


```C++
HRESULT CopyPalette(
   const CMediaType *pSrc,
   const CMediaType *pDest
);
```



## <a name="parameters"></a><span data-ttu-id="1933f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1933f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1933f-107">*pSrc*</span><span class="sxs-lookup"><span data-stu-id="1933f-107">*pSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="1933f-108">Puntero al tipo de medio de origen.</span><span class="sxs-lookup"><span data-stu-id="1933f-108">Pointer to the source media type.</span></span>

</dd> <dt>

<span data-ttu-id="1933f-109">*pDest*</span><span class="sxs-lookup"><span data-stu-id="1933f-109">*pDest*</span></span> 
</dt> <dd>

<span data-ttu-id="1933f-110">Puntero al tipo de medio de destino.</span><span class="sxs-lookup"><span data-stu-id="1933f-110">Pointer to the destination media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1933f-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1933f-111">Return value</span></span>

<span data-ttu-id="1933f-112">Devuelve S \_ OK si se copió la paleta.</span><span class="sxs-lookup"><span data-stu-id="1933f-112">Returns S\_OK if the palette was copied.</span></span> <span data-ttu-id="1933f-113">Devuelve S \_ false si el tipo de medio de origen o de destino no tiene una paleta.</span><span class="sxs-lookup"><span data-stu-id="1933f-113">Returns S\_FALSE if either the source or destination media type does not have a palette.</span></span>

## <a name="remarks"></a><span data-ttu-id="1933f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1933f-114">Remarks</span></span>

<span data-ttu-id="1933f-115">El tipo de medio *pDest* debe ser un formato de paleta con una profundidad de color de 8 bits o menos.</span><span class="sxs-lookup"><span data-stu-id="1933f-115">The *pDest* media type must be a palettized format with a color depth of 8 bits or less.</span></span> <span data-ttu-id="1933f-116">El tipo de medio *pSrc* puede ser cualquier tipo de [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) con una paleta, incluidos los formatos YUV y de color verdadero con entradas de paleta.</span><span class="sxs-lookup"><span data-stu-id="1933f-116">The *pSrc* media type can be any [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) type with a palette, including YUV and true-color formats with palette entries.</span></span> <span data-ttu-id="1933f-117">El método copia las entradas de la paleta de *pSrc* en una nueva paleta y asocia la nueva paleta a *pDest*.</span><span class="sxs-lookup"><span data-stu-id="1933f-117">The method copies the palette entries from *pSrc* into a new palette, and attaches the new palette to *pDest*.</span></span>

## <a name="requirements"></a><span data-ttu-id="1933f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1933f-118">Requirements</span></span>



| <span data-ttu-id="1933f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1933f-119">Requirement</span></span> | <span data-ttu-id="1933f-120">Value</span><span class="sxs-lookup"><span data-stu-id="1933f-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1933f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1933f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1933f-122"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1933f-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1933f-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1933f-123">Library</span></span><br/> | <dl> <span data-ttu-id="1933f-124"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1933f-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1933f-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="1933f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1933f-126">**Clase CImagePalette**</span><span class="sxs-lookup"><span data-stu-id="1933f-126">**CImagePalette Class**</span></span>](cimagepalette.md)
</dt> </dl>

 

 




