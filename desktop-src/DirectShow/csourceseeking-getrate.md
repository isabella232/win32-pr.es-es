---
description: 'Método CSourceSeeking.GetRate: el método GetRate recupera la velocidad de reproducción. Este método implementa el método IMediaSeeking::GetRate.'
ms.assetid: e5c3ef27-6f57-4c74-b197-a3c4efb31239
title: Método CSourceSeeking.GetRate (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fef379ef06cd0982f1eb5742ac2624d706ed73a8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085233"
---
# <a name="csourceseekinggetrate-method"></a><span data-ttu-id="63482-104">Método CSourceSeeking.GetRate</span><span class="sxs-lookup"><span data-stu-id="63482-104">CSourceSeeking.GetRate method</span></span>

<span data-ttu-id="63482-105">El `GetRate` método recupera la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="63482-105">The `GetRate` method retrieves the playback rate.</span></span> <span data-ttu-id="63482-106">Este método implementa el [**método IMediaSeeking::GetRate.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate)</span><span class="sxs-lookup"><span data-stu-id="63482-106">This method implements the [**IMediaSeeking::GetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="63482-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63482-107">Syntax</span></span>


```C++
HRESULT GetRate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="63482-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63482-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63482-109">*pdRate*</span><span class="sxs-lookup"><span data-stu-id="63482-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="63482-110">Puntero a una variable que recibe la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="63482-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63482-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63482-111">Return value</span></span>

<span data-ttu-id="63482-112">Devuelve uno de los **valores HRESULT** enumerados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="63482-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="63482-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="63482-113">Return code</span></span>                                                                               | <span data-ttu-id="63482-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="63482-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="63482-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="63482-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="63482-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="63482-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="63482-117"><dt>**PUNTERO \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="63482-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="63482-118">**Valor de** puntero NULL</span><span class="sxs-lookup"><span data-stu-id="63482-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="63482-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="63482-119">Remarks</span></span>

<span data-ttu-id="63482-120">La velocidad de reproducción se especifica mediante la variable miembro [**CSourceSeeking::m \_ dRateSeeking.**](csourceseeking-m-drateseeking.md)</span><span class="sxs-lookup"><span data-stu-id="63482-120">The playback rate is specified by the [**CSourceSeeking::m\_dRateSeeking**](csourceseeking-m-drateseeking.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="63482-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63482-121">Requirements</span></span>



| <span data-ttu-id="63482-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="63482-122">Requirement</span></span> | <span data-ttu-id="63482-123">Value</span><span class="sxs-lookup"><span data-stu-id="63482-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63482-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63482-124">Header</span></span><br/>  | <dl> <span data-ttu-id="63482-125"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="63482-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="63482-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="63482-126">Library</span></span><br/> | <dl> <span data-ttu-id="63482-127"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="63482-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63482-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="63482-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63482-129">**CSourceSeeking (clase)**</span><span class="sxs-lookup"><span data-stu-id="63482-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




