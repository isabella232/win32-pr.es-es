---
description: Define un sistema virtual.
ms.assetid: c3964e99-9227-4b98-af87-7caa59296306
title: Método DefineSystem de la clase CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e38111d52044ed385fdd8cd19dd9094834e794c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687340"
---
# <a name="definesystem-method-of-the-cim_virtualsystemmanagementservice-class"></a><span data-ttu-id="c786e-103">Método DefineSystem de la \_ clase VirtualSystemManagementService de CIM</span><span class="sxs-lookup"><span data-stu-id="c786e-103">DefineSystem method of the CIM\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="c786e-104">Define un sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="c786e-104">Defines a virtual system.</span></span>

<span data-ttu-id="c786e-105">La entrada que no se ha especificado completamente puede rellenarse con valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="c786e-105">Input that is not completely specified may be filled out with default values.</span></span>

## <a name="syntax"></a><span data-ttu-id="c786e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c786e-106">Syntax</span></span>


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="c786e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c786e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c786e-108">*Configuración* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c786e-108">*SystemSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c786e-109">Cadena que contiene una instancia incrustada de la clase [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que se utiliza para definir los atributos del sistema virtual que se va a crear.</span><span class="sxs-lookup"><span data-stu-id="c786e-109">String containing an embedded instance of class [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) that is used to define attributes of the virtual system to be created.</span></span>

</dd> <dt>

<span data-ttu-id="c786e-110">*ResourceSettings* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c786e-110">*ResourceSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c786e-111">Matriz de cadenas que contiene una instancia incrustada de la clase [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que describe los aspectos virtuales de un recurso virtual que se va a crear en el ámbito del nuevo sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="c786e-111">Array of strings each containing an embedded instance of class [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) that describes the virtual aspects of a virtual resource to be created in the scope of the new virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="c786e-112">*ReferenceConfiguration* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c786e-112">*ReferenceConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c786e-113">Referencia a una instancia del objeto [**\_ VirtualSystemSettingDat de CIM**](cim-virtualsystemsettingdata.md) que es el objeto de nivel superior de una configuración de sistema virtual de referencia.</span><span class="sxs-lookup"><span data-stu-id="c786e-113">Reference to a [**CIM\_VirtualSystemSettingDat**](cim-virtualsystemsettingdata.md) object instance that is the top level object of a reference virtual system configuration.</span></span> <span data-ttu-id="c786e-114">La configuración de referencia se utiliza para complementar la configuración del nuevo sistema virtual si los parámetros *configuración* y *ResourceSettings* no proporcionaron la información correspondiente.</span><span class="sxs-lookup"><span data-stu-id="c786e-114">The reference configuration is used to complement the configuration of the new virtual system if the *SystemSettings* and *ResourceSettings* parameters did not provide respective information.</span></span>

</dd> <dt>

<span data-ttu-id="c786e-115">*ResultingSystem* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c786e-115">*ResultingSystem* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c786e-116">Si un equipo virtual se define correctamente, se devuelve una referencia a una instancia de la clase [**CIM \_ ComputerSystem**](cim-computersystem.md) que representa el sistema del equipo virtual recién definido.</span><span class="sxs-lookup"><span data-stu-id="c786e-116">If a virtual computer system is successfully defined, a reference to an instance of class [**CIM\_ComputerSystem**](cim-computersystem.md) that represents the newly defined virtual computer system is returned.</span></span>

</dd> <dt>

<span data-ttu-id="c786e-117">*Trabajo* \[ de enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c786e-117">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c786e-118">Si la operación es de larga ejecución, opcionalmente se puede devolver un trabajo.</span><span class="sxs-lookup"><span data-stu-id="c786e-118">If the operation is long running, then optionally a job may be returned.</span></span> <span data-ttu-id="c786e-119">En este caso, la instancia de la [**clase CIM \_ ComputerSystem**](cim-computersystem.md) que representa el nuevo sistema virtual se presenta a través de la Asociación [**CIM \_ AffectedJobElement**](cim-affectedjobelement.md) con la propiedad **AffectedElement** que hace referencia a la nueva instancia de la clase **CIM \_ ComputerSystem** y la propiedad **ElementEffects** establecida en 5 (Create).</span><span class="sxs-lookup"><span data-stu-id="c786e-119">In this case, the instance of class [**CIM\_ComputerSystem**](cim-computersystem.md) representing the new virtual system is presented via association [**CIM\_AffectedJobElement**](cim-affectedjobelement.md) with the property **AffectedElement** referring to the new instance of class **CIM\_ComputerSystem** and property **ElementEffects** set to 5 (Create).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c786e-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c786e-120">Return value</span></span>

<span data-ttu-id="c786e-121">Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="c786e-121">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="c786e-122">**Completado sin error** (0)</span><span class="sxs-lookup"><span data-stu-id="c786e-122">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c786e-123">**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="c786e-123">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c786e-124">**Error** (2)</span><span class="sxs-lookup"><span data-stu-id="c786e-124">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c786e-125">**Tiempo de espera** (3)</span><span class="sxs-lookup"><span data-stu-id="c786e-125">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c786e-126">**Parámetro no válido** (4)</span><span class="sxs-lookup"><span data-stu-id="c786e-126">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c786e-127">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="c786e-127">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c786e-128">**Parámetros de método comprobados: trabajo iniciado** (4096)</span><span class="sxs-lookup"><span data-stu-id="c786e-128">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c786e-129">**Método reservado** (de no.. 32767)</span><span class="sxs-lookup"><span data-stu-id="c786e-129">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="c786e-130">**Específico del proveedor** (32768... 65535)</span><span class="sxs-lookup"><span data-stu-id="c786e-130">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c786e-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c786e-131">Requirements</span></span>



| <span data-ttu-id="c786e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="c786e-132">Requirement</span></span> | <span data-ttu-id="c786e-133">Value</span><span class="sxs-lookup"><span data-stu-id="c786e-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c786e-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c786e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c786e-135">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="c786e-135">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="c786e-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c786e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c786e-137">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="c786e-137">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="c786e-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c786e-138">Namespace</span></span><br/>                | <span data-ttu-id="c786e-139">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="c786e-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c786e-140">MOF</span><span class="sxs-lookup"><span data-stu-id="c786e-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c786e-141"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c786e-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c786e-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c786e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c786e-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c786e-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c786e-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="c786e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c786e-145">**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="c786e-145">**CIM\_VirtualSystemManagementService**</span></span>](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




