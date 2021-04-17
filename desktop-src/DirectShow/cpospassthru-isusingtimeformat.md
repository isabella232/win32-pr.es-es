---
description: 'El método IsUsingTimeFormat determina si un formato de hora especificado es el formato que se está usando actualmente. Este método implementa el método IMediaSeeking:: IsUsingTimeFormat.'
ms.assetid: e377bcf0-0518-42b2-8975-e4c345e3fed4
title: Método CPosPassThru. IsUsingTimeFormat (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.IsUsingTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 012a9487f5840117edb9f8bc0afa1d9388b4bce0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661294"
---
# <a name="cpospassthruisusingtimeformat-method"></a><span data-ttu-id="65df6-104">CPosPassThru. IsUsingTimeFormat, método</span><span class="sxs-lookup"><span data-stu-id="65df6-104">CPosPassThru.IsUsingTimeFormat method</span></span>

<span data-ttu-id="65df6-105">El `IsUsingTimeFormat` método determina si un formato de hora especificado es el formato que se está usando actualmente.</span><span class="sxs-lookup"><span data-stu-id="65df6-105">The `IsUsingTimeFormat` method determines whether a specified time format is the format currently in use.</span></span> <span data-ttu-id="65df6-106">Este método implementa el método [**IMediaSeeking:: IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat) .</span><span class="sxs-lookup"><span data-stu-id="65df6-106">This method implements the [**IMediaSeeking::IsUsingTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="65df6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="65df6-107">Syntax</span></span>


```C++
HRESULT IsUsingTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="65df6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="65df6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65df6-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="65df6-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="65df6-110">Puntero a un GUID de formato de hora.</span><span class="sxs-lookup"><span data-stu-id="65df6-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65df6-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="65df6-111">Return value</span></span>

<span data-ttu-id="65df6-112">Devuelve el valor **HRESULT** del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="65df6-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="65df6-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65df6-113">Requirements</span></span>



| <span data-ttu-id="65df6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="65df6-114">Requirement</span></span> | <span data-ttu-id="65df6-115">Value</span><span class="sxs-lookup"><span data-stu-id="65df6-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65df6-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="65df6-116">Header</span></span><br/>  | <dl> <span data-ttu-id="65df6-117"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65df6-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="65df6-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="65df6-118">Library</span></span><br/> | <dl> <span data-ttu-id="65df6-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="65df6-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65df6-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="65df6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65df6-121">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="65df6-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="65df6-122">**GUID de formato de hora**</span><span class="sxs-lookup"><span data-stu-id="65df6-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




