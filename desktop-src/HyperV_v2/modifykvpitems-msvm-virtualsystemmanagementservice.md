---
description: Modifica los pares de clave y valor existentes en una máquina virtual.
ms.assetid: A014F681-4429-4982-95AA-DF371925BB3B
title: Método ModifyKvpItems de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyKvpItems
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6269e1a7794b6f04de606d13c90ef8dac1777369
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688066"
---
# <a name="modifykvpitems-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="397bc-103">Método ModifyKvpItems de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="397bc-103">ModifyKvpItems method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="397bc-104">Modifica los pares de clave y valor existentes en una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="397bc-104">Modifies existing key-value pairs on a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="397bc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="397bc-105">Syntax</span></span>


```mof
uint32 ModifyKvpItems(
  [in]  CIM_ComputerSystem REF TargetSystem,
  [in]  string                 DataItems[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="397bc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="397bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="397bc-107">*TargetSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="397bc-107">*TargetSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="397bc-108">Tipo: **[ **CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span><span class="sxs-lookup"><span data-stu-id="397bc-108">Type: **[**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span></span>

<span data-ttu-id="397bc-109">Referencia a la máquina virtual en la que se modificarán los pares clave-valor.</span><span class="sxs-lookup"><span data-stu-id="397bc-109">A reference to the virtual machine on which the key-value pairs will be modified.</span></span>

</dd> <dt>

<span data-ttu-id="397bc-110">*Elementos de elemento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="397bc-110">*DataItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="397bc-111">Tipo: **String \[ \]**</span><span class="sxs-lookup"><span data-stu-id="397bc-111">Type: **string\[\]**</span></span>

<span data-ttu-id="397bc-112">Matriz de pares de clave y valor que se van a modificar.</span><span class="sxs-lookup"><span data-stu-id="397bc-112">An array of key-value pairs to be modified.</span></span> <span data-ttu-id="397bc-113">Cada elemento de la matriz es una instancia incrustada de la clase [**MSVM \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) .</span><span class="sxs-lookup"><span data-stu-id="397bc-113">Each element of the array is an embedded instance of the [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) class.</span></span> <span data-ttu-id="397bc-114">Este método produce un error si alguno de los pares clave-valor especificados no existe en el sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="397bc-114">This method fails if any of the specified key-value pairs does not exist on the target system.</span></span> <span data-ttu-id="397bc-115">Esta matriz puede contener como máximo 128 elementos.</span><span class="sxs-lookup"><span data-stu-id="397bc-115">This array can contain at most 128 elements.</span></span>

</dd> <dt>

<span data-ttu-id="397bc-116">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="397bc-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="397bc-117">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="397bc-117">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="397bc-118">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="397bc-118">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="397bc-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="397bc-119">Return value</span></span>

<span data-ttu-id="397bc-120">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="397bc-120">Type: **uint32**</span></span>

<span data-ttu-id="397bc-121">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="397bc-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="397bc-122">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="397bc-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="397bc-123">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="397bc-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="397bc-124">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="397bc-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="397bc-125">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="397bc-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="397bc-126">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="397bc-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="397bc-127">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="397bc-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="397bc-128">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="397bc-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="397bc-129">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="397bc-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="397bc-130">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="397bc-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="397bc-131">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="397bc-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="397bc-132">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="397bc-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="397bc-133">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="397bc-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="397bc-134">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="397bc-134">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="397bc-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="397bc-135">Remarks</span></span>

<span data-ttu-id="397bc-136">El acceso a la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="397bc-136">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="397bc-137">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="397bc-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="397bc-138">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="397bc-138">Examples</span></span>

<span data-ttu-id="397bc-139">En el siguiente ejemplo de C# se modifican los pares clave-valor de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="397bc-139">The following C# sample modifies key-value pairs on a virtual machine.</span></span> <span data-ttu-id="397bc-140">Las utilidades a las que se hace referencia se pueden encontrar en [utilidades comunes para los ejemplos de virtualización (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="397bc-140">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="397bc-141">Para que funcione correctamente, se debe ejecutar el código siguiente en el servidor host de máquina virtual y se debe ejecutar con privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="397bc-141">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    class ModifyKvpItemsClass
    {
        static void ModifyKvpItems(string vmName, string itemName, string itemValue)
        {
            ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
            ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
            ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("ModifyKvpItems");
            ManagementClass kvpExchangeDataItem = new ManagementClass(scope, new ManagementPath("Msvm_KvpExchangeDataItem"), null);

            ManagementObject dataItem = kvpExchangeDataItem.CreateInstance();
            
            dataItem["Data"] = itemValue;
            dataItem["Name"] = itemName;
            dataItem["Source"] = 0;

            string[] dataItems = new string[1];
            dataItems[0] = dataItem.GetText(TextFormat.CimDtd20);

            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
            inParams["TargetSystem"] = vm.Path.Path;
            inParams["DataItems"] = dataItems;

            ManagementBaseObject outParams = virtualSystemService.InvokeMethod("ModifyKvpItems", inParams, null);

            if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
            {
                if (Utility.JobCompleted(outParams, scope))
                {
                    Console.WriteLine("KvpItems were modified successfully.");
                }
                else
                {
                    Console.WriteLine("Failed to modify KvpItems");
                }
            }
            else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                Console.WriteLine("KvpItems were modified successfully.");
            }
            else
            {
                Console.WriteLine("Modify virtual system kvp items failed with error {0}", outParams["ReturnValue"]);
            }

            inParams.Dispose();
            outParams.Dispose();
            vm.Dispose();
            dataItem.Dispose();
            virtualSystemService.Dispose();
        }

        static void Main(string[] args)
        {
            if (args != null && args.Length != 3)
            {
                Console.WriteLine("Usage: ModifyKvpItems vmName itemName itemValue");
                return;
            }
            ModifyKvpItems(args[0], args[1], args[2]);
        }
    }
}
```



