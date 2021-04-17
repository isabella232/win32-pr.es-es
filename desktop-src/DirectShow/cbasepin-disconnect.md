---
description: El método Disconnect interrumpe la conexión del PIN actual. Este método implementa el método IPin::D Ulta.
ms.assetid: 04e07978-fca5-419f-8807-fd7a6846eff9
title: Método CBasePin. disconnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98cbf894767eeb89042134344df218f2c18bc1be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671105"
---
# <a name="cbasepindisconnect-method"></a><span data-ttu-id="4e59b-104">CBasePin. disconnect (método)</span><span class="sxs-lookup"><span data-stu-id="4e59b-104">CBasePin.Disconnect method</span></span>

<span data-ttu-id="4e59b-105">El `Disconnect` método interrumpe la conexión del PIN actual.</span><span class="sxs-lookup"><span data-stu-id="4e59b-105">The `Disconnect` method breaks the current pin connection.</span></span> <span data-ttu-id="4e59b-106">Este método implementa el método [**IPin::D Ulta**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="4e59b-106">This method implements the [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e59b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4e59b-107">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="4e59b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4e59b-108">Parameters</span></span>

<span data-ttu-id="4e59b-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="4e59b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4e59b-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4e59b-110">Return value</span></span>

<span data-ttu-id="4e59b-111">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4e59b-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4e59b-112">Entre los valores posibles se incluyen los de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="4e59b-112">Possible values include those in the following table.</span></span>



| <span data-ttu-id="4e59b-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="4e59b-113">Return code</span></span>                                                                                         | <span data-ttu-id="4e59b-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="4e59b-114">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4e59b-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="4e59b-115"><dt>**S\_FALSE**</dt></span></span> </dl>             | <span data-ttu-id="4e59b-116">El PIN no estaba conectado.</span><span class="sxs-lookup"><span data-stu-id="4e59b-116">The pin was not connected.</span></span><br/>                                              |
| <dl> <span data-ttu-id="4e59b-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="4e59b-117"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="4e59b-118">Correcto.</span><span class="sxs-lookup"><span data-stu-id="4e59b-118">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="4e59b-119"><dt>**VFW \_ E \_ no \_ detenido**</dt></span><span class="sxs-lookup"><span data-stu-id="4e59b-119"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="4e59b-120">El filtro está activo y el PIN no admite la reconexión dinámica.</span><span class="sxs-lookup"><span data-stu-id="4e59b-120">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4e59b-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4e59b-121">Remarks</span></span>

<span data-ttu-id="4e59b-122">La clase base delega la mayor parte del trabajo en el método [**CBasePin::D isconnectinternal**](cbasepin-disconnectinternal.md) .</span><span class="sxs-lookup"><span data-stu-id="4e59b-122">The base class delegates most of the work to the [**CBasePin::DisconnectInternal**](cbasepin-disconnectinternal.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e59b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4e59b-123">Requirements</span></span>



| <span data-ttu-id="4e59b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e59b-124">Requirement</span></span> | <span data-ttu-id="4e59b-125">Value</span><span class="sxs-lookup"><span data-stu-id="4e59b-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e59b-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4e59b-126">Header</span></span><br/>  | <dl> <span data-ttu-id="4e59b-127"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e59b-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4e59b-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4e59b-128">Library</span></span><br/> | <dl> <span data-ttu-id="4e59b-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="4e59b-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e59b-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="4e59b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e59b-131">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="4e59b-131">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




