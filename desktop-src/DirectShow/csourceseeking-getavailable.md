---
description: 'Método CSourceSeeking.GetAvailable: el método GetAvailable recupera el intervalo de veces en que la búsqueda es eficaz. Este método implementa el método IMediaSeeking::GetAvailable.'
ms.assetid: 2a7b6cdb-47c3-4aeb-89ff-ea968c6a809b
title: Método CSourceSeeking.GetAvailable (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetAvailable
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f24bc667eec4f5b21c90415e4721aa8cf0a0ad4c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085243"
---
# <a name="csourceseekinggetavailable-method"></a><span data-ttu-id="26f69-104">Método CSourceSeeking.GetAvailable</span><span class="sxs-lookup"><span data-stu-id="26f69-104">CSourceSeeking.GetAvailable method</span></span>

<span data-ttu-id="26f69-105">El `GetAvailable` método recupera el intervalo de veces en que la búsqueda es eficaz.</span><span class="sxs-lookup"><span data-stu-id="26f69-105">The `GetAvailable` method retrieves the range of times in which seeking is efficient.</span></span> <span data-ttu-id="26f69-106">Este método implementa el [**método IMediaSeeking::GetAvailable.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable)</span><span class="sxs-lookup"><span data-stu-id="26f69-106">This method implements the [**IMediaSeeking::GetAvailable**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getavailable) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="26f69-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26f69-107">Syntax</span></span>


```C++
HRESULT GetAvailable(
   LONGLONG *pEarliest,
   LONGLONG *pLatest
);
```



## <a name="parameters"></a><span data-ttu-id="26f69-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="26f69-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26f69-109">*pEarliest*</span><span class="sxs-lookup"><span data-stu-id="26f69-109">*pEarliest*</span></span> 
</dt> <dd>

<span data-ttu-id="26f69-110">Puntero a una variable que recibe la primera hora para una búsqueda eficaz.</span><span class="sxs-lookup"><span data-stu-id="26f69-110">Pointer to a variable that receives the earliest time for efficient seeking.</span></span> <span data-ttu-id="26f69-111">La variable se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="26f69-111">The variable is set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="26f69-112">*pLatest*</span><span class="sxs-lookup"><span data-stu-id="26f69-112">*pLatest*</span></span> 
</dt> <dd>

<span data-ttu-id="26f69-113">Puntero a una variable que recibe la hora más reciente para una búsqueda eficaz.</span><span class="sxs-lookup"><span data-stu-id="26f69-113">Pointer to a variable that receives the latest time for efficient seeking.</span></span> <span data-ttu-id="26f69-114">La variable se establece en el valor de la variable miembro [**CSourceSeeking::m \_ rtDuration.**](csourceseeking-m-rtduration.md)</span><span class="sxs-lookup"><span data-stu-id="26f69-114">The variable is set to the value of the [**CSourceSeeking::m\_rtDuration**](csourceseeking-m-rtduration.md) member variable.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26f69-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="26f69-115">Return value</span></span>

<span data-ttu-id="26f69-116">Devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="26f69-116">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="26f69-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26f69-117">Requirements</span></span>



| <span data-ttu-id="26f69-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="26f69-118">Requirement</span></span> | <span data-ttu-id="26f69-119">Value</span><span class="sxs-lookup"><span data-stu-id="26f69-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26f69-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26f69-120">Header</span></span><br/>  | <dl> <span data-ttu-id="26f69-121"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="26f69-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="26f69-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="26f69-122">Library</span></span><br/> | <dl> <span data-ttu-id="26f69-123"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="26f69-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26f69-124">Consulte también</span><span class="sxs-lookup"><span data-stu-id="26f69-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26f69-125">**CSourceSeeking (clase)**</span><span class="sxs-lookup"><span data-stu-id="26f69-125">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




