---
description: Windows incluye los siguientes elementos de programación nuevos para la sincronización.
ms.assetid: 16cd98d2-adc5-4a14-ad39-a0c5b4cc00cc
title: Novedades de la sincronización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4702ba10126d9c0eeeb85462195680b074918584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104276993"
---
# <a name="whats-new-in-synchronization"></a><span data-ttu-id="2207b-103">Novedades de la sincronización</span><span class="sxs-lookup"><span data-stu-id="2207b-103">What's New in Synchronization</span></span>

<span data-ttu-id="2207b-104">Windows incluye los siguientes elementos de programación nuevos para la sincronización.</span><span class="sxs-lookup"><span data-stu-id="2207b-104">Windows includes the following new programming elements for synchronization.</span></span>

## <a name="windows-8"></a><span data-ttu-id="2207b-105">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2207b-105">Windows 8</span></span>

### <a name="new-functions"></a><span data-ttu-id="2207b-106">Funciones nuevas</span><span class="sxs-lookup"><span data-stu-id="2207b-106">New Functions</span></span>

<dl> <dt>

[<span data-ttu-id="2207b-107">**DeleteSynchronizationBarrier**</span><span class="sxs-lookup"><span data-stu-id="2207b-107">**DeleteSynchronizationBarrier**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-deletesynchronizationbarrier)
</dt> <dd>

<span data-ttu-id="2207b-108">Elimina una barrera de sincronización.</span><span class="sxs-lookup"><span data-stu-id="2207b-108">Deletes a synchronization barrier.</span></span>

</dd> <dt>

[<span data-ttu-id="2207b-109">**EnterSynchronizationBarrier**</span><span class="sxs-lookup"><span data-stu-id="2207b-109">**EnterSynchronizationBarrier**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)
</dt> <dd>

<span data-ttu-id="2207b-110">Hace que el subproceso que realiza la llamada espere en una barrera de sincronización hasta que el número máximo de subprocesos haya entrado en la barrera.</span><span class="sxs-lookup"><span data-stu-id="2207b-110">Causes the calling thread to wait at a synchronization barrier until the maximum number of threads have entered the barrier.</span></span>

</dd> <dt>

[<span data-ttu-id="2207b-111">**GetOverlappedResultEx**</span><span class="sxs-lookup"><span data-stu-id="2207b-111">**GetOverlappedResultEx**</span></span>](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex)
</dt> <dd>

<span data-ttu-id="2207b-112">Recupera los resultados de una operación superpuesta en el archivo especificado, la canalización con nombre o el dispositivo de comunicaciones dentro del intervalo de tiempo de espera especificado.</span><span class="sxs-lookup"><span data-stu-id="2207b-112">Retrieves the results of an overlapped operation on the specified file, named pipe, or communications device within the specified time-out interval.</span></span> <span data-ttu-id="2207b-113">El subproceso que realiza la llamada puede realizar una espera de alerta.</span><span class="sxs-lookup"><span data-stu-id="2207b-113">The calling thread can perform an alertable wait.</span></span>

</dd> <dt>

[<span data-ttu-id="2207b-114">**InitializeSynchronizationBarrier**</span><span class="sxs-lookup"><span data-stu-id="2207b-114">**InitializeSynchronizationBarrier**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)
</dt> <dd>

<span data-ttu-id="2207b-115">Especifica el número máximo de subprocesos y el número de giros para una nueva barrera de sincronización.</span><span class="sxs-lookup"><span data-stu-id="2207b-115">Specifies the maximum number of threads and spin count for a new synchronization barrier.</span></span>

</dd> <dt>

[<span data-ttu-id="2207b-116">**WaitOnAddress**</span><span class="sxs-lookup"><span data-stu-id="2207b-116">**WaitOnAddress**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress)
</dt> <dd>

<span data-ttu-id="2207b-117">Espera a que cambie el valor de la dirección especificada.</span><span class="sxs-lookup"><span data-stu-id="2207b-117">Waits for the value at the specified address to change.</span></span>

