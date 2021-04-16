---
description: El método Disconnect interrumpe la conexión con el PIN de salida.
ms.assetid: 6e362e32-7b74-4392-b46f-1ab47a30a07b
title: Método CPullPin. disconnect (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Disconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ec13a7f29a06bab4f79ddb58932796f8363adadc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671391"
---
# <a name="cpullpindisconnect-method"></a><span data-ttu-id="5b15a-103">CPullPin. disconnect (método)</span><span class="sxs-lookup"><span data-stu-id="5b15a-103">CPullPin.Disconnect method</span></span>

<span data-ttu-id="5b15a-104">El `Disconnect` método interrumpe la conexión con el PIN de salida.</span><span class="sxs-lookup"><span data-stu-id="5b15a-104">The `Disconnect` method breaks the connection with the output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b15a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b15a-105">Syntax</span></span>


```C++
HRESULT Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="5b15a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5b15a-106">Parameters</span></span>

<span data-ttu-id="5b15a-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="5b15a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5b15a-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5b15a-108">Return value</span></span>

<span data-ttu-id="5b15a-109">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="5b15a-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b15a-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b15a-110">Remarks</span></span>

<span data-ttu-id="5b15a-111">Este método interrumpe cualquier conexión realizada en el método [**CPullPin:: Connect**](cpullpin-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="5b15a-111">This method breaks any connection made in the [**CPullPin::Connect**](cpullpin-connect.md) method.</span></span> <span data-ttu-id="5b15a-112">Llame a este método dentro del método [**IPin::D Ulta**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) .</span><span class="sxs-lookup"><span data-stu-id="5b15a-112">Call this method inside your [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect) method.</span></span> <span data-ttu-id="5b15a-113">(Si el código PIN deriva de [**CBasePin**](cbasepin.md), invalide [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) para llamar a este método).</span><span class="sxs-lookup"><span data-stu-id="5b15a-113">(If your pin derives from [**CBasePin**](cbasepin.md), override [**CBasePin::BreakConnect**](cbasepin-breakconnect.md) to call this method.)</span></span>

## <a name="requirements"></a><span data-ttu-id="5b15a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b15a-114">Requirements</span></span>



| <span data-ttu-id="5b15a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b15a-115">Requirement</span></span> | <span data-ttu-id="5b15a-116">Value</span><span class="sxs-lookup"><span data-stu-id="5b15a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b15a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5b15a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="5b15a-118"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b15a-118"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="5b15a-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5b15a-119">Library</span></span><br/> | <dl> <span data-ttu-id="5b15a-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5b15a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b15a-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="5b15a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b15a-122">**Clase CPullPin**</span><span class="sxs-lookup"><span data-stu-id="5b15a-122">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




