---
description: El método DisconnectInternal interrumpe la conexión del PIN actual.
ms.assetid: 070301ad-d079-4ad3-abdf-d5de88872e52
title: Método CBasePin. DisconnectInternal (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisconnectInternal
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0891a9446e09c56e3845c02217d39037aad38bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660793"
---
# <a name="cbasepindisconnectinternal-method"></a><span data-ttu-id="7c4b6-103">CBasePin. DisconnectInternal, método</span><span class="sxs-lookup"><span data-stu-id="7c4b6-103">CBasePin.DisconnectInternal method</span></span>

<span data-ttu-id="7c4b6-104">El `DisconnectInternal` método interrumpe la conexión del PIN actual.</span><span class="sxs-lookup"><span data-stu-id="7c4b6-104">The `DisconnectInternal` method breaks the current pin connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c4b6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c4b6-105">Syntax</span></span>


```C++
HRESULT DisconnectInternal();
```



## <a name="parameters"></a><span data-ttu-id="7c4b6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c4b6-106">Parameters</span></span>

<span data-ttu-id="7c4b6-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7c4b6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7c4b6-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c4b6-108">Return value</span></span>

<span data-ttu-id="7c4b6-109">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7c4b6-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7c4b6-110">Entre los valores posibles se incluyen los de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="7c4b6-110">Possible values include those in the following table.</span></span>



| <span data-ttu-id="7c4b6-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="7c4b6-111">Return code</span></span>                                                                                         | <span data-ttu-id="7c4b6-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="7c4b6-112">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7c4b6-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="7c4b6-113"><dt>**S\_FALSE**</dt></span></span> </dl>             | <span data-ttu-id="7c4b6-114">El PIN no estaba conectado.</span><span class="sxs-lookup"><span data-stu-id="7c4b6-114">The pin was not connected.</span></span><br/>                                              |
| <dl> <span data-ttu-id="7c4b6-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="7c4b6-115"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="7c4b6-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="7c4b6-116">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="7c4b6-117"><dt>**VFW \_ E \_ no \_ detenido**</dt></span><span class="sxs-lookup"><span data-stu-id="7c4b6-117"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="7c4b6-118">El filtro está activo y el PIN no admite la reconexión dinámica.</span><span class="sxs-lookup"><span data-stu-id="7c4b6-118">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7c4b6-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7c4b6-119">Remarks</span></span>

<span data-ttu-id="7c4b6-120">El método [**CBasePin::D Ulta**](cbasepin-disconnect.md) delega el proceso de desconexión a este método.</span><span class="sxs-lookup"><span data-stu-id="7c4b6-120">The [**CBasePin::Disconnect**](cbasepin-disconnect.md) method delegates the disconnect process to this method.</span></span> <span data-ttu-id="7c4b6-121">Este método llama al método [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="7c4b6-121">This method calls the [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) method.</span></span> <span data-ttu-id="7c4b6-122">También libera el recuento de referencias en el otro PIN, que está contenido en la variable de miembro [**\_ conectada CBasePin:: m**](cbasepin-m-connected.md) .</span><span class="sxs-lookup"><span data-stu-id="7c4b6-122">It also releases the reference count on the other pin, which is held by the [**CBasePin::m\_Connected**](cbasepin-m-connected.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c4b6-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c4b6-123">Requirements</span></span>



| <span data-ttu-id="7c4b6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c4b6-124">Requirement</span></span> | <span data-ttu-id="7c4b6-125">Value</span><span class="sxs-lookup"><span data-stu-id="7c4b6-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c4b6-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c4b6-126">Header</span></span><br/>  | <dl> <span data-ttu-id="7c4b6-127"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c4b6-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7c4b6-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c4b6-128">Library</span></span><br/> | <dl> <span data-ttu-id="7c4b6-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7c4b6-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c4b6-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="7c4b6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c4b6-131">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="7c4b6-131">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




