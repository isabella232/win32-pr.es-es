---
description: Estado de bloqueo.
ms.assetid: 55afd314-efd3-47bf-80e3-e17c1332a4cf
title: 'Miembro CDynamicOutputPin:: m_BlockState (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_BlockState
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f02a59854b381db5e7b13a85ccca0754cc38f51d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661321"
---
# <a name="cdynamicoutputpinm_blockstate-member"></a><span data-ttu-id="b71f6-103">Miembro BlockState CDynamicOutputPin:: m \_</span><span class="sxs-lookup"><span data-stu-id="b71f6-103">CDynamicOutputPin::m\_BlockState member</span></span>

<span data-ttu-id="b71f6-104">Estado de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="b71f6-104">Blocking state.</span></span>

## <a name="syntax"></a><span data-ttu-id="b71f6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b71f6-105">Syntax</span></span>


```C++
BLOCK_STATE m_BlockState;
```



## <a name="remarks"></a><span data-ttu-id="b71f6-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b71f6-106">Remarks</span></span>

<span data-ttu-id="b71f6-107">Se definen los siguientes Estados:</span><span class="sxs-lookup"><span data-stu-id="b71f6-107">The following states are defined:</span></span>

-   <span data-ttu-id="b71f6-108">NO \_ bloqueado</span><span class="sxs-lookup"><span data-stu-id="b71f6-108">NOT\_BLOCKED</span></span>
-   <span data-ttu-id="b71f6-109">PENDING</span><span class="sxs-lookup"><span data-stu-id="b71f6-109">PENDING</span></span>
-   <span data-ttu-id="b71f6-110">BLOQUEO</span><span class="sxs-lookup"><span data-stu-id="b71f6-110">BLOCKED</span></span>

<span data-ttu-id="b71f6-111">Antes de tener acceso a esta variable, conserve la sección crítica [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="b71f6-111">Before accessing this variable, hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="b71f6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b71f6-112">Requirements</span></span>



| <span data-ttu-id="b71f6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b71f6-113">Requirement</span></span> | <span data-ttu-id="b71f6-114">Value</span><span class="sxs-lookup"><span data-stu-id="b71f6-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b71f6-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b71f6-115">Header</span></span><br/>  | <dl> <span data-ttu-id="b71f6-116"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b71f6-116"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b71f6-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b71f6-117">Library</span></span><br/> | <dl> <span data-ttu-id="b71f6-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b71f6-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b71f6-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="b71f6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b71f6-120">**Clase CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="b71f6-120">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




