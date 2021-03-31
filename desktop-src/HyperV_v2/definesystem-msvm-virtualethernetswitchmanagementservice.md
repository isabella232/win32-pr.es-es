---
description: Crea un nuevo conmutador virtual.
ms.assetid: de7495e9-48c5-427a-b9bb-0821b53a9b09
title: Método DefineSystem de la clase Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bd6e2dfb7d9cf7e64fb76c35f6f3c3b8457d69d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911694"
---
# <a name="definesystem-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="39203-103">Método DefineSystem de la \_ clase VirtualEthernetSwitchManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="39203-103">DefineSystem method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="39203-104">Crea un nuevo conmutador virtual.</span><span class="sxs-lookup"><span data-stu-id="39203-104">Creates a new virtual switch.</span></span> <span data-ttu-id="39203-105">Las propiedades que no se especifican se rellenarán con los valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="39203-105">Properties that are not specified will be populated with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="39203-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39203-106">Syntax</span></span>


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="39203-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="39203-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39203-108">*Configuración* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="39203-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39203-109">Instancia insertada de la clase [**MSVM \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) que se usa para definir los atributos del conmutador virtual que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="39203-109">An embedded instance of the [**Msvm\_VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) class that is used to define the attributes of the virtual switch to be created.</span></span> <span data-ttu-id="39203-110">Este parámetro es necesario.</span><span class="sxs-lookup"><span data-stu-id="39203-110">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="39203-111">*ResourceSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="39203-111">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39203-112">Una matriz de instancias incrustadas de la clase [**MSVM \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) que describe la configuración de los puertos de conmutador que se van a crear en el ámbito del nuevo conmutador virtual.</span><span class="sxs-lookup"><span data-stu-id="39203-112">An array of embedded instances of the [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) class that describes the settings of the switch ports to be created in the scope of the new virtual switch.</span></span> <span data-ttu-id="39203-113">Si se especifica **null** , se creará el conmutador virtual sin recursos (es decir, sin puertos de conmutador).</span><span class="sxs-lookup"><span data-stu-id="39203-113">If **Null** is specified, the virtual switch will be created with no resources (i.e. no switch ports).</span></span>

</dd> <dt>

<span data-ttu-id="39203-114">*ReferenceConfiguration* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="39203-114">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39203-115">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="39203-115">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="39203-116">*ResultingSystem* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="39203-116">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39203-117">Si un conmutador virtual se crea correctamente, una referencia a una instancia de la clase [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) que representa el conmutador virtual recién definido.</span><span class="sxs-lookup"><span data-stu-id="39203-117">If a virtual switch is successfully created, a reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the newly defined virtual switch.</span></span>

</dd> <dt>

<span data-ttu-id="39203-118">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="39203-118">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39203-119">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="39203-119">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39203-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="39203-120">Return value</span></span>

<span data-ttu-id="39203-121">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="39203-121">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="39203-122">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="39203-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="39203-123">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="39203-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="39203-124">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="39203-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="39203-125">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="39203-125">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="39203-126">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="39203-126">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="39203-127">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="39203-127">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="39203-128">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="39203-128">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="39203-129">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="39203-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="39203-130">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="39203-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="39203-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39203-131">Requirements</span></span>



| <span data-ttu-id="39203-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="39203-132">Requirement</span></span> | <span data-ttu-id="39203-133">Value</span><span class="sxs-lookup"><span data-stu-id="39203-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39203-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39203-134">Minimum supported client</span></span><br/> | <span data-ttu-id="39203-135">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="39203-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="39203-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39203-136">Minimum supported server</span></span><br/> | <span data-ttu-id="39203-137">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="39203-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="39203-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="39203-138">Namespace</span></span><br/>                | <span data-ttu-id="39203-139">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="39203-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="39203-140">MOF</span><span class="sxs-lookup"><span data-stu-id="39203-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39203-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="39203-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="39203-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="39203-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39203-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="39203-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="39203-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="39203-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39203-145">**MSVM \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="39203-145">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

