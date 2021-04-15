---
description: Representa la clase de tipo de evento para controlar los eventos de duplicación.
ms.assetid: a933ffaa-8c99-4b87-ad00-4c40fa4d8d26
title: Clase ObHandleDuplicateEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleDuplicateEvent
- ObHandleDuplicateEvent.Object
- ObHandleDuplicateEvent.ObjectType
- ObHandleDuplicateEvent.SourceHandle
- ObHandleDuplicateEvent.TargetHandle
- ObHandleDuplicateEvent.TargetProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0f81ff9d85c0c5de8469f563db21e2054fa065f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986003"
---
# <a name="obhandleduplicateevent-class"></a><span data-ttu-id="cc81c-103">Clase ObHandleDuplicateEvent</span><span class="sxs-lookup"><span data-stu-id="cc81c-103">ObHandleDuplicateEvent class</span></span>

<span data-ttu-id="cc81c-104">Representa la clase de tipo de evento para controlar los eventos de duplicación.</span><span class="sxs-lookup"><span data-stu-id="cc81c-104">Represents the event type class for handle duplication events.</span></span>

<span data-ttu-id="cc81c-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="cc81c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc81c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cc81c-106">Syntax</span></span>

``` syntax
[Dynamic, EventType(34), EventTypeName("DuplicateHandle")]
class ObHandleDuplicateEvent : ObTrace
{
  uint32 Object;
  uint16 ObjectType;
  uint32 SourceHandle;
  uint32 TargetHandle;
  uint32 TargetProcessId;
};
```

## <a name="members"></a><span data-ttu-id="cc81c-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="cc81c-107">Members</span></span>

<span data-ttu-id="cc81c-108">La clase **ObHandleDuplicateEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cc81c-108">The **ObHandleDuplicateEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="cc81c-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cc81c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cc81c-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cc81c-110">Properties</span></span>

<span data-ttu-id="cc81c-111">La clase **ObHandleDuplicateEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cc81c-111">The **ObHandleDuplicateEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cc81c-112">**Object**</span><span class="sxs-lookup"><span data-stu-id="cc81c-112">**Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc81c-113">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cc81c-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc81c-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc81c-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc81c-115">Calificadores: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**puntero**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="cc81c-115">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**Pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="cc81c-116">El objeto.</span><span class="sxs-lookup"><span data-stu-id="cc81c-116">The object.</span></span>

</dd> <dt>

<span data-ttu-id="cc81c-117">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="cc81c-117">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc81c-118">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cc81c-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cc81c-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc81c-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc81c-120">Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span><span class="sxs-lookup"><span data-stu-id="cc81c-120">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="cc81c-121">Tipo del objeto.</span><span class="sxs-lookup"><span data-stu-id="cc81c-121">The object type.</span></span>

</dd> <dt>

<span data-ttu-id="cc81c-122">**SourceHandle**</span><span class="sxs-lookup"><span data-stu-id="cc81c-122">**SourceHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc81c-123">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cc81c-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc81c-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc81c-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc81c-125">Calificadores: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="cc81c-125">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="cc81c-126">Identificador del objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="cc81c-126">The handle of the source object.</span></span>

</dd> <dt>

<span data-ttu-id="cc81c-127">**TargetHandle**</span><span class="sxs-lookup"><span data-stu-id="cc81c-127">**TargetHandle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc81c-128">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cc81c-128">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc81c-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc81c-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc81c-130">Calificadores: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="cc81c-130">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="cc81c-131">Identificador del objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="cc81c-131">The handle of the target object.</span></span>

</dd> <dt>

<span data-ttu-id="cc81c-132">**TargetProcessId**</span><span class="sxs-lookup"><span data-stu-id="cc81c-132">**TargetProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cc81c-133">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cc81c-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cc81c-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cc81c-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cc81c-135">Calificadores: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span><span class="sxs-lookup"><span data-stu-id="cc81c-135">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="cc81c-136">Identificador de proceso del destino.</span><span class="sxs-lookup"><span data-stu-id="cc81c-136">The process identifier of the target.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cc81c-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc81c-137">Requirements</span></span>



| <span data-ttu-id="cc81c-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc81c-138">Requirement</span></span> | <span data-ttu-id="cc81c-139">Value</span><span class="sxs-lookup"><span data-stu-id="cc81c-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cc81c-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc81c-140">Minimum supported client</span></span><br/> | <span data-ttu-id="cc81c-141">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="cc81c-141">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cc81c-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cc81c-142">Minimum supported server</span></span><br/> | <span data-ttu-id="cc81c-143">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="cc81c-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cc81c-144">MOF</span><span class="sxs-lookup"><span data-stu-id="cc81c-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cc81c-145"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cc81c-145"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




