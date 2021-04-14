---
description: Esta clase es la clase de tipo de evento para los eventos del registro. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 93031f3e-963f-46a6-9355-988eefd94836
title: Registry_V0_TypeGroup1 (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_V0_TypeGroup1
- Registry_V0_TypeGroup1.Status
- Registry_V0_TypeGroup1.KeyHandle
- Registry_V0_TypeGroup1.ElapsedTime
- Registry_V0_TypeGroup1.KeyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9a72a0d6ddfe5e441b21dff4ba58fa3bb37457a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984475"
---
# <a name="registry_v0_typegroup1-class"></a><span data-ttu-id="cd2ee-104">Clase del registro \_ V0 \_ TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="cd2ee-104">Registry\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="cd2ee-105">Esta clase es la clase de tipo de evento para los eventos del registro.</span><span class="sxs-lookup"><span data-stu-id="cd2ee-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="cd2ee-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="cd2ee-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd2ee-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd2ee-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21}, EventTypeName{"Create", "Open", "Delete", "Query", "SetValue", "DeleteValue", "QueryValue", "EnumerateKey", "EnumerateValueKey", "QueryMultipleValue", "SetInformation", "Flush"}]
class Registry_V0_TypeGroup1 : Registry_V0
{
  uint32 Status;
  uint32 KeyHandle;
  sint64 ElapsedTime;
  string KeyName;
};
```

## <a name="members"></a><span data-ttu-id="cd2ee-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="cd2ee-108">Members</span></span>

<span data-ttu-id="cd2ee-109">La clase **Registry \_ V0 \_ TypeGroup1** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cd2ee-109">The **Registry\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="cd2ee-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cd2ee-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cd2ee-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cd2ee-111">Properties</span></span>

<span data-ttu-id="cd2ee-112">La clase **Registry \_ V0 \_ TypeGroup1** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cd2ee-112">The **Registry\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cd2ee-113">ElapsedTime</span><span class="sxs-lookup"><span data-stu-id="cd2ee-113">ElapsedTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2ee-114">Tipo de datos: **sint64**</span><span class="sxs-lookup"><span data-stu-id="cd2ee-114">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="cd2ee-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cd2ee-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2ee-116">Calificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="cd2ee-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="cd2ee-117">Tiempo transcurrido de la operación del registro.</span><span class="sxs-lookup"><span data-stu-id="cd2ee-117">Elapsed time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="cd2ee-118">KeyHandle</span><span class="sxs-lookup"><span data-stu-id="cd2ee-118">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2ee-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd2ee-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd2ee-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cd2ee-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2ee-121">Calificadores: WmiDataId (2), puntero</span><span class="sxs-lookup"><span data-stu-id="cd2ee-121">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="cd2ee-122">Identificador de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="cd2ee-122">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="cd2ee-123">KeyName</span><span class="sxs-lookup"><span data-stu-id="cd2ee-123">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2ee-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="cd2ee-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cd2ee-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cd2ee-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2ee-126">Calificadores: WmiDataId (4), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="cd2ee-126">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="cd2ee-127">Nombre de la clave del Registro.</span><span class="sxs-lookup"><span data-stu-id="cd2ee-127">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="cd2ee-128">Estado</span><span class="sxs-lookup"><span data-stu-id="cd2ee-128">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cd2ee-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cd2ee-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="cd2ee-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cd2ee-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cd2ee-131">Calificadores: WmiDataId (1), puntero</span><span class="sxs-lookup"><span data-stu-id="cd2ee-131">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="cd2ee-132">Valor de NTSTATUS de la operación del registro.</span><span class="sxs-lookup"><span data-stu-id="cd2ee-132">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd2ee-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd2ee-133">Requirements</span></span>



| <span data-ttu-id="cd2ee-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd2ee-134">Requirement</span></span> | <span data-ttu-id="cd2ee-135">Value</span><span class="sxs-lookup"><span data-stu-id="cd2ee-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cd2ee-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd2ee-136">Minimum supported client</span></span><br/> | <span data-ttu-id="cd2ee-137">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="cd2ee-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="cd2ee-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd2ee-138">Minimum supported server</span></span><br/> | <span data-ttu-id="cd2ee-139">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cd2ee-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cd2ee-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd2ee-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd2ee-141">**Registro \_ v0**</span><span class="sxs-lookup"><span data-stu-id="cd2ee-141">**Registry\_V0**</span></span>](registry-v0.md)
</dt> </dl>

 

 




