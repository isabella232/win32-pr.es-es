---
description: Win32Shutdown &\# 8194; El método de clase WMI proporciona el conjunto completo de opciones de apagado compatibles con los sistemas operativos Win32. Entre ellas se incluyen cerrar sesión, apagar, reiniciar y forzar el cierre de sesión, el apagado o el reinicio.
ms.assetid: 7108570a-81ba-46d5-8b05-de6194f93f18
ms.tgt_platform: multiple
title: Método Win32Shutdown de la clase Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f2cca60c376859438b40ca35be26a99b115634c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907451"
---
# <a name="win32shutdown-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="78c8b-104">Método Win32Shutdown de la \_ clase Win32 OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="78c8b-104">Win32Shutdown method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="78c8b-105">El método de   [clase WMI](../wmisdk/retrieving-a-class.md) **Win32Shutdown** proporciona el conjunto completo de opciones de apagado compatibles con los sistemas operativos Win32.</span><span class="sxs-lookup"><span data-stu-id="78c8b-105">The **Win32Shutdown**   [WMI class](../wmisdk/retrieving-a-class.md) method provides the full set of shutdown options supported by Win32 operating systems.</span></span> <span data-ttu-id="78c8b-106">Entre ellas se incluyen cerrar sesión, apagar, reiniciar y forzar el cierre de sesión, el apagado o el reinicio.</span><span class="sxs-lookup"><span data-stu-id="78c8b-106">These include logoff, shutdown, reboot, and forcing a logoff, shutdown, or reboot.</span></span>

<span data-ttu-id="78c8b-107">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="78c8b-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="78c8b-108">Para obtener más información sobre el uso de este método, consulte [llamar a un método](../wmisdk/calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="78c8b-108">For more information about using this method, see [Calling a Method](../wmisdk/calling-a-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="78c8b-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78c8b-109">Syntax</span></span>


```mof
uint32 Win32Shutdown(
  [in] sint32 Flags,
  [in] sint32 Reserved = 
);
```



## <a name="parameters"></a><span data-ttu-id="78c8b-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="78c8b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78c8b-111">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="78c8b-111">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78c8b-112">Conjunto de mapas Dete de marcas para apagar el equipo.</span><span class="sxs-lookup"><span data-stu-id="78c8b-112">Bitmapped set of flags to shut the computer down.</span></span> <span data-ttu-id="78c8b-113">Para forzar un comando, agregue la marca Force (4) al valor del comando.</span><span class="sxs-lookup"><span data-stu-id="78c8b-113">To force a command, add the Force flag (4) to the command value.</span></span> <span data-ttu-id="78c8b-114">Al usar forzar junto con el apagado o el reinicio de un equipo remoto, se cierra inmediatamente todo (incluido WMI, COM, etc.) o se reinicia el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="78c8b-114">Using Force in conjunction with Shutdown or Reboot on a remote computer immediately shuts down everything (including WMI, COM, and so on), or reboots the remote computer.</span></span> <span data-ttu-id="78c8b-115">Esto da como resultado un valor devuelto indeterminado.</span><span class="sxs-lookup"><span data-stu-id="78c8b-115">This results in an indeterminate return value.</span></span>

<dt>

<span data-ttu-id="78c8b-116">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="78c8b-116">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="78c8b-117">**Cerrar sesión** : cierra la sesión del usuario en el equipo.</span><span class="sxs-lookup"><span data-stu-id="78c8b-117">**Log Off** - Logs the user off the computer.</span></span> <span data-ttu-id="78c8b-118">El cierre de sesión detiene todos los procesos asociados con el contexto de seguridad del proceso que llamó a la función Exit, registra el usuario actual en el sistema y muestra el cuadro de diálogo logon.</span><span class="sxs-lookup"><span data-stu-id="78c8b-118">Logging off stops all processes associated with the security context of the process that called the exit function, logs the current user off the system, and displays the logon dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="78c8b-119">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="78c8b-119">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="78c8b-120">Cierre de **sesión forzado (0 + 4)** : cierra el usuario del equipo inmediatamente y no notifica a las aplicaciones que la sesión de inicio de sesión está finalizando.</span><span class="sxs-lookup"><span data-stu-id="78c8b-120">**Forced Log Off (0 + 4)** - Logs the user off the computer immediately and does not notify applications that the logon session is ending.</span></span> <span data-ttu-id="78c8b-121">Esto puede dar lugar a una pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="78c8b-121">This can result in a loss of data.</span></span>

