---
description: El método Insert agrega un objeto CDeferredCommand a la cola.
ms.assetid: 41f9c30c-6267-435a-9089-eb34ae606896
title: Método CCmdQueue. Insert (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Insert
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bad004641258e29ed42d7142a5b0ab2c0ceb78d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660169"
---
# <a name="ccmdqueueinsert-method"></a><span data-ttu-id="661bc-103">CCmdQueue. Insert (método)</span><span class="sxs-lookup"><span data-stu-id="661bc-103">CCmdQueue.Insert method</span></span>

<span data-ttu-id="661bc-104">El `Insert` método agrega un objeto [**CDeferredCommand**](cdeferredcommand.md) a la cola.</span><span class="sxs-lookup"><span data-stu-id="661bc-104">The `Insert` method adds a [**CDeferredCommand**](cdeferredcommand.md) object to the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="661bc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="661bc-105">Syntax</span></span>


```C++
virtual HRESULT Insert(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a><span data-ttu-id="661bc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="661bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="661bc-107">*pCmd*</span><span class="sxs-lookup"><span data-stu-id="661bc-107">*pCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="661bc-108">Puntero al objeto **CDeferredCommand** que se va a agregar a la cola.</span><span class="sxs-lookup"><span data-stu-id="661bc-108">Pointer to the **CDeferredCommand** object to add to the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="661bc-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="661bc-109">Return value</span></span>

<span data-ttu-id="661bc-110">Devuelve S \_ OK en la implementación predeterminada.</span><span class="sxs-lookup"><span data-stu-id="661bc-110">Returns S\_OK in the default implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="661bc-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="661bc-111">Requirements</span></span>



| <span data-ttu-id="661bc-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="661bc-112">Requirement</span></span> | <span data-ttu-id="661bc-113">Value</span><span class="sxs-lookup"><span data-stu-id="661bc-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="661bc-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="661bc-114">Header</span></span><br/>  | <dl> <span data-ttu-id="661bc-115"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="661bc-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="661bc-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="661bc-116">Library</span></span><br/> | <dl> <span data-ttu-id="661bc-117"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="661bc-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="661bc-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="661bc-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="661bc-119">**Clase CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="661bc-119">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




