---
description: Esta clase es la clase de tipo de evento para los eventos de proceso. La siguiente sintaxis se simplifica desde el código MOF.
ms.assetid: ff5c1f64-2087-4238-81f9-6283f0f0e68a
title: Process_V2_TypeGroup1 (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Process_V2_TypeGroup1
- Process_V2_TypeGroup1.UniqueProcessKey
- Process_V2_TypeGroup1.ProcessId
- Process_V2_TypeGroup1.ParentId
- Process_V2_TypeGroup1.SessionId
- Process_V2_TypeGroup1.ExitStatus
- Process_V2_TypeGroup1.UserSID
- Process_V2_TypeGroup1.ImageFileName
- Process_V2_TypeGroup1.CommandLine
api_type:
- NA
api_location: ''
ms.openlocfilehash: 01da5a8254627d6378c9f99aa2ba36dc6714e6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985863"
---
# <a name="process_v2_typegroup1-class"></a><span data-ttu-id="a41f5-104">\_ \_ Clase TypeGroup1 de proceso V2</span><span class="sxs-lookup"><span data-stu-id="a41f5-104">Process\_V2\_TypeGroup1 class</span></span>

<span data-ttu-id="a41f5-105">Esta clase es la clase de tipo de evento para los eventos de proceso.</span><span class="sxs-lookup"><span data-stu-id="a41f5-105">This class is the event type class for process events.</span></span>

<span data-ttu-id="a41f5-106">La siguiente sintaxis se simplifica desde el código MOF.</span><span class="sxs-lookup"><span data-stu-id="a41f5-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="a41f5-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a41f5-107">Syntax</span></span>

``` syntax
[EventType{1, 2, 3, 4, 39}, EventTypeName{"Start", "End", "DCStart", "DCEnd", "Defunct"}]
class Process_V2_TypeGroup1 : Process_V2
{
  uint32 UniqueProcessKey;
  uint32 ProcessId;
  uint32 ParentId;
  uint32 SessionId;
  sint32 ExitStatus;
  object UserSID;
  string ImageFileName;
  string CommandLine;
};
```

## <a name="members"></a><span data-ttu-id="a41f5-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a41f5-108">Members</span></span>

<span data-ttu-id="a41f5-109">La **clase \_ \_ TypeGroup1 de Process V2** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a41f5-109">The **Process\_V2\_TypeGroup1** class has these types of members:</span></span>

-   [<span data-ttu-id="a41f5-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a41f5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a41f5-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a41f5-111">Properties</span></span>

<span data-ttu-id="a41f5-112">La **clase \_ \_ TypeGroup1 de proceso V2** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a41f5-112">The **Process\_V2\_TypeGroup1** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a41f5-113">CommandLine</span><span class="sxs-lookup"><span data-stu-id="a41f5-113">CommandLine</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a41f5-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a41f5-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a41f5-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a41f5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a41f5-116">Calificadores: WmiDataId (8), StringTermination ("NullTerminated"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="a41f5-116">Qualifiers: WmiDataId(8), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="a41f5-117">Línea de comandos completa del proceso.</span><span class="sxs-lookup"><span data-stu-id="a41f5-117">Full command line of the process.</span></span>

</dd> <dt>

<span data-ttu-id="a41f5-118">ExitStatus</span><span class="sxs-lookup"><span data-stu-id="a41f5-118">ExitStatus</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a41f5-119">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="a41f5-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="a41f5-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a41f5-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a41f5-121">Calificadores: WmiDataId (5)</span><span class="sxs-lookup"><span data-stu-id="a41f5-121">Qualifiers: WmiDataId(5)</span></span>
</dt> </dl>

<span data-ttu-id="a41f5-122">Estado de salida del proceso detenido.</span><span class="sxs-lookup"><span data-stu-id="a41f5-122">Exit status of the stopped process.</span></span>

</dd> <dt>

<span data-ttu-id="a41f5-123">ImageFileName</span><span class="sxs-lookup"><span data-stu-id="a41f5-123">ImageFileName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a41f5-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a41f5-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a41f5-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a41f5-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a41f5-126">Calificadores: WmiDataId (7), StringTermination ("NullTerminated")</span><span class="sxs-lookup"><span data-stu-id="a41f5-126">Qualifiers: WmiDataId(7), StringTermination("NullTerminated")</span></span>
</dt> </dl>

<span data-ttu-id="a41f5-127">Ruta de acceso al archivo ejecutable del proceso.</span><span class="sxs-lookup"><span data-stu-id="a41f5-127">Path to the executable file of the process.</span></span>

</dd> <dt>

<span data-ttu-id="a41f5-128">ParentId</span><span class="sxs-lookup"><span data-stu-id="a41f5-128">ParentId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a41f5-129">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a41f5-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a41f5-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a41f5-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a41f5-131">Calificadores: WmiDataId (3), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="a41f5-131">Qualifiers: WmiDataId(3), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="a41f5-132">Identificador único del proceso que crea este proceso.</span><span class="sxs-lookup"><span data-stu-id="a41f5-132">Unique identifier of the process that creates this process.</span></span> <span data-ttu-id="a41f5-133">Los números de identificador de proceso se reutilizan, por lo que solo identifican un proceso para la duración de ese proceso.</span><span class="sxs-lookup"><span data-stu-id="a41f5-133">Process identifier numbers are reused, so they only identify a process for the lifetime of that process.</span></span> <span data-ttu-id="a41f5-134">Es posible que el proceso identificado por ParentProcessId termine, de modo que ParentProcessId no puede hacer referencia a un proceso en ejecución.</span><span class="sxs-lookup"><span data-stu-id="a41f5-134">It is possible that the process identified by ParentProcessId is terminated, so ParentProcessId may not refer to a running process.</span></span> <span data-ttu-id="a41f5-135">También es posible que ParentProcessId haga referencia incorrectamente a un proceso que reutiliza un identificador de proceso.</span><span class="sxs-lookup"><span data-stu-id="a41f5-135">It is also possible that ParentProcessId incorrectly refers to a process that reuses a process identifier.</span></span>

</dd> <dt>

<span data-ttu-id="a41f5-136">ProcessId</span><span class="sxs-lookup"><span data-stu-id="a41f5-136">ProcessId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a41f5-137">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a41f5-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a41f5-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a41f5-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a41f5-139">Calificadores: WmiDataId (2), Format ("x")</span><span class="sxs-lookup"><span data-stu-id="a41f5-139">Qualifiers: WmiDataId(2), Format("x")</span></span>
</dt> </dl>

<span data-ttu-id="a41f5-140">Identificador de proceso global que puede usar para identificar un proceso.</span><span class="sxs-lookup"><span data-stu-id="a41f5-140">Global process identifier that you can use to identify a process.</span></span> <span data-ttu-id="a41f5-141">El valor es válido desde el momento en que se crea un proceso hasta que se termina.</span><span class="sxs-lookup"><span data-stu-id="a41f5-141">The value is valid from the time a process is created until it is terminated.</span></span>

</dd> <dt>

<span data-ttu-id="a41f5-142">SessionId</span><span class="sxs-lookup"><span data-stu-id="a41f5-142">SessionId</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a41f5-143">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a41f5-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a41f5-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a41f5-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a41f5-145">Calificadores: WmiDataId (4)</span><span class="sxs-lookup"><span data-stu-id="a41f5-145">Qualifiers: WmiDataId(4)</span></span>
</dt> </dl>

<span data-ttu-id="a41f5-146">Identificador único que genera un sistema operativo cuando crea una nueva sesión.</span><span class="sxs-lookup"><span data-stu-id="a41f5-146">Unique identifier that an operating system generates when it creates a new session.</span></span> <span data-ttu-id="a41f5-147">Una sesión abarca un período de tiempo desde el inicio de sesión hasta que se cierra la sesión desde un sistema específico.</span><span class="sxs-lookup"><span data-stu-id="a41f5-147">A session spans a period of time from log on until log off from a specific system.</span></span>

</dd> <dt>

<span data-ttu-id="a41f5-148">UniqueProcessKey</span><span class="sxs-lookup"><span data-stu-id="a41f5-148">UniqueProcessKey</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a41f5-149">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a41f5-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a41f5-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a41f5-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a41f5-151">Calificadores: WmiDataId (1), puntero</span><span class="sxs-lookup"><span data-stu-id="a41f5-151">Qualifiers: WmiDataId(1), Pointer</span></span>
</dt> </dl>

<span data-ttu-id="a41f5-152">La dirección del objeto de proceso en el kernel.</span><span class="sxs-lookup"><span data-stu-id="a41f5-152">The address of the process object in the kernel.</span></span>

</dd> <dt>

<span data-ttu-id="a41f5-153">UserSID</span><span class="sxs-lookup"><span data-stu-id="a41f5-153">UserSID</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a41f5-154">Tipo de datos: **objeto**</span><span class="sxs-lookup"><span data-stu-id="a41f5-154">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="a41f5-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a41f5-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a41f5-156">Calificadores: WmiDataId (6), extensión ("Sid")</span><span class="sxs-lookup"><span data-stu-id="a41f5-156">Qualifiers: WmiDataId(6), Extension("Sid")</span></span>
</dt> </dl>

<span data-ttu-id="a41f5-157">Identificador de seguridad (SID) del contexto de usuario en el que se produce el evento.</span><span class="sxs-lookup"><span data-stu-id="a41f5-157">Security identifier (SID) for the user context under which the event happens.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a41f5-158">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a41f5-158">Remarks</span></span>

<span data-ttu-id="a41f5-159">Los tipos de eventos DCStart y DCEnd enumeran el proceso que se está ejecutando actualmente, incluidos los procesos inactivos y del sistema, en el momento en que se inicia y finaliza la sesión del kernel, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a41f5-159">The DCStart and DCEnd event types enumerate the process that are currently running, including idle and system process, at the time the kernel session starts and ends, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="a41f5-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a41f5-160">Requirements</span></span>



| <span data-ttu-id="a41f5-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="a41f5-161">Requirement</span></span> | <span data-ttu-id="a41f5-162">Value</span><span class="sxs-lookup"><span data-stu-id="a41f5-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a41f5-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a41f5-163">Minimum supported client</span></span><br/> | <span data-ttu-id="a41f5-164">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a41f5-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a41f5-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a41f5-165">Minimum supported server</span></span><br/> | <span data-ttu-id="a41f5-166">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a41f5-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a41f5-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="a41f5-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a41f5-168">**Proceso \_ V2**</span><span class="sxs-lookup"><span data-stu-id="a41f5-168">**Process\_V2**</span></span>](process-v2.md)
</dt> </dl>

 

 




