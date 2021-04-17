---
description: Este operador asigna una nueva hora de referencia.
ms.assetid: ae6a33ab-f4e0-4f1c-80a0-8a25ee1e9dc5
title: Método COARefTime. Operator = (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f5a051cea555975fd8606c3693d4b7d63cb9ce4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680591"
---
# <a name="coareftimeoperator-method-ctlutilh"></a><span data-ttu-id="37a9f-103">Método COARefTime. Operator = (Ctlutil. h)</span><span class="sxs-lookup"><span data-stu-id="37a9f-103">COARefTime.operator= method (Ctlutil.h)</span></span>

<span data-ttu-id="37a9f-104">Este operador asigna una nueva hora de referencia.</span><span class="sxs-lookup"><span data-stu-id="37a9f-104">This operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="37a9f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37a9f-105">Syntax</span></span>


```C++
COARefTime& operator=(
  [ref] const double &rd
);
```



## <a name="parameters"></a><span data-ttu-id="37a9f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37a9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37a9f-107">*Rd* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="37a9f-107">*rd* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="37a9f-108">Referencia a un valor **Double** que especifica el nuevo tiempo de referencia en segundos.</span><span class="sxs-lookup"><span data-stu-id="37a9f-108">Reference to a **double** value that specifies the new reference time in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37a9f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37a9f-109">Return value</span></span>

<span data-ttu-id="37a9f-110">Devuelve una referencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="37a9f-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="37a9f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37a9f-111">Requirements</span></span>



| <span data-ttu-id="37a9f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="37a9f-112">Requirement</span></span> | <span data-ttu-id="37a9f-113">Value</span><span class="sxs-lookup"><span data-stu-id="37a9f-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37a9f-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37a9f-114">Header</span></span><br/>  | <dl> <span data-ttu-id="37a9f-115"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="37a9f-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="37a9f-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="37a9f-116">Library</span></span><br/> | <dl> <span data-ttu-id="37a9f-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="37a9f-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37a9f-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="37a9f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37a9f-119">**Clase COARefTime**</span><span class="sxs-lookup"><span data-stu-id="37a9f-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




