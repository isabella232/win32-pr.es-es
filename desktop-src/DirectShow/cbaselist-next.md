---
description: El método siguiente recupera la posición siguiente en la lista.
ms.assetid: ba9753b0-c82e-4772-84a7-e9982de3b8ad
title: Método CBaseList. Next (Wxlist. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseList.Next
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f8a09ec91191437fbfb851ce92824b118a5440ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670926"
---
# <a name="cbaselistnext-method"></a><span data-ttu-id="58d22-103">CBaseList. Next (método)</span><span class="sxs-lookup"><span data-stu-id="58d22-103">CBaseList.Next method</span></span>

<span data-ttu-id="58d22-104">El `Next` método recupera la posición siguiente en la lista.</span><span class="sxs-lookup"><span data-stu-id="58d22-104">The `Next` method retrieves the next position in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="58d22-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="58d22-105">Syntax</span></span>


```C++
POSITION Next(
   POSITION pos
);
```



## <a name="parameters"></a><span data-ttu-id="58d22-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58d22-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58d22-107">*pos*</span><span class="sxs-lookup"><span data-stu-id="58d22-107">*pos*</span></span> 
</dt> <dd>

<span data-ttu-id="58d22-108">Valor de posición.</span><span class="sxs-lookup"><span data-stu-id="58d22-108">POSITION value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58d22-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58d22-109">Return value</span></span>

<span data-ttu-id="58d22-110">Devuelve el indicador de posición que sigue a la posición especificada por *pos*.</span><span class="sxs-lookup"><span data-stu-id="58d22-110">Returns the position indicator that follows the position specified by *pos*.</span></span>

## <a name="remarks"></a><span data-ttu-id="58d22-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="58d22-111">Remarks</span></span>

<span data-ttu-id="58d22-112">Si *pos* es la última posición de la lista, el método devuelve **null**.</span><span class="sxs-lookup"><span data-stu-id="58d22-112">If *pos* is the last position in the list, the method returns **NULL**.</span></span> <span data-ttu-id="58d22-113">Si *pos* es **null**, el método devuelve la primera posición de la lista.</span><span class="sxs-lookup"><span data-stu-id="58d22-113">If *pos* is **NULL**, the method returns the first position in the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="58d22-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58d22-114">Requirements</span></span>



| <span data-ttu-id="58d22-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="58d22-115">Requirement</span></span> | <span data-ttu-id="58d22-116">Value</span><span class="sxs-lookup"><span data-stu-id="58d22-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58d22-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="58d22-117">Header</span></span><br/>  | <dl> <span data-ttu-id="58d22-118"><dt>Wxlist. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="58d22-118"><dt>Wxlist.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="58d22-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="58d22-119">Library</span></span><br/> | <dl> <span data-ttu-id="58d22-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="58d22-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58d22-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="58d22-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58d22-122">**Clase CBaseList**</span><span class="sxs-lookup"><span data-stu-id="58d22-122">**CBaseList Class**</span></span>](cbaselist.md)
</dt> </dl>

 

 




