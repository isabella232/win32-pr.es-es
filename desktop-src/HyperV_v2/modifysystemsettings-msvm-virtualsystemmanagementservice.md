---
description: Modifica la configuración de la máquina virtual.
ms.assetid: 3266bd0d-398b-4d3b-9248-e29c069aab11
title: Método ModifySystemSettings de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4e6bf40b3dd206affcdc014e98554bfa8f88b4c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668077"
---
# <a name="modifysystemsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="6ef9b-103">Método ModifySystemSettings de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="6ef9b-103">ModifySystemSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="6ef9b-104">Modifica la configuración de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6ef9b-104">Modifies virtual machine settings.</span></span> <span data-ttu-id="6ef9b-105">Cuando se aplica a la configuración del sistema de una configuración de máquina virtual "actual", se puede modificar la instancia de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6ef9b-105">When applied to the system settings of a "current" virtual machine configuration, as a side effect the virtual machine instance may be modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ef9b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ef9b-106">Syntax</span></span>


```mof
uint32 ModifySystemSettings(
  [in]  string              SystemSettings,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6ef9b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6ef9b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ef9b-108">*Configuración* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6ef9b-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ef9b-109">Instancia insertada de la clase [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que contiene los aspectos modificados de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="6ef9b-109">An embedded instance of the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class that contains the modified aspects of the virtual machine.</span></span> <span data-ttu-id="6ef9b-110">La propiedad **InstanceID** identifica la configuración de la máquina virtual que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="6ef9b-110">The **InstanceID** property identifies the virtual machine setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="6ef9b-111">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6ef9b-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ef9b-112">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6ef9b-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ef9b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ef9b-113">Return value</span></span>

<span data-ttu-id="6ef9b-114">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="6ef9b-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6ef9b-115">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="6ef9b-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6ef9b-116">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="6ef9b-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="6ef9b-117">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="6ef9b-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="6ef9b-118">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="6ef9b-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="6ef9b-119">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="6ef9b-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="6ef9b-120">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="6ef9b-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="6ef9b-121">**Parámetros incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="6ef9b-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="6ef9b-122">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="6ef9b-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="6ef9b-123">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="6ef9b-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6ef9b-124">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="6ef9b-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="6ef9b-125">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="6ef9b-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6ef9b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ef9b-126">Requirements</span></span>



| <span data-ttu-id="6ef9b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ef9b-127">Requirement</span></span> | <span data-ttu-id="6ef9b-128">Value</span><span class="sxs-lookup"><span data-stu-id="6ef9b-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ef9b-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ef9b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6ef9b-130">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="6ef9b-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6ef9b-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6ef9b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6ef9b-132">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="6ef9b-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6ef9b-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6ef9b-133">Namespace</span></span><br/>                | <span data-ttu-id="6ef9b-134">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="6ef9b-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6ef9b-135">MOF</span><span class="sxs-lookup"><span data-stu-id="6ef9b-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ef9b-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ef9b-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ef9b-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6ef9b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ef9b-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6ef9b-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6ef9b-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ef9b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ef9b-140">**ModifyVirtualSystem (V1)**</span><span class="sxs-lookup"><span data-stu-id="6ef9b-140">**ModifyVirtualSystem (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyvirtualsystem-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="6ef9b-141">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="6ef9b-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

