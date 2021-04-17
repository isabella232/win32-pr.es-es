---
description: El método SetMediaType establece el tipo de medio para la conexión.
ms.assetid: db32b33b-df71-4f46-b53f-d7e647f5f559
title: Método CBasePin. SetMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 07ac736558cea12a16c695cf109c3d6283ce4a13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660943"
---
# <a name="cbasepinsetmediatype-method"></a><span data-ttu-id="5c491-103">CBasePin. SetMediaType, método</span><span class="sxs-lookup"><span data-stu-id="5c491-103">CBasePin.SetMediaType method</span></span>

<span data-ttu-id="5c491-104">El `SetMediaType` método establece el tipo de medio para la conexión.</span><span class="sxs-lookup"><span data-stu-id="5c491-104">The `SetMediaType` method sets the media type for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c491-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c491-105">Syntax</span></span>


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="5c491-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5c491-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c491-107">*p.p.*</span><span class="sxs-lookup"><span data-stu-id="5c491-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="5c491-108">Puntero a un objeto [**CMediaType**](cmediatype.md) que especifica el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="5c491-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c491-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5c491-109">Return value</span></span>

<span data-ttu-id="5c491-110">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="5c491-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c491-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c491-111">Remarks</span></span>

<span data-ttu-id="5c491-112">Este método establece el formato para una conexión de PIN.</span><span class="sxs-lookup"><span data-stu-id="5c491-112">This method establishes the format for a pin connection.</span></span> <span data-ttu-id="5c491-113">Antes de llamar a este método, el PIN llama al método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) para determinar si el tipo de medio es aceptable.</span><span class="sxs-lookup"><span data-stu-id="5c491-113">Before calling this method, the pin calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to determine whether the media type is acceptable.</span></span> <span data-ttu-id="5c491-114">Por lo tanto, se supone que el parámetro *PMT* es un tipo de medio aceptable.</span><span class="sxs-lookup"><span data-stu-id="5c491-114">Therefore, the *pmt* parameter is assumed to be an acceptable media type.</span></span>

<span data-ttu-id="5c491-115">En la clase base, este método establece la variable miembro [**CBasePin:: m \_ MT**](cbasepin-m-mt.md) y devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5c491-115">In the base class, this method sets the [**CBasePin::m\_mt**](cbasepin-m-mt.md) member variable and returns S\_OK.</span></span> <span data-ttu-id="5c491-116">Una clase derivada puede invalidar este método si requiere una notificación cuando se establece el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="5c491-116">A derived class can override this method if it requires notification when the media type is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c491-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c491-117">Requirements</span></span>



| <span data-ttu-id="5c491-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c491-118">Requirement</span></span> | <span data-ttu-id="5c491-119">Value</span><span class="sxs-lookup"><span data-stu-id="5c491-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c491-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5c491-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5c491-121"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5c491-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5c491-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5c491-122">Library</span></span><br/> | <dl> <span data-ttu-id="5c491-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="5c491-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c491-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="5c491-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c491-125">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="5c491-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




