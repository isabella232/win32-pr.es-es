---
description: Este operador multiplica un tiempo de referencia por un valor.
ms.assetid: f575fd41-1d3e-43a6-abf8-8e64093e408e
title: Método COARefTime. Operator * (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator*
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c62a4282f7a43ba3d7ba35daf81530f8b246be32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671247"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="89fa6-103">COARefTime. Operator ( \* método)</span><span class="sxs-lookup"><span data-stu-id="89fa6-103">COARefTime.operator\* method</span></span>

<span data-ttu-id="89fa6-104">Este operador multiplica un tiempo de referencia por un valor.</span><span class="sxs-lookup"><span data-stu-id="89fa6-104">This operator multiplies a reference time by a value.</span></span>

## <a name="syntax"></a><span data-ttu-id="89fa6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89fa6-105">Syntax</span></span>


```C++
COARefTime operator*(
   LONG l
);
```



## <a name="parameters"></a><span data-ttu-id="89fa6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="89fa6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89fa6-107">*l*</span><span class="sxs-lookup"><span data-stu-id="89fa6-107">*l*</span></span> 
</dt> <dd>

<span data-ttu-id="89fa6-108">Multiplicador.</span><span class="sxs-lookup"><span data-stu-id="89fa6-108">Multiplier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89fa6-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="89fa6-109">Return value</span></span>

<span data-ttu-id="89fa6-110">Devuelve un nuevo objeto **COARefTime** igual al producto de este objeto y **l**.</span><span class="sxs-lookup"><span data-stu-id="89fa6-110">Returns a new **COARefTime** object equal to the product of this object and **l**.</span></span>

## <a name="requirements"></a><span data-ttu-id="89fa6-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89fa6-111">Requirements</span></span>



| <span data-ttu-id="89fa6-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="89fa6-112">Requirement</span></span> | <span data-ttu-id="89fa6-113">Value</span><span class="sxs-lookup"><span data-stu-id="89fa6-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89fa6-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="89fa6-114">Header</span></span><br/>  | <dl> <span data-ttu-id="89fa6-115"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="89fa6-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="89fa6-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="89fa6-116">Library</span></span><br/> | <dl> <span data-ttu-id="89fa6-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="89fa6-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89fa6-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="89fa6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89fa6-119">**Clase COARefTime**</span><span class="sxs-lookup"><span data-stu-id="89fa6-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




