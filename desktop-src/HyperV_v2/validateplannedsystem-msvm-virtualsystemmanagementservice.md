---
description: Valida el sistema planeado especificado.
ms.assetid: cb969b38-f36d-4c70-b234-590f1c219d22
title: Método ValidatePlannedSystem de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ValidatePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 96137c3774291e06bfffdea3843658a427e36950
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817086"
---
# <a name="validateplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="4fca3-103">Método ValidatePlannedSystem de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="4fca3-103">ValidatePlannedSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="4fca3-104">Valida el sistema planeado especificado.</span><span class="sxs-lookup"><span data-stu-id="4fca3-104">Validates the specified planned system.</span></span> <span data-ttu-id="4fca3-105">Esto implica comprobaciones de la configuración de la máquina virtual, los dispositivos, la configuración de instantáneas, los dispositivos de instantáneas, los archivos de estado guardado y los archivos de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="4fca3-105">This involves checks of the virtual machine configuration, devices, snapshot configuration, snapshot devices, saved state files and storage files.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fca3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4fca3-106">Syntax</span></span>


```mof
uint32 ValidatePlannedSystem(
  [in]  Msvm_PlannedComputerSystem REF PlannedSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="4fca3-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4fca3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fca3-108">*PlannedSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="4fca3-108">*PlannedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fca3-109">Referencia a un objeto [**MSVM \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) que representa el sistema planeado que se va a validar.</span><span class="sxs-lookup"><span data-stu-id="4fca3-109">A reference to an [**Msvm\_PlannedComputerSystem**](msvm-plannedcomputersystem.md) object that represents the planned system to be validated.</span></span>

</dd> <dt>

<span data-ttu-id="4fca3-110">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="4fca3-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fca3-111">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4fca3-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fca3-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4fca3-112">Return value</span></span>

<span data-ttu-id="4fca3-113">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4fca3-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="4fca3-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="4fca3-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="4fca3-115">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="4fca3-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="4fca3-116">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="4fca3-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="4fca3-117">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="4fca3-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="4fca3-118">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="4fca3-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="4fca3-119">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="4fca3-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="4fca3-120">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="4fca3-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="4fca3-121">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="4fca3-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="4fca3-122">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="4fca3-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="4fca3-123">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="4fca3-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="4fca3-124">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="4fca3-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="4fca3-125">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="4fca3-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="4fca3-126">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="4fca3-126">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="4fca3-127">**Archivo en uso** (32779)</span><span class="sxs-lookup"><span data-stu-id="4fca3-127">**File in Use** (32779)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="4fca3-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4fca3-128">Examples</span></span>

<span data-ttu-id="4fca3-129">En el siguiente ejemplo de C# se usa el método **ValidatePlannedSystem** para validar una máquina virtual planeada.</span><span class="sxs-lookup"><span data-stu-id="4fca3-129">The following C# sample uses the **ValidatePlannedSystem** method to validate a planned virtual machine.</span></span> <span data-ttu-id="4fca3-130">Este código se toma del [ejemplo de máquinas virtuales planeadas de Hyper-V](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span><span class="sxs-lookup"><span data-stu-id="4fca3-130">This code is taken from the [Hyper-V planned virtual machines sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm).</span></span> <span data-ttu-id="4fca3-131">Las utilidades a las que se hace referencia se pueden encontrar en [utilidades comunes para los ejemplos de virtualización (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="4fca3-131">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4fca3-132">Para que funcione correctamente, se debe ejecutar el código siguiente en el servidor host de máquina virtual y se debe ejecutar con privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="4fca3-132">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and validates it, displaying
/// any warnings produced.
/// </summary>
/// <param name="pvmName">The name of the PVM to be validated.</param>
internal static void
ValidatePvm(
    string pvmName
    )
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams = 
        managementService.GetMethodParameters("ValidatePlannedSystem"))
    {
        inParams["PlannedSystem"] = pvm.Path;

        Console.WriteLine("Validating Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams = 
            managementService.InvokeMethod("ValidatePlannedSystem", inParams, null))
        {
            if (WmiUtilities.ValidateOutput(outParams, scope))
            {
                using (ManagementObject job = 
                    new ManagementObject((string)outParams["Job"]))
                {
                    WmiUtilities.PrintMsvmErrors(job);
                }
            }
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="4fca3-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fca3-133">Requirements</span></span>



| <span data-ttu-id="4fca3-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fca3-134">Requirement</span></span> | <span data-ttu-id="4fca3-135">Value</span><span class="sxs-lookup"><span data-stu-id="4fca3-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fca3-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4fca3-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4fca3-137">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="4fca3-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4fca3-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4fca3-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4fca3-139">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="4fca3-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4fca3-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4fca3-140">Namespace</span></span><br/>                | <span data-ttu-id="4fca3-141">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="4fca3-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4fca3-142">MOF</span><span class="sxs-lookup"><span data-stu-id="4fca3-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4fca3-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4fca3-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4fca3-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4fca3-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fca3-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4fca3-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4fca3-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="4fca3-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fca3-147">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="4fca3-147">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

