---
description: 'Destructor CCritSec.~CCritSec: método Destructor.'
ms.assetid: cade850c-391c-41dc-adfe-56de8b2bbfff
title: Destructor CCritSec.~CCritSec (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.~CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f282bfe6ea6bca8cb8553572c18cfbc85db6c77
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095813"
---
# <a name="ccritsecccritsec-destructor"></a><span data-ttu-id="bdd97-103">Destructor CCritSec.~CCritSec</span><span class="sxs-lookup"><span data-stu-id="bdd97-103">CCritSec.~CCritSec destructor</span></span>

<span data-ttu-id="bdd97-104">Método destructor.</span><span class="sxs-lookup"><span data-stu-id="bdd97-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdd97-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bdd97-105">Syntax</span></span>


```C++
~CCritSec();
```



## <a name="remarks"></a><span data-ttu-id="bdd97-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bdd97-106">Remarks</span></span>

<span data-ttu-id="bdd97-107">Este método llama a [**la función DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) para eliminar la sección crítica.</span><span class="sxs-lookup"><span data-stu-id="bdd97-107">This method calls the [**DeleteCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-deletecriticalsection) function to delete the critical section.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdd97-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdd97-108">Requirements</span></span>



| <span data-ttu-id="bdd97-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdd97-109">Requirement</span></span> | <span data-ttu-id="bdd97-110">Value</span><span class="sxs-lookup"><span data-stu-id="bdd97-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdd97-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bdd97-111">Header</span></span><br/>  | <dl> <span data-ttu-id="bdd97-112"><dt>Wxutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="bdd97-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="bdd97-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bdd97-113">Library</span></span><br/> | <dl> <span data-ttu-id="bdd97-114"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="bdd97-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdd97-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bdd97-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdd97-116">**CCritSec (clase)**</span><span class="sxs-lookup"><span data-stu-id="bdd97-116">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

