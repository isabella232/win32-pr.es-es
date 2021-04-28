---
description: 'Process_V1_TypeGroup1 clase : esta clase es la clase de tipo de evento para los eventos de proceso. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: b114d7fd-c308-4f21-8f1a-ab27dc93abc5
title: Process_V1_TypeGroup1 clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V1_TypeGroup1
- Process_V1_TypeGroup1.PageDirectoryBase
- Process_V1_TypeGroup1.ProcessId
- Process_V1_TypeGroup1.ParentId
- Process_V1_TypeGroup1.SessionId
- Process_V1_TypeGroup1.ExitStatus
- Process_V1_TypeGroup1.UserSID
- Process_V1_TypeGroup1.ImageFileName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8d7f4426f34a97ff79dc41806f1e0070013528d2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106333"
---
# <a name="process_v1_typegroup1-class"></a><span data-ttu-id="ad1bb-104">Clase \_ \_ TypeGroup1 de Process V1</span><span class="sxs-lookup"><span data-stu-id="ad1bb-104">Process\_V1\_TypeGroup1 class</span></span>

<span data-ttu-id="ad1bb-105">Esta clase es la clase de tipo de evento para los eventos de proceso.</span><span class="sxs-lookup"><span data-stu-id="ad1bb-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="ad1bb-106">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="ad1bb-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad1bb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ad1bb-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4}, EventTypeName{"Start", "End", "DCStart", "DCEnd"}]
class Process_V1_TypeGroup1 : Process_V1
{
  uint32 PageDirectoryBase;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  object UserSID;
  string ImageFileName;
};
```

## <a name="members"></a><span data-ttu-id="ad1bb-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ad1bb-108">Members</span></span>

<span data-ttu-id="ad1bb-109">La **clase Process \_ V1 \_ TypeGroup1** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ad1bb-109">The **Process\_V1\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="ad1bb-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ad1bb-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ad1bb-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ad1bb-111">Properties</span></span>

<span data-ttu-id="ad1bb-112">La **clase Process \_ V1 \_ TypeGroup1** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ad1bb-112">The **Process\_V1\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ad1bb-113">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="ad1bb-113">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad1bb-114">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="ad1bb-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad1bb-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ad1bb-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad1bb-116">Calificadores: WmiDataId(5)</span><span class="sxs-lookup"><span data-stu-id="ad1bb-116">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="ad1bb-117">Estado de salida del proceso detenido.</span><span class="sxs-lookup"><span data-stu-id="ad1bb-117">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="ad1bb-118">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="ad1bb-118">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad1bb-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ad1bb-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad1bb-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ad1bb-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad1bb-121">Calificadores: WmiDataId(7), StringTermination("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="ad1bb-121">Qualifiers: WmiDataId(7), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="ad1bb-122">Ruta de acceso al archivo ejecutable del proceso.</span><span class="sxs-lookup"><span data-stu-id="ad1bb-122">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="ad1bb-123">PageDirectoryBase</span><span class="sxs-lookup"><span data-stu-id="ad1bb-123">PageDirectoryBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad1bb-124">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="ad1bb-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad1bb-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ad1bb-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad1bb-126">Calificadores: WmiDataId(1), Pointer</span><span class="sxs-lookup"><span data-stu-id="ad1bb-126">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="ad1bb-127">Reservado.</span><span class="sxs-lookup"><span data-stu-id="ad1bb-127">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="ad1bb-128">ParentId</span><span class="sxs-lookup"><span data-stu-id="ad1bb-128">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad1bb-129">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="ad1bb-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad1bb-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ad1bb-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad1bb-131">Calificadores: WmiDataId(3)</span><span class="sxs-lookup"><span data-stu-id="ad1bb-131">Qualifiers: WmiDataId(3)</span></span>
</dt> </dl>

<span data-ttu-id="ad1bb-132">Identificador único del proceso que crea este proceso.</span><span class="sxs-lookup"><span data-stu-id="ad1bb-132">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="ad1bb-133">Los números de identificador de proceso se reutilizan, por lo que solo identifican un proceso para la duración de ese proceso.</span><span class="sxs-lookup"><span data-stu-id="ad1bb-133">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="ad1bb-134">Es posible que el proceso identificado por ParentProcessId finalice, por lo que ParentProcessId puede no hacer referencia a un proceso en ejecución.</span><span class="sxs-lookup"><span data-stu-id="ad1bb-134">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="ad1bb-135">También es posible que ParentProcessId se refiere incorrectamente a un proceso que reutiliza un identificador de proceso.</span><span class="sxs-lookup"><span data-stu-id="ad1bb-135">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

<span data-ttu-id="ad1bb-136">**Windows Server 2003:** Incluye el calificador Format("x").</span><span class="sxs-lookup"><span data-stu-id="ad1bb-136">**Windows Server 2003:** Includes the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="ad1bb-137">ProcessId</span><span class="sxs-lookup"><span data-stu-id="ad1bb-137">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad1bb-138">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="ad1bb-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad1bb-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ad1bb-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad1bb-140">Calificadores: WmiDataId(2)</span><span class="sxs-lookup"><span data-stu-id="ad1bb-140">Qualifiers: WmiDataId(2)</span></span>
</dt> </dl>

<span data-ttu-id="ad1bb-141">Identificador de proceso global que puede usar para identificar un proceso.</span><span class="sxs-lookup"><span data-stu-id="ad1bb-141">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="ad1bb-142">El valor es válido desde el momento en que se crea un proceso hasta que finaliza.</span><span class="sxs-lookup"><span data-stu-id="ad1bb-142">The value is valid from the time a process is created until it is terminated.</span></span>

<span data-ttu-id="ad1bb-143">**Windows Server 2003:** Incluye el calificador Format("x").</span><span class="sxs-lookup"><span data-stu-id="ad1bb-143">**Windows Server 2003:** Includes the Format("x") qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="ad1bb-144">SessionId</span><span class="sxs-lookup"><span data-stu-id="ad1bb-144">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad1bb-145">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="ad1bb-145">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad1bb-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ad1bb-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad1bb-147">Calificadores: WmiDataId(4)</span><span class="sxs-lookup"><span data-stu-id="ad1bb-147">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="ad1bb-148">Identificador único que genera un sistema operativo cuando crea una nueva sesión.</span><span class="sxs-lookup"><span data-stu-id="ad1bb-148">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="ad1bb-149">Una sesión abarca un período de tiempo desde el inicio de sesión hasta la cierre de sesión desde un sistema específico.</span><span class="sxs-lookup"><span data-stu-id="ad1bb-149">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="ad1bb-150">UserSID</span><span class="sxs-lookup"><span data-stu-id="ad1bb-150">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad1bb-151">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="ad1bb-151">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="ad1bb-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ad1bb-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad1bb-153">Calificadores: WmiDataId(6), Extension("Sid")</span><span class="sxs-lookup"><span data-stu-id="ad1bb-153">Qualifiers: WmiDataId(6), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="ad1bb-154">Identificador de seguridad (SID) para el contexto de usuario en el que se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="ad1bb-154">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ad1bb-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad1bb-155">Requirements</span></span>



| <span data-ttu-id="ad1bb-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad1bb-156">Requirement</span></span> | <span data-ttu-id="ad1bb-157">Valor</span><span class="sxs-lookup"><span data-stu-id="ad1bb-157">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ad1bb-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad1bb-158">Minimum supported client</span></span><br/> | <span data-ttu-id="ad1bb-159">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="ad1bb-159">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="ad1bb-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ad1bb-160">Minimum supported server</span></span><br/> | <span data-ttu-id="ad1bb-161">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ad1bb-161">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ad1bb-162">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ad1bb-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad1bb-163">**Proceso \_ V1**</span><span class="sxs-lookup"><span data-stu-id="ad1bb-163">**Process\_V1**</span></span>](process.md)
</dt> <dt>

[<span data-ttu-id="ad1bb-164">**Proceso \_ V1**</span><span class="sxs-lookup"><span data-stu-id="ad1bb-164">**Process\_V1**</span></span>](process-v1.md)
</dt> </dl>

 

 




