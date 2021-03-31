---
description: Modifica la configuración actual de las características de una conexión Ethernet de máquina virtual.
ms.assetid: 3caa810f-0444-45cf-88a4-e93d04accb46
title: Método ModifyFeatureSettings de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c376158008c5ad0e611d3a05c7e73d2e7d1b44cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360812"
---
# <a name="modifyfeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="13760-103">Método ModifyFeatureSettings de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="13760-103">ModifyFeatureSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="13760-104">Modifica la configuración actual de las características de una conexión Ethernet de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="13760-104">Modifies the current feature settings of a virtual machine Ethernet connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="13760-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13760-105">Syntax</span></span>


```mof
uint32 ModifyFeatureSettings(
  [in]  string                                        FeatureSettings[],
  [out] Msvm_EthernetSwitchPortFeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="13760-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13760-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13760-107">*FeatureSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="13760-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13760-108">Una matriz de cadenas que contienen una instancia incrustada de una clase derivada de la clase [**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) , que describe las modificaciones realizadas a la configuración actual de las características de una conexión Ethernet existente.</span><span class="sxs-lookup"><span data-stu-id="13760-108">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class, that describes modifications to the current feature settings of an existing Ethernet connection.</span></span> <span data-ttu-id="13760-109">La propiedad **InstanceID** de cada una de estas instancias identifica la configuración de características que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="13760-109">The **InstanceID** property of each of these instances identifies the feature settings to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="13760-110">*ResultingFeatureSettings* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="13760-110">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13760-111">Una matriz de referencias a las instancias de la clase [**MSVM \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) que representan la configuración de características modificada.</span><span class="sxs-lookup"><span data-stu-id="13760-111">An array of references to instances of the [**Msvm\_EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) class that represent the modified feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="13760-112">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="13760-112">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13760-113">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="13760-113">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13760-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13760-114">Return value</span></span>

<span data-ttu-id="13760-115">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="13760-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="13760-116">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="13760-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="13760-117">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="13760-117">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="13760-118">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="13760-118">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="13760-119">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="13760-119">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="13760-120">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="13760-120">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="13760-121">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="13760-121">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="13760-122">**Parámetros incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="13760-122">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="13760-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="13760-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="13760-124">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="13760-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="13760-125">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="13760-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="13760-126">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="13760-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="13760-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13760-127">Requirements</span></span>



| <span data-ttu-id="13760-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="13760-128">Requirement</span></span> | <span data-ttu-id="13760-129">Value</span><span class="sxs-lookup"><span data-stu-id="13760-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13760-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13760-130">Minimum supported client</span></span><br/> | <span data-ttu-id="13760-131">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="13760-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="13760-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13760-132">Minimum supported server</span></span><br/> | <span data-ttu-id="13760-133">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="13760-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="13760-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="13760-134">Namespace</span></span><br/>                | <span data-ttu-id="13760-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="13760-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="13760-136">MOF</span><span class="sxs-lookup"><span data-stu-id="13760-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13760-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13760-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="13760-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="13760-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13760-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="13760-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="13760-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="13760-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13760-141">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="13760-141">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

