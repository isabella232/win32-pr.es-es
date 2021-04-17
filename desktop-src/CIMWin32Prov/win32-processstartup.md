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
ms.openlocfilehash: b0be949b106c1fa88b37e0c7764dbddb0546ded7
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187918"
---
# <a name="win32_processstartup-class"></a><span data-ttu-id="68aad-103">\_Clase Win32 ProcessStartup</span><span class="sxs-lookup"><span data-stu-id="68aad-103">Win32\_ProcessStartup class</span></span>

<span data-ttu-id="68aad-104">La [clase WMI](../wmisdk/retrieving-a-class.md) abstracta **\_ ProcessStartup de Win32** representa la configuración de inicio de un proceso basado en Windows.</span><span class="sxs-lookup"><span data-stu-id="68aad-104">The **Win32\_ProcessStartup** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents the startup configuration of a Windows-based process.</span></span> <span data-ttu-id="68aad-105">La clase se define como una definición de tipo de método, lo que significa que solo se usa para pasar información al método [**Create**](create-method-in-class-win32-process.md) de la clase de [**\_ proceso de Win32**](win32-process.md) .</span><span class="sxs-lookup"><span data-stu-id="68aad-105">The class is defined as a method type definition, which means that it is only used for passing information to the [**Create**](create-method-in-class-win32-process.md) method of the [**Win32\_Process**](win32-process.md) class.</span></span>

<span data-ttu-id="68aad-106">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="68aad-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="68aad-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68aad-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="68aad-108">Members</span><span class="sxs-lookup"><span data-stu-id="68aad-108">Members</span></span>

<span data-ttu-id="68aad-109">La **clase \_ ProcessStartup de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="68aad-109">The **Win32\_ProcessStartup** class has these types of members:</span></span>

-   [<span data-ttu-id="68aad-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="68aad-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="68aad-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="68aad-111">Properties</span></span>

<span data-ttu-id="68aad-112">La **clase \_ ProcessStartup de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="68aad-112">The **Win32\_ProcessStartup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="68aad-113">**CreateFlags**</span><span class="sxs-lookup"><span data-stu-id="68aad-113">**CreateFlags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68aad-114">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68aad-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68aad-115">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="68aad-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="68aad-116">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Functions \| [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) \| dwCreationFlags")</span><span class="sxs-lookup"><span data-stu-id="68aad-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Functions\|[**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)\|dwCreationFlags")</span></span>
</dt> </dl>

<span data-ttu-id="68aad-117">Valores adicionales que controlan la clase de prioridad y la creación del proceso.</span><span class="sxs-lookup"><span data-stu-id="68aad-117">Additional values that control the priority class and the creation of the process.</span></span> <span data-ttu-id="68aad-118">Los siguientes valores de creación se pueden especificar en cualquier combinación, a menos que se indique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="68aad-118">The following creation values can be specified in any combination, except as noted.</span></span>

<dt>

<span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>

<span data-ttu-id="68aad-119"><span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>**Depuración \_ Proceso** (1)</span><span class="sxs-lookup"><span data-stu-id="68aad-119"><span id="Debug_Process"></span><span id="debug_process"></span><span id="DEBUG_PROCESS"></span>**Debug\_Process** (1)</span></span>


</dt> <dd>

<span data-ttu-id="68aad-120">Si se establece esta marca, el proceso de llamada se trata como un depurador y se depura el nuevo proceso.</span><span class="sxs-lookup"><span data-stu-id="68aad-120">If this flag is set, the calling process is treated as a debugger, and the new process is being debugged.</span></span> <span data-ttu-id="68aad-121">El sistema notifica al depurador todos los eventos de depuración que se producen en el proceso que se está depurando.</span><span class="sxs-lookup"><span data-stu-id="68aad-121">The system notifies the debugger of all debug events that occur in the process being debugged.</span></span>

</dd> <dt>

<span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>

<span data-ttu-id="68aad-122"><span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>**Depuración \_ Solo \_ este \_ proceso** (2)</span><span class="sxs-lookup"><span data-stu-id="68aad-122"><span id="Debug_Only_This_Process"></span><span id="debug_only_this_process"></span><span id="DEBUG_ONLY_THIS_PROCESS"></span>**Debug\_Only\_This\_Process** (2)</span></span>


</dt> <dd>

<span data-ttu-id="68aad-123">Si no se establece esta marca y se depura el proceso de llamada, el nuevo proceso se convierte en otro proceso que se está depurando.</span><span class="sxs-lookup"><span data-stu-id="68aad-123">If this flag is not set and the calling process is being debugged, the new process becomes another process being debugged.</span></span> <span data-ttu-id="68aad-124">Si el proceso de llamada no es un proceso de depuración, no se produce ninguna acción relacionada con la depuración.</span><span class="sxs-lookup"><span data-stu-id="68aad-124">If the calling process is not a process of being debugged, no debugging-related actions occur.</span></span>

</dd> <dt>

<span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>

<span data-ttu-id="68aad-125"><span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>**Crear \_ Suspendido** (4)</span><span class="sxs-lookup"><span data-stu-id="68aad-125"><span id="Create_Suspended"></span><span id="create_suspended"></span><span id="CREATE_SUSPENDED"></span>**Create\_Suspended** (4)</span></span>


</dt> <dd>

<span data-ttu-id="68aad-126">El subproceso principal del nuevo proceso se crea en un estado suspendido y no se ejecuta hasta que se llama al método [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) .</span><span class="sxs-lookup"><span data-stu-id="68aad-126">The primary thread of the new process is created in a suspended state and does not run until the [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) method is called.</span></span>

</dd> <dt>

<span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>

<span data-ttu-id="68aad-127"><span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>**Separado \_ Proceso** (8)</span><span class="sxs-lookup"><span data-stu-id="68aad-127"><span id="Detached_Process"></span><span id="detached_process"></span><span id="DETACHED_PROCESS"></span>**Detached\_Process** (8)</span></span>


</dt> <dd>

<span data-ttu-id="68aad-128">En los procesos de la consola, el nuevo proceso no tiene acceso a la consola del proceso primario.</span><span class="sxs-lookup"><span data-stu-id="68aad-128">For console processes, the new process does not have access to the console of the parent process.</span></span> <span data-ttu-id="68aad-129">Esta marca no se puede usar si se establece la marca **crear \_ nueva \_ consola** .</span><span class="sxs-lookup"><span data-stu-id="68aad-129">This flag cannot be used if the **Create\_New\_Console** flag is set.</span></span>

</dd> <dt>

<span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>

<span data-ttu-id="68aad-130"><span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>**Crear \_ Nueva \_ consola** (16)</span><span class="sxs-lookup"><span data-stu-id="68aad-130"><span id="Create_New_Console"></span><span id="create_new_console"></span><span id="CREATE_NEW_CONSOLE"></span>**Create\_New\_Console** (16)</span></span>


