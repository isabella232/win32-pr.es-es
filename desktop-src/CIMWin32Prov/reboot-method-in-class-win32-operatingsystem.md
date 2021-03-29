---
description: El reinicio&\# 8194; El método de clase WMI cierra el sistema del equipo y, a continuación, lo reinicia.
ms.assetid: 23b70f2a-28ce-4463-9d22-29de52349ab6
ms.tgt_platform: multiple
title: Método de reinicio de la clase Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Reboot
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4577f708d2f7ec7416ab3455da91b4e35fa079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000741"
---
# <a name="reboot-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="75fe3-103">Método de reinicio de la \_ clase Win32 OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="75fe3-103">Reboot method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="75fe3-104">El método **reboot** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) apaga el equipo y, a continuación, lo reinicia.</span><span class="sxs-lookup"><span data-stu-id="75fe3-104">The **Reboot** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method shuts down the computer system, then restarts it.</span></span>

<span data-ttu-id="75fe3-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="75fe3-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="75fe3-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="75fe3-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="75fe3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="75fe3-107">Syntax</span></span>


```mof
uint32 Reboot();
```



## <a name="parameters"></a><span data-ttu-id="75fe3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="75fe3-108">Parameters</span></span>

<span data-ttu-id="75fe3-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="75fe3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="75fe3-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="75fe3-110">Return value</span></span>

