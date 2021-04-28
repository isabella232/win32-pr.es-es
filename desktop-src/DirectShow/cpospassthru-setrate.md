---
description: 'Método CPosPassThru.SetRate: el método SetRate establece la velocidad de reproducción. Este método implementa el método IMediaSeeking::SetRate.'
ms.assetid: 1b38eb5d-38fd-408b-9f20-4f8d18158f92
title: Método CPosPassThru.SetRate (Ctlutil.h)
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
ms.openlocfilehash: bccc0d7044ccf17ac1c97e4fc5a185bdf6c7f0be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095223"
---
# <a name="cpospassthrusetrate-method"></a><span data-ttu-id="dfab9-104">Método CPosPassThru.SetRate</span><span class="sxs-lookup"><span data-stu-id="dfab9-104">CPosPassThru.SetRate method</span></span>

<span data-ttu-id="dfab9-105">El `SetRate` método establece la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="dfab9-105">The `SetRate` method sets the playback rate.</span></span> <span data-ttu-id="dfab9-106">Este método implementa el [**método IMediaSeeking::SetRate.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)</span><span class="sxs-lookup"><span data-stu-id="dfab9-106">This method implements the [**IMediaSeeking::SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfab9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dfab9-107">Syntax</span></span>


```C++
HRESULT SetRate(
   double dRate
);
```



## <a name="parameters"></a><span data-ttu-id="dfab9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dfab9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfab9-109">*dRate*</span><span class="sxs-lookup"><span data-stu-id="dfab9-109">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="dfab9-110">Velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="dfab9-110">Playback rate.</span></span> <span data-ttu-id="dfab9-111">No debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="dfab9-111">Must not be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfab9-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dfab9-112">Return value</span></span>

<span data-ttu-id="dfab9-113">Devuelve E \_ INVALIDARG si *dRate* es cero.</span><span class="sxs-lookup"><span data-stu-id="dfab9-113">Returns E\_INVALIDARG if *dRate* is zero.</span></span> <span data-ttu-id="dfab9-114">De lo contrario, devuelve **el valor HRESULT** del pin conectado.</span><span class="sxs-lookup"><span data-stu-id="dfab9-114">Otherwise, returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfab9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfab9-115">Requirements</span></span>



| <span data-ttu-id="dfab9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfab9-116">Requirement</span></span> | <span data-ttu-id="dfab9-117">Value</span><span class="sxs-lookup"><span data-stu-id="dfab9-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfab9-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dfab9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="dfab9-119"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="dfab9-119"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dfab9-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dfab9-120">Library</span></span><br/> | <dl> <span data-ttu-id="dfab9-121"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="dfab9-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfab9-122">Consulte también</span><span class="sxs-lookup"><span data-stu-id="dfab9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfab9-123">**CPosPassThru (clase)**</span><span class="sxs-lookup"><span data-stu-id="dfab9-123">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