</dd> <dt>

<span data-ttu-id="78c8b-122">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="78c8b-122">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="78c8b-123">**Apagado** : apaga el equipo hasta un punto en el que es seguro apagar la alimentación.</span><span class="sxs-lookup"><span data-stu-id="78c8b-123">**Shutdown** - Shuts down the computer to a point where it is safe to turn off the power.</span></span> <span data-ttu-id="78c8b-124">(Todos los búferes de archivos se vacían en el disco y se detienen todos los procesos en ejecución). Los usuarios ven el mensaje `It is now safe to turn off your computer.`</span><span class="sxs-lookup"><span data-stu-id="78c8b-124">(All file buffers are flushed to disk, and all running processes are stopped.) Users see the message, `It is now safe to turn off your computer.`</span></span>

<span data-ttu-id="78c8b-125">Durante el apagado, el sistema envía un mensaje a cada aplicación en ejecución.</span><span class="sxs-lookup"><span data-stu-id="78c8b-125">During shutdown the system sends a message to each running application.</span></span> <span data-ttu-id="78c8b-126">Las aplicaciones realizan cualquier limpieza mientras procesan el mensaje y devuelven TRUE para indicar que se pueden terminar.</span><span class="sxs-lookup"><span data-stu-id="78c8b-126">The applications perform any cleanup while processing the message and return True to indicate that they can be terminated.</span></span>

</dd> <dt>

<span data-ttu-id="78c8b-127">5 (0X5)</span><span class="sxs-lookup"><span data-stu-id="78c8b-127">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="78c8b-128">**Cierre forzado (1 + 4)** : apaga el equipo hasta un punto en el que es seguro apagar la alimentación.</span><span class="sxs-lookup"><span data-stu-id="78c8b-128">**Forced Shutdown (1 + 4)** - Shuts down the computer to a point where it is safe to turn off the power.</span></span> <span data-ttu-id="78c8b-129">(Todos los búferes de archivos se vacían en el disco y se detienen todos los procesos en ejecución). Los usuarios ven el mensaje` It is now safe to turn off your computer.`</span><span class="sxs-lookup"><span data-stu-id="78c8b-129">(All file buffers are flushed to disk, and all running processes are stopped.) Users see the message,` It is now safe to turn off your computer.`</span></span>

<span data-ttu-id="78c8b-130">Cuando se usa el enfoque de cierre forzado, todos los servicios, incluido WMI, se apagan inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="78c8b-130">When the forced shutdown approach is used, all services, including WMI, are shut down immediately.</span></span> <span data-ttu-id="78c8b-131">Por este motivo, no podrá recibir un valor devuelto si está ejecutando el script en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="78c8b-131">Because of this, you will not be able to receive a return value if you are running the script against a remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="78c8b-132">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="78c8b-132">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="78c8b-133">**Reiniciar** : cierra y reinicia el equipo.</span><span class="sxs-lookup"><span data-stu-id="78c8b-133">**Reboot** - Shuts down and then restarts the computer.</span></span>

</dd> <dt>

<span data-ttu-id="78c8b-134">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="78c8b-134">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="78c8b-135">**Reinicio forzado (2 + 4)** : cierra y reinicia el equipo.</span><span class="sxs-lookup"><span data-stu-id="78c8b-135">**Forced Reboot (2 + 4)** - Shuts down and then restarts the computer.</span></span>

<span data-ttu-id="78c8b-136">Cuando se utiliza el enfoque de reinicio forzado, todos los servicios, incluido WMI, se apagan inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="78c8b-136">When the forced reboot approach is used, all services, including WMI, are shut down immediately.</span></span> <span data-ttu-id="78c8b-137">Por este motivo, no podrá recibir un valor devuelto si está ejecutando el script en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="78c8b-137">Because of this, you will not be able to receive a return value if you are running the script against a remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="78c8b-138">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="78c8b-138">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="78c8b-139">**Apaga el** equipo y apaga la alimentación (si es compatible con el equipo en cuestión).</span><span class="sxs-lookup"><span data-stu-id="78c8b-139">**Power Off** - Shuts down the computer and turns off the power (if supported by the computer in question).</span></span>

