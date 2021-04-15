---
description: Representa la clase de tipo de evento para los eventos de creación o cierre del control.
ms.assetid: 39d27cdf-fa51-4fb1-8998-7150ca627eff
title: Clase ObHandleEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObHandleEvent
- ObHandleEvent.Handle
- ObHandleEvent.Object
- ObHandleEvent.ObjectName
- ObHandleEvent.ObjectType
api_type:
- NA
api_location: ''
ms.openlocfilehash: ae293684bd09322c7193035d374e5e2bad21447f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985718"
---
# <a name="obhandleevent-class"></a><span data-ttu-id="06635-103">Clase ObHandleEvent</span><span class="sxs-lookup"><span data-stu-id="06635-103">ObHandleEvent class</span></span>

<span data-ttu-id="06635-104">Representa la clase de tipo de evento para los eventos de creación o cierre del control.</span><span class="sxs-lookup"><span data-stu-id="06635-104">Represents the event type class for handle creation or closure events.</span></span>

<span data-ttu-id="06635-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="06635-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="06635-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06635-106">Syntax</span></span>

``` syntax
[Dynamic, EventType{32,33}, EventTypeName{CreateHandle,CloseHandle}]
class ObHandleEvent : ObTrace
{
  uint32 Handle;
  uint32 Object;
  string ObjectName;
  uint16 ObjectType;
};
```

## <a name="members"></a><span data-ttu-id="06635-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="06635-107">Members</span></span>

<span data-ttu-id="06635-108">La clase **ObHandleEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="06635-108">The **ObHandleEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="06635-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="06635-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="06635-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="06635-110">Properties</span></span>

<span data-ttu-id="06635-111">La clase **ObHandleEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="06635-111">The **ObHandleEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="06635-112">**Handle**</span><span class="sxs-lookup"><span data-stu-id="06635-112">**Handle**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06635-113">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="06635-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06635-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06635-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06635-115">Calificadores: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="06635-115">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="06635-116">Identificador del objeto.</span><span class="sxs-lookup"><span data-stu-id="06635-116">The object handle.</span></span>

</dd> <dt>

<span data-ttu-id="06635-117">**Object**</span><span class="sxs-lookup"><span data-stu-id="06635-117">**Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06635-118">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="06635-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="06635-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06635-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06635-120">Calificadores: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**puntero**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="06635-120">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("x"), [**Pointer**](event-tracing-mof-qualifiers.md), [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="06635-121">El objeto.</span><span class="sxs-lookup"><span data-stu-id="06635-121">The object.</span></span>

</dd> <dt>

<span data-ttu-id="06635-122">**ObjectName**</span><span class="sxs-lookup"><span data-stu-id="06635-122">**ObjectName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06635-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="06635-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="06635-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06635-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06635-125">Calificadores: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span><span class="sxs-lookup"><span data-stu-id="06635-125">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (4)</span></span>
</dt> </dl>

<span data-ttu-id="06635-126">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="06635-126">The object name.</span></span>

</dd> <dt>

<span data-ttu-id="06635-127">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="06635-127">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06635-128">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="06635-128">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="06635-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="06635-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="06635-130">Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="06635-130">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="06635-131">Tipo del objeto.</span><span class="sxs-lookup"><span data-stu-id="06635-131">The object type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="06635-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06635-132">Requirements</span></span>



| <span data-ttu-id="06635-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="06635-133">Requirement</span></span> | <span data-ttu-id="06635-134">Value</span><span class="sxs-lookup"><span data-stu-id="06635-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06635-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06635-135">Minimum supported client</span></span><br/> | <span data-ttu-id="06635-136">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="06635-136">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="06635-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="06635-137">Minimum supported server</span></span><br/> | <span data-ttu-id="06635-138">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="06635-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="06635-139">MOF</span><span class="sxs-lookup"><span data-stu-id="06635-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="06635-140"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="06635-140"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




