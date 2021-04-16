---
description: El método CanReconnectWhenActive consulta si el PIN admite reconexiones dinámicas.
ms.assetid: a2679987-7897-4b18-b06b-9ab8f2f3b9f5
title: Método CBasePin. CanReconnectWhenActive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CanReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89a072a26afe0087ce9adfed5b29eb1cc4280dac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671344"
---
# <a name="cbasepincanreconnectwhenactive-method"></a><span data-ttu-id="2d2f5-103">CBasePin. CanReconnectWhenActive, método</span><span class="sxs-lookup"><span data-stu-id="2d2f5-103">CBasePin.CanReconnectWhenActive method</span></span>

<span data-ttu-id="2d2f5-104">El `CanReconnectWhenActive` método consulta si el PIN admite reconexiones dinámicas.</span><span class="sxs-lookup"><span data-stu-id="2d2f5-104">The `CanReconnectWhenActive` method queries whether the pin supports dynamic reconnections.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d2f5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2d2f5-105">Syntax</span></span>


```C++
bool CanReconnectWhenActive();
```



## <a name="parameters"></a><span data-ttu-id="2d2f5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2d2f5-106">Parameters</span></span>

<span data-ttu-id="2d2f5-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2d2f5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2d2f5-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2d2f5-108">Return value</span></span>

<span data-ttu-id="2d2f5-109">Devuelve un valor booleano que especifica si el pin puede volver a conectarse dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="2d2f5-109">Returns a Boolean value that specifies whether the pin can dynamically reconnect.</span></span> <span data-ttu-id="2d2f5-110">Si **es true**, el PIN se puede volver a conectar dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="2d2f5-110">If **TRUE**, the pin can dynamically reconnect.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d2f5-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2d2f5-111">Remarks</span></span>

<span data-ttu-id="2d2f5-112">De forma predeterminada, debe detener un filtro antes de volver a conectar cualquiera de sus clavijas.</span><span class="sxs-lookup"><span data-stu-id="2d2f5-112">By default, you must stop a filter before reconnecting any of its pins.</span></span> <span data-ttu-id="2d2f5-113">Sin embargo, si un PIN admite la reconexión dinámica, se puede volver a conectar mientras el filtro está activo.</span><span class="sxs-lookup"><span data-stu-id="2d2f5-113">If a pin supports dynamic reconnection, however, it can reconnect while the filter is active.</span></span> <span data-ttu-id="2d2f5-114">Para obtener más información, vea [creación de gráficos dinámicos](dynamic-graph-building.md).</span><span class="sxs-lookup"><span data-stu-id="2d2f5-114">For more information, see [Dynamic Graph Building](dynamic-graph-building.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2d2f5-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d2f5-115">Requirements</span></span>



| <span data-ttu-id="2d2f5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d2f5-116">Requirement</span></span> | <span data-ttu-id="2d2f5-117">Value</span><span class="sxs-lookup"><span data-stu-id="2d2f5-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d2f5-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2d2f5-118">Header</span></span><br/>  | <dl> <span data-ttu-id="2d2f5-119"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2d2f5-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2d2f5-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2d2f5-120">Library</span></span><br/> | <dl> <span data-ttu-id="2d2f5-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2d2f5-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d2f5-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="2d2f5-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d2f5-123">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="2d2f5-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




