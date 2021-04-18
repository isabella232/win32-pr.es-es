---
description: Puntero a una \_ estructura de filtro AMOVIESETUP.
ms.assetid: 72db601b-78a3-484a-a27f-147ec36022ab
title: 'Miembro CFactoryTemplate:: m_pAMovieSetup_Filter (ComBase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAMovieSetup_Filter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 087612acf99a41966ccd98d3b41d2b83255a86f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671147"
---
# <a name="cfactorytemplatem_pamoviesetup_filter-member"></a><span data-ttu-id="fd719-103">Miembro de filtro CFactoryTemplate:: m \_ pAMovieSetup \_</span><span class="sxs-lookup"><span data-stu-id="fd719-103">CFactoryTemplate::m\_pAMovieSetup\_Filter member</span></span>

<span data-ttu-id="fd719-104">Puntero a una estructura de [**\_ filtro AMOVIESETUP**](amoviesetup-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="fd719-104">Pointer to an [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd719-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd719-105">Syntax</span></span>


```C++
const AMOVIESETUP_FILTER *m_pAMovieSetup_Filter;
```



## <a name="remarks"></a><span data-ttu-id="fd719-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd719-106">Remarks</span></span>

<span data-ttu-id="fd719-107">Use esta estructura para realizar un registro automático del filtro.</span><span class="sxs-lookup"><span data-stu-id="fd719-107">Use this structure to make a filter self-registering.</span></span> <span data-ttu-id="fd719-108">Si el componente no es un filtro, esta variable miembro puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="fd719-108">If your component is not a filter, this member variable can be **NULL**.</span></span> <span data-ttu-id="fd719-109">Para obtener más información, consulte Cómo registrar filtros de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="fd719-109">For more information, see How to Register DirectShow Filters.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd719-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd719-110">Requirements</span></span>



| <span data-ttu-id="fd719-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd719-111">Requirement</span></span> | <span data-ttu-id="fd719-112">Value</span><span class="sxs-lookup"><span data-stu-id="fd719-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd719-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd719-113">Header</span></span><br/>  | <dl> <span data-ttu-id="fd719-114"><dt>ComBase. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fd719-114"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fd719-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fd719-115">Library</span></span><br/> | <dl> <span data-ttu-id="fd719-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="fd719-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd719-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd719-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd719-118">**Clase CFactoryTemplate**</span><span class="sxs-lookup"><span data-stu-id="fd719-118">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




