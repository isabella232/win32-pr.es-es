---
description: El método InitialThreadProc llama al procedimiento de subproceso principal.
ms.assetid: 1546c214-7ea9-4484-974b-dbd4b2b3e296
title: CAMThread.Inimétodo tialThreadProc (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd7fd0aa12d0659776db7e39fb223095762fc209
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671290"
---
# <a name="camthreadinitialthreadproc-method"></a><span data-ttu-id="b1b91-103">CAMThread.Inimétodo tialThreadProc</span><span class="sxs-lookup"><span data-stu-id="b1b91-103">CAMThread.InitialThreadProc method</span></span>

<span data-ttu-id="b1b91-104">El `InitialThreadProc` método llama al procedimiento de subproceso principal.</span><span class="sxs-lookup"><span data-stu-id="b1b91-104">The `InitialThreadProc` method calls the main thread procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1b91-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1b91-105">Syntax</span></span>


```C++
DWORD InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a><span data-ttu-id="b1b91-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b1b91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1b91-107">*FV*</span><span class="sxs-lookup"><span data-stu-id="b1b91-107">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="b1b91-108">`this` puntero.</span><span class="sxs-lookup"><span data-stu-id="b1b91-108">`this` pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1b91-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b1b91-109">Return value</span></span>

<span data-ttu-id="b1b91-110">Devuelve el **DWORD** devuelto por [**CAMThread:: ThreadProc**](camthread-threadproc.md).</span><span class="sxs-lookup"><span data-stu-id="b1b91-110">Returns the **DWORD** returned by [**CAMThread::ThreadProc**](camthread-threadproc.md).</span></span> <span data-ttu-id="b1b91-111">La clase derivada define este valor.</span><span class="sxs-lookup"><span data-stu-id="b1b91-111">The derived class defines this value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1b91-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b1b91-112">Remarks</span></span>

<span data-ttu-id="b1b91-113">El método [**CAMThread:: Create**](camthread-create.md) usa este método para el procedimiento de subproceso al crear el subproceso.</span><span class="sxs-lookup"><span data-stu-id="b1b91-113">The [**CAMThread::Create**](camthread-create.md) method uses this method for the thread procedure when it creates the thread.</span></span> <span data-ttu-id="b1b91-114">Utiliza el `this` puntero como argumento de subproceso.</span><span class="sxs-lookup"><span data-stu-id="b1b91-114">It uses the `this` pointer as the thread argument.</span></span>

<span data-ttu-id="b1b91-115">Este método llama al método [**CAMThread:: CoInitializeHelper**](camthread-coinitializehelper.md) y después a ThreadProc.</span><span class="sxs-lookup"><span data-stu-id="b1b91-115">This method calls the [**CAMThread::CoInitializeHelper**](camthread-coinitializehelper.md) method and then ThreadProc.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1b91-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1b91-116">Requirements</span></span>



| <span data-ttu-id="b1b91-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1b91-117">Requirement</span></span> | <span data-ttu-id="b1b91-118">Value</span><span class="sxs-lookup"><span data-stu-id="b1b91-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1b91-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b1b91-119">Header</span></span><br/>  | <dl> <span data-ttu-id="b1b91-120"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1b91-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b1b91-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b1b91-121">Library</span></span><br/> | <dl> <span data-ttu-id="b1b91-122"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="b1b91-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1b91-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="b1b91-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1b91-124">**Clase CAMThread**</span><span class="sxs-lookup"><span data-stu-id="b1b91-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




