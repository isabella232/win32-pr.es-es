---
description: El método GetResult recupera la lista de argumentos resultante, si existe.
ms.assetid: a2a8b17c-3dcf-4f59-89c3-f42070d2a8eb
title: Método CDeferredCommand. GetResult (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetResult
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e8c1638dc33be6457dd682f37e2ddd49e73a111a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671765"
---
# <a name="cdeferredcommandgetresult-method"></a><span data-ttu-id="c8dee-103">CDeferredCommand. GetResult (método)</span><span class="sxs-lookup"><span data-stu-id="c8dee-103">CDeferredCommand.GetResult method</span></span>

<span data-ttu-id="c8dee-104">El `GetResult` método recupera la lista de argumentos resultante, si existe.</span><span class="sxs-lookup"><span data-stu-id="c8dee-104">The `GetResult` method retrieves the resulting argument list, if one exists.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8dee-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8dee-105">Syntax</span></span>


```C++
VARIANT* GetResult();
```



## <a name="parameters"></a><span data-ttu-id="c8dee-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8dee-106">Parameters</span></span>

<span data-ttu-id="c8dee-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c8dee-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c8dee-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8dee-108">Return value</span></span>

<span data-ttu-id="c8dee-109">Devuelve un puntero a un **tipo Variant** que contiene la lista de argumentos del método, si existe.</span><span class="sxs-lookup"><span data-stu-id="c8dee-109">Returns a pointer to a **VARIANT** containing the method's argument list, if it exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8dee-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8dee-110">Requirements</span></span>



| <span data-ttu-id="c8dee-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8dee-111">Requirement</span></span> | <span data-ttu-id="c8dee-112">Value</span><span class="sxs-lookup"><span data-stu-id="c8dee-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8dee-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8dee-113">Header</span></span><br/>  | <dl> <span data-ttu-id="c8dee-114"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8dee-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c8dee-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c8dee-115">Library</span></span><br/> | <dl> <span data-ttu-id="c8dee-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c8dee-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8dee-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8dee-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8dee-118">**Clase CDeferredCommand**</span><span class="sxs-lookup"><span data-stu-id="c8dee-118">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




