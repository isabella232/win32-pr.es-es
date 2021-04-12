---
description: El método Win32ShutdownTracker proporciona el mismo conjunto de opciones de cierre admitido por el método Win32Shutdown en el OperatingSystem de Win32 \_ , pero también permite especificar comentarios, un motivo para el apagado o un tiempo de espera.
ms.assetid: 2c5502c9-9ec0-4f9e-b661-1f8015556008
ms.tgt_platform: multiple
title: Método Win32ShutdownTracker de la clase Win32_OperatingSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystem.Win32ShutdownTracker
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44c86972d014da906b98ad8d3bd8e98d01f1cfcb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152853"
---
# <a name="win32shutdowntracker-method-of-the-win32_operatingsystem-class"></a><span data-ttu-id="678a4-103">Método Win32ShutdownTracker de la \_ clase Win32 OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="678a4-103">Win32ShutdownTracker method of the Win32\_OperatingSystem class</span></span>

<span data-ttu-id="678a4-104">El método **Win32ShutdownTracker** proporciona el mismo conjunto de opciones de cierre admitido por el método [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) en el [**\_ OperatingSystem de Win32**](win32-operatingsystem.md), pero también permite especificar comentarios, un motivo para el apagado o un tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="678a4-104">The **Win32ShutdownTracker** method provides the same set of shutdown options supported by the [**Win32Shutdown**](win32shutdown-method-in-class-win32-operatingsystem.md) method in [**Win32\_OperatingSystem**](win32-operatingsystem.md), but it also allows you to specify comments, a reason for shutdown, or a timeout.</span></span>

## <a name="syntax"></a><span data-ttu-id="678a4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="678a4-105">Syntax</span></span>


```mof
uint32 Win32ShutdownTracker(
  [in] uint32 Timeout,
  [in] string Comment,
  [in] uint32 ReasonCode,
  [in] sint32 Flags
);
```



## <a name="parameters"></a><span data-ttu-id="678a4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="678a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="678a4-107">*Tiempo de espera* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="678a4-107">*Timeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="678a4-108">Tiempo, en segundos, antes de que tenga lugar el apagado.</span><span class="sxs-lookup"><span data-stu-id="678a4-108">Time, in seconds, before shutdown takes place.</span></span> <span data-ttu-id="678a4-109">El valor predeterminado es 0 (cero).</span><span class="sxs-lookup"><span data-stu-id="678a4-109">The default value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="678a4-110">*Comentario* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="678a4-110">*Comment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="678a4-111">Mensaje que se va a mostrar en el cuadro de diálogo de apagado que también se almacena como comentario en la entrada del registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="678a4-111">Message to display in the shutdown dialog box that is also stored as a comment in the event log entry.</span></span>

</dd> <dt>

<span data-ttu-id="678a4-112">*ReasonCode* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="678a4-112">*ReasonCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="678a4-113">Motivo por el que se inicia el apagado.</span><span class="sxs-lookup"><span data-stu-id="678a4-113">Reason for initiating the shutdown.</span></span>

</dd> <dt>

<span data-ttu-id="678a4-114">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="678a4-114">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="678a4-115">Conjunto de mapas Dete de marcas para apagar el equipo.</span><span class="sxs-lookup"><span data-stu-id="678a4-115">Bitmapped set of flags to shut the computer down.</span></span> <span data-ttu-id="678a4-116">Para forzar un comando, agregue la marca Force (4) al valor del comando.</span><span class="sxs-lookup"><span data-stu-id="678a4-116">To force a command, add the Force flag (4) to the command value.</span></span> <span data-ttu-id="678a4-117">Al usar forzar junto con el apagado o el reinicio de un equipo remoto, se cierra inmediatamente todo (incluido WMI, COM, etc.) o se reinicia el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="678a4-117">Using Force in conjunction with Shutdown or Reboot on a remote computer immediately shuts down everything (including WMI, COM, and so on), or reboots the remote computer.</span></span> <span data-ttu-id="678a4-118">Esto da como resultado un valor devuelto indeterminado.</span><span class="sxs-lookup"><span data-stu-id="678a4-118">This results in an indeterminate return value.</span></span>

<dt>

<span data-ttu-id="678a4-119">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="678a4-119">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="678a4-120">Cerrar sesión</span><span class="sxs-lookup"><span data-stu-id="678a4-120">Log Off</span></span>

</dd> <dt>

<span data-ttu-id="678a4-121">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="678a4-121">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="678a4-122">Cierre de sesión forzado (0 + 4)</span><span class="sxs-lookup"><span data-stu-id="678a4-122">Forced Log Off (0 + 4)</span></span>

</dd> <dt>

<span data-ttu-id="678a4-123">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="678a4-123">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="678a4-124">Apagar</span><span class="sxs-lookup"><span data-stu-id="678a4-124">Shutdown</span></span>

</dd> <dt>

<span data-ttu-id="678a4-125">5 (0X5)</span><span class="sxs-lookup"><span data-stu-id="678a4-125">5 (0x5)</span></span>
</dt> <dd>

<span data-ttu-id="678a4-126">Cierre forzado (1 + 4)</span><span class="sxs-lookup"><span data-stu-id="678a4-126">Forced Shutdown (1 + 4)</span></span>

</dd> <dt>

