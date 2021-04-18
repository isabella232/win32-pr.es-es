---
description: Destruye un sistema virtual.
ms.assetid: 8d2504dc-ce23-4257-9dfd-6a35dfd84b2d
title: Método DestroySystem de la clase CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 41355970bb70063b8e90deb8f49b5e6f4b439017
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687339"
---
# <a name="destroysystem-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="1cfef-103">Método DestroySystem de la \_ clase VirtualSystemManagementService de CIM</span><span class="sxs-lookup"><span data-stu-id="1cfef-103">DestroySystem method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="1cfef-104">Destruye un sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="1cfef-104">Destroys a virtual system.</span></span>

<span data-ttu-id="1cfef-105">Se destruye el sistema virtual al que se hace referencia, incluidos los elementos que tienen el ámbito.</span><span class="sxs-lookup"><span data-stu-id="1cfef-105">The referenced virtual system is destroyed, including any elements scoped by it.</span></span> <span data-ttu-id="1cfef-106">Los recursos virtuales se devuelven a sus grupos de recursos, lo que puede implicar la destrucción de esos recursos (dependiente de la implementación).</span><span class="sxs-lookup"><span data-stu-id="1cfef-106">Virtual resources are returned to their resource pools, which may imply the destruction of those resources (implementation dependent).</span></span> <span data-ttu-id="1cfef-107">Si el sistema virtual está activo cuando se invoca la operación, primero se desactiva y luego se destruye.</span><span class="sxs-lookup"><span data-stu-id="1cfef-107">If the virtual system is active when the operation is invoked, it is first deactivated and then destroyed.</span></span> <span data-ttu-id="1cfef-108">Si las instantáneas se crearon a partir del sistema virtual, también se destruirán.</span><span class="sxs-lookup"><span data-stu-id="1cfef-108">If snapshots were created from the virtual system, these are destroyed as well.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cfef-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1cfef-109">Syntax</span></span>


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="1cfef-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1cfef-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cfef-111">*AffectedSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1cfef-111">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cfef-112">Referencia a una instancia de clase de tipo [**CIM \_ ComputerSystem**](cim-computersystem.md) que representa el sistema del equipo virtual que se va a destruir.</span><span class="sxs-lookup"><span data-stu-id="1cfef-112">Reference to an instance of class [**CIM\_ComputerSystem**](cim-computersystem.md) representing the virtual computer system that is to be destroyed.</span></span>

</dd> <dt>

<span data-ttu-id="1cfef-113">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1cfef-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1cfef-114">Si la operación es de larga ejecución, opcionalmente se puede devolver un [**\_ ConcreteJob de CIM**](cim-concretejob.md) que represente el trabajo.</span><span class="sxs-lookup"><span data-stu-id="1cfef-114">If the operation is long running, then optionally a [**CIM\_ConcreteJob**](cim-concretejob.md) representing the job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cfef-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1cfef-115">Return value</span></span>

<span data-ttu-id="1cfef-116">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="1cfef-116">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="1cfef-117">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="1cfef-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="1cfef-118">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="1cfef-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="1cfef-119">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="1cfef-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="1cfef-120">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="1cfef-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="1cfef-121">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="1cfef-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="1cfef-122">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="1cfef-122">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="1cfef-123">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="1cfef-123">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="1cfef-124">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="1cfef-124">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="1cfef-125">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="1cfef-125">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="1cfef-126">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="1cfef-126">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="1cfef-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cfef-127">Requirements</span></span>



| <span data-ttu-id="1cfef-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cfef-128">Requirement</span></span> | <span data-ttu-id="1cfef-129">Value</span><span class="sxs-lookup"><span data-stu-id="1cfef-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cfef-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cfef-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1cfef-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="1cfef-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="1cfef-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cfef-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1cfef-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="1cfef-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="1cfef-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1cfef-134">Namespace</span></span><br/>                | <span data-ttu-id="1cfef-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="1cfef-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1cfef-136">MOF</span><span class="sxs-lookup"><span data-stu-id="1cfef-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1cfef-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1cfef-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1cfef-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1cfef-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cfef-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1cfef-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1cfef-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="1cfef-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cfef-141">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="1cfef-141">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




