---
description: Exporta el punto de referencia del sistema virtual.
ms.assetid: e4d80404-6b1b-4153-9ab2-aebab18c331a
title: Método ExportReferencePoint de la clase Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ExportReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bedd051123e4f75d7438b2e3831a84204ff4aec3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105670074"
---
# <a name="exportreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a><span data-ttu-id="cb3d4-103">Método ExportReferencePoint de la \_ clase VirtualSystemReferencePointService de MSVM</span><span class="sxs-lookup"><span data-stu-id="cb3d4-103">ExportReferencePoint method of the Msvm\_VirtualSystemReferencePointService class</span></span>

<span data-ttu-id="cb3d4-104">Exporta el punto de referencia del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="cb3d4-104">Exports the reference point of the virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb3d4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cb3d4-105">Syntax</span></span>


```mof
uint32 ExportReferencePoint(
  [in]  Msvm_VirtualSystemReferencePoint REF ReferencePoint,
  [in]  string                               ExportDirectory,
  [in]  string                               ExportSettingData,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="cb3d4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cb3d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb3d4-107">*ReferencePoint* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb3d4-107">*ReferencePoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3d4-108">Referencia a la instancia [**de \_ VirtualSystemReferencePoint de MSVM**](msvm-virtualsystemreferencepoint.md) que representa el punto de referencia que se va a exportar.</span><span class="sxs-lookup"><span data-stu-id="cb3d4-108">A reference to the [**Msvm\_VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) instance which represents the reference point to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="cb3d4-109">*ExportDirectory* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb3d4-109">*ExportDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3d4-110">Ruta de acceso completa del directorio al que se va a exportar el punto de referencia.</span><span class="sxs-lookup"><span data-stu-id="cb3d4-110">The fully-qualified path of the directory to which the reference point is to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="cb3d4-111">*ExportSettingData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="cb3d4-111">*ExportSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3d4-112">Instancia de [**MSVM \_ VirtualSystemReferencePointExportSettingData**](msvm-virtualsystemreferencepointexportsettingdata.md) que representa la configuración de la operación de exportación.</span><span class="sxs-lookup"><span data-stu-id="cb3d4-112">An instance of [**Msvm\_VirtualSystemReferencePointExportSettingData**](msvm-virtualsystemreferencepointexportsettingdata.md) that represents the settings for the export operation.</span></span>

</dd> <dt>

<span data-ttu-id="cb3d4-113">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="cb3d4-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb3d4-114">Parámetro opcional para supervisar el progreso de la operación, que se utiliza si el método no se pudo ejecutar sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="cb3d4-114">An optional parameter for monitoring progress of the operation, which is used if the method could not be executed synchronously.</span></span> <span data-ttu-id="cb3d4-115">Si la operación se ejecuta de forma asincrónica, el valor devuelto es 4096.</span><span class="sxs-lookup"><span data-stu-id="cb3d4-115">If the operation is executing asynchronously, the return value is 4096.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb3d4-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cb3d4-116">Return value</span></span>

<span data-ttu-id="cb3d4-117">Si se ejecuta correctamente, devuelve un 0 (completado sin errores) o 4096 (trabajo iniciado). de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="cb3d4-117">On success, returns a 0 (Complete with No Error), or 4096 (Job Started); otherwise, return an error.</span></span>

<dl> <dt>

<span data-ttu-id="cb3d4-118">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="cb3d4-118">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cb3d4-119">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="cb3d4-119">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="cb3d4-120">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="cb3d4-120">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="cb3d4-121">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="cb3d4-121">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="cb3d4-122">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="cb3d4-122">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="cb3d4-123">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="cb3d4-123">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="cb3d4-124">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="cb3d4-124">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="cb3d4-125">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="cb3d4-125">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="cb3d4-126">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="cb3d4-126">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="cb3d4-127">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="cb3d4-127">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="cb3d4-128">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="cb3d4-128">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="cb3d4-129">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="cb3d4-129">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="cb3d4-130">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="cb3d4-130">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="cb3d4-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb3d4-131">Requirements</span></span>



| <span data-ttu-id="cb3d4-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb3d4-132">Requirement</span></span> | <span data-ttu-id="cb3d4-133">Value</span><span class="sxs-lookup"><span data-stu-id="cb3d4-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb3d4-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb3d4-134">Minimum supported client</span></span><br/> | <span data-ttu-id="cb3d4-135">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb3d4-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="cb3d4-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb3d4-136">Minimum supported server</span></span><br/> | <span data-ttu-id="cb3d4-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="cb3d4-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="cb3d4-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cb3d4-138">Namespace</span></span><br/>                | <span data-ttu-id="cb3d4-139">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="cb3d4-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cb3d4-140">MOF</span><span class="sxs-lookup"><span data-stu-id="cb3d4-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb3d4-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb3d4-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb3d4-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cb3d4-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb3d4-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cb3d4-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cb3d4-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="cb3d4-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb3d4-145">**MSVM \_ VirtualSystemReferencePointService**</span><span class="sxs-lookup"><span data-stu-id="cb3d4-145">**Msvm\_VirtualSystemReferencePointService**</span></span>](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




