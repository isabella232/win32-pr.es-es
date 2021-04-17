---
description: Identificador de subproceso del subproceso propietario.
ms.assetid: 495598db-a0c9-473b-8184-121a1939b55a
title: 'Miembro CCritSec:: m_currentOwner (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_currentOwner
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6dcb8d968f1f437087a94c5b08db12d31952d92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661231"
---
# <a name="ccritsecm_currentowner-member"></a><span data-ttu-id="7524b-103">Miembro currentOwner CCritSec:: m \_</span><span class="sxs-lookup"><span data-stu-id="7524b-103">CCritSec::m\_currentOwner member</span></span>

<span data-ttu-id="7524b-104">Identificador de subproceso del subproceso propietario.</span><span class="sxs-lookup"><span data-stu-id="7524b-104">Thread identifier of the owning thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="7524b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7524b-105">Syntax</span></span>


```C++
DWORD m_currentOwner;
```



## <a name="remarks"></a><span data-ttu-id="7524b-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7524b-106">Remarks</span></span>

<span data-ttu-id="7524b-107">Esta variable miembro solo se define en la versión de depuración de la clase base.</span><span class="sxs-lookup"><span data-stu-id="7524b-107">This member variable is defined only in the debug version of the base class.</span></span> <span data-ttu-id="7524b-108">Las [funciones de depuración de sección crítica](critical-section-debugging-functions.md) utilizan este miembro.</span><span class="sxs-lookup"><span data-stu-id="7524b-108">The [Critical Section Debugging Functions](critical-section-debugging-functions.md) use this member.</span></span>

## <a name="requirements"></a><span data-ttu-id="7524b-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7524b-109">Requirements</span></span>



| <span data-ttu-id="7524b-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="7524b-110">Requirement</span></span> | <span data-ttu-id="7524b-111">Value</span><span class="sxs-lookup"><span data-stu-id="7524b-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7524b-112">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7524b-112">Header</span></span><br/>  | <dl> <span data-ttu-id="7524b-113"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7524b-113"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7524b-114">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7524b-114">Library</span></span><br/> | <dl> <span data-ttu-id="7524b-115"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7524b-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7524b-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="7524b-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7524b-117">**Clase CCritSec**</span><span class="sxs-lookup"><span data-stu-id="7524b-117">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

 




