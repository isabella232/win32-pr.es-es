---
description: Valor HRESULT que indica si el objeto aceptará ejemplos. Si el valor es S \_ OK, el objeto aceptará ejemplos. De lo contrario, rechaza los ejemplos.
ms.assetid: e05d4d2e-cc3e-4b83-8531-bc4bd6d665ac
title: 'Miembro COutputQueue:: m_hr (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hr
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b786afa24f974d5eab7e13062105f26386da1c30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670749"
---
# <a name="coutputqueuem_hr-member"></a><span data-ttu-id="91d3d-105">Miembro COutputQueue:: m \_ HR</span><span class="sxs-lookup"><span data-stu-id="91d3d-105">COutputQueue::m\_hr member</span></span>

<span data-ttu-id="91d3d-106">Valor **HRESULT** que indica si el objeto aceptará ejemplos.</span><span class="sxs-lookup"><span data-stu-id="91d3d-106">**HRESULT** value that indicates whether the object will accept samples.</span></span> <span data-ttu-id="91d3d-107">Si el valor es S \_ OK, el objeto aceptará ejemplos.</span><span class="sxs-lookup"><span data-stu-id="91d3d-107">If the value is S\_OK, the object will accept samples.</span></span> <span data-ttu-id="91d3d-108">De lo contrario, rechaza los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="91d3d-108">Otherwise, it rejects samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="91d3d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="91d3d-109">Syntax</span></span>


```C++
HRESULT m_hr;
```



## <a name="remarks"></a><span data-ttu-id="91d3d-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91d3d-110">Remarks</span></span>

<span data-ttu-id="91d3d-111">Esta variable miembro se utiliza para coordinar las actividades entre subprocesos.</span><span class="sxs-lookup"><span data-stu-id="91d3d-111">This member variable is used to coordinate activities across threads.</span></span> <span data-ttu-id="91d3d-112">Si el PIN de entrada de nivel inferior rechaza un ejemplo o si el objeto comienza a vaciarse, el valor se establece en S \_ false o en un código de error.</span><span class="sxs-lookup"><span data-stu-id="91d3d-112">If the downstream input pin rejects a sample, or if the object begins flushing, the value is set to S\_FALSE or an error code.</span></span> <span data-ttu-id="91d3d-113">El objeto no proporcionará más muestras hasta que se complete el vaciado o hasta que se llame al método [**COutputQueue:: RESET**](coutputqueue-reset.md) .</span><span class="sxs-lookup"><span data-stu-id="91d3d-113">The object will not deliver any more samples until flushing is complete, or until the [**COutputQueue::Reset**](coutputqueue-reset.md) method is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="91d3d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91d3d-114">Requirements</span></span>



| <span data-ttu-id="91d3d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="91d3d-115">Requirement</span></span> | <span data-ttu-id="91d3d-116">Value</span><span class="sxs-lookup"><span data-stu-id="91d3d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91d3d-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91d3d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="91d3d-118"><dt>Outputq. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="91d3d-118"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="91d3d-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="91d3d-119">Library</span></span><br/> | <dl> <span data-ttu-id="91d3d-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="91d3d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91d3d-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="91d3d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91d3d-122">**Clase COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="91d3d-122">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




