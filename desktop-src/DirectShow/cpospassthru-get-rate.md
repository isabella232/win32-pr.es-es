---
description: 'El \_ método get Rate recupera la velocidad de reproducción. Este método implementa el método de velocidad IMediaPosition:: get \_ .'
ms.assetid: 216cbcef-4874-4565-abb0-8c8bf67fe23c
title: Método CPosPassThru.get_Rate (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_Rate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 46e565f51d7c549f524f9e478b2a8326daf690a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679547"
---
# <a name="cpospassthruget_rate-method"></a><span data-ttu-id="ad9dc-104">CPosPassThru. Get \_ Rate (método)</span><span class="sxs-lookup"><span data-stu-id="ad9dc-104">CPosPassThru.get\_Rate method</span></span>

<span data-ttu-id="ad9dc-105">El `get_Rate` método recupera la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="ad9dc-105">The `get_Rate` method retrieves the playback rate.</span></span> <span data-ttu-id="ad9dc-106">Este método implementa el método de [**\_ velocidad IMediaPosition:: get**](/windows/desktop/api/Control/nf-control-imediaposition-get_rate) .</span><span class="sxs-lookup"><span data-stu-id="ad9dc-106">This method implements the [**IMediaPosition::get\_Rate**](/windows/desktop/api/Control/nf-control-imediaposition-get_rate) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad9dc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad9dc-107">Syntax</span></span>


```C++
HRESULT get_Rate(
   double *pdRate
);
```



## <a name="parameters"></a><span data-ttu-id="ad9dc-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ad9dc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad9dc-109">*pdRate*</span><span class="sxs-lookup"><span data-stu-id="ad9dc-109">*pdRate*</span></span> 
</dt> <dd>

<span data-ttu-id="ad9dc-110">Puntero a una variable que recibe la velocidad de reproducción.</span><span class="sxs-lookup"><span data-stu-id="ad9dc-110">Pointer to a variable that receives the playback rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad9dc-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad9dc-111">Return value</span></span>

<span data-ttu-id="ad9dc-112">Devuelve el valor **HRESULT** del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="ad9dc-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad9dc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad9dc-113">Requirements</span></span>



| <span data-ttu-id="ad9dc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad9dc-114">Requirement</span></span> | <span data-ttu-id="ad9dc-115">Value</span><span class="sxs-lookup"><span data-stu-id="ad9dc-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad9dc-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ad9dc-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ad9dc-117"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad9dc-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ad9dc-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ad9dc-118">Library</span></span><br/> | <dl> <span data-ttu-id="ad9dc-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ad9dc-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad9dc-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="ad9dc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad9dc-121">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="ad9dc-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




