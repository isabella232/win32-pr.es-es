---
description: 'Método CSource.FindPin: el método FindPin recupera el pin con el identificador especificado. Este método implementa el método IBaseFilter::FindPin.'
ms.assetid: ad593dbf-ca56-4409-ac6e-1b88908c8cee
title: Método CSource.FindPin (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.FindPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: daa1e2404e7c6fbf1d879d71374298103bdc621f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098863"
---
# <a name="csourcefindpin-method"></a><span data-ttu-id="ee7fe-104">Método CSource.FindPin</span><span class="sxs-lookup"><span data-stu-id="ee7fe-104">CSource.FindPin method</span></span>

<span data-ttu-id="ee7fe-105">El `FindPin` método recupera el pin con el identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="ee7fe-105">The `FindPin` method retrieves the pin with the specified identifier.</span></span> <span data-ttu-id="ee7fe-106">Este método implementa el [**método IBaseFilter::FindPin.**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin)</span><span class="sxs-lookup"><span data-stu-id="ee7fe-106">This method implements the [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee7fe-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee7fe-107">Syntax</span></span>


```C++
HRESULT FindPin(
   LPCWSTR Id,
   IPin    **ppPin
);
```



## <a name="parameters"></a><span data-ttu-id="ee7fe-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee7fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee7fe-109">*Id*</span><span class="sxs-lookup"><span data-stu-id="ee7fe-109">*Id*</span></span> 
</dt> <dd>

<span data-ttu-id="ee7fe-110">Puntero a una cadena terminada en NULL que identifica el pin.</span><span class="sxs-lookup"><span data-stu-id="ee7fe-110">Pointer to a null-terminated string that identifies the pin.</span></span>

</dd> <dt>

<span data-ttu-id="ee7fe-111">*ppPin*</span><span class="sxs-lookup"><span data-stu-id="ee7fe-111">*ppPin*</span></span> 
</dt> <dd>

<span data-ttu-id="ee7fe-112">Recibe un puntero a la interfaz [**IPin del**](/windows/desktop/api/Strmif/nn-strmif-ipin) pin.</span><span class="sxs-lookup"><span data-stu-id="ee7fe-112">Receives a pointer to the pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span> <span data-ttu-id="ee7fe-113">Si se produce un error en el \* *método, ppPin* se establece en **NULL.**</span><span class="sxs-lookup"><span data-stu-id="ee7fe-113">If the method fails, \**ppPin* is set to **NULL**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee7fe-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee7fe-114">Return value</span></span>

<span data-ttu-id="ee7fe-115">Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="ee7fe-115">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="ee7fe-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="ee7fe-116">Return code</span></span>                                                                                       | <span data-ttu-id="ee7fe-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee7fe-117">Description</span></span>                                           |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="ee7fe-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ee7fe-118"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="ee7fe-119">Correcto.</span><span class="sxs-lookup"><span data-stu-id="ee7fe-119">Success.</span></span><br/>                                   |
| <dl> <span data-ttu-id="ee7fe-120"><dt>**PUNTERO \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="ee7fe-120"><dt>**E\_POINTER**</dt></span></span> </dl>         | <span data-ttu-id="ee7fe-121">**Argumento de** puntero NULL.</span><span class="sxs-lookup"><span data-stu-id="ee7fe-121">**NULL** pointer argument.</span></span><br/>                 |
| <dl> <span data-ttu-id="ee7fe-122"><dt>**VFW \_ E \_ NO \_ ENCONTRADO**</dt></span><span class="sxs-lookup"><span data-stu-id="ee7fe-122"><dt>**VFW\_E\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="ee7fe-123">No se encontró un pin con este identificador.</span><span class="sxs-lookup"><span data-stu-id="ee7fe-123">Could not find a pin with this identifier.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ee7fe-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ee7fe-124">Remarks</span></span>

<span data-ttu-id="ee7fe-125">El primer pin siempre se denomina "1"; el segundo pin se denomina "2"; y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="ee7fe-125">The first pin is always named "1"; the second pin is named "2"; and so forth.</span></span> <span data-ttu-id="ee7fe-126">Para obtener más información, [**vea CSourceStream::QueryId**](csourcestream-queryid.md).</span><span class="sxs-lookup"><span data-stu-id="ee7fe-126">For more information, see [**CSourceStream::QueryId**](csourcestream-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee7fe-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee7fe-127">Requirements</span></span>



| <span data-ttu-id="ee7fe-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee7fe-128">Requirement</span></span> | <span data-ttu-id="ee7fe-129">Value</span><span class="sxs-lookup"><span data-stu-id="ee7fe-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee7fe-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ee7fe-130">Header</span></span><br/>  | <dl> <span data-ttu-id="ee7fe-131"><dt>Source.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee7fe-131"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ee7fe-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ee7fe-132">Library</span></span><br/> | <dl> <span data-ttu-id="ee7fe-133"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ee7fe-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee7fe-134">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ee7fe-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee7fe-135">**CSource (clase)**</span><span class="sxs-lookup"><span data-stu-id="ee7fe-135">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




