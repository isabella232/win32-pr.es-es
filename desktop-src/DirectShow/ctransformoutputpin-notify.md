---
description: 'Método CTransformOutputPin.Notify: el método Notify notifica al pin que se solicita un cambio de calidad. Este método implementa el método IQualityControl::Notify.'
ms.assetid: cdb93eef-90d5-4111-a3d4-175903f44a13
title: Método CTransformOutputPin.Notify (Transfrm.h)
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
ms.openlocfilehash: 9a55e493c737b5a5864ec0a8dd38eee3abbfa586
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084813"
---
# <a name="ctransformoutputpinnotify-method"></a><span data-ttu-id="c4ad1-104">CTransformOutputPin.Notify (método)</span><span class="sxs-lookup"><span data-stu-id="c4ad1-104">CTransformOutputPin.Notify method</span></span>

<span data-ttu-id="c4ad1-105">El `Notify` método notifica al pin que se solicita un cambio de calidad.</span><span class="sxs-lookup"><span data-stu-id="c4ad1-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="c4ad1-106">Este método implementa el [**método IQualityControl::Notify.**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify)</span><span class="sxs-lookup"><span data-stu-id="c4ad1-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4ad1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4ad1-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="c4ad1-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4ad1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4ad1-109">*pSelf*</span><span class="sxs-lookup"><span data-stu-id="c4ad1-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="c4ad1-110">Puntero a la [**interfaz IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro que entregó el mensaje de control de calidad.</span><span class="sxs-lookup"><span data-stu-id="c4ad1-110">Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the filter that delivered the quality control message.</span></span>

</dd> <dt>

<span data-ttu-id="c4ad1-111">*Q*</span><span class="sxs-lookup"><span data-stu-id="c4ad1-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="c4ad1-112">[**Estructura**](/windows/win32/api/strmif/ns-strmif-quality) de calidad que contiene el mensaje de control de calidad.</span><span class="sxs-lookup"><span data-stu-id="c4ad1-112">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4ad1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4ad1-113">Return value</span></span>

<span data-ttu-id="c4ad1-114">Devuelve un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="c4ad1-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c4ad1-115">Los valores posibles incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c4ad1-115">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="c4ad1-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c4ad1-116">Return code</span></span>                                                                                       | <span data-ttu-id="c4ad1-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4ad1-117">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="c4ad1-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c4ad1-118"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="c4ad1-119">Correcto.</span><span class="sxs-lookup"><span data-stu-id="c4ad1-119">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="c4ad1-120"><dt>**VFW \_ E \_ NO \_ ENCONTRADO**</dt></span><span class="sxs-lookup"><span data-stu-id="c4ad1-120"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="c4ad1-121">No se encontró un objeto para aceptar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="c4ad1-121">Could not find an object to accept the message.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c4ad1-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c4ad1-122">Remarks</span></span>

<span data-ttu-id="c4ad1-123">Este método llama al método [**CTransformFilter::AlterQuality del**](ctransformfilter-alterquality.md) filtro.</span><span class="sxs-lookup"><span data-stu-id="c4ad1-123">This method calls the filter's [**CTransformFilter::AlterQuality**](ctransformfilter-alterquality.md) method.</span></span> <span data-ttu-id="c4ad1-124">Si el filtro no controla el mensaje de calidad, este método llama al método [**CBaseInputPin::P assNotify**](cbaseinputpin-passnotify.md) en el pin de entrada del filtro.</span><span class="sxs-lookup"><span data-stu-id="c4ad1-124">If the filter does not handle the quality message, this method calls the [**CBaseInputPin::PassNotify**](cbaseinputpin-passnotify.md) method on the filter's input pin.</span></span> <span data-ttu-id="c4ad1-125">El **método PassNotify** pasa el mensaje de calidad ascendente (o a un administrador de calidad personalizado, si se instaló uno).</span><span class="sxs-lookup"><span data-stu-id="c4ad1-125">The **PassNotify** method passes the quality message upstream (or to a custom quality manager, if one was installed).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4ad1-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4ad1-126">Requirements</span></span>



| <span data-ttu-id="c4ad1-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4ad1-127">Requirement</span></span> | <span data-ttu-id="c4ad1-128">Value</span><span class="sxs-lookup"><span data-stu-id="c4ad1-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4ad1-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c4ad1-129">Header</span></span><br/>  | <dl> <span data-ttu-id="c4ad1-130"><dt>Transfrm.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4ad1-130"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c4ad1-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c4ad1-131">Library</span></span><br/> | <dl> <span data-ttu-id="c4ad1-132"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c4ad1-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




