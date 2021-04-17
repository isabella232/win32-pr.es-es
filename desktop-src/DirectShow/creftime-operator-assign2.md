---
description: El operador = asigna una nueva hora de referencia.
ms.assetid: 556c2e8a-4726-42ab-949d-9a028ebb1b95
title: Método CRefTime. Operator = (Reftime. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8d93a57211c3bc7d787e68f70f36be868ff64449
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681059"
---
# <a name="creftimeoperator-method-reftimeh"></a><span data-ttu-id="7434d-103">Método CRefTime. Operator = (Reftime. h)</span><span class="sxs-lookup"><span data-stu-id="7434d-103">CRefTime.operator= method (Reftime.h)</span></span>

<span data-ttu-id="7434d-104">El operador = asigna una nueva hora de referencia.</span><span class="sxs-lookup"><span data-stu-id="7434d-104">The = operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="7434d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7434d-105">Syntax</span></span>


```C++
CRefTime& operator=(
   const LONGLONG ll
);
```



## <a name="parameters"></a><span data-ttu-id="7434d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7434d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7434d-107">*ll*</span><span class="sxs-lookup"><span data-stu-id="7434d-107">*ll*</span></span> 
</dt> <dd>

<span data-ttu-id="7434d-108">Nuevo tiempo de referencia, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="7434d-108">New reference time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7434d-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7434d-109">Return value</span></span>

<span data-ttu-id="7434d-110">Devuelve una referencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="7434d-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="7434d-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7434d-111">Requirements</span></span>



| <span data-ttu-id="7434d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7434d-112">Requirement</span></span> | <span data-ttu-id="7434d-113">Value</span><span class="sxs-lookup"><span data-stu-id="7434d-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7434d-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7434d-114">Header</span></span><br/>  | <dl> <span data-ttu-id="7434d-115"><dt>Reftime. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7434d-115"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7434d-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7434d-116">Library</span></span><br/> | <dl> <span data-ttu-id="7434d-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7434d-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