<span data-ttu-id="678a4-127">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="678a4-127">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="678a4-128">Reboot</span><span class="sxs-lookup"><span data-stu-id="678a4-128">Reboot</span></span>

</dd> <dt>

<span data-ttu-id="678a4-129">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="678a4-129">6 (0x6)</span></span>
</dt> <dd>

<span data-ttu-id="678a4-130">Reinicio forzado (2 + 4)</span><span class="sxs-lookup"><span data-stu-id="678a4-130">Forced Reboot (2 + 4)</span></span>

</dd> <dt>

<span data-ttu-id="678a4-131">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="678a4-131">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="678a4-132">Apagar</span><span class="sxs-lookup"><span data-stu-id="678a4-132">Power Off</span></span>

</dd> <dt>

<span data-ttu-id="678a4-133">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="678a4-133">12 (0xC)</span></span>
</dt> <dd>

<span data-ttu-id="678a4-134">Apagado forzado (8 + 4)</span><span class="sxs-lookup"><span data-stu-id="678a4-134">Forced Power Off (8 + 4)</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="678a4-135">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="678a4-135">Return value</span></span>

<span data-ttu-id="678a4-136">Devuelve cero (0) para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="678a4-136">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="678a4-137">Cualquier otro número indica que hubo un error.</span><span class="sxs-lookup"><span data-stu-id="678a4-137">Any other number indicates an error.</span></span> <span data-ttu-id="678a4-138">Para ver los códigos de error, consulte [**constantes error de WMI**](../wmisdk/wmi-error-constants.md) o [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="678a4-138">For error codes, see [**WMI Error Constants**](../wmisdk/wmi-error-constants.md) or [**WbemErrorEnum**](/windows/win32/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="678a4-139">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](../debug/system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="678a4-139">For general **HRESULT** values, see [System Error Codes](../debug/system-error-codes.md).</span></span>

<dl> <dt>

<span data-ttu-id="678a4-140">**Correcto** (0)</span><span class="sxs-lookup"><span data-stu-id="678a4-140">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="678a4-141">**Otro** (1 – 4294967295)</span><span class="sxs-lookup"><span data-stu-id="678a4-141">**Other** (1–4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="678a4-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="678a4-142">Remarks</span></span>

<span data-ttu-id="678a4-143">El proceso de llamada debe tener el privilegio de **\_ \_ nombre de cierre de se** .</span><span class="sxs-lookup"><span data-stu-id="678a4-143">The calling process must have the **SE\_SHUTDOWN\_NAME** privilege.</span></span>

## <a name="examples"></a><span data-ttu-id="678a4-144">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="678a4-144">Examples</span></span>

<span data-ttu-id="678a4-145">En el siguiente ejemplo de código de VBScript se describe cómo llamar a **Win32ShutdownTracker**.</span><span class="sxs-lookup"><span data-stu-id="678a4-145">The following VBScript code sample describes how to call **Win32ShutdownTracker**.</span></span>


```VB
Set objArgs = Wscript.Arguments 

intTimeOut = objArgs(0) 'Countdown time (in seconds) before action
strComment = objArgs(1) 'Message to display
intFlags = objArgs(2) 'Set of flags to shutdown the computer:
'0 = Logoff, 4 = Forced Logoff (0+4), 1 = Shutdown, 2 = Reboot, 6 = Forced Reboot (2+4), 8 = Power Off, 12 = Forced Power Off (8+4) - 2 (Reboot) 

strComputer = "." 

Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate,(Shutdown)}!\\" & strComputer & "\root\cimv2")

Set colOperatingSystems = objWMIService.ExecQuery ("Select * from Win32_OperatingSystem") 

For Each objOperatingSystem in colOperatingSystems 
objOperatingSystem.Win32ShutdownTracker intTimeOut,strComment,0,intFlags 
Next
```



## <a name="requirements"></a><span data-ttu-id="678a4-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="678a4-146">Requirements</span></span>



| <span data-ttu-id="678a4-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="678a4-147">Requirement</span></span> | <span data-ttu-id="678a4-148">Value</span><span class="sxs-lookup"><span data-stu-id="678a4-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="678a4-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="678a4-149">Minimum supported client</span></span><br/> | <span data-ttu-id="678a4-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="678a4-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="678a4-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="678a4-151">Minimum supported server</span></span><br/> | <span data-ttu-id="678a4-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="678a4-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="678a4-153">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="678a4-153">Namespace</span></span><br/>                | <span data-ttu-id="678a4-154">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="678a4-154">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="678a4-155">MOF</span><span class="sxs-lookup"><span data-stu-id="678a4-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="678a4-156"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="678a4-156"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="678a4-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="678a4-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="678a4-158"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="678a4-158"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="678a4-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="678a4-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="678a4-160">Clases de sistema operativo</span><span class="sxs-lookup"><span data-stu-id="678a4-160">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> <dt>

[<span data-ttu-id="678a4-161">**OperatingSystem de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="678a4-161">**Win32\_OperatingSystem**</span></span>](win32-operatingsystem.md)
</dt> <dt>

[<span data-ttu-id="678a4-162">**Win32Shutdown**</span><span class="sxs-lookup"><span data-stu-id="678a4-162">**Win32Shutdown**</span></span>](win32shutdown-method-in-class-win32-operatingsystem.md)
</dt> </dl>

 

 
