---
description: El método DisplayTypeInfo muestra información de tipo de medio durante la depuración.
ms.assetid: fd10d37b-57f5-4246-8ca3-f4bc59911445
title: Método CBasePin. DisplayTypeInfo (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisplayTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 681e424505bb2ff840ac5beaa48431f17a5d177b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660792"
---
# <a name="cbasepindisplaytypeinfo-method"></a><span data-ttu-id="6ce54-103">CBasePin. DisplayTypeInfo, método</span><span class="sxs-lookup"><span data-stu-id="6ce54-103">CBasePin.DisplayTypeInfo method</span></span>

<span data-ttu-id="6ce54-104">El `DisplayTypeInfo` método muestra información de tipo de medio durante la depuración.</span><span class="sxs-lookup"><span data-stu-id="6ce54-104">The `DisplayTypeInfo` method displays media type information during debugging.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ce54-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ce54-105">Syntax</span></span>


```C++
void DisplayTypeInfo(
         IPin       *pPin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="6ce54-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ce54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ce54-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="6ce54-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="6ce54-108">ignorado.</span><span class="sxs-lookup"><span data-stu-id="6ce54-108">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="6ce54-109">*p.p.*</span><span class="sxs-lookup"><span data-stu-id="6ce54-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="6ce54-110">Puntero a un objeto [**CMediaType**](cmediatype.md) que especifica el tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="6ce54-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ce54-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ce54-111">Return value</span></span>

<span data-ttu-id="6ce54-112">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6ce54-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ce54-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ce54-113">Remarks</span></span>

<span data-ttu-id="6ce54-114">En las compilaciones de depuración, este método llama a la función [**DbgLog**](dbglog.md) para mostrar el tipo de medio especificado.</span><span class="sxs-lookup"><span data-stu-id="6ce54-114">In debug builds, this method calls the [**DbgLog**](dbglog.md) function to display the specified media type.</span></span> <span data-ttu-id="6ce54-115">En las compilaciones comerciales, este método no hace nada.</span><span class="sxs-lookup"><span data-stu-id="6ce54-115">In retail builds, this method does nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ce54-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ce54-116">Requirements</span></span>



| <span data-ttu-id="6ce54-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ce54-117">Requirement</span></span> | <span data-ttu-id="6ce54-118">Value</span><span class="sxs-lookup"><span data-stu-id="6ce54-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ce54-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ce54-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6ce54-120"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ce54-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6ce54-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6ce54-121">Library</span></span><br/> | <dl> <span data-ttu-id="6ce54-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6ce54-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ce54-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ce54-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ce54-124">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="6ce54-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




