---
description: El método CheckReady consulta si se ha completado una transición de estado.
ms.assetid: dfa669ed-a5ab-498e-9fc2-ff15d6ddbc13
title: Método CBaseRenderer. CheckReady (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckReady
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 28c0c8bcb6efb0e3cbd648c1e45d36e8b18d4b74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660760"
---
# <a name="cbaserenderercheckready-method"></a><span data-ttu-id="4a9d0-103">CBaseRenderer. CheckReady, método</span><span class="sxs-lookup"><span data-stu-id="4a9d0-103">CBaseRenderer.CheckReady method</span></span>

<span data-ttu-id="4a9d0-104">El `CheckReady` método consulta si se ha completado una transición de estado.</span><span class="sxs-lookup"><span data-stu-id="4a9d0-104">The `CheckReady` method queries whether a state transition is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a9d0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4a9d0-105">Syntax</span></span>


```C++
BOOL CheckReady();
```



## <a name="parameters"></a><span data-ttu-id="4a9d0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4a9d0-106">Parameters</span></span>

<span data-ttu-id="4a9d0-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="4a9d0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4a9d0-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a9d0-108">Return value</span></span>

<span data-ttu-id="4a9d0-109">Devuelve **true** si la transición de estado está completa o **false** si el filtro sigue pasando a un nuevo estado.</span><span class="sxs-lookup"><span data-stu-id="4a9d0-109">Returns **TRUE** if the state transition is complete, or **FALSE** if the filter is still transitioning to a new state.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a9d0-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a9d0-110">Requirements</span></span>



| <span data-ttu-id="4a9d0-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a9d0-111">Requirement</span></span> | <span data-ttu-id="4a9d0-112">Value</span><span class="sxs-lookup"><span data-stu-id="4a9d0-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a9d0-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a9d0-113">Header</span></span><br/>  | <dl> <span data-ttu-id="4a9d0-114"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a9d0-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4a9d0-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4a9d0-115">Library</span></span><br/> | <dl> <span data-ttu-id="4a9d0-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="4a9d0-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a9d0-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="4a9d0-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a9d0-118">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="4a9d0-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="4a9d0-119">**CBaseRenderer::**</span><span class="sxs-lookup"><span data-stu-id="4a9d0-119">**CBaseRenderer::NotReady**</span></span>](cbaserenderer-notready.md)
</dt> <dt>

[<span data-ttu-id="4a9d0-120">**CBaseRenderer:: Ready**</span><span class="sxs-lookup"><span data-stu-id="4a9d0-120">**CBaseRenderer::Ready**</span></span>](cbaserenderer-ready.md)
</dt> </dl>

 

 