</dt> <dd>

<span data-ttu-id="68aad-131">Este nuevo proceso tiene una nueva consola, en lugar de heredar la consola primaria.</span><span class="sxs-lookup"><span data-stu-id="68aad-131">This new process has a new console, instead of inheriting the parent console.</span></span> <span data-ttu-id="68aad-132">Esta marca no se puede usar con la marca de **\_ proceso desasociada** .</span><span class="sxs-lookup"><span data-stu-id="68aad-132">This flag cannot be used with the **Detached\_Process** flag.</span></span>

</dd> <dt>

<span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>

<span data-ttu-id="68aad-133"><span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>**Crear \_ Nuevo \_ \_ grupo de procesos** (512)</span><span class="sxs-lookup"><span data-stu-id="68aad-133"><span id="Create_New_Process_Group"></span><span id="create_new_process_group"></span><span id="CREATE_NEW_PROCESS_GROUP"></span>**Create\_New\_Process\_Group** (512)</span></span>


</dt> <dd>

<span data-ttu-id="68aad-134">Este nuevo proceso es el proceso raíz de un nuevo grupo de procesos.</span><span class="sxs-lookup"><span data-stu-id="68aad-134">This new process is the root process of a new process group.</span></span> <span data-ttu-id="68aad-135">El grupo de procesos incluye todos los procesos descendientes de este proceso raíz.</span><span class="sxs-lookup"><span data-stu-id="68aad-135">The process group includes all of the processes that are descendants of this root process.</span></span> <span data-ttu-id="68aad-136">El identificador de proceso del nuevo grupo de procesos es el mismo que el identificador de proceso que se devuelve en la propiedad **ProcessId** de la clase de [**\_ proceso de Win32**](win32-process.md) .</span><span class="sxs-lookup"><span data-stu-id="68aad-136">The process identifier of the new process group is the same as the process identifier that is returned in the **ProcessID** property of the [**Win32\_Process**](win32-process.md) class.</span></span> <span data-ttu-id="68aad-137">El método [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) usa los grupos de procesos para habilitar el envío de una señal CTRL + C o una señal Ctrl + Inter a un grupo de procesos de consola.</span><span class="sxs-lookup"><span data-stu-id="68aad-137">Process groups are used by the [**GenerateConsoleCtrlEvent**](/windows/console/generateconsolectrlevent) method to enable the sending of either a CTRL+C signal or a CTRL+BREAK signal to a group of console processes.</span></span>

</dd> <dt>

<span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>

<span data-ttu-id="68aad-138"><span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>**Crear \_ \_Entorno Unicode** (1024)</span><span class="sxs-lookup"><span data-stu-id="68aad-138"><span id="Create_Unicode_Environment"></span><span id="create_unicode_environment"></span><span id="CREATE_UNICODE_ENVIRONMENT"></span>**Create\_Unicode\_Environment** (1024)</span></span>


</dt> <dd>

<span data-ttu-id="68aad-139">La configuración del entorno que se muestra en la propiedad **EnvironmentVariables** utiliza caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="68aad-139">The environment settings listed in the **EnvironmentVariables** property use Unicode characters.</span></span> <span data-ttu-id="68aad-140">Si no se establece esta marca, el bloque de entorno utiliza caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="68aad-140">If this flag is not set, the environment block uses ANSI characters.</span></span>

</dd> <dt>

<span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>

<span data-ttu-id="68aad-141"><span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>**Crear \_ \_ \_ Modo de error predeterminado** (67108864)</span><span class="sxs-lookup"><span data-stu-id="68aad-141"><span id="Create_Default_Error_Mode"></span><span id="create_default_error_mode"></span><span id="CREATE_DEFAULT_ERROR_MODE"></span>**Create\_Default\_Error\_Mode** (67108864)</span></span>


</dt> <dd>

<span data-ttu-id="68aad-142">A los procesos recién creados se les asigna el modo de error predeterminado del sistema del proceso de llamada en lugar de heredar el modo de error del proceso primario.</span><span class="sxs-lookup"><span data-stu-id="68aad-142">Newly created processes are given the system default error mode of the calling process instead of inheriting the error mode of the parent process.</span></span> <span data-ttu-id="68aad-143">Esta marca es útil para las aplicaciones de Shell multiproceso que se ejecutan con errores severos deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="68aad-143">This flag is useful for multithreaded shell applications that run with hard errors disabled.</span></span>

</dd> <dt>

<span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>

<span data-ttu-id="68aad-144"><span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>**Crear \_ SEPARACIÓN \_ del \_ trabajo** (16777216)</span><span class="sxs-lookup"><span data-stu-id="68aad-144"><span id="CREATE_BREAKAWAY_FROM_JOB"></span><span id="create_breakaway_from_job"></span>**CREATE\_BREAKAWAY\_FROM\_JOB** (16777216)</span></span>


</dt> <dd>

<span data-ttu-id="68aad-145">Se usa para que el proceso creado no esté limitado por el objeto de trabajo.</span><span class="sxs-lookup"><span data-stu-id="68aad-145">Used for the created process not to be limited by the job object.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="68aad-146">**EnvironmentVariables**</span><span class="sxs-lookup"><span data-stu-id="68aad-146">**EnvironmentVariables**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68aad-147">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="68aad-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="68aad-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="68aad-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="68aad-149">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| HKEY \_ Current \_ User \\ \\ Environment")</span><span class="sxs-lookup"><span data-stu-id="68aad-149">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|HKEY\_CURRENT\_USER\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="68aad-150">Lista de valores para la configuración de un equipo.</span><span class="sxs-lookup"><span data-stu-id="68aad-150">List of settings for the configuration of a computer.</span></span> <span data-ttu-id="68aad-151">Las variables de entorno especifican rutas de acceso de búsqueda para archivos, directorios para archivos temporales, opciones específicas de la aplicación y otra información similar.</span><span class="sxs-lookup"><span data-stu-id="68aad-151">Environment variables specify search paths for files, directories for temporary files, application-specific options, and other similar information.</span></span> <span data-ttu-id="68aad-152">El sistema mantiene un bloque de configuración del entorno para cada usuario y uno para el equipo.</span><span class="sxs-lookup"><span data-stu-id="68aad-152">The system maintains a block of environment settings for each user and one for the computer.</span></span> <span data-ttu-id="68aad-153">El bloque de entorno del sistema representa las variables de entorno para todos los usuarios de un equipo específico.</span><span class="sxs-lookup"><span data-stu-id="68aad-153">The system environment block represents environment variables for all of the users of a specific computer.</span></span> <span data-ttu-id="68aad-154">El bloque de entorno de un usuario representa las variables de entorno que el sistema mantiene para un usuario específico e incluye el conjunto de variables de entorno del sistema.</span><span class="sxs-lookup"><span data-stu-id="68aad-154">A user's environment block represents the environment variables that the system maintains for a specific user, and includes the set of system environment variables.</span></span> <span data-ttu-id="68aad-155">De forma predeterminada, cada proceso recibe una copia del bloque de entorno para su proceso primario.</span><span class="sxs-lookup"><span data-stu-id="68aad-155">By default, each process receives a copy of the environment block for its parent process.</span></span> <span data-ttu-id="68aad-156">Normalmente, es el bloque de entorno para el usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="68aad-156">Typically, this is the environment block for the user who is logged on.</span></span> <span data-ttu-id="68aad-157">Un proceso puede especificar distintos bloques de entorno para sus procesos secundarios.</span><span class="sxs-lookup"><span data-stu-id="68aad-157">A process can specify different environment blocks for its child processes.</span></span>

