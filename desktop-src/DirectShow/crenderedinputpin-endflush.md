---
description: 'Método CRenderedInputPin.EndFlush: el método EndFlush finaliza una operación de vaciado. Este método implementa el método IPin::EndFlush.'
ms.assetid: 5c27bf76-6886-431d-9958-5064c53909ec
title: Método CRenderedInputPin.EndFlush (Amextra.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7be740df2b3b45d0b681a86b8f70bed8e1395e8f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098923"
---
# <a name="crenderedinputpinendflush-method"></a><span data-ttu-id="28437-104">Método CRenderedInputPin.EndFlush</span><span class="sxs-lookup"><span data-stu-id="28437-104">CRenderedInputPin.EndFlush method</span></span>

<span data-ttu-id="28437-105">El `EndFlush` método finaliza una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="28437-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="28437-106">Este método implementa el [**método IPin::EndFlush.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush)</span><span class="sxs-lookup"><span data-stu-id="28437-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="28437-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="28437-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="28437-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="28437-108">Parameters</span></span>

<span data-ttu-id="28437-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="28437-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="28437-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="28437-110">Return value</span></span>

<span data-ttu-id="28437-111">Devuelve S \_ OK si se realiza correctamente o un código de error de lo contrario.</span><span class="sxs-lookup"><span data-stu-id="28437-111">Returns S\_OK if successful, or an error code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="28437-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="28437-112">Remarks</span></span>

<span data-ttu-id="28437-113">Este método borra los eventos [**EC \_ COMPLETE pendientes.**](ec-complete.md)</span><span class="sxs-lookup"><span data-stu-id="28437-113">This method clears any pending [**EC\_COMPLETE**](ec-complete.md) events.</span></span>

## <a name="requirements"></a><span data-ttu-id="28437-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="28437-114">Requirements</span></span>



| <span data-ttu-id="28437-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="28437-115">Requirement</span></span> | <span data-ttu-id="28437-116">Value</span><span class="sxs-lookup"><span data-stu-id="28437-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28437-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="28437-117">Header</span></span><br/>  | <dl> <span data-ttu-id="28437-118"><dt>Amextra.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="28437-118"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="28437-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="28437-119">Library</span></span><br/> | <dl> <span data-ttu-id="28437-120"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="28437-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28437-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="28437-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28437-122">**CRenderedInputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="28437-122">**CRenderedInputPin Class**</span></span>](crenderedinputpin.md)
</dt> </dl>

 

 




