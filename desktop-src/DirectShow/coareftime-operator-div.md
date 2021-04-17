---
description: Este operador divide una hora de referencia por un valor.
ms.assetid: fb2e2a4b-dc0b-42e3-86c7-8aa2c60daedc
title: COARefTime. Operator/Method (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator/
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e1e4d7b7adb881ac11988a2d2c46946ff6cddcc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671228"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="d95fa-103">COARefTime. Operator/(método)</span><span class="sxs-lookup"><span data-stu-id="d95fa-103">COARefTime.operator/ method</span></span>

<span data-ttu-id="d95fa-104">Este operador divide una hora de referencia por un valor.</span><span class="sxs-lookup"><span data-stu-id="d95fa-104">This operator divides a reference time by a value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d95fa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d95fa-105">Syntax</span></span>


```C++
COARefTime operator/(
   LONG l
);
```



## <a name="parameters"></a><span data-ttu-id="d95fa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d95fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d95fa-107">*l*</span><span class="sxs-lookup"><span data-stu-id="d95fa-107">*l*</span></span> 
</dt> <dd>

<span data-ttu-id="d95fa-108">Divisor.</span><span class="sxs-lookup"><span data-stu-id="d95fa-108">Divisor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d95fa-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d95fa-109">Return value</span></span>

<span data-ttu-id="d95fa-110">Devuelve un nuevo objeto **COARefTime** igual al cociente de este objeto y **l**.</span><span class="sxs-lookup"><span data-stu-id="d95fa-110">Returns a new **COARefTime** object equal to the quotient of this object and **l**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d95fa-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d95fa-111">Requirements</span></span>



| <span data-ttu-id="d95fa-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d95fa-112">Requirement</span></span> | <span data-ttu-id="d95fa-113">Value</span><span class="sxs-lookup"><span data-stu-id="d95fa-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d95fa-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d95fa-114">Header</span></span><br/>  | <dl> <span data-ttu-id="d95fa-115"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d95fa-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d95fa-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d95fa-116">Library</span></span><br/> | <dl> <span data-ttu-id="d95fa-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d95fa-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d95fa-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="d95fa-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d95fa-119">**Clase COARefTime**</span><span class="sxs-lookup"><span data-stu-id="d95fa-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




