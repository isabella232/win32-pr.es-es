---
description: 'Método CTransformInputPin.BreakConnect: el método BreakConnect libera el pin de una conexión.'
ms.assetid: 9874717d-f4d8-426d-a717-9f5d83b4683c
title: Método CTransformInputPin.BreakConnect (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe425ba617909dcfb1d66dbb4777b579139d436b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085023"
---
# <a name="ctransforminputpinbreakconnect-method"></a><span data-ttu-id="6f881-103">Método CTransformInputPin.BreakConnect</span><span class="sxs-lookup"><span data-stu-id="6f881-103">CTransformInputPin.BreakConnect method</span></span>

<span data-ttu-id="6f881-104">El `BreakConnect` método libera el pin de una conexión.</span><span class="sxs-lookup"><span data-stu-id="6f881-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f881-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f881-105">Syntax</span></span>


```C++
HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="6f881-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f881-106">Parameters</span></span>

<span data-ttu-id="6f881-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="6f881-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6f881-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f881-108">Return value</span></span>

<span data-ttu-id="6f881-109">Devuelve S \_ OK u otro valor **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="6f881-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f881-110">Comentarios</span><span class="sxs-lookup"><span data-stu-id="6f881-110">Remarks</span></span>

<span data-ttu-id="6f881-111">Este método invalida el [**método CBaseInputPin::BreakConnect.**](cbaseinputpin-breakconnect.md)</span><span class="sxs-lookup"><span data-stu-id="6f881-111">This method overrides the [**CBaseInputPin::BreakConnect**](cbaseinputpin-breakconnect.md) method.</span></span> <span data-ttu-id="6f881-112">Llama al método [**CTransformFilter::BreakConnect**](ctransformfilter-breakconnect.md) del filtro, que devuelve S \_ OK en la clase base.</span><span class="sxs-lookup"><span data-stu-id="6f881-112">It calls the filter's [**CTransformFilter::BreakConnect**](ctransformfilter-breakconnect.md) method, which returns S\_OK in the base class.</span></span> <span data-ttu-id="6f881-113">La clase derivada puede invalidar el **método CTransformFilter::BreakConnect.**</span><span class="sxs-lookup"><span data-stu-id="6f881-113">The derived class can override the **CTransformFilter::BreakConnect** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f881-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f881-114">Requirements</span></span>



| <span data-ttu-id="6f881-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f881-115">Requirement</span></span> | <span data-ttu-id="6f881-116">Value</span><span class="sxs-lookup"><span data-stu-id="6f881-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f881-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f881-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6f881-118"><dt>Transfrm.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="6f881-118"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6f881-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6f881-119">Library</span></span><br/> | <dl> <span data-ttu-id="6f881-120"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6f881-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




