---
description: El método InitMediaType inicializa el tipo de medio.
ms.assetid: 141ced68-11ed-4567-b2e1-82c040d3b4a4
title: CMediaType.Inimétodo tMediaType (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.InitMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c3bbe170c6d896f3b28d9b85cf49f18269341d50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678880"
---
# <a name="cmediatypeinitmediatype-method"></a><span data-ttu-id="2df30-103">CMediaType.Inimétodo tMediaType</span><span class="sxs-lookup"><span data-stu-id="2df30-103">CMediaType.InitMediaType method</span></span>

<span data-ttu-id="2df30-104">El `InitMediaType` método inicializa el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="2df30-104">The `InitMediaType` method initializes the media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="2df30-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2df30-105">Syntax</span></span>


```C++
void InitMediaType();
```



## <a name="parameters"></a><span data-ttu-id="2df30-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2df30-106">Parameters</span></span>

<span data-ttu-id="2df30-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2df30-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2df30-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2df30-108">Return value</span></span>

<span data-ttu-id="2df30-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2df30-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2df30-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2df30-110">Remarks</span></span>

<span data-ttu-id="2df30-111">Este método llena la memoria del objeto, establece la propiedad Fixed-Sample-Size en **true** y establece el tamaño de ejemplo en 1.</span><span class="sxs-lookup"><span data-stu-id="2df30-111">This method zeroes the object's memory, sets the fixed-sample-size property to **TRUE**, and sets the sample size to 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="2df30-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2df30-112">Requirements</span></span>



| <span data-ttu-id="2df30-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2df30-113">Requirement</span></span> | <span data-ttu-id="2df30-114">Value</span><span class="sxs-lookup"><span data-stu-id="2df30-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2df30-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2df30-115">Header</span></span><br/>  | <dl> <span data-ttu-id="2df30-116"><dt>Mtype. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2df30-116"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="2df30-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2df30-117">Library</span></span><br/> | <dl> <span data-ttu-id="2df30-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="2df30-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2df30-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="2df30-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2df30-120">**Clase CMediaType**</span><span class="sxs-lookup"><span data-stu-id="2df30-120">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




