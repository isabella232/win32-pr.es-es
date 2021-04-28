---
description: 'Process_TypeGroup1 clase : esta clase es la clase de tipo de evento para los eventos de proceso. La sintaxis siguiente se simplifica a partir del código MOF.'
ms.assetid: 4f06e1af-3f9a-4346-aa50-50f3ee82cd98
title: Process_TypeGroup1 clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_TypeGroup1
- Process_TypeGroup1.UniqueProcessKey
- Process_TypeGroup1.ProcessId
- Process_TypeGroup1.ParentId
- Process_TypeGroup1.SessionId
- Process_TypeGroup1.ExitStatus
- Process_TypeGroup1.DirectoryTableBase
- Process_TypeGroup1.UserSID
- Process_TypeGroup1.ImageFileName
- Process_TypeGroup1.CommandLine
api_type:
- NA
api_location: ''
ms.openlocfilehash: bd67059f5257dad9b66e1c21f642fef04f03719e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106383"
---
# <a name="process_typegroup1-class"></a><span data-ttu-id="bf3ca-104">Clase \_ Process TypeGroup1</span><span class="sxs-lookup"><span data-stu-id="bf3ca-104">Process\_TypeGroup1 class</span></span>

<span data-ttu-id="bf3ca-105">Esta clase es la clase de tipo de evento para los eventos de proceso.</span><span class="sxs-lookup"><span data-stu-id="bf3ca-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="bf3ca-106">La sintaxis siguiente se simplifica a partir del código MOF.</span><span class="sxs-lookup"><span data-stu-id="bf3ca-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf3ca-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bf3ca-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4, 39}, EventTypeName{"Start", "End", "DCStart", "DCEnd", "Defunct"}]
class Process_TypeGroup1 : Process
{
  uint32 UniqueProcessKey;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  uint32 DirectoryTableBase;
  object UserSID;
  string ImageFileName;
  string CommandLine;
};
```

## <a name="members"></a><span data-ttu-id="bf3ca-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="bf3ca-108">Members</span></span>

<span data-ttu-id="bf3ca-109">La **clase \_ Process TypeGroup1** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bf3ca-109">The **Process\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="bf3ca-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bf3ca-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bf3ca-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bf3ca-111">Properties</span></span>

<span data-ttu-id="bf3ca-112">La **clase \_ Process TypeGroup1** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bf3ca-112">The **Process\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bf3ca-113">CommandLine</span><span class="sxs-lookup"><span data-stu-id="bf3ca-113">CommandLine</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3ca-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bf3ca-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf3ca-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bf3ca-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3ca-116">Calificadores: WmiDataId(9), StringTermination("NullTerminated"), Format("w")</span><span class="sxs-lookup"><span data-stu-id="bf3ca-116">Qualifiers: WmiDataId(9), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="bf3ca-117">Línea de comandos completa del proceso.</span><span class="sxs-lookup"><span data-stu-id="bf3ca-117">Full command line of the process.</span></span>

</dd> <dt>

<span data-ttu-id="bf3ca-118">DirectoryTableBase</span><span class="sxs-lookup"><span data-stu-id="bf3ca-118">DirectoryTableBase</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3ca-119">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="bf3ca-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf3ca-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bf3ca-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3ca-121">Calificadores: WmiDataId(6), Pointer</span><span class="sxs-lookup"><span data-stu-id="bf3ca-121">Qualifiers: WmiDataId(6), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="bf3ca-122">Dirección física de la tabla de páginas del proceso.</span><span class="sxs-lookup"><span data-stu-id="bf3ca-122">The physical address of the page table of the process.</span></span>

</dd> <dt>

<span data-ttu-id="bf3ca-123">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="bf3ca-123">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3ca-124">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bf3ca-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf3ca-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bf3ca-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3ca-126">Calificadores: WmiDataId(5)</span><span class="sxs-lookup"><span data-stu-id="bf3ca-126">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="bf3ca-127">Estado de salida del proceso detenido.</span><span class="sxs-lookup"><span data-stu-id="bf3ca-127">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="bf3ca-128">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="bf3ca-128">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3ca-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bf3ca-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bf3ca-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bf3ca-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3ca-131">Calificadores: WmiDataId(8), StringTermination("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="bf3ca-131">Qualifiers: WmiDataId(8), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="bf3ca-132">Ruta de acceso al archivo ejecutable del proceso.</span><span class="sxs-lookup"><span data-stu-id="bf3ca-132">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="bf3ca-133">ParentId</span><span class="sxs-lookup"><span data-stu-id="bf3ca-133">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3ca-134">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="bf3ca-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf3ca-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bf3ca-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3ca-136">Calificadores: WmiDataId(3), Format("x")</span><span class="sxs-lookup"><span data-stu-id="bf3ca-136">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="bf3ca-137">Identificador único del proceso que crea este proceso.</span><span class="sxs-lookup"><span data-stu-id="bf3ca-137">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="bf3ca-138">Los números de identificador de proceso se reutilizan, por lo que solo identifican un proceso durante la vigencia de ese proceso.</span><span class="sxs-lookup"><span data-stu-id="bf3ca-138">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="bf3ca-139">Es posible que el proceso identificado por ParentProcessId finalice, por lo que ParentProcessId puede no hacer referencia a un proceso en ejecución.</span><span class="sxs-lookup"><span data-stu-id="bf3ca-139">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="bf3ca-140">También es posible que ParentProcessId se refiere incorrectamente a un proceso que reutiliza un identificador de proceso.</span><span class="sxs-lookup"><span data-stu-id="bf3ca-140">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

</dd> <dt>

<span data-ttu-id="bf3ca-141">ProcessId</span><span class="sxs-lookup"><span data-stu-id="bf3ca-141">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3ca-142">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="bf3ca-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf3ca-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bf3ca-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3ca-144">Calificadores: WmiDataId(2), Format("x")</span><span class="sxs-lookup"><span data-stu-id="bf3ca-144">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="bf3ca-145">Identificador de proceso global que puede usar para identificar un proceso.</span><span class="sxs-lookup"><span data-stu-id="bf3ca-145">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="bf3ca-146">El valor es válido desde el momento en que se crea un proceso hasta que finaliza.</span><span class="sxs-lookup"><span data-stu-id="bf3ca-146">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="bf3ca-147">SessionId</span><span class="sxs-lookup"><span data-stu-id="bf3ca-147">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3ca-148">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="bf3ca-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf3ca-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bf3ca-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3ca-150">Calificadores: WmiDataId(4)</span><span class="sxs-lookup"><span data-stu-id="bf3ca-150">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="bf3ca-151">Identificador único que genera un sistema operativo cuando crea una nueva sesión.</span><span class="sxs-lookup"><span data-stu-id="bf3ca-151">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="bf3ca-152">Una sesión abarca un período de tiempo desde el inicio de sesión hasta la cierre de sesión desde un sistema específico.</span><span class="sxs-lookup"><span data-stu-id="bf3ca-152">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="bf3ca-153">UniqueProcessKey</span><span class="sxs-lookup"><span data-stu-id="bf3ca-153">UniqueProcessKey</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3ca-154">Tipo de datos: **uint32**</span><span class="sxs-lookup"><span data-stu-id="bf3ca-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bf3ca-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bf3ca-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3ca-156">Calificadores: WmiDataId(1), Pointer</span><span class="sxs-lookup"><span data-stu-id="bf3ca-156">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="bf3ca-157">Dirección del objeto de proceso en el kernel.</span><span class="sxs-lookup"><span data-stu-id="bf3ca-157">The address of the process object in the kernel.</span></span>

</dd> <dt>

<span data-ttu-id="bf3ca-158">UserSID</span><span class="sxs-lookup"><span data-stu-id="bf3ca-158">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bf3ca-159">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="bf3ca-159">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="bf3ca-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bf3ca-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bf3ca-161">Calificadores: WmiDataId(7), Extension("Sid")</span><span class="sxs-lookup"><span data-stu-id="bf3ca-161">Qualifiers: WmiDataId(7), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="bf3ca-162">Identificador de seguridad (SID) para el contexto de usuario en el que se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="bf3ca-162">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bf3ca-163">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bf3ca-163">Remarks</span></span>

<span data-ttu-id="bf3ca-164">Los tipos de eventos DCStart y DCEnd enumeran el proceso que se está ejecutando actualmente, incluidos los procesos inactivos y del sistema, en el momento en que se inicia y finaliza la sesión del kernel, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="bf3ca-164">The DCStart and DCEnd event types enumerate the process that are currently running, including idle and system process, at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf3ca-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf3ca-165">Requirements</span></span>



| <span data-ttu-id="bf3ca-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf3ca-166">Requirement</span></span> | <span data-ttu-id="bf3ca-167">Valor</span><span class="sxs-lookup"><span data-stu-id="bf3ca-167">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="bf3ca-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf3ca-168">Minimum supported client</span></span><br/> | <span data-ttu-id="bf3ca-169">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bf3ca-169">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bf3ca-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bf3ca-170">Minimum supported server</span></span><br/> | <span data-ttu-id="bf3ca-171">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bf3ca-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="bf3ca-172">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bf3ca-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf3ca-173">**Proceso**</span><span class="sxs-lookup"><span data-stu-id="bf3ca-173">**Process**</span></span>](process.md)
</dt> </dl>

 

 




