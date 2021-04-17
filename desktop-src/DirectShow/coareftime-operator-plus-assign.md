---
description: Este operador agrega dos horas de referencia y establece este objeto en el resultado.
ms.assetid: 6d29014b-0e31-497e-8326-e3fefc022227
title: Método COARefTime. Operator + = (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator+=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a03d9e98c3c2f2ca09c3f90f2cb0867d976e02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680600"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="8b822-103">COARefTime. Operator + = (método)</span><span class="sxs-lookup"><span data-stu-id="8b822-103">COARefTime.operator+= method</span></span>

<span data-ttu-id="8b822-104">Este operador agrega dos horas de referencia y establece este objeto en el resultado.</span><span class="sxs-lookup"><span data-stu-id="8b822-104">This operator adds two reference times, and sets this object to the result.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b822-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8b822-105">Syntax</span></span>


```C++
COARefTime& operator+=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="8b822-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8b822-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b822-107">*RT* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="8b822-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="8b822-108">Referencia al objeto **COARefTime** que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="8b822-108">Reference to the **COARefTime** object to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b822-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8b822-109">Return value</span></span>

<span data-ttu-id="8b822-110">Devuelve una referencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="8b822-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b822-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b822-111">Requirements</span></span>



| <span data-ttu-id="8b822-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b822-112">Requirement</span></span> | <span data-ttu-id="8b822-113">Value</span><span class="sxs-lookup"><span data-stu-id="8b822-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b822-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8b822-114">Header</span></span><br/>  | <dl> <span data-ttu-id="8b822-115"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8b822-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8b822-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8b822-116">Library</span></span><br/> | <dl> <span data-ttu-id="8b822-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="8b822-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b822-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="8b822-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b822-119">**Clase COARefTime**</span><span class="sxs-lookup"><span data-stu-id="8b822-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




