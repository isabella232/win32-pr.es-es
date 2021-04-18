---
description: El método Exit indica al subproceso de streaming que salga.
ms.assetid: 1bb59848-e405-40f9-87ec-33de8754e2dd
title: Método CSourceStream. Exit (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Exit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1ede6cf2318fa9226b8e220ff526f411def9b0f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660743"
---
# <a name="csourcestreamexit-method"></a><span data-ttu-id="798e6-103">CSourceStream. Exit (método)</span><span class="sxs-lookup"><span data-stu-id="798e6-103">CSourceStream.Exit method</span></span>

<span data-ttu-id="798e6-104">El `Exit` método indica al subproceso de streaming que salga.</span><span class="sxs-lookup"><span data-stu-id="798e6-104">The `Exit` method signals the streaming thread to exit.</span></span>

## <a name="syntax"></a><span data-ttu-id="798e6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="798e6-105">Syntax</span></span>


```C++
HRESULT Exit();
```



## <a name="parameters"></a><span data-ttu-id="798e6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="798e6-106">Parameters</span></span>

<span data-ttu-id="798e6-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="798e6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="798e6-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="798e6-108">Return value</span></span>

<span data-ttu-id="798e6-109">Devuelve S \_ correcto o E \_ inesperados.</span><span class="sxs-lookup"><span data-stu-id="798e6-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="798e6-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="798e6-110">Remarks</span></span>

<span data-ttu-id="798e6-111">El método [**CSourceStream:: Inactive**](csourcestream-inactive.md) llama a este método.</span><span class="sxs-lookup"><span data-stu-id="798e6-111">The [**CSourceStream::Inactive**](csourcestream-inactive.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="798e6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="798e6-112">Requirements</span></span>



| <span data-ttu-id="798e6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="798e6-113">Requirement</span></span> | <span data-ttu-id="798e6-114">Value</span><span class="sxs-lookup"><span data-stu-id="798e6-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="798e6-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="798e6-115">Header</span></span><br/>  | <dl> <span data-ttu-id="798e6-116"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="798e6-116"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="798e6-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="798e6-117">Library</span></span><br/> | <dl> <span data-ttu-id="798e6-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="798e6-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="798e6-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="798e6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="798e6-120">**Clase CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="798e6-120">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




