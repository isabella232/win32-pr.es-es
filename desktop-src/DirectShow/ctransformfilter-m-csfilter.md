---
description: Sección crítica que protege el estado del filtro. Para obtener más información, vea flujo de datos para desarrolladores de filtros.
ms.assetid: 75b9c8b0-e911-41fd-8d07-b854dbe25551
title: 'Miembro CTransformFilter:: m_csFilter (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_csFilter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 991b07aa654ce42a651f4fa169e757d8380fdc8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661029"
---
# <a name="ctransformfilterm_csfilter-member"></a><span data-ttu-id="a6ff9-104">Miembro csFilter CTransformFilter:: m \_</span><span class="sxs-lookup"><span data-stu-id="a6ff9-104">CTransformFilter::m\_csFilter member</span></span>

<span data-ttu-id="a6ff9-105">Sección crítica que protege el estado del filtro.</span><span class="sxs-lookup"><span data-stu-id="a6ff9-105">Critical section that protects the filter state.</span></span> <span data-ttu-id="a6ff9-106">Para obtener más información, vea [flujo de datos para desarrolladores de filtros](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="a6ff9-106">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a6ff9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a6ff9-107">Syntax</span></span>


```C++
CCritSec m_csFilter;
```



## <a name="requirements"></a><span data-ttu-id="a6ff9-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6ff9-108">Requirements</span></span>



| <span data-ttu-id="a6ff9-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6ff9-109">Requirement</span></span> | <span data-ttu-id="a6ff9-110">Value</span><span class="sxs-lookup"><span data-stu-id="a6ff9-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6ff9-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6ff9-111">Header</span></span><br/>  | <dl> <span data-ttu-id="a6ff9-112"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a6ff9-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a6ff9-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a6ff9-113">Library</span></span><br/> | <dl> <span data-ttu-id="a6ff9-114"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a6ff9-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6ff9-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6ff9-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6ff9-116">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="a6ff9-116">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




