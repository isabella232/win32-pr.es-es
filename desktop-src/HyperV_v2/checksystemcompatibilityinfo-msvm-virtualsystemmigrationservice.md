---
description: Comprueba la información de compatibilidad para la compatibilidad con el sistema del equipo host.
ms.assetid: 1991c58e-2d0b-4fc3-a04a-c18f358451f6
title: Método CheckSystemCompatibilityInfo de la clase Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckSystemCompatibilityInfo
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e47b72c6cac6e8a6061b4560b77b82cb0b845a8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907706"
---
# <a name="checksystemcompatibilityinfo-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="c8978-103">Método CheckSystemCompatibilityInfo de la \_ clase VirtualSystemMigrationService de MSVM</span><span class="sxs-lookup"><span data-stu-id="c8978-103">CheckSystemCompatibilityInfo method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="c8978-104">Comprueba la información de compatibilidad para la compatibilidad con el sistema del equipo host.</span><span class="sxs-lookup"><span data-stu-id="c8978-104">Checks the compatibility information for compatibility with the hosting computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8978-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8978-105">Syntax</span></span>


```mof
uint32 CheckSystemCompatibilityInfo(
  [in]  uint8  CompatibilityInfo[],
  [out] string Reasons[]
);
```



## <a name="parameters"></a><span data-ttu-id="c8978-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c8978-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8978-107">*CompatibilityInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c8978-107">*CompatibilityInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8978-108">Un BLOB de datos obtenidos mediante una llamada al método [**GetSystemCompatibilityInfo**](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) en el sistema del equipo host.</span><span class="sxs-lookup"><span data-stu-id="c8978-108">A blob of data obtained by calling the [**GetSystemCompatibilityInfo**](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) method on the hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="c8978-109">*Motivos* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c8978-109">*Reasons* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8978-110">Matriz de cadenas que recibe las instancias incrustadas de la clase de [**\_ error MSVM**](msvm-error.md) que representan cualquier advertencia o error.</span><span class="sxs-lookup"><span data-stu-id="c8978-110">An array of strings that receives the embedded instances of the [**Msvm\_Error**](msvm-error.md) class that represent any warnings or errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8978-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c8978-111">Return value</span></span>

<span data-ttu-id="c8978-112">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c8978-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c8978-113">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="c8978-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c8978-114">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="c8978-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c8978-115">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="c8978-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="c8978-116">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="c8978-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="c8978-117">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="c8978-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="c8978-118">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="c8978-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="c8978-119">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="c8978-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="c8978-120">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="c8978-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="c8978-121">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="c8978-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="c8978-122">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="c8978-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="c8978-123">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="c8978-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="c8978-124">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="c8978-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="c8978-125">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="c8978-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="c8978-126">**No compatible** (32784)</span><span class="sxs-lookup"><span data-stu-id="c8978-126">**Not compatible** (32784)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c8978-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8978-127">Requirements</span></span>



| <span data-ttu-id="c8978-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8978-128">Requirement</span></span> | <span data-ttu-id="c8978-129">Value</span><span class="sxs-lookup"><span data-stu-id="c8978-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8978-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8978-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c8978-131">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="c8978-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c8978-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8978-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c8978-133">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="c8978-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c8978-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c8978-134">Namespace</span></span><br/>                | <span data-ttu-id="c8978-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="c8978-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c8978-136">MOF</span><span class="sxs-lookup"><span data-stu-id="c8978-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8978-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8978-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8978-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c8978-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8978-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c8978-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c8978-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8978-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8978-141">**MSVM \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="c8978-141">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




