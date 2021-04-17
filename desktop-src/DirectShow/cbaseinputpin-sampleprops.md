---
description: El método SampleProps recupera las propiedades del ejemplo más reciente, en una \_ estructura de propiedades AM SAMPLE2 \_ .
ms.assetid: d4c98c35-f8b2-4111-bae9-4e0f58a0cc8a
title: Método CBaseInputPin. SampleProps (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.SampleProps
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 45663cfd221c7a31abe5f85a494869b24d1ddd8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661302"
---
# <a name="cbaseinputpinsampleprops-method"></a><span data-ttu-id="a1516-103">CBaseInputPin. SampleProps, método</span><span class="sxs-lookup"><span data-stu-id="a1516-103">CBaseInputPin.SampleProps method</span></span>

<span data-ttu-id="a1516-104">El `SampleProps` método recupera las propiedades del ejemplo más reciente, en una estructura de [**\_ \_ propiedades AM SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .</span><span class="sxs-lookup"><span data-stu-id="a1516-104">The `SampleProps` method retrieves the properties of the most recent sample, in an [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1516-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1516-105">Syntax</span></span>


```C++
AM_SAMPLE2_PROPERTIES* SampleProps();
```



## <a name="parameters"></a><span data-ttu-id="a1516-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1516-106">Parameters</span></span>

<span data-ttu-id="a1516-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="a1516-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a1516-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a1516-108">Return value</span></span>

<span data-ttu-id="a1516-109">Devuelve la dirección de la variable miembro [**CBaseInputPin:: m \_ SampleProps**](cbaseinputpin-m-sampleprops.md) .</span><span class="sxs-lookup"><span data-stu-id="a1516-109">Returns the address of the [**CBaseInputPin::m\_SampleProps**](cbaseinputpin-m-sampleprops.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1516-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1516-110">Requirements</span></span>



| <span data-ttu-id="a1516-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1516-111">Requirement</span></span> | <span data-ttu-id="a1516-112">Value</span><span class="sxs-lookup"><span data-stu-id="a1516-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1516-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1516-113">Header</span></span><br/>  | <dl> <span data-ttu-id="a1516-114"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a1516-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a1516-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a1516-115">Library</span></span><br/> | <dl> <span data-ttu-id="a1516-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a1516-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1516-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1516-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1516-118">**Clase CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="a1516-118">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




