---
description: Elimina el punto de referencia especificado.
ms.assetid: cb5245b6-5984-40ec-a37e-e4a0a62e318a
title: Método DestroyReferencePoint de la clase Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.DestroyReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9cf7a21e60369a928cc1d617e24db5f5fc70c522
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105670069"
---
# <a name="destroyreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="d5c1f-103">Método DestroyReferencePoint de la \_ clase VirtualSystemReferencePointService de MSVM</span><span class="sxs-lookup"><span data-stu-id="d5c1f-103">DestroyReferencePoint method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="d5c1f-104">Elimina el punto de referencia especificado.</span><span class="sxs-lookup"><span data-stu-id="d5c1f-104">Deletes the specified reference point.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5c1f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d5c1f-105">Syntax</span></span>


```mof
uint32 DestroyReferencePoint(
  [in]  Msvm_VirtualSystemReferencePoint REF AffectedReferencePoint,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="d5c1f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d5c1f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5c1f-107">*AffectedReferencePoint* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d5c1f-107">*AffectedReferencePoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5c1f-108">Referencia a la instancia [**de \_ VirtualSystemReferencePoint de MSVM**](msvm-virtualsystemreferencepoint.md) que representa el punto de referencia que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="d5c1f-108">A reference to the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance which represents the reference point to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="d5c1f-109">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="d5c1f-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5c1f-110">Parámetro opcional para supervisar el progreso de la operación, que se utiliza si el método no se pudo ejecutar sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="d5c1f-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="d5c1f-111">Si la operación se ejecuta de forma asincrónica, el valor devuelto es 4096.</span><span class="sxs-lookup"><span data-stu-id="d5c1f-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5c1f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d5c1f-112">Return value</span></span>

<span data-ttu-id="d5c1f-113">Si se ejecuta correctamente, devuelve un 0 (completado sin errores) o 4096 (trabajo iniciado). de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="d5c1f-113">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="d5c1f-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="d5c1f-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="d5c1f-115">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="d5c1f-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="d5c1f-116">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="d5c1f-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="d5c1f-117">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="d5c1f-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="d5c1f-118">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="d5c1f-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="d5c1f-119">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="d5c1f-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="d5c1f-120">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="d5c1f-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="d5c1f-121">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="d5c1f-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="d5c1f-122">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="d5c1f-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="d5c1f-123">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="d5c1f-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="d5c1f-124">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="d5c1f-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="d5c1f-125">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="d5c1f-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="d5c1f-126">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="d5c1f-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="d5c1f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5c1f-127">Requirements</span></span>



| <span data-ttu-id="d5c1f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5c1f-128">Requirement</span></span> | <span data-ttu-id="d5c1f-129">Value</span><span class="sxs-lookup"><span data-stu-id="d5c1f-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5c1f-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5c1f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d5c1f-131">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="d5c1f-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="d5c1f-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5c1f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d5c1f-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="d5c1f-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="d5c1f-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d5c1f-134">Namespace</span></span><br/>                | <span data-ttu-id="d5c1f-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="d5c1f-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d5c1f-136">MOF</span><span class="sxs-lookup"><span data-stu-id="d5c1f-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5c1f-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5c1f-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5c1f-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d5c1f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5c1f-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d5c1f-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d5c1f-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5c1f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5c1f-141">**MSVM \_ VirtualSystemReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="d5c1f-141">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




