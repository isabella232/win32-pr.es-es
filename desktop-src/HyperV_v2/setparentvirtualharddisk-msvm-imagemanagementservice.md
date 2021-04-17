---
description: Actualiza el elemento primario de los archivos de disco duro virtual de hoja y secundario especificados.
ms.assetid: 5ad41218-bcfd-449a-a66e-2096a1d96bf5
title: Método SetParentVirtualHardDisk de la clase Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetParentVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f1d14d3b2ee19a9768e1ee9ed9333a452153cc9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687462"
---
# <a name="setparentvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="295d5-103">Método SetParentVirtualHardDisk de la \_ clase ImageManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="295d5-103">SetParentVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="295d5-104">Actualiza el elemento primario de los archivos de disco duro virtual de hoja y secundario especificados.</span><span class="sxs-lookup"><span data-stu-id="295d5-104">Updates the parent for the specified leaf and child virtual hard disk files.</span></span> <span data-ttu-id="295d5-105">Vea la sección Comentarios para conocer las restricciones de uso de este método.</span><span class="sxs-lookup"><span data-stu-id="295d5-105">See Remarks for usage restrictions for this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="295d5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="295d5-106">Syntax</span></span>


```mof
uint32 SetParentVirtualHardDisk(
  [in]  string              ChildPath,
  [in]  string              ParentPath,
  [in]  string              LeafPath,
  [in]  boolean             IgnoreIDMismatch,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="295d5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="295d5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="295d5-108">*ChildPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="295d5-108">*ChildPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="295d5-109">Ruta de acceso completa que especifica la ubicación del archivo de disco duro virtual secundario.</span><span class="sxs-lookup"><span data-stu-id="295d5-109">A fully qualified path that specifies the location of the child virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="295d5-110">*ParentPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="295d5-110">*ParentPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="295d5-111">Ruta de acceso completa que especifica la ubicación del archivo de disco duro virtual principal.</span><span class="sxs-lookup"><span data-stu-id="295d5-111">A fully qualified path that specifies the location of the parent virtual hard disk file.</span></span>

</dd> <dt>

<span data-ttu-id="295d5-112">*LeafPath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="295d5-112">*LeafPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="295d5-113">Ruta de acceso completa que especifica la ubicación del archivo de disco duro virtual de hoja.</span><span class="sxs-lookup"><span data-stu-id="295d5-113">A fully qualified path that specifies the location of the leaf virtual hard disk file.</span></span> <span data-ttu-id="295d5-114">El parámetro puede ser **null** si el disco duro virtual está sin conexión, pero debe especificarse si el disco duro virtual está en uso.</span><span class="sxs-lookup"><span data-stu-id="295d5-114">The parameter can be **Null** if the virtual hard disk is offline, but must be specified if the virtual hard disk is in use.</span></span>

</dd> <dt>

<span data-ttu-id="295d5-115">*IgnoreIDMismatch* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="295d5-115">*IgnoreIDMismatch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="295d5-116">Indica si el elemento primario se debe establecer forzosamente cuando los identificadores de disco virtual no coinciden.</span><span class="sxs-lookup"><span data-stu-id="295d5-116">Indicates if the parent should be forcibly set when the virtual disk identifiers do not match.</span></span> <span data-ttu-id="295d5-117">Este parámetro debe usarse con precaución porque si el nuevo disco duro virtual principal no es idéntico al primario original, pueden producirse daños en los datos.</span><span class="sxs-lookup"><span data-stu-id="295d5-117">This parameter must be used with caution because if the new parent virtual hard disk is not identical to the original parent, data corruption can occur.</span></span>

</dd> <dt>

<span data-ttu-id="295d5-118">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="295d5-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="295d5-119">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="295d5-119">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="295d5-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="295d5-120">Return value</span></span>

<span data-ttu-id="295d5-121">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="295d5-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="295d5-122">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="295d5-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="295d5-123">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="295d5-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="295d5-124">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="295d5-124">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="295d5-125">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="295d5-125">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="295d5-126">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="295d5-126">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="295d5-127">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="295d5-127">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="295d5-128">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="295d5-128">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="295d5-129">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="295d5-129">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="295d5-130">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="295d5-130">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="295d5-131">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="295d5-131">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="295d5-132">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="295d5-132">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="295d5-133">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="295d5-133">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="295d5-134">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="295d5-134">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="295d5-135">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="295d5-135">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="295d5-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="295d5-136">Remarks</span></span>

<span data-ttu-id="295d5-137">Solo se pueden usar los siguientes tipos de discos duros virtuales con este método:</span><span class="sxs-lookup"><span data-stu-id="295d5-137">Only the following types of virtual hard disks can be used with this method:</span></span>

-   <span data-ttu-id="295d5-138">VHD de diferenciación</span><span class="sxs-lookup"><span data-stu-id="295d5-138">Differencing VHD</span></span>
-   <span data-ttu-id="295d5-139">VHDX de diferenciación</span><span class="sxs-lookup"><span data-stu-id="295d5-139">Differencing VHDX</span></span>

<span data-ttu-id="295d5-140">El acceso a la clase [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="295d5-140">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="295d5-141">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="295d5-141">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="295d5-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="295d5-142">Requirements</span></span>



| <span data-ttu-id="295d5-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="295d5-143">Requirement</span></span> | <span data-ttu-id="295d5-144">Value</span><span class="sxs-lookup"><span data-stu-id="295d5-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="295d5-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="295d5-145">Minimum supported client</span></span><br/> | <span data-ttu-id="295d5-146">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="295d5-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="295d5-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="295d5-147">Minimum supported server</span></span><br/> | <span data-ttu-id="295d5-148">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="295d5-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="295d5-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="295d5-149">Namespace</span></span><br/>                | <span data-ttu-id="295d5-150">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="295d5-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="295d5-151">MOF</span><span class="sxs-lookup"><span data-stu-id="295d5-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="295d5-152"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="295d5-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="295d5-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="295d5-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="295d5-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="295d5-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="295d5-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="295d5-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="295d5-156">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="295d5-156">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