</dd> <dt>

[<span data-ttu-id="2207b-118">**WakeByAddressAll**</span><span class="sxs-lookup"><span data-stu-id="2207b-118">**WakeByAddressAll**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddressall)
</dt> <dd>

<span data-ttu-id="2207b-119">Activa todos los subprocesos que están a la espera de que cambien el valor de una dirección.</span><span class="sxs-lookup"><span data-stu-id="2207b-119">Wakes all threads that are waiting for the value of an address to change.</span></span>

</dd> <dt>

[<span data-ttu-id="2207b-120">**WakeByAddressSingle**</span><span class="sxs-lookup"><span data-stu-id="2207b-120">**WakeByAddressSingle**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddresssingle)
</dt> <dd>

<span data-ttu-id="2207b-121">Activa un subproceso que está esperando a que cambie el valor de una dirección.</span><span class="sxs-lookup"><span data-stu-id="2207b-121">Wakes one thread that is waiting for the value of an address to change.</span></span>

</dd> </dl>

### <a name="new-interlocked-functions"></a><span data-ttu-id="2207b-122">Nuevas funciones interbloqueadas</span><span class="sxs-lookup"><span data-stu-id="2207b-122">New Interlocked Functions</span></span>

<dl> <dt>

<span data-ttu-id="2207b-123">[**InterlockedAddNoFence**](/previous-versions/windows/desktop/legacy/hh972629(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-123">[**InterlockedAddNoFence**](/previous-versions/windows/desktop/legacy/hh972629(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-124">Realiza una operación de suma atómica en los valores **Long** especificados.</span><span class="sxs-lookup"><span data-stu-id="2207b-124">Performs an atomic addition operation on the specified **LONG** values.</span></span> <span data-ttu-id="2207b-125">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-125">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-126">[**InterlockedAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972630(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-126">[**InterlockedAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972630(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-127">Realiza una operación de suma atómica en los valores de **LONGLONG** especificados.</span><span class="sxs-lookup"><span data-stu-id="2207b-127">Performs an atomic addition operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="2207b-128">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-128">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-129">[**InterlockedAndNoFence**](/previous-versions/windows/desktop/legacy/hh972634(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-129">[**InterlockedAndNoFence**](/previous-versions/windows/desktop/legacy/hh972634(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-130">Realiza una operación atómica y en los valores **largos** especificados.</span><span class="sxs-lookup"><span data-stu-id="2207b-130">Performs an atomic AND operation on the specified **LONG** values.</span></span> <span data-ttu-id="2207b-131">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-131">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-132">[**InterlockedAnd8NoFence**](/previous-versions/windows/desktop/legacy/hh972633(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-132">[**InterlockedAnd8NoFence**](/previous-versions/windows/desktop/legacy/hh972633(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-133">Realiza una operación atómica y en los valores de **carácter** especificados.</span><span class="sxs-lookup"><span data-stu-id="2207b-133">Performs an atomic AND operation on the specified **char** values.</span></span> <span data-ttu-id="2207b-134">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-134">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-135">[**InterlockedAnd16NoFence**](/previous-versions/windows/desktop/legacy/hh972631(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-135">[**InterlockedAnd16NoFence**](/previous-versions/windows/desktop/legacy/hh972631(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-136">Realiza una operación atómica y en los valores **cortos** especificados.</span><span class="sxs-lookup"><span data-stu-id="2207b-136">Performs an atomic AND operation on the specified **SHORT** values.</span></span> <span data-ttu-id="2207b-137">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-137">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-138">[**InterlockedAnd64NoFence**](/previous-versions/windows/desktop/legacy/hh972632(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-138">[**InterlockedAnd64NoFence**](/previous-versions/windows/desktop/legacy/hh972632(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-139">Realiza una operación atómica y en los valores de **LONGLONG** especificados.</span><span class="sxs-lookup"><span data-stu-id="2207b-139">Performs an atomic AND operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="2207b-140">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-140">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-141">[**InterlockedBitTestAndComplement64**](/previous-versions/windows/desktop/legacy/hh972635(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-141">[**InterlockedBitTestAndComplement64**](/previous-versions/windows/desktop/legacy/hh972635(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-142">Comprueba el bit especificado del valor de **LONG64** especificado y lo complementa.</span><span class="sxs-lookup"><span data-stu-id="2207b-142">Tests the specified bit of the specified **LONG64** value and complements it.</span></span> <span data-ttu-id="2207b-143">La operación es atómica.</span><span class="sxs-lookup"><span data-stu-id="2207b-143">The operation is atomic.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-144">[**InterlockedBitTestAndResetAcquire**](/previous-versions/windows/desktop/legacy/hh972636(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-144">[**InterlockedBitTestAndResetAcquire**](/previous-versions/windows/desktop/legacy/hh972636(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-145">Comprueba el bit especificado del valor **Long** especificado y lo establece en 0.</span><span class="sxs-lookup"><span data-stu-id="2207b-145">Tests the specified bit of the specified **LONG** value and sets it to 0.</span></span> <span data-ttu-id="2207b-146">La operación es atómica y se realiza con la adquisición de la semántica de ordenación de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-146">The operation is atomic, and it is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-147">[**InterlockedBitTestAndResetRelease**](/previous-versions/windows/desktop/legacy/hh972637(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-147">[**InterlockedBitTestAndResetRelease**](/previous-versions/windows/desktop/legacy/hh972637(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-148">Comprueba el bit especificado del valor **Long** especificado y lo establece en 0.</span><span class="sxs-lookup"><span data-stu-id="2207b-148">Tests the specified bit of the specified **LONG** value and sets it to 0.</span></span> <span data-ttu-id="2207b-149">La operación es atómica y se realiza mediante la semántica de liberación de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-149">The operation is atomic, and it is performed using memory release semantics.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-150">[**InterlockedBitTestAndSetAcquire**](/previous-versions/windows/desktop/legacy/hh972638(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-150">[**InterlockedBitTestAndSetAcquire**](/previous-versions/windows/desktop/legacy/hh972638(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-151">Comprueba el bit especificado del valor **Long** especificado y lo establece en 1.</span><span class="sxs-lookup"><span data-stu-id="2207b-151">Tests the specified bit of the specified **LONG** value and sets it to 1.</span></span> <span data-ttu-id="2207b-152">La operación es atómica y se realiza con la adquisición de la semántica de ordenación de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-152">The operation is atomic, and it is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-153">[**InterlockedBitTestAndSetRelease**](/previous-versions/windows/desktop/legacy/hh972639(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-153">[**InterlockedBitTestAndSetRelease**](/previous-versions/windows/desktop/legacy/hh972639(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-154">Comprueba el bit especificado del valor **Long** especificado y lo establece en 1.</span><span class="sxs-lookup"><span data-stu-id="2207b-154">Tests the specified bit of the specified **LONG** value and sets it to 1.</span></span> <span data-ttu-id="2207b-155">La operación es atómica y se realiza con la semántica de ordenación de memoria de la versión.</span><span class="sxs-lookup"><span data-stu-id="2207b-155">The operation is atomic, and it is performed with release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-156">[**InterlockedCompareExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972645(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-156">[**InterlockedCompareExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972645(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-157">Realiza una operación atómica de comparación e intercambio con los valores especificados.</span><span class="sxs-lookup"><span data-stu-id="2207b-157">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="2207b-158">La función compara dos valores de 32 bits especificados e intercambios con otro valor de 32 bits basado en el resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="2207b-158">The function compares two specified 32-bit values and exchanges with another 32-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="2207b-159">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-159">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="2207b-160">**InterlockedCompareExchange16**</span><span class="sxs-lookup"><span data-stu-id="2207b-160">**InterlockedCompareExchange16**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange16)
</dt> <dd>

<span data-ttu-id="2207b-161">Realiza una operación atómica de comparación e intercambio con los valores especificados.</span><span class="sxs-lookup"><span data-stu-id="2207b-161">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="2207b-162">La función compara dos valores de 16 bits especificados e intercambios con otro valor de 16 bits basado en el resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="2207b-162">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-163">[**InterlockedCompareExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972642(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-163">[**InterlockedCompareExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972642(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-164">Realiza una operación atómica de comparación e intercambio con los valores especificados.</span><span class="sxs-lookup"><span data-stu-id="2207b-164">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="2207b-165">La función compara dos valores de 16 bits especificados e intercambios con otro valor de 16 bits basado en el resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="2207b-165">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="2207b-166">La operación se realiza con la adquisición de la semántica de ordenación de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-166">The operation is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-167">[**InterlockedCompareExchange16Release**](/previous-versions/windows/desktop/legacy/hh972644(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-167">[**InterlockedCompareExchange16Release**](/previous-versions/windows/desktop/legacy/hh972644(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-168">Realiza una operación atómica de comparación e intercambio con los valores especificados.</span><span class="sxs-lookup"><span data-stu-id="2207b-168">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="2207b-169">La función compara dos valores de 16 bits especificados e intercambios con otro valor de 16 bits basado en el resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="2207b-169">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="2207b-170">El intercambio se realiza con la semántica de ordenación de memoria de la versión.</span><span class="sxs-lookup"><span data-stu-id="2207b-170">The exchange is performed with release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-171">[**InterlockedCompareExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972643(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-171">[**InterlockedCompareExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972643(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-172">Realiza una operación atómica de comparación e intercambio con los valores especificados.</span><span class="sxs-lookup"><span data-stu-id="2207b-172">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="2207b-173">La función compara dos valores de 16 bits especificados e intercambios con otro valor de 16 bits basado en el resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="2207b-173">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="2207b-174">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-174">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-175">[**InterlockedCompareExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972646(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-175">[**InterlockedCompareExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972646(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-176">Realiza una operación atómica de comparación e intercambio con los valores especificados.</span><span class="sxs-lookup"><span data-stu-id="2207b-176">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="2207b-177">La función compara dos valores de 64 bits especificados e intercambios con otro valor de 64 bits basado en el resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="2207b-177">The function compares two specified 64-bit values and exchanges with another 64-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="2207b-178">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-178">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="2207b-179">**InterlockedCompareExchange128**</span><span class="sxs-lookup"><span data-stu-id="2207b-179">**InterlockedCompareExchange128**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange128)
</dt> <dd>

<span data-ttu-id="2207b-180">Realiza una operación atómica de comparación e intercambio con los valores especificados.</span><span class="sxs-lookup"><span data-stu-id="2207b-180">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="2207b-181">La función compara dos valores de 128 bits especificados e intercambios con otro valor de 128 bits basado en el resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="2207b-181">The function compares two specified 128-bit values and exchanges with another 128-bit value based on the outcome of the comparison.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-182">[**InterlockedCompareExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972647(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-182">[**InterlockedCompareExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972647(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-183">Realiza una operación atómica de comparación e intercambio con los valores especificados.</span><span class="sxs-lookup"><span data-stu-id="2207b-183">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="2207b-184">La función compara dos valores de puntero especificados e intercambios con otro valor de puntero basado en el resultado de la comparación.</span><span class="sxs-lookup"><span data-stu-id="2207b-184">The function compares two specified pointer values and exchanges with another pointer value based on the outcome of the comparison.</span></span> <span data-ttu-id="2207b-185">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-185">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-186">[**InterlockedDecrementNoFence**](/previous-versions/windows/desktop/legacy/hh972652(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-186">[**InterlockedDecrementNoFence**](/previous-versions/windows/desktop/legacy/hh972652(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-187">Reduce (disminuye en uno) el valor de la variable especificada de 32 bits como una operación atómica.</span><span class="sxs-lookup"><span data-stu-id="2207b-187">Decrements (decreases by one) the value of the specified 32-bit variable as an atomic operation.</span></span> <span data-ttu-id="2207b-188">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-188">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="2207b-189">**InterlockedDecrement16**</span><span class="sxs-lookup"><span data-stu-id="2207b-189">**InterlockedDecrement16**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockeddecrement16)
</dt> <dd>

<span data-ttu-id="2207b-190">Reduce (disminuye en uno) el valor de la variable de 16 bits especificada como una operación atómica.</span><span class="sxs-lookup"><span data-stu-id="2207b-190">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-191">[**InterlockedDecrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972649(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-191">[**InterlockedDecrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972649(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-192">Reduce (disminuye en uno) el valor de la variable de 16 bits especificada como una operación atómica.</span><span class="sxs-lookup"><span data-stu-id="2207b-192">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="2207b-193">La operación se realiza con la adquisición de la semántica de ordenación de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-193">The operation is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-194">[**InterlockedDecrement16Release**](/previous-versions/windows/desktop/legacy/hh972651(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-194">[**InterlockedDecrement16Release**](/previous-versions/windows/desktop/legacy/hh972651(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-195">Reduce (disminuye en uno) el valor de la variable de 16 bits especificada como una operación atómica.</span><span class="sxs-lookup"><span data-stu-id="2207b-195">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="2207b-196">La operación se realiza con la semántica de ordenación de memoria de la versión.</span><span class="sxs-lookup"><span data-stu-id="2207b-196">The operation is performed with release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-197">[**InterlockedDecrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972650(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-197">[**InterlockedDecrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972650(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-198">Reduce (disminuye en uno) el valor de la variable de 16 bits especificada como una operación atómica.</span><span class="sxs-lookup"><span data-stu-id="2207b-198">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="2207b-199">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-199">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-200">[**InterlockedDecrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972653(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-200">[**InterlockedDecrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972653(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-201">Reduce (disminuye en uno) el valor de la variable especificada de 64 bits como una operación atómica.</span><span class="sxs-lookup"><span data-stu-id="2207b-201">Decrements (decreases by one) the value of the specified 64-bit variable as an atomic operation.</span></span> <span data-ttu-id="2207b-202">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-202">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-203">[**InterlockedExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-203">[**InterlockedExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972659(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-204">Establece una variable de 64 bits en el valor especificado como una operación atómica.</span><span class="sxs-lookup"><span data-stu-id="2207b-204">Sets a 64-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="2207b-205">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-205">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="2207b-206">**InterlockedExchange8**</span><span class="sxs-lookup"><span data-stu-id="2207b-206">**InterlockedExchange8**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedexchange8)
</dt> <dd>

<span data-ttu-id="2207b-207">Establece una variable de 8 bits en el valor especificado como una operación atómica.</span><span class="sxs-lookup"><span data-stu-id="2207b-207">Sets an 8-bit variable to the specified value as an atomic operation.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-208">[**InterlockedExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972654(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-208">[**InterlockedExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972654(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-209">Establece una variable de 16 bits en el valor especificado como una operación atómica.</span><span class="sxs-lookup"><span data-stu-id="2207b-209">Sets a 16-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="2207b-210">La operación se realiza utilizando la semántica de ordenación de memoria de adquisición.</span><span class="sxs-lookup"><span data-stu-id="2207b-210">The operation is performed using acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-211">[**InterlockedExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972655(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-211">[**InterlockedExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972655(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-212">Establece una variable de 16 bits en el valor especificado como una operación atómica.</span><span class="sxs-lookup"><span data-stu-id="2207b-212">Sets a 16-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="2207b-213">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-213">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-214">[**InterlockedExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972660(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-214">[**InterlockedExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972660(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-215">Establece una variable de 64 bits en el valor especificado como una operación atómica.</span><span class="sxs-lookup"><span data-stu-id="2207b-215">Sets a 64-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="2207b-216">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-216">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-217">[**InterlockedExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972661(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-217">[**InterlockedExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972661(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-218">Intercambia atómicamente un par de direcciones.</span><span class="sxs-lookup"><span data-stu-id="2207b-218">Atomically exchanges a pair of addresses.</span></span> <span data-ttu-id="2207b-219">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-219">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-220">[**InterlockedExchangeAddNoFence**](/previous-versions/windows/desktop/legacy/hh972657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-220">[**InterlockedExchangeAddNoFence**](/previous-versions/windows/desktop/legacy/hh972657(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-221">Realiza una adición atómica de valores de 2 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2207b-221">Performs an atomic addition of two 32-bit values.</span></span> <span data-ttu-id="2207b-222">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-222">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-223">[**InterlockedExchangeAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972658(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-223">[**InterlockedExchangeAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972658(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-224">Realiza una adición atómica de valores de 2 64 bits.</span><span class="sxs-lookup"><span data-stu-id="2207b-224">Performs an atomic addition of two 64-bit values.</span></span> <span data-ttu-id="2207b-225">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-225">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-226">[**InterlockedIncrementNoFence**](/previous-versions/windows/desktop/legacy/hh972667(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-226">[**InterlockedIncrementNoFence**](/previous-versions/windows/desktop/legacy/hh972667(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-227">Incrementos (aumenta en uno) el valor de la variable especificada de 32 bits como una operación atómica.</span><span class="sxs-lookup"><span data-stu-id="2207b-227">Increments (increases by one) the value of the specified 32-bit variable as an atomic operation.</span></span> <span data-ttu-id="2207b-228">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-228">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="2207b-229">**InterlockedIncrement16**</span><span class="sxs-lookup"><span data-stu-id="2207b-229">**InterlockedIncrement16**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedincrement16)
</dt> <dd>

<span data-ttu-id="2207b-230">Incrementos (aumenta en uno) el valor de la variable de 16 bits especificada como una operación atómica.</span><span class="sxs-lookup"><span data-stu-id="2207b-230">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-231">[**InterlockedIncrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972663(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-231">[**InterlockedIncrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972663(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-232">Incrementos (aumenta en uno) el valor de la variable de 16 bits especificada como una operación atómica.</span><span class="sxs-lookup"><span data-stu-id="2207b-232">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="2207b-233">La operación se realiza utilizando la semántica de ordenación de memoria de adquisición.</span><span class="sxs-lookup"><span data-stu-id="2207b-233">The operation is performed using acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-234">[**InterlockedIncrement16Release**](/previous-versions/windows/desktop/legacy/hh972665(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-234">[**InterlockedIncrement16Release**](/previous-versions/windows/desktop/legacy/hh972665(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-235">Incrementos (aumenta en uno) el valor de la variable de 16 bits especificada como una operación atómica.</span><span class="sxs-lookup"><span data-stu-id="2207b-235">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="2207b-236">La operación se realiza mediante la semántica de ordenación de memoria de la versión.</span><span class="sxs-lookup"><span data-stu-id="2207b-236">The operation is performed using release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-237">[**InterlockedIncrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972664(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-237">[**InterlockedIncrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972664(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-238">Incrementos (aumenta en uno) el valor de la variable de 16 bits especificada como una operación atómica.</span><span class="sxs-lookup"><span data-stu-id="2207b-238">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="2207b-239">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-239">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-240">[**InterlockedIncrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972668(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-240">[**InterlockedIncrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972668(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-241">Incrementos (aumenta en uno) el valor de la variable especificada de 64 bits como una operación atómica.</span><span class="sxs-lookup"><span data-stu-id="2207b-241">Increments (increases by one) the value of the specified 64-bit variable as an atomic operation.</span></span> <span data-ttu-id="2207b-242">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-242">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-243">[**InterlockedOrNoFence**](/previous-versions/windows/desktop/legacy/hh972672(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-243">[**InterlockedOrNoFence**](/previous-versions/windows/desktop/legacy/hh972672(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-244">Realiza una operación atómica o en los valores **largos** especificados.</span><span class="sxs-lookup"><span data-stu-id="2207b-244">Performs an atomic OR operation on the specified **LONG** values.</span></span> <span data-ttu-id="2207b-245">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-245">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-246">[**InterlockedOr8NoFence**](/previous-versions/windows/desktop/legacy/hh972671(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-246">[**InterlockedOr8NoFence**](/previous-versions/windows/desktop/legacy/hh972671(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-247">Realiza una operación atómica o en los valores de **carácter** especificados.</span><span class="sxs-lookup"><span data-stu-id="2207b-247">Performs an atomic OR operation on the specified **char** values.</span></span> <span data-ttu-id="2207b-248">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-248">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-249">[**InterlockedOr16NoFence**](/previous-versions/windows/desktop/legacy/hh972669(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-249">[**InterlockedOr16NoFence**](/previous-versions/windows/desktop/legacy/hh972669(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-250">Realiza una operación atómica o en los valores **cortos** especificados.</span><span class="sxs-lookup"><span data-stu-id="2207b-250">Performs an atomic OR operation on the specified **SHORT** values.</span></span> <span data-ttu-id="2207b-251">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-251">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-252">[**InterlockedOr64NoFence**](/previous-versions/windows/desktop/legacy/hh972670(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-252">[**InterlockedOr64NoFence**](/previous-versions/windows/desktop/legacy/hh972670(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-253">Realiza una operación atómica o en los valores de **LONGLONG** especificados.</span><span class="sxs-lookup"><span data-stu-id="2207b-253">Performs an atomic OR operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="2207b-254">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-254">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="2207b-255">**InterlockedPushListSListEx**</span><span class="sxs-lookup"><span data-stu-id="2207b-255">**InterlockedPushListSListEx**</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)
</dt> <dd>

<span data-ttu-id="2207b-256">Inserta una lista vinculada individualmente en la parte frontal de otra lista vinculada de forma individual.</span><span class="sxs-lookup"><span data-stu-id="2207b-256">Inserts a singly-linked list at the front of another singly linked list.</span></span> <span data-ttu-id="2207b-257">El acceso a las listas se sincroniza en un sistema con varios procesadores.</span><span class="sxs-lookup"><span data-stu-id="2207b-257">Access to the lists is synchronized on a multiprocessor system.</span></span> <span data-ttu-id="2207b-258">Esta versión del método no usa la Convención de llamada [ \_ \_ fastcall](https://msdn.microsoft.com/library/6xa169sk(v=VS.71).aspx) .</span><span class="sxs-lookup"><span data-stu-id="2207b-258">This version of the method does not use the [\_\_fastcall](https://msdn.microsoft.com/library/6xa169sk(v=VS.71).aspx) calling convention.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-259">[**InterlockedXorNoFence**](/previous-versions/windows/desktop/legacy/hh972677(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-259">[**InterlockedXorNoFence**](/previous-versions/windows/desktop/legacy/hh972677(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-260">Realiza una operación XOR atómica en los valores **Long** especificados.</span><span class="sxs-lookup"><span data-stu-id="2207b-260">Performs an atomic XOR operation on the specified **LONG** values.</span></span> <span data-ttu-id="2207b-261">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-261">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-262">[**InterlockedXor8NoFence**](/previous-versions/windows/desktop/legacy/hh972676(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-262">[**InterlockedXor8NoFence**](/previous-versions/windows/desktop/legacy/hh972676(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-263">Realiza una operación XOR atómica en los valores de **carácter** especificados.</span><span class="sxs-lookup"><span data-stu-id="2207b-263">Performs an atomic XOR operation on the specified **char** values.</span></span> <span data-ttu-id="2207b-264">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-264">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-265">[**InterlockedXor16NoFence**](/previous-versions/windows/desktop/legacy/hh972674(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-265">[**InterlockedXor16NoFence**](/previous-versions/windows/desktop/legacy/hh972674(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-266">Realiza una operación XOR atómica en los valores **cortos** especificados.</span><span class="sxs-lookup"><span data-stu-id="2207b-266">Performs an atomic XOR operation on the specified **SHORT** values.</span></span> <span data-ttu-id="2207b-267">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-267">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="2207b-268">[**InterlockedXor64NoFence**](/previous-versions/windows/desktop/legacy/hh972675(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2207b-268">[**InterlockedXor64NoFence**](/previous-versions/windows/desktop/legacy/hh972675(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="2207b-269">Realiza una operación XOR atómica en los valores de **LONGLONG** especificados.</span><span class="sxs-lookup"><span data-stu-id="2207b-269">Performs an atomic XOR operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="2207b-270">La operación se realiza de forma atómica, pero sin usar barreras de memoria.</span><span class="sxs-lookup"><span data-stu-id="2207b-270">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> </dl>

## <a name="windows-7"></a><span data-ttu-id="2207b-271">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2207b-271">Windows 7</span></span>

### <a name="new-functions"></a><span data-ttu-id="2207b-272">Funciones nuevas</span><span class="sxs-lookup"><span data-stu-id="2207b-272">New Functions</span></span>

<dl> <dt>

[<span data-ttu-id="2207b-273">**SetWaitableTimerEx**</span><span class="sxs-lookup"><span data-stu-id="2207b-273">**SetWaitableTimerEx**</span></span>](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)
</dt> <dd>

<span data-ttu-id="2207b-274">Activa el temporizador de espera especificado y proporciona información de contexto para el temporizador.</span><span class="sxs-lookup"><span data-stu-id="2207b-274">Activates the specified waitable timer and provides context information for the timer.</span></span>

</dd> <dt>

[<span data-ttu-id="2207b-275">**TryAcquireSRWLockExclusive**</span><span class="sxs-lookup"><span data-stu-id="2207b-275">**TryAcquireSRWLockExclusive**</span></span>](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive)
</dt> <dd>

<span data-ttu-id="2207b-276">Intenta adquirir un bloqueo delgado de lector/escritor (SRW) en modo exclusivo.</span><span class="sxs-lookup"><span data-stu-id="2207b-276">Attempts to acquire a slim reader/writer (SRW) lock in exclusive mode.</span></span> <span data-ttu-id="2207b-277">Si la llamada se realiza correctamente, el subproceso que realiza la llamada toma la propiedad del bloqueo.</span><span class="sxs-lookup"><span data-stu-id="2207b-277">If the call is successful, the calling thread takes ownership of the lock.</span></span>

</dd> <dt>

[<span data-ttu-id="2207b-278">**TryAcquireSRWLockShared**</span><span class="sxs-lookup"><span data-stu-id="2207b-278">**TryAcquireSRWLockShared**</span></span>](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockshared)
</dt> <dd>

<span data-ttu-id="2207b-279">Intenta adquirir un bloqueo delgado de lector/escritor (SRW) en modo compartido.</span><span class="sxs-lookup"><span data-stu-id="2207b-279">Attempts to acquire a slim reader/writer (SRW) lock in shared mode.</span></span> <span data-ttu-id="2207b-280">Si la llamada se realiza correctamente, el subproceso que realiza la llamada toma la propiedad del bloqueo.</span><span class="sxs-lookup"><span data-stu-id="2207b-280">If the call is successful, the calling thread takes ownership of the lock.</span></span>

</dd> </dl>

### <a name="new-structures"></a><span data-ttu-id="2207b-281">Nuevas estructuras</span><span class="sxs-lookup"><span data-stu-id="2207b-281">New Structures</span></span>

<dl> <dt>

[<span data-ttu-id="2207b-282">**contexto de motivo \_**</span><span class="sxs-lookup"><span data-stu-id="2207b-282">**REASON\_CONTEXT**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-reason_context)
</dt> <dd>

<span data-ttu-id="2207b-283">Contiene información de contexto para un temporizador activado con [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex).</span><span class="sxs-lookup"><span data-stu-id="2207b-283">Contains context information for a timer activated with [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex).</span></span>

</dd> </dl>

 

 
