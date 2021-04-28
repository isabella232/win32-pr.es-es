---
description: 'Método CSourceSeeking.GetCapabilities: el método GetCapabilities recupera todas las funcionalidades de búsqueda de la secuencia. Este método implementa el método IMediaSeeking::GetCapabilities.'
ms.assetid: a2ff7ea2-09bd-49a7-8e1b-d6360939036e
title: Método CSourceSeeking.GetCapabilities (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f1f354381c4c99cf880c75cbbc4b13355e386030
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098783"
---
# <a name="csourceseekinggetcapabilities-method"></a><span data-ttu-id="206af-104">Método CSourceSeeking.GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="206af-104">CSourceSeeking.GetCapabilities method</span></span>

<span data-ttu-id="206af-105">El `GetCapabilities` método recupera todas las funcionalidades de búsqueda de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="206af-105">The `GetCapabilities` method retrieves all the seeking capabilities of the stream.</span></span> <span data-ttu-id="206af-106">Este método implementa el [**método IMediaSeeking::GetCapabilities.**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities)</span><span class="sxs-lookup"><span data-stu-id="206af-106">This method implements the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="206af-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="206af-107">Syntax</span></span>


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="206af-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="206af-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="206af-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="206af-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="206af-110">Puntero a una variable que recibe una combinación bit a bit de marcas [**AM \_ SEEKING SEEKING \_ \_ CAPABILITIES.**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities)</span><span class="sxs-lookup"><span data-stu-id="206af-110">Pointer to a variable that receives a bitwise combination of [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="206af-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="206af-111">Return value</span></span>

<span data-ttu-id="206af-112">Devuelve uno de los **valores HRESULT** enumerados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="206af-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="206af-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="206af-113">Return code</span></span>                                                                               | <span data-ttu-id="206af-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="206af-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="206af-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="206af-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="206af-116">Correcto</span><span class="sxs-lookup"><span data-stu-id="206af-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="206af-117"><dt>**PUNTERO \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="206af-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="206af-118">**Valor de** puntero NULL</span><span class="sxs-lookup"><span data-stu-id="206af-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="206af-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="206af-119">Remarks</span></span>

<span data-ttu-id="206af-120">La variable miembro [**CSourceSeeking::m \_ dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) especifica las funcionalidades de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="206af-120">The seeking capabilities are specified by the [**CSourceSeeking::m\_dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="206af-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="206af-121">Requirements</span></span>



| <span data-ttu-id="206af-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="206af-122">Requirement</span></span> | <span data-ttu-id="206af-123">Value</span><span class="sxs-lookup"><span data-stu-id="206af-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="206af-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="206af-124">Header</span></span><br/>  | <dl> <span data-ttu-id="206af-125"><dt>Ctlutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="206af-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="206af-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="206af-126">Library</span></span><br/> | <dl> <span data-ttu-id="206af-127"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="206af-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="206af-128">Consulte también</span><span class="sxs-lookup"><span data-stu-id="206af-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="206af-129">**CSourceSeeking (clase)**</span><span class="sxs-lookup"><span data-stu-id="206af-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




