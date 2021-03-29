---
description: El operador = asigna una nueva hora de referencia.
ms.assetid: 0b11e2ea-23dc-4c75-88c6-94215a4b14b6
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
ms.openlocfilehash: b87e6517946c64cb2a60e95912aba423a1880215
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680885"
---
# <a name="creftimeoperator-method-reftimeh"></a><span data-ttu-id="7c7e1-103">Método CRefTime. Operator = (Reftime. h)</span><span class="sxs-lookup"><span data-stu-id="7c7e1-103">CRefTime.operator= method (Reftime.h)</span></span>

<span data-ttu-id="7c7e1-104">El operador = asigna una nueva hora de referencia.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-104">The = operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c7e1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7c7e1-105">Syntax</span></span>


```C++
CRefTime& operator=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="7c7e1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7c7e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c7e1-107">*RT* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="7c7e1-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="7c7e1-108">Referencia a un objeto **CRefTime** que especifica la nueva hora de referencia.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-108">Reference to a **CRefTime** object that specifies the new reference time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c7e1-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7c7e1-109">Return value</span></span>

<span data-ttu-id="7c7e1-110">Devuelve una referencia al objeto.</span><span class="sxs-lookup"><span data-stu-id="7c7e1-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c7e1-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7c7e1-111">Requirements</span></span>



| <span data-ttu-id="7c7e1-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7c7e1-112">Requirement</span></span> | <span data-ttu-id="7c7e1-113">Value</span><span class="sxs-lookup"><span data-stu-id="7c7e1-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c7e1-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7c7e1-114">Header</span></span><br/>  | <dl> <span data-ttu-id="7c7e1-115"><dt>Reftime. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7c7e1-115"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7c7e1-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7c7e1-116">Library</span></span><br/> | <dl> <span data-ttu-id="7c7e1-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7c7e1-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




