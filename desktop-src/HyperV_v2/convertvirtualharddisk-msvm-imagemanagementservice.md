---
description: Convierte un disco duro virtual existente en un tipo o formato diferente.
ms.assetid: D4F3A030-D860-4569-B6CD-31661BD40D54
title: Método ConvertVirtualHardDisk de la clase Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ConvertVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 766b117b69ecfebd13986d02ca21df3725981bb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687854"
---
# <a name="convertvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="c7eec-103">Método ConvertVirtualHardDisk de la \_ clase ImageManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="c7eec-103">ConvertVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="c7eec-104">Convierte un disco duro virtual existente en un tipo o formato diferente.</span><span class="sxs-lookup"><span data-stu-id="c7eec-104">Converts an existing virtual hard disk to a different type or format.</span></span> <span data-ttu-id="c7eec-105">Este método crea un nuevo disco duro virtual y no convierte el disco duro virtual de origen en su lugar.</span><span class="sxs-lookup"><span data-stu-id="c7eec-105">This method creates a new virtual hard disk and does not convert the source virtual hard disk in place.</span></span> <span data-ttu-id="c7eec-106">Vea la sección Comentarios para conocer las restricciones de uso de este método.</span><span class="sxs-lookup"><span data-stu-id="c7eec-106">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7eec-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7eec-107">Syntax</span></span>


