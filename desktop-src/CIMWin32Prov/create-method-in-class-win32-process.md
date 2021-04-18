---
description: Crear&\# 8194; El método de clase WMI crea un nuevo proceso.
ms.assetid: be80abec-fab4-4403-bc29-d0d4a38e3c87
ms.tgt_platform: multiple
title: Método Create de la clase Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 42c675f61fc8b42790aeb811ec275554b355a392
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659503"
---
# <a name="create-method-of-the-win32_process-class"></a><span data-ttu-id="beb46-103">Método Create de la \_ clase de proceso Win32</span><span class="sxs-lookup"><span data-stu-id="beb46-103">Create method of the Win32\_Process class</span></span>

<span data-ttu-id="beb46-104">El método **crear** [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) crea un nuevo proceso.</span><span class="sxs-lookup"><span data-stu-id="beb46-104">The **Create** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method creates a new process.</span></span>

<span data-ttu-id="beb46-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="beb46-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="beb46-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="beb46-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="beb46-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="beb46-107">Syntax</span></span>


```mof
uint32 Create(
  [in]  string               CommandLine,
  [in]  string               CurrentDirectory,
  [in]  Win32_ProcessStartup ProcessStartupInformation,
  [out] uint32               ProcessId
);
```



## <a name="parameters"></a><span data-ttu-id="beb46-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="beb46-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="beb46-109">*Línea de comandos* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="beb46-109">*CommandLine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beb46-110">Línea de comandos que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="beb46-110">Command line to execute.</span></span> <span data-ttu-id="beb46-111">El sistema agrega un carácter nulo a la línea de comandos, recortando la cadena si es necesario, para indicar qué archivo se usó realmente.</span><span class="sxs-lookup"><span data-stu-id="beb46-111">The system adds a null character to the command line, trimming the string if necessary, to indicate which file was actually used.</span></span>

</dd> <dt>

<span data-ttu-id="beb46-112">*CurrentDirectory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="beb46-112">*CurrentDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beb46-113">Unidad y directorio actuales para el proceso secundario.</span><span class="sxs-lookup"><span data-stu-id="beb46-113">Current drive and directory for the child process.</span></span> <span data-ttu-id="beb46-114">La cadena requiere que el directorio actual se resuelva en una ruta de acceso conocida.</span><span class="sxs-lookup"><span data-stu-id="beb46-114">The string requires that the current directory resolves to a known path.</span></span> <span data-ttu-id="beb46-115">Un usuario puede especificar una ruta de acceso absoluta o una ruta de acceso relativa al directorio de trabajo actual.</span><span class="sxs-lookup"><span data-stu-id="beb46-115">A user can specify an absolute path or a path relative to the current working directory.</span></span> <span data-ttu-id="beb46-116">Si este parámetro es **null**, el nuevo proceso tendrá la misma ruta de acceso que el proceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="beb46-116">If this parameter is **NULL**, the new process will have the same path as the calling process.</span></span> <span data-ttu-id="beb46-117">Esta opción se proporciona principalmente para los shells que deben iniciar una aplicación y especificar la unidad inicial y el directorio de trabajo de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="beb46-117">This option is provided primarily for shells that must start an application and specify the application's initial drive and working directory.</span></span>

</dd> <dt>

<span data-ttu-id="beb46-118">*ProcessStartupInformation* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="beb46-118">*ProcessStartupInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beb46-119">La configuración de inicio de un proceso de Windows.</span><span class="sxs-lookup"><span data-stu-id="beb46-119">The startup configuration of a Windows process.</span></span> <span data-ttu-id="beb46-120">Para obtener más información, vea [**Win32 \_ ProcessStartup**](win32-processstartup.md).</span><span class="sxs-lookup"><span data-stu-id="beb46-120">For more information, see [**Win32\_ProcessStartup**](win32-processstartup.md).</span></span>

</dd> <dt>

<span data-ttu-id="beb46-121">*ProcessId* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="beb46-121">*ProcessId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="beb46-122">Identificador de proceso global que se puede usar para identificar un proceso.</span><span class="sxs-lookup"><span data-stu-id="beb46-122">Global process identifier that can be used to identify a process.</span></span> <span data-ttu-id="beb46-123">El valor es válido desde el momento en que se crea el proceso hasta la hora de finalización del proceso.</span><span class="sxs-lookup"><span data-stu-id="beb46-123">The value is valid from the time the process is created until the time the process is terminated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="beb46-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="beb46-124">Return value</span></span>

