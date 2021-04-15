---
description: Crea un punto de referencia de una colección de sistemas virtuales.
ms.assetid: 40ec5715-0dbc-43e3-a305-c8c31de60977
title: Método CreateReferencePoint de la clase Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.CreateReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7681795ee18965e3e04b75c800e3e574d6627ea9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361662"
---
# <a name="createreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a><span data-ttu-id="d8672-103">Método CreateReferencePoint de la \_ clase CollectionReferencePointService de MSVM</span><span class="sxs-lookup"><span data-stu-id="d8672-103">CreateReferencePoint method of the Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="d8672-104">Crea un punto de referencia de una colección de sistemas virtuales.</span><span class="sxs-lookup"><span data-stu-id="d8672-104">Creates a reference point of a virtual system collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8672-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8672-105">Syntax</span></span>


```mof
uint32 CreateReferencePoint(
  [in]      Msvm_VirtualSystemCollection REF Collection,
  [in]      string                           ReferencePointSettings,
  [in]      uint16                           ReferencePointType,
  [in, out] CIM_Collection               REF ResultingReferencePointCollection,
  [out]     CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d8672-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d8672-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8672-107">*Colección* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d8672-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8672-108">Referencia a la colección de sistemas virtuales afectada.</span><span class="sxs-lookup"><span data-stu-id="d8672-108">Reference to the affected virtual system collection.</span></span>

</dd> <dt>

<span data-ttu-id="d8672-109">*ReferencePointSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d8672-109">*ReferencePointSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8672-110">Configuración de parámetros.</span><span class="sxs-lookup"><span data-stu-id="d8672-110">Parameter settings.</span></span>

</dd> <dt>

<span data-ttu-id="d8672-111">*ReferencePointType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d8672-111">*ReferencePointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d8672-112">Indica el tipo del punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="d8672-112">Indicates the type of the reference point.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d8672-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="d8672-113"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span data-ttu-id="d8672-114"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Basado en el registro** (1)</span><span class="sxs-lookup"><span data-stu-id="d8672-114"><span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>**Log based** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d8672-115">Seguimiento del registro de réplica de Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="d8672-115">Hyper-V replica log tracking.</span></span>

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span data-ttu-id="d8672-116"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT basado** (2)</span><span class="sxs-lookup"><span data-stu-id="d8672-116"><span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**RCT based** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d8672-117">Basado en Change Tracking resistente de los discos virtuales.</span><span class="sxs-lookup"><span data-stu-id="d8672-117">Based on Resilient Change Tracking of virtual disks.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="d8672-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d8672-118"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

<span data-ttu-id="d8672-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="d8672-119"><span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>**Vendor Specific** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="d8672-120">*ResultingReferencePointCollection* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d8672-120">*ResultingReferencePointCollection* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8672-121">Punto de referencia resultante de una colección de sistemas virtuales.</span><span class="sxs-lookup"><span data-stu-id="d8672-121">Resulting reference point of a virtual system collection.</span></span>

</dd> <dt>

<span data-ttu-id="d8672-122">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d8672-122">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8672-123">Si la operación es de larga ejecución, opcionalmente se puede devolver un trabajo.</span><span class="sxs-lookup"><span data-stu-id="d8672-123">If the operation is long running, then optionally a job may be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8672-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8672-124">Return value</span></span>

<span data-ttu-id="d8672-125">Si se realiza correctamente, devuelve 0 (sin errores) o 4096 (se inició el trabajo). de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="d8672-125">If successful, returns either 0 (no error), or 4096 (job started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="d8672-126">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="d8672-126">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d8672-127">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="d8672-127">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="d8672-128">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="d8672-128">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="d8672-129">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="d8672-129">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="d8672-130">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="d8672-130">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="d8672-131">**Estado no válido** (5)</span><span class="sxs-lookup"><span data-stu-id="d8672-131">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="d8672-132">**Tipo no válido** (6)</span><span class="sxs-lookup"><span data-stu-id="d8672-132">**Invalid Type** (6)</span></span>
</dt> <dt>

<span data-ttu-id="d8672-133">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d8672-133">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="d8672-134">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="d8672-134">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d8672-135">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="d8672-135">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="d8672-136">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="d8672-136">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d8672-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8672-137">Requirements</span></span>



| <span data-ttu-id="d8672-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8672-138">Requirement</span></span> | <span data-ttu-id="d8672-139">Value</span><span class="sxs-lookup"><span data-stu-id="d8672-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8672-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8672-140">Minimum supported client</span></span><br/> | <span data-ttu-id="d8672-141">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="d8672-141">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="d8672-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8672-142">Minimum supported server</span></span><br/> | <span data-ttu-id="d8672-143">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d8672-143">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d8672-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d8672-144">Namespace</span></span><br/>                | <span data-ttu-id="d8672-145">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="d8672-145">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d8672-146">MOF</span><span class="sxs-lookup"><span data-stu-id="d8672-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8672-147"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8672-147"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8672-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d8672-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8672-149"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d8672-149"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d8672-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8672-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8672-151">**MSVM \_ CollectionReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="d8672-151">**Msvm\_CollectionReferencePointService**</span></span>](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




