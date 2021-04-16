---
description: Elimina el \_ objeto CIM CollectionOfMSEs determinado.
ms.assetid: 2c79e281-44c3-4a91-98d5-fdf973d149c3
title: Método DestroyCollection de la clase Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.DestroyCollection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 69b35bfac3601bd92bc7b1fea967de404b716773
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688722"
---
# <a name="destroycollection-method-of-the-msvm_collectionmanagementservice-class"></a><span data-ttu-id="f97de-103">Método DestroyCollection de la \_ clase CollectionManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="f97de-103">DestroyCollection method of the Msvm\_CollectionManagementService class</span></span>

<span data-ttu-id="f97de-104">Elimina el objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) determinado.</span><span class="sxs-lookup"><span data-stu-id="f97de-104">Deletes the given [**CIM\_CollectionOfMSEs**](cim-collectionofmses.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f97de-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f97de-105">Syntax</span></span>


```mof
uint32 DestroyCollection(
  [in]  CIM_CollectionOfMSEs REF Collection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f97de-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f97de-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f97de-107">*Colección* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="f97de-107">*Collection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f97de-108">Colección que se va a destruir.</span><span class="sxs-lookup"><span data-stu-id="f97de-108">The collection to destroy.</span></span>

</dd> <dt>

<span data-ttu-id="f97de-109">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="f97de-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f97de-110">Referencia al trabajo (puede ser null si se ha completado la tarea).</span><span class="sxs-lookup"><span data-stu-id="f97de-110">A reference to the job (can be null if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f97de-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f97de-111">Return value</span></span>

<span data-ttu-id="f97de-112">Devuelve 0 si se realiza correctamente, o 4096 si se inició el trabajo; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="f97de-112">Returns 0 if successful, or 4096 if the job started; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="f97de-113">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="f97de-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f97de-114">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="f97de-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f97de-115">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="f97de-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f97de-116">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="f97de-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f97de-117">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="f97de-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f97de-118">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="f97de-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f97de-119">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="f97de-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f97de-120">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="f97de-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f97de-121">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="f97de-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f97de-122">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="f97de-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f97de-123">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="f97de-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f97de-124">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="f97de-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f97de-125">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="f97de-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="f97de-126">**No se encontró el archivo** (32779)</span><span class="sxs-lookup"><span data-stu-id="f97de-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f97de-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f97de-127">Requirements</span></span>



| <span data-ttu-id="f97de-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="f97de-128">Requirement</span></span> | <span data-ttu-id="f97de-129">Value</span><span class="sxs-lookup"><span data-stu-id="f97de-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f97de-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f97de-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f97de-131">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="f97de-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="f97de-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f97de-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f97de-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f97de-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f97de-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f97de-134">Namespace</span></span><br/>                | <span data-ttu-id="f97de-135">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f97de-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f97de-136">MOF</span><span class="sxs-lookup"><span data-stu-id="f97de-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f97de-137"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f97de-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f97de-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f97de-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f97de-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f97de-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f97de-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="f97de-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f97de-141">**MSVM \_ CollectionManagementService**</span><span class="sxs-lookup"><span data-stu-id="f97de-141">**Msvm\_CollectionManagementService**</span></span>](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




