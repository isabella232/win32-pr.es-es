---
description: Crea una instantánea de una máquina virtual.
ms.assetid: 2de12fe7-5ec2-49d0-87ff-cd48c34fec46
title: Método CreateSnapshot de la clase Msvm_VirtualSystemSnapshotService (Dbdaoint. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.CreateSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c62b4abf60e367da1c4ac4b176e5f5d70f547c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360872"
---
# <a name="createsnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a><span data-ttu-id="1ae28-103">Método CreateSnapshot de la \_ clase VirtualSystemSnapshotService de MSVM</span><span class="sxs-lookup"><span data-stu-id="1ae28-103">CreateSnapshot method of the Msvm\_VirtualSystemSnapshotService class</span></span>

<span data-ttu-id="1ae28-104">Crea una instantánea de una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1ae28-104">Creates a snapshot of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ae28-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1ae28-105">Syntax</span></span>


```mof
uint32 CreateSnapshot(
  [in]      CIM_ComputerSystem           REF AffectedSystem,
  [in]      string                           SnapshotSettings,
  [in]      uint16                           SnapshotType,
  [in, out] CIM_VirtualSystemSettingData REF ResultingSnapshot,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="1ae28-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ae28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ae28-107">*AffectedSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1ae28-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae28-108">Referencia a una clase [**de \_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual de la que se va a crear una instantánea.</span><span class="sxs-lookup"><span data-stu-id="1ae28-108">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the virtual machine to create a snapshot of.</span></span>

</dd> <dt>

<span data-ttu-id="1ae28-109">*SnapshotSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1ae28-109">*SnapshotSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae28-110">Una cadena que contiene una instancia incrustada de una clase [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)) que contiene la configuración de parámetros de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="1ae28-110">A string that contains an embedded instance of a [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) class that contains the parameter settings for the snapshot.</span></span> <span data-ttu-id="1ae28-111">Este parámetro es opcional y puede ser una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="1ae28-111">This parameter is optional and may be an empty string.</span></span>

</dd> <dt>

<span data-ttu-id="1ae28-112">*SnapshotType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1ae28-112">*SnapshotType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae28-113">Especifica el tipo de instantánea solicitada.</span><span class="sxs-lookup"><span data-stu-id="1ae28-113">Specifies the type of snapshot requested.</span></span> <span data-ttu-id="1ae28-114">Debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="1ae28-114">This must be one of the following values.</span></span>

<dt>

<span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>

<span data-ttu-id="1ae28-115"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Instantánea completa** (2)</span><span class="sxs-lookup"><span data-stu-id="1ae28-115"><span id="Full_Snapshot"></span><span id="full_snapshot"></span><span id="FULL_SNAPSHOT"></span>**Full Snapshot** (2)</span></span>


</dt> <dd>

<span data-ttu-id="1ae28-116">Instantánea completa de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1ae28-116">Complete snapshot of the virtual machine.</span></span>

</dd> <dt>

<span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>

<span data-ttu-id="1ae28-117"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Instantánea de disco** (3)</span><span class="sxs-lookup"><span data-stu-id="1ae28-117"><span id="Disk_Snapshot"></span><span id="disk_snapshot"></span><span id="DISK_SNAPSHOT"></span>**Disk Snapshot** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1ae28-118">Instantánea de discos de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1ae28-118">Snapshot of virtual machine disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="1ae28-119"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1ae28-119"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="1ae28-120"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="1ae28-120"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="1ae28-121">*ResultingSnapshot* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1ae28-121">*ResultingSnapshot* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae28-122">Referencia a un objeto [**\_ VirtualSystemSettingData de CIM**](/previous-versions//cc136954(v=vs.85)) que representa la instantánea de máquina virtual resultante.</span><span class="sxs-lookup"><span data-stu-id="1ae28-122">A reference to a [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) object that represents the resulting virtual machine snapshot.</span></span>

</dd> <dt>

<span data-ttu-id="1ae28-123">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1ae28-123">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ae28-124">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1ae28-124">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ae28-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ae28-125">Return value</span></span>

<span data-ttu-id="1ae28-126">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="1ae28-126">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="1ae28-127">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="1ae28-127">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1ae28-128">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="1ae28-128">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1ae28-129">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="1ae28-129">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1ae28-130">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="1ae28-130">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1ae28-131">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="1ae28-131">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1ae28-132">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="1ae28-132">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1ae28-133">**Tipo no válido** (6)</span><span class="sxs-lookup"><span data-stu-id="1ae28-133">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="1ae28-134">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1ae28-134">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1ae28-135">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="1ae28-135">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1ae28-136">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="1ae28-136">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="1ae28-137">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="1ae28-137">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="1ae28-138">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1ae28-138">Examples</span></span>

<span data-ttu-id="1ae28-139">En el siguiente código de ejemplo de C# se crea una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="1ae28-139">The following C# example code creates a virtual machine.</span></span> <span data-ttu-id="1ae28-140">Las utilidades a las que se hace referencia se pueden encontrar en [utilidades comunes para los ejemplos de virtualización (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="1ae28-140">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1ae28-141">Para que funcione correctamente, se debe ejecutar el código siguiente en el servidor host de máquina virtual y se debe ejecutar con privilegios de administrador.</span><span class="sxs-lookup"><span data-stu-id="1ae28-141">To function correctly, the following code must be run on the virtual machine host server, and it must be run with Administrator privileges.</span></span>

 


```CSharp
public static void CreateSnapshot(string vmName)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemSnapshotService");

    ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("CreateSnapshot");

    // Set the AffectedSystem property.
    ManagementObject vm = Utility.GetTargetComputer(vmName, scope);
    if (null == vm)
    {
        throw new ArgumentException(string.Format("The virtual machine \"{0}\" could not be found.", vmName));
    }

    inParams["AffectedSystem"] = vm.Path.Path;

    // Set the SnapshotSettings property.
#if(true)
    inParams["SnapshotSettings"] = "";
#else
    ManagementObject snapshotSettings = Utility.GetServiceObject(scope, "CIM_SettingData"); 
    inParams["SnapshotSettings"] = snapshotSettings.ToString();
#endif       
    // Set the SnapshotType property.
    inParams["SnapshotType"] = 2; // Full snapshot.

    ManagementBaseObject outParams = virtualSystemService.InvokeMethod("CreateSnapshot", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("Snapshot was created successfully.");

            MiscClass.GetAffectedElement(outParams, scope);
        }
        else
        {
            Console.WriteLine("Failed to create snapshot VM");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        Console.WriteLine("Snapshot was created successfully.");
    }
    else
    {
        Console.WriteLine("Create virtual system snapshot failed with error {0}", outParams["ReturnValue"]);
    }

    inParams.Dispose();
    outParams.Dispose();
    vm.Dispose();
    virtualSystemService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="1ae28-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ae28-142">Requirements</span></span>



| <span data-ttu-id="1ae28-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ae28-143">Requirement</span></span> | <span data-ttu-id="1ae28-144">Value</span><span class="sxs-lookup"><span data-stu-id="1ae28-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ae28-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ae28-145">Minimum supported client</span></span><br/> | <span data-ttu-id="1ae28-146">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="1ae28-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="1ae28-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ae28-147">Minimum supported server</span></span><br/> | <span data-ttu-id="1ae28-148">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="1ae28-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1ae28-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1ae28-149">Namespace</span></span><br/>                | <span data-ttu-id="1ae28-150">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="1ae28-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="1ae28-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ae28-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ae28-152"><dt>Dbdaoint. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ae28-152"><dt>Dbdaoint.h</dt></span></span> </dl>                   |
| <span data-ttu-id="1ae28-153">MOF</span><span class="sxs-lookup"><span data-stu-id="1ae28-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ae28-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ae28-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ae28-155">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1ae28-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ae28-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1ae28-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1ae28-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ae28-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ae28-158">**MSVM \_ VirtualSystemSnapshotService**</span><span class="sxs-lookup"><span data-stu-id="1ae28-158">**Msvm\_VirtualSystemSnapshotService**</span></span>](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[<span data-ttu-id="1ae28-159">**CreateVirtualSystemSnapshot (V1)**</span><span class="sxs-lookup"><span data-stu-id="1ae28-159">**CreateVirtualSystemSnapshot (V1)**</span></span>](/previous-versions/windows/desktop/virtual/createvirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> </dl>

 

