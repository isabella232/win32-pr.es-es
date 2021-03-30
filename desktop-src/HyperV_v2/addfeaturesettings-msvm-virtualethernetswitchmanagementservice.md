---
description: Agrega configuraciones de características a la configuración de un puerto de conmutador Ethernet.
ms.assetid: 628a6546-cc78-4fde-be0c-533a2c3f9483
title: Método AddFeatureSettings de la clase Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.AddFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e3b46a26d3c67f5efce4944c8b2e874febced32e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104002021"
---
# <a name="addfeaturesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="b9189-103">Método AddFeatureSettings de la \_ clase VirtualEthernetSwitchManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="b9189-103">AddFeatureSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="b9189-104">Agrega configuraciones de características a la configuración de un puerto de conmutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="b9189-104">Adds feature settings to the configuration of an Ethernet switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9189-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b9189-105">Syntax</span></span>


```mof
uint32 AddFeatureSettings(
  [in]  CIM_SettingData         REF AffectedConfiguration,
  [in]  string                      FeatureSettings[],
  [out] Msvm_FeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob         REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b9189-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b9189-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9189-107">*AffectedConfiguration* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b9189-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9189-108">Una referencia a una clase derivada de [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)) que representa el puerto del conmutador Ethernet afectado o la configuración del conmutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="b9189-108">A reference to a [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) derived class that represents the affected Ethernet switch port or Ethernet switch configuration.</span></span>

</dd> <dt>

<span data-ttu-id="b9189-109">*FeatureSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b9189-109">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9189-110">Matriz de cadenas que contiene una instancia incrustada de una clase derivada de la clase [**MSVM \_ FeatureSettingData**](msvm-featuresettingdata.md) , que describe la configuración de características que se va a agregar a la configuración del puerto del conmutador.</span><span class="sxs-lookup"><span data-stu-id="b9189-110">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class, that describes the feature settings to be added to the switch port configuration.</span></span>

</dd> <dt>

<span data-ttu-id="b9189-111">*ResultingFeatureSettings* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b9189-111">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9189-112">Una matriz de referencias a las instancias de la clase [**MSVM \_ FeatureSettingData**](msvm-featuresettingdata.md) que representan la configuración de características agregada.</span><span class="sxs-lookup"><span data-stu-id="b9189-112">An array of references to instances of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represent the added feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="b9189-113">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b9189-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9189-114">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b9189-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9189-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b9189-115">Return value</span></span>

<span data-ttu-id="b9189-116">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="b9189-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b9189-117">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="b9189-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b9189-118">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="b9189-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b9189-119">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="b9189-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b9189-120">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="b9189-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b9189-121">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="b9189-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="b9189-122">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="b9189-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="b9189-123">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="b9189-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b9189-124">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="b9189-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="b9189-125">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="b9189-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b9189-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9189-126">Requirements</span></span>



| <span data-ttu-id="b9189-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9189-127">Requirement</span></span> | <span data-ttu-id="b9189-128">Value</span><span class="sxs-lookup"><span data-stu-id="b9189-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9189-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9189-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b9189-130">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="b9189-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b9189-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b9189-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b9189-132">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="b9189-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b9189-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b9189-133">Namespace</span></span><br/>                | <span data-ttu-id="b9189-134">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b9189-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b9189-135">MOF</span><span class="sxs-lookup"><span data-stu-id="b9189-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9189-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b9189-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9189-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b9189-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9189-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b9189-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b9189-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="b9189-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9189-140">**ModifyFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="b9189-140">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="b9189-141">**RemoveFeatureSettings**</span><span class="sxs-lookup"><span data-stu-id="b9189-141">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="b9189-142">**MSVM \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="b9189-142">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