<span data-ttu-id="beb46-125">Devuelve un valor de 0 (cero) si el proceso se ha creado correctamente, y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="beb46-125">Returns a value of 0 (zero) if the process was successfully created, and any other number to indicate an error.</span></span> <span data-ttu-id="beb46-126">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="beb46-126">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="beb46-127">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="beb46-127">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="beb46-128">**Finalización correcta** (0)</span><span class="sxs-lookup"><span data-stu-id="beb46-128">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="beb46-129">**Acceso denegado** (2)</span><span class="sxs-lookup"><span data-stu-id="beb46-129">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="beb46-130">**Privilegios insuficientes** (3)</span><span class="sxs-lookup"><span data-stu-id="beb46-130">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="beb46-131">**Error desconocido** (8)</span><span class="sxs-lookup"><span data-stu-id="beb46-131">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="beb46-132">**No se encontró la ruta de acceso** (9)</span><span class="sxs-lookup"><span data-stu-id="beb46-132">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="beb46-133">**Parámetro no válido** (21)</span><span class="sxs-lookup"><span data-stu-id="beb46-133">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="beb46-134">**Otro** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="beb46-134">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="beb46-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="beb46-135">Remarks</span></span>

<span data-ttu-id="beb46-136">Puede crear una instancia de la clase [**Win32 \_ ProcessStartup**](win32-processstartup.md) para configurar el proceso antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="beb46-136">You can create an instance of the [**Win32\_ProcessStartup**](win32-processstartup.md) class to configure the process before calling this method.</span></span>

<span data-ttu-id="beb46-137">Se debe especificar una ruta de acceso completa en los casos en que el programa que se va a iniciar no está en la ruta de acceso de búsqueda de Winmgmt.exe.</span><span class="sxs-lookup"><span data-stu-id="beb46-137">A fully qualified path must be specified in cases where the program to be launched is not in the search path of Winmgmt.exe.</span></span> <span data-ttu-id="beb46-138">Si el proceso recién creado intenta interactuar con objetos en el sistema de destino sin los privilegios de acceso adecuados, se termina sin notificación a este método.</span><span class="sxs-lookup"><span data-stu-id="beb46-138">If the newly created process attempts to interact with objects on the target system without the appropriate access privileges, it is terminated without notification to this method.</span></span>

<span data-ttu-id="beb46-139">Por motivos de seguridad, el método **\_ Process. Create de Win32** no se puede usar para iniciar un proceso interactivo de forma remota.</span><span class="sxs-lookup"><span data-stu-id="beb46-139">For security reasons the **Win32\_Process.Create** method cannot be used to start an interactive process remotely.</span></span>

<span data-ttu-id="beb46-140">Los procesos creados con el método **\_ Process. Create de Win32** están limitados por el objeto de trabajo a menos que se especifique la marca **crear \_ separación \_ del \_ trabajo** .</span><span class="sxs-lookup"><span data-stu-id="beb46-140">Processes created with the **Win32\_Process.Create** method are limited by the job object unless the **CREATE\_BREAKAWAY\_FROM\_JOB** flag is specified.</span></span> <span data-ttu-id="beb46-141">Para obtener más información, vea [**Win32 \_ ProcessStartup**](win32-processstartup.md) y [**\_ \_ ProviderHostQuotaConfiguration**](/windows/desktop/WmiSdk/--providerhostquotaconfiguration).</span><span class="sxs-lookup"><span data-stu-id="beb46-141">For more information, see [**Win32\_ProcessStartup**](win32-processstartup.md) and [**\_\_ProviderHostQuotaConfiguration**](/windows/desktop/WmiSdk/--providerhostquotaconfiguration).</span></span>

## <a name="examples"></a><span data-ttu-id="beb46-142">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="beb46-142">Examples</span></span>

<span data-ttu-id="beb46-143">En el siguiente ejemplo de VBScript se muestra cómo invocar un método CIM como si fuera un método de automatización de SWbemObject.</span><span class="sxs-lookup"><span data-stu-id="beb46-143">The following VBScript example demonstrates how to invoke a CIM method as if it were an automation method of SWbemObject.</span></span>