</dd> <dt>

<span data-ttu-id="68aad-158">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="68aad-158">**ErrorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68aad-159">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68aad-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68aad-160">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="68aad-160">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="68aad-161">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| error Functions \| SetErrorMode")</span><span class="sxs-lookup"><span data-stu-id="68aad-161">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Error Functions\|SetErrorMode")</span></span>
</dt> </dl>

<span data-ttu-id="68aad-162">En algunos procesadores que no son x86, las referencias de memoria mal alineadas causan una excepción de error de alineación.</span><span class="sxs-lookup"><span data-stu-id="68aad-162">On some non-x86 processors, misaligned memory references cause an alignment fault exception.</span></span> <span data-ttu-id="68aad-163">La marca no se produce un **\_ error de alineación, \_ \_ excepto** que le permite controlar si un sistema operativo corrige automáticamente o no dichos errores de alineación o hace que sean visibles para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="68aad-163">The **No\_Alignment\_Fault\_Except** flag lets you control whether or not an operating system automatically fixes such alignment faults, or makes them visible to an application.</span></span> <span data-ttu-id="68aad-164">En una plataforma de millones de instrucciones por segundo (MIPS), una aplicación debe llamar explícitamente a [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) con el indicador de **no hay ningún \_ error de alineación \_ \_ excepto** para que el sistema operativo corrija automáticamente los errores de alineación.</span><span class="sxs-lookup"><span data-stu-id="68aad-164">On a millions of instructions per second (MIPS) platform, an application must explicitly call [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) with the **No\_Alignment\_Fault\_Except** flag to have the operating system automatically fix alignment faults.</span></span>

<span data-ttu-id="68aad-165">Cómo un sistema operativo procesa varios tipos de errores graves.</span><span class="sxs-lookup"><span data-stu-id="68aad-165">How an operating system processes several types of serious errors.</span></span> <span data-ttu-id="68aad-166">Puede especificar que los errores del proceso del sistema operativo o una aplicación pueden recibir y procesar errores.</span><span class="sxs-lookup"><span data-stu-id="68aad-166">You can specify that the operating system process errors, or an application can receive and process errors.</span></span>

<span data-ttu-id="68aad-167">La configuración predeterminada es que el sistema operativo cree errores de alineación visibles para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="68aad-167">The default setting is for the operating system to make alignment faults visible to an application.</span></span> <span data-ttu-id="68aad-168">Dado que la plataforma x86 no hace que los errores de alineación sean visibles para una aplicación, la marca no se produce un error de **\_ alineación, \_ \_ excepto** si la marca no se establece.</span><span class="sxs-lookup"><span data-stu-id="68aad-168">Because the x86 platform does not make alignment faults visible to an application, the **No\_Alignment\_Fault\_Except** flag does not make the operating system raise an alignment fault error—even if the flag is not set.</span></span> <span data-ttu-id="68aad-169">El estado predeterminado de [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) es establecer todas las marcas en 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="68aad-169">The default state for [**SetErrorMode**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-seterrormode) is to set all of the flags to 0 (zero).</span></span>

<dt>



 <span data-ttu-id="68aad-170">(1)</span><span class="sxs-lookup"><span data-stu-id="68aad-170">(1)</span></span>


</dt> <dd>

<span data-ttu-id="68aad-171">Default</span><span class="sxs-lookup"><span data-stu-id="68aad-171">Default</span></span>

</dd> <dt>

<span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>

<span data-ttu-id="68aad-172"><span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>**Error \_ \_Errores críticos** (2)</span><span class="sxs-lookup"><span data-stu-id="68aad-172"><span id="Fail_Critical_Errors"></span><span id="fail_critical_errors"></span><span id="FAIL_CRITICAL_ERRORS"></span>**Fail\_Critical\_Errors** (2)</span></span>


</dt> <dd>

<span data-ttu-id="68aad-173">Si se establece esta marca, el sistema operativo no muestra el cuadro de mensaje del controlador de errores críticos cuando se produce este tipo de error.</span><span class="sxs-lookup"><span data-stu-id="68aad-173">If this flag is set, the operating system does not display the critical error handler message box when such an error occurs.</span></span> <span data-ttu-id="68aad-174">En su lugar, el sistema operativo envía el error al proceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="68aad-174">Instead, the operating system sends the error to the calling process.</span></span>

</dd> <dt>

<span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>

<span data-ttu-id="68aad-175"><span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>**No \_ Error de alineación \_ \_ excepto** (4)</span><span class="sxs-lookup"><span data-stu-id="68aad-175"><span id="No_Alignment_Fault_Except"></span><span id="no_alignment_fault_except"></span><span id="NO_ALIGNMENT_FAULT_EXCEPT"></span>**No\_Alignment\_Fault\_Except** (4)</span></span>


</dt> <dd>

<span data-ttu-id="68aad-176">Si se establece esta marca, el sistema operativo corrige automáticamente los errores de alineación de memoria y hace que sean invisibles para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="68aad-176">If this flag is set, the operating system automatically fixes memory alignment faults and makes them invisible to the application.</span></span> <span data-ttu-id="68aad-177">Lo hace para los procesos de llamada y descendientes.</span><span class="sxs-lookup"><span data-stu-id="68aad-177">It does this for the calling and descendant processes.</span></span> <span data-ttu-id="68aad-178">Esta marca se aplica solo a la tecnología de conjunto de instrucciones reducida (RISC) y no tiene ningún efecto en los procesadores x86.</span><span class="sxs-lookup"><span data-stu-id="68aad-178">This flag applies to reduced instruction set computing (RISC) only, and has no effect on x86 processors.</span></span>

</dd> <dt>

<span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>

<span data-ttu-id="68aad-179"><span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>**No \_ \_ \_ \_ Cuadro error de GP** (8)</span><span class="sxs-lookup"><span data-stu-id="68aad-179"><span id="No_GP_Fault_Error_Box"></span><span id="no_gp_fault_error_box"></span><span id="NO_GP_FAULT_ERROR_BOX"></span>**No\_GP\_Fault\_Error\_Box** (8)</span></span>


</dt> <dd>

