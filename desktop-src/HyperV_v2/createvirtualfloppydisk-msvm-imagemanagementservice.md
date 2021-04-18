---
description: Crea un archivo de disquete virtual.
ms.assetid: C7B5712C-55DD-4784-8B2E-A8DE02E4CFD8
title: Método CreateVirtualFloppyDisk de la clase Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.CreateVirtualFloppyDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 98781a4f72218ee61a4966dc76b21f7417353e0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668135"
---
# <a name="createvirtualfloppydisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="7e213-103">Método CreateVirtualFloppyDisk de la \_ clase ImageManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="7e213-103">CreateVirtualFloppyDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="7e213-104">Crea un archivo de disquete virtual.</span><span class="sxs-lookup"><span data-stu-id="7e213-104">Creates a virtual floppy disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e213-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e213-105">Syntax</span></span>


```mof
uint32 CreateVirtualFloppyDisk(
  [in]  string              Path,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7e213-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7e213-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e213-107">*Ruta de acceso* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7e213-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e213-108">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="7e213-108">Type: **string**</span></span>

<span data-ttu-id="7e213-109">Ruta de acceso completa que especifica la ubicación del nuevo archivo.</span><span class="sxs-lookup"><span data-stu-id="7e213-109">A fully qualified path that specifies the location of the new file.</span></span>

</dd> <dt>

<span data-ttu-id="7e213-110">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7e213-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e213-111">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="7e213-111">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="7e213-112">Referencia al trabajo (puede ser **null** si se ha completado la tarea).</span><span class="sxs-lookup"><span data-stu-id="7e213-112">A reference to the job (can be **Null** if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e213-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e213-113">Return value</span></span>

<span data-ttu-id="7e213-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7e213-114">Type: **uint32**</span></span>

<span data-ttu-id="7e213-115">Este método puede devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="7e213-115">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7e213-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="7e213-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7e213-117">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="7e213-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7e213-118">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="7e213-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="7e213-119">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="7e213-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="7e213-120">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="7e213-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="7e213-121">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="7e213-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="7e213-122">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="7e213-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="7e213-123">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="7e213-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="7e213-124">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="7e213-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="7e213-125">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="7e213-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="7e213-126">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="7e213-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="7e213-127">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="7e213-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="7e213-128">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="7e213-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="7e213-129">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="7e213-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="7e213-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7e213-130">Remarks</span></span>

<span data-ttu-id="7e213-131">El acceso a la clase [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="7e213-131">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="7e213-132">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="7e213-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="7e213-133">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7e213-133">Examples</span></span>

<span data-ttu-id="7e213-134">En el siguiente ejemplo de C# se crea un archivo de disquete virtual.</span><span class="sxs-lookup"><span data-stu-id="7e213-134">The following C# example creates a virtual floppy disk file.</span></span> <span data-ttu-id="7e213-135">Las utilidades a las que se hace referencia se pueden encontrar en [utilidades comunes para los ejemplos de virtualización (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="7e213-135">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class CreateVFD
    {
        static void CreateVirtualFlopy(string vhdPath)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

            ManagementBaseObject inParams = imageService.GetMethodParameters("CreateVirtualFloppyDisk");
            inParams["Path"] = vhdPath;
            ManagementBaseObject outParams = imageService.InvokeMethod("CreateVirtualFloppyDisk", inParams, null);
            if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
            {
                if (Utility.JobCompleted(outParams, scope))
                {
                    Console.WriteLine("{0} was created successfully.", inParams["Path"]);
                }
                else
                {
                    Console.WriteLine("Unable to create {0}", inParams["Path"]);
                }
            }

            inParams.Dispose();
            outParams.Dispose();
            imageService.Dispose();
        }

        static void Main(string[] args)
        {
            if (args != null && args.Length != 1)
            {
                Console.WriteLine("Usage: CreateVFD path");
                return;
            }
            CreateVirtualFlopy(args[0]);
        }
    }
}

```



<span data-ttu-id="7e213-136">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se crea un archivo de disquete virtual.</span><span class="sxs-lookup"><span data-stu-id="7e213-136">The following Visual Basic Scripting Edition (VBScript) example creates a virtual floppy disk file.</span></span>


