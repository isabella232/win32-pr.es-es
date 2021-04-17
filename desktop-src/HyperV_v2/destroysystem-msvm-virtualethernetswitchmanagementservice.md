---
description: Destruye un conmutador virtual.
ms.assetid: f0b6b4cc-e9b7-4255-a9e1-a2a826b8f119
title: Método DestroySystem de la clase Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d8f01a3f72d15fba908c7891f76b4128a1ee8200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688074"
---
# <a name="destroysystem-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="7828c-103">Método DestroySystem de la \_ clase VirtualEthernetSwitchManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="7828c-103">DestroySystem method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="7828c-104">Destruye un conmutador virtual.</span><span class="sxs-lookup"><span data-stu-id="7828c-104">Destroys a virtual switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="7828c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7828c-105">Syntax</span></span>


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="7828c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7828c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7828c-107">*AffectedSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7828c-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7828c-108">Referencia a una instancia de la clase [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) que representa el conmutador virtual que se va a destruir.</span><span class="sxs-lookup"><span data-stu-id="7828c-108">A reference to an instance of the [**Msvm\_VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) class that represents the virtual switch that is to be destroyed.</span></span>

</dd> <dt>

<span data-ttu-id="7828c-109">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="7828c-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7828c-110">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7828c-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7828c-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7828c-111">Return value</span></span>

<span data-ttu-id="7828c-112">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="7828c-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="7828c-113">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="7828c-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7828c-114">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="7828c-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7828c-115">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="7828c-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7828c-116">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="7828c-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="7828c-117">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="7828c-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="7828c-118">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="7828c-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="7828c-119">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="7828c-119">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="7828c-120">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="7828c-120">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="7828c-121">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="7828c-121">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="7828c-122">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="7828c-122">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7828c-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7828c-123">Requirements</span></span>



| <span data-ttu-id="7828c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="7828c-124">Requirement</span></span> | <span data-ttu-id="7828c-125">Value</span><span class="sxs-lookup"><span data-stu-id="7828c-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7828c-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7828c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7828c-127">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="7828c-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7828c-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7828c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7828c-129">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="7828c-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7828c-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7828c-130">Namespace</span></span><br/>                | <span data-ttu-id="7828c-131">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="7828c-131">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7828c-132">MOF</span><span class="sxs-lookup"><span data-stu-id="7828c-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7828c-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7828c-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7828c-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7828c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7828c-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7828c-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7828c-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="7828c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7828c-137">**MSVM \_ VirtualEthernetSwitchManagementService**</span><span class="sxs-lookup"><span data-stu-id="7828c-137">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

