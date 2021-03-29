---
description: Valida si un sistema de archivos puede admitir un disco duro virtual con reservas persistentes habilitadas.
ms.assetid: c5fed9d5-0fa6-4b96-ae6e-84468b011e2a
title: Método ValidatePersistentReservationSupport de la clase Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ValidatePersistentReservationSupport
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 596e5cf840ee65dc0b3ad5315462db4666c8b262
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001252"
---
# <a name="validatepersistentreservationsupport-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="ded42-103">Método ValidatePersistentReservationSupport de la \_ clase ImageManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="ded42-103">ValidatePersistentReservationSupport method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="ded42-104">Valida si un sistema de archivos puede admitir un disco duro virtual con reservas persistentes habilitadas.</span><span class="sxs-lookup"><span data-stu-id="ded42-104">Validates whether a file system can support a virtual hard disk with persistent reservations enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="ded42-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ded42-105">Syntax</span></span>


```mof
uint32 ValidatePersistentReservationSupport(
  [in]  string              Path,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ded42-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ded42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ded42-107">*Ruta de acceso* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ded42-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ded42-108">Ruta de acceso completa que especifica la ubicación de un archivo de imagen de disco o un directorio en el que se puede colocar un archivo de imagen de disco.</span><span class="sxs-lookup"><span data-stu-id="ded42-108">A fully-qualified path that specifies the location of a disk image file or a directory in which a disk image file might be placed.</span></span>

</dd> <dt>

<span data-ttu-id="ded42-109">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="ded42-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ded42-110">Referencia al trabajo (puede ser null si la tarea se ha completado correctamente).</span><span class="sxs-lookup"><span data-stu-id="ded42-110">A reference to the job (can be null if the task is completed succesfully).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ded42-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ded42-111">Return value</span></span>

<span data-ttu-id="ded42-112">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="ded42-112">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="ded42-113">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="ded42-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ded42-114">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="ded42-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="ded42-115">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="ded42-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="ded42-116">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="ded42-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="ded42-117">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="ded42-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="ded42-118">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="ded42-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="ded42-119">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="ded42-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="ded42-120">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="ded42-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="ded42-121">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="ded42-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="ded42-122">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="ded42-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="ded42-123">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="ded42-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="ded42-124">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="ded42-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="ded42-125">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="ded42-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="ded42-126">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="ded42-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ded42-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ded42-127">Requirements</span></span>



| <span data-ttu-id="ded42-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ded42-128">Requirement</span></span> | <span data-ttu-id="ded42-129">Value</span><span class="sxs-lookup"><span data-stu-id="ded42-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ded42-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ded42-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ded42-131">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ded42-131">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ded42-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ded42-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ded42-133">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ded42-133">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ded42-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ded42-134">Namespace</span></span><br/>                | <span data-ttu-id="ded42-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ded42-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ded42-136">MOF</span><span class="sxs-lookup"><span data-stu-id="ded42-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ded42-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ded42-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ded42-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ded42-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ded42-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ded42-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ded42-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="ded42-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ded42-141">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="ded42-141">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




