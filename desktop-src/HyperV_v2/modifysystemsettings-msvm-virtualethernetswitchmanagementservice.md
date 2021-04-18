---
description: Modifica la configuración del conmutador virtual.
ms.assetid: 8d323578-990f-483c-8515-8a21479767b1
title: Método ModifySystemSettings de la clase Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3512debfd6d49e3c09cb8a508a7f0d748ab128e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688060"
---
# <a name="modifysystemsettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="0b71e-103">Método ModifySystemSettings de la \_ clase VirtualEthernetSwitchManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="0b71e-103">ModifySystemSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="0b71e-104">Modifica la configuración del conmutador virtual.</span><span class="sxs-lookup"><span data-stu-id="0b71e-104">Modifies virtual switch settings.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b71e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b71e-105">Syntax</span></span>


```mof
uint32 ModifySystemSettings(
  [in]  string              SystemSettings,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="0b71e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b71e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b71e-107">*Configuración* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0b71e-107">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b71e-108">Instancia insertada de la clase [**MSVM \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) que contiene los aspectos modificados del conmutador virtual.</span><span class="sxs-lookup"><span data-stu-id="0b71e-108">An embedded instance of the [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) class that contains the modified aspects of the virtual switch.</span></span> <span data-ttu-id="0b71e-109">La propiedad **InstanceID** identifica la configuración del conmutador virtual que se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="0b71e-109">The **InstanceID** property identifies the virtual switch setting to be modified.</span></span>

</dd> <dt>

<span data-ttu-id="0b71e-110">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="0b71e-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0b71e-111">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0b71e-111">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b71e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0b71e-112">Return value</span></span>

<span data-ttu-id="0b71e-113">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="0b71e-113">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="0b71e-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="0b71e-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0b71e-115">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="0b71e-115">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0b71e-116">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="0b71e-116">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="0b71e-117">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="0b71e-117">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="0b71e-118">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="0b71e-118">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="0b71e-119">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="0b71e-119">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="0b71e-120">**Parámetros incompatibles** (6)</span><span class="sxs-lookup"><span data-stu-id="0b71e-120">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="0b71e-121">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0b71e-121">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="0b71e-122">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="0b71e-122">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="0b71e-123">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="0b71e-123">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="0b71e-124">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="0b71e-124">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0b71e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b71e-125">Requirements</span></span>



| <span data-ttu-id="0b71e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b71e-126">Requirement</span></span> | <span data-ttu-id="0b71e-127">Value</span><span class="sxs-lookup"><span data-stu-id="0b71e-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b71e-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b71e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0b71e-129">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="0b71e-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0b71e-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b71e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0b71e-131">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="0b71e-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0b71e-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0b71e-132">Namespace</span></span><br/>                | <span data-ttu-id="0b71e-133">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="0b71e-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0b71e-134">MOF</span><span class="sxs-lookup"><span data-stu-id="0b71e-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b71e-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b71e-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b71e-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0b71e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b71e-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0b71e-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0b71e-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b71e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b71e-139">**MSVM \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="0b71e-139">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

