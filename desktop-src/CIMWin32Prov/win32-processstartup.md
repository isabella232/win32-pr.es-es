---
description: La \_ clase WMI abstracta ProcessStartup de Win32 representa la configuración de inicio de un proceso basado en Windows.
ms.assetid: 78508404-cab2-42fb-a0ed-0e6e7d21408c
ms.tgt_platform: multiple
title: Win32_ProcessStartup (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProcessStartup
- Win32_ProcessStartup.CreateFlags
- Win32_ProcessStartup.EnvironmentVariables
- Win32_ProcessStartup.ErrorMode
- Win32_ProcessStartup.FillAttribute
- Win32_ProcessStartup.PriorityClass
- Win32_ProcessStartup.ShowWindow
- Win32_ProcessStartup.Title
- Win32_ProcessStartup.WinstationDesktop
- Win32_ProcessStartup.X
- Win32_ProcessStartup.XCountChars
- Win32_ProcessStartup.XSize
- Win32_ProcessStartup.Y
- Win32_ProcessStartup.YCountChars
- Win32_ProcessStartup.YSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8def1e7ff8e3011d5ca6c2df303818bea36eca65
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152859"
---
# <a name="win32_processstartup-class"></a><span data-ttu-id="f130b-103">\_Clase Win32 ProcessStartup</span><span class="sxs-lookup"><span data-stu-id="f130b-103">Win32\_ProcessStartup class</span></span>

<span data-ttu-id="f130b-104">La [clase WMI](../wmisdk/retrieving-a-class.md) abstracta **\_ ProcessStartup de Win32** representa la configuración de inicio de un proceso basado en Windows.</span><span class="sxs-lookup"><span data-stu-id="f130b-104">The **Win32\_ProcessStartup** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents the startup configuration of a Windows-based process.</span></span> <span data-ttu-id="f130b-105">La clase se define como una definición de tipo de método, lo que significa que solo se usa para pasar información al método [**Create**](create-method-in-class-win32-process.md) de la clase de [**\_ proceso de Win32**](win32-process.md) .</span><span class="sxs-lookup"><span data-stu-id="f130b-105">The class is defined as a method type definition, which means that it is only used for passing information to the [**Create**](create-method-in-class-win32-process.md) method of the [**Win32\_Process**](win32-process.md) class.</span></span>

<span data-ttu-id="f130b-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f130b-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f130b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f130b-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4DB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_ProcessStartup : Win32_MethodParameterClass
{
  uint32 CreateFlags;
  string EnvironmentVariables[];
  uint16 ErrorMode = 1;
  uint32 FillAttribute;
  uint32 PriorityClass;
  uint16 ShowWindow;
  string Title;
  string WinstationDesktop;
  uint32 X;
  uint32 XCountChars;
  uint32 XSize;
  uint32 Y;
  uint32 YCountChars;
  uint32 YSize;
};
```

## <a name="members"></a><span data-ttu-id="f130b-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f130b-108">Members</span></span>

<span data-ttu-id="f130b-109">La **clase \_ ProcessStartup de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f130b-109">The **Win32\_ProcessStartup** class has these types of members:</span></span>

-   [<span data-ttu-id="f130b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f130b-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f130b-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f130b-111">Properties</span></span>

<span data-ttu-id="f130b-112">La **clase \_ ProcessStartup de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f130b-112">The **Win32\_ProcessStartup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f130b-113">**CreateFlags**</span><span class="sxs-lookup"><span data-stu-id="f130b-113">**CreateFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f130b-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f130b-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f130b-115">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f130b-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f130b-116">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Functions \| [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) \| dwCreationFlags")</span><span class="sxs-lookup"><span data-stu-id="f130b-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Functions\|[**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)\|dwCreationFlags")</span></span>
</dt> </dl>

<span data-ttu-id="f130b-117">Valores adicionales que controlan la clase de prioridad y la creación del proceso.</span><span class="sxs-lookup"><span data-stu-id="f130b-117">Additional values that control the priority class and the creation of the process.</span></span> <span data-ttu-id="f130b-118">Los siguientes valores de creación se pueden especificar en cualquier combinación, a menos que se indique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="f130b-118">The following creation values can be specified in any combination, except as noted.</span></span>

<dt>

<span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>

<span data-ttu-id="f130b-119"><span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>**Depuración \_ Proceso** (1)</span><span class="sxs-lookup"><span data-stu-id="f130b-119"><span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>**Debug\_Process** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-120">Si se establece esta marca, el proceso de llamada se trata como un depurador y se depura el nuevo proceso.</span><span class="sxs-lookup"><span data-stu-id="f130b-120">If this flag is set, the calling process is treated as a debugger, and the new process is being debugged.</span></span> <span data-ttu-id="f130b-121">El sistema notifica al depurador todos los eventos de depuración que se producen en el proceso que se está depurando.</span><span class="sxs-lookup"><span data-stu-id="f130b-121">The system notifies the debugger of all debug events that occur in the process being debugged.</span></span>

</dd> <dt>

<span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>

<span data-ttu-id="f130b-122"><span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>**Depuración \_ Solo \_ este \_ proceso** (2)</span><span class="sxs-lookup"><span data-stu-id="f130b-122"><span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>**Debug\_Only\_This\_Process** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-123">Si no se establece esta marca y se depura el proceso de llamada, el nuevo proceso se convierte en otro proceso que se está depurando.</span><span class="sxs-lookup"><span data-stu-id="f130b-123">If this flag is not set and the calling process is being debugged, the new process becomes another process being debugged.</span></span> <span data-ttu-id="f130b-124">Si el proceso de llamada no es un proceso de depuración, no se produce ninguna acción relacionada con la depuración.</span><span class="sxs-lookup"><span data-stu-id="f130b-124">If the calling process is not a process of being debugged, no debugging-related actions occur.</span></span>

</dd> <dt>

<span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>

<span data-ttu-id="f130b-125"><span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>**Crear \_ Suspendido** (4)</span><span class="sxs-lookup"><span data-stu-id="f130b-125"><span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>**Create\_Suspended** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-126">El subproceso principal del nuevo proceso se crea en un estado suspendido y no se ejecuta hasta que se llama al método [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) .</span><span class="sxs-lookup"><span data-stu-id="f130b-126">The primary thread of the new process is created in a suspended state and does not run until the [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) method is called.</span></span>

</dd> <dt>

<span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>

<span data-ttu-id="f130b-127"><span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>**Separado \_ Proceso** (8)</span><span class="sxs-lookup"><span data-stu-id="f130b-127"><span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>**Detached\_Process** (8)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-128">En los procesos de la consola, el nuevo proceso no tiene acceso a la consola del proceso primario.</span><span class="sxs-lookup"><span data-stu-id="f130b-128">For console processes, the new process does not have access to the console of the parent process.</span></span> <span data-ttu-id="f130b-129">Esta marca no se puede usar si se establece la marca **crear \_ nueva \_ consola** .</span><span class="sxs-lookup"><span data-stu-id="f130b-129">This flag cannot be used if the **Create\_New\_Console** flag is set.</span></span>

</dd> <dt>

<span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>

<span data-ttu-id="f130b-130"><span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>**Crear \_ Nueva \_ consola** (16)</span><span class="sxs-lookup"><span data-stu-id="f130b-130"><span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>**Create\_New\_Console** (16)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-131">Este nuevo proceso tiene una nueva consola, en lugar de heredar la consola primaria.</span><span class="sxs-lookup"><span data-stu-id="f130b-131">This new process has a new console, instead of inheriting the parent console.</span></span> <span data-ttu-id="f130b-132">Esta marca no se puede usar con la marca de **\_ proceso desasociada** .</span><span class="sxs-lookup"><span data-stu-id="f130b-132">This flag cannot be used with the **Detached\_Process** flag.</span></span>

</dd> <dt>

<span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>

<span data-ttu-id="f130b-133"><span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>**Crear \_ Nuevo \_ \_ grupo de procesos** (512)</span><span class="sxs-lookup"><span data-stu-id="f130b-133"><span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>**Create\_New\_Process\_Group** (512)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-134">Este nuevo proceso es el proceso raíz de un nuevo grupo de procesos.</span><span class="sxs-lookup"><span data-stu-id="f130b-134">This new process is the root process of a new process group.</span></span> <span data-ttu-id="f130b-135">El grupo de procesos incluye todos los procesos descendientes de este proceso raíz.</span><span class="sxs-lookup"><span data-stu-id="f130b-135">The process group includes all of the processes that are descendants of this root process.</span></span> <span data-ttu-id="f130b-136">El identificador de proceso del nuevo grupo de procesos es el mismo que el identificador de proceso que se devuelve en la propiedad **ProcessId** de la clase de [**\_ proceso de Win32**](win32-process.md) .</span><span class="sxs-lookup"><span data-stu-id="f130b-136">The process identifier of the new process group is the same as the process identifier that is returned in the **ProcessID** property of the [**Win32\_Process**](win32-process.md) class.</span></span> <span data-ttu-id="f130b-137">El método [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) usa los grupos de procesos para habilitar el envío de una señal CTRL + C o una señal Ctrl + Inter a un grupo de procesos de consola.</span><span class="sxs-lookup"><span data-stu-id="f130b-137">Process groups are used by the [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) method to enable the sending of either a CTRL+C signal or a CTRL+BREAK signal to a group of console processes.</span></span>

</dd> <dt>

<span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>

<span data-ttu-id="f130b-138"><span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>**Crear \_ \_Entorno Unicode** (1024)</span><span class="sxs-lookup"><span data-stu-id="f130b-138"><span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>**Create\_Unicode\_Environment** (1024)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-139">La configuración del entorno que se muestra en la propiedad **EnvironmentVariables** utiliza caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="f130b-139">The environment settings listed in the **EnvironmentVariables** property use Unicode characters.</span></span> <span data-ttu-id="f130b-140">Si no se establece esta marca, el bloque de entorno utiliza caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="f130b-140">If this flag is not set, the environment block uses ANSI characters.</span></span>

</dd> <dt>

<span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>

<span data-ttu-id="f130b-141"><span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>**Crear \_ \_ \_ Modo de error predeterminado** (67108864)</span><span class="sxs-lookup"><span data-stu-id="f130b-141"><span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>**Create\_Default\_Error\_Mode** (67108864)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-142">A los procesos recién creados se les asigna el modo de error predeterminado del sistema del proceso de llamada en lugar de heredar el modo de error del proceso primario.</span><span class="sxs-lookup"><span data-stu-id="f130b-142">Newly created processes are given the system default error mode of the calling process instead of inheriting the error mode of the parent process.</span></span> <span data-ttu-id="f130b-143">Esta marca es útil para las aplicaciones de Shell multiproceso que se ejecutan con errores severos deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="f130b-143">This flag is useful for multithreaded shell applications that run with hard errors disabled.</span></span>

</dd> <dt>

<span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>

<span data-ttu-id="f130b-144"><span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>**Crear \_ SEPARACIÓN \_ del \_ trabajo** (16777216)</span><span class="sxs-lookup"><span data-stu-id="f130b-144"><span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>**CREATE\_BREAKAWAY\_FROM\_JOB** (16777216)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-145">Se usa para que el proceso creado no esté limitado por el objeto de trabajo.</span><span class="sxs-lookup"><span data-stu-id="f130b-145">Used for the created process not to be limited by the job object.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f130b-146">**EnvironmentVariables**</span><span class="sxs-lookup"><span data-stu-id="f130b-146">**EnvironmentVariables**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f130b-147">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="f130b-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f130b-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f130b-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f130b-149">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ Current \_ User \\ \\ Environment")</span><span class="sxs-lookup"><span data-stu-id="f130b-149">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HKEY\_CURRENT\_USER\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="f130b-150">Lista de valores para la configuración de un equipo.</span><span class="sxs-lookup"><span data-stu-id="f130b-150">List of settings for the configuration of a computer.</span></span> <span data-ttu-id="f130b-151">Las variables de entorno especifican rutas de acceso de búsqueda para archivos, directorios para archivos temporales, opciones específicas de la aplicación y otra información similar.</span><span class="sxs-lookup"><span data-stu-id="f130b-151">Environment variables specify search paths for files, directories for temporary files, application-specific options, and other similar information.</span></span> <span data-ttu-id="f130b-152">El sistema mantiene un bloque de configuración del entorno para cada usuario y uno para el equipo.</span><span class="sxs-lookup"><span data-stu-id="f130b-152">The system maintains a block of environment settings for each user and one for the computer.</span></span> <span data-ttu-id="f130b-153">El bloque de entorno del sistema representa las variables de entorno para todos los usuarios de un equipo específico.</span><span class="sxs-lookup"><span data-stu-id="f130b-153">The system environment block represents environment variables for all of the users of a specific computer.</span></span> <span data-ttu-id="f130b-154">El bloque de entorno de un usuario representa las variables de entorno que el sistema mantiene para un usuario específico e incluye el conjunto de variables de entorno del sistema.</span><span class="sxs-lookup"><span data-stu-id="f130b-154">A user's environment block represents the environment variables that the system maintains for a specific user, and includes the set of system environment variables.</span></span> <span data-ttu-id="f130b-155">De forma predeterminada, cada proceso recibe una copia del bloque de entorno para su proceso primario.</span><span class="sxs-lookup"><span data-stu-id="f130b-155">By default, each process receives a copy of the environment block for its parent process.</span></span> <span data-ttu-id="f130b-156">Normalmente, es el bloque de entorno para el usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="f130b-156">Typically, this is the environment block for the user who is logged on.</span></span> <span data-ttu-id="f130b-157">Un proceso puede especificar distintos bloques de entorno para sus procesos secundarios.</span><span class="sxs-lookup"><span data-stu-id="f130b-157">A process can specify different environment blocks for its child processes.</span></span>

</dd> <dt>

<span data-ttu-id="f130b-158">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="f130b-158">**ErrorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f130b-159">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f130b-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f130b-160">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f130b-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f130b-161">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| error Functions \| SetErrorMode")</span><span class="sxs-lookup"><span data-stu-id="f130b-161">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Error Functions\|SetErrorMode")</span></span>
</dt> </dl>

<span data-ttu-id="f130b-162">En algunos procesadores que no son x86, las referencias de memoria mal alineadas causan una excepción de error de alineación.</span><span class="sxs-lookup"><span data-stu-id="f130b-162">On some non-x86 processors, misaligned memory references cause an alignment fault exception.</span></span> <span data-ttu-id="f130b-163">La marca no se produce un **\_ error de alineación, \_ \_ excepto** que le permite controlar si un sistema operativo corrige automáticamente o no dichos errores de alineación o hace que sean visibles para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="f130b-163">The **No\_Alignment\_Fault\_Except** flag lets you control whether or not an operating system automatically fixes such alignment faults, or makes them visible to an application.</span></span> <span data-ttu-id="f130b-164">En una plataforma de millones de instrucciones por segundo (MIPS), una aplicación debe llamar explícitamente a [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) con el indicador de **no hay ningún \_ error de alineación \_ \_ excepto** para que el sistema operativo corrija automáticamente los errores de alineación.</span><span class="sxs-lookup"><span data-stu-id="f130b-164">On a millions of instructions per second (MIPS) platform, an application must explicitly call [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) with the **No\_Alignment\_Fault\_Except** flag to have the operating system automatically fix alignment faults.</span></span>

<span data-ttu-id="f130b-165">Cómo un sistema operativo procesa varios tipos de errores graves.</span><span class="sxs-lookup"><span data-stu-id="f130b-165">How an operating system processes several types of serious errors.</span></span> <span data-ttu-id="f130b-166">Puede especificar que los errores del proceso del sistema operativo o una aplicación pueden recibir y procesar errores.</span><span class="sxs-lookup"><span data-stu-id="f130b-166">You can specify that the operating system process errors, or an application can receive and process errors.</span></span>

<span data-ttu-id="f130b-167">La configuración predeterminada es que el sistema operativo cree errores de alineación visibles para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="f130b-167">The default setting is for the operating system to make alignment faults visible to an application.</span></span> <span data-ttu-id="f130b-168">Dado que la plataforma x86 no hace que los errores de alineación sean visibles para una aplicación, la marca no se produce un error de **\_ alineación, \_ \_ excepto** si la marca no se establece.</span><span class="sxs-lookup"><span data-stu-id="f130b-168">Because the x86 platform does not make alignment faults visible to an application, the **No\_Alignment\_Fault\_Except** flag does not make the operating system raise an alignment fault error—even if the flag is not set.</span></span> <span data-ttu-id="f130b-169">El estado predeterminado de [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) es establecer todas las marcas en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="f130b-169">The default state for [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) is to set all of the flags to 0 (zero).</span></span>

<dt>



 <span data-ttu-id="f130b-170">(1)</span><span class="sxs-lookup"><span data-stu-id="f130b-170">(1)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-171">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="f130b-171">Default</span></span>

</dd> <dt>

<span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>

<span data-ttu-id="f130b-172"><span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>**Error \_ \_Errores críticos** (2)</span><span class="sxs-lookup"><span data-stu-id="f130b-172"><span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>**Fail\_Critical\_Errors** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-173">Si se establece esta marca, el sistema operativo no muestra el cuadro de mensaje del controlador de errores críticos cuando se produce este tipo de error.</span><span class="sxs-lookup"><span data-stu-id="f130b-173">If this flag is set, the operating system does not display the critical error handler message box when such an error occurs.</span></span> <span data-ttu-id="f130b-174">En su lugar, el sistema operativo envía el error al proceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="f130b-174">Instead, the operating system sends the error to the calling process.</span></span>

</dd> <dt>

<span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>

<span data-ttu-id="f130b-175"><span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>**No \_ Error de alineación \_ \_ excepto** (4)</span><span class="sxs-lookup"><span data-stu-id="f130b-175"><span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>**No\_Alignment\_Fault\_Except** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-176">Si se establece esta marca, el sistema operativo corrige automáticamente los errores de alineación de memoria y hace que sean invisibles para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f130b-176">If this flag is set, the operating system automatically fixes memory alignment faults and makes them invisible to the application.</span></span> <span data-ttu-id="f130b-177">Lo hace para los procesos de llamada y descendientes.</span><span class="sxs-lookup"><span data-stu-id="f130b-177">It does this for the calling and descendant processes.</span></span> <span data-ttu-id="f130b-178">Esta marca se aplica solo a la tecnología de conjunto de instrucciones reducida (RISC) y no tiene ningún efecto en los procesadores x86.</span><span class="sxs-lookup"><span data-stu-id="f130b-178">This flag applies to reduced instruction set computing (RISC) only, and has no effect on x86 processors.</span></span>

</dd> <dt>

<span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>

<span data-ttu-id="f130b-179"><span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>**No \_ \_ \_ \_ Cuadro error de GP** (8)</span><span class="sxs-lookup"><span data-stu-id="f130b-179"><span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>**No\_GP\_Fault\_Error\_Box** (8)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-180">Si se establece esta marca, el sistema operativo no muestra el cuadro de mensaje de error de protección general (GP) cuando se produce un error de GP.</span><span class="sxs-lookup"><span data-stu-id="f130b-180">If this flag is set, the operating system does not display the general protection (GP) fault message box when a GP error occurs.</span></span> <span data-ttu-id="f130b-181">Esta marca solo debe establecerse mediante la depuración de aplicaciones que controlen errores de GP.</span><span class="sxs-lookup"><span data-stu-id="f130b-181">This flag should only be set by debugging applications that handle GP errors.</span></span>

</dd> <dt>

<span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>

<span data-ttu-id="f130b-182"><span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>**No \_ \_Cuadro de \_ error \_ de abrir archivo** (16)</span><span class="sxs-lookup"><span data-stu-id="f130b-182"><span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>**No\_Open\_File\_Error\_Box** (16)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-183">Si se establece esta marca, el sistema operativo no mostrará un cuadro de mensaje cuando no encuentre un archivo.</span><span class="sxs-lookup"><span data-stu-id="f130b-183">If this flag is set, the operating system does not display a message box when it fails to find a file.</span></span> <span data-ttu-id="f130b-184">En su lugar, el error se devuelve al proceso de llamada.</span><span class="sxs-lookup"><span data-stu-id="f130b-184">Instead, the error is returned to the calling process.</span></span> <span data-ttu-id="f130b-185">Esta marca se omite actualmente.</span><span class="sxs-lookup"><span data-stu-id="f130b-185">This flag is currently ignored.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f130b-186">**FillAttribute**</span><span class="sxs-lookup"><span data-stu-id="f130b-186">**FillAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f130b-187">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f130b-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f130b-188">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f130b-188">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f130b-189">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwFillAttribute")</span><span class="sxs-lookup"><span data-stu-id="f130b-189">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwFillAttribute")</span></span>
</dt> </dl>

<span data-ttu-id="f130b-190">Los colores de texto y de fondo si se crea una nueva ventana de consola en una aplicación de consola.</span><span class="sxs-lookup"><span data-stu-id="f130b-190">The text and background colors if a new console window is created in a console application.</span></span> <span data-ttu-id="f130b-191">Estos valores se omiten en las aplicaciones de la interfaz gráfica de usuario (GUI).</span><span class="sxs-lookup"><span data-stu-id="f130b-191">These values are ignored in graphical user interface (GUI) applications.</span></span> <span data-ttu-id="f130b-192">Para especificar los colores de primer plano y de fondo, agregue los valores juntos.</span><span class="sxs-lookup"><span data-stu-id="f130b-192">To specify both foreground and background colors, add the values together.</span></span> <span data-ttu-id="f130b-193">Por ejemplo, para tener el tipo rojo (4) en un fondo azul (16), establezca FillAttribute en 20.</span><span class="sxs-lookup"><span data-stu-id="f130b-193">For example, to have red type (4) on a blue background (16), set the FillAttribute to 20.</span></span>

<dt>

<span data-ttu-id="f130b-194">1</span><span class="sxs-lookup"><span data-stu-id="f130b-194">1</span></span>
</dt> <dd>

<span data-ttu-id="f130b-195">Azul de primer plano \_</span><span class="sxs-lookup"><span data-stu-id="f130b-195">Foreground\_Blue</span></span>

</dd> <dt>

<span data-ttu-id="f130b-196">2</span><span class="sxs-lookup"><span data-stu-id="f130b-196">2</span></span>
</dt> <dd>

<span data-ttu-id="f130b-197">Verde de primer plano \_</span><span class="sxs-lookup"><span data-stu-id="f130b-197">Foreground\_Green</span></span>

</dd> <dt>

<span data-ttu-id="f130b-198">4</span><span class="sxs-lookup"><span data-stu-id="f130b-198">4</span></span>
</dt> <dd>

<span data-ttu-id="f130b-199">Rojo de primer plano \_</span><span class="sxs-lookup"><span data-stu-id="f130b-199">Foreground\_Red</span></span>

</dd> <dt>

<span data-ttu-id="f130b-200">8</span><span class="sxs-lookup"><span data-stu-id="f130b-200">8</span></span>
</dt> <dd>

<span data-ttu-id="f130b-201">Intensidad de primer plano \_</span><span class="sxs-lookup"><span data-stu-id="f130b-201">Foreground\_Intensity</span></span>

</dd> <dt>

<span data-ttu-id="f130b-202">16</span><span class="sxs-lookup"><span data-stu-id="f130b-202">16</span></span>
</dt> <dd>

<span data-ttu-id="f130b-203">Azul de fondo \_</span><span class="sxs-lookup"><span data-stu-id="f130b-203">Background\_Blue</span></span>

</dd> <dt>

<span data-ttu-id="f130b-204">32</span><span class="sxs-lookup"><span data-stu-id="f130b-204">32</span></span>
</dt> <dd>

<span data-ttu-id="f130b-205">Verde de fondo \_</span><span class="sxs-lookup"><span data-stu-id="f130b-205">Background\_Green</span></span>

</dd> <dt>

<span data-ttu-id="f130b-206">64</span><span class="sxs-lookup"><span data-stu-id="f130b-206">64</span></span>
</dt> <dd>

<span data-ttu-id="f130b-207">Rojo de fondo \_</span><span class="sxs-lookup"><span data-stu-id="f130b-207">Background\_Red</span></span>

</dd> <dt>

<span data-ttu-id="f130b-208">128</span><span class="sxs-lookup"><span data-stu-id="f130b-208">128</span></span>
</dt> <dd>

<span data-ttu-id="f130b-209">Intensidad de fondo \_</span><span class="sxs-lookup"><span data-stu-id="f130b-209">Background\_Intensity</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f130b-210">**PriorityClass**</span><span class="sxs-lookup"><span data-stu-id="f130b-210">**PriorityClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f130b-211">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f130b-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f130b-212">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f130b-212">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f130b-213">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| proceso y estructuras de subproceso \| [**JOBOBJECT \_ \_ \_ información básica de límite**](/windows/win32/api/winnt/ns-winnt-jobobject_basic_limit_information) \| PriorityClass")</span><span class="sxs-lookup"><span data-stu-id="f130b-213">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**JOBOBJECT\_BASIC\_LIMIT\_INFORMATION**](/windows/win32/api/winnt/ns-winnt-jobobject_basic_limit_information)\|PriorityClass")</span></span>
</dt> </dl>

<span data-ttu-id="f130b-214">Clase de prioridad del nuevo proceso.</span><span class="sxs-lookup"><span data-stu-id="f130b-214">Priority class of the new process.</span></span> <span data-ttu-id="f130b-215">Utilice esta propiedad para determinar las prioridades de programación de los subprocesos del proceso.</span><span class="sxs-lookup"><span data-stu-id="f130b-215">Use this property to determine the schedule priorities of the threads in the process.</span></span> <span data-ttu-id="f130b-216">Si la propiedad es null, el valor predeterminado de la clase Priority es normal, a menos que la clase de prioridad del proceso de creación esté inactiva o por debajo de lo \_ normal.</span><span class="sxs-lookup"><span data-stu-id="f130b-216">If the property is left null, the priority class defaults to Normal—unless the priority class of the creating process is Idle or Below\_Normal.</span></span> <span data-ttu-id="f130b-217">En estos casos, el proceso secundario recibe la clase de prioridad predeterminada del proceso de llamada.</span><span class="sxs-lookup"><span data-stu-id="f130b-217">In these cases, the child process receives the default priority class of the calling process.</span></span>

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="f130b-218"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)</span><span class="sxs-lookup"><span data-stu-id="f130b-218"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-219">Indica un proceso normal sin necesidad de una programación especial.</span><span class="sxs-lookup"><span data-stu-id="f130b-219">Indicates a normal process with no special schedule needs.</span></span>

</dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="f130b-220"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Inactivo** (64)</span><span class="sxs-lookup"><span data-stu-id="f130b-220"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Idle** (64)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-221">Indica un proceso con subprocesos que se ejecutan solo cuando el sistema está inactivo y son retenidos por los subprocesos de cualquier proceso que se ejecute en una clase de prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="f130b-221">Indicates a process with threads that run only when the system is idle and are preempted by the threads of any process running in a higher priority class.</span></span> <span data-ttu-id="f130b-222">Un ejemplo es un protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="f130b-222">An example is a screen saver.</span></span> <span data-ttu-id="f130b-223">Los procesos secundarios heredan la clase de prioridad inactiva.</span><span class="sxs-lookup"><span data-stu-id="f130b-223">The idle priority class is inherited by child processes.</span></span>

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="f130b-224"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**Alto** (128)</span><span class="sxs-lookup"><span data-stu-id="f130b-224"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (128)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-225">Indica un proceso que realiza tareas críticas en el tiempo que se deben ejecutar inmediatamente para ejecutarse correctamente.</span><span class="sxs-lookup"><span data-stu-id="f130b-225">Indicates a process that performs time-critical tasks that must be executed immediately to run correctly.</span></span> <span data-ttu-id="f130b-226">Los subprocesos de un proceso de clase de prioridad alta tienen preferencia sobre los subprocesos de los procesos de clase de prioridad normal o de prioridad inactiva.</span><span class="sxs-lookup"><span data-stu-id="f130b-226">The threads of a high-priority class process preempt the threads of normal-priority or idle-priority class processes.</span></span> <span data-ttu-id="f130b-227">Un ejemplo es Windows Lista de tareas, que debe responder rápidamente cuando el usuario lo llama, independientemente de la carga del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f130b-227">An example is Windows Task List, which must respond quickly when called by the user, regardless of the load on the operating system.</span></span> <span data-ttu-id="f130b-228">Extreme las precauciones al usar la clase de prioridad alta, ya que una aplicación de alta prioridad enlazada a la CPU puede usar casi todos los ciclos disponibles.</span><span class="sxs-lookup"><span data-stu-id="f130b-228">Use extreme care when using the high-priority class, because a high-priority class CPU-bound application can use nearly all of the available cycles.</span></span> <span data-ttu-id="f130b-229">Solo los subprocesos de prioridad en tiempo real se establecen en este nivel.</span><span class="sxs-lookup"><span data-stu-id="f130b-229">Only a real-time priority preempts threads set to this level.</span></span>

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span data-ttu-id="f130b-230"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Tiempo real** (256)</span><span class="sxs-lookup"><span data-stu-id="f130b-230"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Realtime** (256)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-231">Indica un proceso que tiene la prioridad más alta posible.</span><span class="sxs-lookup"><span data-stu-id="f130b-231">Indicates a process that has the highest possible priority.</span></span> <span data-ttu-id="f130b-232">Los subprocesos de un proceso de clase de prioridad en tiempo real tienen preferencia sobre los subprocesos de todos los demás procesos, incluidos los subprocesos de alta prioridad y los procesos del sistema operativo que realizan tareas importantes.</span><span class="sxs-lookup"><span data-stu-id="f130b-232">The threads of a real-time priority class process preempt the threads of all other processes—including high-priority threads and operating system processes performing important tasks.</span></span> <span data-ttu-id="f130b-233">Por ejemplo, un proceso en tiempo real que se ejecuta durante más de un intervalo muy breve puede hacer que las cachés del disco no se vacíen o hacer que el mouse deje de responder.</span><span class="sxs-lookup"><span data-stu-id="f130b-233">For example, a real-time process that executes for more than a very brief interval can cause disk caches not to flush, or cause a mouse to be unresponsive.</span></span>

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span data-ttu-id="f130b-234"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**A continuación \_ Normal** (16384)</span><span class="sxs-lookup"><span data-stu-id="f130b-234"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Below\_Normal** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-235">Indica un proceso que tiene una prioridad mayor que inactiva pero menor que normal.</span><span class="sxs-lookup"><span data-stu-id="f130b-235">Indicates a process that has a priority higher than Idle but lower than Normal.</span></span>

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span data-ttu-id="f130b-236"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Por encima \_ Normal** (32768)</span><span class="sxs-lookup"><span data-stu-id="f130b-236"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Above\_Normal** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-237">Indica un proceso que tiene una prioridad mayor que el normal pero menor que el alto.</span><span class="sxs-lookup"><span data-stu-id="f130b-237">Indicates a process that has a priority higher than Normal but lower than High.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f130b-238">**ShowWindow**</span><span class="sxs-lookup"><span data-stu-id="f130b-238">**ShowWindow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f130b-239">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f130b-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f130b-240">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f130b-240">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f130b-241">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| wShowWindow")</span><span class="sxs-lookup"><span data-stu-id="f130b-241">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|wShowWindow")</span></span>
</dt> </dl>

<span data-ttu-id="f130b-242">Cómo se muestra la ventana al usuario.</span><span class="sxs-lookup"><span data-stu-id="f130b-242">How the window is displayed to the user.</span></span>

<dt>

<span id="SW_HIDE"></span><span id="sw_hide"></span>

<span data-ttu-id="f130b-243"><span id="SW_HIDE"></span><span id="sw_hide"></span>**SW \_ OCULTAR** (0)</span><span class="sxs-lookup"><span data-stu-id="f130b-243"><span id="SW_HIDE"></span><span id="sw_hide"></span>**SW\_HIDE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-244">Oculta la ventana y activa otra ventana.</span><span class="sxs-lookup"><span data-stu-id="f130b-244">Hides the window and activates another window.</span></span>

</dd> <dt>

<span id="SW_NORMAL"></span><span id="sw_normal"></span>

<span data-ttu-id="f130b-245"><span id="SW_NORMAL"></span><span id="sw_normal"></span>**SW \_ NORMAL** (1)</span><span class="sxs-lookup"><span data-stu-id="f130b-245"><span id="SW_NORMAL"></span><span id="sw_normal"></span>**SW\_NORMAL** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-246">Activa y muestra una ventana.</span><span class="sxs-lookup"><span data-stu-id="f130b-246">Activates and displays a window.</span></span> <span data-ttu-id="f130b-247">Si la ventana está minimizada o maximizada, el sistema la restaura en el tamaño y la posición originales.</span><span class="sxs-lookup"><span data-stu-id="f130b-247">If the window is minimized or maximized, the system restores it to the original size and position.</span></span> <span data-ttu-id="f130b-248">Una aplicación especifica esta marca cuando se muestra la ventana por primera vez.</span><span class="sxs-lookup"><span data-stu-id="f130b-248">An application specifies this flag when displaying the window for the first time.</span></span>

</dd> <dt>

<span id="SW_SHOWMINIMIZED"></span><span id="sw_showminimized"></span>

<span data-ttu-id="f130b-249"><span id="SW_SHOWMINIMIZED"></span><span id="sw_showminimized"></span>**SW \_ SHOWMINIMIZED** (2)</span><span class="sxs-lookup"><span data-stu-id="f130b-249"><span id="SW_SHOWMINIMIZED"></span><span id="sw_showminimized"></span>**SW\_SHOWMINIMIZED** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-250">Activa la ventana y la muestra como una ventana minimizada.</span><span class="sxs-lookup"><span data-stu-id="f130b-250">Activates the window, and displays it as a minimized window.</span></span>

</dd> <dt>

<span id="SW_SHOWMAXIMIZED"></span><span id="sw_showmaximized"></span>

<span data-ttu-id="f130b-251"><span id="SW_SHOWMAXIMIZED"></span><span id="sw_showmaximized"></span>**SW \_ SHOWMAXIMIZED** (3)</span><span class="sxs-lookup"><span data-stu-id="f130b-251"><span id="SW_SHOWMAXIMIZED"></span><span id="sw_showmaximized"></span>**SW\_SHOWMAXIMIZED** (3)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-252">Activa la ventana y la muestra como una ventana maximizada.</span><span class="sxs-lookup"><span data-stu-id="f130b-252">Activates the window, and displays it as a maximized window.</span></span>

</dd> <dt>

<span id="SW_SHOWNOACTIVATE"></span><span id="sw_shownoactivate"></span>

<span data-ttu-id="f130b-253"><span id="SW_SHOWNOACTIVATE"></span><span id="sw_shownoactivate"></span>**SW \_ SHOWNOACTIVATE** (4)</span><span class="sxs-lookup"><span data-stu-id="f130b-253"><span id="SW_SHOWNOACTIVATE"></span><span id="sw_shownoactivate"></span>**SW\_SHOWNOACTIVATE** (4)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-254">Muestra una ventana en su tamaño y posición más recientes.</span><span class="sxs-lookup"><span data-stu-id="f130b-254">Displays a window in its most recent size and position.</span></span> <span data-ttu-id="f130b-255">Este valor es similar a **SW \_ normal**, salvo que la ventana no está activada.</span><span class="sxs-lookup"><span data-stu-id="f130b-255">This value is similar to **SW\_NORMAL**, except that the window is not activated.</span></span>

</dd> <dt>

<span id="SW_SHOW"></span><span id="sw_show"></span>

<span data-ttu-id="f130b-256"><span id="SW_SHOW"></span><span id="sw_show"></span>**SW \_ Mostrar** (5)</span><span class="sxs-lookup"><span data-stu-id="f130b-256"><span id="SW_SHOW"></span><span id="sw_show"></span>**SW\_SHOW** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-257">Activa la ventana y la muestra en el tamaño y la posición actuales.</span><span class="sxs-lookup"><span data-stu-id="f130b-257">Activates the window, and displays it at the current size and position.</span></span>

</dd> <dt>

<span id="SW_MINIMIZE"></span><span id="sw_minimize"></span>

<span data-ttu-id="f130b-258"><span id="SW_MINIMIZE"></span><span id="sw_minimize"></span>**SW \_ MINIMIZAR** (6)</span><span class="sxs-lookup"><span data-stu-id="f130b-258"><span id="SW_MINIMIZE"></span><span id="sw_minimize"></span>**SW\_MINIMIZE** (6)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-259">Minimiza la ventana especificada y activa la ventana de nivel superior siguiente en el orden Z.</span><span class="sxs-lookup"><span data-stu-id="f130b-259">Minimizes the specified window, and activates the next top-level window in the Z order.</span></span>

</dd> <dt>

<span id="SW_SHOWMINNOACTIVE"></span><span id="sw_showminnoactive"></span>

<span data-ttu-id="f130b-260"><span id="SW_SHOWMINNOACTIVE"></span><span id="sw_showminnoactive"></span>**SW \_ SHOWMINNOACTIVE** (7)</span><span class="sxs-lookup"><span data-stu-id="f130b-260"><span id="SW_SHOWMINNOACTIVE"></span><span id="sw_showminnoactive"></span>**SW\_SHOWMINNOACTIVE** (7)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-261">Muestra la ventana como una ventana minimizada.</span><span class="sxs-lookup"><span data-stu-id="f130b-261">Displays the window as a minimized window.</span></span> <span data-ttu-id="f130b-262">Este valor es similar a **SW \_ SHOWMINIMZED**, con la excepción de que la ventana no está activada.</span><span class="sxs-lookup"><span data-stu-id="f130b-262">This value is similar to **SW\_SHOWMINIMZED**, except that the window is not activated.</span></span>

</dd> <dt>

<span id="SW_SHOWNA"></span><span id="sw_showna"></span>

<span data-ttu-id="f130b-263"><span id="SW_SHOWNA"></span><span id="sw_showna"></span>**SW \_ MOSTRADO** (8)</span><span class="sxs-lookup"><span data-stu-id="f130b-263"><span id="SW_SHOWNA"></span><span id="sw_showna"></span>**SW\_SHOWNA** (8)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-264">Muestra la ventana en el tamaño y la posición actuales.</span><span class="sxs-lookup"><span data-stu-id="f130b-264">Displays the window at the current size and position.</span></span> <span data-ttu-id="f130b-265">Este valor es similar a **SW \_ Show**, salvo que la ventana no está activada.</span><span class="sxs-lookup"><span data-stu-id="f130b-265">This value is similar to **SW\_SHOW**, except that the window is not activated.</span></span>

</dd> <dt>

<span id="SW_RESTORE"></span><span id="sw_restore"></span>

<span data-ttu-id="f130b-266"><span id="SW_RESTORE"></span><span id="sw_restore"></span>**SW \_ RESTOre** (9)</span><span class="sxs-lookup"><span data-stu-id="f130b-266"><span id="SW_RESTORE"></span><span id="sw_restore"></span>**SW\_RESTORE** (9)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-267">Activa y muestra la ventana.</span><span class="sxs-lookup"><span data-stu-id="f130b-267">Activates and displays the window.</span></span> <span data-ttu-id="f130b-268">Si la ventana está minimizada o maximizada, el sistema la restaura en el tamaño y la posición originales.</span><span class="sxs-lookup"><span data-stu-id="f130b-268">If the window is minimized or maximized, the system restores it to the original size and position.</span></span> <span data-ttu-id="f130b-269">Una aplicación especifica esta marca al restaurar una ventana minimizada.</span><span class="sxs-lookup"><span data-stu-id="f130b-269">An application specifies this flag when restoring a minimized window.</span></span>

</dd> <dt>

<span id="SW_SHOWDEFAULT"></span><span id="sw_showdefault"></span>

<span data-ttu-id="f130b-270"><span id="SW_SHOWDEFAULT"></span><span id="sw_showdefault"></span>**SW \_ SHOWDEFAULT** (10)</span><span class="sxs-lookup"><span data-stu-id="f130b-270"><span id="SW_SHOWDEFAULT"></span><span id="sw_showdefault"></span>**SW\_SHOWDEFAULT** (10)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-271">Establece el estado de la presentación basándose en el valor \**SW \_ \** _ que se especifica en la estructura [_ *STARTUPINFO* \*](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) pasada a la función [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) por el programa que inicia la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f130b-271">Sets the show state based on the \**SW\_\** _ value that is specified in the [_ *STARTUPINFO*\*](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) structure passed to the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function by the program that starts the application.</span></span>

</dd> <dt>

<span id="SW_FORCEMINIMIZE"></span><span id="sw_forceminimize"></span>

<span data-ttu-id="f130b-272"><span id="SW_FORCEMINIMIZE"></span><span id="sw_forceminimize"></span>**SW \_ FORCEMINIMIZE** (11)</span><span class="sxs-lookup"><span data-stu-id="f130b-272"><span id="SW_FORCEMINIMIZE"></span><span id="sw_forceminimize"></span>**SW\_FORCEMINIMIZE** (11)</span></span>


</dt> <dd>

<span data-ttu-id="f130b-273">Minimiza una ventana, incluso cuando el subproceso que posee la ventana deja de responder.</span><span class="sxs-lookup"><span data-stu-id="f130b-273">Minimizes a window, even when the thread that owns the window stops responding.</span></span> <span data-ttu-id="f130b-274">Use esta marca solo al minimizar Windows desde un subproceso diferente.</span><span class="sxs-lookup"><span data-stu-id="f130b-274">Only use this flag when minimizing windows from a different thread.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f130b-275">**Título**</span><span class="sxs-lookup"><span data-stu-id="f130b-275">**Title**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f130b-276">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f130b-276">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f130b-277">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f130b-277">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f130b-278">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lpTitle")</span><span class="sxs-lookup"><span data-stu-id="f130b-278">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|lpTitle")</span></span>
</dt> </dl>

<span data-ttu-id="f130b-279">Texto que se muestra en la barra de título cuando se crea una nueva ventana de consola. se usa para los procesos de la consola.</span><span class="sxs-lookup"><span data-stu-id="f130b-279">Text displayed in the title bar when a new console window is created; used for console processes.</span></span> <span data-ttu-id="f130b-280">Si es **null**, se usa el nombre del archivo ejecutable como título de la ventana.</span><span class="sxs-lookup"><span data-stu-id="f130b-280">If **NULL**, the name of the executable file is used as the window title.</span></span> <span data-ttu-id="f130b-281">Esta propiedad debe ser **null** para los procesos de la GUI o de la consola que no crean una nueva ventana de consola.</span><span class="sxs-lookup"><span data-stu-id="f130b-281">This property must be **NULL** for GUI or console processes that do not create a new console window.</span></span>

</dd> <dt>

<span data-ttu-id="f130b-282">**WinstationDesktop**</span><span class="sxs-lookup"><span data-stu-id="f130b-282">**WinstationDesktop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f130b-283">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f130b-283">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f130b-284">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f130b-284">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f130b-285">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lpDesktop")</span><span class="sxs-lookup"><span data-stu-id="f130b-285">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|lpDesktop")</span></span>
</dt> </dl>

<span data-ttu-id="f130b-286">El nombre del escritorio o el nombre del escritorio y de la estación de ventana para el proceso.</span><span class="sxs-lookup"><span data-stu-id="f130b-286">The name of the desktop or the name of both the desktop and window station for the process.</span></span> <span data-ttu-id="f130b-287">Una barra diagonal inversa en la cadena indica que la cadena incluye nombres de estaciones de escritorio y de ventanas.</span><span class="sxs-lookup"><span data-stu-id="f130b-287">A backslash in the string indicates that the string includes both desktop and window station names.</span></span> <span data-ttu-id="f130b-288">Si **WinstationDesktop** es **null**, el nuevo proceso hereda el escritorio y la estación de ventana de su proceso principal.</span><span class="sxs-lookup"><span data-stu-id="f130b-288">If **WinstationDesktop** is **NULL**, the new process inherits the desktop and window station of its parent process.</span></span> <span data-ttu-id="f130b-289">Si **WinstationDesktop** es una cadena vacía, el proceso no hereda el escritorio y la estación de ventana de su proceso principal.</span><span class="sxs-lookup"><span data-stu-id="f130b-289">If **WinstationDesktop** is an empty string, the process does not inherit the desktop and window station of its parent process.</span></span> <span data-ttu-id="f130b-290">El sistema determina si se debe crear un nuevo escritorio y una estación de ventana.</span><span class="sxs-lookup"><span data-stu-id="f130b-290">The system determines if a new desktop and window station must be created.</span></span> <span data-ttu-id="f130b-291">Una estación de ventana es un objeto seguro que contiene un portapapeles, un conjunto de átomos globales y un grupo de objetos de escritorio.</span><span class="sxs-lookup"><span data-stu-id="f130b-291">A window station is a secure object that contains a clipboard, a set of global atoms, and a group of desktop objects.</span></span> <span data-ttu-id="f130b-292">La estación de ventana interactiva que está asignada a la sesión de inicio de sesión del usuario interactivo también contiene el teclado, el mouse y el dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="f130b-292">The interactive window station that is assigned to the logon session of the interactive user also contains the keyboard, mouse, and display device.</span></span> <span data-ttu-id="f130b-293">Un escritorio es un objeto seguro que se encuentra dentro de una estación de ventana.</span><span class="sxs-lookup"><span data-stu-id="f130b-293">A desktop is a secure object contained within a window station.</span></span> <span data-ttu-id="f130b-294">Un escritorio tiene una superficie de visualización lógica y contiene ventanas, menús y enlaces.</span><span class="sxs-lookup"><span data-stu-id="f130b-294">A desktop has a logical display surface and contains windows, menus, and hooks.</span></span> <span data-ttu-id="f130b-295">Una estación de ventana puede tener varios escritorios.</span><span class="sxs-lookup"><span data-stu-id="f130b-295">A window station can have multiple desktops.</span></span> <span data-ttu-id="f130b-296">Solo los equipos de escritorio de la estación de ventana interactiva pueden estar visibles y recibir datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="f130b-296">Only the desktops of the interactive window station can be visible and receive user input.</span></span>

</dd> <dt>

<span data-ttu-id="f130b-297">**X**</span><span class="sxs-lookup"><span data-stu-id="f130b-297">**X**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f130b-298">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f130b-298">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f130b-299">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f130b-299">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f130b-300">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwX")</span><span class="sxs-lookup"><span data-stu-id="f130b-300">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwX")</span></span>
</dt> </dl>

<span data-ttu-id="f130b-301">Desplazamiento X de la esquina superior izquierda de una ventana si se crea una nueva ventana, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="f130b-301">The X offset of the upper left corner of a window if a new window is created—in pixels.</span></span> <span data-ttu-id="f130b-302">Los desplazamientos se encuentran en la esquina superior izquierda de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="f130b-302">The offsets are from the upper left corner of the screen.</span></span> <span data-ttu-id="f130b-303">En los procesos de GUI, la posición especificada se usa la primera vez que el nuevo proceso llama a [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para crear una ventana superpuesta si el parámetro *X* de **CreateWindow** es **CW \_ USEDEFAULT**.</span><span class="sxs-lookup"><span data-stu-id="f130b-303">For GUI processes, the specified position is used the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the *X* parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> <span data-ttu-id="f130b-304">\[! NOTA X\]</span><span class="sxs-lookup"><span data-stu-id="f130b-304">\[!Note  X\]</span></span>  
> <span data-ttu-id="f130b-305">y **y no se** pueden especificar de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="f130b-305">and **Y** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="f130b-306">**XCountChars**</span><span class="sxs-lookup"><span data-stu-id="f130b-306">**XCountChars**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f130b-307">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f130b-307">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f130b-308">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f130b-308">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f130b-309">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| XCountChars")</span><span class="sxs-lookup"><span data-stu-id="f130b-309">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|XCountChars")</span></span>
</dt> </dl>

<span data-ttu-id="f130b-310">Ancho del búfer de pantalla en columnas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f130b-310">Screen buffer width in character columns.</span></span> <span data-ttu-id="f130b-311">Esta propiedad se usa para los procesos que crean una ventana de consola y se omite en los procesos de la GUI.</span><span class="sxs-lookup"><span data-stu-id="f130b-311">This property is used for processes that create a console window, and is ignored in GUI processes.</span></span>

> [!Note]  
> <span data-ttu-id="f130b-312">**XCountChars** y **YCountChars** no se pueden especificar de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="f130b-312">**XCountChars** and **YCountChars** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="f130b-313">**XSize**</span><span class="sxs-lookup"><span data-stu-id="f130b-313">**XSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f130b-314">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f130b-314">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f130b-315">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f130b-315">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f130b-316">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwXSize")</span><span class="sxs-lookup"><span data-stu-id="f130b-316">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwXSize")</span></span>
</dt> </dl>

<span data-ttu-id="f130b-317">Ancho en píxeles de una ventana si se crea una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="f130b-317">Pixel width of a window if a new window is created.</span></span> <span data-ttu-id="f130b-318">Para los procesos de GUI, solo se usa la primera vez que el nuevo proceso llama a [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para crear una ventana superpuesta si el parámetro NWidth de **CreateWindow** es **CW \_ USEDEFAULT**.</span><span class="sxs-lookup"><span data-stu-id="f130b-318">For GUI processes, this is only used the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the nWidth parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> [!Note]  
> <span data-ttu-id="f130b-319">**Xsize** y **YSize** no se pueden especificar de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="f130b-319">**XSize** and **YSize** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="f130b-320">**S**</span><span class="sxs-lookup"><span data-stu-id="f130b-320">**Y**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f130b-321">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f130b-321">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f130b-322">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f130b-322">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f130b-323">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwY")</span><span class="sxs-lookup"><span data-stu-id="f130b-323">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwY")</span></span>
</dt> </dl>

<span data-ttu-id="f130b-324">Desplazamiento en píxeles de la esquina superior izquierda de una ventana si se crea una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="f130b-324">Pixel offset of the upper-left corner of a window if a new window is created.</span></span> <span data-ttu-id="f130b-325">Los desplazamientos se encuentran en la esquina superior izquierda de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="f130b-325">The offsets are from the upper-left corner of the screen.</span></span> <span data-ttu-id="f130b-326">En los procesos de GUI, la posición especificada se usa la primera vez que el nuevo proceso llama a [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para crear una ventana superpuesta si el parámetro *y* de **CreateWindow** es **CW \_ USEDEFAULT**.</span><span class="sxs-lookup"><span data-stu-id="f130b-326">For GUI processes, the specified position is used the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the *y* parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> <span data-ttu-id="f130b-327">\[! NOTA X\]</span><span class="sxs-lookup"><span data-stu-id="f130b-327">\[!Note  X\]</span></span>  
> <span data-ttu-id="f130b-328">y **y no se** pueden especificar de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="f130b-328">and **Y** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="f130b-329">**YCountChars**</span><span class="sxs-lookup"><span data-stu-id="f130b-329">**YCountChars**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f130b-330">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f130b-330">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f130b-331">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f130b-331">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f130b-332">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| YCountChars")</span><span class="sxs-lookup"><span data-stu-id="f130b-332">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|YCountChars")</span></span>
</dt> </dl>

<span data-ttu-id="f130b-333">Alto del búfer de pantalla en filas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f130b-333">Screen buffer height in character rows.</span></span> <span data-ttu-id="f130b-334">Esta propiedad se usa para los procesos que crean una ventana de la consola, pero se omite en los procesos de la GUI.</span><span class="sxs-lookup"><span data-stu-id="f130b-334">This property is used for processes that create a console window, but is ignored in GUI processes.</span></span>

> [!Note]  
> <span data-ttu-id="f130b-335">**XCountChars** y **YCountChars** no se pueden especificar de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="f130b-335">**XCountChars** and **YCountChars** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="f130b-336">**YSize**</span><span class="sxs-lookup"><span data-stu-id="f130b-336">**YSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f130b-337">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f130b-337">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f130b-338">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f130b-338">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="f130b-339">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwYSize")</span><span class="sxs-lookup"><span data-stu-id="f130b-339">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwYSize")</span></span>
</dt> </dl>

<span data-ttu-id="f130b-340">Alto en píxeles de una ventana si se crea una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="f130b-340">Pixel height of a window if a new window is created.</span></span> <span data-ttu-id="f130b-341">Para los procesos de GUI, se usa solo la primera vez que el nuevo proceso llama a [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para crear una ventana superpuesta si el parámetro *nWidth* de **CreateWindow** es **CW \_ USEDEFAULT**.</span><span class="sxs-lookup"><span data-stu-id="f130b-341">For GUI processes, this is used only the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the *nWidth* parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> [!Note]  
> <span data-ttu-id="f130b-342">**Xsize** y **YSize** no se pueden especificar de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="f130b-342">**XSize** and **YSize** cannot be specified independently.</span></span>

 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f130b-343">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f130b-343">Remarks</span></span>

<span data-ttu-id="f130b-344">Esta clase se deriva de [**Win32 \_ MethodParameterClass**](win32-methodparameterclass.md).</span><span class="sxs-lookup"><span data-stu-id="f130b-344">This class is derived from [**Win32\_MethodParameterClass**](win32-methodparameterclass.md).</span></span>

<span data-ttu-id="f130b-345">Información general</span><span class="sxs-lookup"><span data-stu-id="f130b-345">Overview</span></span>

<span data-ttu-id="f130b-346">El método de [**creación**](create-method-in-class-win32-process.md) de [**\_ procesos de Win32**](win32-process.md) permite configurar las opciones de inicio de cualquier proceso nuevo que se ejecute en un equipo.</span><span class="sxs-lookup"><span data-stu-id="f130b-346">The [**Win32\_Process**](win32-process.md) [**Create**](create-method-in-class-win32-process.md) method enables you to configure startup options for any new process running on a computer.</span></span> <span data-ttu-id="f130b-347">Por ejemplo, puede configurar un proceso para que se inicie en una ventana "oculta", lo que evita que un usuario vea y, posiblemente, lo interrumpa.</span><span class="sxs-lookup"><span data-stu-id="f130b-347">For example, you can configure a process so that it starts in a "hidden" window, which prevents a user from seeing, and possibly interrupting, it.</span></span> <span data-ttu-id="f130b-348">Si el proceso se ejecuta en una ventana de comandos, puede configurar el tamaño, el título y los colores de primer plano y de fondo de la ventana.</span><span class="sxs-lookup"><span data-stu-id="f130b-348">If the process runs in a command window, you can configure the size, title, and foreground and background colors of the window.</span></span>

<span data-ttu-id="f130b-349">Las opciones de inicio se configuran mediante la clase **\_ ProcessStartup de Win32** .</span><span class="sxs-lookup"><span data-stu-id="f130b-349">Startup options are configured using the **Win32\_ProcessStartup** class.</span></span> <span data-ttu-id="f130b-350">**Win32 \_ ProcessStartup** es una clase de tipo de método; la clase de tipo de método existe únicamente para pasar información a un método.</span><span class="sxs-lookup"><span data-stu-id="f130b-350">**Win32\_ProcessStartup** is a Method Type class; the Method Type class exists solely to pass information to a method.</span></span> <span data-ttu-id="f130b-351">En este caso, todas las propiedades de una instancia de **Win32 \_ ProcessStartup** se pasan a una instancia del [**\_ proceso de Win32**](win32-process.md).</span><span class="sxs-lookup"><span data-stu-id="f130b-351">In this case, all the properties of an instance of **Win32\_ProcessStartup** are passed to an instance of [**Win32\_Process**](win32-process.md).</span></span>

<span data-ttu-id="f130b-352">**Usar Win32 \_ ProcessStartup**</span><span class="sxs-lookup"><span data-stu-id="f130b-352">**Using Win32\_ProcessStartup**</span></span>

1.  <span data-ttu-id="f130b-353">Cree una instancia de **Win32 \_ ProcessStartup**.</span><span class="sxs-lookup"><span data-stu-id="f130b-353">Create an instance of **Win32\_ProcessStartup**.</span></span>
2.  <span data-ttu-id="f130b-354">Configure las propiedades de la nueva instancia.</span><span class="sxs-lookup"><span data-stu-id="f130b-354">Configure the properties of the new instance.</span></span>
3.  <span data-ttu-id="f130b-355">Incluya la instancia como parte del método de creación de [**\_ procesos de Win32**](win32-process.md) .</span><span class="sxs-lookup"><span data-stu-id="f130b-355">Include the instance as part of the [**Win32\_Process**](win32-process.md) Create method.</span></span>

<span data-ttu-id="f130b-356">Por ejemplo, si ha creado una instancia de **Win32 \_ ProcessStartup** denominada objConfig, debe pasar el nombre del objeto en el método Create como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="f130b-356">For example, if you have created a **Win32\_ProcessStartup** instance named objConfig, you would pass the object name in the Create method as follows:</span></span>

`errReturn = objProcess.Create("Database.exe", null, objConfig, intProcessID)`

## <a name="examples"></a><span data-ttu-id="f130b-357">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f130b-357">Examples</span></span>

<span data-ttu-id="f130b-358">Puede usar la clase **Win32 \_ ProcessStartup** para configurar varias opciones de inicio para un proceso.</span><span class="sxs-lookup"><span data-stu-id="f130b-358">You can use the **Win32\_ProcessStartup** class to configure various startup options for a process.</span></span> <span data-ttu-id="f130b-359">Estas opciones incluyen, entre otras, la creación de un proceso en una ventana oculta y la creación de un proceso de mayor prioridad.</span><span class="sxs-lookup"><span data-stu-id="f130b-359">These options include, but are not limited to, such things as creating a process in a hidden window and creating a higher-priority process.</span></span> <span data-ttu-id="f130b-360">El siguiente VBScript crea un proceso en una ventana oculta.</span><span class="sxs-lookup"><span data-stu-id="f130b-360">The following VBScript creates a process in a hidden window.</span></span>


```VB
Const HIDDEN_WINDOW = 12
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = HIDDEN_WINDOW
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process")
errReturn = objProcess.Create("Notepad.exe", null, objConfig, intProcessID)
```



<span data-ttu-id="f130b-361">El siguiente VBScript crea un proceso de mayor prioridad.</span><span class="sxs-lookup"><span data-stu-id="f130b-361">The following VBScript creates a higher-priority process.</span></span>


```VB
Const ABOVE_NORMAL = 32768
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.PriorityClass = ABOVE_NORMAL
Set objProcess = GetObject("winmgmts:root\cimv2:Win32_Process")
objProcess.Create "Database.exe", Null, objConfig, intProcessID
```



<span data-ttu-id="f130b-362">En el siguiente ejemplo de código de VBScript se crea un proceso de Bloc de notas en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="f130b-362">The following VBScript code example creates a Notepad process on the local computer.</span></span> <span data-ttu-id="f130b-363">**Win32 \_ ProcessStartup** se usa para configurar las opciones del proceso.</span><span class="sxs-lookup"><span data-stu-id="f130b-363">**Win32\_ProcessStartup** is used to configure the process settings.</span></span>


```VB
Const SW_NORMAL = 1
strComputer = "."
strCommand = "Notepad.exe" 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

' Configure the Notepad process to show a window
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = SW_NORMAL

' Create Notepad process
Set objProcess = objWMIService.Get("Win32_Process")
intReturn = objProcess.Create _
    (strCommand, Null, objConfig, intProcessID)
If intReturn <> 0 Then
    Wscript.Echo "Process could not be created." & vbNewLine & _
                 "Command line: " & strCommand & vbNewLine & _
                 "Return value: " & intReturn
Else
    Wscript.Echo "Process created." & vbNewLine & _
                 "Command line: " & strCommand & vbNewLine & _
                 "Process ID: " & intProcessID
End If
```



## <a name="requirements"></a><span data-ttu-id="f130b-364">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f130b-364">Requirements</span></span>



| <span data-ttu-id="f130b-365">Requisito</span><span class="sxs-lookup"><span data-stu-id="f130b-365">Requirement</span></span> | <span data-ttu-id="f130b-366">Value</span><span class="sxs-lookup"><span data-stu-id="f130b-366">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f130b-367">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f130b-367">Minimum supported client</span></span><br/> | <span data-ttu-id="f130b-368">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f130b-368">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f130b-369">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f130b-369">Minimum supported server</span></span><br/> | <span data-ttu-id="f130b-370">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f130b-370">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f130b-371">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f130b-371">Namespace</span></span><br/>                | <span data-ttu-id="f130b-372">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f130b-372">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f130b-373">MOF</span><span class="sxs-lookup"><span data-stu-id="f130b-373">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f130b-374"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f130b-374"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f130b-375">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f130b-375">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f130b-376"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f130b-376"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f130b-377">Vea también</span><span class="sxs-lookup"><span data-stu-id="f130b-377">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f130b-378">**Win32 \_ MethodParameterClass**</span><span class="sxs-lookup"><span data-stu-id="f130b-378">**Win32\_MethodParameterClass**</span></span>](win32-methodparameterclass.md)
</dt> <dt>

[<span data-ttu-id="f130b-379">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="f130b-379">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="f130b-380">**\_Proceso Win32**</span><span class="sxs-lookup"><span data-stu-id="f130b-380">**Win32\_Process**</span></span>](win32-process.md)
</dt> <dt>

[<span data-ttu-id="f130b-381">**\_\_ProviderHostQuotaConfiguration**</span><span class="sxs-lookup"><span data-stu-id="f130b-381">**\_\_ProviderHostQuotaConfiguration**</span></span>](../wmisdk/--providerhostquotaconfiguration.md)
</dt> <dt>

[<span data-ttu-id="f130b-382">Tareas de WMI: procesos</span><span class="sxs-lookup"><span data-stu-id="f130b-382">WMI Tasks: Processes</span></span>](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
