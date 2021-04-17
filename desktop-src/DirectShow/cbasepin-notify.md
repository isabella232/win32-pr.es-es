---
description: 'El método Notify notifica al pin que se ha solicitado un cambio de calidad. Este método implementa el método IQualityControl:: Notify.'
ms.assetid: 5e9394d9-8d3c-4091-b45f-345a3f7270db
title: Método CBasePin. Notify (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f34ea630a461226c32b9d827b2b91dcd0874cac7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670908"
---
# <a name="cbasepinnotify-method"></a><span data-ttu-id="20a63-104">CBasePin. Notify (método)</span><span class="sxs-lookup"><span data-stu-id="20a63-104">CBasePin.Notify method</span></span>

<span data-ttu-id="20a63-105">El `Notify` método notifica al pin que se ha solicitado un cambio de calidad.</span><span class="sxs-lookup"><span data-stu-id="20a63-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="20a63-106">Este método implementa el método [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) .</span><span class="sxs-lookup"><span data-stu-id="20a63-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="20a63-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20a63-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="20a63-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="20a63-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20a63-109">*pSelf*</span><span class="sxs-lookup"><span data-stu-id="20a63-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="20a63-110">Puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro que entregó el mensaje de control de calidad.</span><span class="sxs-lookup"><span data-stu-id="20a63-110">Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the filter that delivered the quality-control message.</span></span>

</dd> <dt>

<span data-ttu-id="20a63-111">*respuestas*</span><span class="sxs-lookup"><span data-stu-id="20a63-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="20a63-112">Especifica una estructura de [**calidad**](/windows/win32/api/strmif/ns-strmif-quality) que contiene el mensaje de control de calidad.</span><span class="sxs-lookup"><span data-stu-id="20a63-112">Specifies a [**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20a63-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="20a63-113">Return value</span></span>

<span data-ttu-id="20a63-114">La clase base devuelve E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="20a63-114">The base class returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="20a63-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="20a63-115">Remarks</span></span>

<span data-ttu-id="20a63-116">Los pin de salida deben invalidar este método para aceptar mensajes de control de calidad.</span><span class="sxs-lookup"><span data-stu-id="20a63-116">Output pins should override this method to accept quality-control messages.</span></span>

<span data-ttu-id="20a63-117">Si se instaló un administrador de calidad externo (consulte [**CBasePin:: SetSink**](cbasepin-setsink.md)), pase el mensaje a ese administrador de calidad.</span><span class="sxs-lookup"><span data-stu-id="20a63-117">If an external quality manager was installed (see [**CBasePin::SetSink**](cbasepin-setsink.md)), pass the message to that quality manager.</span></span> <span data-ttu-id="20a63-118">De lo contrario, el filtro debe controlar el propio mensaje o pasar el mensaje ascendente.</span><span class="sxs-lookup"><span data-stu-id="20a63-118">Otherwise, the filter should handle the message itself, or pass the message upstream.</span></span> <span data-ttu-id="20a63-119">Para obtener más información, vea [Administración de control de calidad](quality-control-management.md).</span><span class="sxs-lookup"><span data-stu-id="20a63-119">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="20a63-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20a63-120">Requirements</span></span>



| <span data-ttu-id="20a63-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="20a63-121">Requirement</span></span> | <span data-ttu-id="20a63-122">Value</span><span class="sxs-lookup"><span data-stu-id="20a63-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20a63-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="20a63-123">Header</span></span><br/>  | <dl> <span data-ttu-id="20a63-124"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20a63-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="20a63-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="20a63-125">Library</span></span><br/> | <dl> <span data-ttu-id="20a63-126"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="20a63-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20a63-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="20a63-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20a63-128">**Clase CBasePin**</span><span class="sxs-lookup"><span data-stu-id="20a63-128">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




