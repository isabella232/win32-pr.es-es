---
description: Exporta una máquina virtual, o una instantánea de una máquina virtual, a un archivo.
ms.assetid: b88712e4-a1a6-4188-8082-f4973f89018d
title: Método ExportSystemDefinition de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ExportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9f6b6dc5728a4275965ccd482d851601ecd1c6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808378"
---
# <a name="exportsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="644e4-103">Método ExportSystemDefinition de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="644e4-103">ExportSystemDefinition method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="644e4-104">Exporta una máquina virtual, o una instantánea de una máquina virtual, a un archivo.</span><span class="sxs-lookup"><span data-stu-id="644e4-104">Exports a virtual machine, or a snapshot of a virtual machine, to a file.</span></span> <span data-ttu-id="644e4-105">La máquina virtual debe estar en el estado "apagado" o "guardado" que se va a exportar.</span><span class="sxs-lookup"><span data-stu-id="644e4-105">The virtual machine must be in the "powered off" or "saved" state to be exported.</span></span> <span data-ttu-id="644e4-106">La máquina virtual, sus valores de configuración asociados y su configuración de recursos asociada se conservarán en el archivo resultante.</span><span class="sxs-lookup"><span data-stu-id="644e4-106">The virtual machine, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span>

## <a name="syntax"></a><span data-ttu-id="644e4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="644e4-107">Syntax</span></span>


```mof
uint32 ExportSystemDefinition(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ExportDirectory,
  [in]  string                 ExportSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="644e4-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="644e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="644e4-109">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="644e4-109">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="644e4-110">Referencia a un [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual que se va a exportar.</span><span class="sxs-lookup"><span data-stu-id="644e4-110">A reference to a [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) that represents the virtual machine to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="644e4-111">*ExportDirectory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="644e4-111">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="644e4-112">Ruta de acceso completa del directorio al que se va a exportar la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="644e4-112">The fully qualified path of the directory to which the virtual machine is to be exported.</span></span> <span data-ttu-id="644e4-113">Si la propiedad **CreateVmExportSubdirectory** de la [**clase \_ VirtualSystemExportSettingData de MSVM**](msvm-virtualsystemexportsettingdata.md) en el parámetro *ExportSettingData* está establecida en **true**, este directorio se puede reutilizar para exportar varias máquinas virtuales y este método coloca cada definición de máquina virtual en un subdirectorio independiente en esta ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="644e4-113">If the **CreateVmExportSubdirectory** property of the [**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) class in the *ExportSettingData* parameter is set to **True**, then this directory can be reused for exporting multiple virtual machines and this method places each virtual machine definition in a separate subdirectory under this path.</span></span>

</dd> <dt>

<span data-ttu-id="644e4-114">*ExportSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="644e4-114">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="644e4-115">Instancia insertada de la clase [**MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) que representa la configuración de la operación de exportación.</span><span class="sxs-lookup"><span data-stu-id="644e4-115">An embedded instance of the [**Msvm\_VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) class that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="644e4-116">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="644e4-116">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="644e4-117">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="644e4-117">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="644e4-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="644e4-118">Return value</span></span>

<span data-ttu-id="644e4-119">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="644e4-119">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="644e4-120">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="644e4-120">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="644e4-121">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="644e4-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="644e4-122">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="644e4-122">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="644e4-123">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="644e4-123">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="644e4-124">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="644e4-124">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="644e4-125">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="644e4-125">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="644e4-126">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="644e4-126">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="644e4-127">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="644e4-127">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="644e4-128">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="644e4-128">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="644e4-129">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="644e4-129">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="644e4-130">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="644e4-130">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="644e4-131">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="644e4-131">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="644e4-132">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="644e4-132">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="644e4-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="644e4-133">Requirements</span></span>



| <span data-ttu-id="644e4-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="644e4-134">Requirement</span></span> | <span data-ttu-id="644e4-135">Value</span><span class="sxs-lookup"><span data-stu-id="644e4-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="644e4-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="644e4-136">Minimum supported client</span></span><br/> | <span data-ttu-id="644e4-137">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="644e4-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="644e4-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="644e4-138">Minimum supported server</span></span><br/> | <span data-ttu-id="644e4-139">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="644e4-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="644e4-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="644e4-140">Namespace</span></span><br/>                | <span data-ttu-id="644e4-141">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="644e4-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="644e4-142">MOF</span><span class="sxs-lookup"><span data-stu-id="644e4-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="644e4-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="644e4-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="644e4-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="644e4-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="644e4-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="644e4-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="644e4-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="644e4-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="644e4-147">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="644e4-147">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

