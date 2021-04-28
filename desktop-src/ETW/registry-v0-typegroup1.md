---
description: 'Registry_V0_TypeGroup1 clase : esta clase es la clase de tipo de evento para los eventos del Registro. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: 93031f3e-963f-46a6-9355-988eefd94836
title: Registry_V0_TypeGroup1 clase
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
ms.openlocfilehash: 86f6d695afa2e05c87a076cf88ed8023e9416beb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106193"
---
# <a name="registry_v0_typegroup1-class"></a><span data-ttu-id="b43ce-104">Clase \_ \_ TypeGroup1 del Registro V0</span><span class="sxs-lookup"><span data-stu-id="b43ce-104">Registry\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="b43ce-105">Esta clase es la clase de tipo de evento para los eventos del Registro.</span><span class="sxs-lookup"><span data-stu-id="b43ce-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="b43ce-106">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="b43ce-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="b43ce-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b43ce-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="b43ce-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b43ce-108">Members</span></span>

<span data-ttu-id="b43ce-109">La **clase \_ \_ TypeGroup1 de Registry V0** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b43ce-109">The **Registry\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="b43ce-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b43ce-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b43ce-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b43ce-111">Properties</span></span>

<span data-ttu-id="b43ce-112">La **clase \_ \_ TypeGroup1 de Registry V0** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b43ce-112">The **Registry\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b43ce-113">ElapsedTime</span><span class="sxs-lookup"><span data-stu-id="b43ce-113">ElapsedTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b43ce-114">Tipo de datos: **sint64**</span><span class="sxs-lookup"><span data-stu-id="b43ce-114">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="b43ce-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b43ce-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b43ce-116">Calificadores: WmiDataId(3)</span><span class="sxs-lookup"><span data-stu-id="b43ce-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="b43ce-117">Tiempo transcurrido de la operación del Registro.</span><span class="sxs-lookup"><span data-stu-id="b43ce-117">Elapsed time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="b43ce-118">KeyHandle</span><span class="sxs-lookup"><span data-stu-id="b43ce-118">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b43ce-119">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="b43ce-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b43ce-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b43ce-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b43ce-121">Calificadores: WmiDataId(2), Pointer</span><span class="sxs-lookup"><span data-stu-id="b43ce-121">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b43ce-122">Identificador de la clave del Registro.</span><span class="sxs-lookup"><span data-stu-id="b43ce-122">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="b43ce-123">KeyName</span><span class="sxs-lookup"><span data-stu-id="b43ce-123">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b43ce-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b43ce-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b43ce-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b43ce-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b43ce-126">Calificadores: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span><span class="sxs-lookup"><span data-stu-id="b43ce-126">Qualifiers: WmiDataId(4), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="b43ce-127">Nombre de la clave del Registro.</span><span class="sxs-lookup"><span data-stu-id="b43ce-127">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="b43ce-128">Status</span><span class="sxs-lookup"><span data-stu-id="b43ce-128">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b43ce-129">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="b43ce-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b43ce-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b43ce-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b43ce-131">Calificadores: WmiDataId(1), Pointer</span><span class="sxs-lookup"><span data-stu-id="b43ce-131">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="b43ce-132">Valor NTSTATUS de la operación del Registro.</span><span class="sxs-lookup"><span data-stu-id="b43ce-132">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b43ce-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b43ce-133">Requirements</span></span>



| <span data-ttu-id="b43ce-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b43ce-134">Requirement</span></span> | <span data-ttu-id="b43ce-135">Valor</span><span class="sxs-lookup"><span data-stu-id="b43ce-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b43ce-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b43ce-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b43ce-137">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b43ce-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="b43ce-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b43ce-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b43ce-139">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b43ce-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b43ce-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b43ce-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b43ce-141">**Registro \_ V0**</span><span class="sxs-lookup"><span data-stu-id="b43ce-141">**Registry\_V0**</span></span>](registry-v0.md)
</dt> </dl>

 

 