```mof
uint32 ConvertVirtualHardDisk(
  [in]  string              SourcePath,
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c7eec-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c7eec-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7eec-109">*SourcePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c7eec-109">*SourcePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7eec-110">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="c7eec-110">Type: **string**</span></span>

<span data-ttu-id="c7eec-111">Ruta de acceso completa del archivo de disco duro virtual de origen que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="c7eec-111">The fully qualified path of the source virtual hard disk file to convert.</span></span> <span data-ttu-id="c7eec-112">Este archivo no se modificará como resultado de esta operación.</span><span class="sxs-lookup"><span data-stu-id="c7eec-112">This file will not be modified as a result of this operation.</span></span>

</dd> <dt>

<span data-ttu-id="c7eec-113">*VirtualDiskSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c7eec-113">*VirtualDiskSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7eec-114">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="c7eec-114">Type: **string**</span></span>

<span data-ttu-id="c7eec-115">Representación de cadena de la clase [**MSVM \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) que especifica los atributos del nuevo disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="c7eec-115">A string representation of the [**Msvm\_VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) class that specifies the attributes of the new virtual hard disk.</span></span> <span data-ttu-id="c7eec-116">Deben establecerse las propiedades **path**, **Type**, **Format**, **ParentPath**, **blocksize** y **LogicalSectorSize** .</span><span class="sxs-lookup"><span data-stu-id="c7eec-116">The **Path**, **Type**, **Format**, **ParentPath**, **BlockSize**, and **LogicalSectorSize** properties must be set.</span></span> <span data-ttu-id="c7eec-117">La propiedad **ParentPath** puede ser **null** si no se necesita.</span><span class="sxs-lookup"><span data-stu-id="c7eec-117">The **ParentPath** property can be **Null** if it is not needed.</span></span> <span data-ttu-id="c7eec-118">Establezca las propiedades **blocksize** y **LogicalSectorSize** en 0 para usar los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="c7eec-118">Set the **BlockSize** and **LogicalSectorSize** properties to 0 to use the default values.</span></span>

<span data-ttu-id="c7eec-119">Para especificar el formato (VHD o VHDX) del nuevo disco duro virtual, establezca la extensión de la **ruta de acceso** en el valor adecuado (". vhd" o ". VHDX").</span><span class="sxs-lookup"><span data-stu-id="c7eec-119">To specify the format (VHD or VHDX) of the new virtual hard disk, set the extension of the **Path** to the appropriate value (".vhd" or ".vhdx").</span></span> <span data-ttu-id="c7eec-120">La propiedad **Format** debe coincidir con la extensión de nombre de archivo de la **ruta de acceso**.</span><span class="sxs-lookup"><span data-stu-id="c7eec-120">The **Format** property must match the file name extension in the **Path**.</span></span>

<span data-ttu-id="c7eec-121">Se omitirá la propiedad **LogicalSectorSize** .</span><span class="sxs-lookup"><span data-stu-id="c7eec-121">The **LogicalSectorSize** property will be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="c7eec-122">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c7eec-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7eec-123">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="c7eec-123">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="c7eec-124">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c7eec-124">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7eec-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c7eec-125">Return value</span></span>

<span data-ttu-id="c7eec-126">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7eec-126">Type: **uint32**</span></span>

<span data-ttu-id="c7eec-127">Este método puede devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c7eec-127">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c7eec-128">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="c7eec-128">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c7eec-129">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="c7eec-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c7eec-130">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="c7eec-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c7eec-131">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="c7eec-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c7eec-132">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="c7eec-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c7eec-133">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="c7eec-133">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c7eec-134">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="c7eec-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c7eec-135">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="c7eec-135">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c7eec-136">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="c7eec-136">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c7eec-137">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="c7eec-137">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c7eec-138">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="c7eec-138">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c7eec-139">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="c7eec-139">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c7eec-140">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="c7eec-140">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="c7eec-141">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="c7eec-141">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="c7eec-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c7eec-142">Remarks</span></span>

<span data-ttu-id="c7eec-143">Solo se pueden usar los siguientes tipos de discos duros virtuales con este método:</span><span class="sxs-lookup"><span data-stu-id="c7eec-143">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="c7eec-144">VHD fijo</span><span class="sxs-lookup"><span data-stu-id="c7eec-144">Fixed VHD</span></span>
-   <span data-ttu-id="c7eec-145">VHDX fijo</span><span class="sxs-lookup"><span data-stu-id="c7eec-145">Fixed VHDX</span></span>
-   <span data-ttu-id="c7eec-146">VHD dinámico</span><span class="sxs-lookup"><span data-stu-id="c7eec-146">Dynamic VHD</span></span>
-   <span data-ttu-id="c7eec-147">VHDX dinámico</span><span class="sxs-lookup"><span data-stu-id="c7eec-147">Dynamic VHDX</span></span>
-   <span data-ttu-id="c7eec-148">VHD de diferenciación</span><span class="sxs-lookup"><span data-stu-id="c7eec-148">Differencing VHD</span></span>
-   <span data-ttu-id="c7eec-149">VHDX de diferenciación</span><span class="sxs-lookup"><span data-stu-id="c7eec-149">Differencing VHDX</span></span>

<span data-ttu-id="c7eec-150">El acceso a la clase [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="c7eec-150">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c7eec-151">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c7eec-151">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="c7eec-152">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c7eec-152">Examples</span></span>

<span data-ttu-id="c7eec-153">En el siguiente ejemplo de C# se convierte un disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="c7eec-153">The following C# example converts a virtual hard disk.</span></span> <span data-ttu-id="c7eec-154">Las utilidades a las que se hace referencia se pueden encontrar en [utilidades comunes para los ejemplos de virtualización (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="c7eec-154">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public enum VirtualHardDiskType
{
    Fixed = 2,
    Dynamic = 3,
    Differencing = 4
}

public enum VirtualHardDiskFormat
{
    Unknown = 0,
    Vhd = 2,
    Vhdx = 3
}

public static void ConvertVirtualHardDisk(string sourcePath, string destinationPath, VirtualHardDiskType diskType, VirtualHardDiskFormat diskFormat)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementPath path = new ManagementPath()
    {
        Server = null,
        NamespacePath = imageService.Path.Path,
        ClassName = "Msvm_VirtualHardDiskSettingData"
    };

    ManagementClass settingsClass = new ManagementClass(path);
    ManagementObject settingsInstance = settingsClass.CreateInstance();
    settingsInstance["Path"] = destinationPath;
    settingsInstance["Type"] = diskType;
    settingsInstance["Format"] = diskFormat;
    settingsInstance["ParentPath"] = null;
    settingsInstance["MaxInternalSize"] = 0;
    settingsInstance["BlockSize"] = 0;
    settingsInstance["LogicalSectorSize"] = 0;
    settingsInstance["PhysicalSectorSize"] = 0;

    ManagementBaseObject inParams = imageService.GetMethodParameters("ConvertVirtualHardDisk");

    inParams["SourcePath"] = sourcePath;
    inParams["VirtualDiskSettingData"] = settingsInstance.GetText(TextFormat.WmiDtd20);

    ManagementBaseObject outParams = imageService.InvokeMethod("ConvertVirtualHardDisk", inParams, null);
    UInt32 result = (UInt32)outParams["ReturnValue"];
    if (ReturnCode.Completed == result)
    {
        Console.WriteLine("{0} was converted successfully.", inParams["SourcePath"]);
    }
    else if (ReturnCode.Started == result)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was converted successfully.", inParams["SourcePath"]);
        }
        else
        {
            Console.WriteLine("Unable to convert {0}", inParams["SourcePath"]);
        }
    }
    else
    {
        // The method failed.
        Console.WriteLine("ConvertVirtualHardDisk failed with error code {0}.", result);
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="c7eec-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7eec-155">Requirements</span></span>



| <span data-ttu-id="c7eec-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7eec-156">Requirement</span></span> | <span data-ttu-id="c7eec-157">Value</span><span class="sxs-lookup"><span data-stu-id="c7eec-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7eec-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7eec-158">Minimum supported client</span></span><br/> | <span data-ttu-id="c7eec-159">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="c7eec-159">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c7eec-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7eec-160">Minimum supported server</span></span><br/> | <span data-ttu-id="c7eec-161">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="c7eec-161">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c7eec-162">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c7eec-162">Namespace</span></span><br/>                | <span data-ttu-id="c7eec-163">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="c7eec-163">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c7eec-164">MOF</span><span class="sxs-lookup"><span data-stu-id="c7eec-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7eec-165"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7eec-165"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7eec-166">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c7eec-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7eec-167"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c7eec-167"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c7eec-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7eec-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7eec-169">**ConvertVirtualHardDisk (V1)**</span><span class="sxs-lookup"><span data-stu-id="c7eec-169">**ConvertVirtualHardDisk (V1)**</span></span>](/previous-versions/windows/desktop/virtual/convertvirtualharddisk-msvm-imagemanagementservice)
</dt> <dt>

<span data-ttu-id="c7eec-170">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c7eec-170">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c7eec-171">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="c7eec-171">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

