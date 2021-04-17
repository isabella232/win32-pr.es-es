---
description: Este operador comprueba la igualdad entre los objetos CMediaType.
ms.assetid: d50f3a72-c5e8-44a5-aa0e-b1c40a19fee3
title: 'CMediaType. CMediaType:: Operator = = (método, mtype. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType::operator==
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 79631415ce562f1cf3d7251e1f325960f5baa28b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690680"
---
# <a name="cmediatypecmediatypeoperator-method"></a><span data-ttu-id="92961-103">CMediaType. CMediaType:: Operator = = (método)</span><span class="sxs-lookup"><span data-stu-id="92961-103">CMediaType.CMediaType::operator== method</span></span>

<span data-ttu-id="92961-104">Este operador comprueba la igualdad entre los objetos [**CMediaType**](cmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="92961-104">This operator tests for equality between [**CMediaType**](cmediatype.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="92961-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92961-105">Syntax</span></span>


```C++
BOOL CMediaType::operator==(
  [ref] const CMediaType &rt
);
```



## <a name="parameters"></a><span data-ttu-id="92961-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92961-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92961-107">*RT* \[ CLI\]</span><span class="sxs-lookup"><span data-stu-id="92961-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="92961-108">Referencia al objeto **CMediaType** que se va a comparar.</span><span class="sxs-lookup"><span data-stu-id="92961-108">Reference to the **CMediaType** object to compare.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92961-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92961-109">Return value</span></span>

<span data-ttu-id="92961-110">Devuelve **true** si *RT* es igual a este objeto.</span><span class="sxs-lookup"><span data-stu-id="92961-110">Returns **TRUE** if *rt* is equal to this object.</span></span> <span data-ttu-id="92961-111">De lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="92961-111">Otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="92961-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92961-112">Requirements</span></span>



| <span data-ttu-id="92961-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="92961-113">Requirement</span></span> | <span data-ttu-id="92961-114">Value</span><span class="sxs-lookup"><span data-stu-id="92961-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92961-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92961-115">Header</span></span><br/>  | <dl> <span data-ttu-id="92961-116"><dt>Mtype. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="92961-116"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="92961-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="92961-117">Library</span></span><br/> | <dl> <span data-ttu-id="92961-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="92961-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92961-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="92961-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92961-120">**Clase CMediaType**</span><span class="sxs-lookup"><span data-stu-id="92961-120">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




