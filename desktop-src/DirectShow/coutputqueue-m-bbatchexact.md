---
description: Marca que especifica si el objeto proporciona ejemplos en lotes exactos.
ms.assetid: 1a37c78f-4499-4ebb-92b4-b71ba3ff1a02
title: 'Miembro COutputQueue:: m_bBatchExact (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bBatchExact
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5f38d8a0e7335025688f52015ff9ed4d4892820
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671343"
---
# <a name="coutputqueuem_bbatchexact-member"></a><span data-ttu-id="9b6c7-103">Miembro bBatchExact COutputQueue:: m \_</span><span class="sxs-lookup"><span data-stu-id="9b6c7-103">COutputQueue::m\_bBatchExact member</span></span>

<span data-ttu-id="9b6c7-104">Marca que especifica si el objeto proporciona ejemplos en lotes exactos.</span><span class="sxs-lookup"><span data-stu-id="9b6c7-104">Flag that specifies whether the object delivers samples in exact batches.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b6c7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b6c7-105">Syntax</span></span>


```C++
const BOOL m_bBatchExact;
```



## <a name="remarks"></a><span data-ttu-id="9b6c7-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b6c7-106">Remarks</span></span>

<span data-ttu-id="9b6c7-107">Si el valor es **true**, el objeto espera hasta que tenga un lote completo de ejemplos de medios antes de entregar cualquiera.</span><span class="sxs-lookup"><span data-stu-id="9b6c7-107">If the value is **TRUE**, the object waits until it has a complete batch of media samples before delivering any.</span></span> <span data-ttu-id="9b6c7-108">De lo contrario, proporciona ejemplos a medida que llegan.</span><span class="sxs-lookup"><span data-stu-id="9b6c7-108">Otherwise, it delivers samples as they arrive.</span></span> <span data-ttu-id="9b6c7-109">La variable miembro [**COutputQueue:: m \_ lBatchSize**](coutputqueue-m-lbatchsize.md) define el tamaño del lote.</span><span class="sxs-lookup"><span data-stu-id="9b6c7-109">The [**COutputQueue::m\_lBatchSize**](coutputqueue-m-lbatchsize.md) member variable defines the batch size.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b6c7-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b6c7-110">Requirements</span></span>



| <span data-ttu-id="9b6c7-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b6c7-111">Requirement</span></span> | <span data-ttu-id="9b6c7-112">Value</span><span class="sxs-lookup"><span data-stu-id="9b6c7-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b6c7-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b6c7-113">Header</span></span><br/>  | <dl> <span data-ttu-id="9b6c7-114"><dt>Outputq. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9b6c7-114"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9b6c7-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9b6c7-115">Library</span></span><br/> | <dl> <span data-ttu-id="9b6c7-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="9b6c7-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b6c7-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b6c7-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b6c7-118">**Clase COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="9b6c7-118">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




