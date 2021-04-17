---
description: Genera un BLOB opaco de datos que contiene información de compatibilidad del sistema especificado.
ms.assetid: 5cfb50c4-d695-4867-ac6a-234ce5120a6d
title: Método GetSystemCompatibilityInfo de la clase Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.GetSystemCompatibilityInfo
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9b0326dfb39123e508e9c5fefbd0404288cb97b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686614"
---
# <a name="getsystemcompatibilityinfo-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="cbf0f-103">Método GetSystemCompatibilityInfo de la \_ clase VirtualSystemMigrationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="cbf0f-103">GetSystemCompatibilityInfo method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="cbf0f-104">Genera un BLOB opaco de datos que contiene información de compatibilidad del sistema especificado.</span><span class="sxs-lookup"><span data-stu-id="cbf0f-104">Generates an opaque blob of data that contains compatibility information for the specified system.</span></span> <span data-ttu-id="cbf0f-105">Este método se usa junto con el método [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) para determinar si es posible realizar una migración rápida o en vivo de una máquina virtual a otro equipo de hospedaje sin intentar realmente la migración.</span><span class="sxs-lookup"><span data-stu-id="cbf0f-105">This method is used in conjunction with the [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) method to determine whether a quick or live migration of a virtual machine to another hosting computer system is possible without actually attempting the migration.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbf0f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cbf0f-106">Syntax</span></span>


```mof
uint32 GetSystemCompatibilityInfo(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] uint8                  CompatibilityInfo[]
);
```



## <a name="parameters"></a><span data-ttu-id="cbf0f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cbf0f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbf0f-108">*ComputerSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cbf0f-108">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbf0f-109">Una referencia a una clase de [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representa la máquina virtual para la que se va a recuperar la información de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="cbf0f-109">A reference to a [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine to retrieve compatibility information for.</span></span> <span data-ttu-id="cbf0f-110">Si este parámetro hace referencia al sistema del equipo host, los datos devueltos en el parámetro *CompatibilityInfo* se pueden usar para determinar si cualquiera de las máquinas virtuales del equipo host se puede migrar rápidamente a otro sistema de host.</span><span class="sxs-lookup"><span data-stu-id="cbf0f-110">If this parameter refers to the hosting computer system, the data returned in the *CompatibilityInfo* parameter can be used to determine whether any of the virtual machines on the hosting computer system can be quickly migrated to another hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="cbf0f-111">*CompatibilityInfo* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cbf0f-111">*CompatibilityInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cbf0f-112">Un BLOB opaco de datos que se puede pasar al método [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) en otro sistema de equipo host para confirmar la compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="cbf0f-112">An opaque blob of data that can be passed to the [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) method on another hosting computer system to confirm compatibility.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbf0f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cbf0f-113">Return value</span></span>

<span data-ttu-id="cbf0f-114">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="cbf0f-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="cbf0f-115">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="cbf0f-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cbf0f-116">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="cbf0f-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="cbf0f-117">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="cbf0f-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="cbf0f-118">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="cbf0f-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="cbf0f-119">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="cbf0f-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="cbf0f-120">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="cbf0f-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="cbf0f-121">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="cbf0f-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="cbf0f-122">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="cbf0f-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="cbf0f-123">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="cbf0f-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="cbf0f-124">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="cbf0f-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="cbf0f-125">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="cbf0f-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="cbf0f-126">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="cbf0f-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="cbf0f-127">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="cbf0f-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="cbf0f-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbf0f-128">Requirements</span></span>



| <span data-ttu-id="cbf0f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbf0f-129">Requirement</span></span> | <span data-ttu-id="cbf0f-130">Value</span><span class="sxs-lookup"><span data-stu-id="cbf0f-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbf0f-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbf0f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="cbf0f-132">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="cbf0f-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cbf0f-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cbf0f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="cbf0f-134">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="cbf0f-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cbf0f-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cbf0f-135">Namespace</span></span><br/>                | <span data-ttu-id="cbf0f-136">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="cbf0f-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cbf0f-137">MOF</span><span class="sxs-lookup"><span data-stu-id="cbf0f-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cbf0f-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cbf0f-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cbf0f-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cbf0f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbf0f-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cbf0f-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cbf0f-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="cbf0f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbf0f-142">**MSVM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="cbf0f-142">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




