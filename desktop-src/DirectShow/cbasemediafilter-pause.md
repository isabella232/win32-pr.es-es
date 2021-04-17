---
description: Pausa el objeto. Implementa el método IMediaFilter::P ause.
ms.assetid: 4f4cbe7e-3004-4731-864f-737c2f51afff
title: Método CBaseMediaFilter. PAUSE (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a75cbcf1d629b997584cff35ebd4095094fe8607
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670499"
---
# <a name="cbasemediafilterpause-method"></a><span data-ttu-id="56c9a-104">CBaseMediaFilter. PAUSE (método)</span><span class="sxs-lookup"><span data-stu-id="56c9a-104">CBaseMediaFilter.Pause method</span></span>

<span data-ttu-id="56c9a-105">Pausa el objeto.</span><span class="sxs-lookup"><span data-stu-id="56c9a-105">Pauses the object.</span></span> <span data-ttu-id="56c9a-106">Implementa el método [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) .</span><span class="sxs-lookup"><span data-stu-id="56c9a-106">Implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="56c9a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56c9a-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="56c9a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="56c9a-108">Parameters</span></span>

<span data-ttu-id="56c9a-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="56c9a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="56c9a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="56c9a-110">Return value</span></span>

<span data-ttu-id="56c9a-111">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="56c9a-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="56c9a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56c9a-112">Remarks</span></span>

<span data-ttu-id="56c9a-113">En la clase base, este método establece la variable miembro de [**\_ Estado CBaseMediaFilter:: m**](cbasemediafilter-m-state.md) en el estado \_ pausado, pero no hace nada más.</span><span class="sxs-lookup"><span data-stu-id="56c9a-113">In the base class, this method sets the [**CBaseMediaFilter::m\_State**](cbasemediafilter-m-state.md) member variable to State\_Paused but does nothing else.</span></span>

## <a name="requirements"></a><span data-ttu-id="56c9a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56c9a-114">Requirements</span></span>



| <span data-ttu-id="56c9a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="56c9a-115">Requirement</span></span> | <span data-ttu-id="56c9a-116">Value</span><span class="sxs-lookup"><span data-stu-id="56c9a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56c9a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="56c9a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="56c9a-118"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="56c9a-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="56c9a-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="56c9a-119">Library</span></span><br/> | <dl> <span data-ttu-id="56c9a-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="56c9a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56c9a-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="56c9a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56c9a-122">**Clase CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="56c9a-122">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




