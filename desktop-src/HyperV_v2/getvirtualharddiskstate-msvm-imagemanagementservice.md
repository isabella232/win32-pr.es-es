---
description: Recupera información de estado de un archivo de disco duro virtual.
ms.assetid: 398b098b-dc1a-45e0-abcb-37b4b0a32290
title: Método GetVirtualHardDiskState de la clase Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.GetVirtualHardDiskState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e608078b88415eb683a95e3ba41d81b99014961d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688068"
---
# <a name="getvirtualharddiskstate-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="a0735-103">Método GetVirtualHardDiskState de la \_ clase ImageManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="a0735-103">GetVirtualHardDiskState method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="a0735-104">Recupera información de estado de un archivo de disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="a0735-104">Retrieves state information for a virtual hard disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0735-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a0735-105">Syntax</span></span>


```mof
uint32 GetVirtualHardDiskState(
  [in]  string              Path,
  [out] string              State,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a0735-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a0735-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0735-107">*Ruta de acceso* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a0735-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0735-108">Ruta de acceso completa del archivo de imagen de disco.</span><span class="sxs-lookup"><span data-stu-id="a0735-108">The fully qualified path of the disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="a0735-109">*Estado* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a0735-109">*State* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0735-110">Si se realiza correctamente, recibe una instancia incrustada de la clase [**MSVM \_ VirtualHardDiskState**](msvm-virtualharddiskstate.md) que contiene la información de estado para el disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="a0735-110">If successful, receives an embedded instance of the [**Msvm\_VirtualHardDiskState**](msvm-virtualharddiskstate.md) class that contains the state information for the virtual hard disk.</span></span>

</dd> <dt>

<span data-ttu-id="a0735-111">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a0735-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a0735-112">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a0735-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0735-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a0735-113">Return value</span></span>

<span data-ttu-id="a0735-114">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="a0735-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a0735-115">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="a0735-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a0735-116">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="a0735-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a0735-117">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="a0735-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a0735-118">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="a0735-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a0735-119">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="a0735-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a0735-120">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="a0735-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a0735-121">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="a0735-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a0735-122">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="a0735-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a0735-123">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="a0735-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a0735-124">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="a0735-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a0735-125">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="a0735-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a0735-126">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="a0735-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a0735-127">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="a0735-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="a0735-128">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="a0735-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="a0735-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a0735-129">Remarks</span></span>

<span data-ttu-id="a0735-130">El acceso a la clase [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="a0735-130">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a0735-131">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a0735-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="a0735-132">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a0735-132">Examples</span></span>

<span data-ttu-id="a0735-133">En el siguiente ejemplo de C# se muestra cómo llamar al método **GetVirtualHardDiskState** .</span><span class="sxs-lookup"><span data-stu-id="a0735-133">The following C# example shows how to call the **GetVirtualHardDiskState** method.</span></span> <span data-ttu-id="a0735-134">Las utilidades a las que se hace referencia se pueden encontrar en [utilidades comunes para los ejemplos de virtualización (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="a0735-134">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>


```CSharp
public static void GetVirtualHardDiskState(string vhdPath)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");
    ManagementBaseObject inParams = imageService.GetMethodParameters("GetVirtualHardDiskState");

    inParams["Path"] = vhdPath;
    
    ManagementBaseObject outParams = imageService.InvokeMethod("GetVirtualHardDiskState", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("GetVirtualHardDiskState was successful.");
        }
        else
        {
            Console.WriteLine("GetVirtualHardDiskState was not successful.");
        }
    }
    else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
    {
        string diskStateString = outParams["State"].ToString();
        Utility.PrintEmbeddedInstance(diskStateString);
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a><span data-ttu-id="a0735-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0735-135">Requirements</span></span>



| <span data-ttu-id="a0735-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0735-136">Requirement</span></span> | <span data-ttu-id="a0735-137">Value</span><span class="sxs-lookup"><span data-stu-id="a0735-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0735-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0735-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a0735-139">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="a0735-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a0735-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a0735-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a0735-141">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="a0735-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a0735-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a0735-142">Namespace</span></span><br/>                | <span data-ttu-id="a0735-143">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="a0735-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a0735-144">MOF</span><span class="sxs-lookup"><span data-stu-id="a0735-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0735-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0735-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0735-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a0735-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0735-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a0735-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a0735-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="a0735-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0735-149">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="a0735-149">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

