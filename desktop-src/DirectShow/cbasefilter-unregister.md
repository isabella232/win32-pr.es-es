---
description: El método unregister quita el filtro del registro.
ms.assetid: 2eb70e9f-1acf-433e-972f-24fb32eaeb13
title: Método CBaseFilter. Unregister (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Unregister
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8b46e74e4009f6767788fa120984eca0e89fb551
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660433"
---
# <a name="cbasefilterunregister-method"></a><span data-ttu-id="bd34c-103">CBaseFilter. Unregister (método)</span><span class="sxs-lookup"><span data-stu-id="bd34c-103">CBaseFilter.Unregister method</span></span>

<span data-ttu-id="bd34c-104">El `Unregister` método quita el filtro del registro.</span><span class="sxs-lookup"><span data-stu-id="bd34c-104">The `Unregister` method removes the filter from the registry.</span></span>

> [!Note]  
> <span data-ttu-id="bd34c-105">Este método está obsoleto.</span><span class="sxs-lookup"><span data-stu-id="bd34c-105">This method is obsolete.</span></span> <span data-ttu-id="bd34c-106">Se debe anular el registro de nuevos filtros mediante la función [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) .</span><span class="sxs-lookup"><span data-stu-id="bd34c-106">New filters should be unregistered using the [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md) function.</span></span> <span data-ttu-id="bd34c-107">Para obtener más información, consulte [Cómo registrar filtros de DirectShow](how-to-register-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="bd34c-107">For more information, see [How to Register DirectShow Filters](how-to-register-directshow-filters.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="bd34c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd34c-108">Syntax</span></span>


```C++
HRESULT Unregister();
```



## <a name="parameters"></a><span data-ttu-id="bd34c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bd34c-109">Parameters</span></span>

<span data-ttu-id="bd34c-110">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="bd34c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bd34c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bd34c-111">Return value</span></span>

<span data-ttu-id="bd34c-112">Devuelve S \_ correcto si es correcto o un valor **HRESULT** que indica la causa del error.</span><span class="sxs-lookup"><span data-stu-id="bd34c-112">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd34c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd34c-113">Requirements</span></span>



| <span data-ttu-id="bd34c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd34c-114">Requirement</span></span> | <span data-ttu-id="bd34c-115">Value</span><span class="sxs-lookup"><span data-stu-id="bd34c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd34c-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bd34c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="bd34c-117"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bd34c-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bd34c-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bd34c-118">Library</span></span><br/> | <dl> <span data-ttu-id="bd34c-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="bd34c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd34c-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="bd34c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd34c-121">**Clase CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="bd34c-121">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




