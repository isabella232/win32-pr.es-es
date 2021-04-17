---
description: 'El método Notify notifica al pin que se ha solicitado un cambio de calidad. Este método implementa el método IQualityControl:: Notify.'
ms.assetid: cdb93eef-90d5-4111-a3d4-175903f44a13
title: Método CTransformOutputPin. Notify (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6ace7e25f1413f6e17a4d19ef937732ea8c689a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661003"
---
# <a name="ctransformoutputpinnotify-method"></a><span data-ttu-id="bcd03-104">CTransformOutputPin. Notify (método)</span><span class="sxs-lookup"><span data-stu-id="bcd03-104">CTransformOutputPin.Notify method</span></span>

<span data-ttu-id="bcd03-105">El `Notify` método notifica al pin que se ha solicitado un cambio de calidad.</span><span class="sxs-lookup"><span data-stu-id="bcd03-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="bcd03-106">Este método implementa el método [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) .</span><span class="sxs-lookup"><span data-stu-id="bcd03-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcd03-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bcd03-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="bcd03-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bcd03-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcd03-109">*pSelf*</span><span class="sxs-lookup"><span data-stu-id="bcd03-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="bcd03-110">Puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro que entregó el mensaje de control de calidad.</span><span class="sxs-lookup"><span data-stu-id="bcd03-110">Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the filter that delivered the quality control message.</span></span>

</dd> <dt>

<span data-ttu-id="bcd03-111">*respuestas*</span><span class="sxs-lookup"><span data-stu-id="bcd03-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="bcd03-112">Estructura de [**calidad**](/windows/win32/api/strmif/ns-strmif-quality) que contiene el mensaje de control de calidad.</span><span class="sxs-lookup"><span data-stu-id="bcd03-112">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcd03-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bcd03-113">Return value</span></span>

<span data-ttu-id="bcd03-114">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bcd03-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="bcd03-115">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="bcd03-115">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="bcd03-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="bcd03-116">Return code</span></span>                                                                                       | <span data-ttu-id="bcd03-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="bcd03-117">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="bcd03-118"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="bcd03-118"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="bcd03-119">Correcto.</span><span class="sxs-lookup"><span data-stu-id="bcd03-119">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="bcd03-120"><dt>**VFW \_ E \_ no \_ encontrado**</dt></span><span class="sxs-lookup"><span data-stu-id="bcd03-120"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="bcd03-121">No se encontró un objeto para aceptar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="bcd03-121">Could not find an object to accept the message.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bcd03-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bcd03-122">Remarks</span></span>

<span data-ttu-id="bcd03-123">Este método llama al método [**CTransformFilter:: AlterQuality**](ctransformfilter-alterquality.md) del filtro.</span><span class="sxs-lookup"><span data-stu-id="bcd03-123">This method calls the filter's [**CTransformFilter::AlterQuality**](ctransformfilter-alterquality.md) method.</span></span> <span data-ttu-id="bcd03-124">Si el filtro no controla el mensaje de calidad, este método llama al método [**CBaseInputPin::P assnotify**](cbaseinputpin-passnotify.md) en el PIN de entrada del filtro.</span><span class="sxs-lookup"><span data-stu-id="bcd03-124">If the filter does not handle the quality message, this method calls the [**CBaseInputPin::PassNotify**](cbaseinputpin-passnotify.md) method on the filter's input pin.</span></span> <span data-ttu-id="bcd03-125">El método **PassNotify** pasa el mensaje de calidad ascendente (o a un administrador de calidad personalizado, si se ha instalado alguno).</span><span class="sxs-lookup"><span data-stu-id="bcd03-125">The **PassNotify** method passes the quality message upstream (or to a custom quality manager, if one was installed).</span></span>

## <a name="requirements"></a><span data-ttu-id="bcd03-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcd03-126">Requirements</span></span>



| <span data-ttu-id="bcd03-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcd03-127">Requirement</span></span> | <span data-ttu-id="bcd03-128">Value</span><span class="sxs-lookup"><span data-stu-id="bcd03-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcd03-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bcd03-129">Header</span></span><br/>  | <dl> <span data-ttu-id="bcd03-130"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bcd03-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bcd03-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bcd03-131">Library</span></span><br/> | <dl> <span data-ttu-id="bcd03-132"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="bcd03-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




