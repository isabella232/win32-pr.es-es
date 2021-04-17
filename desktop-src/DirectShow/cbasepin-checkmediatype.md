---
description: El método CheckMediaType determina si el PIN acepta un tipo de medio específico.
ms.assetid: 6a138679-02b7-4ccc-8881-a0d496f84f93
title: Método CBasePin. CheckMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e203851a44a5468567e75ee8c0cc955f8ad0278a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661234"
---
# <a name="cbasepincheckmediatype-method"></a><span data-ttu-id="e1f96-103">CBasePin. CheckMediaType, método</span><span class="sxs-lookup"><span data-stu-id="e1f96-103">CBasePin.CheckMediaType method</span></span>

<span data-ttu-id="e1f96-104">El `CheckMediaType` método determina si el PIN acepta un tipo de medio específico.</span><span class="sxs-lookup"><span data-stu-id="e1f96-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1f96-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e1f96-105">Syntax</span></span>


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="e1f96-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e1f96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1f96-107">*p.p.*</span><span class="sxs-lookup"><span data-stu-id="e1f96-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="e1f96-108">Puntero a un objeto [**CMediaType**](cmediatype.md) que contiene el tipo de medio propuesto.</span><span class="sxs-lookup"><span data-stu-id="e1f96-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1f96-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e1f96-109">Return value</span></span>

<span data-ttu-id="e1f96-110">Devuelve S \_ OK si el tipo de medio propuesto es aceptable.</span><span class="sxs-lookup"><span data-stu-id="e1f96-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="e1f96-111">De lo contrario, devuelve S \_ false o un código de error.</span><span class="sxs-lookup"><span data-stu-id="e1f96-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1f96-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e1f96-112">Remarks</span></span>

<span data-ttu-id="e1f96-113">La clase derivada debe reemplazar este método virtual puro.</span><span class="sxs-lookup"><span data-stu-id="e1f96-113">The derived class must override this pure virtual method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1f96-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1f96-114">Requirements</span></span>



| <span data-ttu-id="e1f96-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1f96-115">Requirement</span></span> | <span data-ttu-id="e1f96-116">Value</span><span class="sxs-lookup"><span data-stu-id="e1f96-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1f96-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e1f96-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e1f96-118"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1f96-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e1f96-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e1f96-119">Library</span></span><br/> | <dl> <span data-ttu-id="e1f96-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e1f96-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1f96-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="e1f96-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1f96-122">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="e1f96-122">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




