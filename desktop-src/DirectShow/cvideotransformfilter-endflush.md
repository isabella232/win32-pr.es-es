---
description: 'El método EndFlush finaliza una operación de vaciado. Este método invalida el método CTransformFilter:: EndFlush.'
ms.assetid: e7dfc6f9-1630-426b-95b2-9814331b5e61
title: Método CVideoTransformFilter. EndFlush (Vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca160bd2e3e66df3bcf6f293abe6f828309172c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660929"
---
# <a name="cvideotransformfilterendflush-method"></a><span data-ttu-id="737c3-104">CVideoTransformFilter. EndFlush, método</span><span class="sxs-lookup"><span data-stu-id="737c3-104">CVideoTransformFilter.EndFlush method</span></span>

<span data-ttu-id="737c3-105">El `EndFlush` método finaliza una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="737c3-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="737c3-106">Este método invalida el método [**CTransformFilter:: EndFlush**](ctransformfilter-endflush.md) .</span><span class="sxs-lookup"><span data-stu-id="737c3-106">This method overrides the [**CTransformFilter::EndFlush**](ctransformfilter-endflush.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="737c3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="737c3-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="737c3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="737c3-108">Parameters</span></span>

<span data-ttu-id="737c3-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="737c3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="737c3-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="737c3-110">Return value</span></span>

<span data-ttu-id="737c3-111">Devuelve \_ si es correcto, o un código de error.</span><span class="sxs-lookup"><span data-stu-id="737c3-111">Returns S\_OK if successful, or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="737c3-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="737c3-112">Remarks</span></span>

<span data-ttu-id="737c3-113">Este método restablece todas las medidas de rendimiento internas del filtro.</span><span class="sxs-lookup"><span data-stu-id="737c3-113">This method resets all of the filter's internal performance measurements.</span></span>

## <a name="requirements"></a><span data-ttu-id="737c3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="737c3-114">Requirements</span></span>



| <span data-ttu-id="737c3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="737c3-115">Requirement</span></span> | <span data-ttu-id="737c3-116">Value</span><span class="sxs-lookup"><span data-stu-id="737c3-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="737c3-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="737c3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="737c3-118"><dt>Vtrans. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="737c3-118"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="737c3-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="737c3-119">Library</span></span><br/> | <dl> <span data-ttu-id="737c3-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="737c3-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="737c3-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="737c3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="737c3-122">**Clase CVideoTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="737c3-122">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




