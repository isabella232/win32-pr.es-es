---
description: Quita la máquina virtual definida previamente del ámbito de administración del sistema host.
ms.assetid: 16E6EEB0-CB29-4FFC-AEFF-872E099337FA
title: Método DestroySystem de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1caf4e4a590bdbfe2f7543e23d5ca00018300fb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911693"
---
# <a name="destroysystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="730d3-103">Método DestroySystem de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="730d3-103">DestroySystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="730d3-104">Quita la máquina virtual definida previamente del ámbito de administración del sistema host.</span><span class="sxs-lookup"><span data-stu-id="730d3-104">Removes the previously defined virtual machine from the management scope of the host system.</span></span> <span data-ttu-id="730d3-105">También se quitarán las definiciones de recursos asociadas.</span><span class="sxs-lookup"><span data-stu-id="730d3-105">Any associated resource definitions will also be removed.</span></span> <span data-ttu-id="730d3-106">La máquina virtual debe estar en estado apagado o guardado antes de llamar a este método.</span><span class="sxs-lookup"><span data-stu-id="730d3-106">The virtual machine must be in the powered off or saved state prior to calling this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="730d3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="730d3-107">Syntax</span></span>


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="730d3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="730d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="730d3-109">*AffectedSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="730d3-109">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="730d3-110">Tipo: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="730d3-110">Type: **CIM\_ComputerSystem**</span></span>

<span data-ttu-id="730d3-111">Referencia a una instancia del ComputerSystem de [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la instancia de máquina virtual que se va a destruir.</span><span class="sxs-lookup"><span data-stu-id="730d3-111">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) that represents the virtual machine instance to be destroyed.</span></span>

</dd> <dt>

<span data-ttu-id="730d3-112">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="730d3-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="730d3-113">Tipo: **CIM \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="730d3-113">Type: **CIM\_ConcreteJob**</span></span>

<span data-ttu-id="730d3-114">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="730d3-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="730d3-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="730d3-115">Return value</span></span>

<span data-ttu-id="730d3-116">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="730d3-116">Type: **uint32**</span></span>

<span data-ttu-id="730d3-117">Si este método se ejecuta sincrónicamente, devuelve 0 si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="730d3-117">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="730d3-118">Si este método se ejecuta de forma asincrónica, devuelve 4096 y el parámetro de salida del *trabajo* se puede usar para realizar el seguimiento del progreso de la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="730d3-118">If this method is executed asynchronously, it returns 4096 and the *Job* output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="730d3-119">Cualquier otro valor devuelto indica un error.</span><span class="sxs-lookup"><span data-stu-id="730d3-119">Any other return value indicates an error.</span></span>

<dl> <dt>

<span data-ttu-id="730d3-120">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="730d3-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="730d3-121">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="730d3-121">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="730d3-122">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="730d3-122">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="730d3-123">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="730d3-123">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="730d3-124">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="730d3-124">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="730d3-125">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="730d3-125">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="730d3-126">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="730d3-126">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="730d3-127">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="730d3-127">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="730d3-128">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="730d3-128">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="730d3-129">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="730d3-129">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="730d3-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="730d3-130">Remarks</span></span>

<span data-ttu-id="730d3-131">El acceso a la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="730d3-131">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="730d3-132">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="730d3-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="730d3-133">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="730d3-133">Examples</span></span>

<span data-ttu-id="730d3-134">En el siguiente ejemplo de C# se usa el método **DestroySystem** para quitar una máquina virtual planeada.</span><span class="sxs-lookup"><span data-stu-id="730d3-134">The following C# sample uses the **DestroySystem** method to remove a planned virtual machine.</span></span> <span data-ttu-id="730d3-135">Este código se toma del [ejemplo de máquinas virtuales planeadas de Hyper-V](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span><span class="sxs-lookup"><span data-stu-id="730d3-135">This code is taken from the [Hyper-V planned virtual machines sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span></span> <span data-ttu-id="730d3-136">Las utilidades a las que se hace referencia se pueden encontrar en [utilidades comunes para los ejemplos de virtualización (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="730d3-136">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="730d3-137">Para que funcione correctamente, se debe ejecutar el código siguiente en el servidor host de máquina virtual y se debe ejecutar con privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="730d3-137">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and removes it.
/// </summary>
/// <param name="pvmName">The name of the PVM to be removed.</param>
internal static void
RemovePvm(
    string pvmName
    )
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams =
        managementService.GetMethodParameters("DestroySystem"))
    {
        inParams["AffectedSystem"] = pvm.Path;

        Console.WriteLine("Removing Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams =
            managementService.InvokeMethod("DestroySystem", inParams, null))
        {
            WmiUtilities.ValidateOutput(outParams, scope);
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="730d3-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="730d3-138">Requirements</span></span>



| <span data-ttu-id="730d3-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="730d3-139">Requirement</span></span> | <span data-ttu-id="730d3-140">Value</span><span class="sxs-lookup"><span data-stu-id="730d3-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="730d3-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="730d3-141">Minimum supported client</span></span><br/> | <span data-ttu-id="730d3-142">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="730d3-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="730d3-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="730d3-143">Minimum supported server</span></span><br/> | <span data-ttu-id="730d3-144">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="730d3-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="730d3-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="730d3-145">Namespace</span></span><br/>                | <span data-ttu-id="730d3-146">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="730d3-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="730d3-147">MOF</span><span class="sxs-lookup"><span data-stu-id="730d3-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="730d3-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="730d3-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="730d3-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="730d3-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="730d3-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="730d3-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="730d3-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="730d3-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="730d3-152">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="730d3-152">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