```VB
on error resume next

set process = GetObject("winmgmts:Win32_Process")

result = process.Create ("notepad.exe",null,null,processid)

WScript.Echo "Method returned result = " & result
WScript.Echo "Id of new process is " & processid

if err <>0 then
 WScript.Echo Err.Description, "0x" & Hex(Err.Number)
end if
```



<span data-ttu-id="beb46-144">En el siguiente ejemplo de Perl se muestra cómo invocar un método CIM como si fuera un método de automatización de SWbemObject.</span><span class="sxs-lookup"><span data-stu-id="beb46-144">The following Perl example demonstrates how to invoke a CIM method as if it were an automation method of SWbemObject.</span></span>


```VB
use strict;
use Win32::OLE;

my ($process, $outParam, $processid, $inParam, $objMethod);

eval { $process = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2:Win32_Process"); };

if (!$@ && defined $process)
{
 $objMethod = $process->Methods_("Create");

 #Spawn an instance of inParameters and assign the values.
 $inParam = $objMethod->inParameters->SpawnInstance_ if (defined $objMethod);
 $inParam->{CommandLine} = "notepad.exe";
 $inParam->{CurrentDirectory} = undef;
 $inParam->{ProcessStartupInformation} = undef;

 $outParam = $process->ExecMethod_("Create", $inParam) if (defined $inParam);
 if ($outParam->{ReturnValue})
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
 else
 {
  print "Method returned result = $outParam->{ReturnValue}\n";
  print "Id of new process is $outParam->{ProcessId}\n"
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="beb46-145">En el siguiente ejemplo de código de VBScript se crea un proceso de Bloc de notas en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="beb46-145">The following VBScript code example creates a Notepad process on the local computer.</span></span> <span data-ttu-id="beb46-146">[**Win32 \_ ProcessStartup**](win32-processstartup.md) se usa para configurar las opciones del proceso.</span><span class="sxs-lookup"><span data-stu-id="beb46-146">[**Win32\_ProcessStartup**](win32-processstartup.md) is used to configure the process settings.</span></span>


```VB
Const SW_NORMAL = 1
strComputer = "."
strCommand = "Notepad.exe" 
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" _
    & strComputer & "\root\cimv2")

' Configure the Notepad process to show a window
Set objStartup = objWMIService.Get("Win32_ProcessStartup")
Set objConfig = objStartup.SpawnInstance_
objConfig.ShowWindow = SW_NORMAL

' Create Notepad process
Set objProcess = objWMIService.Get("Win32_Process")
intReturn = objProcess.Create _
    (strCommand, Null, objConfig, intProcessID)
If intReturn <> 0 Then
    Wscript.Echo "Process could not be created." & _
        vbNewLine & "Command line: " & strCommand & _
        vbNewLine & "Return value: " & intReturn
Else
    Wscript.Echo "Process created." & _
        vbNewLine & "Command line: " & strCommand & _
        vbNewLine & "Process ID: " & intProcessID
End If
```



## <a name="requirements"></a><span data-ttu-id="beb46-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="beb46-147">Requirements</span></span>



| <span data-ttu-id="beb46-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="beb46-148">Requirement</span></span> | <span data-ttu-id="beb46-149">Value</span><span class="sxs-lookup"><span data-stu-id="beb46-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="beb46-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="beb46-150">Minimum supported client</span></span><br/> | <span data-ttu-id="beb46-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="beb46-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="beb46-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="beb46-152">Minimum supported server</span></span><br/> | <span data-ttu-id="beb46-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="beb46-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="beb46-154">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="beb46-154">Namespace</span></span><br/>                | <span data-ttu-id="beb46-155">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="beb46-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="beb46-156">MOF</span><span class="sxs-lookup"><span data-stu-id="beb46-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="beb46-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="beb46-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="beb46-158">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="beb46-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="beb46-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="beb46-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="beb46-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="beb46-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="beb46-161">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="beb46-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="beb46-162">**\_Proceso Win32**</span><span class="sxs-lookup"><span data-stu-id="beb46-162">**Win32\_Process**</span></span>](win32-process.md)
</dt> <dt>

[<span data-ttu-id="beb46-163">Tareas de WMI: procesos</span><span class="sxs-lookup"><span data-stu-id="beb46-163">WMI Tasks: Processes</span></span>](/windows/desktop/WmiSdk/wmi-tasks--processes)
</dt> </dl>

 

