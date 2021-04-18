---
description: 'El método GetTimeFormat recupera el formato de hora actual. Este método implementa el método IMediaSeeking:: GetTimeFormat.'
ms.assetid: 445c1873-da6f-42be-a4cf-0c475c5f0723
title: Método CPosPassThru. GetTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7db1b46cfe2ac06dc43b52009043ae32676f154
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661298"
---
# <a name="cpospassthrugettimeformat-method"></a><span data-ttu-id="d64a3-104">CPosPassThru. GetTimeFormat, método</span><span class="sxs-lookup"><span data-stu-id="d64a3-104">CPosPassThru.GetTimeFormat method</span></span>

<span data-ttu-id="d64a3-105">El `GetTimeFormat` método recupera el formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="d64a3-105">The `GetTimeFormat` method retrieves the current time format.</span></span> <span data-ttu-id="d64a3-106">Este método implementa el método [**IMediaSeeking:: GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="d64a3-106">This method implements the [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d64a3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d64a3-107">Syntax</span></span>


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="d64a3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d64a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d64a3-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="d64a3-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="d64a3-110">Puntero a una variable que recibe un GUID con formato de hora.</span><span class="sxs-lookup"><span data-stu-id="d64a3-110">Pointer to a variable that receives a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d64a3-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d64a3-111">Return value</span></span>

<span data-ttu-id="d64a3-112">Devuelve el valor **HRESULT** del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="d64a3-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="d64a3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d64a3-113">Requirements</span></span>



| <span data-ttu-id="d64a3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d64a3-114">Requirement</span></span> | <span data-ttu-id="d64a3-115">Value</span><span class="sxs-lookup"><span data-stu-id="d64a3-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d64a3-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d64a3-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d64a3-117"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d64a3-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d64a3-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d64a3-118">Library</span></span><br/> | <dl> <span data-ttu-id="d64a3-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="d64a3-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d64a3-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="d64a3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d64a3-121">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="d64a3-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="d64a3-122">**GUID de formato de hora**</span><span class="sxs-lookup"><span data-stu-id="d64a3-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




