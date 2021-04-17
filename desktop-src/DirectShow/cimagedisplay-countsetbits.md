---
description: El método CountSetBits devuelve el número de bits establecido en 1 en un campo de bits especificado.
ms.assetid: fc5701b8-88ff-4c23-9d26-854bb65cc55c
title: Método CImageDisplay. CountSetBits (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountSetBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cb425b08b524b1d36b622bcfffcc9f311dccbbdf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681134"
---
# <a name="cimagedisplaycountsetbits-method"></a><span data-ttu-id="80937-103">CImageDisplay. CountSetBits, método</span><span class="sxs-lookup"><span data-stu-id="80937-103">CImageDisplay.CountSetBits method</span></span>

<span data-ttu-id="80937-104">El `CountSetBits` método devuelve el número de bits establecidos en 1 en un campo de bits especificado.</span><span class="sxs-lookup"><span data-stu-id="80937-104">The `CountSetBits` method returns the number of bits set to 1 in a specified bit field.</span></span>

## <a name="syntax"></a><span data-ttu-id="80937-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80937-105">Syntax</span></span>


```C++
DWORD CountSetBits(
   const DWORD Field
);
```



## <a name="parameters"></a><span data-ttu-id="80937-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="80937-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80937-107">*Campo*</span><span class="sxs-lookup"><span data-stu-id="80937-107">*Field*</span></span> 
</dt> <dd>

<span data-ttu-id="80937-108">Especifica un campo de bits como un valor **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="80937-108">Specifies a bit field as a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80937-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80937-109">Return value</span></span>

<span data-ttu-id="80937-110">Devuelve el número de bits que se establecen en 1.</span><span class="sxs-lookup"><span data-stu-id="80937-110">Returns the number of bits that are set to 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="80937-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80937-111">Requirements</span></span>



| <span data-ttu-id="80937-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="80937-112">Requirement</span></span> | <span data-ttu-id="80937-113">Value</span><span class="sxs-lookup"><span data-stu-id="80937-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80937-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="80937-114">Header</span></span><br/>  | <dl> <span data-ttu-id="80937-115"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="80937-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="80937-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="80937-116">Library</span></span><br/> | <dl> <span data-ttu-id="80937-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="80937-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80937-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="80937-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80937-119">**Clase CImageDisplay**</span><span class="sxs-lookup"><span data-stu-id="80937-119">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




