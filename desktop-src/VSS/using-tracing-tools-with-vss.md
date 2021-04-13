---
description: Para recopilar información de seguimiento de la infraestructura de VSS, puede usar la herramienta VssTrace, la herramienta Logman o la herramienta tracelog.
ms.assetid: afe2a0ed-1a8e-4f8b-be9e-241d55cd9ef6
title: Usar herramientas de seguimiento con VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073a2ae9ba2ba2771abdc37ff0291764ed5e9efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275426"
---
# <a name="using-tracing-tools-with-vss"></a><span data-ttu-id="da34c-103">Usar herramientas de seguimiento con VSS</span><span class="sxs-lookup"><span data-stu-id="da34c-103">Using Tracing Tools with VSS</span></span>

<span data-ttu-id="da34c-104">Para recopilar información de seguimiento de la infraestructura de VSS, puede usar la herramienta VssTrace, la herramienta Logman o la herramienta tracelog.</span><span class="sxs-lookup"><span data-stu-id="da34c-104">To collect tracing information for the VSS infrastructure, you can use the VssTrace tool, the Logman tool, or the Tracelog tool.</span></span> <span data-ttu-id="da34c-105">VssTrace está disponible en el kit de desarrollo de software (SDK) de Microsoft Windows y se puede usar para realizar un seguimiento de las aplicaciones VSS en Windows 7 y versiones posteriores del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="da34c-105">VssTrace is available in the Microsoft Windows Software Development Kit (SDK) and can be used to trace VSS applications on Windows 7 and later versions of the Windows operating system.</span></span> <span data-ttu-id="da34c-106">Logman es un controlador de seguimiento para los eventos de seguimiento y los contadores de rendimiento. también se puede usar para realizar un seguimiento de las aplicaciones VSS en Windows 7 y versiones posteriores del sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="da34c-106">Logman is a trace controller for trace events and performance counters; it can also be used to trace VSS applications on Windows 7 and later versions of the Windows operating system.</span></span> <span data-ttu-id="da34c-107">Tracelog se incluye en el kit de controladores de Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="da34c-107">Tracelog is included in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="da34c-108">Para usar las herramientas de seguimiento con [recuperación automática del sistema (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md), consulte [usar herramientas de seguimiento con aplicaciones de ASR](using-tracing-tools-with-vss-asr-applications.md).</span><span class="sxs-lookup"><span data-stu-id="da34c-108">To use tracing tools with [Automated System Recovery (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md), see [Using Tracing Tools with ASR Applications](using-tracing-tools-with-vss-asr-applications.md).</span></span>

> [!Note]  
> <span data-ttu-id="da34c-109">VssTrace, Logman y tracelog requieren privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="da34c-109">VssTrace, Logman, and Tracelog all require administrator privilege.</span></span>

 

<span data-ttu-id="da34c-110">Para obtener información acerca de cada herramienta, vea las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="da34c-110">For information about each tool, see the following sections:</span></span>

-   [<span data-ttu-id="da34c-111">Usar VssTrace</span><span class="sxs-lookup"><span data-stu-id="da34c-111">Using VssTrace</span></span>](#using-vsstrace)
    -   [<span data-ttu-id="da34c-112">Opciones de Command-Line de VssTrace</span><span class="sxs-lookup"><span data-stu-id="da34c-112">VssTrace Command-Line Options</span></span>](#vsstrace-command-line-options)
-   [<span data-ttu-id="da34c-113">Usar Logman</span><span class="sxs-lookup"><span data-stu-id="da34c-113">Using Logman</span></span>](#using-logman)
-   [<span data-ttu-id="da34c-114">Usar tracelog</span><span class="sxs-lookup"><span data-stu-id="da34c-114">Using Tracelog</span></span>](#using-tracelog)

## <a name="using-vsstrace"></a><span data-ttu-id="da34c-115">Usar VssTrace</span><span class="sxs-lookup"><span data-stu-id="da34c-115">Using VssTrace</span></span>

<span data-ttu-id="da34c-116">Para ejecutar la herramienta VssTrace desde la línea de comandos, use la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="da34c-116">To run the VssTrace tool from the command line, use the following syntax:</span></span>

<span data-ttu-id="da34c-117"> *Opciones de la línea de comandos de* vsstrace</span><span class="sxs-lookup"><span data-stu-id="da34c-117">**vsstrace** *command-line-options*</span></span>

<span data-ttu-id="da34c-118">Para mostrar la ayuda de línea de comandos concisa para la herramienta VssTrace, use la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="da34c-118">To display concise command-line help for the VssTrace tool, use the following syntax:</span></span>

<span data-ttu-id="da34c-119">**vsstrace-ayuda**</span><span class="sxs-lookup"><span data-stu-id="da34c-119">**vsstrace -help**</span></span>

<span data-ttu-id="da34c-120">Para mostrar ayuda detallada de la línea de comandos para la herramienta VssTrace, use la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="da34c-120">To display detailed command-line help for the VssTrace tool, use the following syntax:</span></span>

<span data-ttu-id="da34c-121">**vsstrace-help all**</span><span class="sxs-lookup"><span data-stu-id="da34c-121">**vsstrace -help all**</span></span>

### <a name="vsstrace-command-line-options"></a><span data-ttu-id="da34c-122">Opciones de Command-Line de VssTrace</span><span class="sxs-lookup"><span data-stu-id="da34c-122">VssTrace Command-Line Options</span></span>

<span data-ttu-id="da34c-123">La herramienta VssTrace utiliza las siguientes opciones de la línea de comandos:</span><span class="sxs-lookup"><span data-stu-id="da34c-123">The VssTrace tool uses the following command-line options:</span></span>

<dl> <dt>

<span data-ttu-id="da34c-124"><span id="-f_Flags"></span><span id="-f_flags"></span><span id="-F_FLAGS"></span>**-f (** *marcas* )</span><span class="sxs-lookup"><span data-stu-id="da34c-124"><span id="-f_Flags"></span><span id="-f_flags"></span><span id="-F_FLAGS"></span>**-f** *Flags*</span></span>
</dt> <dd>

<span data-ttu-id="da34c-125">Habilite los módulos cuyas marcas se especifican en *la máscara de* la máscara.</span><span class="sxs-lookup"><span data-stu-id="da34c-125">Enable the modules whose flags are specified by the *Flags* bitmask.</span></span> <span data-ttu-id="da34c-126">Cada marca corresponde a un módulo de VSS.</span><span class="sxs-lookup"><span data-stu-id="da34c-126">Each flag corresponds to a VSS module.</span></span> <span data-ttu-id="da34c-127">Si *Flags* es cero, no se habilita ningún módulo.</span><span class="sxs-lookup"><span data-stu-id="da34c-127">If *Flags* is zero, no modules are enabled.</span></span> <span data-ttu-id="da34c-128">Tenga en cuenta que la mayoría de los módulos están habilitados de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="da34c-128">Note that most modules are enabled by default.</span></span> <span data-ttu-id="da34c-129">Esta opción se puede combinar con la **+** opción _Module_ .</span><span class="sxs-lookup"><span data-stu-id="da34c-129">This option can be combined with the **+**_Module_ option.</span></span> <span data-ttu-id="da34c-130">Por ejemplo, **vsstrace-f 0 + Writer + coords** deshabilita el seguimiento de todos los módulos que están habilitados de forma predeterminada y habilita el seguimiento de escritores de VSS y el servicio VSS.</span><span class="sxs-lookup"><span data-stu-id="da34c-130">For example, **vsstrace -f 0 +WRITER +COORD** disables tracing of all of the modules that are enabled by default and enables tracing of VSS writers and the VSS service.</span></span> <span data-ttu-id="da34c-131">Como alternativa, **vsstrace + f 0xFFFF-coordenadas** permite el seguimiento de todos los módulos excepto el servicio VSS.</span><span class="sxs-lookup"><span data-stu-id="da34c-131">Alternatively, **vsstrace +f 0xffff -COORD** enables tracing of all modules except the VSS service.</span></span>

> [!Note]  
> <span data-ttu-id="da34c-132">Si usa la opción **-f** junto con la **+** opción de _módulo_ , el **-f** debe aparecer antes de la opción de **+** _módulo_ .</span><span class="sxs-lookup"><span data-stu-id="da34c-132">If you use the **-f** option together with the **+**_Module_ option, the **-f** must appear before the **+**_Module_ option.</span></span>

 

<span data-ttu-id="da34c-133">En la tabla siguiente se enumeran el nombre del módulo y la marca de cada módulo disponible.</span><span class="sxs-lookup"><span data-stu-id="da34c-133">The following table lists the module name and flag for each available module.</span></span>

| <span data-ttu-id="da34c-134">Módulo</span><span class="sxs-lookup"><span data-stu-id="da34c-134">Module</span></span> | <span data-ttu-id="da34c-135">Marca</span><span class="sxs-lookup"><span data-stu-id="da34c-135">Flag</span></span>       | <span data-ttu-id="da34c-136">Habilitado de forma predeterminada</span><span class="sxs-lookup"><span data-stu-id="da34c-136">Enabled by default</span></span> | <span data-ttu-id="da34c-137">Elementos con seguimiento</span><span class="sxs-lookup"><span data-stu-id="da34c-137">Items traced</span></span>                                                                                                                                  |
|--------|------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da34c-138">EXCEPT</span><span class="sxs-lookup"><span data-stu-id="da34c-138">EXCEPT</span></span> | <span data-ttu-id="da34c-139">0x00000001</span><span class="sxs-lookup"><span data-stu-id="da34c-139">0x00000001</span></span> | <span data-ttu-id="da34c-140">Sí</span><span class="sxs-lookup"><span data-stu-id="da34c-140">Yes</span></span>                | <span data-ttu-id="da34c-141">Control de excepciones de C++.</span><span class="sxs-lookup"><span data-stu-id="da34c-141">C++ exception handling.</span></span>                                                                                                                       |
| <span data-ttu-id="da34c-142">COORDS</span><span class="sxs-lookup"><span data-stu-id="da34c-142">COORD</span></span>  | <span data-ttu-id="da34c-143">0x00000002</span><span class="sxs-lookup"><span data-stu-id="da34c-143">0x00000002</span></span> | <span data-ttu-id="da34c-144">Sí</span><span class="sxs-lookup"><span data-stu-id="da34c-144">Yes</span></span>                | <span data-ttu-id="da34c-145">El servicio VSS, que también se denomina Coordinador de VSS.</span><span class="sxs-lookup"><span data-stu-id="da34c-145">The VSS service, which is also called the VSS coordinator.</span></span>                                                                                    |
| <span data-ttu-id="da34c-146">SWPRV</span><span class="sxs-lookup"><span data-stu-id="da34c-146">SWPRV</span></span>  | <span data-ttu-id="da34c-147">0x00000004</span><span class="sxs-lookup"><span data-stu-id="da34c-147">0x00000004</span></span> | <span data-ttu-id="da34c-148">Sí</span><span class="sxs-lookup"><span data-stu-id="da34c-148">Yes</span></span>                | <span data-ttu-id="da34c-149">El servicio de proveedor de instantáneas de sistema de VSS.</span><span class="sxs-lookup"><span data-stu-id="da34c-149">The VSS System Shadow Copy Provider service.</span></span>                                                                                                  |
| <span data-ttu-id="da34c-150">BUCOMP</span><span class="sxs-lookup"><span data-stu-id="da34c-150">BUCOMP</span></span> | <span data-ttu-id="da34c-151">0x00000008</span><span class="sxs-lookup"><span data-stu-id="da34c-151">0x00000008</span></span> | <span data-ttu-id="da34c-152">Sí</span><span class="sxs-lookup"><span data-stu-id="da34c-152">Yes</span></span>                | <span data-ttu-id="da34c-153">El solicitante de VSS y el procesamiento de metadatos de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="da34c-153">The VSS requester and backup metadata processing.</span></span>                                                                                             |
| <span data-ttu-id="da34c-154">WRITER</span><span class="sxs-lookup"><span data-stu-id="da34c-154">WRITER</span></span> | <span data-ttu-id="da34c-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="da34c-155">0x00000010</span></span> | <span data-ttu-id="da34c-156">Sí</span><span class="sxs-lookup"><span data-stu-id="da34c-156">Yes</span></span>                | <span data-ttu-id="da34c-157">VSS Writer operaciones y las implementaciones del escritor hospedado de VSS, como el sistema de escritura del registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="da34c-157">VSS writer operations and VSS hosted writer implementations, such as the Windows Registry writer.</span></span>                                             |
| <span data-ttu-id="da34c-158">VSSAPI</span><span class="sxs-lookup"><span data-stu-id="da34c-158">VSSAPI</span></span> | <span data-ttu-id="da34c-159">0x00000020</span><span class="sxs-lookup"><span data-stu-id="da34c-159">0x00000020</span></span> | <span data-ttu-id="da34c-160">Sí</span><span class="sxs-lookup"><span data-stu-id="da34c-160">Yes</span></span>                | <span data-ttu-id="da34c-161">Funciones varias de la API de VSS exportadas por VSSAPI.DLL.</span><span class="sxs-lookup"><span data-stu-id="da34c-161">Miscellaneous functions of the VSS API exported by VSSAPI.DLL.</span></span>                                                                                |
| <span data-ttu-id="da34c-162">HWDIAG</span><span class="sxs-lookup"><span data-stu-id="da34c-162">HWDIAG</span></span> | <span data-ttu-id="da34c-163">0x00000040</span><span class="sxs-lookup"><span data-stu-id="da34c-163">0x00000040</span></span> | <span data-ttu-id="da34c-164">Sí</span><span class="sxs-lookup"><span data-stu-id="da34c-164">Yes</span></span>                | <span data-ttu-id="da34c-165">Operaciones y infraestructura del proveedor de hardware de VSS.</span><span class="sxs-lookup"><span data-stu-id="da34c-165">VSS hardware provider infrastructure and operations.</span></span>                                                                                          |
| <span data-ttu-id="da34c-166">ADMIN</span><span class="sxs-lookup"><span data-stu-id="da34c-166">ADMIN</span></span>  | <span data-ttu-id="da34c-167">0x00000080</span><span class="sxs-lookup"><span data-stu-id="da34c-167">0x00000080</span></span> | <span data-ttu-id="da34c-168">Sí</span><span class="sxs-lookup"><span data-stu-id="da34c-168">Yes</span></span>                | <span data-ttu-id="da34c-169">Utilidades de línea de comandos de VSS como VSSADMIN.EXE y DISKSHADOW.EXE.</span><span class="sxs-lookup"><span data-stu-id="da34c-169">VSS command line utilities such as VSSADMIN.EXE and DISKSHADOW.EXE.</span></span>                                                                           |
| <span data-ttu-id="da34c-170">VSSUI</span><span class="sxs-lookup"><span data-stu-id="da34c-170">VSSUI</span></span>  | <span data-ttu-id="da34c-171">0x00000100</span><span class="sxs-lookup"><span data-stu-id="da34c-171">0x00000100</span></span> | <span data-ttu-id="da34c-172">Sí</span><span class="sxs-lookup"><span data-stu-id="da34c-172">Yes</span></span>                | <span data-ttu-id="da34c-173">La interfaz de usuario (UI) de configuración de Instantáneas para carpetas compartidas.</span><span class="sxs-lookup"><span data-stu-id="da34c-173">The Shadow Copies for Shared Folders configuration user interface (UI).</span></span> <span data-ttu-id="da34c-174">La interfaz de usuario solo está disponible en los sistemas operativos Windows Server.</span><span class="sxs-lookup"><span data-stu-id="da34c-174">The UI is available only on Windows Server operating systems.</span></span>         |
| <span data-ttu-id="da34c-175">PRUEBA</span><span class="sxs-lookup"><span data-stu-id="da34c-175">TEST</span></span>   | <span data-ttu-id="da34c-176">0x00000200</span><span class="sxs-lookup"><span data-stu-id="da34c-176">0x00000200</span></span> | <span data-ttu-id="da34c-177">Sí</span><span class="sxs-lookup"><span data-stu-id="da34c-177">Yes</span></span>                | <span data-ttu-id="da34c-178">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="da34c-178">Not applicable.</span></span> <span data-ttu-id="da34c-179">(Este módulo de seguimiento está reservado).</span><span class="sxs-lookup"><span data-stu-id="da34c-179">(This tracing module is reserved.)</span></span>                                                                                            |
| <span data-ttu-id="da34c-180">INSERCIÓN</span><span class="sxs-lookup"><span data-stu-id="da34c-180">IOCTL</span></span>  | <span data-ttu-id="da34c-181">0x00000400</span><span class="sxs-lookup"><span data-stu-id="da34c-181">0x00000400</span></span> | <span data-ttu-id="da34c-182">Sí</span><span class="sxs-lookup"><span data-stu-id="da34c-182">Yes</span></span>                | <span data-ttu-id="da34c-183">Detalles de las operaciones de FSCTL y IOCTL que ha iniciado el servicio VSS mediante una llamada a la función [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) .</span><span class="sxs-lookup"><span data-stu-id="da34c-183">Details of FSCTL and IOCTL operations that the VSS service has initiated by calling the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function.</span></span> |
| <span data-ttu-id="da34c-184">Group</span><span class="sxs-lookup"><span data-stu-id="da34c-184">GEN</span></span>    | <span data-ttu-id="da34c-185">0x00000800</span><span class="sxs-lookup"><span data-stu-id="da34c-185">0x00000800</span></span> | <span data-ttu-id="da34c-186">Sí</span><span class="sxs-lookup"><span data-stu-id="da34c-186">Yes</span></span>                | <span data-ttu-id="da34c-187">Funciones generales de la utilidad VSS, como asignadores, clases de cadena y operaciones de registro y de volumen.</span><span class="sxs-lookup"><span data-stu-id="da34c-187">General VSS utility functions, such as allocators, string classes, and registry and volume operations.</span></span>                                        |
| <span data-ttu-id="da34c-188">WRXML</span><span class="sxs-lookup"><span data-stu-id="da34c-188">WRXML</span></span>  | <span data-ttu-id="da34c-189">0x00001000</span><span class="sxs-lookup"><span data-stu-id="da34c-189">0x00001000</span></span> | <span data-ttu-id="da34c-190">No</span><span class="sxs-lookup"><span data-stu-id="da34c-190">No</span></span>                 | <span data-ttu-id="da34c-191">Procesamiento XML para metadatos del escritor.</span><span class="sxs-lookup"><span data-stu-id="da34c-191">XML processing for writer metadata.</span></span> <span data-ttu-id="da34c-192">Este módulo tiene un nivel muy alto de ruido.</span><span class="sxs-lookup"><span data-stu-id="da34c-192">This module has a very high level of noise.</span></span>                                                               |
| <span data-ttu-id="da34c-193">VSSXML</span><span class="sxs-lookup"><span data-stu-id="da34c-193">VSSXML</span></span> | <span data-ttu-id="da34c-194">0x00002000</span><span class="sxs-lookup"><span data-stu-id="da34c-194">0x00002000</span></span> | <span data-ttu-id="da34c-195">No</span><span class="sxs-lookup"><span data-stu-id="da34c-195">No</span></span>                 | <span data-ttu-id="da34c-196">Clases base de procesamiento XML.</span><span class="sxs-lookup"><span data-stu-id="da34c-196">XML processing base classes.</span></span> <span data-ttu-id="da34c-197">Este módulo tiene un nivel muy alto de ruido.</span><span class="sxs-lookup"><span data-stu-id="da34c-197">This module has a very high level of noise.</span></span>                                                                      |



 

</dd> <dt>

<span data-ttu-id="da34c-198"><span id="_Module"></span><span id="_module"></span><span id="_MODULE"></span>**+**_Destina_</span><span class="sxs-lookup"><span data-stu-id="da34c-198"><span id="_Module"></span><span id="_module"></span><span id="_MODULE"></span>**+**_Module_</span></span>
</dt> <dd>

<span data-ttu-id="da34c-199">Habilite el módulo especificado por *módulo*.</span><span class="sxs-lookup"><span data-stu-id="da34c-199">Enable the module specified by *Module*.</span></span> <span data-ttu-id="da34c-200">Se puede habilitar más de un módulo a la vez.</span><span class="sxs-lookup"><span data-stu-id="da34c-200">More than one module can be enabled at a time.</span></span> <span data-ttu-id="da34c-201">Para enumerar los módulos disponibles, escriba **vsstrace – Help modules** en el símbolo de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="da34c-201">To list the available modules, type **vsstrace –help modules** at the command-line prompt.</span></span>

</dd> <dt>

<span data-ttu-id="da34c-202"><span id="-Module"></span><span id="-module"></span><span id="-MODULE"></span>**-**_Destina_</span><span class="sxs-lookup"><span data-stu-id="da34c-202"><span id="-Module"></span><span id="-module"></span><span id="-MODULE"></span>**-**_Module_</span></span>
</dt> <dd>

<span data-ttu-id="da34c-203">Deshabilite el módulo especificado por *módulo*.</span><span class="sxs-lookup"><span data-stu-id="da34c-203">Disable the module specified by *Module*.</span></span> <span data-ttu-id="da34c-204">Para enumerar los módulos disponibles, escriba **vsstrace – Help modules** en el símbolo de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="da34c-204">To list the available modules, type **vsstrace –help modules** at the command-line prompt.</span></span>

</dd> <dt>

<span data-ttu-id="da34c-205"><span id="_pid_ProcessId"></span><span id="_pid_processid"></span><span id="_PID_PROCESSID"></span>**+**  ID. de la PID</span><span class="sxs-lookup"><span data-stu-id="da34c-205"><span id="_pid_ProcessId"></span><span id="_pid_processid"></span><span id="_PID_PROCESSID"></span>**+pid** *ProcessId*</span></span>
</dt> <dd>

<span data-ttu-id="da34c-206">Habilite el proceso especificado por *ProcessId*.</span><span class="sxs-lookup"><span data-stu-id="da34c-206">Enable the process specified by *ProcessId*.</span></span> <span data-ttu-id="da34c-207">Para habilitar todos los procesos, use " \* " para el valor de *ProcessId*.</span><span class="sxs-lookup"><span data-stu-id="da34c-207">To enable all processes, use "\*" for the value of *ProcessId*.</span></span> <span data-ttu-id="da34c-208">Se puede especificar más de una opción de **PID** a la vez.</span><span class="sxs-lookup"><span data-stu-id="da34c-208">More than one **pid** option can be specified at a time.</span></span> <span data-ttu-id="da34c-209">El orden de las opciones determina qué procesos están habilitados o deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="da34c-209">The order of the options determines which processes are enabled or disabled.</span></span> <span data-ttu-id="da34c-210">Por ejemplo, para habilitar solo el proceso cuyo identificador de proceso es 0xe8c, use **vsstrace-PID \* + PID 0xe8c**.</span><span class="sxs-lookup"><span data-stu-id="da34c-210">For example, to enable only the process whose process identifier is 0xe8c, use **vsstrace -pid \* +pid 0xe8c**.</span></span>

</dd> <dt>

<span data-ttu-id="da34c-211"><span id="-pid_ProcessId"></span><span id="-pid_processid"></span><span id="-PID_PROCESSID"></span>**-ID. de la PID** </span><span class="sxs-lookup"><span data-stu-id="da34c-211"><span id="-pid_ProcessId"></span><span id="-pid_processid"></span><span id="-PID_PROCESSID"></span>**-pid** *ProcessId*</span></span>
</dt> <dd>

<span data-ttu-id="da34c-212">Deshabilitar el proceso especificado por *ProcessId*.</span><span class="sxs-lookup"><span data-stu-id="da34c-212">Disable the process specified by *ProcessId*.</span></span> <span data-ttu-id="da34c-213">Para deshabilitar todos los procesos, use " \* " para el valor de *ProcessId*.</span><span class="sxs-lookup"><span data-stu-id="da34c-213">To disable all processes, use "\*" for the value of *ProcessId*.</span></span> <span data-ttu-id="da34c-214">Se puede especificar más de una opción de **PID** a la vez.</span><span class="sxs-lookup"><span data-stu-id="da34c-214">More than one **pid** option can be specified at a time.</span></span> <span data-ttu-id="da34c-215">El orden de las opciones determina qué procesos están habilitados o deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="da34c-215">The order of the options determines which processes are enabled or disabled.</span></span> <span data-ttu-id="da34c-216">Por ejemplo, para deshabilitar todos los procesos excepto el proceso cuyo identificador de proceso es 0xe8c, use **vsstrace-PID \* + PID 0xe8c**.</span><span class="sxs-lookup"><span data-stu-id="da34c-216">For example, to disable all processes except the process whose process identifier is 0xe8c, use **vsstrace -pid \* +pid 0xe8c**.</span></span>

</dd> <dt>

<span data-ttu-id="da34c-217"><span id="_tid_ThreadId"></span><span id="_tid_threadid"></span><span id="_TID_THREADID"></span>**+** *ThreadId* de TID</span><span class="sxs-lookup"><span data-stu-id="da34c-217"><span id="_tid_ThreadId"></span><span id="_tid_threadid"></span><span id="_TID_THREADID"></span>**+tid** *ThreadId*</span></span>
</dt> <dd>

<span data-ttu-id="da34c-218">Habilita el subproceso especificado por *ThreadId*.</span><span class="sxs-lookup"><span data-stu-id="da34c-218">Enable the thread specified by *ThreadId*.</span></span> <span data-ttu-id="da34c-219">Para habilitar todos los subprocesos, use " \* " para el valor de *ThreadId*.</span><span class="sxs-lookup"><span data-stu-id="da34c-219">To enable all threads, use "\*" for the value of *ThreadId*.</span></span> <span data-ttu-id="da34c-220">Se puede especificar más de una opción de **TID** a la vez.</span><span class="sxs-lookup"><span data-stu-id="da34c-220">More than one **tid** option can be specified at a time.</span></span> <span data-ttu-id="da34c-221">El orden de las opciones determina los subprocesos que están habilitados o deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="da34c-221">The order of the options determines which threads are enabled or disabled.</span></span> <span data-ttu-id="da34c-222">Por ejemplo, para habilitar solo el subproceso cuyo identificador de proceso es 0x31a, use **vsstrace-TID \* + TID 0x31a**.</span><span class="sxs-lookup"><span data-stu-id="da34c-222">For example, to enable only the thread whose process identifier is 0x31a, use **vsstrace -tid \* +tid 0x31a**.</span></span>

</dd> <dt>

<span data-ttu-id="da34c-223"><span id="-tid_ThreadId"></span><span id="-tid_threadid"></span><span id="-TID_THREADID"></span>**-ThreadId de TID** </span><span class="sxs-lookup"><span data-stu-id="da34c-223"><span id="-tid_ThreadId"></span><span id="-tid_threadid"></span><span id="-TID_THREADID"></span>**-tid** *ThreadId*</span></span>
</dt> <dd>

<span data-ttu-id="da34c-224">Deshabilitar el subproceso especificado por *ThreadId*.</span><span class="sxs-lookup"><span data-stu-id="da34c-224">Disable the thread specified by *ThreadId*.</span></span> <span data-ttu-id="da34c-225">Para deshabilitar todos los subprocesos, use " \* " para el valor de *ThreadId*.</span><span class="sxs-lookup"><span data-stu-id="da34c-225">To disable all threads, use "\*" for the value of *ThreadId*.</span></span> <span data-ttu-id="da34c-226">Se puede especificar más de una opción de **TID** a la vez.</span><span class="sxs-lookup"><span data-stu-id="da34c-226">More than one **tid** option can be specified at a time.</span></span> <span data-ttu-id="da34c-227">El orden de las opciones determina los subprocesos que están habilitados o deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="da34c-227">The order of the options determines which threads are enabled or disabled.</span></span> <span data-ttu-id="da34c-228">Por ejemplo, para deshabilitar todos los subprocesos excepto el subproceso cuyo identificador de proceso es 0x31a, use **vsstrace-TID \* + TID 0x31a**.</span><span class="sxs-lookup"><span data-stu-id="da34c-228">For example, to disable all threads except the thread whose process identifier is 0x31a, use **vsstrace -tid \* +tid 0x31a**.</span></span>

</dd> <dt>

<span data-ttu-id="da34c-229"><span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span>*nivel* **-l**</span><span class="sxs-lookup"><span data-stu-id="da34c-229"><span id="-l_Level"></span><span id="-l_level"></span><span id="-L_LEVEL"></span>**-l** *Level*</span></span>
</dt> <dd>

<span data-ttu-id="da34c-230">Use el nivel de seguimiento especificado por *nivel*.</span><span class="sxs-lookup"><span data-stu-id="da34c-230">Use the tracing level specified by *Level*.</span></span> <span data-ttu-id="da34c-231">Cuanto mayor sea el nivel, más detallado será el resultado del seguimiento.</span><span class="sxs-lookup"><span data-stu-id="da34c-231">The higher the level, the more verbose the trace output.</span></span> <span data-ttu-id="da34c-232">Cada nivel incluye todos los niveles inferiores.</span><span class="sxs-lookup"><span data-stu-id="da34c-232">Each level includes all of the lower levels.</span></span> <span data-ttu-id="da34c-233">El nivel predeterminado es 170.</span><span class="sxs-lookup"><span data-stu-id="da34c-233">The default level is 170.</span></span> <span data-ttu-id="da34c-234">Están disponibles los siguientes niveles.</span><span class="sxs-lookup"><span data-stu-id="da34c-234">The following levels are available.</span></span>



| <span data-ttu-id="da34c-235">Nivel</span><span class="sxs-lookup"><span data-stu-id="da34c-235">Level</span></span> | <span data-ttu-id="da34c-236">Información incluida en el resultado del seguimiento</span><span class="sxs-lookup"><span data-stu-id="da34c-236">Information included in the trace output</span></span> |
|-------|------------------------------------------|
| <span data-ttu-id="da34c-237">000</span><span class="sxs-lookup"><span data-stu-id="da34c-237">000</span></span>   | <span data-ttu-id="da34c-238">None</span><span class="sxs-lookup"><span data-stu-id="da34c-238">None</span></span>                                     |
| <span data-ttu-id="da34c-239">020</span><span class="sxs-lookup"><span data-stu-id="da34c-239">020</span></span>   | <span data-ttu-id="da34c-240">Errores graves</span><span class="sxs-lookup"><span data-stu-id="da34c-240">Fatal errors</span></span>                             |
| <span data-ttu-id="da34c-241">030</span><span class="sxs-lookup"><span data-stu-id="da34c-241">030</span></span>   | <span data-ttu-id="da34c-242">Excepciones no controladas</span><span class="sxs-lookup"><span data-stu-id="da34c-242">Unhandled exceptions</span></span>                     |
| <span data-ttu-id="da34c-243">040</span><span class="sxs-lookup"><span data-stu-id="da34c-243">040</span></span>   | <span data-ttu-id="da34c-244">Errors</span><span class="sxs-lookup"><span data-stu-id="da34c-244">Errors</span></span>                                   |
| <span data-ttu-id="da34c-245">050</span><span class="sxs-lookup"><span data-stu-id="da34c-245">050</span></span>   | <span data-ttu-id="da34c-246">Aserciones</span><span class="sxs-lookup"><span data-stu-id="da34c-246">Assertions</span></span>                               |
| <span data-ttu-id="da34c-247">060</span><span class="sxs-lookup"><span data-stu-id="da34c-247">060</span></span>   | <span data-ttu-id="da34c-248">Advertencias</span><span class="sxs-lookup"><span data-stu-id="da34c-248">Warnings</span></span>                                 |
| <span data-ttu-id="da34c-249">080</span><span class="sxs-lookup"><span data-stu-id="da34c-249">080</span></span>   | <span data-ttu-id="da34c-250">Control de excepciones</span><span class="sxs-lookup"><span data-stu-id="da34c-250">Exception handling</span></span>                       |
| <span data-ttu-id="da34c-251">100</span><span class="sxs-lookup"><span data-stu-id="da34c-251">100</span></span>   | <span data-ttu-id="da34c-252">Actividad de registro de eventos</span><span class="sxs-lookup"><span data-stu-id="da34c-252">Event Log activity</span></span>                       |
| <span data-ttu-id="da34c-253">120</span><span class="sxs-lookup"><span data-stu-id="da34c-253">120</span></span>   | <span data-ttu-id="da34c-254">Información general</span><span class="sxs-lookup"><span data-stu-id="da34c-254">General information</span></span>                      |
| <span data-ttu-id="da34c-255">140</span><span class="sxs-lookup"><span data-stu-id="da34c-255">140</span></span>   | <span data-ttu-id="da34c-256">flujo de código</span><span class="sxs-lookup"><span data-stu-id="da34c-256">Code flow</span></span>                                |
| <span data-ttu-id="da34c-257">160</span><span class="sxs-lookup"><span data-stu-id="da34c-257">160</span></span>   | <span data-ttu-id="da34c-258">Entrar y salir de la función</span><span class="sxs-lookup"><span data-stu-id="da34c-258">Function enter and exit</span></span>                  |
| <span data-ttu-id="da34c-259">170</span><span class="sxs-lookup"><span data-stu-id="da34c-259">170</span></span>   | <span data-ttu-id="da34c-260">Valores devueltos de función</span><span class="sxs-lookup"><span data-stu-id="da34c-260">Function return values</span></span>                   |
| <span data-ttu-id="da34c-261">180</span><span class="sxs-lookup"><span data-stu-id="da34c-261">180</span></span>   | <span data-ttu-id="da34c-262">Parámetros de función (conciso)</span><span class="sxs-lookup"><span data-stu-id="da34c-262">Function parameters (terse)</span></span>              |
| <span data-ttu-id="da34c-263">190</span><span class="sxs-lookup"><span data-stu-id="da34c-263">190</span></span>   | <span data-ttu-id="da34c-264">Parámetros de función (detallado)</span><span class="sxs-lookup"><span data-stu-id="da34c-264">Function parameters (verbose)</span></span>            |
| <span data-ttu-id="da34c-265">200</span><span class="sxs-lookup"><span data-stu-id="da34c-265">200</span></span>   | <span data-ttu-id="da34c-266">Nivel de información detallado 1</span><span class="sxs-lookup"><span data-stu-id="da34c-266">Verbose information level 1</span></span>              |
| <span data-ttu-id="da34c-267">210</span><span class="sxs-lookup"><span data-stu-id="da34c-267">210</span></span>   | <span data-ttu-id="da34c-268">Nivel de información detallado 2</span><span class="sxs-lookup"><span data-stu-id="da34c-268">Verbose information level 2</span></span>              |
| <span data-ttu-id="da34c-269">220</span><span class="sxs-lookup"><span data-stu-id="da34c-269">220</span></span>   | <span data-ttu-id="da34c-270">Nivel de información detallado 3</span><span class="sxs-lookup"><span data-stu-id="da34c-270">Verbose information level 3</span></span>              |
| <span data-ttu-id="da34c-271">230</span><span class="sxs-lookup"><span data-stu-id="da34c-271">230</span></span>   | <span data-ttu-id="da34c-272">Nivel de código rápido 1</span><span class="sxs-lookup"><span data-stu-id="da34c-272">Fast Code Level 1</span></span>                        |
| <span data-ttu-id="da34c-273">240</span><span class="sxs-lookup"><span data-stu-id="da34c-273">240</span></span>   | <span data-ttu-id="da34c-274">Nivel de código rápido 2</span><span class="sxs-lookup"><span data-stu-id="da34c-274">Fast Code Level 2</span></span>                        |
| <span data-ttu-id="da34c-275">250</span><span class="sxs-lookup"><span data-stu-id="da34c-275">250</span></span>   | <span data-ttu-id="da34c-276">Nivel de código rápido 3</span><span class="sxs-lookup"><span data-stu-id="da34c-276">Fast Code Level 3</span></span>                        |
| <span data-ttu-id="da34c-277">255</span><span class="sxs-lookup"><span data-stu-id="da34c-277">255</span></span>   | <span data-ttu-id="da34c-278">All</span><span class="sxs-lookup"><span data-stu-id="da34c-278">All</span></span>                                      |



 

</dd> <dt>

<span data-ttu-id="da34c-279"><span id="_indent"></span><span id="_INDENT"></span>**+ sangría**</span><span class="sxs-lookup"><span data-stu-id="da34c-279"><span id="_indent"></span><span id="_INDENT"></span>**+indent**</span></span>
</dt> <dd>

<span data-ttu-id="da34c-280">Aplique sangría a la salida del seguimiento con formato en cada función y límite de subfunción.</span><span class="sxs-lookup"><span data-stu-id="da34c-280">Indent the formatted trace output at each function and subfunction boundary.</span></span>

</dd> <dt>

<span data-ttu-id="da34c-281"><span id="-indent"></span><span id="-INDENT"></span>**-aplicar sangría**</span><span class="sxs-lookup"><span data-stu-id="da34c-281"><span id="-indent"></span><span id="-INDENT"></span>**-indent**</span></span>
</dt> <dd>

<span data-ttu-id="da34c-282">No aplique sangría a la salida de seguimiento con formato.</span><span class="sxs-lookup"><span data-stu-id="da34c-282">Do not indent the formatted trace output.</span></span>

</dd> <dt>

<span data-ttu-id="da34c-283"><span id="-etl_EtlFile"></span><span id="-etl_etlfile"></span><span id="-ETL_ETLFILE"></span>**-** *EtlFile* ETL</span><span class="sxs-lookup"><span data-stu-id="da34c-283"><span id="-etl_EtlFile"></span><span id="-etl_etlfile"></span><span id="-ETL_ETLFILE"></span>**-etl** *EtlFile*</span></span>
</dt> <dd>

<span data-ttu-id="da34c-284">Convierta el archivo de salida Logman especificado por *EtlFile* en un formato de texto legible.</span><span class="sxs-lookup"><span data-stu-id="da34c-284">Convert the Logman output file specified by *EtlFile* into a readable text format.</span></span>

</dd> <dt>

<span data-ttu-id="da34c-285"><span id="-o_OutputFile"></span><span id="-o_outputfile"></span><span id="-O_OUTPUTFILE"></span>**-o** *OutputFile*</span><span class="sxs-lookup"><span data-stu-id="da34c-285"><span id="-o_OutputFile"></span><span id="-o_outputfile"></span><span id="-O_OUTPUTFILE"></span>**-o** *OutputFile*</span></span>
</dt> <dd>

<span data-ttu-id="da34c-286">Guarde la información de seguimiento en el archivo de salida especificado por *OutputFile*.</span><span class="sxs-lookup"><span data-stu-id="da34c-286">Save the tracing information to the output file specified by *OutputFile*.</span></span> <span data-ttu-id="da34c-287">Para obtener el mejor rendimiento, el archivo de salida debe estar ubicado en un volumen que no sea parte de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="da34c-287">For best performance, the output file should be located on a volume that is not part of the shadow copy.</span></span>

</dd> <dt>

<span data-ttu-id="da34c-288"><span id="-help_HelpOption"></span><span id="-help_helpoption"></span><span id="-HELP_HELPOPTION"></span>**-Help** *HelpOption*</span><span class="sxs-lookup"><span data-stu-id="da34c-288"><span id="-help_HelpOption"></span><span id="-help_helpoption"></span><span id="-HELP_HELPOPTION"></span>**-help** *HelpOption*</span></span>
</dt> <dd>

<span data-ttu-id="da34c-289">Muestra la ayuda de la línea de comandos tal y como se especifica en *HelpOption*.</span><span class="sxs-lookup"><span data-stu-id="da34c-289">Display the command-line help as specified by *HelpOption*.</span></span> <span data-ttu-id="da34c-290">Los valores de *HelpOption* válidos son **módulos**, **niveles** y **todos**.</span><span class="sxs-lookup"><span data-stu-id="da34c-290">The valid *HelpOption* values are **modules**, **levels**, and **all**.</span></span> <span data-ttu-id="da34c-291">Al especificar **módulos** , se enumeran los módulos.</span><span class="sxs-lookup"><span data-stu-id="da34c-291">Specifying **modules** causes the modules to be listed.</span></span> <span data-ttu-id="da34c-292">Al especificar **niveles** , se enumeran los niveles disponibles.</span><span class="sxs-lookup"><span data-stu-id="da34c-292">Specifying **levels** causes the available levels to be listed.</span></span> <span data-ttu-id="da34c-293">Si se especifica **All** , se mostrará la ayuda detallada.</span><span class="sxs-lookup"><span data-stu-id="da34c-293">Specifying **all** causes detailed help to be displayed.</span></span> <span data-ttu-id="da34c-294">Si no se usa ninguna opción, se muestra la ayuda concisa.</span><span class="sxs-lookup"><span data-stu-id="da34c-294">If no options are used, concise help is displayed.</span></span>

</dd> </dl>

## <a name="using-logman"></a><span data-ttu-id="da34c-295">Usar Logman</span><span class="sxs-lookup"><span data-stu-id="da34c-295">Using Logman</span></span>

<span data-ttu-id="da34c-296">En el procedimiento siguiente se describe cómo usar Logman con la aplicación VSS.</span><span class="sxs-lookup"><span data-stu-id="da34c-296">The following procedure describes how to use Logman with your VSS application.</span></span>

<span data-ttu-id="da34c-297">**Para usar Logman con la aplicación VSS**</span><span class="sxs-lookup"><span data-stu-id="da34c-297">**To use Logman with your VSS application**</span></span>

1.  <span data-ttu-id="da34c-298">Use el siguiente comando para iniciar el seguimiento:</span><span class="sxs-lookup"><span data-stu-id="da34c-298">Use the following command to start tracing:</span></span>

    <span data-ttu-id="da34c-299">**Logman Start VSS-o** *x: \\ \* \* \* VSS. ETL-ETS-p {9138500e-3648-4edb-aa4c-859e9f7b7c38} 0xfff 170*\*</span><span class="sxs-lookup"><span data-stu-id="da34c-299">**logman start vss -o** *x:\\*\*\*vss.etl -ets -p {9138500e-3648-4edb-aa4c-859e9f7b7c38} 0xfff 170*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="da34c-300">Reemplace "x: \\ " con la ruta de acceso al directorio donde desea que se almacene el archivo de registro de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="da34c-300">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span>

     

2.  <span data-ttu-id="da34c-301">Use el siguiente comando para detener el seguimiento:</span><span class="sxs-lookup"><span data-stu-id="da34c-301">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="da34c-302">**Logman STOP VSS-ETS**</span><span class="sxs-lookup"><span data-stu-id="da34c-302">**logman stop vss -ets**</span></span>

<span data-ttu-id="da34c-303">El archivo de registro de seguimiento es *x: \\* VSS. ETL.</span><span class="sxs-lookup"><span data-stu-id="da34c-303">The trace log file is *x:\\* vss.etl.</span></span>

<span data-ttu-id="da34c-304">Para obtener más información acerca de la herramienta Logman, consulte [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="da34c-304">For more information about the Logman tool, see [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).</span></span>

## <a name="using-tracelog"></a><span data-ttu-id="da34c-305">Usar tracelog</span><span class="sxs-lookup"><span data-stu-id="da34c-305">Using Tracelog</span></span>

<span data-ttu-id="da34c-306">En el procedimiento siguiente se describe cómo usar tracelog.</span><span class="sxs-lookup"><span data-stu-id="da34c-306">The following procedure describes how to use Tracelog.</span></span>

<span data-ttu-id="da34c-307">**Para usar tracelog**</span><span class="sxs-lookup"><span data-stu-id="da34c-307">**To use Tracelog**</span></span>

1.  <span data-ttu-id="da34c-308">Cree un archivo de texto denominado VSS. CTL que contenga solo el siguiente texto:</span><span class="sxs-lookup"><span data-stu-id="da34c-308">Create a text file named vss.ctl that contains only the following text:</span></span>

    <span data-ttu-id="da34c-309">**9138500e-3648-4edb-aa4c-859e9f7b7c38 VSS**</span><span class="sxs-lookup"><span data-stu-id="da34c-309">**9138500e-3648-4edb-aa4c-859e9f7b7c38 vss**</span></span>

2.  <span data-ttu-id="da34c-310">Use el siguiente comando para iniciar el seguimiento:</span><span class="sxs-lookup"><span data-stu-id="da34c-310">Use the following command to start tracing:</span></span>

    <span data-ttu-id="da34c-311">**tracelog-Start VSS-f** *x: \\ \* \* \* VSS. ETL-GUID VSS. CTL: flag de nivel 0xFF-0xAA*\*</span><span class="sxs-lookup"><span data-stu-id="da34c-311">**tracelog -start vss -f** *x:\\*\*\*vss.etl -guid vss.ctl -flag 0xff -level 0xaa*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="da34c-312">Reemplace "x: \\ " con la ruta de acceso al directorio donde desea que se almacene el archivo de registro de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="da34c-312">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span>

     

3.  <span data-ttu-id="da34c-313">Use el siguiente comando para detener el seguimiento:</span><span class="sxs-lookup"><span data-stu-id="da34c-313">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="da34c-314">**tracelog: detener VSS**</span><span class="sxs-lookup"><span data-stu-id="da34c-314">**tracelog -stop vss**</span></span>

<span data-ttu-id="da34c-315">El archivo de registro de seguimiento es *x: \\* VSS. ETL.</span><span class="sxs-lookup"><span data-stu-id="da34c-315">The trace log file is *x:\\* vss.etl.</span></span>

<span data-ttu-id="da34c-316">Para obtener más información acerca de la herramienta tracelog, consulte [tracelog](https://msdn.microsoft.com/library/ms797927.aspx).</span><span class="sxs-lookup"><span data-stu-id="da34c-316">For more information about the Tracelog tool, see [Tracelog](https://msdn.microsoft.com/library/ms797927.aspx).</span></span>

 

 
