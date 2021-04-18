---
description: WinMgmt es el servicio WMI dentro del proceso SVCHOST que se ejecuta en el &\# 0034; LocalSystem&\# 0034; cuenta.
ms.assetid: 3923322a-3acb-407e-8a07-09c59d252e8b
ms.tgt_platform: multiple
title: WinMgmt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- winmgmt
api_type:
- NA
api_location: ''
ms.openlocfilehash: 090fe71edbb00bd7964e5dcc1d518f57179af943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707205"
---
# <a name="winmgmt"></a><span data-ttu-id="dcd2a-103">WinMgmt</span><span class="sxs-lookup"><span data-stu-id="dcd2a-103">winmgmt</span></span>

<span data-ttu-id="dcd2a-104">WinMgmt es el servicio WMI dentro del proceso SVCHOST que se ejecuta con la cuenta "LocalSystem".</span><span class="sxs-lookup"><span data-stu-id="dcd2a-104">Winmgmt is the WMI service within the SVCHOST process running under the "LocalSystem" account.</span></span>

<span data-ttu-id="dcd2a-105">En todos los casos, el servicio WMI se inicia automáticamente cuando la primera aplicación de administración o el script solicita la conexión a un espacio de nombres WMI.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-105">In all cases, the WMI service automatically starts when the first management application or script requests connection to a WMI namespace.</span></span> <span data-ttu-id="dcd2a-106">Para más información, vea [Inicio y detención del servicio WMI](starting-and-stopping-the-wmi-service.md).</span><span class="sxs-lookup"><span data-stu-id="dcd2a-106">For more information, see [Starting and Stopping the WMI Service](starting-and-stopping-the-wmi-service.md).</span></span>

