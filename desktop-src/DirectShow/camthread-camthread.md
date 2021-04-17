---
description: Método de constructor.
ms.assetid: 0057adfe-e397-476b-90f9-7edbf7377b65
title: Constructor CAMThread. CAMThread (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abaac0c3b0330cd41db7ecd21f894733de10a1b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661149"
---
# <a name="camthreadcamthread-constructor"></a><span data-ttu-id="1c532-103">Constructor CAMThread. CAMThread</span><span class="sxs-lookup"><span data-stu-id="1c532-103">CAMThread.CAMThread constructor</span></span>

<span data-ttu-id="1c532-104">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="1c532-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c532-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c532-105">Syntax</span></span>


```C++
CAMThread(
   HRESULT *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="1c532-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c532-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c532-107">*phr*</span><span class="sxs-lookup"><span data-stu-id="1c532-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="1c532-108">Puntero a un valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1c532-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="1c532-109">Si se produce un error en el constructor, este parámetro recibe un código de error.</span><span class="sxs-lookup"><span data-stu-id="1c532-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="1c532-110">Si esto ocurre, el objeto no tiene un estado válido.</span><span class="sxs-lookup"><span data-stu-id="1c532-110">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="1c532-111">Para mantener la compatibilidad con versiones anteriores de strmbase. lib, este parámetro tiene como valor predeterminado **null**.</span><span class="sxs-lookup"><span data-stu-id="1c532-111">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="1c532-112">Sin embargo, se prefiere pasar un valor distinto de **null** para que el autor de la llamada pueda comprobar el estado del objeto.</span><span class="sxs-lookup"><span data-stu-id="1c532-112">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c532-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1c532-113">Remarks</span></span>

<span data-ttu-id="1c532-114">El método de constructor no crea el subproceso.</span><span class="sxs-lookup"><span data-stu-id="1c532-114">The constructor method does not create the thread.</span></span> <span data-ttu-id="1c532-115">Para crear el subproceso, llame al método [**CAMThread:: Create**](camthread-create.md) .</span><span class="sxs-lookup"><span data-stu-id="1c532-115">To create the thread, call the [**CAMThread::Create**](camthread-create.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c532-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c532-116">Requirements</span></span>



| <span data-ttu-id="1c532-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c532-117">Requirement</span></span> | <span data-ttu-id="1c532-118">Value</span><span class="sxs-lookup"><span data-stu-id="1c532-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c532-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c532-119">Header</span></span><br/>  | <dl> <span data-ttu-id="1c532-120"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c532-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1c532-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1c532-121">Library</span></span><br/> | <dl> <span data-ttu-id="1c532-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="1c532-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c532-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c532-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c532-124">**Clase CAMThread**</span><span class="sxs-lookup"><span data-stu-id="1c532-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




