---
description: Busca un \_ objeto MSVM MountedStorageImage para una ruta de acceso de imagen de disco determinada.
ms.assetid: 498ed285-2b5b-472b-b0ee-649c97b61274
title: Método FindMountedStorageImageInstance de la clase Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.FindMountedStorageImageInstance
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 80462fb57be8c3f89764774ea68e73a988f11643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542470"
---
# <a name="findmountedstorageimageinstance-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="14d4b-103">Método FindMountedStorageImageInstance de la \_ clase ImageManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="14d4b-103">FindMountedStorageImageInstance method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="14d4b-104">Busca un objeto [**MSVM \_ MountedStorageImage**](msvm-mountedstorageimage.md) para una ruta de acceso de imagen de disco determinada.</span><span class="sxs-lookup"><span data-stu-id="14d4b-104">Finds an [**Msvm\_MountedStorageImage**](msvm-mountedstorageimage.md) object for a given disk image path.</span></span>

## <a name="syntax"></a><span data-ttu-id="14d4b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="14d4b-105">Syntax</span></span>


```mof
uint32 FindMountedStorageImageInstance(
  [in]  string                       SelectionCriterion,
  [in]  uint16                       CriterionType,
  [out] Msvm_MountedStorageImage REF Image
);
```



## <a name="parameters"></a><span data-ttu-id="14d4b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="14d4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14d4b-107">*SelectionCriterion* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="14d4b-107">*SelectionCriterion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14d4b-108">Ruta de acceso completa que especifica la ubicación de un archivo de imagen de disco.</span><span class="sxs-lookup"><span data-stu-id="14d4b-108">A fully-qualified path that specifies the location of a disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="14d4b-109">*CriterionType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="14d4b-109">*CriterionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14d4b-110">Tipo de criterio que se va a buscar al buscar la imagen de disco.</span><span class="sxs-lookup"><span data-stu-id="14d4b-110">The type of criterion to look for when finding the disk image.</span></span>

<dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="14d4b-111">**desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="14d4b-111">**unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>

<span data-ttu-id="14d4b-112">**Ruta de acceso** (2)</span><span class="sxs-lookup"><span data-stu-id="14d4b-112">**Path** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="14d4b-113">*Imagen* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="14d4b-113">*Image* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14d4b-114">Una referencia a [**MSVM \_ MountedStorageImage**](msvm-mountedstorageimage.md) (puede ser null si la imagen no está montada).</span><span class="sxs-lookup"><span data-stu-id="14d4b-114">A reference to the [**Msvm\_MountedStorageImage**](msvm-mountedstorageimage.md) (can be null if the image is not mounted).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14d4b-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14d4b-115">Return value</span></span>

<span data-ttu-id="14d4b-116">Este método devuelve uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="14d4b-116">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="14d4b-117">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="14d4b-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="14d4b-118">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="14d4b-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="14d4b-119">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="14d4b-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="14d4b-120">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="14d4b-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="14d4b-121">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="14d4b-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="14d4b-122">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="14d4b-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="14d4b-123">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="14d4b-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="14d4b-124">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="14d4b-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="14d4b-125">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="14d4b-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="14d4b-126">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="14d4b-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="14d4b-127">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="14d4b-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="14d4b-128">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="14d4b-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="14d4b-129">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="14d4b-129">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="14d4b-130">**Objeto no encontrado** (32789)</span><span class="sxs-lookup"><span data-stu-id="14d4b-130">**Object not found** (32789)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="14d4b-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14d4b-131">Requirements</span></span>



| <span data-ttu-id="14d4b-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="14d4b-132">Requirement</span></span> | <span data-ttu-id="14d4b-133">Value</span><span class="sxs-lookup"><span data-stu-id="14d4b-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14d4b-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14d4b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="14d4b-135">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="14d4b-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="14d4b-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="14d4b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="14d4b-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="14d4b-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="14d4b-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="14d4b-138">Namespace</span></span><br/>                | <span data-ttu-id="14d4b-139">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="14d4b-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="14d4b-140">MOF</span><span class="sxs-lookup"><span data-stu-id="14d4b-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="14d4b-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="14d4b-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="14d4b-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="14d4b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14d4b-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="14d4b-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="14d4b-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="14d4b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14d4b-145">**MSVM \_ ImageManagementService**</span><span class="sxs-lookup"><span data-stu-id="14d4b-145">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




