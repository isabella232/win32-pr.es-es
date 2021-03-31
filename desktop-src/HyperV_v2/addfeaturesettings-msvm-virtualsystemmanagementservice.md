---
description: Agrega la configuración de características Ethernet a la configuración de una conexión Ethernet de máquina virtual.
ms.assetid: f233bf2f-5201-4b02-8384-bb7e2d1e7dee
title: Método AddFeatureSettings de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5e9acbaaf6ff1da6439dcb243869e09133e0031e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360711"
---
# <a name="addfeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="a918c-103">Método AddFeatureSettings de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="a918c-103">AddFeatureSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="a918c-104">Agrega la configuración de características Ethernet a la configuración de una conexión Ethernet de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="a918c-104">Adds Ethernet feature settings to the configuration of a virtual machine Ethernet connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a918c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a918c-105">Syntax</span></span>


```mof
uint32 AddFeatureSettings(
  [in]  Msvm_EthernetPortAllocationSettingData    REF AffectedConfiguration,
  [in]  string                                        FeatureSettings[],
  [out] Msvm_EthernetSwitchPortFeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a918c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a918c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a918c-107">*AffectedConfiguration* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a918c-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a918c-108">Referencia a una instancia de la clase [**MSVM \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) que representa la conexión Ethernet afectada.</span><span class="sxs-lookup"><span data-stu-id="a918c-108">Reference to an instance of the [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) class that represents the affected Ethernet connection.</span></span>

</dd> <dt>

<span data-ttu-id="a918c-109">*FeatureSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a918c-109">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a918c-110">Matriz de cadenas que contiene una instancia incrustada de la clase [**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) que describe la configuración de características que se va a agregar a la configuración de conexión.</span><span class="sxs-lookup"><span data-stu-id="a918c-110">An array of strings that contain one embedded instance of the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class that describes the feature settings to be added to the connection configuration.</span></span>

</dd> <dt>

<span data-ttu-id="a918c-111">*ResultingFeatureSettings* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a918c-111">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a918c-112">Una matriz de referencias a las instancias de la clase [**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) que representa la configuración de características agregada.</span><span class="sxs-lookup"><span data-stu-id="a918c-112">An array of references to instances of the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) class that represents the added feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="a918c-113">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="a918c-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a918c-114">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a918c-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a918c-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a918c-115">Return value</span></span>

<span data-ttu-id="a918c-116">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="a918c-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a918c-117">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="a918c-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a918c-118">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="a918c-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a918c-119">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="a918c-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a918c-120">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="a918c-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a918c-121">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="a918c-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a918c-122">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="a918c-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="a918c-123">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="a918c-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a918c-124">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="a918c-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="a918c-125">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="a918c-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a918c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a918c-126">Requirements</span></span>



| <span data-ttu-id="a918c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a918c-127">Requirement</span></span> | <span data-ttu-id="a918c-128">Value</span><span class="sxs-lookup"><span data-stu-id="a918c-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a918c-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a918c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a918c-130">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="a918c-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a918c-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a918c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a918c-132">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="a918c-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a918c-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a918c-133">Namespace</span></span><br/>                | <span data-ttu-id="a918c-134">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="a918c-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a918c-135">MOF</span><span class="sxs-lookup"><span data-stu-id="a918c-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a918c-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a918c-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a918c-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a918c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a918c-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a918c-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a918c-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="a918c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a918c-140">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="a918c-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

