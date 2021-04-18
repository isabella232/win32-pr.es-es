---
description: Método de destructor.
ms.assetid: 678085c2-5999-4e62-8749-99b783787cc6
title: CSourceStream. ~ CSourceStream (Source. h)
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
ms.openlocfilehash: fa27d50a9c1acbc9c8a27407cb97673d60158e4a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660724"
---
# <a name="csourcestreamcsourcestream-destructor"></a><span data-ttu-id="7901b-103">CSourceStream. ~ CSourceStream (destructor)</span><span class="sxs-lookup"><span data-stu-id="7901b-103">CSourceStream.~CSourceStream destructor</span></span>

<span data-ttu-id="7901b-104">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="7901b-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7901b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7901b-105">Syntax</span></span>


```C++
~CSourceStream();
```



## <a name="remarks"></a><span data-ttu-id="7901b-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7901b-106">Remarks</span></span>

<span data-ttu-id="7901b-107">El destructor quita automáticamente el PIN del filtro propietario llamando a [**CSource:: RemovePin**](csource-removepin.md).</span><span class="sxs-lookup"><span data-stu-id="7901b-107">The destructor automatically removes the pin from the owning filter, by calling [**CSource::RemovePin**](csource-removepin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7901b-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7901b-108">Requirements</span></span>



| <span data-ttu-id="7901b-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="7901b-109">Requirement</span></span> | <span data-ttu-id="7901b-110">Value</span><span class="sxs-lookup"><span data-stu-id="7901b-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7901b-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7901b-111">Header</span></span><br/>  | <dl> <span data-ttu-id="7901b-112"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7901b-112"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7901b-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7901b-113">Library</span></span><br/> | <dl> <span data-ttu-id="7901b-114"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="7901b-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7901b-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="7901b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7901b-116">**Clase CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="7901b-116">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




