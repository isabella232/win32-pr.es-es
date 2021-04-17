---
description: La función ContainsPalette determina si una estructura VIDEOINFOHEADER especificada contiene una paleta.
ms.assetid: e87ab1af-a822-45d8-9326-08b450e11279
title: Función ContainsPalette (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ContainsPalette
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9417d9dd39f958e4a4caf68ef368d231a2097de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680510"
---
# <a name="containspalette-function"></a><span data-ttu-id="9b3c8-103">ContainsPalette función)</span><span class="sxs-lookup"><span data-stu-id="9b3c8-103">ContainsPalette function</span></span>

<span data-ttu-id="9b3c8-104">La función **ContainsPalette** determina si una estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) especificada contiene una paleta.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-104">The **ContainsPalette** function determines whether a specified [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure contains a palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b3c8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b3c8-105">Syntax</span></span>


```C++
BOOL ContainsPalette(
   const VIDEOINFOHEADER *pVideoInfo

);
```



## <a name="parameters"></a><span data-ttu-id="9b3c8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9b3c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9b3c8-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="9b3c8-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="9b3c8-108">Puntero a una estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="9b3c8-108">Pointer to a [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9b3c8-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9b3c8-109">Return value</span></span>

<span data-ttu-id="9b3c8-110">Devuelve **true** si bitdepth es 8 o menos (**bmiHeader. biBitCount**), o el número de índices de color es mayor que cero (**bmiHeader. biClrUsed**).</span><span class="sxs-lookup"><span data-stu-id="9b3c8-110">Returns **TRUE** if the bitdepth is 8 or less (**bmiHeader.biBitCount**), or the number of color indexes is more than zero (**bmiHeader.biClrUsed**).</span></span> <span data-ttu-id="9b3c8-111">Devuelve **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="9b3c8-111">Returns **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b3c8-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b3c8-112">Requirements</span></span>



| <span data-ttu-id="9b3c8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b3c8-113">Requirement</span></span> | <span data-ttu-id="9b3c8-114">Value</span><span class="sxs-lookup"><span data-stu-id="9b3c8-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b3c8-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b3c8-115">Header</span></span><br/>  | <dl> <span data-ttu-id="9b3c8-116"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9b3c8-116"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9b3c8-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b3c8-117">Library</span></span><br/> | <dl> <span data-ttu-id="9b3c8-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9b3c8-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b3c8-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b3c8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b3c8-120">Funciones de vídeo e imagen</span><span class="sxs-lookup"><span data-stu-id="9b3c8-120">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




