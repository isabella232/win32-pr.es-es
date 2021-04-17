---
description: Quita la configuración de características de un puerto de conmutador Ethernet.
ms.assetid: 3d45259e-34e4-417b-a895-4926b0eaaf59
title: Método RemoveFeatureSettings de la clase Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.RemoveFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 919e2b69e2a0ef215a522c601088cb7aa2976a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687943"
---
# <a name="removefeaturesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="c4055-103">Método RemoveFeatureSettings de la \_ clase VirtualEthernetSwitchManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="c4055-103">RemoveFeatureSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="c4055-104">Quita la configuración de características de un puerto de conmutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="c4055-104">Removes feature settings from an Ethernet switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4055-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4055-105">Syntax</span></span>


```mof
uint32 RemoveFeatureSettings(
  [in]  Msvm_FeatureSettingData REF FeatureSettings[],
  [out] CIM_ConcreteJob         REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c4055-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4055-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4055-107">*FeatureSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c4055-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4055-108">Una matriz de referencias a las instancias de la clase [**MSVM \_ FeatureSettingData**](msvm-featuresettingdata.md) que representan la configuración de características que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="c4055-108">An array of references to instances of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represent the feature settings to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="c4055-109">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c4055-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4055-110">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c4055-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4055-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4055-111">Return value</span></span>

<span data-ttu-id="c4055-112">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c4055-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c4055-113">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="c4055-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c4055-114">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="c4055-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c4055-115">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="c4055-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c4055-116">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="c4055-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c4055-117">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="c4055-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c4055-118">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="c4055-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c4055-119">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="c4055-119">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c4055-120">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="c4055-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c4055-121">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="c4055-121">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="c4055-122">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="c4055-122">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c4055-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4055-123">Requirements</span></span>



| <span data-ttu-id="c4055-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4055-124">Requirement</span></span> | <span data-ttu-id="c4055-125">Value</span><span class="sxs-lookup"><span data-stu-id="c4055-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4055-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4055-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c4055-127">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="c4055-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c4055-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4055-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c4055-129">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="c4055-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c4055-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c4055-130">Namespace</span></span><br/>                | <span data-ttu-id="c4055-131">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="c4055-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c4055-132">MOF</span><span class="sxs-lookup"><span data-stu-id="c4055-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4055-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4055-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4055-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c4055-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4055-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c4055-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c4055-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4055-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4055-137">**AddFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="c4055-137">**AddFeatureSettings**</span></span>](addfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="c4055-138">**ModifyFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="c4055-138">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="c4055-139">**MSVM \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="c4055-139">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

