---
description: Quita los pares de clave y valor existentes de una máquina virtual.
ms.assetid: B2ECF609-89BB-4117-982B-EF56D51E1321
title: Método RemoveKvpItems de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveKvpItems
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4921805ade9538a4e05a15331f707b9356411aa7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546822"
---
# <a name="removekvpitems-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="ff353-103">Método RemoveKvpItems de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="ff353-103">RemoveKvpItems method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="ff353-104">Quita los pares de clave y valor existentes de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ff353-104">Removes existing key-value pairs from a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff353-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ff353-105">Syntax</span></span>


```mof
uint32 RemoveKvpItems(
  [in]  CIM_ComputerSystem REF TargetSystem,
  [in]  string                 DataItems[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ff353-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ff353-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff353-107">*TargetSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ff353-107">*TargetSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff353-108">Tipo: **[ **CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span><span class="sxs-lookup"><span data-stu-id="ff353-108">Type: **[**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**</span></span>

<span data-ttu-id="ff353-109">Referencia a la máquina virtual en la que se quitarán los pares clave-valor.</span><span class="sxs-lookup"><span data-stu-id="ff353-109">A reference to the virtual machine on which the key-value pairs will be removed.</span></span>

</dd> <dt>

<span data-ttu-id="ff353-110">*Elementos de elemento* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ff353-110">*DataItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff353-111">Tipo: **String \[ \]**</span><span class="sxs-lookup"><span data-stu-id="ff353-111">Type: **string\[\]**</span></span>

<span data-ttu-id="ff353-112">Matriz de pares de clave y valor que se van a quitar (solo deben coincidir las claves).</span><span class="sxs-lookup"><span data-stu-id="ff353-112">An array of key-value pairs to be removed (only the keys need to match).</span></span> <span data-ttu-id="ff353-113">Cada elemento de la matriz es una instancia incrustada de la clase [**MSVM \_ KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) .</span><span class="sxs-lookup"><span data-stu-id="ff353-113">Each element of the array is an embedded instance of the [**Msvm\_KvpExchangeDataItem**](msvm-kvpexchangedataitem.md) class.</span></span> <span data-ttu-id="ff353-114">Este método produce un error si alguno de los pares clave-valor especificados no existe en el sistema de destino.</span><span class="sxs-lookup"><span data-stu-id="ff353-114">This method fails if any of the specified key-value pairs does not exist on the target system.</span></span> <span data-ttu-id="ff353-115">Esta matriz puede contener como máximo 128 elementos.</span><span class="sxs-lookup"><span data-stu-id="ff353-115">This array can contain at most 128 elements.</span></span>

</dd> <dt>

<span data-ttu-id="ff353-116">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ff353-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff353-117">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="ff353-117">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="ff353-118">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ff353-118">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff353-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ff353-119">Return value</span></span>

<span data-ttu-id="ff353-120">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ff353-120">Type: **uint32**</span></span>

<span data-ttu-id="ff353-121">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="ff353-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ff353-122">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="ff353-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ff353-123">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="ff353-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ff353-124">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="ff353-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ff353-125">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="ff353-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ff353-126">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="ff353-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ff353-127">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="ff353-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ff353-128">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="ff353-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ff353-129">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="ff353-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ff353-130">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="ff353-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ff353-131">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="ff353-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ff353-132">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="ff353-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ff353-133">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="ff353-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ff353-134">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="ff353-134">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="ff353-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff353-135">Remarks</span></span>

<span data-ttu-id="ff353-136">El acceso a la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="ff353-136">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ff353-137">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ff353-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="ff353-138">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ff353-138">Examples</span></span>

<span data-ttu-id="ff353-139">En el siguiente ejemplo de C# se quitan los pares clave-valor de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ff353-139">The following C# sample removes key-value pairs from a virtual machine.</span></span> <span data-ttu-id="ff353-140">Las utilidades a las que se hace referencia se pueden encontrar en [utilidades comunes para los ejemplos de virtualización (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="ff353-140">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ff353-141">Para que funcione correctamente, se debe ejecutar el código siguiente en el servidor host de máquina virtual y se debe ejecutar con privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="ff353-141">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
public static void RemoveKvpItems(string vmName, string itemName)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
    ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("RemoveKvpItems");
    ManagementClass kvpExchangeDataItem = new ManagementClass(scope, new ManagementPath("Msvm_KvpExchangeDataItem"), null);

    ManagementObject dataItem = kvpExchangeDataItem.CreateInstance();

    dataItem["Data"] = "";
    dataItem["Name"] = itemName;
    dataItem["Source"] = 0;

    string[] dataItems = new string[1];
    dataItems[0] = dataItem.GetText(TextFormat.CimDtd20);

    ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
    inParams["TargetSystem"] = vm.Path.Path;
    inParams["DataItems"] = dataItems;

    ManagementBaseObject outParams = virtualSystemService.InvokeMethod("RemoveKvpItems", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("KvpItems were removed successfully.");

        }
        else
        {
            Console.WriteLine("Failed to remove KvpItems");
        }
    } 
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        Console.WriteLine("KvpItems were removed successfully.");
    }
    else
    {
        Console.WriteLine("Remove KvpItems failed with error {0}", outParams["ReturnValue"]);
    }

    inParams.Dispose();
    outParams.Dispose();
    dataItem.Dispose();
    vm.Dispose();
    virtualSystemService.Dispose();
    
}
```



