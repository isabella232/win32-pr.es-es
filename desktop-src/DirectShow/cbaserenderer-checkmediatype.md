---
description: El método CheckMediaType determina si el filtro acepta un tipo de medio específico.
ms.assetid: 90d26cf6-443c-4a06-98c6-ffa14e27ee41
title: Método CBaseRenderer. CheckMediaType (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CheckMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dc0d4fc70e9ed64f9481d827cb678eb3ff9721d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671078"
---
# <a name="cbaserenderercheckmediatype-method"></a><span data-ttu-id="f1378-103">CBaseRenderer. CheckMediaType, método</span><span class="sxs-lookup"><span data-stu-id="f1378-103">CBaseRenderer.CheckMediaType method</span></span>

<span data-ttu-id="f1378-104">El `CheckMediaType` método determina si el filtro acepta un tipo de medio específico.</span><span class="sxs-lookup"><span data-stu-id="f1378-104">The `CheckMediaType` method determines if the filter accepts a specific media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1378-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f1378-105">Syntax</span></span>


```C++
virtual HRESULT CheckMediaType(
   const CMediaType *pmt
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="f1378-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f1378-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1378-107">*p.p.*</span><span class="sxs-lookup"><span data-stu-id="f1378-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="f1378-108">Puntero a un objeto [**CMediaType**](cmediatype.md) que contiene el tipo de medio propuesto.</span><span class="sxs-lookup"><span data-stu-id="f1378-108">Pointer to a [**CMediaType**](cmediatype.md) object that contains the proposed media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1378-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f1378-109">Return value</span></span>

<span data-ttu-id="f1378-110">Devuelve S \_ OK si el tipo de medio propuesto es aceptable.</span><span class="sxs-lookup"><span data-stu-id="f1378-110">Returns S\_OK if the proposed media type is acceptable.</span></span> <span data-ttu-id="f1378-111">De lo contrario, devuelve S \_ false o un código de error.</span><span class="sxs-lookup"><span data-stu-id="f1378-111">Otherwise, returns S\_FALSE or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1378-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f1378-112">Remarks</span></span>

<span data-ttu-id="f1378-113">El PIN de entrada llama a este método desde su propio método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="f1378-113">The input pin calls this method from its own [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method.</span></span> <span data-ttu-id="f1378-114">La clase derivada debe implementar este método.</span><span class="sxs-lookup"><span data-stu-id="f1378-114">The derived class must implement this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1378-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1378-115">Requirements</span></span>



| <span data-ttu-id="f1378-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1378-116">Requirement</span></span> | <span data-ttu-id="f1378-117">Value</span><span class="sxs-lookup"><span data-stu-id="f1378-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1378-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f1378-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f1378-119"><dt>Renbase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1378-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f1378-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f1378-120">Library</span></span><br/> | <dl> <span data-ttu-id="f1378-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f1378-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1378-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="f1378-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1378-123">**Clase CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="f1378-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




