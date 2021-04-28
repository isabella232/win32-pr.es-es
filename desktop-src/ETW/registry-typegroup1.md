---
description: 'Registry_TypeGroup1 clase : esta clase es la clase de tipo de evento para los eventos del Registro. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: 8d0e9d97-3837-46da-a217-13e943580352
title: Registry_TypeGroup1 clase
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
ms.openlocfilehash: d86412a950246bee4f9a692ab80e91b99d945c20
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106253"
---
# <a name="registry_typegroup1-class"></a><span data-ttu-id="f4c6c-104">Clase \_ Registry TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="f4c6c-104">Registry\_TypeGroup1 class</span></span>

<span data-ttu-id="f4c6c-105">Esta clase es la clase de tipo de evento para los eventos del Registro.</span><span class="sxs-lookup"><span data-stu-id="f4c6c-105">This class is the event type class for registry events.</span></span>

<span data-ttu-id="f4c6c-106">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="f4c6c-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4c6c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f4c6c-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="f4c6c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f4c6c-108">Members</span></span>

<span data-ttu-id="f4c6c-109">La **clase \_ Registry TypeGroup1** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f4c6c-109">The **Registry\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="f4c6c-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f4c6c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f4c6c-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f4c6c-111">Properties</span></span>

<span data-ttu-id="f4c6c-112">La **clase \_ Registry TypeGroup1** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f4c6c-112">The **Registry\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f4c6c-113">Índice</span><span class="sxs-lookup"><span data-stu-id="f4c6c-113">Index</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4c6c-114">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="f4c6c-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4c6c-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4c6c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4c6c-116">Calificadores: WmiDataId(3)</span><span class="sxs-lookup"><span data-stu-id="f4c6c-116">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="f4c6c-117">Índice de subclave para la operación del Registro (por ejemplo, EnumerateKey).</span><span class="sxs-lookup"><span data-stu-id="f4c6c-117">The subkey index for the registry operation (such as EnumerateKey).</span></span>

</dd> <dt>

<span data-ttu-id="f4c6c-118">InitialTime</span><span class="sxs-lookup"><span data-stu-id="f4c6c-118">InitialTime</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4c6c-119">Tipo de datos: **sint64**</span><span class="sxs-lookup"><span data-stu-id="f4c6c-119">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="f4c6c-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4c6c-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4c6c-121">Calificadores: WmiDataId(1)</span><span class="sxs-lookup"><span data-stu-id="f4c6c-121">Qualifiers: WmiDataId(1)</span></span>
</dt> </dl>

<span data-ttu-id="f4c6c-122">Hora inicial de la operación del Registro.</span><span class="sxs-lookup"><span data-stu-id="f4c6c-122">Initial time of the registry operation.</span></span>

</dd> <dt>

<span data-ttu-id="f4c6c-123">KeyHandle</span><span class="sxs-lookup"><span data-stu-id="f4c6c-123">KeyHandle</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4c6c-124">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="f4c6c-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4c6c-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4c6c-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4c6c-126">Calificadores: WmiDataId(4), Pointer</span><span class="sxs-lookup"><span data-stu-id="f4c6c-126">Qualifiers: WmiDataId(4), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f4c6c-127">Identificador de la clave del Registro.</span><span class="sxs-lookup"><span data-stu-id="f4c6c-127">Handle to the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="f4c6c-128">KeyName</span><span class="sxs-lookup"><span data-stu-id="f4c6c-128">KeyName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4c6c-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f4c6c-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4c6c-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4c6c-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4c6c-131">Calificadores: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span><span class="sxs-lookup"><span data-stu-id="f4c6c-131">Qualifiers: WmiDataId(5), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="f4c6c-132">Nombre de la clave del Registro.</span><span class="sxs-lookup"><span data-stu-id="f4c6c-132">Name of the registry key.</span></span>

</dd> <dt>

<span data-ttu-id="f4c6c-133">Status</span><span class="sxs-lookup"><span data-stu-id="f4c6c-133">Status</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4c6c-134">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="f4c6c-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f4c6c-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4c6c-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4c6c-136">Calificadores: WmiDataId(2), Pointer</span><span class="sxs-lookup"><span data-stu-id="f4c6c-136">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="f4c6c-137">Valor NTSTATUS de la operación del Registro.</span><span class="sxs-lookup"><span data-stu-id="f4c6c-137">NTSTATUS value of the registry operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f4c6c-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4c6c-138">Requirements</span></span>



| <span data-ttu-id="f4c6c-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4c6c-139">Requirement</span></span> | <span data-ttu-id="f4c6c-140">Valor</span><span class="sxs-lookup"><span data-stu-id="f4c6c-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f4c6c-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4c6c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f4c6c-142">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f4c6c-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f4c6c-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4c6c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f4c6c-144">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="f4c6c-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f4c6c-145">Consulte también</span><span class="sxs-lookup"><span data-stu-id="f4c6c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4c6c-146">**Registro**</span><span class="sxs-lookup"><span data-stu-id="f4c6c-146">**Registry**</span></span>](registry.md)
</dt> </dl>

 

 




