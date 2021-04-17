---
description: La función GetTrueColorType recupera el nombre legible de un subtipo de vídeo.
ms.assetid: 479a020c-b55c-44ec-9096-5528113a4b74
title: Función GetTrueColorType (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetTrueColorType
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c262031045eed3755fe2d19d3bd703a347e6117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653636"
---
# <a name="gettruecolortype-function"></a><span data-ttu-id="0c1e3-103">GetTrueColorType función)</span><span class="sxs-lookup"><span data-stu-id="0c1e3-103">GetTrueColorType function</span></span>

<span data-ttu-id="0c1e3-104">La función **GetTrueColorType** recupera el nombre legible de un subtipo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0c1e3-104">The **GetTrueColorType** function retrieves the human-readable name of a video subtype.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c1e3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c1e3-105">Syntax</span></span>


```C++
const GUID GetTrueColorType(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="0c1e3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0c1e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c1e3-107">*pHeader*</span><span class="sxs-lookup"><span data-stu-id="0c1e3-107">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="0c1e3-108">Puntero a una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) que define el mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="0c1e3-108">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure that defines the bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c1e3-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0c1e3-109">Return value</span></span>

<span data-ttu-id="0c1e3-110">Devuelve MEDIASUBTYPE \_ RGB555 o MEDIASUBTYPE \_ RGB565.</span><span class="sxs-lookup"><span data-stu-id="0c1e3-110">Returns MEDIASUBTYPE\_RGB555 or MEDIASUBTYPE\_RGB565.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c1e3-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c1e3-111">Requirements</span></span>



| <span data-ttu-id="0c1e3-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c1e3-112">Requirement</span></span> | <span data-ttu-id="0c1e3-113">Value</span><span class="sxs-lookup"><span data-stu-id="0c1e3-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c1e3-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0c1e3-114">Header</span></span><br/>  | <dl> <span data-ttu-id="0c1e3-115"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0c1e3-115"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0c1e3-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0c1e3-116">Library</span></span><br/> | <dl> <span data-ttu-id="0c1e3-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0c1e3-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c1e3-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c1e3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c1e3-119">Funciones de vídeo e imagen</span><span class="sxs-lookup"><span data-stu-id="0c1e3-119">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




