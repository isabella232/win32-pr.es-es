---
description: Combina un disco duro virtual secundario en una cadena de diferenciación con uno o varios discos duros virtuales principales de la cadena.
ms.assetid: 10633176-F0C3-4CA0-8E7B-2B11FF93B0EA
title: Método MergeVirtualHardDisk de la clase Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.MergeVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 347e11d55357a8b3366aeb09badc53c1afad9e01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546243"
---
# <a name="mergevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="0784d-103">Método MergeVirtualHardDisk de la \_ clase ImageManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="0784d-103">MergeVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="0784d-104">Combina un disco duro virtual secundario en una cadena de diferenciación con uno o varios discos duros virtuales principales de la cadena.</span><span class="sxs-lookup"><span data-stu-id="0784d-104">Merges a child virtual hard disk in a differencing chain with one or more parent virtual hard disks in the chain.</span></span> <span data-ttu-id="0784d-105">Vea la sección Comentarios para conocer las restricciones de uso de este método.</span><span class="sxs-lookup"><span data-stu-id="0784d-105">See Remarks for usage restrictions for this method.</span></span>

<span data-ttu-id="0784d-106">Si el usuario que ejecuta esta función no tiene permiso para actualizar las máquinas virtuales, se producirá un error en esta función.</span><span class="sxs-lookup"><span data-stu-id="0784d-106">If the user executing this function does not have permission to update the virtual machines, then this function will fail.</span></span>

## <a name="syntax"></a><span data-ttu-id="0784d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0784d-107">Syntax</span></span>


```mof
uint32 MergeVirtualHardDisk(
  [in]  string              SourcePath,
  [in]  string              DestinationPath,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0784d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0784d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0784d-109">*SourcePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0784d-109">*SourcePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0784d-110">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="0784d-110">Type: **string**</span></span>

<span data-ttu-id="0784d-111">Ruta de acceso completa que especifica la ubicación del archivo de disco duro virtual que se va a combinar.</span><span class="sxs-lookup"><span data-stu-id="0784d-111">A fully qualified path that specifies the location of the virtual hard disk file to merge.</span></span>

</dd> <dt>

<span data-ttu-id="0784d-112">*DestinationPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0784d-112">*DestinationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0784d-113">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="0784d-113">Type: **string**</span></span>

<span data-ttu-id="0784d-114">Ruta de acceso completa que especifica la ubicación del archivo de disco duro virtual primario en el que se van a combinar los datos.</span><span class="sxs-lookup"><span data-stu-id="0784d-114">A fully qualified path that specifies the location of the parent virtual hard disk file into which data is to be merged.</span></span> <span data-ttu-id="0784d-115">Podría ser el disco duro virtual primario inmediato del archivo de combinación o la imagen de disco principal unos pocos niveles hacia arriba en la cadena de diferenciación.</span><span class="sxs-lookup"><span data-stu-id="0784d-115">This could be the immediate parent virtual hard disk of the merging file or the parent disk image a few levels up the differencing chain.</span></span>

</dd> <dt>

<span data-ttu-id="0784d-116">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0784d-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0784d-117">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="0784d-117">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="0784d-118">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0784d-118">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0784d-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0784d-119">Return value</span></span>

<span data-ttu-id="0784d-120">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0784d-120">Type: **uint32**</span></span>

<span data-ttu-id="0784d-121">Este método puede devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="0784d-121">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0784d-122">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="0784d-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0784d-123">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="0784d-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0784d-124">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="0784d-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="0784d-125">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="0784d-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="0784d-126">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="0784d-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="0784d-127">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="0784d-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="0784d-128">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="0784d-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="0784d-129">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="0784d-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="0784d-130">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="0784d-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="0784d-131">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="0784d-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="0784d-132">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="0784d-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="0784d-133">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="0784d-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="0784d-134">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="0784d-134">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="0784d-135">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="0784d-135">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="0784d-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0784d-136">Remarks</span></span>

<span data-ttu-id="0784d-137">El disco duro virtual secundario debe estar sin conexión.</span><span class="sxs-lookup"><span data-stu-id="0784d-137">The child virtual hard disk must be offline.</span></span>

<span data-ttu-id="0784d-138">Solo se pueden usar los siguientes tipos de discos duros virtuales con este método:</span><span class="sxs-lookup"><span data-stu-id="0784d-138">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="0784d-139">VHD de diferenciación</span><span class="sxs-lookup"><span data-stu-id="0784d-139">Differencing VHD</span></span>
-   <span data-ttu-id="0784d-140">VHDX de diferenciación</span><span class="sxs-lookup"><span data-stu-id="0784d-140">Differencing VHDX</span></span>

<span data-ttu-id="0784d-141">El acceso a la clase [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="0784d-141">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0784d-142">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="0784d-142">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="0784d-143">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0784d-143">Examples</span></span>

<span data-ttu-id="0784d-144">En el siguiente ejemplo de C# se expande un archivo de disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="0784d-144">The following C# example expands a virtual hard disk file.</span></span> <span data-ttu-id="0784d-145">Las utilidades a las que se hace referencia se pueden encontrar en [utilidades comunes para los ejemplos de virtualización (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="0784d-145">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
// Merges a VHD into a parent VHD.
// ChildPath: The path to the VHD to merge.</param>
// ParentPath: The path to the parent into which to merge.</param>
public static void MergeVirtualHardDisk(string ChildPath, string ParentPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("MergeVirtualHardDisk");

    inParams["SourcePath"] = ChildPath;
    inParams["DestinationPath"] = ParentPath;

    ManagementBaseObject outParams = imageService.InvokeMethod("MergeVirtualHardDisk", inParams, null);

    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("MergeVirtualHardDisk succeeded.");
        }
        else
        {
            Console.WriteLine("MergeVirtualHardDisk failed.");
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="0784d-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0784d-146">Requirements</span></span>



| <span data-ttu-id="0784d-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="0784d-147">Requirement</span></span> | <span data-ttu-id="0784d-148">Value</span><span class="sxs-lookup"><span data-stu-id="0784d-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0784d-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0784d-149">Minimum supported client</span></span><br/> | <span data-ttu-id="0784d-150">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="0784d-150">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0784d-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0784d-151">Minimum supported server</span></span><br/> | <span data-ttu-id="0784d-152">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="0784d-152">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0784d-153">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0784d-153">Namespace</span></span><br/>                | <span data-ttu-id="0784d-154">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="0784d-154">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0784d-155">MOF</span><span class="sxs-lookup"><span data-stu-id="0784d-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0784d-156"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0784d-156"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0784d-157">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0784d-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0784d-158"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0784d-158"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0784d-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="0784d-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="0784d-160">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0784d-160">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0784d-161">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="0784d-161">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

