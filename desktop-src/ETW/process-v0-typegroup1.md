---
description: 'Process_V0_TypeGroup1 clase : esta clase es la clase de tipo de evento para los eventos de proceso. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: fcf2897d-32b4-42b9-892c-f0106687d3c2
title: Process_V0_TypeGroup1 clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V0_TypeGroup1
- Process_V0_TypeGroup1.ProcessId
- Process_V0_TypeGroup1.ParentId
- Process_V0_TypeGroup1.UserSID
- Process_V0_TypeGroup1.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 524d3c7da9f8ff76608da120834c5365eb1deb41
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106363"
---
# <a name="process_v0_typegroup1-class"></a><span data-ttu-id="c59f4-104">Clase \_ TypeGroup1 de Process V0 \_</span><span class="sxs-lookup"><span data-stu-id="c59f4-104">Process\_V0\_TypeGroup1 class</span></span>

<span data-ttu-id="c59f4-105">Esta clase es la clase de tipo de evento para los eventos de proceso.</span><span class="sxs-lookup"><span data-stu-id="c59f4-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="c59f4-106">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="c59f4-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c59f4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c59f4-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Process_V0_TypeGroup1 : Process_V0
{
  uint32 ProcessId;
  uint32 ParentId;
  object UserSID;
  string ImageFileName;
};
```

## <a name="members"></a><span data-ttu-id="c59f4-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="c59f4-108">Members</span></span>

<span data-ttu-id="c59f4-109">La **clase Process \_ V0 \_ TypeGroup1** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c59f4-109">The **Process\_V0\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="c59f4-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c59f4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c59f4-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c59f4-111">Properties</span></span>

<span data-ttu-id="c59f4-112">La **clase \_ \_ TypeGroup1 Process V0** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c59f4-112">The **Process\_V0\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c59f4-113">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="c59f4-113">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f4-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c59f4-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c59f4-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c59f4-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c59f4-116">Calificadores: WmiDataId(4), StringTermination("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="c59f4-116">Qualifiers: WmiDataId(4), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="c59f4-117">Ruta de acceso al archivo ejecutable del proceso.</span><span class="sxs-lookup"><span data-stu-id="c59f4-117">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="c59f4-118">ParentId</span><span class="sxs-lookup"><span data-stu-id="c59f4-118">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f4-119">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="c59f4-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c59f4-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c59f4-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c59f4-121">Calificadores: WmiDataId(2), Pointer</span><span class="sxs-lookup"><span data-stu-id="c59f4-121">Qualifiers: WmiDataId(2), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c59f4-122">Identificador único del proceso que crea un proceso.</span><span class="sxs-lookup"><span data-stu-id="c59f4-122">Unique identifier of the process that creates a process.</span></span> <span data-ttu-id="c59f4-123">Los números de identificador de proceso se reutilizan, por lo que solo identifican un proceso para la duración de ese proceso.</span><span class="sxs-lookup"><span data-stu-id="c59f4-123">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="c59f4-124">Es posible que el proceso identificado por ParentProcessId finalice, por lo que ParentProcessId puede no hacer referencia a un proceso en ejecución.</span><span class="sxs-lookup"><span data-stu-id="c59f4-124">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="c59f4-125">También es posible que ParentProcessId hace referencia incorrectamente a un proceso que reutiliza un identificador de proceso.</span><span class="sxs-lookup"><span data-stu-id="c59f4-125">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

</dd> <dt>

<span data-ttu-id="c59f4-126">ProcessId</span><span class="sxs-lookup"><span data-stu-id="c59f4-126">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f4-127">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="c59f4-127">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c59f4-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c59f4-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c59f4-129">Calificadores: WmiDataId(1), Pointer</span><span class="sxs-lookup"><span data-stu-id="c59f4-129">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="c59f4-130">Identificador de proceso global que puede usar para identificar un proceso.</span><span class="sxs-lookup"><span data-stu-id="c59f4-130">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="c59f4-131">El valor es válido desde el momento en que se crea un proceso hasta que finaliza.</span><span class="sxs-lookup"><span data-stu-id="c59f4-131">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="c59f4-132">UserSID</span><span class="sxs-lookup"><span data-stu-id="c59f4-132">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c59f4-133">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="c59f4-133">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="c59f4-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c59f4-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c59f4-135">Calificadores: WmiDataId(3), Extension("Sid")</span><span class="sxs-lookup"><span data-stu-id="c59f4-135">Qualifiers: WmiDataId(3), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="c59f4-136">Identificador de seguridad (SID) para el contexto de usuario en el que se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="c59f4-136">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c59f4-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c59f4-137">Requirements</span></span>



| <span data-ttu-id="c59f4-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="c59f4-138">Requirement</span></span> | <span data-ttu-id="c59f4-139">Valor</span><span class="sxs-lookup"><span data-stu-id="c59f4-139">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c59f4-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c59f4-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c59f4-141">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c59f4-141">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="c59f4-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c59f4-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c59f4-143">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c59f4-143">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c59f4-144">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c59f4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c59f4-145">**Proceso \_ V0**</span><span class="sxs-lookup"><span data-stu-id="c59f4-145">**Process\_V0**</span></span>](process-v0.md)
</dt> </dl>

 

 




