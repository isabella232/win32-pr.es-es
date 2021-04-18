---
description: 'El método CheckCapabilities consulta si la secuencia tiene capacidades de búsqueda especificadas. Este método implementa el método IMediaSeeking:: CheckCapabilities.'
ms.assetid: 5d37e179-9e04-44e1-acbc-dfd2682830c0
title: Método CSourceSeeking. CheckCapabilities (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.CheckCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2f537973ac6c8f084ea42ba915a6293e581debef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660306"
---
# <a name="csourceseekingcheckcapabilities-method"></a><span data-ttu-id="f323b-104">CSourceSeeking. CheckCapabilities, método</span><span class="sxs-lookup"><span data-stu-id="f323b-104">CSourceSeeking.CheckCapabilities method</span></span>

<span data-ttu-id="f323b-105">El `CheckCapabilities` método consulta si la secuencia tiene capacidades de búsqueda especificadas.</span><span class="sxs-lookup"><span data-stu-id="f323b-105">The `CheckCapabilities` method queries whether the stream has specified seeking capabilities.</span></span> <span data-ttu-id="f323b-106">Este método implementa el método [**IMediaSeeking:: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="f323b-106">This method implements the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f323b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f323b-107">Syntax</span></span>


```C++
HRESULT CheckCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="f323b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f323b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f323b-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="f323b-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="f323b-110">Puntero a una combinación bit a bit de uno o más atributos de [**\_ \_ \_ funciones de búsqueda**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="f323b-110">Pointer to a bitwise combination of one or more [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f323b-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f323b-111">Return value</span></span>

<span data-ttu-id="f323b-112">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f323b-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="f323b-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f323b-113">Return code</span></span>                                                                               | <span data-ttu-id="f323b-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="f323b-114">Description</span></span>                                                            |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f323b-115"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="f323b-115"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="f323b-116">No todas las funcionalidades de *pCapabilities* están presentes.</span><span class="sxs-lookup"><span data-stu-id="f323b-116">Not all of the capabilities in *pCapabilities* are present.</span></span><br/> |
| <dl> <span data-ttu-id="f323b-117"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f323b-117"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="f323b-118">Todas las funcionalidades de *pCapabilities* están presentes.</span><span class="sxs-lookup"><span data-stu-id="f323b-118">All capabilities in *pCapabilities* are present.</span></span><br/>            |
| <dl> <span data-ttu-id="f323b-119"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="f323b-119"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="f323b-120">Argumento de puntero **nulo** .</span><span class="sxs-lookup"><span data-stu-id="f323b-120">**NULL** pointer argument.</span></span><br/>                                  |



 

## <a name="remarks"></a><span data-ttu-id="f323b-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f323b-121">Remarks</span></span>

<span data-ttu-id="f323b-122">Tal y como se implementa, este método comprueba el valor de *\* pCapabilities* con respecto a la variable miembro [**CSourceSeeking:: m \_ dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="f323b-122">As implemented, this method checks the value of *\*pCapabilities* against the [**CSourceSeeking::m\_dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) member variable.</span></span> <span data-ttu-id="f323b-123">Sin embargo, no establece *\* pCapabilities* igual a **m \_ dwSeekingCaps**, tal y como se describe en el método [**IMediaSeeking:: CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="f323b-123">However, it does not set *\*pCapabilities* equal to **m\_dwSeekingCaps**, as described for the [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) method.</span></span> <span data-ttu-id="f323b-124">Además, en el caso de que ninguna de las funcionalidades especificadas esté disponible, el método no devuelve E \_ .</span><span class="sxs-lookup"><span data-stu-id="f323b-124">Also, in the case where none of the specified capabilities are available, the method does not return E\_FAIL.</span></span> <span data-ttu-id="f323b-125">Una implementación más completa sería la siguiente:</span><span class="sxs-lookup"><span data-stu-id="f323b-125">A more complete implementation would be as follows:</span></span>


```C++
STDMETHODIMP CheckCapabilities(DWORD *pCapabilities)
{
    CheckPointer(pCapabilities, E_POINTER)
;
    DWORD dwCaps;
    HRESULT hr = GetCapabilities(&dwCaps);
    if (SUCCEEDED(hr))
    {
        dwCaps &= *pCapabilities;
        if (dwCaps)
        {
            hr =  (dwCaps == *pCapabilities ? S_OK : S_FALSE );
        }
        else 
        {
            hr = E_FAIL;
        }
        *pCapabilities = dwCaps;
    }
    else 
    {
        *pCapabilities = 0;
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="f323b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f323b-126">Requirements</span></span>



| <span data-ttu-id="f323b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f323b-127">Requirement</span></span> | <span data-ttu-id="f323b-128">Value</span><span class="sxs-lookup"><span data-stu-id="f323b-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f323b-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f323b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="f323b-130"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f323b-130"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f323b-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f323b-131">Library</span></span><br/> | <dl> <span data-ttu-id="f323b-132"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f323b-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f323b-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="f323b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f323b-134">**Clase CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="f323b-134">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