<span data-ttu-id="75fe3-111">Devuelve cero (0) para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="75fe3-111">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="75fe3-112">Cualquier otro número indica que hubo un error.</span><span class="sxs-lookup"><span data-stu-id="75fe3-112">Any other number indicates an error.</span></span> <span data-ttu-id="75fe3-113">Para ver los códigos de error, consulte [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="75fe3-113">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="75fe3-114">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="75fe3-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="75fe3-115">**Correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="75fe3-115">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="75fe3-116">**Otro** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="75fe3-116">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="75fe3-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="75fe3-117">Remarks</span></span>

<span data-ttu-id="75fe3-118">La capacidad de reiniciar un equipo mediante programación permite a los administradores realizar muchas tareas de administración de equipos de forma remota.</span><span class="sxs-lookup"><span data-stu-id="75fe3-118">The ability to programmatically restart a computer allows administrators to perform many computer management tasks remotely.</span></span>

<span data-ttu-id="75fe3-119">Por ejemplo, si crea un script para instalar software o realiza un cambio de configuración que requiera el reinicio de un equipo, puede incluir el comando de reinicio en el script y realizar toda la operación de forma remota.</span><span class="sxs-lookup"><span data-stu-id="75fe3-119">For example, if you create a script to install software or make a configuration change that requires restarting a computer, you can include the restart command in the script and perform the entire operation remotely.</span></span> <span data-ttu-id="75fe3-120">El método de **reinicio** se puede usar para reiniciar un equipo.</span><span class="sxs-lookup"><span data-stu-id="75fe3-120">The **Reboot** method can be used to restart a computer.</span></span> <span data-ttu-id="75fe3-121">Al igual que el método [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) , el método de **reinicio** requiere el usuario cuyas credenciales de seguridad usa el script para poseer el privilegio de apagado.</span><span class="sxs-lookup"><span data-stu-id="75fe3-121">Like the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method, the **Reboot** method requires the user whose security credentials are being used by the script to possess the Shutdown privilege.</span></span>

## <a name="examples"></a><span data-ttu-id="75fe3-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="75fe3-122">Examples</span></span>

<span data-ttu-id="75fe3-123">En el siguiente ejemplo de código de VBScript se invoca el método de reinicio de la clase [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) .</span><span class="sxs-lookup"><span data-stu-id="75fe3-123">The following VBScript code sample invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="75fe3-124">Debe tener el privilegio SHUTDOWN para invocar correctamente el método shutdown.</span><span class="sxs-lookup"><span data-stu-id="75fe3-124">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



<span data-ttu-id="75fe3-125">El siguiente código Perl invoca el método de reinicio de la clase [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) .</span><span class="sxs-lookup"><span data-stu-id="75fe3-125">The following Perl code invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="75fe3-126">Debe tener el privilegio SHUTDOWN para invocar correctamente el método shutdown.</span><span class="sxs-lookup"><span data-stu-id="75fe3-126">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```
use Win32::OLE;
use strict;
my $OpSysSet;
eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
 ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if (!$@ && defined $OpSysSet)
{
 close(STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Reboot(); 
  if (!defined $RetVal || $RetVal != 0)
  {
   print Win32::OLE->LastError, "\n"; 
  }
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



<span data-ttu-id="75fe3-127">El siguiente código de VBScript invoca el método de reinicio de la clase [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) en un sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="75fe3-127">The following VBScript invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class on a remote system.</span></span> <span data-ttu-id="75fe3-128">Rellene \_ nombre del sistema remoto \_ con el nombre del sistema remoto que se va a reiniciar.</span><span class="sxs-lookup"><span data-stu-id="75fe3-128">Fill in REMOTE\_SYSTEM\_NAME with the name of the remote system to reboot.</span></span>

> [!Note]  
> <span data-ttu-id="75fe3-129">Debe tener el privilegio RemoteShutdown para invocar correctamente el método de reinicio.</span><span class="sxs-lookup"><span data-stu-id="75fe3-129">You must have the RemoteShutdown privilege to successfully invoke the Reboot method</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Reboot()
next
```



<span data-ttu-id="75fe3-130">el siguiente Perl invoca el método de reinicio de la clase [**Win32 \_ OperatingSystem**](win32-operatingsystem.md) en un sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="75fe3-130">he following Perl invokes the Reboot method of the [**Win32\_OperatingSystem**](win32-operatingsystem.md) class on a remote system.</span></span> <span data-ttu-id="75fe3-131">Rellene \_ nombre del sistema remoto \_ con el nombre del sistema remoto que se va a reiniciar.</span><span class="sxs-lookup"><span data-stu-id="75fe3-131">Fill in REMOTE\_SYSTEM\_NAME with the name of the remote system to reboot.</span></span>

> [!Note]  
> <span data-ttu-id="75fe3-132">Debe tener el privilegio RemoteShutdown para invocar correctamente el método de reinicio.</span><span class="sxs-lookup"><span data-stu-id="75fe3-132">You must have the RemoteShutdown privilege to successfully invoke the Reboot method.</span></span>

 


```
use strict;
use Win32::OLE;

use constant REMOTE_SYSTEM_NAME => "MACHINENAME";
use constant USERNAME => "USER";
use constant PASSWORD => "PASSWORD";
use constant NAMESPACE => "root\\cimv2";
use constant wbemPrivilegeRemoteShutdown => 23;
use constant wbemImpersonationLevelImpersonate => 3;
close(STDERR);
my ($locator, $services, $OpSysSet);
eval {
  $locator = Win32::OLE->new('WbemScripting.SWbemLocator');
  $locator->{Security_}->{impersonationlevel} = wbemImpersonationLevelImpersonate;
  $services = $locator->ConnectServer(REMOTE_SYSTEM_NAME, NAMESPACE, USERNAME, PASSWORD);
  $services->{Security_}->{Privileges}->Add(wbemPrivilegeRemoteShutdown);
  $OpSysSet = $services->ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true");
 };

if (!$@ && defined $OpSysSet)
{
 foreach my $OpSys (in $OpSysSet)
 {
  $OpSys->Reboot();
 }
}
else
{
 print Win32::OLE->LastError, "\n";
 exit(1);
}
```



## <a name="requirements"></a><span data-ttu-id="75fe3-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75fe3-133">Requirements</span></span>



| <span data-ttu-id="75fe3-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="75fe3-134">Requirement</span></span> | <span data-ttu-id="75fe3-135">Value</span><span class="sxs-lookup"><span data-stu-id="75fe3-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75fe3-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75fe3-136">Minimum supported client</span></span><br/> | <span data-ttu-id="75fe3-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75fe3-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="75fe3-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="75fe3-138">Minimum supported server</span></span><br/> | <span data-ttu-id="75fe3-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75fe3-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="75fe3-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="75fe3-140">Namespace</span></span><br/>                | <span data-ttu-id="75fe3-141">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="75fe3-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="75fe3-142">MOF</span><span class="sxs-lookup"><span data-stu-id="75fe3-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75fe3-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="75fe3-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="75fe3-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="75fe3-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75fe3-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75fe3-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75fe3-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="75fe3-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="75fe3-147">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="75fe3-147">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="75fe3-148">**OperatingSystem de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="75fe3-148">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="75fe3-149">**CIM \_ OperatingSystem. Shutdown (método)**</span><span class="sxs-lookup"><span data-stu-id="75fe3-149">**CIM\_OperatingSystem.Shutdown method**</span></span>](shutdown-method-in-class-cim-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="75fe3-150">Tareas WMI: administración de escritorio</span><span class="sxs-lookup"><span data-stu-id="75fe3-150">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> </dl>

 

