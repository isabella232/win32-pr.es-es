---
description: El método IsStreamTime especifica si el comando se va a ejecutar en el momento de la secuencia o en el tiempo de presentación.
ms.assetid: 4fb315a4-1bc6-49c8-a47f-0a8a46f3f790
title: Método CDeferredCommand. IsStreamTime (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.IsStreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e15b579f911f6461df30c6b5ae9d3fc29f6fa1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681266"
---
# <a name="cdeferredcommandisstreamtime-method"></a><span data-ttu-id="73dac-103">CDeferredCommand. IsStreamTime, método</span><span class="sxs-lookup"><span data-stu-id="73dac-103">CDeferredCommand.IsStreamTime method</span></span>

<span data-ttu-id="73dac-104">El `IsStreamTime` método especifica si el comando se va a ejecutar en el momento de la secuencia o en el tiempo de presentación.</span><span class="sxs-lookup"><span data-stu-id="73dac-104">The `IsStreamTime` method specifies whether the command is to be run at stream time or presentation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="73dac-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="73dac-105">Syntax</span></span>


```C++
BOOL IsStreamTime();
```



## <a name="parameters"></a><span data-ttu-id="73dac-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="73dac-106">Parameters</span></span>

<span data-ttu-id="73dac-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="73dac-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="73dac-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="73dac-108">Return value</span></span>

<span data-ttu-id="73dac-109">Devuelve **true** si se establece en Stream Time; de lo contrario, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="73dac-109">Returns **TRUE** if set to stream time; otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="73dac-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73dac-110">Requirements</span></span>



| <span data-ttu-id="73dac-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="73dac-111">Requirement</span></span> | <span data-ttu-id="73dac-112">Value</span><span class="sxs-lookup"><span data-stu-id="73dac-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73dac-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73dac-113">Header</span></span><br/>  | <dl> <span data-ttu-id="73dac-114"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="73dac-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="73dac-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="73dac-115">Library</span></span><br/> | <dl> <span data-ttu-id="73dac-116"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="73dac-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73dac-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="73dac-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73dac-118">**Clase CDeferredCommand**</span><span class="sxs-lookup"><span data-stu-id="73dac-118">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




