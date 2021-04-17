---
description: La función CheckVideoInfoType comprueba un tipo de medio que contenga una estructura de formato VIDEOINFOHEADER para algunos errores comunes que pueden producir desbordamientos de búfer o desbordamientos de enteros.
ms.assetid: 7ffca7de-26f9-4d8d-b70e-231eca462211
title: Función CheckVideoInfoType (Checkbmi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CheckVideoInfoType
api_type:
- HeaderDef
api_location:
- checkbmi.h
ms.openlocfilehash: 7c3a3c9603f974458ed3012dc651815abd432645
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660824"
---
# <a name="checkvideoinfotype-function"></a><span data-ttu-id="8ee96-103">CheckVideoInfoType función)</span><span class="sxs-lookup"><span data-stu-id="8ee96-103">CheckVideoInfoType function</span></span>

<span data-ttu-id="8ee96-104">La `CheckVideoInfoType` función comprueba un tipo de medio que contiene una estructura de formato [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) para algunos errores comunes que pueden producir desbordamientos de búfer o desbordamientos de enteros.</span><span class="sxs-lookup"><span data-stu-id="8ee96-104">The `CheckVideoInfoType` function checks a media type that contains a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) format structure for certain common errors that can cause buffer overruns or integer overflows.</span></span>

> [!Note]  
> <span data-ttu-id="8ee96-105">Esta función no garantiza que el tipo de medio sea válido o que el código que usa la estructura sea seguro.</span><span class="sxs-lookup"><span data-stu-id="8ee96-105">This function does not guarantee that the media type is valid or that code using the structure is secure.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8ee96-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ee96-106">Syntax</span></span>


```C++
HRESULT CheckVideoInfoType(
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="8ee96-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ee96-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ee96-108">*p.p.*</span><span class="sxs-lookup"><span data-stu-id="8ee96-108">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="8ee96-109">Puntero a la estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que se va a validar</span><span class="sxs-lookup"><span data-stu-id="8ee96-109">Pointer to the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure to validate</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ee96-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ee96-110">Return value</span></span>

<span data-ttu-id="8ee96-111">Devuelve uno de los siguientes valores **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8ee96-111">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="8ee96-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8ee96-112">Return code</span></span>                                                                                                | <span data-ttu-id="8ee96-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ee96-113">Description</span></span>                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------|
| <dl> <span data-ttu-id="8ee96-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="8ee96-114"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="8ee96-115">Correcto.</span><span class="sxs-lookup"><span data-stu-id="8ee96-115">Success.</span></span><br/>                |
| <dl> <span data-ttu-id="8ee96-116"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="8ee96-116"><dt>**E\_POINTER**</dt></span></span> </dl>                  | <span data-ttu-id="8ee96-117">Valor de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="8ee96-117">**NULL** pointer value.</span></span><br/> |
| <dl> <span data-ttu-id="8ee96-118"><dt>**\_tipo VFW \_ E \_ no \_ aceptado**</dt></span><span class="sxs-lookup"><span data-stu-id="8ee96-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="8ee96-119">Tipo de medio no válido.</span><span class="sxs-lookup"><span data-stu-id="8ee96-119">Invalid media type.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="8ee96-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ee96-120">Remarks</span></span>

<span data-ttu-id="8ee96-121">Esta función llama a [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) para validar la estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) en el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="8ee96-121">This function calls [**ValidateBitmapInfoHeader**](validatebitmapinfoheader.md) to validate the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure in the media type.</span></span> <span data-ttu-id="8ee96-122">Si el tipo de formato no es FORMAT \_ info, la función devuelve el \_ tipo VFW E \_ \_ no \_ aceptado.</span><span class="sxs-lookup"><span data-stu-id="8ee96-122">If the format type is not FORMAT\_VideoInfo, the function returns VFW\_E\_TYPE\_NOT\_ACCEPTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ee96-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ee96-123">Requirements</span></span>



| <span data-ttu-id="8ee96-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ee96-124">Requirement</span></span> | <span data-ttu-id="8ee96-125">Value</span><span class="sxs-lookup"><span data-stu-id="8ee96-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ee96-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ee96-126">Header</span></span><br/> | <dl> <span data-ttu-id="8ee96-127"><dt>Checkbmi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ee96-127"><dt>Checkbmi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ee96-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ee96-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ee96-129">Funciones de vídeo e imagen</span><span class="sxs-lookup"><span data-stu-id="8ee96-129">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