<span data-ttu-id="68aad-180">Si se establece esta marca, el sistema operativo no muestra el cuadro de mensaje de error de protección general (GP) cuando se produce un error de GP.</span><span class="sxs-lookup"><span data-stu-id="68aad-180">If this flag is set, the operating system does not display the general protection (GP) fault message box when a GP error occurs.</span></span> <span data-ttu-id="68aad-181">Esta marca solo debe establecerse mediante la depuración de aplicaciones que controlen errores de GP.</span><span class="sxs-lookup"><span data-stu-id="68aad-181">This flag should only be set by debugging applications that handle GP errors.</span></span>

</dd> <dt>

<span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>

<span data-ttu-id="68aad-182"><span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>**No \_ \_Cuadro de \_ error \_ de abrir archivo** (16)</span><span class="sxs-lookup"><span data-stu-id="68aad-182"><span id="No_Open_File_Error_Box"></span><span id="no_open_file_error_box"></span><span id="NO_OPEN_FILE_ERROR_BOX"></span>**No\_Open\_File\_Error\_Box** (16)</span></span>


</dt> <dd>

<span data-ttu-id="68aad-183">Si se establece esta marca, el sistema operativo no mostrará un cuadro de mensaje cuando no encuentre un archivo.</span><span class="sxs-lookup"><span data-stu-id="68aad-183">If this flag is set, the operating system does not display a message box when it fails to find a file.</span></span> <span data-ttu-id="68aad-184">En su lugar, el error se devuelve al proceso de llamada.</span><span class="sxs-lookup"><span data-stu-id="68aad-184">Instead, the error is returned to the calling process.</span></span> <span data-ttu-id="68aad-185">Esta marca se omite actualmente.</span><span class="sxs-lookup"><span data-stu-id="68aad-185">This flag is currently ignored.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="68aad-186">**FillAttribute**</span><span class="sxs-lookup"><span data-stu-id="68aad-186">**FillAttribute**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68aad-187">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68aad-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68aad-188">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="68aad-188">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="68aad-189">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwFillAttribute")</span><span class="sxs-lookup"><span data-stu-id="68aad-189">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwFillAttribute")</span></span>
</dt> </dl>

<span data-ttu-id="68aad-190">Los colores de texto y de fondo si se crea una nueva ventana de consola en una aplicación de consola.</span><span class="sxs-lookup"><span data-stu-id="68aad-190">The text and background colors if a new console window is created in a console application.</span></span> <span data-ttu-id="68aad-191">Estos valores se omiten en las aplicaciones de la interfaz gráfica de usuario (GUI).</span><span class="sxs-lookup"><span data-stu-id="68aad-191">These values are ignored in graphical user interface (GUI) applications.</span></span> <span data-ttu-id="68aad-192">Para especificar los colores de primer plano y de fondo, agregue los valores juntos.</span><span class="sxs-lookup"><span data-stu-id="68aad-192">To specify both foreground and background colors, add the values together.</span></span> <span data-ttu-id="68aad-193">Por ejemplo, para tener el tipo rojo (4) en un fondo azul (16), establezca FillAttribute en 20.</span><span class="sxs-lookup"><span data-stu-id="68aad-193">For example, to have red type (4) on a blue background (16), set the FillAttribute to 20.</span></span>

<dt>

<span data-ttu-id="68aad-194">1</span><span class="sxs-lookup"><span data-stu-id="68aad-194">1</span></span>
</dt> <dd>

<span data-ttu-id="68aad-195">Azul de primer plano \_</span><span class="sxs-lookup"><span data-stu-id="68aad-195">Foreground\_Blue</span></span>

</dd> <dt>

<span data-ttu-id="68aad-196">2</span><span class="sxs-lookup"><span data-stu-id="68aad-196">2</span></span>
</dt> <dd>

<span data-ttu-id="68aad-197">Verde de primer plano \_</span><span class="sxs-lookup"><span data-stu-id="68aad-197">Foreground\_Green</span></span>

</dd> <dt>

<span data-ttu-id="68aad-198">4</span><span class="sxs-lookup"><span data-stu-id="68aad-198">4</span></span>
</dt> <dd>

<span data-ttu-id="68aad-199">Rojo de primer plano \_</span><span class="sxs-lookup"><span data-stu-id="68aad-199">Foreground\_Red</span></span>

</dd> <dt>

<span data-ttu-id="68aad-200">8</span><span class="sxs-lookup"><span data-stu-id="68aad-200">8</span></span>
</dt> <dd>

<span data-ttu-id="68aad-201">Intensidad de primer plano \_</span><span class="sxs-lookup"><span data-stu-id="68aad-201">Foreground\_Intensity</span></span>

</dd> <dt>

<span data-ttu-id="68aad-202">16</span><span class="sxs-lookup"><span data-stu-id="68aad-202">16</span></span>
</dt> <dd>

<span data-ttu-id="68aad-203">Azul de fondo \_</span><span class="sxs-lookup"><span data-stu-id="68aad-203">Background\_Blue</span></span>

</dd> <dt>

<span data-ttu-id="68aad-204">32</span><span class="sxs-lookup"><span data-stu-id="68aad-204">32</span></span>
</dt> <dd>

<span data-ttu-id="68aad-205">Verde de fondo \_</span><span class="sxs-lookup"><span data-stu-id="68aad-205">Background\_Green</span></span>

</dd> <dt>

<span data-ttu-id="68aad-206">64</span><span class="sxs-lookup"><span data-stu-id="68aad-206">64</span></span>
</dt> <dd>

<span data-ttu-id="68aad-207">Rojo de fondo \_</span><span class="sxs-lookup"><span data-stu-id="68aad-207">Background\_Red</span></span>

</dd> <dt>

<span data-ttu-id="68aad-208">128</span><span class="sxs-lookup"><span data-stu-id="68aad-208">128</span></span>
</dt> <dd>

<span data-ttu-id="68aad-209">Intensidad de fondo \_</span><span class="sxs-lookup"><span data-stu-id="68aad-209">Background\_Intensity</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="68aad-210">**PriorityClass**</span><span class="sxs-lookup"><span data-stu-id="68aad-210">**PriorityClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68aad-211">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68aad-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68aad-212">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="68aad-212">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="68aad-213">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| proceso y estructuras de subproceso \| [**JOBOBJECT \_ \_ \_ información básica de límite**](/windows/win32/api/winnt/ns-winnt-jobobject_basic_limit_information) \| PriorityClass")</span><span class="sxs-lookup"><span data-stu-id="68aad-213">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**JOBOBJECT\_BASIC\_LIMIT\_INFORMATION**](/windows/win32/api/winnt/ns-winnt-jobobject_basic_limit_information)\|PriorityClass")</span></span>
</dt> </dl>

