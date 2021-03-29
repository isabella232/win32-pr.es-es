---
description: Sección crítica que protege el estado de streaming. Para obtener más información, vea flujo de datos para desarrolladores de filtros.
ms.assetid: f77c3129-ca25-47b8-8a6e-3a07169701af
title: 'Miembro CTransformFilter:: m_csReceive (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_csReceive
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 542f108cee8dbe761040ef8474ae7cec565e0b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680825"
---
# <a name="ctransformfilterm_csreceive-member"></a><span data-ttu-id="c8f69-104">Miembro csReceive CTransformFilter:: m \_</span><span class="sxs-lookup"><span data-stu-id="c8f69-104">CTransformFilter::m\_csReceive member</span></span>

<span data-ttu-id="c8f69-105">Sección crítica que protege el estado de streaming.</span><span class="sxs-lookup"><span data-stu-id="c8f69-105">Critical section that protects the streaming state.</span></span> <span data-ttu-id="c8f69-106">Para obtener más información, vea [flujo de datos para desarrolladores de filtros](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="c8f69-106">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c8f69-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8f69-107">Syntax</span></span>


```C++
CCritSec m_csReceive;
```



## <a name="requirements"></a><span data-ttu-id="c8f69-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8f69-108">Requirements</span></span>



| <span data-ttu-id="c8f69-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8f69-109">Requirement</span></span> | <span data-ttu-id="c8f69-110">Value</span><span class="sxs-lookup"><span data-stu-id="c8f69-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8f69-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8f69-111">Header</span></span><br/>  | <dl> <span data-ttu-id="c8f69-112"><dt>Transfrm. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8f69-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c8f69-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c8f69-113">Library</span></span><br/> | <dl> <span data-ttu-id="c8f69-114"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="c8f69-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8f69-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8f69-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8f69-116">**Clase CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="c8f69-116">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