> [!Note]  
> <span data-ttu-id="dcd2a-107">WMI es un componente básico del sistema operativo Windows que permite a los desarrolladores y administradores de ti escribir scripts y aplicaciones para automatizar determinadas tareas.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-107">WMI is a core component of the Windows operating system that allows developers and IT administrators to write scripts and applications to automate certain tasks.</span></span> <span data-ttu-id="dcd2a-108">Winmgmt.exe es el servicio que permite a WMI ejecutarse en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-108">Winmgmt.exe is the service that allows WMI to run on your local computer.</span></span> <span data-ttu-id="dcd2a-109">Para obtener más información sobre el uso de WMI, vea [usar WMI](using-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="dcd2a-109">For more information on using WMI, see [Using WMI](using-wmi.md).</span></span> <span data-ttu-id="dcd2a-110">Si ha recibido un mensaje de error relacionado con winmgmt.exe, consulte [solución de problemas de WMI](wmi-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="dcd2a-110">If you have received an error message regarding winmgmt.exe, see [WMI Troubleshooting](wmi-troubleshooting.md).</span></span> <span data-ttu-id="dcd2a-111">Para obtener más información sobre Winmgmt.exe, consulte [uso de las herramientas de administración de WMI](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="dcd2a-111">For more information on Winmgmt.exe, see [Using WMI Management Tools](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).</span></span>

 

<span data-ttu-id="dcd2a-112">Cuando se ejecuta desde el símbolo del sistema, el servicio WMI tiene los siguientes modificadores.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-112">When run from the command prompt, the WMI service has the following switches.</span></span>

``` syntax
winmgmt 
  [/backup <filename>] 
  [/restore <filename> <mode>] 
  [/resyncperf <winmgmt service process id>] 
  [/standalonehost <level>]
  [/sharedhost]
  [/verifyrepository <path>]
  [/salvagerepository] 
  [/resetrepository]
```

## <a name="switches"></a><span data-ttu-id="dcd2a-113">Conmutadores</span><span class="sxs-lookup"><span data-stu-id="dcd2a-113">Switches</span></span>

<dl> <dt>

<span data-ttu-id="dcd2a-114"><span id="__________backup__filename_________"></span><span id="__________BACKUP__FILENAME_________"></span>\**/backup\*\*\*<filename>*</span><span class="sxs-lookup"><span data-stu-id="dcd2a-114"><span id="__________backup__filename_________"></span><span id="__________BACKUP__FILENAME_________"></span> **/backup** *<filename>*</span></span> 
</dt> <dd>

<span data-ttu-id="dcd2a-115">Hace que WMI realice una copia de seguridad del repositorio en el nombre de archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-115">Causes WMI to back up the repository to the specified file name.</span></span> <span data-ttu-id="dcd2a-116">El argumento *filename* debe contener la ruta de acceso completa a la ubicación del archivo.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-116">The *filename* argument should contain the full path to the file location.</span></span> <span data-ttu-id="dcd2a-117">Este proceso requiere un bloqueo de escritura en el repositorio para que las operaciones de escritura en el repositorio se suspenda hasta que se complete el proceso de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-117">This process requires a write lock on the repository so that write operations to the repository are suspended until the backup process is completed.</span></span>

<span data-ttu-id="dcd2a-118">Si no especifica una ruta de acceso para el archivo, se coloca en el directorio% WINDIR% \\ system32.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-118">If you do not specify a path for the file, it is put in the %Windir%\\System32 directory.</span></span>

</dd> <dt>

<span data-ttu-id="dcd2a-119"><span id="__________restore__filename____flag_____"></span><span id="__________RESTORE__FILENAME____FLAG_____"></span>**/restore** *<filename>\*\*<flag>*</span><span class="sxs-lookup"><span data-stu-id="dcd2a-119"><span id="__________restore__filename____flag_____"></span><span id="__________RESTORE__FILENAME____FLAG_____"></span> **/restore** *<filename>* *<flag>*</span></span> 
</dt> <dd>

<span data-ttu-id="dcd2a-120">Restaura manualmente el repositorio WMI a partir del archivo de copia de seguridad especificado.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-120">Manually restores the WMI repository from the specified backup file.</span></span> <span data-ttu-id="dcd2a-121">El argumento *filename* debe contener la ruta de acceso completa a la ubicación del archivo de copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-121">The *filename* argument should contain the full path to the backup file location.</span></span> <span data-ttu-id="dcd2a-122">Para realizar la operación de restauración, WMI guarda el repositorio existente para que se vuelva a escribir si se produce un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-122">To perform the restore operation, WMI saves the existing repository to write back if the operation fails.</span></span> <span data-ttu-id="dcd2a-123">A continuación, se restaura el repositorio a partir del archivo de copia de seguridad que se especifica en el argumento *filename* .</span><span class="sxs-lookup"><span data-stu-id="dcd2a-123">Then the repository is restored from the backup file that is specified in the *filename* argument.</span></span> <span data-ttu-id="dcd2a-124">Si no se puede obtener acceso exclusivo al repositorio, los clientes existentes se desconectan de WMI.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-124">If exclusive access to the repository cannot be achieved, existing clients are disconnected from WMI.</span></span>

<span data-ttu-id="dcd2a-125">El argumento *Flag* debe ser 1 (forzar la desconexión de usuarios y restauración) o 0 (restauración predeterminada si no hay usuarios conectados) y especifica el modo de restauración.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-125">The *flag* argument must be a 1 (force   disconnect users and restore) or 0 (default   restore if no users connected) and specifies the restore mode.</span></span>

</dd> <dt>

<span data-ttu-id="dcd2a-126"><span id="__________resyncperf__winmgmt-service-process-id_____"></span><span id="__________RESYNCPERF__WINMGMT-SERVICE-PROCESS-ID_____"></span>**/resyncperf** *<WinMgmt-Service-process-ID>*</span><span class="sxs-lookup"><span data-stu-id="dcd2a-126"><span id="__________resyncperf__winmgmt-service-process-id_____"></span><span id="__________RESYNCPERF__WINMGMT-SERVICE-PROCESS-ID_____"></span> **/resyncperf** *<winmgmt-service-process-id>*</span></span> 
</dt> <dd>

<span data-ttu-id="dcd2a-127">Registra las bibliotecas de rendimiento del equipo con WMI.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-127">Registers the computer's performance libraries with WMI.</span></span> <span data-ttu-id="dcd2a-128">El PID de WMI es el identificador de proceso del servicio WMI.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-128">WMI PID is the process ID for the WMI service.</span></span>

<span data-ttu-id="dcd2a-129">Solo es necesario si las clases del monitor de rendimiento no devuelven resultados confiables.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-129">Only needed if the performance monitor classes are not returning reliable results.</span></span>

</dd> <dt>

<span data-ttu-id="dcd2a-130"><span id="_standalonehost__level_"></span><span id="_STANDALONEHOST__LEVEL_"></span>**/standalonehost**\[*<level>*\]</span><span class="sxs-lookup"><span data-stu-id="dcd2a-130"><span id="_standalonehost__level_"></span><span id="_STANDALONEHOST__LEVEL_"></span>**/standalonehost** \[*<level>*\]</span></span>
</dt> <dd>

<span data-ttu-id="dcd2a-131">Mueve el servicio WinMgmt a un proceso svchost independiente que tiene un punto de conexión DCOM fijo.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-131">Moves the Winmgmt service to a standalone Svchost process that has a fixed DCOM endpoint.</span></span> <span data-ttu-id="dcd2a-132">El punto de conexión predeterminado es "ncacn \_ IP \_ TCP. 0.24158".</span><span class="sxs-lookup"><span data-stu-id="dcd2a-132">The default endpoint is "ncacn\_ip\_tcp.0.24158".</span></span> <span data-ttu-id="dcd2a-133">Sin embargo, el punto de conexión se puede cambiar mediante la ejecución de Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-133">However, the endpoint may be changed by running Dcomcnfg.exe.</span></span> <span data-ttu-id="dcd2a-134">Para obtener más información acerca de cómo configurar un puerto fijo para WMI, consulte [configuración de un puerto fijo para WMI](setting-up-a-fixed-port-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="dcd2a-134">For more information about setting up a fixed port for WMI, see [Setting Up a Fixed Port for WMI](setting-up-a-fixed-port-for-wmi.md).</span></span>

<span data-ttu-id="dcd2a-135">El argumento *LEVEL* es el nivel de autenticación del proceso svchost.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-135">The *level* argument is the authentication level for the Svchost process.</span></span> <span data-ttu-id="dcd2a-136">Normalmente, WMI se ejecuta como parte de un host de servicio compartido y no se puede aumentar el nivel de autenticación solo para WMI.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-136">WMI normally runs as part of a shared service host and you cannot increase the authentication level for WMI alone.</span></span> <span data-ttu-id="dcd2a-137">Si no se especifica el *nivel* , el valor predeterminado es 4 (**nivel de autenticación de RPC \_ \_ \_ \_ C** o **WbemAuthenticationLevelPkt**).</span><span class="sxs-lookup"><span data-stu-id="dcd2a-137">If *level* is not specified, the default is 4 (**RPC\_C\_AUTHN\_LEVEL\_PKT** or **WbemAuthenticationLevelPkt**).</span></span>

<span data-ttu-id="dcd2a-138">Puede ejecutar WMI de forma más segura aumentando el nivel de autenticación en privacidad de paquetes **( \_ \_ \_ \_ \_ privacidad de nivel de autenticación de RPC C** o **WbemAuthenticationLevelPktPrivacy**).</span><span class="sxs-lookup"><span data-stu-id="dcd2a-138">You can run WMI more securely by increasing the authentication level to Packet Privacy (**RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** or **WbemAuthenticationLevelPktPrivacy**).</span></span> <span data-ttu-id="dcd2a-139">Los niveles de autenticación para Visual Basic y scripting se describen en [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span><span class="sxs-lookup"><span data-stu-id="dcd2a-139">The authentication levels for Visual Basic and scripting are described in [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span></span> <span data-ttu-id="dcd2a-140">Para C++, vea [establecer el nivel de seguridad de proceso predeterminado mediante c++](setting-the-default-process-security-level-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="dcd2a-140">For C++, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md).</span></span> <span data-ttu-id="dcd2a-141">Para obtener más información, vea [mantener la seguridad de WMI](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="dcd2a-141">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

</dd> <dt>

<span data-ttu-id="dcd2a-142"><span id="_sharedhost"></span><span id="_SHAREDHOST"></span>**/sharedhost**</span><span class="sxs-lookup"><span data-stu-id="dcd2a-142"><span id="_sharedhost"></span><span id="_SHAREDHOST"></span>**/sharedhost**</span></span>
</dt> <dd>

<span data-ttu-id="dcd2a-143">Mueve el servicio WinMgmt al proceso compartido svchost.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-143">Moves the Winmgmt service into the shared Svchost process.</span></span>

</dd> <dt>

<span data-ttu-id="dcd2a-144"><span id="__________verifyrepository__path_____"></span><span id="__________VERIFYREPOSITORY__PATH_____"></span>\**/verifyrepository\*\*\*<path>*</span><span class="sxs-lookup"><span data-stu-id="dcd2a-144"><span id="__________verifyrepository__path_____"></span><span id="__________VERIFYREPOSITORY__PATH_____"></span> **/verifyrepository** *<path>*</span></span> 
</dt> <dd>

<span data-ttu-id="dcd2a-145">Realiza una comprobación de coherencia en el repositorio WMI.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-145">Performs a consistency check on the WMI repository.</span></span> <span data-ttu-id="dcd2a-146">Al agregar el modificador **/verifyrepository** sin el *<path>* argumento, se comprueba el repositorio activo actualmente utilizado por WMI.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-146">When you add the **/verifyrepository** switch without the *<path>* argument, then the live repository currently used by WMI is verified.</span></span> <span data-ttu-id="dcd2a-147">Al especificar el argumento *path* , puede comprobar cualquier copia guardada del repositorio.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-147">When you specify the *path* argument, you can verify any saved copy of the repository.</span></span> <span data-ttu-id="dcd2a-148">En este caso, el argumento de ruta de acceso debe contener la ruta de acceso completa a la copia del repositorio guardada.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-148">In this case, the path argument should contain the full path to the saved repository copy.</span></span> <span data-ttu-id="dcd2a-149">El repositorio guardado debe ser una copia de toda la carpeta del repositorio.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-149">The saved repository should be a copy of the entire repository folder.</span></span> <span data-ttu-id="dcd2a-150">Para obtener más información sobre los errores devueltos por este comando, consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-150">For more information about errors returned by this command, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="dcd2a-151"><span id="_salvagerepository"></span><span id="_SALVAGEREPOSITORY"></span>**/salvagerepository**</span><span class="sxs-lookup"><span data-stu-id="dcd2a-151"><span id="_salvagerepository"></span><span id="_SALVAGEREPOSITORY"></span>**/salvagerepository**</span></span>
</dt> <dd>

<span data-ttu-id="dcd2a-152">Realiza una comprobación de coherencia en el repositorio WMI y, si se detecta una incoherencia, vuelve a generar el repositorio.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-152">Performs a consistency check on the WMI repository, and if an inconsistency is detected, rebuilds the repository.</span></span> <span data-ttu-id="dcd2a-153">El contenido del repositorio incoherente se combina en el repositorio regenerado, si se puede leer.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-153">The content of the inconsistent repository is merged into the rebuilt repository, if it can be read.</span></span> <span data-ttu-id="dcd2a-154">La operación de recuperación siempre funciona con el repositorio que el servicio WMI está usando actualmente.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-154">The salvage operation always works with the repository that the WMI service is currently using.</span></span> <span data-ttu-id="dcd2a-155">Para obtener más información sobre los errores devueltos por este comando, consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-155">For more information about errors returned by this command, see the Remarks section.</span></span>

<span data-ttu-id="dcd2a-156">% Archivos MOF que contienen la instrucción de preprocesador [**\# pragma de Autorrecuperación**](pragma-autorecover.md) se restauran en el repositorio.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-156">% MOF files that contain the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor statement are restored to the repository.</span></span>

</dd> <dt>

<span data-ttu-id="dcd2a-157"><span id="_resetrepository"></span><span id="_RESETREPOSITORY"></span>**/resetrepository**</span><span class="sxs-lookup"><span data-stu-id="dcd2a-157"><span id="_resetrepository"></span><span id="_RESETREPOSITORY"></span>**/resetrepository**</span></span>
</dt> <dd>

<span data-ttu-id="dcd2a-158">El repositorio se restablece al estado inicial cuando se instala el sistema operativo por primera vez.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-158">The repository is reset to the initial state when the operating system is first installed.</span></span> <span data-ttu-id="dcd2a-159">Los archivos MOF que contienen la instrucción [**\# pragma autorecover**](pragma-autorecover.md) preprocessr se restauran en el repositorio.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-159">MOF files that contain the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor statement are restored to the repository.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dcd2a-160">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dcd2a-160">Remarks</span></span>

<span data-ttu-id="dcd2a-161">Esta herramienta se encuentra en el directorio% WINDIR% \\ system32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-161">This tool is located in the %Windir%\\System32\\wbem directory.</span></span> <span data-ttu-id="dcd2a-162">Para obtener una lista de los modificadores disponibles, escriba `WinMgmt /?` en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-162">For a list of the available switches, type `WinMgmt /?` at the command prompt.</span></span>

<span data-ttu-id="dcd2a-163">El repositorio WMI, también conocido como repositorio CIM, no es solo un archivo, sino una colección de archivos dentro de la carpeta del repositorio que funcionan conjuntamente como una base de datos.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-163">The WMI repository, also known as the CIM repository, is not just a single file, but a collection of files within the Repository folder that work together as a database.</span></span> <span data-ttu-id="dcd2a-164">Cuando se usa el modificador **/backup** para realizar una copia de seguridad del repositorio, la copia de seguridad resultante es un único archivo comprimido.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-164">When you use the **/backup** switch to backup the repository, the resulting backup is a single compressed file.</span></span>

<span data-ttu-id="dcd2a-165">WMI devuelve el error Error interno de la **\_ base de \_ BD \_** (net helpmsg 1358) si una operación de comprobación indica que el repositorio no está en un estado coherente.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-165">WMI returns the error **ERROR\_INTERNAL\_DB\_CORRUPTION** (net helpmsg 1358) if a verification operation indicates that the repository is not in a consistent state.</span></span> <span data-ttu-id="dcd2a-166">Este error se puede devolver desde cualquier comando que realice la comprobación del repositorio, como **/verifyrepository** o **/salvagerepository**.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-166">This error can be returned from any command which performs repository verification, such as **/verifyrepository** or **/salvagerepository**.</span></span>

> [!Note]
>
> <span data-ttu-id="dcd2a-167">Si WMI devuelve mensajes de error, tenga en cuenta que es posible que no indiquen problemas en el servicio WMI o en los proveedores WMI.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-167">If WMI returns error messages, be aware that they may not indicate problems in the WMI service or in WMI providers.</span></span> <span data-ttu-id="dcd2a-168">Los errores pueden originarse en otras partes del sistema operativo y surgir como errores a través de WMI.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-168">Failures can originate in other parts of the operating system and emerge as errors through WMI.</span></span> <span data-ttu-id="dcd2a-169">En cualquier circunstancia, no elimine el repositorio WMI como primera acción, ya que la eliminación del repositorio puede provocar daños en el sistema o en las aplicaciones instaladas.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-169">Under any circumstances, do not delete the WMI repository as a first action because deleting the repository can cause damage to the system or to installed applications.</span></span>
>
> <span data-ttu-id="dcd2a-170">Para obtener más información sobre el origen del problema, descargue y ejecute la herramienta de línea de comandos de diagnóstico de [utilidad de diagnóstico de WMI](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) .</span><span class="sxs-lookup"><span data-stu-id="dcd2a-170">For more information about the source of the problem, download and run the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/en/details.aspx?familyid=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d&displaylang=en) diagnostic command line tool.</span></span> <span data-ttu-id="dcd2a-171">Esta herramienta genera un informe que normalmente puede aislar el origen del problema y proporcionar instrucciones sobre cómo corregirlo.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-171">This tool produces a report that can usually isolate the source of the problem and provide instructions on how to fix it.</span></span> <span data-ttu-id="dcd2a-172">El informe también ayuda a los servicios de soporte técnico de Microsoft para ayudarle.</span><span class="sxs-lookup"><span data-stu-id="dcd2a-172">The report also aids Microsoft support services in assisting you.</span></span> <span data-ttu-id="dcd2a-173">Puede descargar el [utilidad de diagnóstico de WMI](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span><span class="sxs-lookup"><span data-stu-id="dcd2a-173">You can download the [WMI Diagnosis Utility](https://www.microsoft.com/downloads/details.aspx?FamilyID=d7ba3cd6-18d1-4d05-b11e-4c64192ae97d).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dcd2a-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcd2a-174">Requirements</span></span>



| <span data-ttu-id="dcd2a-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcd2a-175">Requirement</span></span> | <span data-ttu-id="dcd2a-176">Value</span><span class="sxs-lookup"><span data-stu-id="dcd2a-176">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="dcd2a-177">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dcd2a-177">Minimum supported client</span></span><br/> | <span data-ttu-id="dcd2a-178">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dcd2a-178">Windows Vista</span></span><br/>       |
| <span data-ttu-id="dcd2a-179">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dcd2a-179">Minimum supported server</span></span><br/> | <span data-ttu-id="dcd2a-180">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dcd2a-180">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dcd2a-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="dcd2a-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcd2a-182">Solución de problemas de WMI</span><span class="sxs-lookup"><span data-stu-id="dcd2a-182">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> <dt>

[<span data-ttu-id="dcd2a-183">Conexión a WMI de forma remota a partir de vista</span><span class="sxs-lookup"><span data-stu-id="dcd2a-183">Connecting to WMI Remotely Starting with Vista</span></span>](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> </dl>

 

