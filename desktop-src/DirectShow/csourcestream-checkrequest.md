---
description: El método CheckRequest comprueba si hay una solicitud de subproceso, sin bloqueos.
ms.assetid: b4691dde-abec-4671-bea6-0f22cc4e7c61
title: CSourceStream. CheckRequest (método) (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3100d449d2f29b2080541c5968cad6abc5643b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690508"
---
# <a name="csourcestreamcheckrequest-method"></a><span data-ttu-id="0dfd8-103">CSourceStream. CheckRequest, método</span><span class="sxs-lookup"><span data-stu-id="0dfd8-103">CSourceStream.CheckRequest method</span></span>

<span data-ttu-id="0dfd8-104">El `CheckRequest` método comprueba si hay una solicitud de subproceso, sin bloqueos.</span><span class="sxs-lookup"><span data-stu-id="0dfd8-104">The `CheckRequest` method checks if there is a thread request, without blocking.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dfd8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0dfd8-105">Syntax</span></span>


```C++
BOOL CheckRequest(
   Command *pCom
);
```



## <a name="parameters"></a><span data-ttu-id="0dfd8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0dfd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dfd8-107">*pCom*</span><span class="sxs-lookup"><span data-stu-id="0dfd8-107">*pCom*</span></span> 
</dt> <dd>

<span data-ttu-id="0dfd8-108">Puntero a una variable que recibe el valor pasado en la última llamada al método [**CAMThread:: CallWorker**](camthread-callworker.md) .</span><span class="sxs-lookup"><span data-stu-id="0dfd8-108">Pointer to a variable that receives the value passed in the last call to the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dfd8-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0dfd8-109">Return value</span></span>

<span data-ttu-id="0dfd8-110">Devuelve **true** si hay una solicitud pendiente o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="0dfd8-110">Returns **TRUE** if there is a pending request, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dfd8-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0dfd8-111">Remarks</span></span>

<span data-ttu-id="0dfd8-112">Este método invalida el método [**CAMThread:: CheckRequest**](camthread-checkrequest.md) para realizar la comprobación de tipos.</span><span class="sxs-lookup"><span data-stu-id="0dfd8-112">This method overrides the [**CAMThread::CheckRequest**](camthread-checkrequest.md) method to perform type-checking.</span></span> <span data-ttu-id="0dfd8-113">La clase **CSourceStream** define el siguiente tipo enumerado para el parámetro *pCom* :</span><span class="sxs-lookup"><span data-stu-id="0dfd8-113">The **CSourceStream** class defines the following enumerated type for the *pCom* parameter:</span></span>


```C++
enum Command {CMD_INIT, CMD_PAUSE, CMD_RUN, CMD_STOP, CMD_EXIT};
```



## <a name="requirements"></a><span data-ttu-id="0dfd8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0dfd8-114">Requirements</span></span>



| <span data-ttu-id="0dfd8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dfd8-115">Requirement</span></span> | <span data-ttu-id="0dfd8-116">Value</span><span class="sxs-lookup"><span data-stu-id="0dfd8-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dfd8-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0dfd8-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0dfd8-118"><dt>Source. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0dfd8-118"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0dfd8-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0dfd8-119">Library</span></span><br/> | <dl> <span data-ttu-id="0dfd8-120"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="0dfd8-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0dfd8-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="0dfd8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dfd8-122">**Clase CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="0dfd8-122">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




