---
description: La función GetBitmapFormatSize calcula el tamaño necesario para una estructura de videoinfo que puede contener una estructura BITMAPINFOHEADER especificada.
ms.assetid: a559415a-070f-4674-be12-a65a46025809
title: Función GetBitmapFormatSize (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapFormatSize
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39a64f6d975e403de6c177906b23ef7e09f29ddf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653662"
---
# <a name="getbitmapformatsize-function"></a><span data-ttu-id="a6592-103">GetBitmapFormatSize función)</span><span class="sxs-lookup"><span data-stu-id="a6592-103">GetBitmapFormatSize function</span></span>

<span data-ttu-id="a6592-104">La `GetBitmapFormatSize` función calcula el tamaño necesario para una estructura de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) que puede contener una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) especificada.</span><span class="sxs-lookup"><span data-stu-id="a6592-104">The `GetBitmapFormatSize` function calculates the size needed for a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure that can hold a specified [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6592-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a6592-105">Syntax</span></span>


```C++
LONG GetBitmapFormatSize(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="a6592-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a6592-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6592-107">*pHeader*</span><span class="sxs-lookup"><span data-stu-id="a6592-107">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="a6592-108">Puntero a una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="a6592-108">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6592-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a6592-109">Return value</span></span>

<span data-ttu-id="a6592-110">Devuelve el tamaño, en bytes.</span><span class="sxs-lookup"><span data-stu-id="a6592-110">Returns the size, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6592-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6592-111">Remarks</span></span>

<span data-ttu-id="a6592-112">Una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) puede ir seguida de máscaras de color o de paletas, por lo que puede ser difícil determinar el número de bytes necesarios para construir una estructura de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) a partir de una estructura **BITMAPINFOHEADER** existente.</span><span class="sxs-lookup"><span data-stu-id="a6592-112">A [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure might be followed by color masks or palette entries, so it can be difficult to determine the number of bytes required to construct a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure from an existing **BITMAPINFOHEADER** structure.</span></span>

<span data-ttu-id="a6592-113">Para copiar una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) en una estructura de [**videoinfo**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) , utilice la macro [**Header**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header) , que calcula el desplazamiento correcto.</span><span class="sxs-lookup"><span data-stu-id="a6592-113">To copy a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure into a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure, use the [**HEADER**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-header) macro, which calculates the correct offset.</span></span>

## <a name="examples"></a><span data-ttu-id="a6592-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a6592-114">Examples</span></span>


```
LONG size = GetBitmapFormatSize(&bmi);

VIDEOINFO *pVi = static_cast<VIDEOINFO*>(CoTaskMemAlloc(size));

if (pVi != NULL)
{
    CopyMemory(HEADER(pVi), &bmi, sizeof(BITMAPINFOHEADER));
}
```



## <a name="requirements"></a><span data-ttu-id="a6592-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6592-115">Requirements</span></span>



| <span data-ttu-id="a6592-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6592-116">Requirement</span></span> | <span data-ttu-id="a6592-117">Value</span><span class="sxs-lookup"><span data-stu-id="a6592-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6592-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6592-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a6592-119"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a6592-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a6592-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a6592-120">Library</span></span><br/> | <dl> <span data-ttu-id="a6592-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a6592-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6592-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6592-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6592-123">Funciones de vídeo e imagen</span><span class="sxs-lookup"><span data-stu-id="a6592-123">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




