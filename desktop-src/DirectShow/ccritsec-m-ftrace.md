---
description: Valor booleano que especifica si se va a realizar el seguimiento de este bloqueo.
ms.assetid: 23417410-cfdc-426e-a662-7d6580b43a28
title: 'Miembro CCritSec:: m_fTrace (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_fTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 691e078bb3b502704aed585ba020d49b2bd99af1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661239"
---
# <a name="ccritsecm_ftrace-member"></a><span data-ttu-id="f74a5-103">Miembro fTrace CCritSec:: m \_</span><span class="sxs-lookup"><span data-stu-id="f74a5-103">CCritSec::m\_fTrace member</span></span>

<span data-ttu-id="f74a5-104">Valor booleano que especifica si se va a realizar el seguimiento de este bloqueo.</span><span class="sxs-lookup"><span data-stu-id="f74a5-104">Boolean value that specifies whether to trace this lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="f74a5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f74a5-105">Syntax</span></span>


```C++
BOOL m_fTrace;
```



## <a name="remarks"></a><span data-ttu-id="f74a5-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f74a5-106">Remarks</span></span>

<span data-ttu-id="f74a5-107">Esta variable miembro solo se define en la versión de depuración de la clase base.</span><span class="sxs-lookup"><span data-stu-id="f74a5-107">This member variable is defined only in the debug version of the base class.</span></span> <span data-ttu-id="f74a5-108">Si el valor es **true**, se escribe un seguimiento del estado de bloqueo en el registro de depuración.</span><span class="sxs-lookup"><span data-stu-id="f74a5-108">If the value is **TRUE**, a trace of the lock state is written to the debug log.</span></span> <span data-ttu-id="f74a5-109">(El registro de depuración de las secciones críticas debe estar activo). Para obtener más información, vea [**DbgLockTrace**](dbglocktrace.md).</span><span class="sxs-lookup"><span data-stu-id="f74a5-109">(Debug logging for critical sections must be active.) For more information, see [**DbgLockTrace**](dbglocktrace.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f74a5-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f74a5-110">Requirements</span></span>



| <span data-ttu-id="f74a5-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f74a5-111">Requirement</span></span> | <span data-ttu-id="f74a5-112">Value</span><span class="sxs-lookup"><span data-stu-id="f74a5-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f74a5-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f74a5-113">Header</span></span><br/>  | <dl> <span data-ttu-id="f74a5-114"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f74a5-114"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f74a5-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f74a5-115">Library</span></span><br/> | <dl> <span data-ttu-id="f74a5-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="f74a5-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f74a5-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="f74a5-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f74a5-118">**Clase CCritSec**</span><span class="sxs-lookup"><span data-stu-id="f74a5-118">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

 




