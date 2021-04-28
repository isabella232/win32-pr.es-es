---
description: 'Método CBasePin.CheckMediaType: el método CheckMediaType determina si el pin acepta un tipo de medio específico.'
ms.assetid: 6a138679-02b7-4ccc-8881-a0d496f84f93
title: Método CBasePin.CheckMediaType (Amfilter.h)
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
ms.openlocfilehash: afe39f3a7aac155f3cc87fa6d58f402043861d1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099403"
---
# <a name="cbasepincheckmediatype-method"></a><span data-ttu-id="bf13b-103">Método CBasePin.CheckMediaType</span><span class="sxs-lookup"><span data-stu-id="bf13b-103">CBasePin.CheckMediaType method</span></span>

<span data-ttu-id="bf13b-104">El `CheckMediaType` método determina si el pin acepta un tipo de medio específico.</span><span class="sxs-lookup"><span data-stu-id="bf13b-104">The `CheckMediaType` method determines if the pin accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf13b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf13b-105">Syntax</span></span>


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="bf13b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bf13b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf13b-107">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="bf13b-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="bf13b-108">Puntero a un [**objeto CMediaType**](cmediatype.md) que contiene el tipo de medio propuesto.</span><span class="sxs-lookup"><span data-stu-id="bf13b-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf13b-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf13b-109">Return value</span></span>

<span data-ttu-id="bf13b-110">Devuelve S \_ OK si el tipo de medio propuesto es aceptable.</span><span class="sxs-lookup"><span data-stu-id="bf13b-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="bf13b-111">De lo contrario, devuelve S \_ FALSE o un código de error.</span><span class="sxs-lookup"><span data-stu-id="bf13b-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf13b-112">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bf13b-112">Remarks</span></span>

<span data-ttu-id="bf13b-113">La clase derivada debe invalidar este método virtual puro.</span><span class="sxs-lookup"><span data-stu-id="bf13b-113">The derived class must override this pure virtual method.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf13b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf13b-114">Requirements</span></span>



| <span data-ttu-id="bf13b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf13b-115">Requirement</span></span> | <span data-ttu-id="bf13b-116">Value</span><span class="sxs-lookup"><span data-stu-id="bf13b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf13b-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf13b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="bf13b-118"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf13b-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bf13b-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf13b-119">Library</span></span><br/> | <dl> <span data-ttu-id="bf13b-120"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="bf13b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf13b-121">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bf13b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf13b-122">**CBasePin (clase)**</span><span class="sxs-lookup"><span data-stu-id="bf13b-122">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




