---
description: Modifica la configuración del sistema virtual.
ms.assetid: 9c3d28f8-9806-411a-866f-d062c6d31818
title: Método ModifySystemSettings de la clase CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: da610d03e683b06ad743d1b6d4fe413dc5b31d34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001618"
---
# <a name="modifysystemsettings-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="2ddc3-103">Método ModifySystemSettings de la \_ clase VirtualSystemManagementService de CIM</span><span class="sxs-lookup"><span data-stu-id="2ddc3-103">ModifySystemSettings method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="2ddc3-104">Modifica la configuración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="2ddc3-104">Modifies virtual system settings.</span></span>

<span data-ttu-id="2ddc3-105">Cuando se aplica a la configuración del sistema de una configuración de sistema virtual "actual", se puede modificar la instancia del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="2ddc3-105">When applied to the system settings of a "current" virtual system configuration, as a side effect the virtual system instance may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ddc3-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2ddc3-106">Syntax</span></span>


```mof
uint32 ModifySystemSettings(
  [in]  string              SystemSettings,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2ddc3-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2ddc3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ddc3-108">*Configuración* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2ddc3-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ddc3-109">Cadena que contiene una instancia de la clase [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que se utiliza para modificar la configuración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="2ddc3-109">String containing an instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that is used to modify the settings of the virtual system.</span></span> <span data-ttu-id="2ddc3-110">La instancia de debe tener un **InstanceID** válido para poder identificar la configuración del sistema virtual que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="2ddc3-110">The instance must have a valid **InstanceID** in order to identify the virtual system setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="2ddc3-111">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2ddc3-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ddc3-112">Si la operación es de larga ejecución, opcionalmente se puede devolver un [**\_ ConcreteJob de CIM**](cim-concretejob.md) que represente el trabajo.</span><span class="sxs-lookup"><span data-stu-id="2ddc3-112">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ddc3-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ddc3-113">Return value</span></span>

<span data-ttu-id="2ddc3-114">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="2ddc3-114">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="2ddc3-115">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="2ddc3-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2ddc3-116">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="2ddc3-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2ddc3-117">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="2ddc3-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2ddc3-118">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="2ddc3-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2ddc3-119">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="2ddc3-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2ddc3-120">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="2ddc3-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="2ddc3-121">**Parámetros incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="2ddc3-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="2ddc3-122">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="2ddc3-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2ddc3-123">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="2ddc3-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2ddc3-124">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="2ddc3-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="2ddc3-125">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="2ddc3-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2ddc3-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ddc3-126">Requirements</span></span>



| <span data-ttu-id="2ddc3-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ddc3-127">Requirement</span></span> | <span data-ttu-id="2ddc3-128">Value</span><span class="sxs-lookup"><span data-stu-id="2ddc3-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ddc3-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ddc3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2ddc3-130">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="2ddc3-130">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="2ddc3-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2ddc3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2ddc3-132">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="2ddc3-132">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="2ddc3-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2ddc3-133">Namespace</span></span><br/>                | <span data-ttu-id="2ddc3-134">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="2ddc3-134">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2ddc3-135">MOF</span><span class="sxs-lookup"><span data-stu-id="2ddc3-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2ddc3-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2ddc3-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2ddc3-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2ddc3-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ddc3-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2ddc3-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2ddc3-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ddc3-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ddc3-140">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="2ddc3-140">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




