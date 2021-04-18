---
description: 'El método SetRate establece la velocidad de reproducción. Este método implementa el método IMediaSeeking:: SetRate.'
ms.assetid: 1b38eb5d-38fd-408b-9f20-4f8d18158f92
title: Método CPosPassThru. SetRate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.SetRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ada5c8bc8d265b33e1d4b243bdfd0cf8bf03a7dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680283"
---
# <a name="cpospassthrusetrate-method"></a><span data-ttu-id="39d4c-104">CPosPassThru. SetRate, método</span><span class="sxs-lookup"><span data-stu-id="39d4c-104">CPosPassThru.SetRate method</span></span>

<span data-ttu-id="39d4c-105">El `SetRate` método establece la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="39d4c-105">The `SetRate` method sets the playback rate.</span></span> <span data-ttu-id="39d4c-106">Este método implementa el método [**IMediaSeeking:: SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) .</span><span class="sxs-lookup"><span data-stu-id="39d4c-106">This method implements the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="39d4c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39d4c-107">Syntax</span></span>


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="39d4c-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39d4c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39d4c-109">*dRate*</span><span class="sxs-lookup"><span data-stu-id="39d4c-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="39d4c-110">Velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="39d4c-110">Playback rate.</span></span> <span data-ttu-id="39d4c-111">No debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="39d4c-111">Must not be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39d4c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39d4c-112">Return value</span></span>

<span data-ttu-id="39d4c-113">Devuelve E \_ INVALIDARG si *dRate* es cero.</span><span class="sxs-lookup"><span data-stu-id="39d4c-113">Returns E\_INVALIDARG if *dRate* is zero.</span></span> <span data-ttu-id="39d4c-114">De lo contrario, devuelve el valor **HRESULT** del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="39d4c-114">Otherwise, returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="39d4c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39d4c-115">Requirements</span></span>



| <span data-ttu-id="39d4c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="39d4c-116">Requirement</span></span> | <span data-ttu-id="39d4c-117">Value</span><span class="sxs-lookup"><span data-stu-id="39d4c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39d4c-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="39d4c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="39d4c-119"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39d4c-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="39d4c-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="39d4c-120">Library</span></span><br/> | <dl> <span data-ttu-id="39d4c-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="39d4c-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39d4c-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="39d4c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39d4c-123">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="39d4c-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




