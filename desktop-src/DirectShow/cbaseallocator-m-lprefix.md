---
description: Prefijo de cada búfer, en bytes.
ms.assetid: 471b73bf-f959-41aa-84ba-324a2738dd0e
title: 'Miembro CBaseAllocator:: m_lPrefix (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lPrefix
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fc52db44dcdfa050cf8bc7faf57cb7094d8cac91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660325"
---
# <a name="cbaseallocatorm_lprefix-member"></a><span data-ttu-id="cabf5-103">Miembro lPrefix CBaseAllocator:: m \_</span><span class="sxs-lookup"><span data-stu-id="cabf5-103">CBaseAllocator::m\_lPrefix member</span></span>

<span data-ttu-id="cabf5-104">Prefijo de cada búfer, en bytes.</span><span class="sxs-lookup"><span data-stu-id="cabf5-104">Prefix of each buffer, in bytes.</span></span> <span data-ttu-id="cabf5-105">Si el valor es distinto de cero, cada puntero de búfer devuelto por el método [**CBaseAllocator:: getBuffer**](cbaseallocator-getbuffer.md) va precedido de un bloque de bytes de tamaño *m \_ lPrefix*.</span><span class="sxs-lookup"><span data-stu-id="cabf5-105">If the value is non-zero, each buffer pointer returned by the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method is preceded by a block of bytes of size *m\_lPrefix*.</span></span> <span data-ttu-id="cabf5-106">Este bloque de memoria se denomina *prefijo*.</span><span class="sxs-lookup"><span data-stu-id="cabf5-106">This memory block is called the *prefix*.</span></span> <span data-ttu-id="cabf5-107">La variable miembro [**CBaseAllocator:: m \_ Lsize**](cbaseallocator-m-lsize.md) no incluye el valor de prefijo.</span><span class="sxs-lookup"><span data-stu-id="cabf5-107">The [**CBaseAllocator::m\_lSize**](cbaseallocator-m-lsize.md) member variable does not include the prefix value.</span></span>

## <a name="syntax"></a><span data-ttu-id="cabf5-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cabf5-108">Syntax</span></span>


```C++
long m_lPrefix;
```



## <a name="requirements"></a><span data-ttu-id="cabf5-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cabf5-109">Requirements</span></span>



| <span data-ttu-id="cabf5-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="cabf5-110">Requirement</span></span> | <span data-ttu-id="cabf5-111">Value</span><span class="sxs-lookup"><span data-stu-id="cabf5-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cabf5-112">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cabf5-112">Header</span></span><br/>  | <dl> <span data-ttu-id="cabf5-113"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cabf5-113"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cabf5-114">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cabf5-114">Library</span></span><br/> | <dl> <span data-ttu-id="cabf5-115"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="cabf5-115"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cabf5-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="cabf5-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cabf5-117">**Clase CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="cabf5-117">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




