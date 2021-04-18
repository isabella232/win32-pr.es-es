---
description: Objeto de sección crítica que protege el estado del filtro. El método auxiliar CSource::p StateLock devuelve un puntero a esta variable miembro.
ms.assetid: faaf5fea-54bc-4856-9bca-3ed420c491e4
title: 'Miembro CSource:: m_cStateLock (Source. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_cStateLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85ff046b7e1f7a0ccfcc41f630785a3e8404e256
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670596"
---
# <a name="csourcem_cstatelock-member"></a><span data-ttu-id="3b9b5-104">Miembro cStateLock CSource:: m \_</span><span class="sxs-lookup"><span data-stu-id="3b9b5-104">CSource::m\_cStateLock member</span></span>

<span data-ttu-id="3b9b5-105">Objeto de sección crítica que protege el estado del filtro.</span><span class="sxs-lookup"><span data-stu-id="3b9b5-105">Critical section object that protects the filter state.</span></span> <span data-ttu-id="3b9b5-106">El método auxiliar [**CSource::P statelock**](csource--pstatelock.md) devuelve un puntero a esta variable miembro.</span><span class="sxs-lookup"><span data-stu-id="3b9b5-106">The [**CSource::pStateLock**](csource--pstatelock.md) helper method returns a pointer to this member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b9b5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3b9b5-107">Syntax</span></span>


```C++
CCritSec m_cStateLock;
```



## <a name="requirements"></a><span data-ttu-id="3b9b5-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b9b5-108">Requirements</span></span>



| <span data-ttu-id="3b9b5-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b9b5-109">Requirement</span></span> | <span data-ttu-id="3b9b5-110">Value</span><span class="sxs-lookup"><span data-stu-id="3b9b5-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b9b5-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3b9b5-111">Header</span></span><br/>  | <dl> <span data-ttu-id="3b9b5-112"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3b9b5-112"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3b9b5-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b9b5-113">Library</span></span><br/> | <dl> <span data-ttu-id="3b9b5-114"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="3b9b5-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b9b5-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b9b5-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b9b5-116">**Clase CSource**</span><span class="sxs-lookup"><span data-stu-id="3b9b5-116">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




