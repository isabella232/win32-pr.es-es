---
description: 'Método CBasePin.SetMediaType: el método SetMediaType establece el tipo de medio para la conexión.'
ms.assetid: db32b33b-df71-4f46-b53f-d7e647f5f559
title: Método CBasePin.SetMediaType (Amfilter.h)
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
ms.openlocfilehash: b61b6179aa6364ebddd940b8853e22d628463e56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095993"
---
# <a name="cbasepinsetmediatype-method"></a><span data-ttu-id="09f7a-103">Método CBasePin.SetMediaType</span><span class="sxs-lookup"><span data-stu-id="09f7a-103">CBasePin.SetMediaType method</span></span>

<span data-ttu-id="09f7a-104">El `SetMediaType` método establece el tipo de medio para la conexión.</span><span class="sxs-lookup"><span data-stu-id="09f7a-104">The `SetMediaType` method sets the media type for the connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="09f7a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="09f7a-105">Syntax</span></span>


```C++
virtual HRESULT SetMediaType(
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="09f7a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="09f7a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09f7a-107">*Pmt*</span><span class="sxs-lookup"><span data-stu-id="09f7a-107">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="09f7a-108">Puntero a un [**objeto CMediaType**](cmediatype.md) que especifica el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="09f7a-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09f7a-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="09f7a-109">Return value</span></span>

<span data-ttu-id="09f7a-110">Devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="09f7a-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="09f7a-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="09f7a-111">Remarks</span></span>

<span data-ttu-id="09f7a-112">Este método establece el formato para una conexión de pin.</span><span class="sxs-lookup"><span data-stu-id="09f7a-112">This method establishes the format for a pin connection.</span></span> <span data-ttu-id="09f7a-113">Antes de llamar a este método, el pin llama al método [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) para determinar si el tipo de medio es aceptable.</span><span class="sxs-lookup"><span data-stu-id="09f7a-113">Before calling this method, the pin calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to determine whether the media type is acceptable.</span></span> <span data-ttu-id="09f7a-114">Por lo tanto, se supone que el parámetro *pmt* es un tipo de medio aceptable.</span><span class="sxs-lookup"><span data-stu-id="09f7a-114">Therefore, the *pmt* parameter is assumed to be an acceptable media type.</span></span>

<span data-ttu-id="09f7a-115">En la clase base, este método establece la variable miembro [**CBasePin::m \_ mt**](cbasepin-m-mt.md) y devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="09f7a-115">In the base class, this method sets the [**CBasePin::m\_mt**](cbasepin-m-mt.md) member variable and returns S\_OK.</span></span> <span data-ttu-id="09f7a-116">Una clase derivada puede invalidar este método si requiere notificación cuando se establece el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="09f7a-116">A derived class can override this method if it requires notification when the media type is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="09f7a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09f7a-117">Requirements</span></span>



| <span data-ttu-id="09f7a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="09f7a-118">Requirement</span></span> | <span data-ttu-id="09f7a-119">Value</span><span class="sxs-lookup"><span data-stu-id="09f7a-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09f7a-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="09f7a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="09f7a-121"><dt>Amfilter.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="09f7a-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="09f7a-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="09f7a-122">Library</span></span><br/> | <dl> <span data-ttu-id="09f7a-123"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="09f7a-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09f7a-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="09f7a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09f7a-125">**CBasePin (clase)**</span><span class="sxs-lookup"><span data-stu-id="09f7a-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




