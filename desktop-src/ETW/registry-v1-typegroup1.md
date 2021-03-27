---
description: Esta clase es la clase de tipo de evento para los eventos del registro. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: 59c455a0-af7e-4fd5-9af4-07ff72ee0545
title: Registry_V1_TypeGroup1 (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_V1_TypeGroup1
- Registry_V1_TypeGroup1.Status
- Registry_V1_TypeGroup1.KeyHandle
- Registry_V1_TypeGroup1.ElapsedTime
- Registry_V1_TypeGroup1.Index
- Registry_V1_TypeGroup1.KeyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2cd77ad0c12769c657b4e7c23c1fe1993a248481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908101"
---
# <a name="registry_v1_typegroup1-class"></a><span data-ttu-id="5dae2-104">\_ \_ Clase TypeGroup1 del registro v1</span><span class="sxs-lookup"><span data-stu-id="5dae2-104">Registry\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="5dae2-105">Esta clase es la clase de tipo de evento para los eventos del registro.</span><span class="sxs-lookup"><span data-stu-id="5dae2-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="5dae2-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="5dae2-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5dae2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5dae2-107">Syntax</span></span>

``` syntax
[EventType{10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22}, EventTypeName{"Create", "Open", "Delete", "Query", "SetValue", "DeleteValue", "QueryValue", "EnumerateKey", "EnumerateValueKey", "QueryMultipleValue", "SetInformation", "Flush", "RunDown"}]
class Registry_V1_TypeGroup1 : Registry
{
  uint32 Status;
  uint32 KeyHandle;
  sint64 ElapsedTime;
  uint32 Index;
  string KeyName;
};
```

## <a name="members"></a><span data-ttu-id="5dae2-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="5dae2-108">Members</span></span>

<span data-ttu-id="5dae2-109">La **clase \_ \_ TypeGroup1 del registro v1** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5dae2-109">The **Registry\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="5dae2-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5dae2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5dae2-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5dae2-111">Properties</span></span>

<span data-ttu-id="5dae2-112">La **clase \_ \_ TypeGroup1 del registro v1** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5dae2-112">The **Registry\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5dae2-113">ElapsedTime</span><span class="sxs-lookup"><span data-stu-id="5dae2-113">ElapsedTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dae2-114">Tipo de datos: **sint64**</span><span class="sxs-lookup"><span data-stu-id="5dae2-114">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="5dae2-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5dae2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dae2-116">Calificadores: WmiDataId (3)</span><span class="sxs-lookup"><span data-stu-id="5dae2-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="5dae2-117">Tiempo transcurrido de la operación del registro.</span><span class="sxs-lookup"><span data-stu-id="5dae2-117">Elapsed time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="5dae2-118">Índice</span><span class="sxs-lookup"><span data-stu-id="5dae2-118">Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dae2-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5dae2-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5dae2-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5dae2-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dae2-121">Calificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="5dae2-121">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="5dae2-122">Índice de la subclave de la operación del registro (por ejemplo, EnumerateKey).</span><span class="sxs-lookup"><span data-stu-id="5dae2-122">The subkey index for the registry operation (such as EnumerateKey).</span></span>

</dd> <dt>

<span data-ttu-id="5dae2-123">KeyHandle</span><span class="sxs-lookup"><span data-stu-id="5dae2-123">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dae2-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5dae2-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5dae2-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5dae2-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dae2-126">Calificadores: WmiDataId (2), puntero</span><span class="sxs-lookup"><span data-stu-id="5dae2-126">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5dae2-127">Identificador de la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="5dae2-127">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="5dae2-128">KeyName</span><span class="sxs-lookup"><span data-stu-id="5dae2-128">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dae2-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5dae2-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5dae2-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5dae2-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dae2-131">Calificadores: WmiDataId (5), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="5dae2-131">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="5dae2-132">Nombre de la clave del Registro.</span><span class="sxs-lookup"><span data-stu-id="5dae2-132">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="5dae2-133">Estado</span><span class="sxs-lookup"><span data-stu-id="5dae2-133">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5dae2-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5dae2-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5dae2-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5dae2-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5dae2-136">Calificadores: WmiDataId (1), puntero</span><span class="sxs-lookup"><span data-stu-id="5dae2-136">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="5dae2-137">Valor de NTSTATUS de la operación del registro.</span><span class="sxs-lookup"><span data-stu-id="5dae2-137">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5dae2-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5dae2-138">Requirements</span></span>



| <span data-ttu-id="5dae2-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="5dae2-139">Requirement</span></span> | <span data-ttu-id="5dae2-140">Value</span><span class="sxs-lookup"><span data-stu-id="5dae2-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="5dae2-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5dae2-141">Minimum supported client</span></span><br/> | <span data-ttu-id="5dae2-142">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5dae2-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="5dae2-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5dae2-143">Minimum supported server</span></span><br/> | <span data-ttu-id="5dae2-144">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5dae2-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="5dae2-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="5dae2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dae2-146">**Registro**</span><span class="sxs-lookup"><span data-stu-id="5dae2-146">**Registry**</span></span>](registry.md)
</dt> <dt>

[<span data-ttu-id="5dae2-147">**Registro \_ v1**</span><span class="sxs-lookup"><span data-stu-id="5dae2-147">**Registry\_V1**</span></span>](registry-v1.md)
</dt> </dl>

 

 




