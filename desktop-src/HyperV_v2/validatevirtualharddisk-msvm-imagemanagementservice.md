---
description: Determina si un archivo de disco duro virtual es válido.
ms.assetid: 5F7C99DB-0C81-46D5-A965-B6D87647ABF6
title: Método ValidateVirtualHardDisk de la clase Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ValidateVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 50c00dc4336e3e85b7db8ffd334de8868054c997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668419"
---
# <a name="validatevirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="9aa4b-103">Método ValidateVirtualHardDisk de la \_ clase ImageManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="9aa4b-103">ValidateVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="9aa4b-104">Determina si un archivo de disco duro virtual es válido.</span><span class="sxs-lookup"><span data-stu-id="9aa4b-104">Determines whether a virtual hard disk file is valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aa4b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9aa4b-105">Syntax</span></span>


```mof
uint32 ValidateVirtualHardDisk(
  [in]  string              Path,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="9aa4b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9aa4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aa4b-107">*Ruta de acceso* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9aa4b-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa4b-108">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="9aa4b-108">Type: **string**</span></span>

<span data-ttu-id="9aa4b-109">Ruta de acceso completa que especifica la ubicación del archivo de disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="9aa4b-109">A fully qualified path that specifies the location of the virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="9aa4b-110">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="9aa4b-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa4b-111">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="9aa4b-111">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="9aa4b-112">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9aa4b-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aa4b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9aa4b-113">Return value</span></span>

<span data-ttu-id="9aa4b-114">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9aa4b-114">Type: **uint32**</span></span>

<span data-ttu-id="9aa4b-115">Este método puede devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="9aa4b-115">This method can return one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="9aa4b-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="9aa4b-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="9aa4b-117">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="9aa4b-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="9aa4b-118">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="9aa4b-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="9aa4b-119">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="9aa4b-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="9aa4b-120">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="9aa4b-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="9aa4b-121">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="9aa4b-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="9aa4b-122">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="9aa4b-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="9aa4b-123">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="9aa4b-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="9aa4b-124">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="9aa4b-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="9aa4b-125">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="9aa4b-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="9aa4b-126">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="9aa4b-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="9aa4b-127">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="9aa4b-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="9aa4b-128">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="9aa4b-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="9aa4b-129">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="9aa4b-129">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="9aa4b-130">Se **detectó un ciclo de cadena de diferenciación de VHD** (32787)</span><span class="sxs-lookup"><span data-stu-id="9aa4b-130">**Vhd differencing chain cycle detected** (32787)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="9aa4b-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9aa4b-131">Remarks</span></span>

<span data-ttu-id="9aa4b-132">Si el disco duro virtual es un disco de diferenciación, se abre toda la cadena de discos virtuales.</span><span class="sxs-lookup"><span data-stu-id="9aa4b-132">If the virtual hard disk is a differencing disk, the entire virtual disk chain is opened.</span></span> <span data-ttu-id="9aa4b-133">Si el vínculo está roto en la cadena de disco, se devuelve un objeto de trabajo con el error correspondiente inicializado y las propiedades secundaria y primaria se inicializan en la ubicación donde se rompe el vínculo.</span><span class="sxs-lookup"><span data-stu-id="9aa4b-133">If the link is broken in the disk chain, a job object is returned with the appropriate error initialized and the child and parent properties are initialized to the location where the link is broken.</span></span>

<span data-ttu-id="9aa4b-134">El acceso a la clase [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="9aa4b-134">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9aa4b-135">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="9aa4b-135">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="9aa4b-136">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9aa4b-136">Examples</span></span>

<span data-ttu-id="9aa4b-137">En el siguiente ejemplo de C# se valida una imagen de disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="9aa4b-137">The following C# example validates a virtual hard disk image.</span></span> <span data-ttu-id="9aa4b-138">Las utilidades a las que se hace referencia se pueden encontrar en [utilidades comunes para los ejemplos de virtualización (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="9aa4b-138">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void ValidateVirtualHardDisk(string vhdPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("ValidateVirtualHardDisk");
    inParams["Path"] = vhdPath;
    ManagementBaseObject outParams = imageService.InvokeMethod("ValidateVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} is a valid virtual hard disk.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to validate {0}", inParams["Path"]);
        }
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="9aa4b-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9aa4b-139">Requirements</span></span>



| <span data-ttu-id="9aa4b-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="9aa4b-140">Requirement</span></span> | <span data-ttu-id="9aa4b-141">Value</span><span class="sxs-lookup"><span data-stu-id="9aa4b-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9aa4b-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9aa4b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="9aa4b-143">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="9aa4b-143">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9aa4b-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9aa4b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="9aa4b-145">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="9aa4b-145">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9aa4b-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9aa4b-146">Namespace</span></span><br/>                | <span data-ttu-id="9aa4b-147">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="9aa4b-147">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9aa4b-148">MOF</span><span class="sxs-lookup"><span data-stu-id="9aa4b-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9aa4b-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9aa4b-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9aa4b-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9aa4b-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9aa4b-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9aa4b-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9aa4b-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="9aa4b-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aa4b-153">**ValidateVirtualHardDisk (V1)**</span><span class="sxs-lookup"><span data-stu-id="9aa4b-153">**ValidateVirtualHardDisk (V1)**</span></span>](/previous-versions/windows/desktop/virtual/validatevirtualharddisk-msvm-imagemanagementservice)
</dt> <dt>

<span data-ttu-id="9aa4b-154">[**\_CONCRETEJOB CIM**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9aa4b-154">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="9aa4b-155">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="9aa4b-155">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

