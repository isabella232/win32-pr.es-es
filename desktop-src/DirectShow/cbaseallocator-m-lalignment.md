---
description: 'Alineación de cada búfer. La dirección de cada búfer debe ser un múltiplo par de este valor. El prefijo debe calcularse en la alineación; vea CBaseAllocator:: m \_ lPrefix.'
ms.assetid: 2b71b60a-feeb-4f09-bd56-e126eac8e150
title: 'Miembro CBaseAllocator:: m_lAlignment (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_lAlignment
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bfdfe7a83a244d5c8cd40a0a4ec747f286c5099
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660879"
---
# <a name="cbaseallocatorm_lalignment-member"></a><span data-ttu-id="20fcb-105">Miembro lAlignment CBaseAllocator:: m \_</span><span class="sxs-lookup"><span data-stu-id="20fcb-105">CBaseAllocator::m\_lAlignment member</span></span>

<span data-ttu-id="20fcb-106">Alineación de cada búfer.</span><span class="sxs-lookup"><span data-stu-id="20fcb-106">Alignment of each buffer.</span></span> <span data-ttu-id="20fcb-107">La dirección de cada búfer debe ser un múltiplo par de este valor.</span><span class="sxs-lookup"><span data-stu-id="20fcb-107">The address of each buffer must be an even multiple of this value.</span></span> <span data-ttu-id="20fcb-108">El prefijo debe calcularse en la alineación; vea [**CBaseAllocator:: m \_ lPrefix**](cbaseallocator-m-lprefix.md).</span><span class="sxs-lookup"><span data-stu-id="20fcb-108">The prefix must be calculated into the alignment; see [**CBaseAllocator::m\_lPrefix**](cbaseallocator-m-lprefix.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="20fcb-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="20fcb-109">Syntax</span></span>


```C++
long m_lAlignment;
```



## <a name="requirements"></a><span data-ttu-id="20fcb-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20fcb-110">Requirements</span></span>



| <span data-ttu-id="20fcb-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="20fcb-111">Requirement</span></span> | <span data-ttu-id="20fcb-112">Value</span><span class="sxs-lookup"><span data-stu-id="20fcb-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20fcb-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="20fcb-113">Header</span></span><br/>  | <dl> <span data-ttu-id="20fcb-114"><dt>Amfilter. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20fcb-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="20fcb-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="20fcb-115">Library</span></span><br/> | <dl> <span data-ttu-id="20fcb-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="20fcb-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20fcb-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="20fcb-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20fcb-118">**Clase CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="20fcb-118">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




