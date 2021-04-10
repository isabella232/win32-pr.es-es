---
description: GetOwner&\# 8194; El método de clase WMI recupera el nombre de usuario y el nombre de dominio en el que se está ejecutando el proceso.
ms.assetid: bbd6d22b-ca54-42f3-8098-d3034048ec4d
ms.tgt_platform: multiple
title: Método GetOwner de la clase Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.GetOwner
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 007acbe997f555e9a439ed27740a447d3bf7fe4d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152990"
---
# <a name="getowner-method-of-the-win32_process-class"></a><span data-ttu-id="820a9-103">Método GetOwner de la \_ clase Process de Win32</span><span class="sxs-lookup"><span data-stu-id="820a9-103">GetOwner method of the Win32\_Process class</span></span>

<span data-ttu-id="820a9-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **GetOwner** recupera el nombre de usuario y el nombre de dominio en el que se está ejecutando el proceso.</span><span class="sxs-lookup"><span data-stu-id="820a9-104">The **GetOwner** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method retrieves the user name and domain name under which the process is running.</span></span>

<span data-ttu-id="820a9-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="820a9-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="820a9-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="820a9-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="820a9-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="820a9-107">Syntax</span></span>


```mof
uint32 GetOwner(
  [out] string User,
  [out] string Domain
);
```



## <a name="parameters"></a><span data-ttu-id="820a9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="820a9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="820a9-109">*Usuario* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="820a9-109">*User* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="820a9-110">Devuelve el nombre de usuario del propietario de este proceso.</span><span class="sxs-lookup"><span data-stu-id="820a9-110">Returns the user name of the owner of this process.</span></span>

</dd> <dt>

<span data-ttu-id="820a9-111">*Dominio* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="820a9-111">*Domain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="820a9-112">Devuelve el nombre de dominio en el que se ejecuta este proceso.</span><span class="sxs-lookup"><span data-stu-id="820a9-112">Returns the domain name under which this process is running.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="820a9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="820a9-113">Return value</span></span>

<span data-ttu-id="820a9-114">Devuelve cero (0) para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="820a9-114">Returns zero (0) to indicate success.</span></span> <span data-ttu-id="820a9-115">Cualquier otro número indica que hubo un error.</span><span class="sxs-lookup"><span data-stu-id="820a9-115">Any other number indicates an error.</span></span> <span data-ttu-id="820a9-116">Para ver otros códigos de error, consulte [**constantes de error de WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="820a9-116">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="820a9-117">Para obtener valores de **HRESULT** generales, vea [códigos de error del sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="820a9-117">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="820a9-118">**Finalización correcta** (0)</span><span class="sxs-lookup"><span data-stu-id="820a9-118">**Successful completion** (0)</span></span>
</dt> <dt>

<span data-ttu-id="820a9-119">**Acceso denegado** (2)</span><span class="sxs-lookup"><span data-stu-id="820a9-119">**Access denied** (2)</span></span>
</dt> <dt>

<span data-ttu-id="820a9-120">**Privilegios insuficientes** (3)</span><span class="sxs-lookup"><span data-stu-id="820a9-120">**Insufficient privilege** (3)</span></span>
</dt> <dt>

<span data-ttu-id="820a9-121">**Error desconocido** (8)</span><span class="sxs-lookup"><span data-stu-id="820a9-121">**Unknown failure** (8)</span></span>
</dt> <dt>

<span data-ttu-id="820a9-122">**No se encontró la ruta de acceso** (9)</span><span class="sxs-lookup"><span data-stu-id="820a9-122">**Path not found** (9)</span></span>
</dt> <dt>

<span data-ttu-id="820a9-123">**Parámetro no válido** (21)</span><span class="sxs-lookup"><span data-stu-id="820a9-123">**Invalid parameter** (21)</span></span>
</dt> <dt>

<span data-ttu-id="820a9-124">**Otro** (22 4294967295)</span><span class="sxs-lookup"><span data-stu-id="820a9-124">**Other** (22 4294967295)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="820a9-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="820a9-125">Examples</span></span>

<span data-ttu-id="820a9-126">[El proceso de supervisión de PCT de CPU por nombre con propietario](https://Gallery.TechNet.Microsoft.Com/Monitor-Process-CPU-Pct-by-0f3a5a1c) El ejemplo de VBScript recopila el porcentaje de uso del procesador o la CPU y busca el propietario del proceso.</span><span class="sxs-lookup"><span data-stu-id="820a9-126">[The Monitor Process CPU Pct by Name with Owner](https://Gallery.TechNet.Microsoft.Com/Monitor-Process-CPU-Pct-by-0f3a5a1c) VBScript sample collects the CPU or Processor utilization percent and looks up the process owner.</span></span>

<span data-ttu-id="820a9-127">En el ejemplo [obtener todos los servidores en los que se ha iniciado sesión una lista de usuarios en PowerShell se](https://Gallery.TechNet.Microsoft.Com/Get-all-servers-that-a-aecc07ef) consulta WMI para el propietario de todos los procesos de explorer.exe.</span><span class="sxs-lookup"><span data-stu-id="820a9-127">The [Get all servers that a list of users is logged onto](https://Gallery.TechNet.Microsoft.Com/Get-all-servers-that-a-aecc07ef) PowerShell sample querys WMI for the owner of all explorer.exe processes.</span></span>

<span data-ttu-id="820a9-128">El siguiente ejemplo de código VBScript obtiene el propietario de cada proceso en ejecución.</span><span class="sxs-lookup"><span data-stu-id="820a9-128">The following VBScript code example obtains the owner for each running process.</span></span>


```VB
strComputer = "."
Set colProcesses = GetObject("winmgmts:" & _
   "{impersonationLevel=impersonate}!\\" & strComputer & _
   "\root\cimv2").ExecQuery("Select * from Win32_Process")

For Each objProcess in colProcesses

    Return = objProcess.GetOwner(strNameOfUser)
    If Return <> 0 Then
        Wscript.Echo "Could not get owner info for process " & _  
            objProcess.Name & VBNewLine _
            & "Error = " & Return
    Else 
        Wscript.Echo "Process " _
            & objProcess.Name & " is owned by " _ 
            & "\" & strNameOfUser & "."
    End If
Next
```



## <a name="requirements"></a><span data-ttu-id="820a9-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="820a9-129">Requirements</span></span>



| <span data-ttu-id="820a9-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="820a9-130">Requirement</span></span> | <span data-ttu-id="820a9-131">Value</span><span class="sxs-lookup"><span data-stu-id="820a9-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="820a9-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="820a9-132">Minimum supported client</span></span><br/> | <span data-ttu-id="820a9-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="820a9-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="820a9-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="820a9-134">Minimum supported server</span></span><br/> | <span data-ttu-id="820a9-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="820a9-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="820a9-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="820a9-136">Namespace</span></span><br/>                | <span data-ttu-id="820a9-137">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="820a9-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="820a9-138">MOF</span><span class="sxs-lookup"><span data-stu-id="820a9-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="820a9-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="820a9-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="820a9-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="820a9-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="820a9-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="820a9-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="820a9-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="820a9-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="820a9-143">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="820a9-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="820a9-144">**\_Proceso Win32**</span><span class="sxs-lookup"><span data-stu-id="820a9-144">**Win32\_Process**</span></span>](win32-process.md)
</dt> </dl>

 

