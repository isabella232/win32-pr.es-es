---
description: 'Destructor CSourceStream.~CSourceStream: método destructor.'
ms.assetid: 678085c2-5999-4e62-8749-99b783787cc6
title: Destructor CSourceStream.~CSourceStream (Source.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.~CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bbf53184dadc42145758ab387d15e8b0a1bfe09d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085213"
---
# <a name="csourcestreamcsourcestream-destructor"></a><span data-ttu-id="e04b6-103">Destructor CSourceStream.~CSourceStream</span><span class="sxs-lookup"><span data-stu-id="e04b6-103">CSourceStream.~CSourceStream destructor</span></span>

<span data-ttu-id="e04b6-104">Método destructor.</span><span class="sxs-lookup"><span data-stu-id="e04b6-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e04b6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e04b6-105">Syntax</span></span>


```C++
~CSourceStream();
```



## <a name="remarks"></a><span data-ttu-id="e04b6-106">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e04b6-106">Remarks</span></span>

<span data-ttu-id="e04b6-107">El destructor quita automáticamente el pin del filtro propietario mediante una llamada [**a CSource::RemovePin**](csource-removepin.md).</span><span class="sxs-lookup"><span data-stu-id="e04b6-107">The destructor automatically removes the pin from the owning filter, by calling [**CSource::RemovePin**](csource-removepin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e04b6-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e04b6-108">Requirements</span></span>



| <span data-ttu-id="e04b6-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="e04b6-109">Requirement</span></span> | <span data-ttu-id="e04b6-110">Value</span><span class="sxs-lookup"><span data-stu-id="e04b6-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e04b6-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e04b6-111">Header</span></span><br/>  | <dl> <span data-ttu-id="e04b6-112"><dt>Source.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="e04b6-112"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e04b6-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e04b6-113">Library</span></span><br/> | <dl> <span data-ttu-id="e04b6-114"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="e04b6-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e04b6-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e04b6-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e04b6-116">**CSourceStream (clase)**</span><span class="sxs-lookup"><span data-stu-id="e04b6-116">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




