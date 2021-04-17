---
description: El método SetReconnectWhenActive especifica si el PIN admite reconexiones dinámicas.
ms.assetid: 64776008-5d1b-461c-a446-8cd6124276c0
title: Método CBasePin. SetReconnectWhenActive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10840ad60c858f69164b19f2460a0039cd332700
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670345"
---
# <a name="cbasepinsetreconnectwhenactive-method"></a><span data-ttu-id="a86f9-103">CBasePin. SetReconnectWhenActive, método</span><span class="sxs-lookup"><span data-stu-id="a86f9-103">CBasePin.SetReconnectWhenActive method</span></span>

<span data-ttu-id="a86f9-104">El `SetReconnectWhenActive` método especifica si el PIN admite reconexiones dinámicas.</span><span class="sxs-lookup"><span data-stu-id="a86f9-104">The `SetReconnectWhenActive` method specifies whether the pin supports dynamic reconnections.</span></span>

## <a name="syntax"></a><span data-ttu-id="a86f9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a86f9-105">Syntax</span></span>


```C++
void SetReconnectWhenActive(
   bool bCanReconnect
);
```



## <a name="parameters"></a><span data-ttu-id="a86f9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a86f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a86f9-107">*bCanReconnect*</span><span class="sxs-lookup"><span data-stu-id="a86f9-107">*bCanReconnect*</span></span> 
</dt> <dd>

<span data-ttu-id="a86f9-108">Valor booleano que especifica si el pin puede volver a conectarse dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="a86f9-108">Boolean value that specifies whether the pin can dynamically reconnect.</span></span> <span data-ttu-id="a86f9-109">Si **es true**, el PIN se puede volver a conectar dinámicamente.</span><span class="sxs-lookup"><span data-stu-id="a86f9-109">If **TRUE**, the pin can dynamically reconnect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a86f9-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a86f9-110">Return value</span></span>

<span data-ttu-id="a86f9-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a86f9-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a86f9-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a86f9-112">Remarks</span></span>

<span data-ttu-id="a86f9-113">De forma predeterminada, debe detener un filtro antes de volver a conectar cualquiera de sus clavijas.</span><span class="sxs-lookup"><span data-stu-id="a86f9-113">By default, you must stop a filter before reconnecting any of its pins.</span></span> <span data-ttu-id="a86f9-114">Si el PIN se puede volver a conectar mientras el filtro está activo, llame a este método con un valor de **true**.</span><span class="sxs-lookup"><span data-stu-id="a86f9-114">If the pin can reconnect while the filter is active, call this method with a value of **TRUE**.</span></span> <span data-ttu-id="a86f9-115">Para obtener más información, vea [creación de gráficos dinámicos](dynamic-graph-building.md).</span><span class="sxs-lookup"><span data-stu-id="a86f9-115">For more information, see [Dynamic Graph Building](dynamic-graph-building.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a86f9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a86f9-116">Requirements</span></span>



| <span data-ttu-id="a86f9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a86f9-117">Requirement</span></span> | <span data-ttu-id="a86f9-118">Value</span><span class="sxs-lookup"><span data-stu-id="a86f9-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a86f9-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a86f9-119">Header</span></span><br/>  | <dl> <span data-ttu-id="a86f9-120"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a86f9-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a86f9-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a86f9-121">Library</span></span><br/> | <dl> <span data-ttu-id="a86f9-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a86f9-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a86f9-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="a86f9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a86f9-124">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="a86f9-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