<span data-ttu-id="68aad-214">Clase de prioridad del nuevo proceso.</span><span class="sxs-lookup"><span data-stu-id="68aad-214">Priority class of the new process.</span></span> <span data-ttu-id="68aad-215">Utilice esta propiedad para determinar las prioridades de programación de los subprocesos del proceso.</span><span class="sxs-lookup"><span data-stu-id="68aad-215">Use this property to determine the schedule priorities of the threads in the process.</span></span> <span data-ttu-id="68aad-216">Si la propiedad es null, el valor predeterminado de la clase Priority es normal, a menos que la clase de prioridad del proceso de creación esté inactiva o por debajo de lo \_ normal.</span><span class="sxs-lookup"><span data-stu-id="68aad-216">If the property is left null, the priority class defaults to Normal—unless the priority class of the creating process is Idle or Below\_Normal.</span></span> <span data-ttu-id="68aad-217">En estos casos, el proceso secundario recibe la clase de prioridad predeterminada del proceso de llamada.</span><span class="sxs-lookup"><span data-stu-id="68aad-217">In these cases, the child process receives the default priority class of the calling process.</span></span>

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span data-ttu-id="68aad-218"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)</span><span class="sxs-lookup"><span data-stu-id="68aad-218"><span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** (32)</span></span>


</dt> <dd>

<span data-ttu-id="68aad-219">Indica un proceso normal sin necesidad de una programación especial.</span><span class="sxs-lookup"><span data-stu-id="68aad-219">Indicates a normal process with no special schedule needs.</span></span>

</dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span data-ttu-id="68aad-220"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Inactivo** (64)</span><span class="sxs-lookup"><span data-stu-id="68aad-220"><span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**Idle** (64)</span></span>


</dt> <dd>

<span data-ttu-id="68aad-221">Indica un proceso con subprocesos que se ejecutan solo cuando el sistema está inactivo y son retenidos por los subprocesos de cualquier proceso que se ejecute en una clase de prioridad más alta.</span><span class="sxs-lookup"><span data-stu-id="68aad-221">Indicates a process with threads that run only when the system is idle and are preempted by the threads of any process running in a higher priority class.</span></span> <span data-ttu-id="68aad-222">Un ejemplo es un protector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="68aad-222">An example is a screen saver.</span></span> <span data-ttu-id="68aad-223">Los procesos secundarios heredan la clase de prioridad inactiva.</span><span class="sxs-lookup"><span data-stu-id="68aad-223">The idle priority class is inherited by child processes.</span></span>

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="68aad-224"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**Alto** (128)</span><span class="sxs-lookup"><span data-stu-id="68aad-224"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (128)</span></span>


</dt> <dd>

<span data-ttu-id="68aad-225">Indica un proceso que realiza tareas críticas en el tiempo que se deben ejecutar inmediatamente para ejecutarse correctamente.</span><span class="sxs-lookup"><span data-stu-id="68aad-225">Indicates a process that performs time-critical tasks that must be executed immediately to run correctly.</span></span> <span data-ttu-id="68aad-226">Los subprocesos de un proceso de clase de prioridad alta tienen preferencia sobre los subprocesos de los procesos de clase de prioridad normal o de prioridad inactiva.</span><span class="sxs-lookup"><span data-stu-id="68aad-226">The threads of a high-priority class process preempt the threads of normal-priority or idle-priority class processes.</span></span> <span data-ttu-id="68aad-227">Un ejemplo es Windows Lista de tareas, que debe responder rápidamente cuando el usuario lo llama, independientemente de la carga del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="68aad-227">An example is Windows Task List, which must respond quickly when called by the user, regardless of the load on the operating system.</span></span> <span data-ttu-id="68aad-228">Extreme las precauciones al usar la clase de prioridad alta, ya que una aplicación de alta prioridad enlazada a la CPU puede usar casi todos los ciclos disponibles.</span><span class="sxs-lookup"><span data-stu-id="68aad-228">Use extreme care when using the high-priority class, because a high-priority class CPU-bound application can use nearly all of the available cycles.</span></span> <span data-ttu-id="68aad-229">Solo los subprocesos de prioridad en tiempo real se establecen en este nivel.</span><span class="sxs-lookup"><span data-stu-id="68aad-229">Only a real-time priority preempts threads set to this level.</span></span>

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span data-ttu-id="68aad-230"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Tiempo real** (256)</span><span class="sxs-lookup"><span data-stu-id="68aad-230"><span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**Realtime** (256)</span></span>


</dt> <dd>

<span data-ttu-id="68aad-231">Indica un proceso que tiene la prioridad más alta posible.</span><span class="sxs-lookup"><span data-stu-id="68aad-231">Indicates a process that has the highest possible priority.</span></span> <span data-ttu-id="68aad-232">Los subprocesos de un proceso de clase de prioridad en tiempo real tienen preferencia sobre los subprocesos de todos los demás procesos, incluidos los subprocesos de alta prioridad y los procesos del sistema operativo que realizan tareas importantes.</span><span class="sxs-lookup"><span data-stu-id="68aad-232">The threads of a real-time priority class process preempt the threads of all other processes—including high-priority threads and operating system processes performing important tasks.</span></span> <span data-ttu-id="68aad-233">Por ejemplo, un proceso en tiempo real que se ejecuta durante más de un intervalo muy breve puede hacer que las cachés del disco no se vacíen o hacer que el mouse deje de responder.</span><span class="sxs-lookup"><span data-stu-id="68aad-233">For example, a real-time process that executes for more than a very brief interval can cause disk caches not to flush, or cause a mouse to be unresponsive.</span></span>

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span data-ttu-id="68aad-234"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**A continuación \_ Normal** (16384)</span><span class="sxs-lookup"><span data-stu-id="68aad-234"><span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**Below\_Normal** (16384)</span></span>


</dt> <dd>

<span data-ttu-id="68aad-235">Indica un proceso que tiene una prioridad mayor que inactiva pero menor que normal.</span><span class="sxs-lookup"><span data-stu-id="68aad-235">Indicates a process that has a priority higher than Idle but lower than Normal.</span></span>

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span data-ttu-id="68aad-236"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Por encima \_ Normal** (32768)</span><span class="sxs-lookup"><span data-stu-id="68aad-236"><span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**Above\_Normal** (32768)</span></span>


</dt> <dd>

<span data-ttu-id="68aad-237">Indica un proceso que tiene una prioridad mayor que el normal pero menor que el alto.</span><span class="sxs-lookup"><span data-stu-id="68aad-237">Indicates a process that has a priority higher than Normal but lower than High.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="68aad-238">**ShowWindow**</span><span class="sxs-lookup"><span data-stu-id="68aad-238">**ShowWindow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68aad-239">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="68aad-239">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="68aad-240">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="68aad-240">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="68aad-241">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| wShowWindow")</span><span class="sxs-lookup"><span data-stu-id="68aad-241">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|wShowWindow")</span></span>
</dt> </dl>

