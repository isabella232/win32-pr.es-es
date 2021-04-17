---
description: La función GetBitmapPalette devuelve la primera entrada de la paleta en una estructura VIDEOINFOHEADER.
ms.assetid: 7c620f81-31d9-408f-954d-aeff39f93956
title: Función GetBitmapPalette (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapPalette
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ffa4139c7aaece3e92a26fbf69fc02b8759f1613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680217"
---
# <a name="getbitmappalette-function"></a><span data-ttu-id="196c3-103">GetBitmapPalette función)</span><span class="sxs-lookup"><span data-stu-id="196c3-103">GetBitmapPalette function</span></span>

<span data-ttu-id="196c3-104">La `GetBitmapPalette` función devuelve la primera entrada de la paleta en una estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="196c3-104">The `GetBitmapPalette` function returns the first palette entry in a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="196c3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="196c3-105">Syntax</span></span>


```C++
const RGBQUAD* GetBitmapPalette(
   const VIDEOINFOHEADER *pVideoInfo
);
```



## <a name="parameters"></a><span data-ttu-id="196c3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="196c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="196c3-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="196c3-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="196c3-108">Puntero a una estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="196c3-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="196c3-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="196c3-109">Return value</span></span>

<span data-ttu-id="196c3-110">Devuelve un puntero a la primera entrada de la paleta.</span><span class="sxs-lookup"><span data-stu-id="196c3-110">Returns a pointer to the first palette entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="196c3-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="196c3-111">Requirements</span></span>



| <span data-ttu-id="196c3-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="196c3-112">Requirement</span></span> | <span data-ttu-id="196c3-113">Value</span><span class="sxs-lookup"><span data-stu-id="196c3-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="196c3-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="196c3-114">Header</span></span><br/>  | <dl> <span data-ttu-id="196c3-115"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="196c3-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="196c3-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="196c3-116">Library</span></span><br/> | <dl> <span data-ttu-id="196c3-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="196c3-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




