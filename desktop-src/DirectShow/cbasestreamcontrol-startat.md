---
description: 'El método StartAt informa al pin Cuándo debe comenzar a entregar los datos. Este método implementa el método IAMStreamControl:: StartAt.'
ms.assetid: fd2943e8-8d35-4122-a99e-96d12459b335
title: Método CBaseStreamControl. StartAt (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StartAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7adcf7cbd435992333bb8ae59d5ab1674056223
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660113"
---
# <a name="cbasestreamcontrolstartat-method"></a><span data-ttu-id="42ba9-104">CBaseStreamControl. StartAt (método)</span><span class="sxs-lookup"><span data-stu-id="42ba9-104">CBaseStreamControl.StartAt method</span></span>

<span data-ttu-id="42ba9-105">El `StartAt` método informa al pin Cuándo debe comenzar a entregar los datos.</span><span class="sxs-lookup"><span data-stu-id="42ba9-105">The `StartAt` method informs the pin when to start delivering data.</span></span> <span data-ttu-id="42ba9-106">Este método implementa el método [**IAMStreamControl:: startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .</span><span class="sxs-lookup"><span data-stu-id="42ba9-106">This method implements the [**IAMStreamControl::StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="42ba9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42ba9-107">Syntax</span></span>


```C++
HRESULT StartAt(
   const REFERENCE_TIME *ptStart = NULL,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a><span data-ttu-id="42ba9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="42ba9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42ba9-109">*ptStart*</span><span class="sxs-lookup"><span data-stu-id="42ba9-109">*ptStart*</span></span> 
</dt> <dd>

<span data-ttu-id="42ba9-110">Puntero a un valor de [**\_ hora de referencia**](reference-time.md) que especifica cuándo debe comenzar a entregar los datos el código PIN.</span><span class="sxs-lookup"><span data-stu-id="42ba9-110">Pointer to a [**REFERENCE\_TIME**](reference-time.md) value that specifies when the pin should start delivering data.</span></span>

</dd> <dt>

<span data-ttu-id="42ba9-111">*dwCookie*</span><span class="sxs-lookup"><span data-stu-id="42ba9-111">*dwCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="42ba9-112">Especifica un valor que se enviará junto con la notificación de inicio.</span><span class="sxs-lookup"><span data-stu-id="42ba9-112">Specifies a value to send along with the start notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42ba9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="42ba9-113">Return value</span></span>

<span data-ttu-id="42ba9-114">Devuelve S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="42ba9-114">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="42ba9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42ba9-115">Requirements</span></span>



| <span data-ttu-id="42ba9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="42ba9-116">Requirement</span></span> | <span data-ttu-id="42ba9-117">Value</span><span class="sxs-lookup"><span data-stu-id="42ba9-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42ba9-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42ba9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="42ba9-119"><dt>Strmctl. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="42ba9-119"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="42ba9-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="42ba9-120">Library</span></span><br/> | <dl> <span data-ttu-id="42ba9-121"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="42ba9-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42ba9-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="42ba9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42ba9-123">**Clase CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="42ba9-123">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