<span data-ttu-id="397bc-142">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se modifican los pares clave-valor de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="397bc-142">The following Visual Basic Scripting Edition (VBScript) sample modifies key-value pairs on a virtual machine.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="397bc-143">Para que funcione correctamente, se debe ejecutar el código siguiente en el servidor host de máquina virtual y se debe ejecutar con privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="397bc-143">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```VB
option explicit 

dim objWMIService
dim managementService
dim fileSystem


const JobStarting = 3
const JobRunning = 4
const JobCompleted = 7
const wmiStarted = 4096
const wmiSuccessful = 0

Main()

'-----------------------------------------------------------------
' Main
'-----------------------------------------------------------------
Sub Main()

    dim computer, vmName, itemName, itemValue, myVm, objArgs
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."

    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")
    set managementService = objWMIService.ExecQuery("select * from Msvm_VirtualSystemManagementService").ItemIndex(0)

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 3 then
        vmName = objArgs.Unnamed.Item(0)
        itemName = objArgs.Unnamed.Item(1)
        itemValue = objArgs.Unnamed.Item(2)
    else
        WScript.Echo "usage: cscript AddKvpItems.vbs vmName itemName itemValue"
        WScript.Quit(1)
    end if

    set myVm = GetComputerSystem(vmName)

    if ModifyKvpItems(myVm, itemName, itemValue) then

        WriteLog "Done"
        WScript.Quit(0)

    else
        WriteLog "ModifyKvpItems failed"
        WScript.Quit(1)
    end if


End Sub

'-----------------------------------------------------------------
' Retrieve Msvm_VirtualComputerSystem from base on its ElementName
'-----------------------------------------------------------------
Function GetComputerSystem(vmElementName)
    On Error Resume Next
    dim query
    query = Format1("select * from Msvm_ComputerSystem where ElementName = '{0}'", vmElementName)
    set GetComputerSystem = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function

'-----------------------------------------------------------------
' RemoveVirtualSystemResource
'-----------------------------------------------------------------
Function ModifyKvpItems(computerSystem, itemName, itemValue)

    dim dataItem, dataItems, objInParam, objOutParams
    
    ModifyKvpItems = false
    
    set dataItem = objWMIService.Get("Msvm_KvpExchangeDataItem").SpawnInstance_()
    
    dataItem.Data = itemValue
    dataItem.Name = itemName
    dataItem.Source = 0
    
    dataItems = Array(1)
    dataItems(0) = dataItem.GetText_(1)
    
    set objInParam = managementService.Methods_("ModifyKvpItems").InParameters.SpawnInstance_()
    objInParam.TargetSystem = computerSystem.Path_.Path
    objInParam.dataItems = dataItems
    
    set objOutParams = managementService.ExecMethod_("ModifyKvpItems", objInParam)

    if objOutParams.ReturnValue = wmiStarted then
        if (WMIJobCompleted(objOutParams)) then
            ModifyKvpItems = true
        end if
    elseif objOutParams.ReturnValue = wmiSuccessful then
        ModifyKvpItems = true
    else
        WriteLog Format1("ModifyKvpItems failed with {0}", objOutParams.ReturnValue)
    end if

End Function

'-----------------------------------------------------------------
' Handle wmi Job object
'-----------------------------------------------------------------
Function WMIJobCompleted(outParam)

    dim WMIJob, jobState
    WMIJobCompleted = true

    set WMIJob = objWMIService.Get(outParam.Job)
    
    jobState = WMIJob.JobState

    while jobState = JobRunning or jobState = JobStarting
        WriteLog Format1("In progress... {0}% completed.",WMIJob.PercentComplete)
        WScript.Sleep(1000)
        set WMIJob = objWMIService.Get(outParam.Job)
        jobState = WMIJob.JobState
    wend

    if (WMIJob.JobState <> JobCompleted) then
        WriteLog Format1("ErrorDescription:{0}", WMIJob.ErrorDescription)
        WriteLog Format1("ErrorCode:{0}", WMIJob.ErrorCode)
        WMIJobCompleted = false
    end if
    
End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\ModifyKvpItems.log", 8, true)
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



## <a name="requirements"></a><span data-ttu-id="397bc-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="397bc-144">Requirements</span></span>



| <span data-ttu-id="397bc-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="397bc-145">Requirement</span></span> | <span data-ttu-id="397bc-146">Value</span><span class="sxs-lookup"><span data-stu-id="397bc-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="397bc-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="397bc-147">Minimum supported client</span></span><br/> | <span data-ttu-id="397bc-148">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="397bc-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="397bc-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="397bc-149">Minimum supported server</span></span><br/> | <span data-ttu-id="397bc-150">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="397bc-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="397bc-151">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="397bc-151">Namespace</span></span><br/>                | <span data-ttu-id="397bc-152">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="397bc-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="397bc-153">MOF</span><span class="sxs-lookup"><span data-stu-id="397bc-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="397bc-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="397bc-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="397bc-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="397bc-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="397bc-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="397bc-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="397bc-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="397bc-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="397bc-158">**ModifyKvpItems (V1)**</span><span class="sxs-lookup"><span data-stu-id="397bc-158">**ModifyKvpItems (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifykvpitems-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="397bc-159">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="397bc-159">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

