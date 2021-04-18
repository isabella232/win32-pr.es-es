---
title: DXCoreAdapterMemoryBudget
description: Describe el presupuesto de memoria para un adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 2888b1480e3e394640a10bf0264403cd6c153e3b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488198"
---
# <a name="dxcoreadaptermemorybudget-structure"></a><span data-ttu-id="ee613-103">Estructura DXCoreAdapterMemoryBudget</span><span class="sxs-lookup"><span data-stu-id="ee613-103">DXCoreAdapterMemoryBudget structure</span></span>

<span data-ttu-id="ee613-104">Especifica el estado del adaptador de <em>AdapterMemoryBudget</em> , que recupera o solicita el presupuesto de memoria del adaptador en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="ee613-104">Specifies the <em>AdapterMemoryBudget</em> adapter state, which retrieves or requests the adapter memory budget on the adapter.</span></span> <span data-ttu-id="ee613-105">Establecer (solicitar) un presupuesto representa la memoria física mínima necesaria para reservar, en bytes, en el adaptador.</span><span class="sxs-lookup"><span data-stu-id="ee613-105">Setting (requesting) a budget represents the minimum required physical memory to reserve, in bytes, on the adapter.</span></span> <span data-ttu-id="ee613-106">Se recomienda establecer una reserva de adaptador con el fin de indicar la cantidad de memoria física que no puede tener la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ee613-106">We recommend that you set an adapter reservation in order to denote the amount of physical memory that your application can't go without.</span></span> <span data-ttu-id="ee613-107">Este valor ayuda al sistema operativo (SO) a minimizar rápidamente el impacto de las grandes situaciones de presión de memoria.</span><span class="sxs-lookup"><span data-stu-id="ee613-107">This value helps the operating system (OS) to quickly minimize the impact of large memory-pressure situations.</span></span>

<span data-ttu-id="ee613-108">Al llamar a [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), el estado del adaptador de <em>AdapterMemoryBudget</em> tiene el tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> para *inputStateDetails* y el tipo **DXCoreAdapterMemoryBudget** para *outputBuffer*.</span><span class="sxs-lookup"><span data-stu-id="ee613-108">When calling [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), the <em>AdapterMemoryBudget</em> adapter state has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> for *inputStateDetails*, and type **DXCoreAdapterMemoryBudget** for *outputBuffer*.</span></span>

<span data-ttu-id="ee613-109">Al llamar a [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), el estado del adaptador de <em>AdapterMemoryBudget</em> tiene el tipo <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> para *inputStateDetails* y el tipo **uint64_t** para *inputData*.</span><span class="sxs-lookup"><span data-stu-id="ee613-109">When calling [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), the <em>AdapterMemoryBudget</em> adapter state has type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> for *inputStateDetails*, and type **uint64_t** for *inputData*.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee613-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee613-110">Syntax</span></span>

```cpp
struct DXCoreAdapterMemoryBudget
{
  uint64_t budget;
  uint64_t currentUsage;
  uint64_t availableForReservation;
  uint64_t currentReservation;
};
```

## <a name="members"></a><span data-ttu-id="ee613-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="ee613-111">Members</span></span>

### <a name="budget"></a><span data-ttu-id="ee613-112">budget</span><span class="sxs-lookup"><span data-stu-id="ee613-112">budget</span></span>

<span data-ttu-id="ee613-113">Tipo: **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="ee613-113">Type: **uint64_t**</span></span>

<span data-ttu-id="ee613-114">Especifica el presupuesto de memoria del adaptador proporcionado por el sistema operativo, en bytes, que la aplicación debe tener como destino.</span><span class="sxs-lookup"><span data-stu-id="ee613-114">Specifies the OS-provided adapter memory budget, in bytes, that your application should target.</span></span> <span data-ttu-id="ee613-115">Si *currentUsage* es mayor que el *presupuesto*, es posible que la aplicación incurra en intermitencias o penalizaciones de rendimiento debidas a la actividad en segundo plano por parte del sistema operativo, que está diseñada para proporcionar a otras aplicaciones un uso equitativo de la memoria del adaptador.</span><span class="sxs-lookup"><span data-stu-id="ee613-115">If *currentUsage* is greater than *budget*, then your application may incur stuttering or performance penalties due to background activity by the OS, which is intended to provide other applications with a fair usage of adapter memory.</span></span>

### <a name="currentusage"></a><span data-ttu-id="ee613-116">currentUsage</span><span class="sxs-lookup"><span data-stu-id="ee613-116">currentUsage</span></span>

<span data-ttu-id="ee613-117">Tipo: **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="ee613-117">Type: **uint64_t**</span></span>

<span data-ttu-id="ee613-118">Especifica el uso de memoria actual del adaptador de la misma en bytes.</span><span class="sxs-lookup"><span data-stu-id="ee613-118">Specifies your applicaton's current adapter memory usage, in bytes.</span></span>

### <a name="availableforreservation"></a><span data-ttu-id="ee613-119">availableForReservation</span><span class="sxs-lookup"><span data-stu-id="ee613-119">availableForReservation</span></span>

<span data-ttu-id="ee613-120">Tipo: **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="ee613-120">Type: **uint64_t**</span></span>

<span data-ttu-id="ee613-121">Especifica la cantidad de memoria del adaptador, en bytes, que la aplicación tiene disponible para reserva.</span><span class="sxs-lookup"><span data-stu-id="ee613-121">Specifies the amount of adapter memory, in bytes, that your application has available for reservation.</span></span> <span data-ttu-id="ee613-122">Para reservar esta memoria del adaptador, la aplicación debe llamar a [IDXCoreAdapter:: SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) con el *Estado* establecido en [DXCoreAdapterState:: AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md).</span><span class="sxs-lookup"><span data-stu-id="ee613-122">To reserve this adapter memory, your application should call [IDXCoreAdapter::SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) with *state* set to [DXCoreAdapterState::AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md).</span></span>

### <a name="currentreservation"></a><span data-ttu-id="ee613-123">currentReservation</span><span class="sxs-lookup"><span data-stu-id="ee613-123">currentReservation</span></span>

<span data-ttu-id="ee613-124">Tipo: **uint64_t**</span><span class="sxs-lookup"><span data-stu-id="ee613-124">Type: **uint64_t**</span></span>

<span data-ttu-id="ee613-125">Especifica la cantidad de memoria del adaptador, en bytes, reservada por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ee613-125">Specifies the amount of adapter memory, in bytes, that is reserved by your application.</span></span> <span data-ttu-id="ee613-126">El sistema operativo usa la reserva como una sugerencia para determinar el espacio de trabajo mínimo de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ee613-126">The OS uses the reservation as a hint to determine your application's minimum working set.</span></span> <span data-ttu-id="ee613-127">La aplicación debe intentar asegurarse de que se puede recortar el uso de memoria del adaptador para cumplir este requisito.</span><span class="sxs-lookup"><span data-stu-id="ee613-127">Your application should attempt to ensure that its adapter memory usage can be trimmed to meet this requirement.</span></span>

## <a name="see-also"></a><span data-ttu-id="ee613-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee613-128">See also</span></span>

<span data-ttu-id="ee613-129">[Referencia de DXCore](../dxcore-reference.md), [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="ee613-129">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>