</dd> <dt>

<span data-ttu-id="78c8b-140">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="78c8b-140">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="78c8b-141">**Apagado forzado (8 + 4)** : apaga el equipo y apaga la alimentación (si es compatible con el equipo en cuestión).</span><span class="sxs-lookup"><span data-stu-id="78c8b-141">**Forced Power Off (8 + 4)** - Shuts down the computer and turns off the power (if supported by the computer in question).</span></span>

<span data-ttu-id="78c8b-142">Cuando se usa el enfoque de apagado forzado, todos los servicios, incluido WMI, se apagan inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="78c8b-142">When the forced power off approach is used, all services, including WMI, are shut down immediately.</span></span> <span data-ttu-id="78c8b-143">Por este motivo, no podrá recibir un valor devuelto si está ejecutando el script en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="78c8b-143">Because of this, you will not be able to receive a return value if you are running the script against a remote computer.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="78c8b-144">*Reservado* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="78c8b-144">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78c8b-145">Un medio para extender **Win32Shutdown**.</span><span class="sxs-lookup"><span data-stu-id="78c8b-145">A means to extend **Win32Shutdown**.</span></span> <span data-ttu-id="78c8b-146">Actualmente, se omite el parámetro *Reserved* .</span><span class="sxs-lookup"><span data-stu-id="78c8b-146">Currently, the *Reserved* parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78c8b-147">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="78c8b-147">Return value</span></span>

