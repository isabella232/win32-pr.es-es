---
description: Esta clase es la clase de tipo de evento para los eventos de seguimiento de la pila.
ms.assetid: 05117bd6-a39c-42f3-8aed-c6f758f946c6
title: StackWalk_Event (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StackWalk_Event
- StackWalk_Event.EventTimeStamp
- StackWalk_Event.StackProcess
- StackWalk_Event.StackThread
- StackWalk_Event.Stack1
- StackWalk_Event.Stack192
api_type:
- NA
api_location: ''
ms.openlocfilehash: 746a7f2a9b5f6bb6316bf0d0e20e5645cea15a7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985702"
---
# <a name="stackwalk_event-class"></a><span data-ttu-id="3d87c-103">StackWalk ( \_ clase de eventos)</span><span class="sxs-lookup"><span data-stu-id="3d87c-103">StackWalk\_Event class</span></span>

<span data-ttu-id="3d87c-104">Esta clase es la clase de tipo de evento para los eventos de seguimiento de la pila.</span><span class="sxs-lookup"><span data-stu-id="3d87c-104">This class is the event type class for stack tracing events.</span></span>

<span data-ttu-id="3d87c-105">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3d87c-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d87c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3d87c-106">Syntax</span></span>

``` syntax
[EventType{32}, EventTypeName{"Stack"}]
class StackWalk_Event : StackWalk
{
  uint64 EventTimeStamp;
  uint32 StackProcess;
  uint32 StackThread;
  uint32 Stack1;
  uint32 Stack192;
};
```

## <a name="members"></a><span data-ttu-id="3d87c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="3d87c-107">Members</span></span>

<span data-ttu-id="3d87c-108">La clase de **\_ eventos StackWalk** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3d87c-108">The **StackWalk\_Event** class has these types of members:</span></span>

-   [<span data-ttu-id="3d87c-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3d87c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3d87c-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3d87c-110">Properties</span></span>

<span data-ttu-id="3d87c-111">La clase de **\_ evento StackWalk** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3d87c-111">The **StackWalk\_Event** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3d87c-112">**EventTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="3d87c-112">**EventTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d87c-113">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3d87c-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3d87c-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3d87c-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d87c-115">Calificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="3d87c-115">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="3d87c-116">Marca de tiempo del evento original del encabezado del evento.</span><span class="sxs-lookup"><span data-stu-id="3d87c-116">Original event time stamp from the event header.</span></span> <span data-ttu-id="3d87c-117">Use esta marca de tiempo para hacer coincidir la pila con un evento.</span><span class="sxs-lookup"><span data-stu-id="3d87c-117">Use this time stamp to match the stack to an event.</span></span>

</dd> <dt>

<span data-ttu-id="3d87c-118">**Stack1**</span><span class="sxs-lookup"><span data-stu-id="3d87c-118">**Stack1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d87c-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3d87c-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d87c-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3d87c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d87c-121">Calificadores: WmiDataId (4), puntero</span><span class="sxs-lookup"><span data-stu-id="3d87c-121">Qualifiers: WmiDataId(4), pointer</span></span>
</dt> </dl>

<span data-ttu-id="3d87c-122">Dirección de la llamada.</span><span class="sxs-lookup"><span data-stu-id="3d87c-122">Address of the call.</span></span>

</dd> <dt>

<span data-ttu-id="3d87c-123">**Stack192**</span><span class="sxs-lookup"><span data-stu-id="3d87c-123">**Stack192**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d87c-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3d87c-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d87c-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3d87c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d87c-126">Calificadores: WmiDataId (195), puntero</span><span class="sxs-lookup"><span data-stu-id="3d87c-126">Qualifiers: WmiDataId(195), pointer</span></span>
</dt> </dl>

<span data-ttu-id="3d87c-127">Dirección de la llamada.</span><span class="sxs-lookup"><span data-stu-id="3d87c-127">Address of the call.</span></span>

</dd> <dt>

<span data-ttu-id="3d87c-128">**StackProcess**</span><span class="sxs-lookup"><span data-stu-id="3d87c-128">**StackProcess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d87c-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3d87c-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d87c-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3d87c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d87c-131">Calificadores: WmiDataId (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="3d87c-131">Qualifiers: WmiDataId(2), format("x")</span></span>
</dt> </dl>

<span data-ttu-id="3d87c-132">Identificador de proceso del evento original.</span><span class="sxs-lookup"><span data-stu-id="3d87c-132">The process identifier of the original event.</span></span>

</dd> <dt>

<span data-ttu-id="3d87c-133">**StackThread**</span><span class="sxs-lookup"><span data-stu-id="3d87c-133">**StackThread**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3d87c-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3d87c-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3d87c-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3d87c-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3d87c-136">Calificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="3d87c-136">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="3d87c-137">Identificador del subproceso del evento original.</span><span class="sxs-lookup"><span data-stu-id="3d87c-137">The thread identifier of the original event.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3d87c-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3d87c-138">Remarks</span></span>

<span data-ttu-id="3d87c-139">Tenga en cuenta que la clase no muestra todas las propiedades de **Stack \* n**\* que existen entre **Stack1** y **Stack192**.</span><span class="sxs-lookup"><span data-stu-id="3d87c-139">Note that the class does not show all of the **Stack\*n**\* properties that exist between **Stack1** and **Stack192**.</span></span> <span data-ttu-id="3d87c-140">Use el tamaño del evento para determinar cuántas propiedades de **Stack \* n**\* contienen direcciones válidas.</span><span class="sxs-lookup"><span data-stu-id="3d87c-140">Use the size of the event to determine how many **Stack\*n**\* properties contain valid addresses.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d87c-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d87c-141">Requirements</span></span>



| <span data-ttu-id="3d87c-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d87c-142">Requirement</span></span> | <span data-ttu-id="3d87c-143">Value</span><span class="sxs-lookup"><span data-stu-id="3d87c-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="3d87c-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d87c-144">Minimum supported client</span></span><br/> | <span data-ttu-id="3d87c-145">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="3d87c-145">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="3d87c-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3d87c-146">Minimum supported server</span></span><br/> | <span data-ttu-id="3d87c-147">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3d87c-147">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 




