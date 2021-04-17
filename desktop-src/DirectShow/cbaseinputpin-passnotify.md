---
description: El método PassNotify pasa un mensaje de control de calidad al objeto adecuado.
ms.assetid: dbc9a4b7-a522-4fbf-8e3a-af50e11c1d80
title: Método CBaseInputPin. PassNotify (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.PassNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36316815ae1d9fde1a18fb36029da92ae6263f20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670695"
---
# <a name="cbaseinputpinpassnotify-method"></a><span data-ttu-id="08ab2-103">CBaseInputPin. PassNotify, método</span><span class="sxs-lookup"><span data-stu-id="08ab2-103">CBaseInputPin.PassNotify method</span></span>

<span data-ttu-id="08ab2-104">El `PassNotify` método pasa un mensaje de control de calidad al objeto adecuado.</span><span class="sxs-lookup"><span data-stu-id="08ab2-104">The `PassNotify` method passes a quality-control message to the appropriate object.</span></span>

## <a name="syntax"></a><span data-ttu-id="08ab2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08ab2-105">Syntax</span></span>


```C++
HRESULT PassNotify(
   Quality q
);
```



## <a name="parameters"></a><span data-ttu-id="08ab2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08ab2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08ab2-107">*respuestas*</span><span class="sxs-lookup"><span data-stu-id="08ab2-107">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="08ab2-108">Estructura de [**calidad**](/windows/win32/api/strmif/ns-strmif-quality) que contiene el mensaje de control de calidad.</span><span class="sxs-lookup"><span data-stu-id="08ab2-108">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08ab2-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08ab2-109">Return value</span></span>

<span data-ttu-id="08ab2-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="08ab2-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="08ab2-111">Entre los valores posibles se incluyen los que aparecen en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="08ab2-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="08ab2-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="08ab2-112">Return code</span></span>                                                                                       | <span data-ttu-id="08ab2-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="08ab2-113">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="08ab2-114"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="08ab2-114"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="08ab2-115">Correcto.</span><span class="sxs-lookup"><span data-stu-id="08ab2-115">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="08ab2-116"><dt>**VFW \_ E \_ no \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="08ab2-116"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="08ab2-117">No se encontró un objeto para aceptar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="08ab2-117">Could not find an object to accept the message.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="08ab2-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08ab2-118">Remarks</span></span>

<span data-ttu-id="08ab2-119">Llame a este método si el filtro no controla los mensajes de control de calidad.</span><span class="sxs-lookup"><span data-stu-id="08ab2-119">Call this method if the filter does not handle quality-control messages.</span></span> <span data-ttu-id="08ab2-120">Este método pasa el mensaje a uno de los siguientes objetos, en orden de preferencia:</span><span class="sxs-lookup"><span data-stu-id="08ab2-120">This method passes the message to one of the following objects, in order of preference:</span></span>

-   <span data-ttu-id="08ab2-121">Un administrador de control de calidad externo, si se llamó al método [**IQualityControl:: SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) .</span><span class="sxs-lookup"><span data-stu-id="08ab2-121">An external quality-control manager, if the [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) method was called.</span></span>
-   <span data-ttu-id="08ab2-122">El PIN de salida de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="08ab2-122">The upstream output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="08ab2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08ab2-123">Requirements</span></span>



| <span data-ttu-id="08ab2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="08ab2-124">Requirement</span></span> | <span data-ttu-id="08ab2-125">Value</span><span class="sxs-lookup"><span data-stu-id="08ab2-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08ab2-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="08ab2-126">Header</span></span><br/>  | <dl> <span data-ttu-id="08ab2-127"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="08ab2-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="08ab2-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="08ab2-128">Library</span></span><br/> | <dl> <span data-ttu-id="08ab2-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="08ab2-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08ab2-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="08ab2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08ab2-131">**Clase CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="08ab2-131">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> <dt>

[<span data-ttu-id="08ab2-132">Administración de control de calidad</span><span class="sxs-lookup"><span data-stu-id="08ab2-132">Quality-Control Management</span></span>](quality-control-management.md)
</dt> </dl>

 

 




