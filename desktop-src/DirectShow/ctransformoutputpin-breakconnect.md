---
description: 'Método CTransformOutputPin.BreakConnect: el método BreakConnect libera el pin de una conexión.'
ms.assetid: bf68aca3-93e5-4f9d-9980-1a5eed1513f5
title: Método CTransformOutputPin.BreakConnect (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 92854041e1d553945d0a1ab1755ef3557bd4a8b2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084963"
---
# <a name="ctransformoutputpinbreakconnect-method"></a><span data-ttu-id="9d7ee-103">Método CTransformOutputPin.BreakConnect</span><span class="sxs-lookup"><span data-stu-id="9d7ee-103">CTransformOutputPin.BreakConnect method</span></span>

<span data-ttu-id="9d7ee-104">El `BreakConnect` método libera el pin de una conexión.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d7ee-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9d7ee-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="9d7ee-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9d7ee-106">Parameters</span></span>

<span data-ttu-id="9d7ee-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9d7ee-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9d7ee-108">Return value</span></span>

<span data-ttu-id="9d7ee-109">Devuelve S \_ OK u otro valor **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="9d7ee-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d7ee-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="9d7ee-110">Remarks</span></span>

<span data-ttu-id="9d7ee-111">Este método invalida el método [**CBaseOutputPin::BreakConnect.**](cbaseoutputpin-breakconnect.md)</span><span class="sxs-lookup"><span data-stu-id="9d7ee-111">This method overrides the [**CBaseOutputPin::BreakConnect**](cbaseoutputpin-breakconnect.md) method.</span></span> <span data-ttu-id="9d7ee-112">Llama al método [**CTransformFilter::BreakConnect**](ctransformfilter-breakconnect.md) del filtro, que devuelve S \_ OK en la clase base.</span><span class="sxs-lookup"><span data-stu-id="9d7ee-112">It calls the filter's [**CTransformFilter::BreakConnect**](ctransformfilter-breakconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="9d7ee-113">La clase derivada puede invalidar el **método CTransformFilter::BreakConnect.**</span><span class="sxs-lookup"><span data-stu-id="9d7ee-113">The derived class can override the **CTransformFilter::BreakConnect** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d7ee-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d7ee-114">Requirements</span></span>



| <span data-ttu-id="9d7ee-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d7ee-115">Requirement</span></span> | <span data-ttu-id="9d7ee-116">Value</span><span class="sxs-lookup"><span data-stu-id="9d7ee-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d7ee-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9d7ee-117">Header</span></span><br/>  | <dl> <span data-ttu-id="9d7ee-118"><dt>Transfrm.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d7ee-118"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9d7ee-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9d7ee-119">Library</span></span><br/> | <dl> <span data-ttu-id="9d7ee-120"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9d7ee-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