<span data-ttu-id="78c8b-148">Devuelve cero (0) para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="78c8b-148">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="78c8b-149">Cualquier otro número indica que hubo un error.</span><span class="sxs-lookup"><span data-stu-id="78c8b-149">Any other number indicates an error.</span></span> <span data-ttu-id="78c8b-150">Para ver los códigos de error, consulte [**constantes error de WMI**](../wmisdk/wmi-error-constants.md) o [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="78c8b-150">For error codes, see [**WMI Error Constants**](../wmisdk/wmi-error-constants.md) or [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="78c8b-151">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](../debug/system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="78c8b-151">For general **HRESULT** values, see [System Error Codes](../debug/system-error-codes.md).</span></span>

<dl> <dt>

<span data-ttu-id="78c8b-152">**Correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="78c8b-152">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="78c8b-153">**Otro** (1 – 4294967295)</span><span class="sxs-lookup"><span data-stu-id="78c8b-153">**Other** (1–4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="78c8b-154">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78c8b-154">Remarks</span></span>

<span data-ttu-id="78c8b-155">Para una administración más eficaz de los equipos de una organización, los administradores necesitan la capacidad de apagar o reiniciar un equipo de forma remota o de cerrar la sesión de un usuario de forma remota.</span><span class="sxs-lookup"><span data-stu-id="78c8b-155">For more efficient management of computers in an organization, administrators need the ability to remotely shut down or restart a computer, or to remotely log off a user.</span></span> <span data-ttu-id="78c8b-156">La capacidad de llevar a cabo estas tareas permite a los administradores instalar software, volver a configurar el equipo, quitar equipos de la red y realizar otras tareas sin tener que apagar o reiniciar manualmente cada equipo.</span><span class="sxs-lookup"><span data-stu-id="78c8b-156">The ability to carry out these tasks allows administrators to install software, reconfigure computer settings, remove computers from the network, and perform other tasks without having to manually shut down or restart each computer.</span></span>

<span data-ttu-id="78c8b-157">Por ejemplo, para realizar una actualización de red, es posible que tenga que apagar todos los equipos que se ejecutan en un segmento de red determinado.</span><span class="sxs-lookup"><span data-stu-id="78c8b-157">For example, to perform a network upgrade, you might need to shut down all the computers running on a particular network segment.</span></span> <span data-ttu-id="78c8b-158">Para forzar una actualización de directiva de grupo, debe cerrar la sesión de los usuarios en sus equipos.</span><span class="sxs-lookup"><span data-stu-id="78c8b-158">To force a Group Policy upgrade, you need to log users off their computers.</span></span> <span data-ttu-id="78c8b-159">Si un virus informático está presente en cualquier parte de su organización, es posible que desee apagar tantos equipos como sea posible, antes de que el virus tenga la oportunidad de propagarse.</span><span class="sxs-lookup"><span data-stu-id="78c8b-159">If a computer virus is present anywhere in your organization, you might want to shut down as many computers as possible, before the virus has an opportunity to spread.</span></span> <span data-ttu-id="78c8b-160">La capacidad de apagar y reiniciar los equipos y de cerrar la sesión de los usuarios mediante programación en lugar de hacerlo manualmente puede ser un ahorro de tiempo enorme.</span><span class="sxs-lookup"><span data-stu-id="78c8b-160">The ability to shut down and restart computers and to log off users programmatically instead of manually can be an enormous time-saver.</span></span>

<span data-ttu-id="78c8b-161">El proceso de llamada debe tener el privilegio de **\_ \_ nombre de cierre de se** .</span><span class="sxs-lookup"><span data-stu-id="78c8b-161">The calling process must have the **SE\_SHUTDOWN\_NAME** privilege.</span></span>

<span data-ttu-id="78c8b-162">El método [**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) proporciona el mismo conjunto de opciones de cierre admitido por el método **Win32Shutdown** en el [**\_ OperatingSystem de Win32**](win32-operatingsystem.md) , pero también permite especificar comentarios, un motivo para el apagado o un tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="78c8b-162">The [**Win32ShutdownTracker**](win32shutdowntracker-method-in-class-win32-operatingsystem.md) method provides the same set of shutdown options supported by the **Win32Shutdown** method in [**Win32\_OperatingSystem**](win32-operatingsystem.md) but it also allows you to specify comments, a reason for shutdown, or a timeout.</span></span>

<span data-ttu-id="78c8b-163">El método Win32Shutdown no tiene un parámetro para bloquear una estación de trabajo, lo que hace que el usuario inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="78c8b-163">The Win32Shutdown method does not have a parameter for locking a workstation, leaving the user logged on.</span></span> <span data-ttu-id="78c8b-164">Sin embargo, las estaciones de trabajo se pueden bloquear desde la línea de comandos mediante el comando siguiente:</span><span class="sxs-lookup"><span data-stu-id="78c8b-164">However, workstations can be locked from the command line by using the following command:</span></span>

`% windir %\System32\rundll32.exe user32.dll,LockWorkStation`

## <a name="examples"></a><span data-ttu-id="78c8b-165">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="78c8b-165">Examples</span></span>

<span data-ttu-id="78c8b-166">En el ejemplo de VBScript [Cerrar sesión, reiniciar o apagar varios equipos](https://Gallery.TechNet.Microsoft.Com/2e88d504-a4e5-499b-b09a-f90617a6d87d) de la galería de TechNet se usa Win32Shutdown para cerrar la sesión, apagar, reiniciar o desconectar (dependiendo de la selección) los equipos que aparecen en la matriz de servidores.</span><span class="sxs-lookup"><span data-stu-id="78c8b-166">The [Log Out, Reboot, or Shut Down Multiple Computers](https://Gallery.TechNet.Microsoft.Com/2e88d504-a4e5-499b-b09a-f90617a6d87d) VBScript sample on TechNet Gallery uses Win32Shutdown to log off, shut down, reboot, or power off (depending on the selection) the computers listed in the Server array.</span></span>

<span data-ttu-id="78c8b-167">El ejemplo de [ComputerManagement.ps1](https://Gallery.TechNet.Microsoft.Com/ef8de213-45b6-4751-8c77-01d1b6623e16) PowerShell en la galería de TechNet incluye un método que llama a Win32Shutdown en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="78c8b-167">The [ComputerManagement.ps1](https://Gallery.TechNet.Microsoft.Com/ef8de213-45b6-4751-8c77-01d1b6623e16) PowerShell sample on TechNet Gallery includes a method that calls Win32Shutdown on a remote computer.</span></span>

<span data-ttu-id="78c8b-168">En el siguiente ejemplo de PowerShell se usa el método Win32Shutdown para apagar el equipo especificado.</span><span class="sxs-lookup"><span data-stu-id="78c8b-168">The following PowerShell example uses the Win32Shutdown method to shut down the specified computer.</span></span>


```PowerShell
$computername= "."
$win32OS = get-wmiobject win32_operatingsystem -computername $computername
$win32OS.psbase.Scope.Options.EnablePrivileges = $true
$win32OS.win32shutdown(8)
```



<span data-ttu-id="78c8b-169">En el siguiente ejemplo de código de PowerShell se usa el cmdlet EnableAllPrivileges desde Get-WMIObject para obtener los privilegios adecuados.</span><span class="sxs-lookup"><span data-stu-id="78c8b-169">The following PowerShell code sample uses the EnableAllPrivileges from get-wmiobject cmdlet to achieve the proper priviliges.</span></span>


```PowerShell
$win32OS = get-wmiobject win32_operatingsystem -computername $computername -EnableAllPrivileges
$win32OS.win32shutdown(8)
```



<span data-ttu-id="78c8b-170">El siguiente código de ejemplo de VB.NET usa el método shutdown para reiniciar o cerrar la sesión de un sistema.</span><span class="sxs-lookup"><span data-stu-id="78c8b-170">The following VB.NET sample code uses the Shutdown method to reboot or log off a system.</span></span>


```VB
Dim

testResult AsSingle

Dim WMIServiceObject, ComputerObject AsObject 

'Now get some privileges 

WMIServiceObject = GetObject(
"Winmgmts:{impersonationLevel=impersonate,(Debug,Shutdown)}")
ForEach ComputerObject In WMIServiceObject.InstancesOf("Win32_OperatingSystem") 
    testResult = ComputerObject.Win32Shutdown(2 + 4, 0) 
    'reboot
    'testResult = ComputerObject.Win32Shutdown(0, 0) 'logoff 
    ' testResult = ComputerObject.Win32Shutdown(8 + 4, 0) 'shutdown 

If testResult <> 0 Then 

MsgBox("Sorry, an error has occurred while trying to perform selected operation") 

Else 

'Operation selected in statement above if condition would be carried out 

EndIf 

Next
```



## <a name="requirements"></a><span data-ttu-id="78c8b-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78c8b-171">Requirements</span></span>



| <span data-ttu-id="78c8b-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="78c8b-172">Requirement</span></span> | <span data-ttu-id="78c8b-173">Value</span><span class="sxs-lookup"><span data-stu-id="78c8b-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="78c8b-174">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78c8b-174">Minimum supported client</span></span><br/> | <span data-ttu-id="78c8b-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78c8b-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="78c8b-176">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78c8b-176">Minimum supported server</span></span><br/> | <span data-ttu-id="78c8b-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78c8b-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="78c8b-178">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="78c8b-178">Namespace</span></span><br/>                | <span data-ttu-id="78c8b-179">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="78c8b-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="78c8b-180">MOF</span><span class="sxs-lookup"><span data-stu-id="78c8b-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78c8b-181"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="78c8b-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="78c8b-182">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="78c8b-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78c8b-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78c8b-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78c8b-184">Vea también</span><span class="sxs-lookup"><span data-stu-id="78c8b-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78c8b-185">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="78c8b-185">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="78c8b-186">**OperatingSystem de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="78c8b-186">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="78c8b-187">**Win32ShutdownTracker**</span><span class="sxs-lookup"><span data-stu-id="78c8b-187">**Win32ShutdownTracker**</span></span>](win32shutdowntracker-method-in-class-win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="78c8b-188">Tareas WMI: administración de escritorio</span><span class="sxs-lookup"><span data-stu-id="78c8b-188">WMI Tasks: Desktop Management</span></span>](../wmisdk/wmi-tasks--desktop-management.md)
</dt> <dt>

[<span data-ttu-id="78c8b-189">Ejecutar operaciones con privilegios mediante VBScript</span><span class="sxs-lookup"><span data-stu-id="78c8b-189">Executing Privileged Operations Using VBScript</span></span>](../wmisdk/executing-privileged-operations-using-vbscript.md)
</dt> </dl>

 

 
