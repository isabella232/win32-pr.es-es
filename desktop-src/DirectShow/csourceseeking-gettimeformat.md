---
description: 'Método CSourceSeeking.GetTimeFormat: el método GetTimeFormat recupera el formato de hora actual. Este método implementa el método IMediaSeeking::GetTimeFormat.'
ms.assetid: c90804f7-9a0a-423c-8b26-87abf15eddc5
title: Método CSourceSeeking.GetTimeFormat (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetTimeFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a56f9a490699d68d7a043e9385ad458562058f5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085223"
---
# <a name="csourceseekinggettimeformat-method"></a><span data-ttu-id="888cf-104">Método CSourceSeeking.GetTimeFormat</span><span class="sxs-lookup"><span data-stu-id="888cf-104">CSourceSeeking.GetTimeFormat method</span></span>

<span data-ttu-id="888cf-105">El `GetTimeFormat` método recupera el formato de hora actual.</span><span class="sxs-lookup"><span data-stu-id="888cf-105">The `GetTimeFormat` method retrieves the current time format.</span></span> <span data-ttu-id="888cf-106">Este método implementa el [**método IMediaSeeking::GetTimeFormat.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)</span><span class="sxs-lookup"><span data-stu-id="888cf-106">This method implements the [**IMediaSeeking::GetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="888cf-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="888cf-107">Syntax</span></span>


```C++
HRESULT GetTimeFormat(
   const GUID *pFormat
);
```



## <a name="parameters"></a><span data-ttu-id="888cf-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="888cf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="888cf-109">*pFormat*</span><span class="sxs-lookup"><span data-stu-id="888cf-109">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="888cf-110">Puntero a una variable que recibe un GUID de formato de hora.</span><span class="sxs-lookup"><span data-stu-id="888cf-110">Pointer to a variable that receives a time format GUID.</span></span> <span data-ttu-id="888cf-111">Consulte [**GUID de formato de hora.**](time-format-guids.md)</span><span class="sxs-lookup"><span data-stu-id="888cf-111">See [**Time Format GUIDs**](time-format-guids.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="888cf-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="888cf-112">Return value</span></span>

<span data-ttu-id="888cf-113">Devuelve uno de los **valores HRESULT** enumerados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="888cf-113">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="888cf-114">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="888cf-114">Return code</span></span>                                                                               | <span data-ttu-id="888cf-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="888cf-115">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="888cf-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="888cf-116"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="888cf-117">Correcto</span><span class="sxs-lookup"><span data-stu-id="888cf-117">Success</span></span><br/>                |
| <dl> <span data-ttu-id="888cf-118"><dt>**PUNTERO \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="888cf-118"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="888cf-119">**Valor de** puntero NULL</span><span class="sxs-lookup"><span data-stu-id="888cf-119">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="888cf-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="888cf-120">Remarks</span></span>

<span data-ttu-id="888cf-121">El único formato de hora admitido por la clase base es TIME \_ FORMAT \_ MEDIA TIME \_ (unidades de 100 nanosegundos).</span><span class="sxs-lookup"><span data-stu-id="888cf-121">The only time format supported by the base class is TIME\_FORMAT\_MEDIA\_TIME (100-nanosecond units).</span></span>

## <a name="requirements"></a><span data-ttu-id="888cf-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="888cf-122">Requirements</span></span>



| <span data-ttu-id="888cf-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="888cf-123">Requirement</span></span> | <span data-ttu-id="888cf-124">Value</span><span class="sxs-lookup"><span data-stu-id="888cf-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="888cf-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="888cf-125">Header</span></span><br/>  | <dl> <span data-ttu-id="888cf-126"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="888cf-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="888cf-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="888cf-127">Library</span></span><br/> | <dl> <span data-ttu-id="888cf-128"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="888cf-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="888cf-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="888cf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="888cf-130">**CSourceSeeking (clase)**</span><span class="sxs-lookup"><span data-stu-id="888cf-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




