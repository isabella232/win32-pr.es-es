---
description: Valida la configuración de una máquina virtual planeada y la convierte en una máquina virtual realizada.
ms.assetid: bddbdc35-4603-45c3-96b4-04f445dbb3a6
title: Método RealizePlannedSystem de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RealizePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fc69cbc9be9fc72bc7c1184ec30d9e2b58ba2b6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278618"
---
# <a name="realizeplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="0d4a4-103">Método RealizePlannedSystem de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="0d4a4-103">RealizePlannedSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="0d4a4-104">Valida la configuración de una máquina virtual planeada y la convierte en una máquina virtual realizada.</span><span class="sxs-lookup"><span data-stu-id="0d4a4-104">Validates the configuration of a planned virtual machine and converts it to a realized virtual machine.</span></span> <span data-ttu-id="0d4a4-105">Los archivos de estado en tiempo de ejecución o guardados asociados a la máquina virtual se copiarán del directorio de importación a la raíz de datos de la máquina virtual, si procede.</span><span class="sxs-lookup"><span data-stu-id="0d4a4-105">Any runtime or saved state files associated with the virtual machine will be copied from the import directory to the virtual machine's data root, if applicable.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d4a4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d4a4-106">Syntax</span></span>


```mof
uint32 RealizePlannedSystem(
  [in]  Msvm_PlannedComputerSystem REF PlannedSystem,
  [out] CIM_ComputerSystem         REF ResultingSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0d4a4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0d4a4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d4a4-108">*PlannedSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0d4a4-108">*PlannedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d4a4-109">Referencia a la instancia de [**MSVM \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) que se va a convertir en una máquina virtual realizada.</span><span class="sxs-lookup"><span data-stu-id="0d4a4-109">A reference to the [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) instance which is to be converted into a realized virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="0d4a4-110">*ResultingSystem* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0d4a4-110">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d4a4-111">Si la operación se completa de forma sincrónica, se trata de una referencia a un objeto [**\_ ComputerSystem de CIM**](msvm-computersystem.md) que representa la máquina virtual resultante.</span><span class="sxs-lookup"><span data-stu-id="0d4a4-111">If the operation is completed synchronously, a reference to a [**CIM\_ComputerSystem**](msvm-computersystem.md) object that represents the resulting realized virtual machine.</span></span>

<span data-ttu-id="0d4a4-112">DataType actualizado de [**MSVM \_ ComputerSystem**](msvm-computersystem.md) en Windows 10, versión 1703.</span><span class="sxs-lookup"><span data-stu-id="0d4a4-112">Datatype updated from [**Msvm\_ComputerSystem**](msvm-computersystem.md) in Windows 10, version 1703.</span></span>

</dd> <dt>

<span data-ttu-id="0d4a4-113">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0d4a4-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d4a4-114">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0d4a4-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d4a4-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0d4a4-115">Return value</span></span>

<span data-ttu-id="0d4a4-116">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="0d4a4-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0d4a4-117">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="0d4a4-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0d4a4-118">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="0d4a4-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0d4a4-119">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="0d4a4-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="0d4a4-120">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="0d4a4-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="0d4a4-121">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="0d4a4-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="0d4a4-122">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="0d4a4-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="0d4a4-123">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="0d4a4-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="0d4a4-124">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="0d4a4-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="0d4a4-125">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="0d4a4-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="0d4a4-126">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="0d4a4-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="0d4a4-127">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="0d4a4-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="0d4a4-128">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="0d4a4-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="0d4a4-129">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="0d4a4-129">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="0d4a4-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0d4a4-130">Examples</span></span>

<span data-ttu-id="0d4a4-131">En el siguiente ejemplo de C# se usa el método **RealizePlannedSystem** para obtener una máquina virtual planeada.</span><span class="sxs-lookup"><span data-stu-id="0d4a4-131">The following C# sample uses the **RealizePlannedSystem** method to realize a planned virtual machine.</span></span> <span data-ttu-id="0d4a4-132">Este código se toma del [ejemplo de máquinas virtuales planeadas de Hyper-V](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span><span class="sxs-lookup"><span data-stu-id="0d4a4-132">This code is taken from the [Hyper-V planned virtual machines sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span></span> <span data-ttu-id="0d4a4-133">Las utilidades a las que se hace referencia se pueden encontrar en [utilidades comunes para los ejemplos de virtualización (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="0d4a4-133">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0d4a4-134">Para que funcione correctamente, se debe ejecutar el código siguiente en el servidor host de máquina virtual y se debe ejecutar con privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="0d4a4-134">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and realizes it.
/// </summary>
/// <param name="pvmName">The name of the PVM to be realized.</param>
/// <returns>The Realized Virtual Machine.</returns>
internal static ManagementObject
RealizePvm(
    string pvmName
    )
{
    ManagementObject vm = null;
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams =
        managementService.GetMethodParameters("RealizePlannedSystem"))
    {
        inParams["PlannedSystem"] = pvm.Path;

        Console.WriteLine("Realizing Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams =
            managementService.InvokeMethod("RealizePlannedSystem", inParams, null))
        {
            if (WmiUtilities.ValidateOutput(outParams, scope, true, true))
            {
                using (ManagementObject job =
                    new ManagementObject((string)outParams["Job"]))
                using (ManagementObjectCollection pvmCollection =
                    job.GetRelated("Msvm_ComputerSystem",
                        "Msvm_AffectedJobElement", null, null, null, null, false, null))
                {
                    vm = WmiUtilities.GetFirstObjectFromCollection(pvmCollection);
                }
            }
        }
    }

    return vm;
}
```



## <a name="requirements"></a><span data-ttu-id="0d4a4-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d4a4-135">Requirements</span></span>



| <span data-ttu-id="0d4a4-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d4a4-136">Requirement</span></span> | <span data-ttu-id="0d4a4-137">Value</span><span class="sxs-lookup"><span data-stu-id="0d4a4-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d4a4-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d4a4-138">Minimum supported client</span></span><br/> | <span data-ttu-id="0d4a4-139">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d4a4-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0d4a4-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d4a4-140">Minimum supported server</span></span><br/> | <span data-ttu-id="0d4a4-141">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d4a4-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0d4a4-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0d4a4-142">Namespace</span></span><br/>                | <span data-ttu-id="0d4a4-143">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="0d4a4-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0d4a4-144">MOF</span><span class="sxs-lookup"><span data-stu-id="0d4a4-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d4a4-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d4a4-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d4a4-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0d4a4-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d4a4-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0d4a4-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0d4a4-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d4a4-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d4a4-149">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="0d4a4-149">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

