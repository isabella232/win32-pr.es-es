---
description: El método GetFreeCount recupera el número de muestras de medios que no están en uso.
ms.assetid: f4ce4cca-0168-42db-9fe7-858862f033a8
title: Método CBaseAllocator. GetFreeCount (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetFreeCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a0538229053b5d47ca1bdc8f30b38a0937e36cb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671465"
---
# <a name="cbaseallocatorgetfreecount-method"></a><span data-ttu-id="a3cb4-103">CBaseAllocator. GetFreeCount, método</span><span class="sxs-lookup"><span data-stu-id="a3cb4-103">CBaseAllocator.GetFreeCount method</span></span>

<span data-ttu-id="a3cb4-104">El `GetFreeCount` método recupera el número de muestras de medios que no están en uso.</span><span class="sxs-lookup"><span data-stu-id="a3cb4-104">The `GetFreeCount` method retrieves the number of media samples that are not in use.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3cb4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3cb4-105">Syntax</span></span>


```C++
HRESULT GetFreeCount(
   LONG *plBuffersFree
);
```



## <a name="parameters"></a><span data-ttu-id="a3cb4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a3cb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3cb4-107">*plBuffersFree*</span><span class="sxs-lookup"><span data-stu-id="a3cb4-107">*plBuffersFree*</span></span> 
</dt> <dd>

<span data-ttu-id="a3cb4-108">Dirección de una variable que recibe el número de muestras que no están en uso.</span><span class="sxs-lookup"><span data-stu-id="a3cb4-108">Address of a variable that receives the number of samples that are not in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3cb4-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a3cb4-109">Return value</span></span>

<span data-ttu-id="a3cb4-110">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="a3cb4-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3cb4-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3cb4-111">Remarks</span></span>

<span data-ttu-id="a3cb4-112">Este método implementa el método [**IMemAllocatorCallbackTemp:: GetFreeCount**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-getfreecount) .</span><span class="sxs-lookup"><span data-stu-id="a3cb4-112">This method implements the [**IMemAllocatorCallbackTemp::GetFreeCount**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-getfreecount) method.</span></span> <span data-ttu-id="a3cb4-113">El asignador no expone la interfaz IMemAllocatorCallbackTemp a menos que la marca *fEnableReleaseCallback* esté establecida en **true** en el constructor CBaseAllocator.</span><span class="sxs-lookup"><span data-stu-id="a3cb4-113">The allocator does not expose the IMemAllocatorCallbackTemp interface unless the *fEnableReleaseCallback* flag is set to **TRUE** in the CBaseAllocator constructor.</span></span>

## <a name="requirements"></a><span data-ttu-id="a3cb4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3cb4-114">Requirements</span></span>



| <span data-ttu-id="a3cb4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3cb4-115">Requirement</span></span> | <span data-ttu-id="a3cb4-116">Value</span><span class="sxs-lookup"><span data-stu-id="a3cb4-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3cb4-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3cb4-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a3cb4-118"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a3cb4-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a3cb4-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a3cb4-119">Library</span></span><br/> | <dl> <span data-ttu-id="a3cb4-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a3cb4-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3cb4-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3cb4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3cb4-122">**Clase CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="a3cb4-122">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