<span data-ttu-id="68aad-242">Cómo se muestra la ventana al usuario.</span><span class="sxs-lookup"><span data-stu-id="68aad-242">How the window is displayed to the user.</span></span> <span data-ttu-id="68aad-243">Puede ser cualquiera de los valores que se pueden especificar en el parámetro *nCmdShow* para la función [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="68aad-243">It can be any of the values that can be specified in the *nCmdShow* parameter for the [ShowWindow](/windows/desktop/api/winuser/nf-winuser-showwindow) function.</span></span>

</dd> <dt>

<span data-ttu-id="68aad-244">**Título**</span><span class="sxs-lookup"><span data-stu-id="68aad-244">**Title**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68aad-245">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68aad-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68aad-246">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="68aad-246">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="68aad-247">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lpTitle")</span><span class="sxs-lookup"><span data-stu-id="68aad-247">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|lpTitle")</span></span>
</dt> </dl>

<span data-ttu-id="68aad-248">Texto que se muestra en la barra de título cuando se crea una nueva ventana de consola. se usa para los procesos de la consola.</span><span class="sxs-lookup"><span data-stu-id="68aad-248">Text displayed in the title bar when a new console window is created; used for console processes.</span></span> <span data-ttu-id="68aad-249">Si es **null**, se usa el nombre del archivo ejecutable como título de la ventana.</span><span class="sxs-lookup"><span data-stu-id="68aad-249">If **NULL**, the name of the executable file is used as the window title.</span></span> <span data-ttu-id="68aad-250">Esta propiedad debe ser **null** para los procesos de la GUI o de la consola que no crean una nueva ventana de consola.</span><span class="sxs-lookup"><span data-stu-id="68aad-250">This property must be **NULL** for GUI or console processes that do not create a new console window.</span></span>

</dd> <dt>

<span data-ttu-id="68aad-251">**WinstationDesktop**</span><span class="sxs-lookup"><span data-stu-id="68aad-251">**WinstationDesktop**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68aad-252">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="68aad-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68aad-253">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="68aad-253">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="68aad-254">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| lpDesktop")</span><span class="sxs-lookup"><span data-stu-id="68aad-254">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|lpDesktop")</span></span>
</dt> </dl>

<span data-ttu-id="68aad-255">El nombre del escritorio o el nombre del escritorio y de la estación de ventana para el proceso.</span><span class="sxs-lookup"><span data-stu-id="68aad-255">The name of the desktop or the name of both the desktop and window station for the process.</span></span> <span data-ttu-id="68aad-256">Una barra diagonal inversa en la cadena indica que la cadena incluye nombres de estaciones de escritorio y de ventanas.</span><span class="sxs-lookup"><span data-stu-id="68aad-256">A backslash in the string indicates that the string includes both desktop and window station names.</span></span> <span data-ttu-id="68aad-257">Si **WinstationDesktop** es **null**, el nuevo proceso hereda el escritorio y la estación de ventana de su proceso principal.</span><span class="sxs-lookup"><span data-stu-id="68aad-257">If **WinstationDesktop** is **NULL**, the new process inherits the desktop and window station of its parent process.</span></span> <span data-ttu-id="68aad-258">Si **WinstationDesktop** es una cadena vacía, el proceso no hereda el escritorio y la estación de ventana de su proceso principal.</span><span class="sxs-lookup"><span data-stu-id="68aad-258">If **WinstationDesktop** is an empty string, the process does not inherit the desktop and window station of its parent process.</span></span> <span data-ttu-id="68aad-259">El sistema determina si se debe crear un nuevo escritorio y una estación de ventana.</span><span class="sxs-lookup"><span data-stu-id="68aad-259">The system determines if a new desktop and window station must be created.</span></span> <span data-ttu-id="68aad-260">Una estación de ventana es un objeto seguro que contiene un portapapeles, un conjunto de átomos globales y un grupo de objetos de escritorio.</span><span class="sxs-lookup"><span data-stu-id="68aad-260">A window station is a secure object that contains a clipboard, a set of global atoms, and a group of desktop objects.</span></span> <span data-ttu-id="68aad-261">La estación de ventana interactiva que está asignada a la sesión de inicio de sesión del usuario interactivo también contiene el teclado, el mouse y el dispositivo de pantalla.</span><span class="sxs-lookup"><span data-stu-id="68aad-261">The interactive window station that is assigned to the logon session of the interactive user also contains the keyboard, mouse, and display device.</span></span> <span data-ttu-id="68aad-262">Un escritorio es un objeto seguro que se encuentra dentro de una estación de ventana.</span><span class="sxs-lookup"><span data-stu-id="68aad-262">A desktop is a secure object contained within a window station.</span></span> <span data-ttu-id="68aad-263">Un escritorio tiene una superficie de visualización lógica y contiene ventanas, menús y enlaces.</span><span class="sxs-lookup"><span data-stu-id="68aad-263">A desktop has a logical display surface and contains windows, menus, and hooks.</span></span> <span data-ttu-id="68aad-264">Una estación de ventana puede tener varios escritorios.</span><span class="sxs-lookup"><span data-stu-id="68aad-264">A window station can have multiple desktops.</span></span> <span data-ttu-id="68aad-265">Solo los equipos de escritorio de la estación de ventana interactiva pueden estar visibles y recibir datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="68aad-265">Only the desktops of the interactive window station can be visible and receive user input.</span></span>

</dd> <dt>

<span data-ttu-id="68aad-266">**X**</span><span class="sxs-lookup"><span data-stu-id="68aad-266">**X**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68aad-267">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68aad-267">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68aad-268">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="68aad-268">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="68aad-269">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwX")</span><span class="sxs-lookup"><span data-stu-id="68aad-269">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwX")</span></span>
</dt> </dl>

<span data-ttu-id="68aad-270">Desplazamiento X de la esquina superior izquierda de una ventana si se crea una nueva ventana, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="68aad-270">The X offset of the upper left corner of a window if a new window is created—in pixels.</span></span> <span data-ttu-id="68aad-271">Los desplazamientos se encuentran en la esquina superior izquierda de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="68aad-271">The offsets are from the upper left corner of the screen.</span></span> <span data-ttu-id="68aad-272">En los procesos de GUI, la posición especificada se usa la primera vez que el nuevo proceso llama a [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para crear una ventana superpuesta si el parámetro *X* de **CreateWindow** es **CW \_ USEDEFAULT**.</span><span class="sxs-lookup"><span data-stu-id="68aad-272">For GUI processes, the specified position is used the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the *X* parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> <span data-ttu-id="68aad-273">\[! NOTA X\]</span><span class="sxs-lookup"><span data-stu-id="68aad-273">\[!Note  X\]</span></span>  
> <span data-ttu-id="68aad-274">y **y no se** pueden especificar de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="68aad-274">and **Y** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="68aad-275">**XCountChars**</span><span class="sxs-lookup"><span data-stu-id="68aad-275">**XCountChars**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68aad-276">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68aad-276">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68aad-277">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="68aad-277">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="68aad-278">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| XCountChars")</span><span class="sxs-lookup"><span data-stu-id="68aad-278">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|XCountChars")</span></span>
</dt> </dl>

