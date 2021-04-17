---
description: El método Remove quita el objeto CDeferredCommand de la cola.
ms.assetid: b3cff57d-9625-40db-b815-9529ac706f45
title: Método CCmdQueue. Remove (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef9f45c8176645c5937b5ad74045130ff8cd8c06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661247"
---
# <a name="ccmdqueueremove-method"></a><span data-ttu-id="143ec-103">CCmdQueue. Remove (método)</span><span class="sxs-lookup"><span data-stu-id="143ec-103">CCmdQueue.Remove method</span></span>

<span data-ttu-id="143ec-104">El `Remove` método quita el objeto [**CDeferredCommand**](cdeferredcommand.md) de la cola.</span><span class="sxs-lookup"><span data-stu-id="143ec-104">The `Remove` method removes the [**CDeferredCommand**](cdeferredcommand.md) object from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="143ec-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="143ec-105">Syntax</span></span>


```C++
virtual HRESULT Remove(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a><span data-ttu-id="143ec-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="143ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="143ec-107">*pCmd*</span><span class="sxs-lookup"><span data-stu-id="143ec-107">*pCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="143ec-108">Puntero al objeto **CDeferredCommand** que se va a quitar de la cola.</span><span class="sxs-lookup"><span data-stu-id="143ec-108">Pointer to the **CDeferredCommand** object to remove from the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="143ec-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="143ec-109">Return value</span></span>

<span data-ttu-id="143ec-110">Devuelve VFW \_ E \_ no \_ encontrado si el objeto no se encuentra en la cola.</span><span class="sxs-lookup"><span data-stu-id="143ec-110">Returns VFW\_E\_NOT\_FOUND if the object is not found in the queue.</span></span> <span data-ttu-id="143ec-111">De lo contrario, devuelve S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="143ec-111">Otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="143ec-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="143ec-112">Requirements</span></span>



| <span data-ttu-id="143ec-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="143ec-113">Requirement</span></span> | <span data-ttu-id="143ec-114">Value</span><span class="sxs-lookup"><span data-stu-id="143ec-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="143ec-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="143ec-115">Header</span></span><br/>  | <dl> <span data-ttu-id="143ec-116"><dt>Winutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="143ec-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="143ec-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="143ec-117">Library</span></span><br/> | <dl> <span data-ttu-id="143ec-118"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="143ec-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="143ec-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="143ec-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="143ec-120">**Clase CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="143ec-120">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




