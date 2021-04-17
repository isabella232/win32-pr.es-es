---
description: 'El método GetPreroll recupera el tiempo de prelanzamiento. Este método implementa el método IMediaSeeking:: GetPreroll.'
ms.assetid: 2395d5b2-8c1f-40cd-8d4a-48620debe7a7
title: Método CSourceSeeking. GetPreroll (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetPreroll
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 097af089a7221f005cf7f3aac74953166af3cb2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690556"
---
# <a name="csourceseekinggetpreroll-method"></a><span data-ttu-id="19810-104">CSourceSeeking. GetPreroll, método</span><span class="sxs-lookup"><span data-stu-id="19810-104">CSourceSeeking.GetPreroll method</span></span>

<span data-ttu-id="19810-105">El `GetPreroll` método recupera el tiempo de prelanzamiento.</span><span class="sxs-lookup"><span data-stu-id="19810-105">The `GetPreroll` method retrieves the preroll time.</span></span> <span data-ttu-id="19810-106">Este método implementa el método [**IMediaSeeking:: GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) .</span><span class="sxs-lookup"><span data-stu-id="19810-106">This method implements the [**IMediaSeeking::GetPreroll**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getpreroll) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="19810-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19810-107">Syntax</span></span>


```C++
HRESULT GetPreroll(
   LONGLONG *pPreroll
);
```



## <a name="parameters"></a><span data-ttu-id="19810-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19810-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19810-109">*pPreroll*</span><span class="sxs-lookup"><span data-stu-id="19810-109">*pPreroll*</span></span> 
</dt> <dd>

<span data-ttu-id="19810-110">Puntero a una variable que recibe el tiempo de prelanzamiento.</span><span class="sxs-lookup"><span data-stu-id="19810-110">Pointer to a variable that receives the preroll time.</span></span> <span data-ttu-id="19810-111">El valor se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="19810-111">The value is set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19810-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19810-112">Return value</span></span>

<span data-ttu-id="19810-113">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="19810-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="19810-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="19810-114">Return code</span></span>                                                                               | <span data-ttu-id="19810-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="19810-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="19810-116"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="19810-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="19810-117">Correcto</span><span class="sxs-lookup"><span data-stu-id="19810-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="19810-118"><dt>**\_puntero E**</dt></span><span class="sxs-lookup"><span data-stu-id="19810-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="19810-119">Valor de puntero **nulo**</span><span class="sxs-lookup"><span data-stu-id="19810-119">**NULL** pointer value</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="19810-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19810-120">Requirements</span></span>



| <span data-ttu-id="19810-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="19810-121">Requirement</span></span> | <span data-ttu-id="19810-122">Value</span><span class="sxs-lookup"><span data-stu-id="19810-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19810-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="19810-123">Header</span></span><br/>  | <dl> <span data-ttu-id="19810-124"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="19810-124"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="19810-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="19810-125">Library</span></span><br/> | <dl> <span data-ttu-id="19810-126"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="19810-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19810-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="19810-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19810-128">**Clase CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="19810-128">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




