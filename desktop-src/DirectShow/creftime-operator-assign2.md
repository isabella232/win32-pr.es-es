---
description: El operador = asigna una nueva hora de referencia. Este método usa el parámetro *ll* .
ms.assetid: 556c2e8a-4726-42ab-949d-9a028ebb1b95
title: CRefTime. Operator = Method (Reftime. h)-ll (parámetro)
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
ms.openlocfilehash: d09cb957e06d8b075cff3d831a7f68fbbdf662a8
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187842"
---
# <a name="creftimeoperator-method-reftimeh---ll-parameter"></a><span data-ttu-id="9fec6-104">CRefTime. Operator = Method (Reftime. h)-ll (parámetro)</span><span class="sxs-lookup"><span data-stu-id="9fec6-104">CRefTime.operator= method (Reftime.h) - ll parameter</span></span>

<span data-ttu-id="9fec6-105">El operador = asigna una nueva hora de referencia.</span><span class="sxs-lookup"><span data-stu-id="9fec6-105">The = operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fec6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9fec6-106">Syntax</span></span>


```C++
CRefTime& operator=(
   const LONGLONG ll
);
```



## <a name="parameters"></a><span data-ttu-id="9fec6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9fec6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fec6-108">*ll*</span><span class="sxs-lookup"><span data-stu-id="9fec6-108">*ll*</span></span> 
</dt> <dd>

<span data-ttu-id="9fec6-109">Nuevo tiempo de referencia, en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="9fec6-109">New reference time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fec6-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9fec6-110">Return value</span></span>

<span data-ttu-id="9fec6-111">Devuelve una referencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="9fec6-111">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fec6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fec6-112">Requirements</span></span>



| <span data-ttu-id="9fec6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fec6-113">Requirement</span></span> | <span data-ttu-id="9fec6-114">Value</span><span class="sxs-lookup"><span data-stu-id="9fec6-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fec6-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9fec6-115">Header</span></span>  | <span data-ttu-id="9fec6-116">Reftime. h (incluir streams. h)</span><span class="sxs-lookup"><span data-stu-id="9fec6-116">Reftime.h (include Streams.h)</span></span>                                                                                   |
| <span data-ttu-id="9fec6-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9fec6-117">Library</span></span> | <span data-ttu-id="9fec6-118">Strmbase. lib (compilaciones comerciales); Strmbasd. lib (compilaciones de depuración)</span><span class="sxs-lookup"><span data-stu-id="9fec6-118">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |



 

 




