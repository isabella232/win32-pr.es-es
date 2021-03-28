---
description: Esta clase es la clase de tipo de evento para los eventos del registro. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 8d0e9d97-3837-46da-a217-13e943580352
title: Registry_TypeGroup1 (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_TypeGroup1
- Registry_TypeGroup1.InitialTime
- Registry_TypeGroup1.Status
- Registry_TypeGroup1.Index
- Registry_TypeGroup1.KeyHandle
- Registry_TypeGroup1.KeyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: bfbf0157141473be4cc2460659912dc662ef7c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984567"
---
# <a name="registry_typegroup1-class"></a><span data-ttu-id="f248b-104">\_Clase Registry TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="f248b-104">Registry\_TypeGroup1 class</span></span>

<span data-ttu-id="f248b-105">Esta clase es la clase de tipo de evento para los eventos del registro.</span><span class="sxs-lookup"><span data-stu-id="f248b-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="f248b-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="f248b-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f248b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f248b-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27}, EventTypeName{"Create", "Open", "Delete", "Query", "SetValue", "DeleteValue", "QueryValue", "EnumerateKey", "EnumerateValueKey", "QueryMultipleValue", "SetInformation", "Flush", "KCBCreate", "KCBDelete", "KCBRundownBegin", "KCBRundownEnd", "Virtualize", "Close"}]
class Registry_TypeGroup1 : Registry
{
  sint64 InitialTime;
  uint32 Status;
  uint32 Index;
  uint32 KeyHandle;
  string KeyName;
};
```

## <a name="members"></a><span data-ttu-id="f248b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f248b-108">Members</span></span>

<span data-ttu-id="f248b-109">La clase **Registry \_ TypeGroup1** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f248b-109">The **Registry\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="f248b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f248b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f248b-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f248b-111">Properties</span></span>

<span data-ttu-id="f248b-112">La clase **Registry \_ TypeGroup1** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f248b-112">The **Registry\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f248b-113">Índice</span><span class="sxs-lookup"><span data-stu-id="f248b-113">Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f248b-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f248b-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f248b-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f248b-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f248b-116">Calificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="f248b-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="f248b-117">Índice de la subclave de la operación del registro (por ejemplo, EnumerateKey).</span><span class="sxs-lookup"><span data-stu-id="f248b-117">The subkey index for the registry operation (such as EnumerateKey).</span></span>

</dd> <dt>

<span data-ttu-id="f248b-118">InitialTime</span><span class="sxs-lookup"><span data-stu-id="f248b-118">InitialTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f248b-119">Tipo de datos: **sint64**</span><span class="sxs-lookup"><span data-stu-id="f248b-119">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="f248b-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f248b-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f248b-121">Calificadores: WmiDataId (1)</span><span class="sxs-lookup"><span data-stu-id="f248b-121">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="f248b-122">Hora inicial de la operación del registro.</span><span class="sxs-lookup"><span data-stu-id="f248b-122">Initial time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="f248b-123">KeyHandle</span><span class="sxs-lookup"><span data-stu-id="f248b-123">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f248b-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f248b-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f248b-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f248b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f248b-126">Calificadores: WmiDataId (4), puntero</span><span class="sxs-lookup"><span data-stu-id="f248b-126">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f248b-127">Identificador de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="f248b-127">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="f248b-128">KeyName</span><span class="sxs-lookup"><span data-stu-id="f248b-128">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f248b-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f248b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f248b-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f248b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f248b-131">Calificadores: WmiDataId (5), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="f248b-131">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="f248b-132">Nombre de la clave del Registro.</span><span class="sxs-lookup"><span data-stu-id="f248b-132">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="f248b-133">Estado</span><span class="sxs-lookup"><span data-stu-id="f248b-133">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f248b-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f248b-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f248b-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f248b-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f248b-136">Calificadores: WmiDataId (2), puntero</span><span class="sxs-lookup"><span data-stu-id="f248b-136">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f248b-137">Valor de NTSTATUS de la operación del registro.</span><span class="sxs-lookup"><span data-stu-id="f248b-137">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f248b-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f248b-138">Requirements</span></span>



| <span data-ttu-id="f248b-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="f248b-139">Requirement</span></span> | <span data-ttu-id="f248b-140">Value</span><span class="sxs-lookup"><span data-stu-id="f248b-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f248b-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f248b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f248b-142">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f248b-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f248b-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f248b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f248b-144">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f248b-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f248b-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="f248b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f248b-146">**Registro**</span><span class="sxs-lookup"><span data-stu-id="f248b-146">**Registry**</span></span>](registry.md)
</dt> </dl>

 

 




