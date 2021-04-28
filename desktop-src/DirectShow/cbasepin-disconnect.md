---
description: 'Método CBasePin.Disconnect: el método Disconnect interrumpe la conexión de pin actual. Este método implementa el método IPin::D isconnect.'
ms.assetid: 04e07978-fca5-419f-8807-fd7a6846eff9
title: Método CBasePin.Disconnect (Amfilter.h)
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
ms.openlocfilehash: bda01d02db2a93a90c63f206b723a55df2373418
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096013"
---
# <a name="cbasepindisconnect-method"></a><span data-ttu-id="c608c-104">Método CBasePin.Disconnect</span><span class="sxs-lookup"><span data-stu-id="c608c-104">CBasePin.Disconnect method</span></span>

<span data-ttu-id="c608c-105">El `Disconnect` método interrumpe la conexión de pin actual.</span><span class="sxs-lookup"><span data-stu-id="c608c-105">The `Disconnect` method breaks the current pin connection.</span></span> <span data-ttu-id="c608c-106">Este método implementa el [**método IPin::D isconnect.**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect)</span><span class="sxs-lookup"><span data-stu-id="c608c-106">This method implements the [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c608c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c608c-107">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="c608c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c608c-108">Parameters</span></span>

<span data-ttu-id="c608c-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c608c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c608c-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c608c-110">Return value</span></span>

<span data-ttu-id="c608c-111">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="c608c-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c608c-112">Los valores posibles incluyen los de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c608c-112">Possible values include those in the following table.</span></span>



| <span data-ttu-id="c608c-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c608c-113">Return code</span></span>                                                                                         | <span data-ttu-id="c608c-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="c608c-114">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c608c-115"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="c608c-115"><dt>**S\_FALSE**</dt></span></span> </dl>             | <span data-ttu-id="c608c-116">El pin no estaba conectado.</span><span class="sxs-lookup"><span data-stu-id="c608c-116">The pin was not connected.</span></span><br/>                                              |
| <dl> <span data-ttu-id="c608c-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c608c-117"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="c608c-118">Correcto.</span><span class="sxs-lookup"><span data-stu-id="c608c-118">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="c608c-119"><dt>**VFW \_ E \_ NOT \_ STOPPED**</dt></span><span class="sxs-lookup"><span data-stu-id="c608c-119"><dt>**VFW\_E\_NOT\_STOPPED**</dt></span></span> </dl> | <span data-ttu-id="c608c-120">El filtro está activo y el pin no admite la reconexión dinámica.</span><span class="sxs-lookup"><span data-stu-id="c608c-120">The filter is active and the pin does not support dynamic reconnection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c608c-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c608c-121">Remarks</span></span>

<span data-ttu-id="c608c-122">La clase base delega la mayor parte del trabajo en el método [**CBasePin::D isconnectInternal.**](cbasepin-disconnectinternal.md)</span><span class="sxs-lookup"><span data-stu-id="c608c-122">The base class delegates most of the work to the [**CBasePin::DisconnectInternal**](cbasepin-disconnectinternal.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c608c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c608c-123">Requirements</span></span>



| <span data-ttu-id="c608c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c608c-124">Requirement</span></span> | <span data-ttu-id="c608c-125">Value</span><span class="sxs-lookup"><span data-stu-id="c608c-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c608c-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c608c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c608c-127"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c608c-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c608c-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c608c-128">Library</span></span><br/> | <dl> <span data-ttu-id="c608c-129"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c608c-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c608c-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c608c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c608c-131">**CBasePin (clase)**</span><span class="sxs-lookup"><span data-stu-id="c608c-131">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




