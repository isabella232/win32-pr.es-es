---
description: Esta clase es la clase de tipo de evento para los eventos de cambio de contexto. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 3f9f84d0-18a9-493c-b104-8236b2bd8404
title: Clase CSwitch
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSwitch
- CSwitch.NewThreadId
- CSwitch.OldThreadId
- CSwitch.NewThreadPriority
- CSwitch.OldThreadPriority
- CSwitch.PreviousCState
- CSwitch.SpareByte
- CSwitch.OldThreadWaitReason
- CSwitch.OldThreadWaitMode
- CSwitch.OldThreadState
- CSwitch.OldThreadWaitIdealProcessor
- CSwitch.NewThreadWaitTime
- CSwitch.Reserved
api_type:
- NA
api_location: ''
ms.openlocfilehash: 91004ca276140271e8d73c3fc226e83c4e03d1fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275673"
---
# <a name="cswitch-class"></a><span data-ttu-id="27c5e-104">Clase CSwitch</span><span class="sxs-lookup"><span data-stu-id="27c5e-104">CSwitch class</span></span>

<span data-ttu-id="27c5e-105">Esta clase es la clase de tipo de evento para los eventos de cambio de contexto.</span><span class="sxs-lookup"><span data-stu-id="27c5e-105">This class is the event type class for context switch events.</span></span>

<span data-ttu-id="27c5e-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="27c5e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="27c5e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27c5e-107">Syntax</span></span>

``` syntax
[EventType{36}, EventTypeName{"CSwitch"}]
class CSwitch : Thread_V2
{
  uint32 NewThreadId;
  uint32 OldThreadId;
  sint8  NewThreadPriority;
  sint8  OldThreadPriority;
  uint8  PreviousCState;
  sint8  SpareByte;
  sint8  OldThreadWaitReason;
  sint8  OldThreadWaitMode;
  sint8  OldThreadState;
  sint8  OldThreadWaitIdealProcessor;
  uint32 NewThreadWaitTime;
  uint32 Reserved;
};
```

## <a name="members"></a><span data-ttu-id="27c5e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="27c5e-108">Members</span></span>

<span data-ttu-id="27c5e-109">La clase **CSwitch** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="27c5e-109">The **CSwitch** class has these types of members:</span></span>

