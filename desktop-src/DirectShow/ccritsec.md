---
description: La clase CCritSec proporciona un bloqueo de subprocesos.
ms.assetid: ecc60afe-15d0-4780-8133-1dfc558c6325
title: Clase CCritSec (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8db0243ecfecd47655f547d40390e602c04d5b88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679400"
---
# <a name="ccritsec-class"></a><span data-ttu-id="ab71f-103">Clase CCritSec</span><span class="sxs-lookup"><span data-stu-id="ab71f-103">CCritSec class</span></span>

<span data-ttu-id="ab71f-104">La clase **CCritSec** proporciona un bloqueo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="ab71f-104">The **CCritSec** class provides a thread lock.</span></span>

<span data-ttu-id="ab71f-105">Esta clase es un contenedor fino para un objeto **de \_ sección crítica** de Windows.</span><span class="sxs-lookup"><span data-stu-id="ab71f-105">This class is a thin wrapper for a Windows **CRITICAL\_SECTION** object.</span></span> <span data-ttu-id="ab71f-106">Puede bloquear y desbloquear el subproceso llamando a los métodos [**CCritSec:: Lock**](ccritsec-lock.md) y [**CCritSec:: Unlock**](ccritsec-unlock.md) .</span><span class="sxs-lookup"><span data-stu-id="ab71f-106">You can lock and unlock the thread by calling the [**CCritSec::Lock**](ccritsec-lock.md) and [**CCritSec::Unlock**](ccritsec-unlock.md) methods.</span></span> <span data-ttu-id="ab71f-107">Sin embargo, es más seguro usar esta clase junto con la clase [**CAutoLock**](cautolock.md) .</span><span class="sxs-lookup"><span data-stu-id="ab71f-107">However, it is safer to use this class in conjunction with the [**CAutoLock**](cautolock.md) class.</span></span> <span data-ttu-id="ab71f-108">Cuando la clase **CAutoLock** sale del ámbito, desbloquea automáticamente el objeto **CCritSec** .</span><span class="sxs-lookup"><span data-stu-id="ab71f-108">When the **CAutoLock** class goes out of scope, it automatically unlocks the **CCritSec** object.</span></span> <span data-ttu-id="ab71f-109">Además, se compila en el código en línea eficaz.</span><span class="sxs-lookup"><span data-stu-id="ab71f-109">Moreover, it compiles to efficient inline code.</span></span>



| <span data-ttu-id="ab71f-110">Variables de miembro público</span><span class="sxs-lookup"><span data-stu-id="ab71f-110">Public Member Variables</span></span>                            | <span data-ttu-id="ab71f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab71f-111">Description</span></span>                                              |
|----------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="ab71f-112">**m \_ currentOwner**</span><span class="sxs-lookup"><span data-stu-id="ab71f-112">**m\_currentOwner**</span></span>](ccritsec-m-currentowner.md) | <span data-ttu-id="ab71f-113">Identificador de subproceso del subproceso propietario.</span><span class="sxs-lookup"><span data-stu-id="ab71f-113">Thread identifier of the owning thread.</span></span>                  |
| [<span data-ttu-id="ab71f-114">**m \_ lockCount**</span><span class="sxs-lookup"><span data-stu-id="ab71f-114">**m\_lockCount**</span></span>](ccritsec-m-lockcount.md)       | <span data-ttu-id="ab71f-115">Número de bloqueos pendientes en este objeto.</span><span class="sxs-lookup"><span data-stu-id="ab71f-115">Number of outstanding locks on this object.</span></span>              |
| [<span data-ttu-id="ab71f-116">**m \_ fTrace**</span><span class="sxs-lookup"><span data-stu-id="ab71f-116">**m\_fTrace**</span></span>](ccritsec-m-ftrace.md)             | <span data-ttu-id="ab71f-117">Valor booleano que especifica si se va a realizar el seguimiento de este bloqueo.</span><span class="sxs-lookup"><span data-stu-id="ab71f-117">Boolean value that specifies whether to trace this lock.</span></span> |
| <span data-ttu-id="ab71f-118">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="ab71f-118">Public Methods</span></span>                                     | <span data-ttu-id="ab71f-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab71f-119">Description</span></span>                                              |
| [<span data-ttu-id="ab71f-120">**CCritSec**</span><span class="sxs-lookup"><span data-stu-id="ab71f-120">**CCritSec**</span></span>](ccritsec-ccritsec.md)              | <span data-ttu-id="ab71f-121">Método de constructor.</span><span class="sxs-lookup"><span data-stu-id="ab71f-121">Constructor method.</span></span>                                      |
| [<span data-ttu-id="ab71f-122">**~ CCritSec**</span><span class="sxs-lookup"><span data-stu-id="ab71f-122">**~CCritSec**</span></span>](ccritsec--ccritsec.md)            | <span data-ttu-id="ab71f-123">Método de destructor.</span><span class="sxs-lookup"><span data-stu-id="ab71f-123">Destructor method.</span></span>                                       |
| [<span data-ttu-id="ab71f-124">**Lock**</span><span class="sxs-lookup"><span data-stu-id="ab71f-124">**Lock**</span></span>](ccritsec-lock.md)                      | <span data-ttu-id="ab71f-125">Bloquea el objeto de sección crítica.</span><span class="sxs-lookup"><span data-stu-id="ab71f-125">Locks the critical section object.</span></span>                       |
| [<span data-ttu-id="ab71f-126">**Pulsa**</span><span class="sxs-lookup"><span data-stu-id="ab71f-126">**Unlock**</span></span>](ccritsec-unlock.md)                  | <span data-ttu-id="ab71f-127">Desbloquea el objeto de sección crítica.</span><span class="sxs-lookup"><span data-stu-id="ab71f-127">Unlocks the critical section object.</span></span>                     |



 

## <a name="requirements"></a><span data-ttu-id="ab71f-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab71f-128">Requirements</span></span>



| <span data-ttu-id="ab71f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab71f-129">Requirement</span></span> | <span data-ttu-id="ab71f-130">Value</span><span class="sxs-lookup"><span data-stu-id="ab71f-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab71f-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab71f-131">Header</span></span><br/>  | <dl> <span data-ttu-id="ab71f-132"><dt>Wxutil. h (incluir streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab71f-132"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ab71f-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab71f-133">Library</span></span><br/> | <dl> <span data-ttu-id="ab71f-134"><dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt></span><span class="sxs-lookup"><span data-stu-id="ab71f-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab71f-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab71f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab71f-136">Objetos de sección crítica</span><span class="sxs-lookup"><span data-stu-id="ab71f-136">Critical Section Objects</span></span>](/windows/desktop/Sync/critical-section-objects)
</dt> <dt>

[<span data-ttu-id="ab71f-137">Referencia de clase base de DirectShow</span><span class="sxs-lookup"><span data-stu-id="ab71f-137">DirectShow Base Class Reference</span></span>](base-class-reference.md)
</dt> </dl>

 

