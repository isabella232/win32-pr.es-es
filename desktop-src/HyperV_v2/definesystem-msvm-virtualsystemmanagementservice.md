---
description: Crea una nueva instancia de máquina virtual.
ms.assetid: 15BC967D-F392-45A6-ACF6-5C2F2334AAE6
title: Método DefineSystem de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 965d24313607a767d546503d005a6493234b2f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277993"
---
# <a name="definesystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="34139-103">Método DefineSystem de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="34139-103">DefineSystem method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="34139-104">Crea una nueva instancia de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="34139-104">Creates a new virtual machine instance.</span></span> <span data-ttu-id="34139-105">Las propiedades que no se especifican se rellenarán con los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="34139-105">Properties that are not specified will be populated with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="34139-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="34139-106">Syntax</span></span>


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="34139-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="34139-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34139-108">*Configuración* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="34139-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34139-109">Tipo: **String**</span><span class="sxs-lookup"><span data-stu-id="34139-109">Type: **string**</span></span>

<span data-ttu-id="34139-110">Instancia insertada de la clase [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que se usa para definir los atributos de la máquina virtual que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="34139-110">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that is used to define the attributes of the virtual machine to be created.</span></span> <span data-ttu-id="34139-111">Este parámetro es necesario.</span><span class="sxs-lookup"><span data-stu-id="34139-111">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="34139-112">*ResourceSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="34139-112">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34139-113">Tipo: **String \[ \]**</span><span class="sxs-lookup"><span data-stu-id="34139-113">Type: **string\[\]**</span></span>

<span data-ttu-id="34139-114">Varias instancias incrustadas de la clase [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) (o clases derivadas de ella).</span><span class="sxs-lookup"><span data-stu-id="34139-114">A number of embedded instances of the [**Msvm\_ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) class (or derived classes thereof).</span></span> <span data-ttu-id="34139-115">Juntas, estas instancias describen los recursos virtuales de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="34139-115">Together these instances describe the virtual resources of the virtual machine.</span></span> <span data-ttu-id="34139-116">Se creará un conjunto de dispositivos predeterminado para la máquina virtual, independientemente de si este parámetro está establecido.</span><span class="sxs-lookup"><span data-stu-id="34139-116">A default set of devices will be created for the virtual machine regardless of whether this parameter is set.</span></span> <span data-ttu-id="34139-117">Por ejemplo, el procesador y la memoria se crean y configuran automáticamente con los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="34139-117">For example, processor and memory are automatically created and configured with default values.</span></span>

</dd> <dt>

<span data-ttu-id="34139-118">*ReferenceConfiguration* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="34139-118">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34139-119">Tipo: **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="34139-119">Type: **CIM\_VirtualSystemSettingData**</span></span>

<span data-ttu-id="34139-120">Una referencia a una instancia de la clase [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que es el objeto de nivel superior de una configuración de máquina virtual de referencia.</span><span class="sxs-lookup"><span data-stu-id="34139-120">A reference to an instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that is the top level object of a reference virtual machine configuration.</span></span> <span data-ttu-id="34139-121">La configuración de referencia se utiliza para complementar la configuración de la nueva máquina virtual si los parámetros *configuración* y *ResourceSettings* no proporcionaron la información correspondiente.</span><span class="sxs-lookup"><span data-stu-id="34139-121">The reference configuration is used to complement the configuration of the new virtual machine if the *SystemSettings* and *ResourceSettings* parameters did not provide respective information.</span></span>

</dd> <dt>

<span data-ttu-id="34139-122">*ResultingSystem* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="34139-122">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34139-123">Tipo: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="34139-123">Type: **CIM\_ComputerSystem**</span></span>

<span data-ttu-id="34139-124">Una referencia a una instancia de la clase de [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual recién creada.</span><span class="sxs-lookup"><span data-stu-id="34139-124">A reference to an instance of the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class that represents the newly created virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="34139-125">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="34139-125">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="34139-126">Tipo: **CIM \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="34139-126">Type: **CIM\_ConcreteJob**</span></span>

<span data-ttu-id="34139-127">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="34139-127">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34139-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34139-128">Return value</span></span>

<span data-ttu-id="34139-129">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="34139-129">Type: **uint32**</span></span>

<span data-ttu-id="34139-130">Si este método se ejecuta sincrónicamente, devuelve 0 si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="34139-130">If this method is executed synchronously, it returns 0 if it succeeds.</span></span> <span data-ttu-id="34139-131">Si este método se ejecuta de forma asincrónica, devuelve 4096 y el parámetro de salida del *trabajo* se puede usar para realizar el seguimiento del progreso de la operación asincrónica.</span><span class="sxs-lookup"><span data-stu-id="34139-131">If this method is executed asynchronously, it returns 4096 and the *Job* output parameter can be used to track the progress of the asynchronous operation.</span></span> <span data-ttu-id="34139-132">Cualquier otro valor devuelto indica un error.</span><span class="sxs-lookup"><span data-stu-id="34139-132">Any other return value indicates an error.</span></span>

<dl> <dt>

<span data-ttu-id="34139-133">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="34139-133">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="34139-134">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="34139-134">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="34139-135">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="34139-135">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="34139-136">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="34139-136">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="34139-137">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="34139-137">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="34139-138">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="34139-138">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="34139-139">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="34139-139">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="34139-140">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="34139-140">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="34139-141">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="34139-141">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="34139-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="34139-142">Remarks</span></span>

<span data-ttu-id="34139-143">El acceso a la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="34139-143">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="34139-144">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="34139-144">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="34139-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34139-145">Requirements</span></span>



| <span data-ttu-id="34139-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="34139-146">Requirement</span></span> | <span data-ttu-id="34139-147">Value</span><span class="sxs-lookup"><span data-stu-id="34139-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34139-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34139-148">Minimum supported client</span></span><br/> | <span data-ttu-id="34139-149">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="34139-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="34139-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="34139-150">Minimum supported server</span></span><br/> | <span data-ttu-id="34139-151">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="34139-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="34139-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="34139-152">Namespace</span></span><br/>                | <span data-ttu-id="34139-153">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="34139-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="34139-154">MOF</span><span class="sxs-lookup"><span data-stu-id="34139-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="34139-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="34139-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="34139-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="34139-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="34139-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="34139-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="34139-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="34139-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34139-159">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="34139-159">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

