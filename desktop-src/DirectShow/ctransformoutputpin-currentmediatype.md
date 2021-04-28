---
description: 'Método CTransformOutputPin.CurrentMediaType: el método CurrentMediaType recupera el tipo de medio para la conexión de pin actual.'
ms.assetid: 1c42664d-160a-4f76-9d7a-40414c5c1704
title: Método CTransformOutputPin.CurrentMediaType (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CurrentMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0cb40310afb1c22d00a5394c0a0667fc8d22eb03
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094913"
---
# <a name="ctransformoutputpincurrentmediatype-method"></a><span data-ttu-id="4a11b-103">Método CTransformOutputPin.CurrentMediaType</span><span class="sxs-lookup"><span data-stu-id="4a11b-103">CTransformOutputPin.CurrentMediaType method</span></span>

<span data-ttu-id="4a11b-104">El `CurrentMediaType` método recupera el tipo de medio para la conexión de pin actual.</span><span class="sxs-lookup"><span data-stu-id="4a11b-104">The `CurrentMediaType` method retrieves the media type for the current pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a11b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a11b-105">Syntax</span></span>


```C++
CMediaType& CurrentMediaType();
```



## <a name="parameters"></a><span data-ttu-id="4a11b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a11b-106">Parameters</span></span>

<span data-ttu-id="4a11b-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="4a11b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4a11b-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a11b-108">Return value</span></span>

<span data-ttu-id="4a11b-109">Devuelve una referencia a la variable [**miembro CBasePin::m \_ mt.**](cbasepin-m-mt.md)</span><span class="sxs-lookup"><span data-stu-id="4a11b-109">Returns a reference to the [**CBasePin::m\_mt**](cbasepin-m-mt.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a11b-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a11b-110">Requirements</span></span>



| <span data-ttu-id="4a11b-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a11b-111">Requirement</span></span> | <span data-ttu-id="4a11b-112">Value</span><span class="sxs-lookup"><span data-stu-id="4a11b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a11b-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a11b-113">Header</span></span><br/>  | <dl> <span data-ttu-id="4a11b-114"><dt>Transfrm.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a11b-114"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4a11b-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4a11b-115">Library</span></span><br/> | <dl> <span data-ttu-id="4a11b-116"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="4a11b-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




