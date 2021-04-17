---
description: El método IsActive determina si el filtro está activo actualmente (en ejecución o en pausa).
ms.assetid: 3bbb50d5-6a07-4932-940c-4466b95e6412
title: Método CBaseFilter. IsActive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.IsActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63cf2cd78bb61562c9b4d6a09de3d88c88d4c643
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661078"
---
# <a name="cbasefilterisactive-method"></a><span data-ttu-id="1acb9-103">CBaseFilter. IsActive (método)</span><span class="sxs-lookup"><span data-stu-id="1acb9-103">CBaseFilter.IsActive method</span></span>

<span data-ttu-id="1acb9-104">El `IsActive` método determina si el filtro está activo actualmente (en ejecución o en pausa).</span><span class="sxs-lookup"><span data-stu-id="1acb9-104">The `IsActive` method determines whether the filter is currently active (running or paused).</span></span>

## <a name="syntax"></a><span data-ttu-id="1acb9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1acb9-105">Syntax</span></span>


```C++
BOOL IsActive();
```



## <a name="parameters"></a><span data-ttu-id="1acb9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1acb9-106">Parameters</span></span>

<span data-ttu-id="1acb9-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="1acb9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1acb9-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1acb9-108">Return value</span></span>

<span data-ttu-id="1acb9-109">Devuelve **true** si el filtro está en pausa o en ejecución, o **false** si se detiene.</span><span class="sxs-lookup"><span data-stu-id="1acb9-109">Returns **TRUE** if the filter is paused or running, or **FALSE** if it is stopped.</span></span>

## <a name="requirements"></a><span data-ttu-id="1acb9-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1acb9-110">Requirements</span></span>



| <span data-ttu-id="1acb9-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="1acb9-111">Requirement</span></span> | <span data-ttu-id="1acb9-112">Value</span><span class="sxs-lookup"><span data-stu-id="1acb9-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1acb9-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1acb9-113">Header</span></span><br/>  | <dl> <span data-ttu-id="1acb9-114"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1acb9-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1acb9-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1acb9-115">Library</span></span><br/> | <dl> <span data-ttu-id="1acb9-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1acb9-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1acb9-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="1acb9-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1acb9-118">**Clase CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="1acb9-118">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