-   [<span data-ttu-id="27c5e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="27c5e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="27c5e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="27c5e-111">Properties</span></span>

<span data-ttu-id="27c5e-112">La clase **CSwitch** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="27c5e-112">The **CSwitch** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="27c5e-113">**NewThreadId**</span><span class="sxs-lookup"><span data-stu-id="27c5e-113">**NewThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c5e-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27c5e-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27c5e-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27c5e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27c5e-116">Calificadores: WmiDataId (1), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="27c5e-116">Qualifiers: WmiDataId(1), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="27c5e-117">Nuevo identificador de subproceso después del modificador.</span><span class="sxs-lookup"><span data-stu-id="27c5e-117">New thread ID after the switch.</span></span>

</dd> <dt>

<span data-ttu-id="27c5e-118">**NewThreadPriority**</span><span class="sxs-lookup"><span data-stu-id="27c5e-118">**NewThreadPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c5e-119">Tipo de datos: **sint8**</span><span class="sxs-lookup"><span data-stu-id="27c5e-119">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="27c5e-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27c5e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27c5e-121">Calificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="27c5e-121">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="27c5e-122">Prioridad del subproceso nuevo.</span><span class="sxs-lookup"><span data-stu-id="27c5e-122">Thread priority of the new thread.</span></span>

</dd> <dt>

<span data-ttu-id="27c5e-123">**NewThreadWaitTime**</span><span class="sxs-lookup"><span data-stu-id="27c5e-123">**NewThreadWaitTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c5e-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27c5e-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27c5e-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27c5e-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27c5e-126">Calificadores: WmiDataId (11), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="27c5e-126">Qualifiers: WmiDataId(11), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="27c5e-127">Tiempo de espera para el nuevo subproceso.</span><span class="sxs-lookup"><span data-stu-id="27c5e-127">Wait time for the new thread.</span></span>

</dd> <dt>

<span data-ttu-id="27c5e-128">**OldThreadId**</span><span class="sxs-lookup"><span data-stu-id="27c5e-128">**OldThreadId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c5e-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27c5e-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27c5e-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27c5e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27c5e-131">Calificadores: WmiDataId (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="27c5e-131">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="27c5e-132">IDENTIFICADOR de subproceso anterior.</span><span class="sxs-lookup"><span data-stu-id="27c5e-132">Previous thread ID.</span></span>

</dd> <dt>

<span data-ttu-id="27c5e-133">**OldThreadPriority**</span><span class="sxs-lookup"><span data-stu-id="27c5e-133">**OldThreadPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c5e-134">Tipo de datos: **sint8**</span><span class="sxs-lookup"><span data-stu-id="27c5e-134">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="27c5e-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27c5e-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27c5e-136">Calificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="27c5e-136">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="27c5e-137">Prioridad de subproceso del subproceso anterior.</span><span class="sxs-lookup"><span data-stu-id="27c5e-137">Thread priority of the previous thread.</span></span>

</dd> <dt>

<span data-ttu-id="27c5e-138">**OldThreadState**</span><span class="sxs-lookup"><span data-stu-id="27c5e-138">**OldThreadState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c5e-139">Tipo de datos: **sint8**</span><span class="sxs-lookup"><span data-stu-id="27c5e-139">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="27c5e-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27c5e-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27c5e-141">Calificadores: WmiDataId (9)</span><span class="sxs-lookup"><span data-stu-id="27c5e-141">Qualifiers: WmiDataId(9)</span></span>
</dt> </dl>

<span data-ttu-id="27c5e-142">Estado del subproceso anterior.</span><span class="sxs-lookup"><span data-stu-id="27c5e-142">State of the previous thread.</span></span> <span data-ttu-id="27c5e-143">A continuación se muestran los posibles valores de estado:</span><span class="sxs-lookup"><span data-stu-id="27c5e-143">The following are the possible state values:</span></span>

| <span data-ttu-id="27c5e-144">Estado</span><span class="sxs-lookup"><span data-stu-id="27c5e-144">State</span></span> | <span data-ttu-id="27c5e-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="27c5e-145">Description</span></span>                                   |
|-------|-----------------------------------------------|
| <span data-ttu-id="27c5e-146">0</span><span class="sxs-lookup"><span data-stu-id="27c5e-146">0</span></span>     | <span data-ttu-id="27c5e-147">Inicializado</span><span class="sxs-lookup"><span data-stu-id="27c5e-147">Initialized</span></span>                                   |
| <span data-ttu-id="27c5e-148">1</span><span class="sxs-lookup"><span data-stu-id="27c5e-148">1</span></span>     | <span data-ttu-id="27c5e-149">Ready</span><span class="sxs-lookup"><span data-stu-id="27c5e-149">Ready</span></span>                                         |
| <span data-ttu-id="27c5e-150">2</span><span class="sxs-lookup"><span data-stu-id="27c5e-150">2</span></span>     | <span data-ttu-id="27c5e-151">En ejecución</span><span class="sxs-lookup"><span data-stu-id="27c5e-151">Running</span></span>                                       |
| <span data-ttu-id="27c5e-152">3</span><span class="sxs-lookup"><span data-stu-id="27c5e-152">3</span></span>     | <span data-ttu-id="27c5e-153">Standby</span><span class="sxs-lookup"><span data-stu-id="27c5e-153">Standby</span></span>                                       |
| <span data-ttu-id="27c5e-154">4</span><span class="sxs-lookup"><span data-stu-id="27c5e-154">4</span></span>     | <span data-ttu-id="27c5e-155">Finalizado</span><span class="sxs-lookup"><span data-stu-id="27c5e-155">Terminated</span></span>                                    |
| <span data-ttu-id="27c5e-156">5</span><span class="sxs-lookup"><span data-stu-id="27c5e-156">5</span></span>     | <span data-ttu-id="27c5e-157">En espera</span><span class="sxs-lookup"><span data-stu-id="27c5e-157">Waiting</span></span>                                       |
| <span data-ttu-id="27c5e-158">6</span><span class="sxs-lookup"><span data-stu-id="27c5e-158">6</span></span>     | <span data-ttu-id="27c5e-159">Transición</span><span class="sxs-lookup"><span data-stu-id="27c5e-159">Transition</span></span>                                    |
| <span data-ttu-id="27c5e-160">7</span><span class="sxs-lookup"><span data-stu-id="27c5e-160">7</span></span>     | <span data-ttu-id="27c5e-161">DeferredReady (agregado para Windows Server 2003)</span><span class="sxs-lookup"><span data-stu-id="27c5e-161">DeferredReady (added for Windows Server 2003)</span></span> |



 

</dd> <dt>

<span data-ttu-id="27c5e-162">**OldThreadWaitIdealProcessor**</span><span class="sxs-lookup"><span data-stu-id="27c5e-162">**OldThreadWaitIdealProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c5e-163">Tipo de datos: **sint8**</span><span class="sxs-lookup"><span data-stu-id="27c5e-163">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="27c5e-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27c5e-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27c5e-165">Calificadores: WmiDataId (10), formato ("x")</span><span class="sxs-lookup"><span data-stu-id="27c5e-165">Qualifiers: WmiDataId(10), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="27c5e-166">Tiempo de espera ideal del subproceso anterior.</span><span class="sxs-lookup"><span data-stu-id="27c5e-166">Ideal wait time of the previous thread.</span></span>

</dd> <dt>

<span data-ttu-id="27c5e-167">**OldThreadWaitMode**</span><span class="sxs-lookup"><span data-stu-id="27c5e-167">**OldThreadWaitMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c5e-168">Tipo de datos: **sint8**</span><span class="sxs-lookup"><span data-stu-id="27c5e-168">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="27c5e-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27c5e-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27c5e-170">Calificadores: WmiDataId (8)</span><span class="sxs-lookup"><span data-stu-id="27c5e-170">Qualifiers: WmiDataId(8)</span></span>
</dt> </dl>

<span data-ttu-id="27c5e-171">Modo de espera del subproceso anterior.</span><span class="sxs-lookup"><span data-stu-id="27c5e-171">Wait mode for the previous thread.</span></span> <span data-ttu-id="27c5e-172">Los posibles valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="27c5e-172">The following are the possible values:</span></span>

| <span data-ttu-id="27c5e-173">Estado</span><span class="sxs-lookup"><span data-stu-id="27c5e-173">State</span></span> | <span data-ttu-id="27c5e-174">Descripción</span><span class="sxs-lookup"><span data-stu-id="27c5e-174">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="27c5e-175">0</span><span class="sxs-lookup"><span data-stu-id="27c5e-175">0</span></span>     | <span data-ttu-id="27c5e-176">KernelMode</span><span class="sxs-lookup"><span data-stu-id="27c5e-176">KernelMode</span></span>  |
| <span data-ttu-id="27c5e-177">1</span><span class="sxs-lookup"><span data-stu-id="27c5e-177">1</span></span>     | <span data-ttu-id="27c5e-178">En modo usuario</span><span class="sxs-lookup"><span data-stu-id="27c5e-178">UserMode</span></span>    |



 

</dd> <dt>

<span data-ttu-id="27c5e-179">**OldThreadWaitReason**</span><span class="sxs-lookup"><span data-stu-id="27c5e-179">**OldThreadWaitReason**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c5e-180">Tipo de datos: **sint8**</span><span class="sxs-lookup"><span data-stu-id="27c5e-180">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="27c5e-181">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27c5e-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27c5e-182">Calificadores: WmiDataId (7)</span><span class="sxs-lookup"><span data-stu-id="27c5e-182">Qualifiers: WmiDataId(7)</span></span>
</dt> </dl>

<span data-ttu-id="27c5e-183">Razón de espera del subproceso anterior.</span><span class="sxs-lookup"><span data-stu-id="27c5e-183">Wait reason for the previous thread.</span></span> <span data-ttu-id="27c5e-184">Los posibles valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="27c5e-184">The following are the possible values:</span></span>

| <span data-ttu-id="27c5e-185">Estado</span><span class="sxs-lookup"><span data-stu-id="27c5e-185">State</span></span> | <span data-ttu-id="27c5e-186">Descripción</span><span class="sxs-lookup"><span data-stu-id="27c5e-186">Description</span></span>       |
|-------|-------------------|
| <span data-ttu-id="27c5e-187">0</span><span class="sxs-lookup"><span data-stu-id="27c5e-187">0</span></span>     | <span data-ttu-id="27c5e-188">Ejecutivo</span><span class="sxs-lookup"><span data-stu-id="27c5e-188">Executive</span></span>         |
| <span data-ttu-id="27c5e-189">1</span><span class="sxs-lookup"><span data-stu-id="27c5e-189">1</span></span>     | <span data-ttu-id="27c5e-190">FreePage</span><span class="sxs-lookup"><span data-stu-id="27c5e-190">FreePage</span></span>          |
| <span data-ttu-id="27c5e-191">2</span><span class="sxs-lookup"><span data-stu-id="27c5e-191">2</span></span>     | <span data-ttu-id="27c5e-192">Pagein.</span><span class="sxs-lookup"><span data-stu-id="27c5e-192">PageIn</span></span>            |
| <span data-ttu-id="27c5e-193">3</span><span class="sxs-lookup"><span data-stu-id="27c5e-193">3</span></span>     | <span data-ttu-id="27c5e-194">PoolAllocation</span><span class="sxs-lookup"><span data-stu-id="27c5e-194">PoolAllocation</span></span>    |
| <span data-ttu-id="27c5e-195">4</span><span class="sxs-lookup"><span data-stu-id="27c5e-195">4</span></span>     | <span data-ttu-id="27c5e-196">DelayExecution</span><span class="sxs-lookup"><span data-stu-id="27c5e-196">DelayExecution</span></span>    |
| <span data-ttu-id="27c5e-197">5</span><span class="sxs-lookup"><span data-stu-id="27c5e-197">5</span></span>     | <span data-ttu-id="27c5e-198">Suspended</span><span class="sxs-lookup"><span data-stu-id="27c5e-198">Suspended</span></span>         |
| <span data-ttu-id="27c5e-199">6</span><span class="sxs-lookup"><span data-stu-id="27c5e-199">6</span></span>     | <span data-ttu-id="27c5e-200">UserRequest</span><span class="sxs-lookup"><span data-stu-id="27c5e-200">UserRequest</span></span>       |
| <span data-ttu-id="27c5e-201">7</span><span class="sxs-lookup"><span data-stu-id="27c5e-201">7</span></span>     | <span data-ttu-id="27c5e-202">WrExecutive</span><span class="sxs-lookup"><span data-stu-id="27c5e-202">WrExecutive</span></span>       |
| <span data-ttu-id="27c5e-203">8</span><span class="sxs-lookup"><span data-stu-id="27c5e-203">8</span></span>     | <span data-ttu-id="27c5e-204">WrFreePage</span><span class="sxs-lookup"><span data-stu-id="27c5e-204">WrFreePage</span></span>        |
| <span data-ttu-id="27c5e-205">9</span><span class="sxs-lookup"><span data-stu-id="27c5e-205">9</span></span>     | <span data-ttu-id="27c5e-206">WrPageIn</span><span class="sxs-lookup"><span data-stu-id="27c5e-206">WrPageIn</span></span>          |
| <span data-ttu-id="27c5e-207">10</span><span class="sxs-lookup"><span data-stu-id="27c5e-207">10</span></span>    | <span data-ttu-id="27c5e-208">WrPoolAllocation</span><span class="sxs-lookup"><span data-stu-id="27c5e-208">WrPoolAllocation</span></span>  |
| <span data-ttu-id="27c5e-209">11</span><span class="sxs-lookup"><span data-stu-id="27c5e-209">11</span></span>    | <span data-ttu-id="27c5e-210">WrDelayExecution</span><span class="sxs-lookup"><span data-stu-id="27c5e-210">WrDelayExecution</span></span>  |
| <span data-ttu-id="27c5e-211">12</span><span class="sxs-lookup"><span data-stu-id="27c5e-211">12</span></span>    | <span data-ttu-id="27c5e-212">WrSuspended</span><span class="sxs-lookup"><span data-stu-id="27c5e-212">WrSuspended</span></span>       |
| <span data-ttu-id="27c5e-213">13</span><span class="sxs-lookup"><span data-stu-id="27c5e-213">13</span></span>    | <span data-ttu-id="27c5e-214">WrUserRequest</span><span class="sxs-lookup"><span data-stu-id="27c5e-214">WrUserRequest</span></span>     |
| <span data-ttu-id="27c5e-215">14</span><span class="sxs-lookup"><span data-stu-id="27c5e-215">14</span></span>    | <span data-ttu-id="27c5e-216">WrEventPair</span><span class="sxs-lookup"><span data-stu-id="27c5e-216">WrEventPair</span></span>       |
| <span data-ttu-id="27c5e-217">15</span><span class="sxs-lookup"><span data-stu-id="27c5e-217">15</span></span>    | <span data-ttu-id="27c5e-218">WrQueue</span><span class="sxs-lookup"><span data-stu-id="27c5e-218">WrQueue</span></span>           |
| <span data-ttu-id="27c5e-219">16</span><span class="sxs-lookup"><span data-stu-id="27c5e-219">16</span></span>    | <span data-ttu-id="27c5e-220">WrLpcReceive</span><span class="sxs-lookup"><span data-stu-id="27c5e-220">WrLpcReceive</span></span>      |
| <span data-ttu-id="27c5e-221">17</span><span class="sxs-lookup"><span data-stu-id="27c5e-221">17</span></span>    | <span data-ttu-id="27c5e-222">WrLpcReply</span><span class="sxs-lookup"><span data-stu-id="27c5e-222">WrLpcReply</span></span>        |
| <span data-ttu-id="27c5e-223">18</span><span class="sxs-lookup"><span data-stu-id="27c5e-223">18</span></span>    | <span data-ttu-id="27c5e-224">WrVirtualMemory</span><span class="sxs-lookup"><span data-stu-id="27c5e-224">WrVirtualMemory</span></span>   |
| <span data-ttu-id="27c5e-225">19</span><span class="sxs-lookup"><span data-stu-id="27c5e-225">19</span></span>    | <span data-ttu-id="27c5e-226">WrPageOut</span><span class="sxs-lookup"><span data-stu-id="27c5e-226">WrPageOut</span></span>         |
| <span data-ttu-id="27c5e-227">20</span><span class="sxs-lookup"><span data-stu-id="27c5e-227">20</span></span>    | <span data-ttu-id="27c5e-228">WrRendezvous</span><span class="sxs-lookup"><span data-stu-id="27c5e-228">WrRendezvous</span></span>      |
| <span data-ttu-id="27c5e-229">21</span><span class="sxs-lookup"><span data-stu-id="27c5e-229">21</span></span>    | <span data-ttu-id="27c5e-230">WrKeyedEvent</span><span class="sxs-lookup"><span data-stu-id="27c5e-230">WrKeyedEvent</span></span>      |
| <span data-ttu-id="27c5e-231">22</span><span class="sxs-lookup"><span data-stu-id="27c5e-231">22</span></span>    | <span data-ttu-id="27c5e-232">WrTerminated</span><span class="sxs-lookup"><span data-stu-id="27c5e-232">WrTerminated</span></span>      |
| <span data-ttu-id="27c5e-233">23</span><span class="sxs-lookup"><span data-stu-id="27c5e-233">23</span></span>    | <span data-ttu-id="27c5e-234">WrProcessInSwap</span><span class="sxs-lookup"><span data-stu-id="27c5e-234">WrProcessInSwap</span></span>   |
| <span data-ttu-id="27c5e-235">24</span><span class="sxs-lookup"><span data-stu-id="27c5e-235">24</span></span>    | <span data-ttu-id="27c5e-236">WrCpuRateControl</span><span class="sxs-lookup"><span data-stu-id="27c5e-236">WrCpuRateControl</span></span>  |
| <span data-ttu-id="27c5e-237">25</span><span class="sxs-lookup"><span data-stu-id="27c5e-237">25</span></span>    | <span data-ttu-id="27c5e-238">WrCalloutStack</span><span class="sxs-lookup"><span data-stu-id="27c5e-238">WrCalloutStack</span></span>    |
| <span data-ttu-id="27c5e-239">26</span><span class="sxs-lookup"><span data-stu-id="27c5e-239">26</span></span>    | <span data-ttu-id="27c5e-240">WrKernel</span><span class="sxs-lookup"><span data-stu-id="27c5e-240">WrKernel</span></span>          |
| <span data-ttu-id="27c5e-241">27</span><span class="sxs-lookup"><span data-stu-id="27c5e-241">27</span></span>    | <span data-ttu-id="27c5e-242">WrResource</span><span class="sxs-lookup"><span data-stu-id="27c5e-242">WrResource</span></span>        |
| <span data-ttu-id="27c5e-243">28</span><span class="sxs-lookup"><span data-stu-id="27c5e-243">28</span></span>    | <span data-ttu-id="27c5e-244">WrPushLock</span><span class="sxs-lookup"><span data-stu-id="27c5e-244">WrPushLock</span></span>        |
| <span data-ttu-id="27c5e-245">29</span><span class="sxs-lookup"><span data-stu-id="27c5e-245">29</span></span>    | <span data-ttu-id="27c5e-246">WrMutex</span><span class="sxs-lookup"><span data-stu-id="27c5e-246">WrMutex</span></span>           |
| <span data-ttu-id="27c5e-247">30</span><span class="sxs-lookup"><span data-stu-id="27c5e-247">30</span></span>    | <span data-ttu-id="27c5e-248">WrQuantumEnd</span><span class="sxs-lookup"><span data-stu-id="27c5e-248">WrQuantumEnd</span></span>      |
| <span data-ttu-id="27c5e-249">31</span><span class="sxs-lookup"><span data-stu-id="27c5e-249">31</span></span>    | <span data-ttu-id="27c5e-250">WrDispatchInt</span><span class="sxs-lookup"><span data-stu-id="27c5e-250">WrDispatchInt</span></span>     |
| <span data-ttu-id="27c5e-251">32</span><span class="sxs-lookup"><span data-stu-id="27c5e-251">32</span></span>    | <span data-ttu-id="27c5e-252">WrPreempted</span><span class="sxs-lookup"><span data-stu-id="27c5e-252">WrPreempted</span></span>       |
| <span data-ttu-id="27c5e-253">33</span><span class="sxs-lookup"><span data-stu-id="27c5e-253">33</span></span>    | <span data-ttu-id="27c5e-254">WrYieldExecution</span><span class="sxs-lookup"><span data-stu-id="27c5e-254">WrYieldExecution</span></span>  |
| <span data-ttu-id="27c5e-255">34</span><span class="sxs-lookup"><span data-stu-id="27c5e-255">34</span></span>    | <span data-ttu-id="27c5e-256">WrFastMutex</span><span class="sxs-lookup"><span data-stu-id="27c5e-256">WrFastMutex</span></span>       |
| <span data-ttu-id="27c5e-257">35</span><span class="sxs-lookup"><span data-stu-id="27c5e-257">35</span></span>    | <span data-ttu-id="27c5e-258">WrGuardedMutex</span><span class="sxs-lookup"><span data-stu-id="27c5e-258">WrGuardedMutex</span></span>    |
| <span data-ttu-id="27c5e-259">36</span><span class="sxs-lookup"><span data-stu-id="27c5e-259">36</span></span>    | <span data-ttu-id="27c5e-260">WrRundown</span><span class="sxs-lookup"><span data-stu-id="27c5e-260">WrRundown</span></span>         |
| <span data-ttu-id="27c5e-261">37</span><span class="sxs-lookup"><span data-stu-id="27c5e-261">37</span></span>    | <span data-ttu-id="27c5e-262">MaximumWaitReason</span><span class="sxs-lookup"><span data-stu-id="27c5e-262">MaximumWaitReason</span></span> |



 

</dd> <dt>

<span data-ttu-id="27c5e-263">**PreviousCState**</span><span class="sxs-lookup"><span data-stu-id="27c5e-263">**PreviousCState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c5e-264">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="27c5e-264">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="27c5e-265">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27c5e-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27c5e-266">Calificadores: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="27c5e-266">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="27c5e-267">Índice del estado de C que el procesador utilizó por última vez.</span><span class="sxs-lookup"><span data-stu-id="27c5e-267">The index of the C-state that was last used by the processor.</span></span> <span data-ttu-id="27c5e-268">Un valor de 0 representa el estado de inactividad más claro con valores más altos que representan los Estados C más profundos.</span><span class="sxs-lookup"><span data-stu-id="27c5e-268">A value of 0 represents the lightest idle state with higher values representing deeper C-states.</span></span>

</dd> <dt>

<span data-ttu-id="27c5e-269">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="27c5e-269">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c5e-270">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="27c5e-270">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="27c5e-271">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27c5e-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27c5e-272">Calificadores: WmiDataId (12)</span><span class="sxs-lookup"><span data-stu-id="27c5e-272">Qualifiers: WmiDataId(12)</span></span>
</dt> </dl>

<span data-ttu-id="27c5e-273">Reservado.</span><span class="sxs-lookup"><span data-stu-id="27c5e-273">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="27c5e-274">**SpareByte**</span><span class="sxs-lookup"><span data-stu-id="27c5e-274">**SpareByte**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="27c5e-275">Tipo de datos: **sint8**</span><span class="sxs-lookup"><span data-stu-id="27c5e-275">Data type: **sint8**</span></span>
</dt> <dt>

<span data-ttu-id="27c5e-276">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="27c5e-276">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="27c5e-277">Calificadores: WmiDataId (6)</span><span class="sxs-lookup"><span data-stu-id="27c5e-277">Qualifiers: WmiDataId(6)</span></span>
</dt> </dl>

<span data-ttu-id="27c5e-278">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="27c5e-278">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="27c5e-279">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27c5e-279">Remarks</span></span>

<span data-ttu-id="27c5e-280">Estos eventos producen un gran volumen de eventos.</span><span class="sxs-lookup"><span data-stu-id="27c5e-280">These events produce a high volume of events.</span></span>

## <a name="requirements"></a><span data-ttu-id="27c5e-281">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27c5e-281">Requirements</span></span>



| <span data-ttu-id="27c5e-282">Requisito</span><span class="sxs-lookup"><span data-stu-id="27c5e-282">Requirement</span></span> | <span data-ttu-id="27c5e-283">Value</span><span class="sxs-lookup"><span data-stu-id="27c5e-283">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="27c5e-284">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27c5e-284">Minimum supported client</span></span><br/> | <span data-ttu-id="27c5e-285">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="27c5e-285">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="27c5e-286">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="27c5e-286">Minimum supported server</span></span><br/> | <span data-ttu-id="27c5e-287">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="27c5e-287">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="27c5e-288">Vea también</span><span class="sxs-lookup"><span data-stu-id="27c5e-288">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27c5e-289">**Conversaciones**</span><span class="sxs-lookup"><span data-stu-id="27c5e-289">**Thread**</span></span>](thread.md)
</dt> <dt>

[<span data-ttu-id="27c5e-290">**Subproceso \_ V2**</span><span class="sxs-lookup"><span data-stu-id="27c5e-290">**Thread\_V2**</span></span>](thread-v2.md)
</dt> </dl>

 

 




