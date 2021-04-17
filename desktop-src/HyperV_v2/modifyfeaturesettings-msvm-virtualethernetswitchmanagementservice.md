---
description: Modifica la configuración de características de un puerto de conmutador Ethernet.
ms.assetid: 8c21a932-fffb-40fd-9166-d7e351329217
title: Método ModifyFeatureSettings de la clase Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.ModifyFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0bee92019f9457a42a0c87ab619f7de1f7d203ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687784"
---
# <a name="modifyfeaturesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="534be-103">Método ModifyFeatureSettings de la \_ clase VirtualEthernetSwitchManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="534be-103">ModifyFeatureSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="534be-104">Modifica la configuración de características de un puerto de conmutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="534be-104">Modifies the feature settings of an Ethernet switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="534be-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="534be-105">Syntax</span></span>


```mof
uint32 ModifyFeatureSettings(
  [in]  string                      FeatureSettings[],
  [out] Msvm_FeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob         REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="534be-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="534be-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="534be-107">*FeatureSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="534be-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="534be-108">Matriz de cadenas que contiene una instancia incrustada de una clase derivada de la clase [**MSVM \_ FeatureSettingData**](msvm-featuresettingdata.md) , que describe la configuración de las características del puerto del conmutador que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="534be-108">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class, that describes the switch port feature settings to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="534be-109">*ResultingFeatureSettings* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="534be-109">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="534be-110">Una matriz de referencias a las instancias de la clase [**MSVM \_ FeatureSettingData**](msvm-featuresettingdata.md) que representan la configuración de características modificada.</span><span class="sxs-lookup"><span data-stu-id="534be-110">An array of references to instances of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represent the modified feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="534be-111">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="534be-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="534be-112">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="534be-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="534be-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="534be-113">Return value</span></span>

<span data-ttu-id="534be-114">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="534be-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="534be-115">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="534be-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="534be-116">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="534be-116">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="534be-117">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="534be-117">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="534be-118">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="534be-118">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="534be-119">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="534be-119">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="534be-120">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="534be-120">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="534be-121">**Parámetros incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="534be-121">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="534be-122">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="534be-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="534be-123">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="534be-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="534be-124">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="534be-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="534be-125">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="534be-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="534be-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="534be-126">Requirements</span></span>



| <span data-ttu-id="534be-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="534be-127">Requirement</span></span> | <span data-ttu-id="534be-128">Value</span><span class="sxs-lookup"><span data-stu-id="534be-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="534be-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="534be-129">Minimum supported client</span></span><br/> | <span data-ttu-id="534be-130">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="534be-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="534be-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="534be-131">Minimum supported server</span></span><br/> | <span data-ttu-id="534be-132">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="534be-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="534be-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="534be-133">Namespace</span></span><br/>                | <span data-ttu-id="534be-134">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="534be-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="534be-135">MOF</span><span class="sxs-lookup"><span data-stu-id="534be-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="534be-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="534be-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="534be-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="534be-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="534be-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="534be-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="534be-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="534be-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="534be-140">**AddFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="534be-140">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="534be-141">**RemoveFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="534be-141">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="534be-142">**MSVM \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="534be-142">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

