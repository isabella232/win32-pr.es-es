---
description: 'Método CSourceSeeking.GetDuration: el método GetDuration recupera la duración de la secuencia. Este método implementa el método IMediaSeeking::GetDuration.'
ms.assetid: 074eb2d0-a7a3-4bc1-82e8-2f42c6d43dac
title: Método CSourceSeeking.GetDuration (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetDuration
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3d5b961ad62d65c1f728af71e82de1373ea20b1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098773"
---
# <a name="csourceseekinggetduration-method"></a><span data-ttu-id="fe9ee-104">Método CSourceSeeking.GetDuration</span><span class="sxs-lookup"><span data-stu-id="fe9ee-104">CSourceSeeking.GetDuration method</span></span>

<span data-ttu-id="fe9ee-105">El `GetDuration` método recupera la duración de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="fe9ee-105">The `GetDuration` method retrieves the duration of the stream.</span></span> <span data-ttu-id="fe9ee-106">Este método implementa el [**método IMediaSeeking::GetDuration.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration)</span><span class="sxs-lookup"><span data-stu-id="fe9ee-106">This method implements the [**IMediaSeeking::GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe9ee-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fe9ee-107">Syntax</span></span>


```C++
HRESULT GetDuration(
   LONGLONG *pDuration
);
```



## <a name="parameters"></a><span data-ttu-id="fe9ee-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fe9ee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe9ee-109">*pDuration*</span><span class="sxs-lookup"><span data-stu-id="fe9ee-109">*pDuration*</span></span> 
</dt> <dd>

<span data-ttu-id="fe9ee-110">Puntero a una variable que recibe la duración, en unidades del formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="fe9ee-110">Pointer to a variable that receives the duration, in units of the current time format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe9ee-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fe9ee-111">Return value</span></span>

<span data-ttu-id="fe9ee-112">Devuelve uno de los **valores HRESULT** enumerados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="fe9ee-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="fe9ee-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="fe9ee-113">Return code</span></span>                                                                               | <span data-ttu-id="fe9ee-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe9ee-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="fe9ee-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fe9ee-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="fe9ee-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="fe9ee-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="fe9ee-117"><dt>**PUNTERO \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="fe9ee-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="fe9ee-118">**Valor de** puntero NULL</span><span class="sxs-lookup"><span data-stu-id="fe9ee-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fe9ee-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fe9ee-119">Remarks</span></span>

<span data-ttu-id="fe9ee-120">La variable miembro [**CSourceSeeking::m \_ rtDuration**](csourceseeking-m-rtduration.md) especifica la duración.</span><span class="sxs-lookup"><span data-stu-id="fe9ee-120">The duration is specified by the [**CSourceSeeking::m\_rtDuration**](csourceseeking-m-rtduration.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe9ee-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe9ee-121">Requirements</span></span>



| <span data-ttu-id="fe9ee-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe9ee-122">Requirement</span></span> | <span data-ttu-id="fe9ee-123">Value</span><span class="sxs-lookup"><span data-stu-id="fe9ee-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe9ee-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fe9ee-124">Header</span></span><br/>  | <dl> <span data-ttu-id="fe9ee-125"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe9ee-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fe9ee-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fe9ee-126">Library</span></span><br/> | <dl> <span data-ttu-id="fe9ee-127"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="fe9ee-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe9ee-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="fe9ee-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe9ee-129">**CSourceSeeking (clase)**</span><span class="sxs-lookup"><span data-stu-id="fe9ee-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




