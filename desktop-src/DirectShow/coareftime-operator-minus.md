---
description: Este operador resta una hora de referencia de otra.
ms.assetid: 5691cd76-0d25-45c0-bb58-6668abe1db01
title: COARefTime. Operator-Method (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator-
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e51ee8aaed69830a498d1d22cebdc3927987f045
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670769"
---
# <a name="coareftimeoperator--method"></a><span data-ttu-id="b1d67-103">COARefTime. Operator-(método)</span><span class="sxs-lookup"><span data-stu-id="b1d67-103">COARefTime.operator- method</span></span>

<span data-ttu-id="b1d67-104">Este operador resta una hora de referencia de otra.</span><span class="sxs-lookup"><span data-stu-id="b1d67-104">This operator subtracts one reference time from another.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1d67-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1d67-105">Syntax</span></span>


```C++
COARefTime operator-(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="b1d67-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b1d67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1d67-107">*RT* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="b1d67-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="b1d67-108">Referencia al objeto **COARefTime** que se va a restar.</span><span class="sxs-lookup"><span data-stu-id="b1d67-108">Reference to the **COARefTime** object to subtract.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1d67-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b1d67-109">Return value</span></span>

<span data-ttu-id="b1d67-110">Devuelve un nuevo objeto **COARefTime** igual a la diferencia de los tiempos de referencia.</span><span class="sxs-lookup"><span data-stu-id="b1d67-110">Returns a new **COARefTime** object equal to the difference of the reference times.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1d67-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1d67-111">Requirements</span></span>



| <span data-ttu-id="b1d67-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1d67-112">Requirement</span></span> | <span data-ttu-id="b1d67-113">Value</span><span class="sxs-lookup"><span data-stu-id="b1d67-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1d67-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b1d67-114">Header</span></span><br/>  | <dl> <span data-ttu-id="b1d67-115"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1d67-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b1d67-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b1d67-116">Library</span></span><br/> | <dl> <span data-ttu-id="b1d67-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b1d67-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1d67-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1d67-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1d67-119">**Clase COARefTime**</span><span class="sxs-lookup"><span data-stu-id="b1d67-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




