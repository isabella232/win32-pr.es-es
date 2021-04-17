---
description: Quita el registro de datos asociado al punto de referencia.
ms.assetid: b6206bda-c195-4c6f-9b80-508c20b53ce5
title: Método RemoveAssociatedData de la clase Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.RemoveAssociatedData
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c0d67502d349f0b0dac7cbf9a1998dcd6db0fb4a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105670087"
---
# <a name="removeassociateddata-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="2b57c-103">Método RemoveAssociatedData de la \_ clase VirtualSystemReferencePointService de MSVM</span><span class="sxs-lookup"><span data-stu-id="2b57c-103">RemoveAssociatedData method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="2b57c-104">Quita el registro de datos asociado al punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="2b57c-104">Removes the data log associated with the reference point.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b57c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b57c-105">Syntax</span></span>


```mof
uint32 RemoveAssociatedData(
  [in]  Msvm_VirtualSystemReferencePoint REF AffectedReferencePoint,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2b57c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b57c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b57c-107">*AffectedReferencePoint* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2b57c-107">*AffectedReferencePoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b57c-108">Referencia a la instancia [**de \_ VirtualSystemReferencePoint de MSVM**](msvm-virtualsystemreferencepoint.md) que representa el punto de referencia que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="2b57c-108">A reference to the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance which represents the reference point to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="2b57c-109">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="2b57c-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b57c-110">Parámetro opcional para supervisar el progreso de la operación, que se utiliza si el método no se pudo ejecutar sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="2b57c-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="2b57c-111">Si la operación se ejecuta de forma asincrónica, el valor devuelto es 4096.</span><span class="sxs-lookup"><span data-stu-id="2b57c-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b57c-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b57c-112">Return value</span></span>

<span data-ttu-id="2b57c-113">Si se ejecuta correctamente, devuelve un 0 (completado sin errores) o 4096 (trabajo iniciado). de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="2b57c-113">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="2b57c-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="2b57c-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2b57c-115">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="2b57c-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2b57c-116">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="2b57c-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="2b57c-117">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="2b57c-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="2b57c-118">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="2b57c-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="2b57c-119">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="2b57c-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="2b57c-120">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="2b57c-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="2b57c-121">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="2b57c-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="2b57c-122">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="2b57c-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="2b57c-123">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="2b57c-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="2b57c-124">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="2b57c-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="2b57c-125">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="2b57c-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="2b57c-126">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="2b57c-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2b57c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b57c-127">Requirements</span></span>



| <span data-ttu-id="2b57c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b57c-128">Requirement</span></span> | <span data-ttu-id="2b57c-129">Value</span><span class="sxs-lookup"><span data-stu-id="2b57c-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b57c-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b57c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2b57c-131">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="2b57c-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="2b57c-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b57c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2b57c-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2b57c-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="2b57c-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2b57c-134">Namespace</span></span><br/>                | <span data-ttu-id="2b57c-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="2b57c-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2b57c-136">MOF</span><span class="sxs-lookup"><span data-stu-id="2b57c-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2b57c-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2b57c-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2b57c-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2b57c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b57c-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2b57c-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2b57c-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b57c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b57c-141">**MSVM \_ VirtualSystemReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="2b57c-141">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