<span data-ttu-id="ff353-142">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se quitan los pares clave-valor de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ff353-142">The following Visual Basic Scripting Edition (VBScript) sample removes key-value pairs from a virtual machine.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ff353-143">Para que funcione correctamente, se debe ejecutar el código siguiente en el servidor host de máquina virtual y se debe ejecutar con privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="ff353-143">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


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

    dim computer, vmName, itemName, myVm, objArgs
    
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    computer = "."

    set objWMIService = GetObject("winmgmts:\\" & computer & "\root\virtualization\v2")
    set managementService = objWMIService.ExecQuery("select * from Msvm_VirtualSystemManagementService").ItemIndex(0)

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 3 then
        vmName = objArgs.Unnamed.Item(0)
        itemName = objArgs.Unnamed.Item(1)
    else
        WScript.Echo "usage: cscript AddKvpItems.vbs vmName itemName"
        WScript.Quit(1)
    end if

    set myVm = GetComputerSystem(vmName)

    if RemoveKvpItems(myVm, itemName) then

        WriteLog "Done"
        WScript.Quit(0)

    else
        WriteLog "RemoveKvpItems failed"
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
' RemoveKvpItems
'-----------------------------------------------------------------
Function RemoveKvpItems(computerSystem, itemName)

    dim dataItem, dataItems, objInParam, objOutParams
    
    RemoveKvpItems = false
    
    set dataItem = objWMIService.Get("Msvm_KvpExchangeDataItem").SpawnInstance_()
    dataItem.Data = ""
    dataItem.Name = itemName
    dataItem.Source = 0
    
    dataItems = Array(1)
    dataItems(0) = dataItem.GetText_(1)
    
    set objInParam = managementService.Methods_("RemoveKvpItems").InParameters.SpawnInstance_()
    objInParam.TargetSystem = computerSystem.Path_.Path
    objInParam.dataItems = dataItems
    
    set objOutParams = managementService.ExecMethod_("RemoveKvpItems", objInParam)

    if objOutParams.ReturnValue = wmiStarted then
        if (WMIJobCompleted(objOutParams)) then
            RemoveKvpItems = true
        end if
    elseif objOutParams.ReturnValue = wmiSuccessful then
        RemoveKvpItems = true
    else
        WriteLog Format1("RemoveKvpItems failed with {0}", objOutParams.ReturnValue )
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
    set fileStream = fileSystem.OpenTextFile(".\RemoveKvpItems.log", 8, true)
    WScript.Echo line
    fileStream.WriteLine line
    fileStream.Close

End Sub

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format1(myString, arg0)
    Format1 = Replace(myString, "{0}", arg0)
End Function
```



## <a name="requirements"></a><span data-ttu-id="ff353-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff353-144">Requirements</span></span>



| <span data-ttu-id="ff353-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff353-145">Requirement</span></span> | <span data-ttu-id="ff353-146">Value</span><span class="sxs-lookup"><span data-stu-id="ff353-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff353-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff353-147">Minimum supported client</span></span><br/> | <span data-ttu-id="ff353-148">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="ff353-148">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ff353-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ff353-149">Minimum supported server</span></span><br/> | <span data-ttu-id="ff353-150">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="ff353-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ff353-151">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ff353-151">Namespace</span></span><br/>                | <span data-ttu-id="ff353-152">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ff353-152">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ff353-153">MOF</span><span class="sxs-lookup"><span data-stu-id="ff353-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ff353-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ff353-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ff353-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ff353-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff353-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ff353-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ff353-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="ff353-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff353-158">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="ff353-158">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

