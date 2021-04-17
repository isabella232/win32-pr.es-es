---
description: El método posponer especifica un nuevo tiempo de presentación para un comando en cola previamente.
ms.assetid: 6201eb18-8180-445c-8d29-980511748fe4
title: Método CDeferredCommand. posponer (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Postpone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9ce19c5391541336f52dd872b44bb9f3a447c27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681265"
---
# <a name="cdeferredcommandpostpone-method"></a><span data-ttu-id="a2673-103">CDeferredCommand. posponer (método)</span><span class="sxs-lookup"><span data-stu-id="a2673-103">CDeferredCommand.Postpone method</span></span>

<span data-ttu-id="a2673-104">El `Postpone` método especifica un nuevo tiempo de presentación para un comando en cola previamente.</span><span class="sxs-lookup"><span data-stu-id="a2673-104">The `Postpone` method specifies a new presentation time for a previously queued command.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2673-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a2673-105">Syntax</span></span>


```C++
HRESULT Postpone(
   REFTIME newtime
);
```



## <a name="parameters"></a><span data-ttu-id="a2673-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a2673-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2673-107">*newtime*</span><span class="sxs-lookup"><span data-stu-id="a2673-107">*newtime*</span></span> 
</dt> <dd>

<span data-ttu-id="a2673-108">Nuevo tiempo de presentación.</span><span class="sxs-lookup"><span data-stu-id="a2673-108">New presentation time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2673-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a2673-109">Return value</span></span>

<span data-ttu-id="a2673-110">Devuelve la \_ hora VFW E \_ \_ ya \_ pasada si *newtime* ya se ha pasado.</span><span class="sxs-lookup"><span data-stu-id="a2673-110">Returns VFW\_E\_TIME\_ALREADY\_PASSED if *newtime* is already passed.</span></span> <span data-ttu-id="a2673-111">De lo contrario, devuelve un **valor HRESULT** que es el resultado de una llamada a [**CCmdQueue:: Remove**](ccmdqueue-remove.md) (al extraer de la lista) o [**CCmdQueue:: Insert**](ccmdqueue-insert.md) (al volver a insertar con la hora modificada).</span><span class="sxs-lookup"><span data-stu-id="a2673-111">Otherwise, returns an **HRESULT** resulting from a call to [**CCmdQueue::Remove**](ccmdqueue-remove.md) (when extracting from the list) or [**CCmdQueue::Insert**](ccmdqueue-insert.md) (when reinserting with the changed time).</span></span>

## <a name="remarks"></a><span data-ttu-id="a2673-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a2673-112">Remarks</span></span>

<span data-ttu-id="a2673-113">Esta función miembro implementa el método [**IDeferredCommand::P ostpone**](/windows/desktop/api/Control/nf-control-ideferredcommand-postpone) .</span><span class="sxs-lookup"><span data-stu-id="a2673-113">This member function implements the [**IDeferredCommand::Postpone**](/windows/desktop/api/Control/nf-control-ideferredcommand-postpone) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2673-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2673-114">Requirements</span></span>



| <span data-ttu-id="a2673-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2673-115">Requirement</span></span> | <span data-ttu-id="a2673-116">Value</span><span class="sxs-lookup"><span data-stu-id="a2673-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2673-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2673-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a2673-118"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2673-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a2673-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a2673-119">Library</span></span><br/> | <dl> <span data-ttu-id="a2673-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="a2673-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2673-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="a2673-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2673-122">**Clase CDeferredCommand**</span><span class="sxs-lookup"><span data-stu-id="a2673-122">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




