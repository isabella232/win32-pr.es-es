---
description: La función GetBitCount devuelve el número de bits por píxel utilizado por un subtipo de vídeo especificado. Esta función solo es válida para los subtipos RGB no comprimidos.
ms.assetid: 876b91c8-50ba-4217-b79c-7f7ec1c22b83
title: Función GetBitCount (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitCount
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6fed9b24ebf2e95b2408de30a407904e6bd3c1c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680218"
---
# <a name="getbitcount-function"></a><span data-ttu-id="7a338-104">GetBitCount función)</span><span class="sxs-lookup"><span data-stu-id="7a338-104">GetBitCount function</span></span>

<span data-ttu-id="7a338-105">La `GetBitCount` función devuelve el número de bits por píxel utilizado por un subtipo de vídeo especificado.</span><span class="sxs-lookup"><span data-stu-id="7a338-105">The `GetBitCount` function returns the number of bits per pixel used by a specified video subtype.</span></span> <span data-ttu-id="7a338-106">Esta función solo es válida para los subtipos RGB no comprimidos.</span><span class="sxs-lookup"><span data-stu-id="7a338-106">This function is valid for uncompressed RGB subtypes only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a338-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7a338-107">Syntax</span></span>


```C++
WORD GetBitCount(
   const GUID *pSubtype
);
```



## <a name="parameters"></a><span data-ttu-id="7a338-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7a338-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a338-109">*pSubtype*</span><span class="sxs-lookup"><span data-stu-id="7a338-109">*pSubtype*</span></span> 
</dt> <dd>

<span data-ttu-id="7a338-110">Puntero a un **GUID** de subtipo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7a338-110">Pointer to a video subtype **GUID**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a338-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7a338-111">Return value</span></span>

<span data-ttu-id="7a338-112">Devuelve el número de bits por píxel para este subtipo, o el valor **USHRT \_ Max** si no se reconoce el subtipo.</span><span class="sxs-lookup"><span data-stu-id="7a338-112">Returns the number of bits per pixel for this subtype, or the value **USHRT\_MAX** if the subtype is not recognized.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a338-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a338-113">Requirements</span></span>



| <span data-ttu-id="7a338-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a338-114">Requirement</span></span> | <span data-ttu-id="7a338-115">Value</span><span class="sxs-lookup"><span data-stu-id="7a338-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a338-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7a338-116">Header</span></span><br/>  | <dl> <span data-ttu-id="7a338-117"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7a338-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7a338-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7a338-118">Library</span></span><br/> | <dl> <span data-ttu-id="7a338-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7a338-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a338-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="7a338-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a338-121">Funciones de vídeo e imagen</span><span class="sxs-lookup"><span data-stu-id="7a338-121">Video and Image Functions</span></span>](video-and-image-functions.md)
</dt> </dl>

 

 




