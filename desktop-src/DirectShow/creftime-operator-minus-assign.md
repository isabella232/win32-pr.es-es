---
description: El operador-= resta una hora de referencia de otra.
ms.assetid: 5b0ec72e-87d8-4562-96b1-40e4f5036fd4
title: Método CRefTime. Operator-= (Reftime. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator-=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bf66abe11d5c61edbb70118020d882c82b08847
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680399"
---
# <a name="creftimeoperator--method"></a><span data-ttu-id="cc7b4-103">CRefTime. Operator-= (método)</span><span class="sxs-lookup"><span data-stu-id="cc7b4-103">CRefTime.operator-= method</span></span>

<span data-ttu-id="cc7b4-104">El operador-= resta una hora de referencia de otra.</span><span class="sxs-lookup"><span data-stu-id="cc7b4-104">The -= operator subtracts one reference time from another.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc7b4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc7b4-105">Syntax</span></span>


```C++
CRefTime& operator-=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="cc7b4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cc7b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc7b4-107">*RT* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="cc7b4-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="cc7b4-108">Referencia a un objeto **CRefTime** .</span><span class="sxs-lookup"><span data-stu-id="cc7b4-108">Reference to a **CRefTime** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc7b4-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cc7b4-109">Return value</span></span>

<span data-ttu-id="cc7b4-110">Devuelve una referencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="cc7b4-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc7b4-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc7b4-111">Requirements</span></span>



| <span data-ttu-id="cc7b4-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc7b4-112">Requirement</span></span> | <span data-ttu-id="cc7b4-113">Value</span><span class="sxs-lookup"><span data-stu-id="cc7b4-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc7b4-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cc7b4-114">Header</span></span><br/>  | <dl> <span data-ttu-id="cc7b4-115"><dt>Reftime. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc7b4-115"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cc7b4-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cc7b4-116">Library</span></span><br/> | <dl> <span data-ttu-id="cc7b4-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="cc7b4-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




