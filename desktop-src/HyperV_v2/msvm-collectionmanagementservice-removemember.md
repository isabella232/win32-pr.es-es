---
description: Quita el elemento administrado especificado como miembro del objeto CIM CollectionOfMSEs determinado \_ .
ms.assetid: ea945d24-bcff-476b-9adb-c6573cdbc0b5
title: Método RemoveMember de la clase Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.RemoveMember
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 894230dcf5e9a537ca444815f8e941a8e6fcf09a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912586"
---
# <a name="removemember-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="6c77f-103">Método RemoveMember de la \_ clase CollectionManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="6c77f-103">RemoveMember method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="6c77f-104">Quita el elemento administrado especificado como miembro del objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) determinado.</span><span class="sxs-lookup"><span data-stu-id="6c77f-104">Removes the specified managed element as a member of the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c77f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6c77f-105">Syntax</span></span>


```mof
uint32 RemoveMember(
  [in]  CIM_ManagedElement   REF Member,
  [in]  CIM_CollectionOfMSEs REF Collection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="6c77f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6c77f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c77f-107">*Miembro* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6c77f-107">*Member* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c77f-108">Miembro que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="6c77f-108">The member to remove.</span></span>

</dd> <dt>

<span data-ttu-id="6c77f-109">*Colección* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6c77f-109">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c77f-110">Colección de la que se va a quitar el miembro.</span><span class="sxs-lookup"><span data-stu-id="6c77f-110">The collection to remove the member from.</span></span>

</dd> <dt>

<span data-ttu-id="6c77f-111">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="6c77f-111">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c77f-112">Referencia al trabajo (puede ser null si se ha completado la tarea).</span><span class="sxs-lookup"><span data-stu-id="6c77f-112">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c77f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6c77f-113">Return value</span></span>

<span data-ttu-id="6c77f-114">Devuelve 0 si se realiza correctamente, o 4096 si se inició el trabajo; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="6c77f-114">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="6c77f-115">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="6c77f-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6c77f-116">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="6c77f-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="6c77f-117">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="6c77f-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6c77f-118">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="6c77f-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6c77f-119">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="6c77f-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6c77f-120">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="6c77f-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6c77f-121">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="6c77f-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6c77f-122">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="6c77f-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6c77f-123">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="6c77f-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6c77f-124">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="6c77f-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6c77f-125">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="6c77f-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6c77f-126">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="6c77f-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6c77f-127">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="6c77f-127">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="6c77f-128">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="6c77f-128">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="6c77f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c77f-129">Requirements</span></span>



| <span data-ttu-id="6c77f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c77f-130">Requirement</span></span> | <span data-ttu-id="6c77f-131">Value</span><span class="sxs-lookup"><span data-stu-id="6c77f-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c77f-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c77f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6c77f-133">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="6c77f-133">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="6c77f-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c77f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6c77f-135">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6c77f-135">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="6c77f-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6c77f-136">Namespace</span></span><br/>                | <span data-ttu-id="6c77f-137">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="6c77f-137">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6c77f-138">MOF</span><span class="sxs-lookup"><span data-stu-id="6c77f-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6c77f-139"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6c77f-139"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6c77f-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6c77f-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c77f-141"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6c77f-141"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6c77f-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c77f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c77f-143">**MSVM \_ CollectionManagementService**</span><span class="sxs-lookup"><span data-stu-id="6c77f-143">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




