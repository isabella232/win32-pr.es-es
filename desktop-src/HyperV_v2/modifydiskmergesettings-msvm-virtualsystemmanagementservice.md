---
description: Modifica los datos de configuración de combinación de discos.
ms.assetid: 91775dc5-105a-4e38-a334-fb34dd4e59f8
title: Método ModifyDiskMergeSettings de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyDiskMergeSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fe737c084b4c1c76a411ce1d2eba513554b40f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687785"
---
# <a name="modifydiskmergesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="b5777-103">Método ModifyDiskMergeSettings de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="b5777-103">ModifyDiskMergeSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="b5777-104">Modifica los datos de configuración de combinación de discos.</span><span class="sxs-lookup"><span data-stu-id="b5777-104">Modifies the disk merge setting data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5777-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b5777-105">Syntax</span></span>


```mof
uint32 ModifyDiskMergeSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="b5777-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b5777-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5777-107">*SettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b5777-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b5777-108">Instancia insertada de la clase [**MSVM \_ DiskMergeSettingData**](msvm-diskmergesettingdata.md) que contiene los datos de configuración modificados para la función de combinación de discos.</span><span class="sxs-lookup"><span data-stu-id="b5777-108">An embedded instance of the [**Msvm\_DiskMergeSettingData**](msvm-diskmergesettingdata.md) class that contains modified setting data for the disk merge function.</span></span>

</dd> <dt>

<span data-ttu-id="b5777-109">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="b5777-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b5777-110">Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b5777-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5777-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b5777-111">Return value</span></span>

<span data-ttu-id="b5777-112">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="b5777-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b5777-113">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="b5777-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b5777-114">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="b5777-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b5777-115">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="b5777-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b5777-116">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="b5777-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b5777-117">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="b5777-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b5777-118">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="b5777-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b5777-119">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="b5777-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b5777-120">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="b5777-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b5777-121">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="b5777-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b5777-122">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="b5777-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b5777-123">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="b5777-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b5777-124">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="b5777-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b5777-125">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="b5777-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b5777-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5777-126">Requirements</span></span>



| <span data-ttu-id="b5777-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5777-127">Requirement</span></span> | <span data-ttu-id="b5777-128">Value</span><span class="sxs-lookup"><span data-stu-id="b5777-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5777-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5777-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b5777-130">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="b5777-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b5777-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b5777-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b5777-132">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="b5777-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b5777-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b5777-133">Namespace</span></span><br/>                | <span data-ttu-id="b5777-134">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b5777-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b5777-135">MOF</span><span class="sxs-lookup"><span data-stu-id="b5777-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b5777-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b5777-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b5777-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b5777-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5777-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b5777-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b5777-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="b5777-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5777-140">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="b5777-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

