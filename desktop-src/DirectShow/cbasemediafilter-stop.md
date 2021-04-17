---
description: 'El método Stop detiene el objeto. Este método implementa el método IMediaFilter:: stop.'
ms.assetid: 9282d90a-932c-4ba0-84f1-1de2c125bfbd
title: Método CBaseMediaFilter. STOP (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22bb45234c8be832f8ea30ed70b50c8f4919b7e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660201"
---
# <a name="cbasemediafilterstop-method"></a><span data-ttu-id="0ed5a-104">CBaseMediaFilter. STOP (método)</span><span class="sxs-lookup"><span data-stu-id="0ed5a-104">CBaseMediaFilter.Stop method</span></span>

<span data-ttu-id="0ed5a-105">El `Stop` método detiene el objeto.</span><span class="sxs-lookup"><span data-stu-id="0ed5a-105">The `Stop` method stops the object.</span></span> <span data-ttu-id="0ed5a-106">Este método implementa el método [**IMediaFilter:: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .</span><span class="sxs-lookup"><span data-stu-id="0ed5a-106">This method implements the [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ed5a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0ed5a-107">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="0ed5a-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ed5a-108">Parameters</span></span>

<span data-ttu-id="0ed5a-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="0ed5a-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ed5a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ed5a-110">Return value</span></span>

<span data-ttu-id="0ed5a-111">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="0ed5a-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ed5a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ed5a-112">Remarks</span></span>

<span data-ttu-id="0ed5a-113">En la clase base, este método establece la variable miembro de [**\_ Estado CBaseMediaFilter:: m**](cbasemediafilter-m-state.md) en estado \_ detenido, pero no hace nada más.</span><span class="sxs-lookup"><span data-stu-id="0ed5a-113">In the base class, this method sets the [**CBaseMediaFilter::m\_State**](cbasemediafilter-m-state.md) member variable to State\_Stopped but does nothing else.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ed5a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ed5a-114">Requirements</span></span>



| <span data-ttu-id="0ed5a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ed5a-115">Requirement</span></span> | <span data-ttu-id="0ed5a-116">Value</span><span class="sxs-lookup"><span data-stu-id="0ed5a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ed5a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ed5a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0ed5a-118"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0ed5a-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0ed5a-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0ed5a-119">Library</span></span><br/> | <dl> <span data-ttu-id="0ed5a-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0ed5a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ed5a-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ed5a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ed5a-122">**Clase CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="0ed5a-122">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




