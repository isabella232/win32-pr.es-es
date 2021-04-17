---
description: 'El método SetSyncPoint especifica si el principio de este ejemplo es un punto de sincronización. Este método implementa el método IMediaSample:: SetSyncPoint.'
ms.assetid: 48fc5145-7cce-4e76-860d-45a0d5b43b67
title: Método CMediaSample. SetSyncPoint (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetSyncPoint
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 679be6a313329a15c83bee4473e5a944aa3532b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670455"
---
# <a name="cmediasamplesetsyncpoint-method"></a><span data-ttu-id="8c052-104">CMediaSample. SetSyncPoint, método</span><span class="sxs-lookup"><span data-stu-id="8c052-104">CMediaSample.SetSyncPoint method</span></span>

<span data-ttu-id="8c052-105">El `SetSyncPoint` método especifica si el principio de este ejemplo es un punto de sincronización.</span><span class="sxs-lookup"><span data-stu-id="8c052-105">The `SetSyncPoint` method specifies whether the beginning of this sample is a synchronization point.</span></span> <span data-ttu-id="8c052-106">Este método implementa el método [**IMediaSample:: SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) .</span><span class="sxs-lookup"><span data-stu-id="8c052-106">This method implements the [**IMediaSample::SetSyncPoint**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setsyncpoint) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c052-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8c052-107">Syntax</span></span>


```C++
HRESULT SetSyncPoint(
   BOOL bIsSyncPoint
);
```



## <a name="parameters"></a><span data-ttu-id="8c052-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8c052-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c052-109">*bIsSyncPoint*</span><span class="sxs-lookup"><span data-stu-id="8c052-109">*bIsSyncPoint*</span></span> 
</dt> <dd>

<span data-ttu-id="8c052-110">Valor booleano que especifica si se trata de un punto de sincronización.</span><span class="sxs-lookup"><span data-stu-id="8c052-110">Boolean value that specifies whether this is a synchronization point.</span></span> <span data-ttu-id="8c052-111">Si es **true**, se trata de un punto de sincronización.</span><span class="sxs-lookup"><span data-stu-id="8c052-111">If **TRUE**, this is a synchronization point.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c052-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8c052-112">Return value</span></span>

<span data-ttu-id="8c052-113">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="8c052-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c052-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8c052-114">Remarks</span></span>

<span data-ttu-id="8c052-115">Este método actualiza la variable miembro [**CMediaSample:: m \_ dwFlags**](cmediasample-m-dwflags.md) , que especifica la propiedad de punto de sincronización.</span><span class="sxs-lookup"><span data-stu-id="8c052-115">This method updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies the synchronization-point property.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c052-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c052-116">Requirements</span></span>



| <span data-ttu-id="8c052-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c052-117">Requirement</span></span> | <span data-ttu-id="8c052-118">Value</span><span class="sxs-lookup"><span data-stu-id="8c052-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c052-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c052-119">Header</span></span><br/>  | <dl> <span data-ttu-id="8c052-120"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8c052-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8c052-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8c052-121">Library</span></span><br/> | <dl> <span data-ttu-id="8c052-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="8c052-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c052-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="8c052-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c052-124">**Clase CMediaSample**</span><span class="sxs-lookup"><span data-stu-id="8c052-124">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




