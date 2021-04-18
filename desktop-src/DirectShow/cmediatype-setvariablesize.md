---
description: El método SetVariableSize especifica que los ejemplos no tienen un tamaño fijo.
ms.assetid: 2a207cdb-f8e6-44aa-8bf6-868267aeb42d
title: Método CMediaType. SetVariableSize (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetVariableSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4621a639b3bc18382bc41ae9425c4de50db920ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681132"
---
# <a name="cmediatypesetvariablesize-method"></a><span data-ttu-id="bff18-103">CMediaType. SetVariableSize, método</span><span class="sxs-lookup"><span data-stu-id="bff18-103">CMediaType.SetVariableSize method</span></span>

<span data-ttu-id="bff18-104">El `SetVariableSize` método especifica que los ejemplos no tienen un tamaño fijo.</span><span class="sxs-lookup"><span data-stu-id="bff18-104">The `SetVariableSize` method specifies that samples do not have a fixed size.</span></span>

## <a name="syntax"></a><span data-ttu-id="bff18-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bff18-105">Syntax</span></span>


```C++
void SetVariableSize();
```



## <a name="parameters"></a><span data-ttu-id="bff18-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bff18-106">Parameters</span></span>

<span data-ttu-id="bff18-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="bff18-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bff18-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bff18-108">Return value</span></span>

<span data-ttu-id="bff18-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="bff18-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bff18-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bff18-110">Remarks</span></span>

<span data-ttu-id="bff18-111">Este método establece el miembro **bFixedSizeSamples** en **false**.</span><span class="sxs-lookup"><span data-stu-id="bff18-111">This method sets the **bFixedSizeSamples** member to **FALSE**.</span></span> <span data-ttu-id="bff18-112">Las llamadas subsiguientes al método [**CMediaType:: GetSampleSize**](cmediatype-getsamplesize.md) devuelven cero.</span><span class="sxs-lookup"><span data-stu-id="bff18-112">Subsequent calls to the [**CMediaType::GetSampleSize**](cmediatype-getsamplesize.md) method return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="bff18-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bff18-113">Requirements</span></span>



| <span data-ttu-id="bff18-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="bff18-114">Requirement</span></span> | <span data-ttu-id="bff18-115">Value</span><span class="sxs-lookup"><span data-stu-id="bff18-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bff18-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bff18-116">Header</span></span><br/>  | <dl> <span data-ttu-id="bff18-117"><dt>Mtype. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bff18-117"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="bff18-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bff18-118">Library</span></span><br/> | <dl> <span data-ttu-id="bff18-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="bff18-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bff18-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="bff18-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bff18-121">**Clase CMediaType**</span><span class="sxs-lookup"><span data-stu-id="bff18-121">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