<span data-ttu-id="68aad-279">Ancho del búfer de pantalla en columnas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="68aad-279">Screen buffer width in character columns.</span></span> <span data-ttu-id="68aad-280">Esta propiedad se usa para los procesos que crean una ventana de consola y se omite en los procesos de la GUI.</span><span class="sxs-lookup"><span data-stu-id="68aad-280">This property is used for processes that create a console window, and is ignored in GUI processes.</span></span>

> [!Note]  
> <span data-ttu-id="68aad-281">**XCountChars** y **YCountChars** no se pueden especificar de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="68aad-281">**XCountChars** and **YCountChars** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="68aad-282">**XSize**</span><span class="sxs-lookup"><span data-stu-id="68aad-282">**XSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68aad-283">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68aad-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68aad-284">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="68aad-284">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="68aad-285">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwXSize")</span><span class="sxs-lookup"><span data-stu-id="68aad-285">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwXSize")</span></span>
</dt> </dl>

<span data-ttu-id="68aad-286">Ancho en píxeles de una ventana si se crea una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="68aad-286">Pixel width of a window if a new window is created.</span></span> <span data-ttu-id="68aad-287">Para los procesos de GUI, solo se usa la primera vez que el nuevo proceso llama a [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para crear una ventana superpuesta si el parámetro NWidth de **CreateWindow** es **CW \_ USEDEFAULT**.</span><span class="sxs-lookup"><span data-stu-id="68aad-287">For GUI processes, this is only used the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the nWidth parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> [!Note]  
> <span data-ttu-id="68aad-288">**Xsize** y **YSize** no se pueden especificar de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="68aad-288">**XSize** and **YSize** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="68aad-289">**S**</span><span class="sxs-lookup"><span data-stu-id="68aad-289">**Y**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68aad-290">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68aad-290">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68aad-291">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="68aad-291">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="68aad-292">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwY")</span><span class="sxs-lookup"><span data-stu-id="68aad-292">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwY")</span></span>
</dt> </dl>

<span data-ttu-id="68aad-293">Desplazamiento en píxeles de la esquina superior izquierda de una ventana si se crea una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="68aad-293">Pixel offset of the upper-left corner of a window if a new window is created.</span></span> <span data-ttu-id="68aad-294">Los desplazamientos se encuentran en la esquina superior izquierda de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="68aad-294">The offsets are from the upper-left corner of the screen.</span></span> <span data-ttu-id="68aad-295">En los procesos de GUI, la posición especificada se usa la primera vez que el nuevo proceso llama a [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para crear una ventana superpuesta si el parámetro *y* de **CreateWindow** es **CW \_ USEDEFAULT**.</span><span class="sxs-lookup"><span data-stu-id="68aad-295">For GUI processes, the specified position is used the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the *y* parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> <span data-ttu-id="68aad-296">\[! NOTA X\]</span><span class="sxs-lookup"><span data-stu-id="68aad-296">\[!Note  X\]</span></span>  
> <span data-ttu-id="68aad-297">y **y no se** pueden especificar de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="68aad-297">and **Y** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="68aad-298">**YCountChars**</span><span class="sxs-lookup"><span data-stu-id="68aad-298">**YCountChars**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68aad-299">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68aad-299">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68aad-300">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="68aad-300">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="68aad-301">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| YCountChars")</span><span class="sxs-lookup"><span data-stu-id="68aad-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|YCountChars")</span></span>
</dt> </dl>

<span data-ttu-id="68aad-302">Alto del búfer de pantalla en filas de caracteres.</span><span class="sxs-lookup"><span data-stu-id="68aad-302">Screen buffer height in character rows.</span></span> <span data-ttu-id="68aad-303">Esta propiedad se usa para los procesos que crean una ventana de la consola, pero se omite en los procesos de la GUI.</span><span class="sxs-lookup"><span data-stu-id="68aad-303">This property is used for processes that create a console window, but is ignored in GUI processes.</span></span>

> [!Note]  
> <span data-ttu-id="68aad-304">**XCountChars** y **YCountChars** no se pueden especificar de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="68aad-304">**XCountChars** and **YCountChars** cannot be specified independently.</span></span>

 

</dd> <dt>

<span data-ttu-id="68aad-305">**YSize**</span><span class="sxs-lookup"><span data-stu-id="68aad-305">**YSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68aad-306">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68aad-306">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68aad-307">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="68aad-307">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="68aad-308">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Process and Thread Structures \| [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) \| dwYSize")</span><span class="sxs-lookup"><span data-stu-id="68aad-308">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Process and Thread Structures\|[**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa)\|dwYSize")</span></span>
</dt> </dl>

