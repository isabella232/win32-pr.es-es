---
description: Actualiza la configuración de un disco duro virtual.
ms.assetid: 10f80313-bc78-447e-bdf2-5635d7354e3c
title: Método SetVirtualHardDiskSettingData de la clase Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetVirtualHardDiskSettingData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 969e9019d05b49f2f171f2177e1e74f135e212da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361405"
---
# <a name="setvirtualharddisksettingdata-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="c0b0c-103">Método SetVirtualHardDiskSettingData de la \_ clase ImageManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="c0b0c-103">SetVirtualHardDiskSettingData method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="c0b0c-104">Actualiza la configuración de un disco duro virtual.</span><span class="sxs-lookup"><span data-stu-id="c0b0c-104">Updates the settings for a virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0b0c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0b0c-105">Syntax</span></span>


```mof
uint32 SetVirtualHardDiskSettingData(
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c0b0c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c0b0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0b0c-107">*VirtualDiskSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c0b0c-107">*VirtualDiskSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0b0c-108">Representación de cadena de la clase [**MSVM \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) que especifica el disco duro virtual que se va a actualizar y que contiene los nuevos datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="c0b0c-108">A string representation of the [**Msvm\_VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) class that specifies the virtual hard disk to update and that contains the new setting data.</span></span> <span data-ttu-id="c0b0c-109">Con este método solo se pueden actualizar las propiedades **ParentPath**, **PhysicalSectorSize** o **VirtualDiskId** .</span><span class="sxs-lookup"><span data-stu-id="c0b0c-109">Only the **ParentPath**, **PhysicalSectorSize**, or **VirtualDiskId** properties can be updated with this method.</span></span> <span data-ttu-id="c0b0c-110">Estas propiedades no se pueden actualizar con una llamada al método.</span><span class="sxs-lookup"><span data-stu-id="c0b0c-110">You can't update these properties with one method call.</span></span> <span data-ttu-id="c0b0c-111">Solo se puede actualizar una de estas propiedades con una única llamada al método.</span><span class="sxs-lookup"><span data-stu-id="c0b0c-111">You can only update one of these properties with a single method call.</span></span>

</dd> <dt>

<span data-ttu-id="c0b0c-112">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c0b0c-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0b0c-113">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c0b0c-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0b0c-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c0b0c-114">Return value</span></span>

<span data-ttu-id="c0b0c-115">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c0b0c-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c0b0c-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="c0b0c-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c0b0c-117">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="c0b0c-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c0b0c-118">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="c0b0c-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c0b0c-119">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="c0b0c-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c0b0c-120">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="c0b0c-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c0b0c-121">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="c0b0c-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c0b0c-122">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="c0b0c-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c0b0c-123">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="c0b0c-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c0b0c-124">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="c0b0c-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c0b0c-125">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="c0b0c-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c0b0c-126">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="c0b0c-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c0b0c-127">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="c0b0c-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c0b0c-128">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="c0b0c-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="c0b0c-129">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="c0b0c-129">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="c0b0c-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c0b0c-130">Remarks</span></span>

<span data-ttu-id="c0b0c-131">El acceso a la clase [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="c0b0c-131">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="c0b0c-132">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="c0b0c-132">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0b0c-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0b0c-133">Requirements</span></span>



| <span data-ttu-id="c0b0c-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0b0c-134">Requirement</span></span> | <span data-ttu-id="c0b0c-135">Value</span><span class="sxs-lookup"><span data-stu-id="c0b0c-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0b0c-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0b0c-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c0b0c-137">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="c0b0c-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c0b0c-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0b0c-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c0b0c-139">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="c0b0c-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c0b0c-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c0b0c-140">Namespace</span></span><br/>                | <span data-ttu-id="c0b0c-141">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="c0b0c-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c0b0c-142">MOF</span><span class="sxs-lookup"><span data-stu-id="c0b0c-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0b0c-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0b0c-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0b0c-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c0b0c-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0b0c-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c0b0c-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c0b0c-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="c0b0c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0b0c-147">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="c0b0c-147">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

