---
description: El cierre&\# 8194; El método de clase WMI descarga programas y dll hasta que es seguro apagar el equipo.
ms.assetid: 3f069699-810c-49bc-b77e-3fe43acc3dd5
ms.tgt_platform: multiple
title: Método Shutdown de la clase Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Shutdown
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: af80442087a0498849388f0da10946b08e282712
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496727"
---
# <a name="shutdown-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="54208-103">Método Shutdown de la \_ clase Win32 OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="54208-103">Shutdown method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="54208-104">El método **Shutdown** de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) descarga programas y dll hasta que es seguro apagar el equipo.</span><span class="sxs-lookup"><span data-stu-id="54208-104">The **Shutdown** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method unloads programs and DLLs until it is safe to turn off the computer.</span></span>

<span data-ttu-id="54208-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="54208-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="54208-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="54208-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="54208-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="54208-107">Syntax</span></span>


```mof
uint32 Shutdown();
```



## <a name="parameters"></a><span data-ttu-id="54208-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="54208-108">Parameters</span></span>

<span data-ttu-id="54208-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="54208-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="54208-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="54208-110">Return value</span></span>

<span data-ttu-id="54208-111">Devuelve cero (0) para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="54208-111">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="54208-112">Cualquier otro número indica que hubo un error.</span><span class="sxs-lookup"><span data-stu-id="54208-112">Any other number indicates an error.</span></span> <span data-ttu-id="54208-113">Para ver los códigos de error, consulte [**constantes error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="54208-113">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="54208-114">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="54208-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="54208-115">**Correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="54208-115">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="54208-116">**Otro** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="54208-116">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="54208-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="54208-117">Remarks</span></span>

<span data-ttu-id="54208-118">En ocasiones, los equipos deben quitarse de la red, quizás para realizar tareas de mantenimiento programado, ya que el equipo no funciona correctamente o para completar un proceso de configuración.</span><span class="sxs-lookup"><span data-stu-id="54208-118">Computers occasionally need to be removed from the network, perhaps for scheduled maintenance, because the computer is not functioning correctly, or to complete a configuration process.</span></span> <span data-ttu-id="54208-119">Por ejemplo, si un servidor DHCP está entregando direcciones IP erróneas, es posible que desee apagar el equipo hasta que se pueda enviar un técnico de servicio para solucionar el problema.</span><span class="sxs-lookup"><span data-stu-id="54208-119">For example, if a DHCP server is handing out erroneous IP addresses, you might want to shut the computer down until a service technician can be dispatched to fix the problem.</span></span> <span data-ttu-id="54208-120">Si sospecha que se ha producido una infracción de seguridad, es posible que tenga que apagar determinados servidores para asegurarse de que no se pueda tener acceso a ellos hasta que se resuelva el problema de seguridad.</span><span class="sxs-lookup"><span data-stu-id="54208-120">If you suspect that a security breach has occurred, you might need to shut down certain servers to ensure that they cannot be accessed until the security issue has been resolved.</span></span> <span data-ttu-id="54208-121">Algunas operaciones de configuración (como cambiar el nombre de un equipo) requieren que se reinicie el equipo para que el cambio surta efecto.</span><span class="sxs-lookup"><span data-stu-id="54208-121">Some configuration operations (such as changing a computer name) require you to restart the computer before the change takes effect.</span></span>

<span data-ttu-id="54208-122">Este método apaga inmediatamente el equipo, si es posible.</span><span class="sxs-lookup"><span data-stu-id="54208-122">This method immediately shuts the computer down, if possible.</span></span> <span data-ttu-id="54208-123">El sistema detiene todos los procesos en ejecución, vacía todos los búferes de archivo en el disco y, a continuación, apaga el sistema.</span><span class="sxs-lookup"><span data-stu-id="54208-123">The system stops all running processes, flushes all file buffers to the disk, and then powers down the system.</span></span> <span data-ttu-id="54208-124">El proceso de llamada debe tener el privilegio de **\_ \_ nombre de cierre se** , tal y como se describe en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="54208-124">The calling process must have the **SE\_SHUTDOWN\_NAME** privilege, as described in the following example.</span></span>


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")
```



<span data-ttu-id="54208-125">Para obtener más información sobre cómo establecer un privilegio, vea [ejecutar operaciones con privilegios](/windows/desktop/WmiSdk/executing-privileged-operations) y [ejecutar operaciones con privilegios mediante VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript).</span><span class="sxs-lookup"><span data-stu-id="54208-125">For more information on setting a privilege, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations) and [Executing Privileged Operations Using VBScript](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript).</span></span> <span data-ttu-id="54208-126">Para más opciones de apagado, como un cierre de sesión o un cierre forzado, consulte el método [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) .</span><span class="sxs-lookup"><span data-stu-id="54208-126">For additional shutdown options, such as a logoff or a forced shutdown, see the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="54208-127">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="54208-127">Examples</span></span>

<span data-ttu-id="54208-128">El siguiente código VBScript cierra el equipo local.</span><span class="sxs-lookup"><span data-stu-id="54208-128">The following VBScript code shuts the local computer down.</span></span>

> [!Note]  
> <span data-ttu-id="54208-129">Debe tener el privilegio SHUTDOWN para invocar correctamente el método shutdown.</span><span class="sxs-lookup"><span data-stu-id="54208-129">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Shutdown)}//./root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



<span data-ttu-id="54208-130">El siguiente código Perl cierra el equipo local.</span><span class="sxs-lookup"><span data-stu-id="54208-130">The following Perl code shuts the local computer down.</span></span>

> [!Note]  
> <span data-ttu-id="54208-131">Debe tener el privilegio SHUTDOWN para invocar correctamente el método shutdown.</span><span class="sxs-lookup"><span data-stu-id="54208-131">You must have the Shutdown privilege to successfully invoke the Shutdown method.</span></span>

 


```
use strict;
use Win32::OLE;

my $OpSysSet;

eval { $OpSysSet = Win32::OLE->GetObject("winmgmts:{(Shutdown)}//./root/cimv2")->
      ExecQuery("SELECT * FROM Win32_OperatingSystem WHERE Primary=true"); };

if(!$@ && defined $OpSysSet)
{
 close (STDERR);
 foreach my $OpSys (in $OpSysSet)
 {
  my $RetVal = $OpSys->Shutdown();
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



<span data-ttu-id="54208-132">El siguiente código VBScript cierra el equipo remoto especificado.</span><span class="sxs-lookup"><span data-stu-id="54208-132">The following VBScript code shuts the specified remote computer down.</span></span> <span data-ttu-id="54208-133">Rellene *\_ \_ nombre del sistema remoto* con el nombre del sistema remoto que se va a cerrar.</span><span class="sxs-lookup"><span data-stu-id="54208-133">Fill in *REMOTE\_SYSTEM\_NAME* with the name of the remote system to shutdown.</span></span>

> [!Note]  
> <span data-ttu-id="54208-134">Debe tener el privilegio RemoteShutdown para invocar correctamente el método **Shutdown** .</span><span class="sxs-lookup"><span data-stu-id="54208-134">You must have the RemoteShutdown privilege to successfully invoke the **Shutdown** method.</span></span>

 


```VB
Set OpSysSet = GetObject("winmgmts:{(Debug,RemoteShutdown)}//REMOTE_SYSTEM_NAME/root/cimv2").ExecQuery("select * from Win32_OperatingSystem where Primary=true")

for each OpSys in OpSysSet
 OpSys.Shutdown()
next
```



## <a name="requirements"></a><span data-ttu-id="54208-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54208-135">Requirements</span></span>



| <span data-ttu-id="54208-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="54208-136">Requirement</span></span> | <span data-ttu-id="54208-137">Value</span><span class="sxs-lookup"><span data-stu-id="54208-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54208-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54208-138">Minimum supported client</span></span><br/> | <span data-ttu-id="54208-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54208-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="54208-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54208-140">Minimum supported server</span></span><br/> | <span data-ttu-id="54208-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54208-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="54208-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="54208-142">Namespace</span></span><br/>                | <span data-ttu-id="54208-143">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="54208-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="54208-144">MOF</span><span class="sxs-lookup"><span data-stu-id="54208-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54208-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="54208-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="54208-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="54208-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54208-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54208-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54208-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="54208-148">See also</span></span>

<dl> <dt>

<span data-ttu-id="54208-149">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="54208-149">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="54208-150">**OperatingSystem de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="54208-150">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="54208-151">Tareas WMI: administración de escritorio</span><span class="sxs-lookup"><span data-stu-id="54208-151">WMI Tasks: Desktop Management</span></span>](/windows/desktop/WmiSdk/wmi-tasks--desktop-management)
</dt> <dt>

[<span data-ttu-id="54208-152">Ejecutar operaciones con privilegios mediante VBScript</span><span class="sxs-lookup"><span data-stu-id="54208-152">Executing Privileged Operations Using VBScript</span></span>](/windows/desktop/WmiSdk/executing-privileged-operations-using-vbscript)
</dt> </dl>

 