<span data-ttu-id="68aad-309">Alto en píxeles de una ventana si se crea una nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="68aad-309">Pixel height of a window if a new window is created.</span></span> <span data-ttu-id="68aad-310">Para los procesos de GUI, se usa solo la primera vez que el nuevo proceso llama a [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) para crear una ventana superpuesta si el parámetro *nWidth* de **CreateWindow** es **CW \_ USEDEFAULT**.</span><span class="sxs-lookup"><span data-stu-id="68aad-310">For GUI processes, this is used only the first time the new process calls [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to create an overlapped window if the *nWidth* parameter of **CreateWindow** is **CW\_USEDEFAULT**.</span></span>

> [!Note]  
> <span data-ttu-id="68aad-311">**Xsize** y **YSize** no se pueden especificar de forma independiente.</span><span class="sxs-lookup"><span data-stu-id="68aad-311">**XSize** and **YSize** cannot be specified independently.</span></span>

 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="68aad-312">Observaciones</span><span class="sxs-lookup"><span data-stu-id="68aad-312">Remarks</span></span>

<span data-ttu-id="68aad-313">Esta clase se deriva de [**Win32 \_ MethodParameterClass**](win32-methodparameterclass.md).</span><span class="sxs-lookup"><span data-stu-id="68aad-313">This class is derived from [**Win32\_MethodParameterClass**](win32-methodparameterclass.md).</span></span>

<span data-ttu-id="68aad-314">Información general</span><span class="sxs-lookup"><span data-stu-id="68aad-314">Overview</span></span>

<span data-ttu-id="68aad-315">El método de [**creación**](create-method-in-class-win32-process.md) de [**\_ procesos de Win32**](win32-process.md) permite configurar las opciones de inicio de cualquier proceso nuevo que se ejecute en un equipo.</span><span class="sxs-lookup"><span data-stu-id="68aad-315">The [**Win32\_Process**](win32-process.md) [**Create**](create-method-in-class-win32-process.md) method enables you to configure startup options for any new process running on a computer.</span></span> <span data-ttu-id="68aad-316">Por ejemplo, puede configurar un proceso para que se inicie en una ventana "oculta", lo que evita que un usuario vea y, posiblemente, lo interrumpa.</span><span class="sxs-lookup"><span data-stu-id="68aad-316">For example, you can configure a process so that it starts in a "hidden" window, which prevents a user from seeing, and possibly interrupting, it.</span></span> <span data-ttu-id="68aad-317">Si el proceso se ejecuta en una ventana de comandos, puede configurar el tamaño, el título y los colores de primer plano y de fondo de la ventana.</span><span class="sxs-lookup"><span data-stu-id="68aad-317">If the process runs in a command window, you can configure the size, title, and foreground and background colors of the window.</span></span>

<span data-ttu-id="68aad-318">Las opciones de inicio se configuran mediante la clase **\_ ProcessStartup de Win32** .</span><span class="sxs-lookup"><span data-stu-id="68aad-318">Startup options are configured using the **Win32\_ProcessStartup** class.</span></span> <span data-ttu-id="68aad-319">**Win32 \_ ProcessStartup** es una clase de tipo de método; la clase de tipo de método existe únicamente para pasar información a un método.</span><span class="sxs-lookup"><span data-stu-id="68aad-319">**Win32\_ProcessStartup** is a Method Type class; the Method Type class exists solely to pass information to a method.</span></span> <span data-ttu-id="68aad-320">En este caso, todas las propiedades de una instancia de **Win32 \_ ProcessStartup** se pasan a una instancia del [**\_ proceso de Win32**](win32-process.md).</span><span class="sxs-lookup"><span data-stu-id="68aad-320">In this case, all the properties of an instance of **Win32\_ProcessStartup** are passed to an instance of [**Win32\_Process**](win32-process.md).</span></span>

<span data-ttu-id="68aad-321">**Usar Win32 \_ ProcessStartup**</span><span class="sxs-lookup"><span data-stu-id="68aad-321">**Using Win32\_ProcessStartup**</span></span>

1.  <span data-ttu-id="68aad-322">Cree una instancia de **Win32 \_ ProcessStartup**.</span><span class="sxs-lookup"><span data-stu-id="68aad-322">Create an instance of **Win32\_ProcessStartup**.</span></span>
2.  <span data-ttu-id="68aad-323">Configure las propiedades de la nueva instancia.</span><span class="sxs-lookup"><span data-stu-id="68aad-323">Configure the properties of the new instance.</span></span>
3.  <span data-ttu-id="68aad-324">Incluya la instancia como parte del método de creación de [**\_ procesos de Win32**](win32-process.md) .</span><span class="sxs-lookup"><span data-stu-id="68aad-324">Include the instance as part of the [**Win32\_Process**](win32-process.md) Create method.</span></span>

<span data-ttu-id="68aad-325">Por ejemplo, si ha creado una instancia de **Win32 \_ ProcessStartup** denominada objConfig, debe pasar el nombre del objeto en el método Create como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="68aad-325">For example, if you have created a **Win32\_ProcessStartup** instance named objConfig, you would pass the object name in the Create method as follows:</span></span>

`errReturn = objProcess.Create("Database.exe", null, objConfig, intProcessID)`

## <a name="examples"></a><span data-ttu-id="68aad-326">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="68aad-326">Examples</span></span>

<span data-ttu-id="68aad-327">Puede usar la clase **Win32 \_ ProcessStartup** para configurar varias opciones de inicio para un proceso.</span><span class="sxs-lookup"><span data-stu-id="68aad-327">You can use the **Win32\_ProcessStartup** class to configure various startup options for a process.</span></span> <span data-ttu-id="68aad-328">Estas opciones incluyen, entre otras, la creación de un proceso en una ventana oculta y la creación de un proceso de mayor prioridad.</span><span class="sxs-lookup"><span data-stu-id="68aad-328">These options include, but are not limited to, such things as creating a process in a hidden window and creating a higher-priority process.</span></span> <span data-ttu-id="68aad-329">El siguiente VBScript crea un proceso en una ventana oculta.</span><span class="sxs-lookup"><span data-stu-id="68aad-329">The following VBScript creates a process in a hidden window.</span></span>


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



<span data-ttu-id="68aad-330">El siguiente VBScript crea un proceso de mayor prioridad.</span><span class="sxs-lookup"><span data-stu-id="68aad-330">The following VBScript creates a higher-priority process.</span></span>


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



<span data-ttu-id="68aad-331">En el siguiente ejemplo de código de VBScript se crea un proceso de Bloc de notas en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="68aad-331">The following VBScript code example creates a Notepad process on the local computer.</span></span> <span data-ttu-id="68aad-332">**Win32 \_ ProcessStartup** se usa para configurar las opciones del proceso.</span><span class="sxs-lookup"><span data-stu-id="68aad-332">**Win32\_ProcessStartup** is used to configure the process settings.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="68aad-333">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68aad-333">Requirements</span></span>



| <span data-ttu-id="68aad-334">Requisito</span><span class="sxs-lookup"><span data-stu-id="68aad-334">Requirement</span></span> | <span data-ttu-id="68aad-335">Value</span><span class="sxs-lookup"><span data-stu-id="68aad-335">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68aad-336">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68aad-336">Minimum supported client</span></span><br/> | <span data-ttu-id="68aad-337">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68aad-337">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="68aad-338">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68aad-338">Minimum supported server</span></span><br/> | <span data-ttu-id="68aad-339">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68aad-339">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="68aad-340">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="68aad-340">Namespace</span></span><br/>                | <span data-ttu-id="68aad-341">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="68aad-341">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="68aad-342">MOF</span><span class="sxs-lookup"><span data-stu-id="68aad-342">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68aad-343"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68aad-343"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="68aad-344">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="68aad-344">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68aad-345"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68aad-345"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68aad-346">Consulte también</span><span class="sxs-lookup"><span data-stu-id="68aad-346">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68aad-347">**Win32 \_ MethodParameterClass**</span><span class="sxs-lookup"><span data-stu-id="68aad-347">**Win32\_MethodParameterClass**</span></span>](win32-methodparameterclass.md)
</dt> <dt>

[<span data-ttu-id="68aad-348">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="68aad-348">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="68aad-349">**\_Proceso Win32**</span><span class="sxs-lookup"><span data-stu-id="68aad-349">**Win32\_Process**</span></span>](win32-process.md)
</dt> <dt>

[<span data-ttu-id="68aad-350">**\_\_ProviderHostQuotaConfiguration**</span><span class="sxs-lookup"><span data-stu-id="68aad-350">**\_\_ProviderHostQuotaConfiguration**</span></span>](../wmisdk/--providerhostquotaconfiguration.md)
</dt> <dt>

[<span data-ttu-id="68aad-351">Tareas de WMI: procesos</span><span class="sxs-lookup"><span data-stu-id="68aad-351">WMI Tasks: Processes</span></span>](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
