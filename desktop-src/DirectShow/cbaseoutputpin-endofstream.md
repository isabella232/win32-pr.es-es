---
description: 'Método CBaseOutputPin.EndOfStream: el método EndOfStream notifica al pin que no se espera ningún dato adicional. Este método implementa el método IPin::EndOfStream.'
ms.assetid: 5c3b5f90-4194-4d65-9f1a-55edf327e3b3
title: Método CBaseOutputPin.EndOfStream (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c5f293b8026456618ad1196c491bce58cf481f07
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096153"
---
# <a name="cbaseoutputpinendofstream-method"></a><span data-ttu-id="d22cf-104">Método CBaseOutputPin.EndOfStream</span><span class="sxs-lookup"><span data-stu-id="d22cf-104">CBaseOutputPin.EndOfStream method</span></span>

<span data-ttu-id="d22cf-105">El `EndOfStream` método notifica al pin que no se espera ningún dato adicional.</span><span class="sxs-lookup"><span data-stu-id="d22cf-105">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="d22cf-106">Este método implementa el [**método IPin::EndOfStream.**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)</span><span class="sxs-lookup"><span data-stu-id="d22cf-106">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d22cf-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d22cf-107">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="d22cf-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d22cf-108">Parameters</span></span>

<span data-ttu-id="d22cf-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d22cf-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d22cf-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d22cf-110">Return value</span></span>

<span data-ttu-id="d22cf-111">Devuelve E \_ UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="d22cf-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="d22cf-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d22cf-112">Remarks</span></span>

<span data-ttu-id="d22cf-113">Solo se debe llamar a este método en los pines de entrada, por lo que la implementación **de CBaseOutputPin** devuelve E \_ UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="d22cf-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="d22cf-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d22cf-114">Requirements</span></span>



| <span data-ttu-id="d22cf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d22cf-115">Requirement</span></span> | <span data-ttu-id="d22cf-116">Value</span><span class="sxs-lookup"><span data-stu-id="d22cf-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d22cf-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d22cf-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d22cf-118"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="d22cf-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d22cf-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d22cf-119">Library</span></span><br/> | <dl> <span data-ttu-id="d22cf-120"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d22cf-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d22cf-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d22cf-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d22cf-122">**CBaseOutputPin (clase)**</span><span class="sxs-lookup"><span data-stu-id="d22cf-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




