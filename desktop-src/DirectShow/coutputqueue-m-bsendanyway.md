---
description: 'Marca para invalidar el procesamiento por lotes. Al establecer esta marca en TRUE, se invalida la marca COutputQueue:: m \_ bBatchExact y se entregan todos los ejemplos pendientes.'
ms.assetid: 95ea6973-65c0-40c9-be22-c2a20a60b459
title: 'Miembro COutputQueue:: m_bSendAnyway (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSendAnyway
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57019ee8844f73fdb6cf6e7943e7e22f72d2c98b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670598"
---
# <a name="coutputqueuem_bsendanyway-member"></a><span data-ttu-id="0cc17-104">Miembro bSendAnyway COutputQueue:: m \_</span><span class="sxs-lookup"><span data-stu-id="0cc17-104">COutputQueue::m\_bSendAnyway member</span></span>

<span data-ttu-id="0cc17-105">Marca para invalidar el procesamiento por lotes.</span><span class="sxs-lookup"><span data-stu-id="0cc17-105">Flag to override batch processing.</span></span> <span data-ttu-id="0cc17-106">Al establecer esta marca en **true** , se invalida la marca [**COutputQueue:: m \_ bBatchExact**](coutputqueue-m-bbatchexact.md) y se entregan todos los ejemplos pendientes.</span><span class="sxs-lookup"><span data-stu-id="0cc17-106">Setting this flag to **TRUE** overrides the [**COutputQueue::m\_bBatchExact**](coutputqueue-m-bbatchexact.md) flag and delivers all pending samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cc17-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0cc17-107">Syntax</span></span>


```C++
BOOL m_bSendAnyway;
```



## <a name="requirements"></a><span data-ttu-id="0cc17-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cc17-108">Requirements</span></span>



| <span data-ttu-id="0cc17-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cc17-109">Requirement</span></span> | <span data-ttu-id="0cc17-110">Value</span><span class="sxs-lookup"><span data-stu-id="0cc17-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cc17-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0cc17-111">Header</span></span><br/>  | <dl> <span data-ttu-id="0cc17-112"><dt>Outputq. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0cc17-112"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0cc17-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0cc17-113">Library</span></span><br/> | <dl> <span data-ttu-id="0cc17-114"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0cc17-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cc17-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="0cc17-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cc17-116">**Clase COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="0cc17-116">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




