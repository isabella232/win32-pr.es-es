---
description: 'El método QueryPreferredFormat recupera el formato de hora preferido para la secuencia. Este método implementa el método IMediaSeeking:: QueryPreferredFormat.'
ms.assetid: 8637448f-6b53-4ec9-9671-43bc8b713668
title: Método CPosPassThru. QueryPreferredFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.QueryPreferredFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c22348a10e8b9e5f241e06252c025e2ec9593486
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680219"
---
# <a name="cpospassthruquerypreferredformat-method"></a><span data-ttu-id="f90d2-104">CPosPassThru. QueryPreferredFormat, método</span><span class="sxs-lookup"><span data-stu-id="f90d2-104">CPosPassThru.QueryPreferredFormat method</span></span>

<span data-ttu-id="f90d2-105">El `QueryPreferredFormat` método recupera el formato de hora preferido para la secuencia.</span><span class="sxs-lookup"><span data-stu-id="f90d2-105">The `QueryPreferredFormat` method retrieves the preferred time format for the stream.</span></span> <span data-ttu-id="f90d2-106">Este método implementa el método [**IMediaSeeking:: QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) .</span><span class="sxs-lookup"><span data-stu-id="f90d2-106">This method implements the [**IMediaSeeking::QueryPreferredFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-querypreferredformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f90d2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f90d2-107">Syntax</span></span>


```C++
HRESULT QueryPreferredFormat(
   GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="f90d2-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f90d2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f90d2-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="f90d2-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="f90d2-110">Puntero a una variable que recibe un GUID con formato de hora.</span><span class="sxs-lookup"><span data-stu-id="f90d2-110">Pointer to a variable that receives a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f90d2-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f90d2-111">Return value</span></span>

<span data-ttu-id="f90d2-112">Devuelve el valor **HRESULT** del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="f90d2-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="f90d2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f90d2-113">Requirements</span></span>



| <span data-ttu-id="f90d2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f90d2-114">Requirement</span></span> | <span data-ttu-id="f90d2-115">Value</span><span class="sxs-lookup"><span data-stu-id="f90d2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f90d2-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f90d2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f90d2-117"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f90d2-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f90d2-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f90d2-118">Library</span></span><br/> | <dl> <span data-ttu-id="f90d2-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f90d2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f90d2-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="f90d2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f90d2-121">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="f90d2-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="f90d2-122">**GUID de formato de hora**</span><span class="sxs-lookup"><span data-stu-id="f90d2-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




