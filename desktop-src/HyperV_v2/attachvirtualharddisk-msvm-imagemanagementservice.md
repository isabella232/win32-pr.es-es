---
description: Conecta un archivo de disco duro virtual en modo de bucle invertido.
ms.assetid: 54bd8e67-e309-4bf3-94bd-e29bc3300a3d
title: Método AttachVirtualHardDisk de la clase Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.AttachVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0f8a22ac377eb96fdc01fa54877cdc6c12619c41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909838"
---
# <a name="attachvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="2e01f-103">Método AttachVirtualHardDisk de la \_ clase ImageManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="2e01f-103">AttachVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="2e01f-104">Conecta un archivo de disco duro virtual en modo de bucle invertido.</span><span class="sxs-lookup"><span data-stu-id="2e01f-104">Attaches a virtual hard disk file in loopback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e01f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2e01f-105">Syntax</span></span>


```mof
uint32 AttachVirtualHardDisk(
  [in]  string              Path,
  [in]  boolean             AssignDriveLetter,
  [in]  boolean             ReadOnly,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2e01f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2e01f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e01f-107">*Ruta de acceso* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2e01f-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e01f-108">Ruta de acceso completa que especifica la ubicación del archivo de disco duro virtual que se va a adjuntar.</span><span class="sxs-lookup"><span data-stu-id="2e01f-108">A fully qualified path that specifies the location of the virtual hard disk file to attach.</span></span>

</dd> <dt>

<span data-ttu-id="2e01f-109">*AssignDriveLetter* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2e01f-109">*AssignDriveLetter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e01f-110">Indica si las letras de unidad se asignan a los volúmenes del disco.</span><span class="sxs-lookup"><span data-stu-id="2e01f-110">Indicates if drive letters are assigned to the disk's volumes.</span></span>

</dd> <dt>

<span data-ttu-id="2e01f-111">*Solo lectura* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2e01f-111">*ReadOnly* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e01f-112">Indica si el disco duro conectado debe ser de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2e01f-112">Indicates if the attached hard disk should be read-only.</span></span>

</dd> <dt>

<span data-ttu-id="2e01f-113">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2e01f-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e01f-114">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2e01f-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e01f-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2e01f-115">Return value</span></span>

<span data-ttu-id="2e01f-116">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2e01f-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2e01f-117">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="2e01f-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2e01f-118">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="2e01f-118">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2e01f-119">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="2e01f-119">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="2e01f-120">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="2e01f-120">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="2e01f-121">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="2e01f-121">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="2e01f-122">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="2e01f-122">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="2e01f-123">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="2e01f-123">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="2e01f-124">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="2e01f-124">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="2e01f-125">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="2e01f-125">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="2e01f-126">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="2e01f-126">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="2e01f-127">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="2e01f-127">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="2e01f-128">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="2e01f-128">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="2e01f-129">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="2e01f-129">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="2e01f-130">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="2e01f-130">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="2e01f-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2e01f-131">Remarks</span></span>

<span data-ttu-id="2e01f-132">Para desasociar el disco duro virtual, use el método [**MSVM \_ MountedStorageImage. DetachVirtualHardDisk**](detachvirtualharddisk-msvm-mountedstorageimage.md) .</span><span class="sxs-lookup"><span data-stu-id="2e01f-132">To detach the virtual hard disk, use the [**Msvm\_MountedStorageImage.DetachVirtualHardDisk**](detachvirtualharddisk-msvm-mountedstorageimage.md) method.</span></span>

<span data-ttu-id="2e01f-133">El acceso a la clase [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="2e01f-133">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="2e01f-134">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="2e01f-134">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="2e01f-135">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2e01f-135">Examples</span></span>

<span data-ttu-id="2e01f-136">En el siguiente ejemplo de C# se muestra cómo adjuntar un archivo de disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="2e01f-136">The following C# example shows how to attach a virtual hard disk file.</span></span> <span data-ttu-id="2e01f-137">Las utilidades a las que se hace referencia se pueden encontrar en [utilidades comunes para los ejemplos de virtualización (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="2e01f-137">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void AttachVirtualHardDisk(string path)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("AttachVirtualHardDisk");
    inParams["Path"] = path;
    inParams["AssignDriveLetter"] = true;
    inParams["ReadOnly"] = false;
    ManagementBaseObject outParams = imageService.InvokeMethod("AttachVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was attached successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to attach {0}", inParams["Path"]);
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="2e01f-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e01f-138">Requirements</span></span>



| <span data-ttu-id="2e01f-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e01f-139">Requirement</span></span> | <span data-ttu-id="2e01f-140">Value</span><span class="sxs-lookup"><span data-stu-id="2e01f-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e01f-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e01f-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2e01f-142">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="2e01f-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2e01f-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2e01f-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2e01f-144">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="2e01f-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2e01f-145">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2e01f-145">Namespace</span></span><br/>                | <span data-ttu-id="2e01f-146">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="2e01f-146">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2e01f-147">MOF</span><span class="sxs-lookup"><span data-stu-id="2e01f-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e01f-148"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e01f-148"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e01f-149">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2e01f-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e01f-150"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2e01f-150"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2e01f-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="2e01f-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e01f-152">**MSVM \_ MountedStorageImage. DetachVirtualHardDisk**</span><span class="sxs-lookup"><span data-stu-id="2e01f-152">**Msvm\_MountedStorageImage.DetachVirtualHardDisk**</span></span>](detachvirtualharddisk-msvm-mountedstorageimage.md)
</dt> <dt>

[<span data-ttu-id="2e01f-153">**Montaje (V1)**</span><span class="sxs-lookup"><span data-stu-id="2e01f-153">**Mount (V1)**</span></span>](/previous-versions/windows/desktop/virtual/mount-msvm-imagemanagementservice)
</dt> <dt>

[<span data-ttu-id="2e01f-154">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="2e01f-154">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

