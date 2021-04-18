---
description: Compacta un archivo de disco duro virtual.
ms.assetid: 1E64BD91-6FE6-4658-9EBF-615FC705B920
title: Método CompactVirtualHardDisk de la clase Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.CompactVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8e8c148e51105d8c78021b58366e2f2df3913f57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687855"
---
# <a name="compactvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="ba99b-103">Método CompactVirtualHardDisk de la \_ clase ImageManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="ba99b-103">CompactVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="ba99b-104">Compacta un archivo de disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="ba99b-104">Compacts a virtual hard disk file.</span></span> <span data-ttu-id="ba99b-105">La compactación es el proceso de liberar partes no utilizadas del disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="ba99b-105">Compacting is the process of freeing unused portions of the virtual hard disk.</span></span> <span data-ttu-id="ba99b-106">El disco duro virtual no se monta automáticamente.</span><span class="sxs-lookup"><span data-stu-id="ba99b-106">The virtual hard disk is not automatically mounted.</span></span> <span data-ttu-id="ba99b-107">Vea la sección Comentarios para conocer las restricciones de uso de este método.</span><span class="sxs-lookup"><span data-stu-id="ba99b-107">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba99b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba99b-108">Syntax</span></span>


```mof
uint32 CompactVirtualHardDisk(
  [in]  string              Path,
  [in]  uint16              Mode,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ba99b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ba99b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba99b-110">*Ruta de acceso* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ba99b-110">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba99b-111">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="ba99b-111">Type: **string**</span></span>

<span data-ttu-id="ba99b-112">Ruta de acceso completa que especifica la ubicación del archivo de combinación.</span><span class="sxs-lookup"><span data-stu-id="ba99b-112">A fully qualified path that specifies the location of the merging file.</span></span>

</dd> <dt>

<span data-ttu-id="ba99b-113">*Modo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="ba99b-113">*Mode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba99b-114">Tipo: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ba99b-114">Type: **uint16**</span></span>

<span data-ttu-id="ba99b-115">Especifica el modo de la operación de compactación.</span><span class="sxs-lookup"><span data-stu-id="ba99b-115">Specifies the mode for the compact operation.</span></span> <span data-ttu-id="ba99b-116">Debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="ba99b-116">This must be one of the following values.</span></span>

<dt>

<span id="Full"></span><span id="full"></span><span id="FULL"></span>

<span data-ttu-id="ba99b-117">**Full** (0)</span><span class="sxs-lookup"><span data-stu-id="ba99b-117">**Full** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Quick"></span><span id="quick"></span><span id="QUICK"></span>

<span data-ttu-id="ba99b-118">**Rápido** (1)</span><span class="sxs-lookup"><span data-stu-id="ba99b-118">**Quick** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Retrim"></span><span id="retrim"></span><span id="RETRIM"></span>

<span data-ttu-id="ba99b-119">**Retrim** (2)</span><span class="sxs-lookup"><span data-stu-id="ba99b-119">**Retrim** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Pretrimmed"></span><span id="pretrimmed"></span><span id="PRETRIMMED"></span>

<span data-ttu-id="ba99b-120">**Recortado** (3)</span><span class="sxs-lookup"><span data-stu-id="ba99b-120">**Pretrimmed** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Prezeroed"></span><span id="prezeroed"></span><span id="PREZEROED"></span>

<span data-ttu-id="ba99b-121">**Precero** (4)</span><span class="sxs-lookup"><span data-stu-id="ba99b-121">**Prezeroed** (4)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="ba99b-122">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ba99b-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba99b-123">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="ba99b-123">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="ba99b-124">Referencia al trabajo (puede ser **null** si se ha completado la tarea).</span><span class="sxs-lookup"><span data-stu-id="ba99b-124">A reference to the job (can be **Null** if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba99b-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ba99b-125">Return value</span></span>

<span data-ttu-id="ba99b-126">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ba99b-126">Type: **uint32**</span></span>

<span data-ttu-id="ba99b-127">Este método puede devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="ba99b-127">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ba99b-128">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="ba99b-128">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ba99b-129">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="ba99b-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ba99b-130">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="ba99b-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ba99b-131">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="ba99b-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ba99b-132">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="ba99b-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ba99b-133">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="ba99b-133">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ba99b-134">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="ba99b-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ba99b-135">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="ba99b-135">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ba99b-136">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="ba99b-136">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ba99b-137">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="ba99b-137">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ba99b-138">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="ba99b-138">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ba99b-139">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="ba99b-139">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ba99b-140">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="ba99b-140">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="ba99b-141">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="ba99b-141">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="ba99b-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ba99b-142">Remarks</span></span>

<span data-ttu-id="ba99b-143">Solo se pueden usar los siguientes tipos de discos duros virtuales con este método:</span><span class="sxs-lookup"><span data-stu-id="ba99b-143">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="ba99b-144">VHDX fijo</span><span class="sxs-lookup"><span data-stu-id="ba99b-144">Fixed VHDX</span></span>
-   <span data-ttu-id="ba99b-145">VHD dinámico</span><span class="sxs-lookup"><span data-stu-id="ba99b-145">Dynamic VHD</span></span>
-   <span data-ttu-id="ba99b-146">VHDX dinámico</span><span class="sxs-lookup"><span data-stu-id="ba99b-146">Dynamic VHDX</span></span>
-   <span data-ttu-id="ba99b-147">VHD de diferenciación</span><span class="sxs-lookup"><span data-stu-id="ba99b-147">Differencing VHD</span></span>
-   <span data-ttu-id="ba99b-148">VHDX de diferenciación</span><span class="sxs-lookup"><span data-stu-id="ba99b-148">Differencing VHDX</span></span>

<span data-ttu-id="ba99b-149">El acceso a la clase [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="ba99b-149">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ba99b-150">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ba99b-150">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="ba99b-151">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ba99b-151">Examples</span></span>

<span data-ttu-id="ba99b-152">En el siguiente ejemplo de C# se compacta un disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="ba99b-152">The following C# example compacts a virtual hard disk.</span></span> <span data-ttu-id="ba99b-153">Las utilidades a las que se hace referencia se pueden encontrar en [utilidades comunes para los ejemplos de virtualización (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="ba99b-153">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public enum VirtualHardDiskCompactMode
{
    Full = 0,
    Quick = 1,
    Retrim = 2,
    Pretrimmed = 3,
    Prezeroed = 4
}

public static void CompactVirtualHardDisk(string vhdPath, VirtualHardDiskCompactMode compactMode)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("CompactVirtualHardDisk");
    inParams["Path"] = vhdPath;
    inParams["Mode"] = compactMode;
    ManagementBaseObject outParams = imageService.InvokeMethod("CompactVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was compacted successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to compact {0}", inParams["Path"]);
        }
    }
    else
    {
        Console.WriteLine("Compact {0} returned error {1}", inParams["Path"], outParams["ReturnValue"]);
    }

    inParams.Dispose();
    outParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="ba99b-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba99b-154">Requirements</span></span>



| <span data-ttu-id="ba99b-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba99b-155">Requirement</span></span> | <span data-ttu-id="ba99b-156">Value</span><span class="sxs-lookup"><span data-stu-id="ba99b-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba99b-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba99b-157">Minimum supported client</span></span><br/> | <span data-ttu-id="ba99b-158">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="ba99b-158">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ba99b-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba99b-159">Minimum supported server</span></span><br/> | <span data-ttu-id="ba99b-160">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="ba99b-160">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ba99b-161">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ba99b-161">Namespace</span></span><br/>                | <span data-ttu-id="ba99b-162">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ba99b-162">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ba99b-163">MOF</span><span class="sxs-lookup"><span data-stu-id="ba99b-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba99b-164"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba99b-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba99b-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ba99b-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba99b-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ba99b-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ba99b-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba99b-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="ba99b-168">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ba99b-168">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ba99b-169">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="ba99b-169">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

