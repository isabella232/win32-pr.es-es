---
description: Actualiza el nombre de elemento para el \_ objeto CIM CollectionOfMSEs especificado.
ms.assetid: 03d3979b-f3d2-4192-8bba-bdf4a19aa47c
title: Método RenameCollection de la clase Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.RenameCollection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e4bb127fc8fba528e883631602fcea8ba0b4de2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912585"
---
# <a name="renamecollection-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="466ab-103">Método RenameCollection de la \_ clase CollectionManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="466ab-103">RenameCollection method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="466ab-104">Actualiza el nombre de elemento para el objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="466ab-104">Updates the element name for the specified [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="466ab-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="466ab-105">Syntax</span></span>


```mof
uint32 RenameCollection(
  [in]  CIM_CollectionOfMSEs REF Collection,
  [in]  string                   NewName,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="466ab-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="466ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="466ab-107">*Colección* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="466ab-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="466ab-108">Colección a la que se va a cambiar el nombre.</span><span class="sxs-lookup"><span data-stu-id="466ab-108">The collection to rename.</span></span>

</dd> <dt>

<span data-ttu-id="466ab-109">*NewName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="466ab-109">*NewName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="466ab-110">Nuevo nombre que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="466ab-110">The new name to use.</span></span>

</dd> <dt>

<span data-ttu-id="466ab-111">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="466ab-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="466ab-112">Referencia al trabajo (puede ser null si se ha completado la tarea).</span><span class="sxs-lookup"><span data-stu-id="466ab-112">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="466ab-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="466ab-113">Return value</span></span>

<span data-ttu-id="466ab-114">Devuelve 0 si se realiza correctamente, o 4096 si se inició el trabajo; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="466ab-114">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="466ab-115">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="466ab-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="466ab-116">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="466ab-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="466ab-117">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="466ab-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="466ab-118">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="466ab-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="466ab-119">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="466ab-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="466ab-120">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="466ab-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="466ab-121">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="466ab-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="466ab-122">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="466ab-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="466ab-123">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="466ab-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="466ab-124">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="466ab-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="466ab-125">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="466ab-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="466ab-126">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="466ab-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="466ab-127">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="466ab-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="466ab-128">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="466ab-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="466ab-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="466ab-129">Requirements</span></span>



| <span data-ttu-id="466ab-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="466ab-130">Requirement</span></span> | <span data-ttu-id="466ab-131">Value</span><span class="sxs-lookup"><span data-stu-id="466ab-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="466ab-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="466ab-132">Minimum supported client</span></span><br/> | <span data-ttu-id="466ab-133">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="466ab-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="466ab-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="466ab-134">Minimum supported server</span></span><br/> | <span data-ttu-id="466ab-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="466ab-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="466ab-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="466ab-136">Namespace</span></span><br/>                | <span data-ttu-id="466ab-137">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="466ab-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="466ab-138">MOF</span><span class="sxs-lookup"><span data-stu-id="466ab-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="466ab-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="466ab-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="466ab-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="466ab-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="466ab-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="466ab-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="466ab-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="466ab-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="466ab-143">**MSVM \_ CollectionManagementService**</span><span class="sxs-lookup"><span data-stu-id="466ab-143">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




