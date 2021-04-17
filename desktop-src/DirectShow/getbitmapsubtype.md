---
description: La función GetBitmapSubtype devuelve el GUID del subtipo de medios para el mapa de bits especificado.
ms.assetid: 0af8a64b-8d3c-4308-9fd6-174864a1ca26
title: Función GetBitmapSubtype (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSubtype
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ba12ffcd1b50b920f28e1969444a2d31a9d073d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680213"
---
# <a name="getbitmapsubtype-function"></a><span data-ttu-id="a45c7-103">GetBitmapSubtype función)</span><span class="sxs-lookup"><span data-stu-id="a45c7-103">GetBitmapSubtype function</span></span>

<span data-ttu-id="a45c7-104">La `GetBitmapSubtype` función devuelve el **GUID** del subtipo de medios para el mapa de bits especificado.</span><span class="sxs-lookup"><span data-stu-id="a45c7-104">The `GetBitmapSubtype` function returns the media subtype **GUID** for the specified bitmap.</span></span>

## <a name="syntax"></a><span data-ttu-id="a45c7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a45c7-105">Syntax</span></span>


```C++
const GUID GetBitmapSubtype(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a><span data-ttu-id="a45c7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a45c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a45c7-107">*pHeader*</span><span class="sxs-lookup"><span data-stu-id="a45c7-107">*pHeader*</span></span> 
</dt> <dd>

<span data-ttu-id="a45c7-108">Puntero a una estructura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .</span><span class="sxs-lookup"><span data-stu-id="a45c7-108">Pointer to a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a45c7-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a45c7-109">Return value</span></span>

<span data-ttu-id="a45c7-110">Devuelve el **GUID** del subtipo de medio.</span><span class="sxs-lookup"><span data-stu-id="a45c7-110">Returns the media subtype **GUID**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a45c7-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a45c7-111">Remarks</span></span>

<span data-ttu-id="a45c7-112">En el caso de los tipos RGB sin comprimir, esta función asigna el campo **biBitCount** al subtipo.</span><span class="sxs-lookup"><span data-stu-id="a45c7-112">For uncompressed RGB types, this function maps the **biBitCount** field to the subtype.</span></span> <span data-ttu-id="a45c7-113">En el caso de los tipos de vídeo comprimidos, esta función usa la clase [**FOURCCMap**](fourccmap.md) para asignar el campo de **bicompresión** al subtipo.</span><span class="sxs-lookup"><span data-stu-id="a45c7-113">For compressed video types, this function uses the [**FOURCCMap**](fourccmap.md) class to map the **biCompression** field to the subtype.</span></span>

<span data-ttu-id="a45c7-114">Si la función no puede coincidir con el formato de un subtipo, el valor devuelto es GUID \_ null.</span><span class="sxs-lookup"><span data-stu-id="a45c7-114">If the function cannot match the format to a subtype, the return value is GUID\_NULL.</span></span>

## <a name="requirements"></a><span data-ttu-id="a45c7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a45c7-115">Requirements</span></span>



| <span data-ttu-id="a45c7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a45c7-116">Requirement</span></span> | <span data-ttu-id="a45c7-117">Value</span><span class="sxs-lookup"><span data-stu-id="a45c7-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a45c7-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a45c7-118">Header</span></span><br/>  | <dl> <span data-ttu-id="a45c7-119"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a45c7-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a45c7-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a45c7-120">Library</span></span><br/> | <dl> <span data-ttu-id="a45c7-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a45c7-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a45c7-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="a45c7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a45c7-123">Funciones de vídeo e imagen</span><span class="sxs-lookup"><span data-stu-id="a45c7-123">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




