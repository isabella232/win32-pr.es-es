---
description: 'El método IsFormatSupported determina si se admite un formato de hora especificado. Este método implementa el método IMediaSeeking:: IsFormatSupported.'
ms.assetid: dd8751d6-8439-4155-bdaf-b152a7c6cad4
title: Método CPosPassThru. IsFormatSupported (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.IsFormatSupported
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85bdbef2315bd2c9e2bc92f639a7d328f1f17ce0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681149"
---
# <a name="cpospassthruisformatsupported-method"></a><span data-ttu-id="f52a8-104">CPosPassThru. IsFormatSupported, método</span><span class="sxs-lookup"><span data-stu-id="f52a8-104">CPosPassThru.IsFormatSupported method</span></span>

<span data-ttu-id="f52a8-105">El `IsFormatSupported` método determina si se admite un formato de hora especificado.</span><span class="sxs-lookup"><span data-stu-id="f52a8-105">The `IsFormatSupported` method determines whether a specified time format is supported.</span></span> <span data-ttu-id="f52a8-106">Este método implementa el método [**IMediaSeeking:: IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) .</span><span class="sxs-lookup"><span data-stu-id="f52a8-106">This method implements the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f52a8-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f52a8-107">Syntax</span></span>


```C++
HRESULT IsFormatSupported(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="f52a8-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f52a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f52a8-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="f52a8-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="f52a8-110">Puntero a un GUID de formato de hora.</span><span class="sxs-lookup"><span data-stu-id="f52a8-110">Pointer to a time format GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f52a8-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f52a8-111">Return value</span></span>

<span data-ttu-id="f52a8-112">Devuelve el valor **HRESULT** del PIN conectado.</span><span class="sxs-lookup"><span data-stu-id="f52a8-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="f52a8-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f52a8-113">Requirements</span></span>



| <span data-ttu-id="f52a8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f52a8-114">Requirement</span></span> | <span data-ttu-id="f52a8-115">Value</span><span class="sxs-lookup"><span data-stu-id="f52a8-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f52a8-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f52a8-116">Header</span></span><br/>  | <dl> <span data-ttu-id="f52a8-117"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f52a8-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f52a8-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f52a8-118">Library</span></span><br/> | <dl> <span data-ttu-id="f52a8-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f52a8-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f52a8-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="f52a8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f52a8-121">**Clase CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="f52a8-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> <dt>

[<span data-ttu-id="f52a8-122">**GUID de formato de hora**</span><span class="sxs-lookup"><span data-stu-id="f52a8-122">**Time Format GUIDs**</span></span>](time-format-guids.md)
</dt> </dl>

 

 




