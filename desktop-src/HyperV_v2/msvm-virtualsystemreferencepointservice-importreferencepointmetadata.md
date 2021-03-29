---
description: Importa los metadatos del punto de referencia del sistema virtual.
ms.assetid: 8e32fded-cd84-4586-83c4-c23200d4698e
title: Método ImportReferencePointMetadata de la clase Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ImportReferencePointMetadata
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c66a374247d324f5df192114d0b66adc3a17c5b0
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003416"
---
# <a name="importreferencepointmetadata-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="13475-103">Método ImportReferencePointMetadata de la \_ clase VirtualSystemReferencePointService de MSVM</span><span class="sxs-lookup"><span data-stu-id="13475-103">ImportReferencePointMetadata method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="13475-104">Importa los metadatos del punto de referencia del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="13475-104">Imports reference point metadata of the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="13475-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13475-105">Syntax</span></span>


```mof
uint32 ImportReferencePointMetadata(
  [in]  Msvm_ComputerSystem REF AffectedSystem,
  [in]  string                  ConfigFilePath,
  [in]  string                  RuntimeStateFilePath,
  [out] CIM_ConcreteJob     REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="13475-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="13475-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13475-107">*AffectedSystem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="13475-107">*AffectedSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13475-108">Una referencia a un [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que describe el sistema afectado.</span><span class="sxs-lookup"><span data-stu-id="13475-108">A reference to a [**Msvm\_ComputerSystem**](msvm-computersystem.md) describing the affected system.</span></span>

</dd> <dt>

<span data-ttu-id="13475-109">*ConfigFilePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="13475-109">*ConfigFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13475-110">Ruta de acceso completa del archivo de configuración desde donde se importarán los metadatos del punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="13475-110">The fully-qualified path of the config file from where the reference point metadata will be imported.</span></span>

</dd> <dt>

<span data-ttu-id="13475-111">*RuntimeStateFilePath* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="13475-111">*RuntimeStateFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13475-112">Ruta de acceso completa del archivo de estado en tiempo de ejecución desde el que se importarán los metadatos del punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="13475-112">The fully-qualified path of the runtime state file from where the reference point metadata will be imported.</span></span>

</dd> <dt>

<span data-ttu-id="13475-113">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="13475-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13475-114">Parámetro opcional para supervisar el progreso de la operación, que se utiliza si el método no se pudo ejecutar sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="13475-114">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="13475-115">Si la operación se ejecuta de forma asincrónica, el valor devuelto es 4096.</span><span class="sxs-lookup"><span data-stu-id="13475-115">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13475-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="13475-116">Return value</span></span>

<span data-ttu-id="13475-117">Devuelve 0 (sin errores) o uno de los siguientes mensajes de error:</span><span class="sxs-lookup"><span data-stu-id="13475-117">Returns either 0 (no error) or one of the following error messages:</span></span>

<dl> <dt>

<span data-ttu-id="13475-118">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="13475-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="13475-119">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="13475-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="13475-120">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="13475-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="13475-121">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="13475-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="13475-122">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="13475-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="13475-123">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="13475-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="13475-124">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="13475-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="13475-125">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="13475-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="13475-126">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="13475-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="13475-127">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="13475-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="13475-128">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="13475-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="13475-129">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="13475-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="13475-130">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="13475-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="13475-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13475-131">Requirements</span></span>



| <span data-ttu-id="13475-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="13475-132">Requirement</span></span> | <span data-ttu-id="13475-133">Value</span><span class="sxs-lookup"><span data-stu-id="13475-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13475-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13475-134">Minimum supported client</span></span><br/> | <span data-ttu-id="13475-135">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="13475-135">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="13475-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13475-136">Minimum supported server</span></span><br/> | <span data-ttu-id="13475-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="13475-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="13475-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="13475-138">Namespace</span></span><br/>                | <span data-ttu-id="13475-139">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="13475-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="13475-140">MOF</span><span class="sxs-lookup"><span data-stu-id="13475-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13475-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13475-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="13475-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="13475-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13475-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="13475-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="13475-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="13475-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13475-145">**MSVM \_ VirtualSystemReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="13475-145">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




