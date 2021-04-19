---
description: La función EqualPins comprueba si dos patillas están en el mismo objeto.
ms.assetid: b6a92cb6-f4a9-4a14-831c-3b123e4692c0
title: Función EqualPins (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EqualPins
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fdf499b494f41a0acc5cc446bc92deade61c045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690081"
---
# <a name="equalpins-function"></a><span data-ttu-id="6ba3b-103">EqualPins función)</span><span class="sxs-lookup"><span data-stu-id="6ba3b-103">EqualPins function</span></span>

<span data-ttu-id="6ba3b-104">La función EqualPins comprueba si dos patillas están en el mismo objeto.</span><span class="sxs-lookup"><span data-stu-id="6ba3b-104">The EqualPins function checks if two pins are on the same object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ba3b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ba3b-105">Syntax</span></span>


```C++
BOOL EqualPins(
   IUnknown *pPin1,
   IUnknown *pPin2
);
```



## <a name="parameters"></a><span data-ttu-id="6ba3b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ba3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ba3b-107">*pPin1*</span><span class="sxs-lookup"><span data-stu-id="6ba3b-107">*pPin1*</span></span> 
</dt> <dd>

<span data-ttu-id="6ba3b-108">Puntero a un PIN.</span><span class="sxs-lookup"><span data-stu-id="6ba3b-108">Pointer to one pin.</span></span>

</dd> <dt>

<span data-ttu-id="6ba3b-109">*pPin2*</span><span class="sxs-lookup"><span data-stu-id="6ba3b-109">*pPin2*</span></span> 
</dt> <dd>

<span data-ttu-id="6ba3b-110">Puntero al otro PIN.</span><span class="sxs-lookup"><span data-stu-id="6ba3b-110">Pointer to the other pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ba3b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ba3b-111">Return value</span></span>

<span data-ttu-id="6ba3b-112">Devuelve **true** si ambos PIN están en el mismo objeto o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="6ba3b-112">Returns **TRUE** if both pins are on the same object, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ba3b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ba3b-113">Requirements</span></span>



| <span data-ttu-id="6ba3b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ba3b-114">Requirement</span></span> | <span data-ttu-id="6ba3b-115">Value</span><span class="sxs-lookup"><span data-stu-id="6ba3b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ba3b-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ba3b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6ba3b-117"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ba3b-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6ba3b-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6ba3b-118">Library</span></span><br/> | <dl> <span data-ttu-id="6ba3b-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6ba3b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ba3b-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ba3b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ba3b-121">Funciones auxiliares misceláneas</span><span class="sxs-lookup"><span data-stu-id="6ba3b-121">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> </dl>

 

 




