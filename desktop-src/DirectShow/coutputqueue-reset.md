---
description: El método Reset restablece el objeto para que pueda recibir más datos.
ms.assetid: 7074ed71-1650-4b21-a9a2-ad74d0e3e882
title: Método COutputQueue. Reset (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.Reset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d380ef738af3b684606e86a7c36dc04217c54b7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678973"
---
# <a name="coutputqueuereset-method"></a><span data-ttu-id="46b28-103">COutputQueue. Reset (método)</span><span class="sxs-lookup"><span data-stu-id="46b28-103">COutputQueue.Reset method</span></span>

<span data-ttu-id="46b28-104">El `Reset` método restablece el objeto para que pueda recibir más datos.</span><span class="sxs-lookup"><span data-stu-id="46b28-104">The `Reset` method resets the object so that it can receive more data.</span></span>

## <a name="syntax"></a><span data-ttu-id="46b28-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="46b28-105">Syntax</span></span>


```C++
void Reset();
```



## <a name="parameters"></a><span data-ttu-id="46b28-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="46b28-106">Parameters</span></span>

<span data-ttu-id="46b28-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="46b28-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="46b28-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="46b28-108">Return value</span></span>

<span data-ttu-id="46b28-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="46b28-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="46b28-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="46b28-110">Remarks</span></span>

<span data-ttu-id="46b28-111">Este método restablece la variable miembro [**COutputQueue:: m \_ HR**](coutputqueue-m-hr.md) a S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="46b28-111">This method resets the [**COutputQueue::m\_hr**](coutputqueue-m-hr.md) member variable to S\_OK.</span></span> <span data-ttu-id="46b28-112">El objeto puede volver a recibir ejemplos de medios; por ejemplo, después de una operación de vaciado.</span><span class="sxs-lookup"><span data-stu-id="46b28-112">The object can receive media samples again; for example, after a flush operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="46b28-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46b28-113">Requirements</span></span>



| <span data-ttu-id="46b28-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="46b28-114">Requirement</span></span> | <span data-ttu-id="46b28-115">Value</span><span class="sxs-lookup"><span data-stu-id="46b28-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46b28-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="46b28-116">Header</span></span><br/>  | <dl> <span data-ttu-id="46b28-117"><dt>Outputq. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="46b28-117"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="46b28-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="46b28-118">Library</span></span><br/> | <dl> <span data-ttu-id="46b28-119"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="46b28-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46b28-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="46b28-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46b28-121">**Clase COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="46b28-121">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




