---
description: Cambia el tamaño de un disco duro virtual existente.
ms.assetid: 54FDCA3B-E12B-4E68-B7EE-893C9CD97E1A
title: Método ResizeVirtualHardDisk de la clase Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ResizeVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5fcd88a9063dcbe4e19705245b36af33672dfc5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686924"
---
# <a name="resizevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="0adc3-103">Método ResizeVirtualHardDisk de la \_ clase ImageManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="0adc3-103">ResizeVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="0adc3-104">Cambia el tamaño de un disco duro virtual existente.</span><span class="sxs-lookup"><span data-stu-id="0adc3-104">Resizes an existing virtual hard disk.</span></span> <span data-ttu-id="0adc3-105">El disco duro virtual debe estar sin conexión.</span><span class="sxs-lookup"><span data-stu-id="0adc3-105">The virtual hard disk must be offline.</span></span> <span data-ttu-id="0adc3-106">Vea la sección Comentarios para conocer las restricciones de uso de este método.</span><span class="sxs-lookup"><span data-stu-id="0adc3-106">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0adc3-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0adc3-107">Syntax</span></span>


```mof
uint32 ResizeVirtualHardDisk(
  [in]  string              Path,
  [in]  uint64              MaxInternalSize,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0adc3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0adc3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0adc3-109">*Ruta de acceso* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0adc3-109">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0adc3-110">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="0adc3-110">Type: **string**</span></span>

<span data-ttu-id="0adc3-111">Ruta de acceso completa del archivo de disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="0adc3-111">The fully qualified path of the virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="0adc3-112">*MaxInternalSize* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0adc3-112">*MaxInternalSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0adc3-113">Tipo: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0adc3-113">Type: **uint64**</span></span>

<span data-ttu-id="0adc3-114">El tamaño máximo del disco duro virtual tal como lo ve la máquina virtual, en bytes.</span><span class="sxs-lookup"><span data-stu-id="0adc3-114">The maximum size of the virtual hard disk as viewable by the virtual machine, in bytes.</span></span> <span data-ttu-id="0adc3-115">El valor mínimo de *MaxInternalSize* es de *disco* + 512 *-(se* va a duplicar mod 512).</span><span class="sxs-lookup"><span data-stu-id="0adc3-115">*MaxInternalSize* minimum value is *DiskSize* + 512 - (*DiskSize* mod 512).</span></span> <span data-ttu-id="0adc3-116">El tamaño de los *discos* es el tamaño del archivo de disco duro virtual, en bytes.</span><span class="sxs-lookup"><span data-stu-id="0adc3-116">*DiskSize* is the size of the virtual hard disk file, in bytes.</span></span> <span data-ttu-id="0adc3-117">Se devuelve el error InvalidParameter (32773) si el valor de *MaxInternalSize* especificado es menor que el valor mínimo.</span><span class="sxs-lookup"><span data-stu-id="0adc3-117">The InvalidParameter error (32773) is returned if the *MaxInternalSize* value specified is less than the minimum value.</span></span>

</dd> <dt>

<span data-ttu-id="0adc3-118">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0adc3-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0adc3-119">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="0adc3-119">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="0adc3-120">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0adc3-120">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0adc3-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0adc3-121">Return value</span></span>

<span data-ttu-id="0adc3-122">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0adc3-122">Type: **uint32**</span></span>

<span data-ttu-id="0adc3-123">Este método puede devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="0adc3-123">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0adc3-124">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="0adc3-124">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0adc3-125">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="0adc3-125">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0adc3-126">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="0adc3-126">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="0adc3-127">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="0adc3-127">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="0adc3-128">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="0adc3-128">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="0adc3-129">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="0adc3-129">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="0adc3-130">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="0adc3-130">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="0adc3-131">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="0adc3-131">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="0adc3-132">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="0adc3-132">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="0adc3-133">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="0adc3-133">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="0adc3-134">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="0adc3-134">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="0adc3-135">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="0adc3-135">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="0adc3-136">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="0adc3-136">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="0adc3-137">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="0adc3-137">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="0adc3-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0adc3-138">Remarks</span></span>

<span data-ttu-id="0adc3-139">Solo se pueden usar los siguientes tipos de discos duros virtuales con este método cuando se aumenta el tamaño del disco duro virtual:</span><span class="sxs-lookup"><span data-stu-id="0adc3-139">Only the following types of virtual hard disks can be used with this method when the size of the virtual hard disk is being increased:</span></span>

-   <span data-ttu-id="0adc3-140">VHD fijo</span><span class="sxs-lookup"><span data-stu-id="0adc3-140">Fixed VHD</span></span>
-   <span data-ttu-id="0adc3-141">VHDX fijo</span><span class="sxs-lookup"><span data-stu-id="0adc3-141">Fixed VHDX</span></span>
-   <span data-ttu-id="0adc3-142">VHD dinámico</span><span class="sxs-lookup"><span data-stu-id="0adc3-142">Dynamic VHD</span></span>
-   <span data-ttu-id="0adc3-143">VHDX dinámico</span><span class="sxs-lookup"><span data-stu-id="0adc3-143">Dynamic VHDX</span></span>
-   <span data-ttu-id="0adc3-144">VHDX de diferenciación</span><span class="sxs-lookup"><span data-stu-id="0adc3-144">Differencing VHDX</span></span>

<span data-ttu-id="0adc3-145">Solo se pueden usar los siguientes tipos de discos duros virtuales con este método cuando se reduce el tamaño del disco duro virtual:</span><span class="sxs-lookup"><span data-stu-id="0adc3-145">Only the following types of virtual hard disks can be used with this method when the size of the virtual hard disk is being decreased:</span></span>

-   <span data-ttu-id="0adc3-146">VHDX fijo</span><span class="sxs-lookup"><span data-stu-id="0adc3-146">Fixed VHDX</span></span>
-   <span data-ttu-id="0adc3-147">VHDX dinámico</span><span class="sxs-lookup"><span data-stu-id="0adc3-147">Dynamic VHDX</span></span>
-   <span data-ttu-id="0adc3-148">VHDX de diferenciación</span><span class="sxs-lookup"><span data-stu-id="0adc3-148">Differencing VHDX</span></span>

<span data-ttu-id="0adc3-149">El acceso a la clase [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="0adc3-149">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0adc3-150">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="0adc3-150">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="0adc3-151">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="0adc3-151">Examples</span></span>

<span data-ttu-id="0adc3-152">En el siguiente ejemplo de C# se expande un archivo de disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="0adc3-152">The following C# example expands a virtual hard disk file.</span></span> <span data-ttu-id="0adc3-153">Las utilidades a las que se hace referencia se pueden encontrar en [utilidades comunes para los ejemplos de virtualización (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="0adc3-153">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
const UInt64 size1G = 0x40000000;

public static void ResizeVirtualHardDisk(string path, UInt64 maxInternalSize)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("ResizeVirtualHardDisk");
    inParams["Path"] = path;
    inParams["MaxInternalSize"] = maxInternalSize * size1G;
    ManagementBaseObject outParams = imageService.InvokeMethod("ResizeVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was resized successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to resize {0}", inParams["Path"]);
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="0adc3-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0adc3-154">Requirements</span></span>



| <span data-ttu-id="0adc3-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="0adc3-155">Requirement</span></span> | <span data-ttu-id="0adc3-156">Value</span><span class="sxs-lookup"><span data-stu-id="0adc3-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0adc3-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0adc3-157">Minimum supported client</span></span><br/> | <span data-ttu-id="0adc3-158">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="0adc3-158">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0adc3-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0adc3-159">Minimum supported server</span></span><br/> | <span data-ttu-id="0adc3-160">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="0adc3-160">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0adc3-161">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0adc3-161">Namespace</span></span><br/>                | <span data-ttu-id="0adc3-162">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="0adc3-162">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0adc3-163">MOF</span><span class="sxs-lookup"><span data-stu-id="0adc3-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0adc3-164"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0adc3-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0adc3-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0adc3-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0adc3-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0adc3-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0adc3-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="0adc3-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="0adc3-168">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0adc3-168">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0adc3-169">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="0adc3-169">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

