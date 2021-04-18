---
description: El método AlterQuality notifica al filtro que se ha solicitado un cambio de calidad.
ms.assetid: 46743d6b-65cf-4d63-8913-114277d76da4
title: Método CTransformFilter. AlterQuality (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.AlterQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 592fc67dd5cee5e4f76b8171b6e842532d71371b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660305"
---
# <a name="ctransformfilteralterquality-method"></a><span data-ttu-id="6db4c-103">CTransformFilter. AlterQuality, método</span><span class="sxs-lookup"><span data-stu-id="6db4c-103">CTransformFilter.AlterQuality method</span></span>

<span data-ttu-id="6db4c-104">El `AlterQuality` método notifica al filtro que se ha solicitado un cambio de calidad.</span><span class="sxs-lookup"><span data-stu-id="6db4c-104">The `AlterQuality` method notifies the filter that a quality change is requested.</span></span>

## <a name="syntax"></a><span data-ttu-id="6db4c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6db4c-105">Syntax</span></span>


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a><span data-ttu-id="6db4c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6db4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6db4c-107">*respuestas*</span><span class="sxs-lookup"><span data-stu-id="6db4c-107">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="6db4c-108">Estructura de [**calidad**](/windows/win32/api/strmif/ns-strmif-quality) que contiene el mensaje de control de calidad.</span><span class="sxs-lookup"><span data-stu-id="6db4c-108">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6db4c-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6db4c-109">Return value</span></span>

<span data-ttu-id="6db4c-110">Devuelve un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6db4c-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6db4c-111">Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="6db4c-111">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="6db4c-112">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6db4c-112">Return code</span></span>                                                                             | <span data-ttu-id="6db4c-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="6db4c-113">Description</span></span>                                                                           |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6db4c-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="6db4c-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="6db4c-115">No controló el mensaje de calidad.</span><span class="sxs-lookup"><span data-stu-id="6db4c-115">Did not handle the quality message.</span></span> <span data-ttu-id="6db4c-116">El mensaje se debe pasar al nivel superior.</span><span class="sxs-lookup"><span data-stu-id="6db4c-116">The message should be passed upstream.</span></span><br/> |
| <dl> <span data-ttu-id="6db4c-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="6db4c-117"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="6db4c-118">Controló el mensaje de calidad.</span><span class="sxs-lookup"><span data-stu-id="6db4c-118">Handled the quality message.</span></span> <span data-ttu-id="6db4c-119">No es necesario realizar ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="6db4c-119">No further action is necessary.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="6db4c-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6db4c-120">Remarks</span></span>

<span data-ttu-id="6db4c-121">Invalide este método si el filtro puede realizar el control de calidad.</span><span class="sxs-lookup"><span data-stu-id="6db4c-121">Override this method if the filter can perform quality control.</span></span> <span data-ttu-id="6db4c-122">Para obtener más información, vea [Administración de control de calidad](quality-control-management.md).</span><span class="sxs-lookup"><span data-stu-id="6db4c-122">For more information, see [Quality-Control Management](quality-control-management.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6db4c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6db4c-123">Requirements</span></span>



| <span data-ttu-id="6db4c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6db4c-124">Requirement</span></span> | <span data-ttu-id="6db4c-125">Value</span><span class="sxs-lookup"><span data-stu-id="6db4c-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6db4c-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6db4c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6db4c-127"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6db4c-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6db4c-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6db4c-128">Library</span></span><br/> | <dl> <span data-ttu-id="6db4c-129"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="6db4c-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6db4c-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="6db4c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6db4c-131">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="6db4c-131">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




