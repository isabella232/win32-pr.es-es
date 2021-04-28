---
description: 'Constructor CAMThread.CAMThread: método constructor.'
ms.assetid: 0057adfe-e397-476b-90f9-7edbf7377b65
title: Constructor CAMThread.CAMThread (Wxutil.h)
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
ms.openlocfilehash: 0c4b9c5f80e131ce089b6a2da924e9cca41a84f6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096413"
---
# <a name="camthreadcamthread-constructor"></a><span data-ttu-id="8714b-103">Constructor CAMThread.CAMThread</span><span class="sxs-lookup"><span data-stu-id="8714b-103">CAMThread.CAMThread constructor</span></span>

<span data-ttu-id="8714b-104">Método constructor.</span><span class="sxs-lookup"><span data-stu-id="8714b-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="8714b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8714b-105">Syntax</span></span>


```C++
CAMThread(
   HRESULT *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="8714b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8714b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8714b-107">*Phr*</span><span class="sxs-lookup"><span data-stu-id="8714b-107">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="8714b-108">Puntero a un **valor HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="8714b-108">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="8714b-109">Si se produce un error en el constructor, este parámetro recibe un código de error.</span><span class="sxs-lookup"><span data-stu-id="8714b-109">If the constructor fails, this parameter receives an error code.</span></span> <span data-ttu-id="8714b-110">Si esto ocurre, el objeto no está en un estado válido.</span><span class="sxs-lookup"><span data-stu-id="8714b-110">If this occurs, the object is not in a valid state.</span></span>

<span data-ttu-id="8714b-111">Para la compatibilidad con versiones anteriores de strmbase.lib, el valor predeterminado de este parámetro es **NULL.**</span><span class="sxs-lookup"><span data-stu-id="8714b-111">For backward compatibility with earlier versions of strmbase.lib, this parameter defaults to **NULL**.</span></span> <span data-ttu-id="8714b-112">Sin embargo, se prefiere pasar un valor distinto de **NULL,** para que el autor de la llamada pueda comprobar el estado del objeto.</span><span class="sxs-lookup"><span data-stu-id="8714b-112">However, passing a non-**NULL** value is preferred, so that the caller can check the status of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8714b-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8714b-113">Remarks</span></span>

<span data-ttu-id="8714b-114">El método constructor no crea el subproceso.</span><span class="sxs-lookup"><span data-stu-id="8714b-114">The constructor method does not create the thread.</span></span> <span data-ttu-id="8714b-115">Para crear el subproceso, llame al [**método CAMThread::Create.**](camthread-create.md)</span><span class="sxs-lookup"><span data-stu-id="8714b-115">To create the thread, call the [**CAMThread::Create**](camthread-create.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8714b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8714b-116">Requirements</span></span>



| <span data-ttu-id="8714b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8714b-117">Requirement</span></span> | <span data-ttu-id="8714b-118">Value</span><span class="sxs-lookup"><span data-stu-id="8714b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8714b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8714b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="8714b-120"><dt>Wxutil.h (incluir Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="8714b-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="8714b-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8714b-121">Library</span></span><br/> | <dl> <span data-ttu-id="8714b-122"><dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="8714b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8714b-123">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8714b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8714b-124">**CLASE CAMThread**</span><span class="sxs-lookup"><span data-stu-id="8714b-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