```VB
option explicit 

dim objWMIService
dim managementService
dim fileSystem


const JobStarting = 3
const JobRunning = 4
const JobCompleted = 7
const wmiStarted = 4096

const method = "CreateVirtualFloppyDisk"
Main()

'-----------------------------------------------------------------
' Main
'-----------------------------------------------------------------
Sub Main()

    dim computer, objArgs, vfdPath

    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."
    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")
    set managementService = objWMIService.ExecQuery("Select * from Msvm_ImageManagementService").ItemIndex(0)

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 1 then
       vfdPath = objArgs.Unnamed.Item(0)
    else
       WScript.Echo "usage: cscript CreateVFD.vbs VFDFilePath "
       WScript.Quit(1)
    end if

    if CreateVirtualFloppyDisk(vfdPath) then
        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "CreateVFD failed"
        WScript.Quit(1)
    end if

End Sub

'-----------------------------------------------------------------
' Execute CreateVirtualFloppyDisk method
'-----------------------------------------------------------------
Function CreateVirtualFloppyDisk(vfdPath)
    WriteLog Format1("Function CreateVirtualFloppyDisk({0})",  vfdPath)
    
    dim objInParam, objOutParams

    CreateVirtualFloppyDisk = false

    set objInParam = managementService.Methods_("CreateVirtualFloppyDisk").InParameters.SpawnInstance_()
    objInParam.Path = vfdPath

    set objOutParams = managementService.ExecMethod_("CreateVirtualFloppyDisk", objInParam)

    if (WMIMethodStarted(objOutParams)) then
        if (WMIJobCompleted(objOutParams)) then
            WriteLog Format1("VHD {0} was created successfully", vfdPath)
            CreateVirtualFloppyDisk = true
        end if
    end if

End Function


'-----------------------------------------------------------------
' Handle wmi return values
'-----------------------------------------------------------------
Function WMIMethodStarted(outParam)
    WriteLog "Function WMIMethodStarted"
    
    dim wmiStatus
    
    WMIMethodStarted = false

    if Not IsNull(outParam) then
        wmiStatus = outParam.ReturnValue

        if  wmiStatus = wmiStarted then
            WMIMethodStarted = true
        else
            WriteLog Format2("Failed to create VFD {0} ConcreteJob with error {1}", vfdPath, wmiStatus)
        end if
   end if

End Function

'-----------------------------------------------------------------
' Handle wmi Job object
'-----------------------------------------------------------------
Function WMIJobCompleted(outParam)
    WriteLog "Function WMIJobCompleted"
    dim WMIJob, jobState

    set WMIJob = objWMIService.Get(outParam.Job)

    WMIJobCompleted = true

    jobState = WMIJob.JobState

    while jobState = JobRunning or jobState = JobStarting
        WriteLog Format1("In progress... {0}% completed.",WMIJob.PercentComplete)
        WScript.Sleep(1000)
        set WMIJob = objWMIService.Get(outParam.Job)
        jobState = WMIJob.JobState
    wend

    if (jobState <> JobCompleted) then
        WriteLog Format1("ErrorCode:{0}", WMIJob.ErrorCode)
        WriteLog Format1("ErrorDescription:{0}", WMIJob.ErrorDescription)
        WMIJobCompleted = false
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\CreateVFD.log", 8, true)
    WScript.Echo line
    fileStream.WriteLine line
    fileStream.Close

End Sub

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format2(myString, arg0, arg1)
    Format2 = Format1(myString, arg0)
    Format2 = Replace(Format2, "{1}", arg1)
End Function

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format1(myString, arg0)
    Format1 = Replace(myString, "{0}", arg0)
End Function
```



## <a name="requirements"></a><span data-ttu-id="7e213-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e213-137">Requirements</span></span>



| <span data-ttu-id="7e213-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e213-138">Requirement</span></span> | <span data-ttu-id="7e213-139">Value</span><span class="sxs-lookup"><span data-stu-id="7e213-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e213-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e213-140">Minimum supported client</span></span><br/> | <span data-ttu-id="7e213-141">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="7e213-141">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7e213-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7e213-142">Minimum supported server</span></span><br/> | <span data-ttu-id="7e213-143">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="7e213-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7e213-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7e213-144">Namespace</span></span><br/>                | <span data-ttu-id="7e213-145">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="7e213-145">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7e213-146">MOF</span><span class="sxs-lookup"><span data-stu-id="7e213-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7e213-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7e213-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7e213-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7e213-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e213-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7e213-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7e213-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e213-150">See also</span></span>

<dl> <dt>

<span data-ttu-id="7e213-151">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7e213-151">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7e213-152">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="7e213-152">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

