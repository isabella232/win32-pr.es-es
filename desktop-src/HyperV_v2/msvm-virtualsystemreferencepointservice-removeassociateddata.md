---
description: 'Método RemoveAssociatedData de la clase Msvm_VirtualSystemReferencePointService : quita el registro de datos asociado al punto de referencia.'
ms.assetid: b6206bda-c195-4c6f-9b80-508c20b53ce5
title: Método RemoveAssociatedData de la Msvm_VirtualSystemReferencePointService clase
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
ms.openlocfilehash: b5291e4e018edc89909ccde36ce0e420698af8e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118623"
---
# <a name="removeassociateddata-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="a61bf-103">Método RemoveAssociatedData de la clase Msvm \_ VirtualSystemReferencePointService</span><span class="sxs-lookup"><span data-stu-id="a61bf-103">RemoveAssociatedData method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="a61bf-104">Quita el registro de datos asociado al punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="a61bf-104">Removes the data log associated with the reference point.</span></span>

## <a name="syntax"></a><span data-ttu-id="a61bf-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a61bf-105">Syntax</span></span>


```mof
uint32 RemoveAssociatedData(
  [in]  Msvm_VirtualSystemReferencePoint REF AffectedReferencePoint,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a61bf-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a61bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a61bf-107">*AffectedReferencePoint* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="a61bf-107">*AffectedReferencePoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a61bf-108">Referencia a la instancia [**de Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) que representa el punto de referencia que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="a61bf-108">A reference to the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance which represents the reference point to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="a61bf-109">*Trabajo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a61bf-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a61bf-110">Parámetro opcional para supervisar el progreso de la operación, que se usa si el método no se pudo ejecutar sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="a61bf-110">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="a61bf-111">Si la operación se ejecuta de forma asincrónica, el valor devuelto es 4096.</span><span class="sxs-lookup"><span data-stu-id="a61bf-111">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a61bf-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a61bf-112">Return value</span></span>

<span data-ttu-id="a61bf-113">Si se ejecuta correctamente, devuelve 0 (completado sin error) o 4096 (trabajo iniciado); de lo contrario, devuelva un error.</span><span class="sxs-lookup"><span data-stu-id="a61bf-113">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="a61bf-114">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="a61bf-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a61bf-115">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="a61bf-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a61bf-116">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="a61bf-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a61bf-117">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="a61bf-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a61bf-118">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="a61bf-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a61bf-119">**El estado es desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="a61bf-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a61bf-120">**Tiempo de** espera (32772)</span><span class="sxs-lookup"><span data-stu-id="a61bf-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a61bf-121">**Parámetro no** válido (32773)</span><span class="sxs-lookup"><span data-stu-id="a61bf-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a61bf-122">**El sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="a61bf-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a61bf-123">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="a61bf-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a61bf-124">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="a61bf-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a61bf-125">**El sistema no está** disponible (32777)</span><span class="sxs-lookup"><span data-stu-id="a61bf-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a61bf-126">**Memoria sin memoria** (32778)</span><span class="sxs-lookup"><span data-stu-id="a61bf-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a61bf-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a61bf-127">Requirements</span></span>



| <span data-ttu-id="a61bf-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="a61bf-128">Requirement</span></span> | <span data-ttu-id="a61bf-129">Valor</span><span class="sxs-lookup"><span data-stu-id="a61bf-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a61bf-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a61bf-130">Minimum supported client</span></span><br/> | <span data-ttu-id="a61bf-131">Windows 10 solo \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="a61bf-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="a61bf-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a61bf-132">Minimum supported server</span></span><br/> | <span data-ttu-id="a61bf-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a61bf-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="a61bf-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a61bf-134">Namespace</span></span><br/>                | <span data-ttu-id="a61bf-135">Virtualización \\ raíz \\ v2</span><span class="sxs-lookup"><span data-stu-id="a61bf-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a61bf-136">MOF</span><span class="sxs-lookup"><span data-stu-id="a61bf-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a61bf-137"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="a61bf-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a61bf-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a61bf-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a61bf-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a61bf-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a61bf-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a61bf-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a61bf-141">**Msvm \_ VirtualSystemReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="a61bf-141">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




