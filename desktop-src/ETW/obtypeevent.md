---
description: Representa la clase de tipo de evento para los eventos de tipo de objeto relacionados con el principio y el final de la recopilación de datos.
ms.assetid: 16b21f61-e734-4f51-9b11-e507b5957107
title: Clase ObTypeEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObTypeEvent
- ObTypeEvent.ObjectType
- ObTypeEvent.Reserved
- ObTypeEvent.TypeName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9d80d5fbe57565d64e9ea53587d7a2c3488e6cf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156728"
---
# <a name="obtypeevent-class"></a><span data-ttu-id="96cd7-103">Clase ObTypeEvent</span><span class="sxs-lookup"><span data-stu-id="96cd7-103">ObTypeEvent class</span></span>

<span data-ttu-id="96cd7-104">Representa la clase de tipo de evento para los eventos de tipo de objeto relacionados con el principio y el final de la recopilación de datos.</span><span class="sxs-lookup"><span data-stu-id="96cd7-104">Represents the event type class for object type events related to the beginning and end of data collection.</span></span> <span data-ttu-id="96cd7-105">Este evento implica la asignación de los valores de índice de tipo a los nombres de tipo.</span><span class="sxs-lookup"><span data-stu-id="96cd7-105">This event involves the mapping of the type index values to the type names.</span></span>

<span data-ttu-id="96cd7-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="96cd7-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="96cd7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96cd7-107">Syntax</span></span>

``` syntax
[Dynamic, EventType{36,37}, EventTypeName{TypeDCStart,TypeDCEnd}]
class ObTypeEvent : ObTrace
{
  uint16 ObjectType;
  uint16 Reserved;
  string TypeName;
};
```

## <a name="members"></a><span data-ttu-id="96cd7-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="96cd7-108">Members</span></span>

<span data-ttu-id="96cd7-109">La clase **ObTypeEvent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="96cd7-109">The **ObTypeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="96cd7-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="96cd7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="96cd7-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="96cd7-111">Properties</span></span>

<span data-ttu-id="96cd7-112">La clase **ObTypeEvent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="96cd7-112">The **ObTypeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="96cd7-113">**ObjectType**</span><span class="sxs-lookup"><span data-stu-id="96cd7-113">**ObjectType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96cd7-114">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="96cd7-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="96cd7-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="96cd7-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96cd7-116">Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span><span class="sxs-lookup"><span data-stu-id="96cd7-116">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (1)</span></span>
</dt> </dl>

<span data-ttu-id="96cd7-117">Tipo del objeto.</span><span class="sxs-lookup"><span data-stu-id="96cd7-117">The object type.</span></span>

</dd> <dt>

<span data-ttu-id="96cd7-118">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="96cd7-118">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96cd7-119">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="96cd7-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="96cd7-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="96cd7-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96cd7-121">Calificadores: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span><span class="sxs-lookup"><span data-stu-id="96cd7-121">Qualifiers: [**WmiDataId**](event-tracing-mof-qualifiers.md) (2)</span></span>
</dt> </dl>

<span data-ttu-id="96cd7-122">Reservado.</span><span class="sxs-lookup"><span data-stu-id="96cd7-122">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="96cd7-123">**TypeName**</span><span class="sxs-lookup"><span data-stu-id="96cd7-123">**TypeName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="96cd7-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="96cd7-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="96cd7-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="96cd7-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="96cd7-126">Calificadores: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span><span class="sxs-lookup"><span data-stu-id="96cd7-126">Qualifiers: [**Format**](event-tracing-mof-qualifiers.md) ("w"), [**StringTermination**](event-tracing-mof-qualifiers.md) ("NullTerminated"), [**WmiDataId**](event-tracing-mof-qualifiers.md) (3)</span></span>
</dt> </dl>

<span data-ttu-id="96cd7-127">Nombre del tipo.</span><span class="sxs-lookup"><span data-stu-id="96cd7-127">The type name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="96cd7-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96cd7-128">Requirements</span></span>



| <span data-ttu-id="96cd7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="96cd7-129">Requirement</span></span> | <span data-ttu-id="96cd7-130">Value</span><span class="sxs-lookup"><span data-stu-id="96cd7-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="96cd7-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96cd7-131">Minimum supported client</span></span><br/> | <span data-ttu-id="96cd7-132">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="96cd7-132">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="96cd7-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="96cd7-133">Minimum supported server</span></span><br/> | <span data-ttu-id="96cd7-134">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="96cd7-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="96cd7-135">MOF</span><span class="sxs-lookup"><span data-stu-id="96cd7-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="96cd7-136"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="96cd7-136"><dt>Wmicore.mof</dt></span></span> </dl> |



 

 




