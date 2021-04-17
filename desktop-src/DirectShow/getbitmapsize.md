---
description: La función GetBitmapSize calcula el número de bytes requeridos por un mapa de bits independiente del dispositivo (DIB). Esta función simplemente llama a la macro de Dib.
ms.assetid: ce23cdf2-9804-4d2e-b9ef-16e54b2d571e
title: Función GetBitmapSize (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 004201cf3ff839aa1301dcfff0240a73a9128e50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653661"
---
# <a name="getbitmapsize-function"></a><span data-ttu-id="2a61a-104">GetBitmapSize función)</span><span class="sxs-lookup"><span data-stu-id="2a61a-104">GetBitmapSize function</span></span>

<span data-ttu-id="2a61a-105">La `GetBitmapSize` función calcula el número de bytes requeridos por un mapa de bits independiente del dispositivo (DIB).</span><span class="sxs-lookup"><span data-stu-id="2a61a-105">The `GetBitmapSize` function calculates the number of bytes required by a device-independent bitmap (DIB).</span></span> <span data-ttu-id="2a61a-106">Esta función simplemente llama a la macro de [**DIB**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize) .</span><span class="sxs-lookup"><span data-stu-id="2a61a-106">This function simply calls the [**DIBSIZE**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-dibsize) macro.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a61a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2a61a-107">Syntax</span></span>


```C++
DWORD GetBitmapSize(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="2a61a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a61a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a61a-109">*pHeader*</span><span class="sxs-lookup"><span data-stu-id="2a61a-109">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="2a61a-110">Puntero a una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="2a61a-110">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a61a-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a61a-111">Return value</span></span>

<span data-ttu-id="2a61a-112">Devuelve el tamaño en bytes.</span><span class="sxs-lookup"><span data-stu-id="2a61a-112">Returns the size in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a61a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a61a-113">Requirements</span></span>



| <span data-ttu-id="2a61a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a61a-114">Requirement</span></span> | <span data-ttu-id="2a61a-115">Value</span><span class="sxs-lookup"><span data-stu-id="2a61a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a61a-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2a61a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2a61a-117"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a61a-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="2a61a-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2a61a-118">Library</span></span><br/> | <dl> <span data-ttu-id="2a61a-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2a61a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a61a-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a61a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a61a-121">Funciones de vídeo e imagen</span><span class="sxs-lookup"><span data-stu-id="2a61a-121">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




