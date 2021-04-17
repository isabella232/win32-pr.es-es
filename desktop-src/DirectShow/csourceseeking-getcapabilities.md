---
description: 'El método GetCapabilities recupera todas las funciones de búsqueda de la secuencia. Este método implementa el método IMediaSeeking:: GetCapabilities.'
ms.assetid: a2ff7ea2-09bd-49a7-8e1b-d6360939036e
title: Método CSourceSeeking. GetCapabilities (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eda23944fd039576bb5de74fbb7c32e375415670
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660786"
---
# <a name="csourceseekinggetcapabilities-method"></a><span data-ttu-id="c0255-104">CSourceSeeking. GetCapabilities, método</span><span class="sxs-lookup"><span data-stu-id="c0255-104">CSourceSeeking.GetCapabilities method</span></span>

<span data-ttu-id="c0255-105">El `GetCapabilities` método recupera todas las funciones de búsqueda de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="c0255-105">The `GetCapabilities` method retrieves all the seeking capabilities of the stream.</span></span> <span data-ttu-id="c0255-106">Este método implementa el método [**IMediaSeeking:: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="c0255-106">This method implements the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0255-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0255-107">Syntax</span></span>


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="c0255-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c0255-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0255-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="c0255-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="c0255-110">Puntero a una variable que recibe una combinación bit a bit de los marcadores de búsqueda de [**\_ \_ \_ funciones de búsqueda**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) .</span><span class="sxs-lookup"><span data-stu-id="c0255-110">Pointer to a variable that receives a bitwise combination of [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0255-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c0255-111">Return value</span></span>

<span data-ttu-id="c0255-112">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="c0255-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="c0255-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c0255-113">Return code</span></span>                                                                               | <span data-ttu-id="c0255-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0255-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="c0255-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="c0255-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="c0255-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="c0255-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="c0255-117"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="c0255-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="c0255-118">Valor de puntero **nulo**</span><span class="sxs-lookup"><span data-stu-id="c0255-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c0255-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c0255-119">Remarks</span></span>

<span data-ttu-id="c0255-120">Las capacidades de búsqueda se especifican mediante la variable miembro [**CSourceSeeking:: m \_ dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="c0255-120">The seeking capabilities are specified by the [**CSourceSeeking::m\_dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0255-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0255-121">Requirements</span></span>



| <span data-ttu-id="c0255-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0255-122">Requirement</span></span> | <span data-ttu-id="c0255-123">Value</span><span class="sxs-lookup"><span data-stu-id="c0255-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0255-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c0255-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c0255-125"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c0255-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c0255-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c0255-126">Library</span></span><br/> | <dl> <span data-ttu-id="c0255-127"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c0255-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0255-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0255-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0255-129">**Clase CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="c0255-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




