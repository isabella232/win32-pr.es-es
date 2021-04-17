---
description: Quita la configuración de características de una conexión Ethernet de máquina virtual.
ms.assetid: 457056d0-7e69-47e4-8744-0136a1816f4a
title: Método RemoveFeatureSettings de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c29151f6544d7eb803ec72ee49e455556d8b2d70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667946"
---
# <a name="removefeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="5e8f2-103">Método RemoveFeatureSettings de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="5e8f2-103">RemoveFeatureSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="5e8f2-104">Quita la configuración de características de una conexión Ethernet de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-104">Removes feature settings from a virtual machine Ethernet connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e8f2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5e8f2-105">Syntax</span></span>


```mof
uint32 RemoveFeatureSettings(
  [in]  Msvm_EthernetSwitchPortFeatureSettingData REF FeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="5e8f2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5e8f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e8f2-107">*FeatureSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5e8f2-107">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5e8f2-108">Matriz de cadenas que contienen una instancia incrustada de una clase derivada de la clase [**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) , que define la configuración de características que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-108">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class, that defines the feature settings to be removed.</span></span> <span data-ttu-id="5e8f2-109">La propiedad **InstanceID** de cada una de estas instancias identifica la configuración de características que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-109">The **InstanceID** property of each of these instances identifies the feature settings to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="5e8f2-110">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="5e8f2-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e8f2-111">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5e8f2-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e8f2-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e8f2-112">Return value</span></span>

<span data-ttu-id="5e8f2-113">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="5e8f2-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="5e8f2-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="5e8f2-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="5e8f2-115">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="5e8f2-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5e8f2-116">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="5e8f2-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5e8f2-117">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="5e8f2-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5e8f2-118">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="5e8f2-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5e8f2-119">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="5e8f2-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="5e8f2-120">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="5e8f2-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="5e8f2-121">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="5e8f2-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="5e8f2-122">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="5e8f2-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="5e8f2-123">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="5e8f2-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="5e8f2-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e8f2-124">Requirements</span></span>



| <span data-ttu-id="5e8f2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e8f2-125">Requirement</span></span> | <span data-ttu-id="5e8f2-126">Value</span><span class="sxs-lookup"><span data-stu-id="5e8f2-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e8f2-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e8f2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5e8f2-128">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e8f2-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5e8f2-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e8f2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5e8f2-130">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="5e8f2-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5e8f2-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5e8f2-131">Namespace</span></span><br/>                | <span data-ttu-id="5e8f2-132">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="5e8f2-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5e8f2-133">MOF</span><span class="sxs-lookup"><span data-stu-id="5e8f2-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5e8f2-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5e8f2-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5e8f2-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5e8f2-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e8f2-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5e8f2-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5e8f2-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e8f2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e8f2-138">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="5e8f2-138">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

