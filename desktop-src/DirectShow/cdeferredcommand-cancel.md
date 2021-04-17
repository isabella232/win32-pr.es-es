---
description: 'El método CANCEL cancela una solicitud CDeferredCommand:: Invoke previamente en cola.'
ms.assetid: 77671f6b-db50-4d8a-b727-aeed365f0303
title: Método CDeferredCommand. Cancel (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Cancel
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 524300da374b10eaac884161bb0195d88f45476d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661299"
---
# <a name="cdeferredcommandcancel-method"></a><span data-ttu-id="ab61f-103">CDeferredCommand. Cancel (método)</span><span class="sxs-lookup"><span data-stu-id="ab61f-103">CDeferredCommand.Cancel method</span></span>

<span data-ttu-id="ab61f-104">El `Cancel` método cancela una solicitud [**CDeferredCommand:: Invoke**](cdeferredcommand-invoke.md) previamente en cola.</span><span class="sxs-lookup"><span data-stu-id="ab61f-104">The `Cancel` method cancels a previously queued [**CDeferredCommand::Invoke**](cdeferredcommand-invoke.md) request.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab61f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab61f-105">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="ab61f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab61f-106">Parameters</span></span>

<span data-ttu-id="ab61f-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="ab61f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ab61f-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab61f-108">Return value</span></span>

<span data-ttu-id="ab61f-109">Devuelve VFW \_ E \_ ya \_ cancelado si **m \_ pQueue** es **null**.</span><span class="sxs-lookup"><span data-stu-id="ab61f-109">Returns VFW\_E\_ALREADY\_CANCELLED if **m\_pQueue** is **NULL**.</span></span> <span data-ttu-id="ab61f-110">Devuelve un **valor HRESULT** de [**CCmdQueue:: Remove**](ccmdqueue-remove.md) si la llamada genera un error.</span><span class="sxs-lookup"><span data-stu-id="ab61f-110">Returns an **HRESULT** from [**CCmdQueue::Remove**](ccmdqueue-remove.md) if the call generates an error.</span></span> <span data-ttu-id="ab61f-111">Devuelve S \_ correcto si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="ab61f-111">Returns S\_OK if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab61f-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab61f-112">Remarks</span></span>

<span data-ttu-id="ab61f-113">Esta función miembro implementa el método [**IDeferredCommand:: CANCEL**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) .</span><span class="sxs-lookup"><span data-stu-id="ab61f-113">This member function implements the [**IDeferredCommand::Cancel**](/windows/desktop/api/Control/nf-control-ideferredcommand-cancel) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab61f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab61f-114">Requirements</span></span>



| <span data-ttu-id="ab61f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab61f-115">Requirement</span></span> | <span data-ttu-id="ab61f-116">Value</span><span class="sxs-lookup"><span data-stu-id="ab61f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab61f-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab61f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ab61f-118"><dt>Ctlutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab61f-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ab61f-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab61f-119">Library</span></span><br/> | <dl> <span data-ttu-id="ab61f-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ab61f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab61f-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab61f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab61f-122">**Clase CDeferredCommand**</span><span class="sxs-lookup"><span data-stu-id="ab61f-122">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




