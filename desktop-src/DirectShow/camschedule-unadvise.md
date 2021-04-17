---
description: El método Advise quita una solicitud de notificación.
ms.assetid: b3dfda82-577e-4499-a114-1c8721e4af9e
title: Método CAMSchedule. unvise (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25dd70a46fcc2b6572500b3164b64fd0facbcbe0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660804"
---
# <a name="camscheduleunadvise-method"></a><span data-ttu-id="f30a8-103">CAMSchedule. Unadvise (método)</span><span class="sxs-lookup"><span data-stu-id="f30a8-103">CAMSchedule.Unadvise method</span></span>

<span data-ttu-id="f30a8-104">El `Unadvise` método quita una solicitud de notificación.</span><span class="sxs-lookup"><span data-stu-id="f30a8-104">The `Unadvise` method removes an advise request.</span></span>

## <a name="syntax"></a><span data-ttu-id="f30a8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f30a8-105">Syntax</span></span>


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseCookie
);
```



## <a name="parameters"></a><span data-ttu-id="f30a8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f30a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f30a8-107">*dwAdviseCookie*</span><span class="sxs-lookup"><span data-stu-id="f30a8-107">*dwAdviseCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="f30a8-108">Identificador de la solicitud de notificación, devuelto por el método [**CAMSchedule:: AddAdvisePacket**](camschedule-addadvisepacket.md) .</span><span class="sxs-lookup"><span data-stu-id="f30a8-108">Identifier of the advise request, returned by the [**CAMSchedule::AddAdvisePacket**](camschedule-addadvisepacket.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f30a8-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f30a8-109">Return value</span></span>

<span data-ttu-id="f30a8-110">Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f30a8-110">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="f30a8-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="f30a8-111">Return code</span></span>                                                                             | <span data-ttu-id="f30a8-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="f30a8-112">Description</span></span>          |
|-----------------------------------------------------------------------------------------|----------------------|
| <dl> <span data-ttu-id="f30a8-113"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="f30a8-113"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="f30a8-114">No encontrado</span><span class="sxs-lookup"><span data-stu-id="f30a8-114">Not found</span></span><br/> |
| <dl> <span data-ttu-id="f30a8-115"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="f30a8-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="f30a8-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="f30a8-116">Success</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="f30a8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f30a8-117">Requirements</span></span>



| <span data-ttu-id="f30a8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f30a8-118">Requirement</span></span> | <span data-ttu-id="f30a8-119">Value</span><span class="sxs-lookup"><span data-stu-id="f30a8-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f30a8-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f30a8-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f30a8-121"><dt>Dsschedule. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f30a8-121"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="f30a8-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f30a8-122">Library</span></span><br/> | <dl> <span data-ttu-id="f30a8-123"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f30a8-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f30a8-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="f30a8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f30a8-125">**Clase CAMSchedule**</span><span class="sxs-lookup"><span data-stu-id="f30a8-125">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




