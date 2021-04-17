---
description: El método SetTemporalCompression especifica si los ejemplos se comprimen mediante la compresión temporal (interframe).
ms.assetid: cdd181ee-d1e9-48b0-96f6-e76db9f3f933
title: Método CMediaType. SetTemporalCompression (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetTemporalCompression
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a0aba07375c5b5c760c432de704562efb2bea148
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680284"
---
# <a name="cmediatypesettemporalcompression-method"></a><span data-ttu-id="63129-103">CMediaType. SetTemporalCompression, método</span><span class="sxs-lookup"><span data-stu-id="63129-103">CMediaType.SetTemporalCompression method</span></span>

<span data-ttu-id="63129-104">El `SetTemporalCompression` método especifica si los ejemplos se comprimen mediante la compresión temporal (interframe).</span><span class="sxs-lookup"><span data-stu-id="63129-104">The `SetTemporalCompression` method specifies whether samples are compressed using temporal (interframe) compression.</span></span>

## <a name="syntax"></a><span data-ttu-id="63129-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63129-105">Syntax</span></span>


```C++
void SetTemporalCompression(
   BOOL bCompressed
);
```



## <a name="parameters"></a><span data-ttu-id="63129-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="63129-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63129-107">*bCompressed*</span><span class="sxs-lookup"><span data-stu-id="63129-107">*bCompressed*</span></span> 
</dt> <dd>

<span data-ttu-id="63129-108">Valor booleano que especifica si la secuencia utiliza la compresión temporal.</span><span class="sxs-lookup"><span data-stu-id="63129-108">Boolean value that specifies whether the stream uses temporal compression.</span></span> <span data-ttu-id="63129-109">Si la secuencia utiliza la compresión temporal, establezca el valor en **true**.</span><span class="sxs-lookup"><span data-stu-id="63129-109">If the stream uses temporal compression, set the value to **TRUE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63129-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="63129-110">Return value</span></span>

<span data-ttu-id="63129-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="63129-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="63129-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63129-112">Remarks</span></span>

<span data-ttu-id="63129-113">Este método establece el miembro **bTemporalCompression** .</span><span class="sxs-lookup"><span data-stu-id="63129-113">This method sets the **bTemporalCompression** member.</span></span>

## <a name="requirements"></a><span data-ttu-id="63129-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63129-114">Requirements</span></span>



| <span data-ttu-id="63129-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="63129-115">Requirement</span></span> | <span data-ttu-id="63129-116">Value</span><span class="sxs-lookup"><span data-stu-id="63129-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63129-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63129-117">Header</span></span><br/>  | <dl> <span data-ttu-id="63129-118"><dt>Mtype. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63129-118"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="63129-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="63129-119">Library</span></span><br/> | <dl> <span data-ttu-id="63129-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="63129-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63129-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="63129-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63129-122">**Clase CMediaType**</span><span class="sxs-lookup"><span data-stu-id="63129-122">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




