---
description: Representa la clase de tipo de evento para los eventos de control de objetos relacionados con el principio y el final de la recopilación de datos.
ms.assetid: 96231819-f4ca-4c5c-bc19-4a76add5d3cf
title: Clase ObHandleRundownEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleRundownEvent
- ObHandleRundownEvent.Handle
- ObHandleRundownEvent.Object
- ObHandleRundownEvent.ObjectName
- ObHandleRundownEvent.ObjectType
- ObHandleRundownEvent.ProcessId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 5477acc1851d9799fe2bf68f9b867ab3f4c032fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985719"
---
# <a name="obhandlerundownevent-class"></a><span data-ttu-id="fd91a-103">Clase ObHandleRundownEvent</span><span class="sxs-lookup"><span data-stu-id="fd91a-103">ObHandleRundownEvent class</span></span>

<span data-ttu-id="fd91a-104">Representa la clase de tipo de evento para los eventos de control de objetos relacionados con el principio y el final de la recopilación de datos.</span><span class="sxs-lookup"><span data-stu-id="fd91a-104">Represents the event type class for object handle events related to the beginning and end of data collection.</span></span> <span data-ttu-id="fd91a-105">Este evento implica la enumeración de todos los identificadores cuando se realiza una detención.</span><span class="sxs-lookup"><span data-stu-id="fd91a-105">This event involves the enumerating of all handles when rundown is performed.</span></span>

<span data-ttu-id="fd91a-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="fd91a-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd91a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd91a-107">Syntax</span></span>

``` syntax
[Dynamic, EventType{38,39}, EventTypeName{HandleDCStart,HandleDCEnd}]
class ObHandleRundownEvent : ObTrace
{
  uint32 Handle;
  uint32 Object;
  string ObjectName;
  uint16 ObjectType;
  uint32 ProcessId;
};
```

## <a name="members"></a><span data-ttu-id="fd91a-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="fd91a-108">Members</span></span>

<span data-ttu-id="fd91a-109">La clase **ObHandleRundownEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fd91a-109">The **ObHandleRundownEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="fd91a-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fd91a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fd91a-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fd91a-111">Properties</span></span>

<span data-ttu-id="fd91a-112">La clase **ObHandleRundownEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fd91a-112">The **ObHandleRundownEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fd91a-113">**Handle**</span><span class="sxs-lookup"><span data-stu-id="fd91a-113">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd91a-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd91a-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd91a-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd91a-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd91a-116">Calificadores: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="fd91a-116">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="fd91a-117">Identificador del objeto.</span><span class="sxs-lookup"><span data-stu-id="fd91a-117">The object handle.</span></span>

</dd> <dt>

<span data-ttu-id="fd91a-118">**Object**</span><span class="sxs-lookup"><span data-stu-id="fd91a-118">**Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd91a-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd91a-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd91a-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd91a-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd91a-121">Calificadores: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**puntero**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="fd91a-121">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**Pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="fd91a-122">El objeto.</span><span class="sxs-lookup"><span data-stu-id="fd91a-122">The object.</span></span>

</dd> <dt>

<span data-ttu-id="fd91a-123">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="fd91a-123">**ObjectName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd91a-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fd91a-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fd91a-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd91a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd91a-126">Calificadores: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span><span class="sxs-lookup"><span data-stu-id="fd91a-126">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (5)</span></span>
</dt> </dl>

<span data-ttu-id="fd91a-127">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="fd91a-127">The object name.</span></span>

</dd> <dt>

<span data-ttu-id="fd91a-128">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="fd91a-128">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd91a-129">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fd91a-129">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fd91a-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd91a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd91a-131">Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span><span class="sxs-lookup"><span data-stu-id="fd91a-131">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="fd91a-132">Tipo del objeto.</span><span class="sxs-lookup"><span data-stu-id="fd91a-132">The object type.</span></span>

</dd> <dt>

<span data-ttu-id="fd91a-133">**ProcessId**</span><span class="sxs-lookup"><span data-stu-id="fd91a-133">**ProcessId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fd91a-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fd91a-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fd91a-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fd91a-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fd91a-136">Calificadores: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="fd91a-136">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="fd91a-137">Identificador del proceso.</span><span class="sxs-lookup"><span data-stu-id="fd91a-137">The process identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fd91a-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd91a-138">Requirements</span></span>



| <span data-ttu-id="fd91a-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd91a-139">Requirement</span></span> | <span data-ttu-id="fd91a-140">Value</span><span class="sxs-lookup"><span data-stu-id="fd91a-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd91a-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd91a-141">Minimum supported client</span></span><br/> | <span data-ttu-id="fd91a-142">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="fd91a-142">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="fd91a-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd91a-143">Minimum supported server</span></span><br/> | <span data-ttu-id="fd91a-144">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="fd91a-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="fd91a-145">MOF</span><span class="sxs-lookup"><span data-stu-id="fd91a-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fd91a-146"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fd91a-146"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




