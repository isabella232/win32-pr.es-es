---
description: 'El método EndFlush finaliza una operación de vaciado. Este método implementa el método IPin:: EndFlush.'
ms.assetid: c5c76cf8-1ca1-4fef-8776-7f4dcca32939
title: Método CBaseOutputPin. EndFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b40bc7db4e8d290ae0cd7e26a9d751e44b0daa4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661163"
---
# <a name="cbaseoutputpinendflush-method"></a><span data-ttu-id="848d2-104">CBaseOutputPin. EndFlush, método</span><span class="sxs-lookup"><span data-stu-id="848d2-104">CBaseOutputPin.EndFlush method</span></span>

<span data-ttu-id="848d2-105">El `EndFlush` método finaliza una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="848d2-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="848d2-106">Este método implementa el método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="848d2-106">This method implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="848d2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="848d2-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="848d2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="848d2-108">Parameters</span></span>

<span data-ttu-id="848d2-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="848d2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="848d2-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="848d2-110">Return value</span></span>

<span data-ttu-id="848d2-111">Devuelve E \_ inesperado.</span><span class="sxs-lookup"><span data-stu-id="848d2-111">Returns E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="848d2-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="848d2-112">Remarks</span></span>

<span data-ttu-id="848d2-113">Solo se debe llamar a este método en los pin de entrada, por lo que la implementación de **CBaseOutputPin** devuelve E \_ inesperada.</span><span class="sxs-lookup"><span data-stu-id="848d2-113">This method should only be called on input pins, so the **CBaseOutputPin** implementation returns E\_UNEXPECTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="848d2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="848d2-114">Requirements</span></span>



| <span data-ttu-id="848d2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="848d2-115">Requirement</span></span> | <span data-ttu-id="848d2-116">Value</span><span class="sxs-lookup"><span data-stu-id="848d2-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="848d2-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="848d2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="848d2-118"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="848d2-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="848d2-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="848d2-119">Library</span></span><br/> | <dl> <span data-ttu-id="848d2-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="848d2-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="848d2-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="848d2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="848d2-122">**Clase CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="848d2-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




