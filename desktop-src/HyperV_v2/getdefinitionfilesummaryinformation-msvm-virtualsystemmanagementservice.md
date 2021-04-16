---
description: Devuelve información de Resumen de la máquina virtual para los archivos de definición de máquina virtual especificados.
ms.assetid: 5a3d7f2c-3b89-4dd6-909d-4452afc3705f
title: Método GetDefinitionFileSummaryInformation de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetDefinitionFileSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a46daedd282d07c2367931a9f20a7fbfa1849f9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686892"
---
# <a name="getdefinitionfilesummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="e855d-103">Método GetDefinitionFileSummaryInformation de la \_ clase VirtualSystemManagementService de MSVM</span><span class="sxs-lookup"><span data-stu-id="e855d-103">GetDefinitionFileSummaryInformation method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="e855d-104">Devuelve información de Resumen de la máquina virtual para los archivos de definición de máquina virtual especificados.</span><span class="sxs-lookup"><span data-stu-id="e855d-104">Returns virtual machine summary information for the specified virtual machine definition files.</span></span>

## <a name="syntax"></a><span data-ttu-id="e855d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e855d-105">Syntax</span></span>


```mof
uint32 GetDefinitionFileSummaryInformation(
  [in]  string                      DefinitionFiles[],
  [out] Msvm_SummaryInformationBase SummaryInformation[]
);
```



## <a name="parameters"></a><span data-ttu-id="e855d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e855d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e855d-107">*DefinitionFiles* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e855d-107">*DefinitionFiles* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e855d-108">Matriz de rutas de acceso a los archivos de configuración XML para los que se va a devolver información de resumen.</span><span class="sxs-lookup"><span data-stu-id="e855d-108">An array of paths to XML configuration files for which to return summary information.</span></span>

</dd> <dt>

<span data-ttu-id="e855d-109">*SummaryInformation* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="e855d-109">*SummaryInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e855d-110">Una matriz de instancias de [**MSVM \_ SummaryInformationBase**](msvm-summaryinformation.md) que contiene la información solicitada para las máquinas virtuales y/o las instantáneas especificadas en la matriz *DefinitionFiles* .</span><span class="sxs-lookup"><span data-stu-id="e855d-110">An array of [**Msvm\_SummaryInformationBase**](msvm-summaryinformation.md) instances containing the requested information for the virtual machines and/or snapshots specified in the *DefinitionFiles* array.</span></span> <span data-ttu-id="e855d-111">Solo se devuelven las propiedades **Name**, **ElementName**, **CreationTime** y **Notes** , todas las demás propiedades serán **null**.</span><span class="sxs-lookup"><span data-stu-id="e855d-111">Only the **Name**, **ElementName**, **CreationTime**, and **Notes** properties are returned, all other properties will be **Null**.</span></span>

> [!Note]  

 

<span data-ttu-id="e855d-112">Antes de Windows 10, versión 1703, DataType era [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md).</span><span class="sxs-lookup"><span data-stu-id="e855d-112">Prior to Windows 10, version 1703, datatype was [**Msvm\_SummaryInformation**](msvm-summaryinformation.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e855d-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e855d-113">Return value</span></span>

<span data-ttu-id="e855d-114">Este método devuelve uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e855d-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="e855d-115">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="e855d-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e855d-116">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="e855d-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="e855d-117">**Error** (32768)</span><span class="sxs-lookup"><span data-stu-id="e855d-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="e855d-118">**Acceso denegado** (32769)</span><span class="sxs-lookup"><span data-stu-id="e855d-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="e855d-119">**No compatible** (32770)</span><span class="sxs-lookup"><span data-stu-id="e855d-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="e855d-120">**Estado desconocido** (32771)</span><span class="sxs-lookup"><span data-stu-id="e855d-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="e855d-121">**Tiempo de espera** (32772)</span><span class="sxs-lookup"><span data-stu-id="e855d-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="e855d-122">**Parámetro no válido** (32773)</span><span class="sxs-lookup"><span data-stu-id="e855d-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="e855d-123">El **sistema está en uso** (32774)</span><span class="sxs-lookup"><span data-stu-id="e855d-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="e855d-124">**Estado no válido para esta operación** (32775)</span><span class="sxs-lookup"><span data-stu-id="e855d-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="e855d-125">**Tipo de datos incorrecto** (32776)</span><span class="sxs-lookup"><span data-stu-id="e855d-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="e855d-126">El **sistema no está disponible** (32777)</span><span class="sxs-lookup"><span data-stu-id="e855d-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="e855d-127">**Memoria insuficiente** (32778)</span><span class="sxs-lookup"><span data-stu-id="e855d-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e855d-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e855d-128">Requirements</span></span>



| <span data-ttu-id="e855d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="e855d-129">Requirement</span></span> | <span data-ttu-id="e855d-130">Value</span><span class="sxs-lookup"><span data-stu-id="e855d-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e855d-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e855d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e855d-132">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="e855d-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e855d-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e855d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e855d-134">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e855d-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e855d-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e855d-135">Namespace</span></span><br/>                | <span data-ttu-id="e855d-136">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="e855d-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e855d-137">MOF</span><span class="sxs-lookup"><span data-stu-id="e855d-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e855d-138"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e855d-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e855d-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e855d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e855d-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e855d-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e855d-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="e855d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e855d-142">**MSVM \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="e855d-142">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




