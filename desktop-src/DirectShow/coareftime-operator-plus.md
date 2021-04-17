---
description: Este operador agrega dos horas de referencia.
ms.assetid: 4dfc087a-ec4f-4a8a-8bd4-4da9e1699bcd
title: Método COARefTime. Operator + (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator+
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1a6f5019c61d4c1baec47652db8842aa5085b675
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680599"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="4cbb9-103">COARefTime. Operator + (método)</span><span class="sxs-lookup"><span data-stu-id="4cbb9-103">COARefTime.operator+ method</span></span>

<span data-ttu-id="4cbb9-104">Este operador agrega dos horas de referencia.</span><span class="sxs-lookup"><span data-stu-id="4cbb9-104">This operator adds two reference times.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cbb9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4cbb9-105">Syntax</span></span>


```C++
COARefTime operator+(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="4cbb9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4cbb9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4cbb9-107">*RT* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="4cbb9-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="4cbb9-108">Referencia al objeto **COARefTime** que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="4cbb9-108">Reference to the **COARefTime** object to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4cbb9-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4cbb9-109">Return value</span></span>

<span data-ttu-id="4cbb9-110">Devuelve un nuevo objeto **COARefTime** igual a la suma de las horas de referencia.</span><span class="sxs-lookup"><span data-stu-id="4cbb9-110">Returns a new **COARefTime** object equal to the sum of the reference times.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cbb9-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cbb9-111">Requirements</span></span>



| <span data-ttu-id="4cbb9-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cbb9-112">Requirement</span></span> | <span data-ttu-id="4cbb9-113">Value</span><span class="sxs-lookup"><span data-stu-id="4cbb9-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cbb9-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4cbb9-114">Header</span></span><br/>  | <dl> <span data-ttu-id="4cbb9-115"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4cbb9-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4cbb9-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4cbb9-116">Library</span></span><br/> | <dl> <span data-ttu-id="4cbb9-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="4cbb9-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cbb9-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="4cbb9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cbb9-119">**Clase COARefTime**</span><span class="sxs-lookup"><span data-stu-id="4cbb9-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




