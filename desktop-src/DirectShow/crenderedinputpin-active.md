---
description: 'Método CRenderedInputPin.Active: el método Active notifica al pin que el filtro ahora está activo. Este método invalida el método CBasePin::Active.'
ms.assetid: e98ca947-df2f-41a7-9785-b35bd1dde1e6
title: Método CRenderedInputPin.Active (Amextra.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d8c9b06f41454d2cb9a7ac35dd7e8f8b335632f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098933"
---
# <a name="crenderedinputpinactive-method"></a><span data-ttu-id="47fd0-104">Método CRenderedInputPin.Active</span><span class="sxs-lookup"><span data-stu-id="47fd0-104">CRenderedInputPin.Active method</span></span>

<span data-ttu-id="47fd0-105">El `Active` método notifica al pin que el filtro ahora está activo.</span><span class="sxs-lookup"><span data-stu-id="47fd0-105">The `Active` method notifies the pin that the filter is now active.</span></span> <span data-ttu-id="47fd0-106">Este método invalida el [**método CBasePin::Active.**](cbasepin-active.md)</span><span class="sxs-lookup"><span data-stu-id="47fd0-106">This method overrides the [**CBasePin::Active**](cbasepin-active.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="47fd0-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47fd0-107">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="47fd0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47fd0-108">Parameters</span></span>

<span data-ttu-id="47fd0-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="47fd0-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="47fd0-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="47fd0-110">Return value</span></span>

<span data-ttu-id="47fd0-111">Devuelve S \_ OK si se realiza correctamente o un código de error de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="47fd0-111">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="47fd0-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47fd0-112">Requirements</span></span>



| <span data-ttu-id="47fd0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="47fd0-113">Requirement</span></span> | <span data-ttu-id="47fd0-114">Value</span><span class="sxs-lookup"><span data-stu-id="47fd0-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47fd0-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="47fd0-115">Header</span></span><br/>  | <dl> <span data-ttu-id="47fd0-116"><dt>Amextra.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="47fd0-116"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="47fd0-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="47fd0-117">Library</span></span><br/> | <dl> <span data-ttu-id="47fd0-118"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="47fd0-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47fd0-119">Consulte también</span><span class="sxs-lookup"><span data-stu-id="47fd0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47fd0-120">**CRenderedInputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="47fd0-120">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




