---
description: Describe los datos de configuración de un controlador de pantalla sintético virtual.
ms.assetid: cea79b24-4175-49db-a8b4-a9efb1fd0b96
title: Msvm_SyntheticDisplayControllerSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticDisplayControllerSettingData
- Msvm_SyntheticDisplayControllerSettingData.ResolutionType
- Msvm_SyntheticDisplayControllerSettingData.HorizontalResolution
- Msvm_SyntheticDisplayControllerSettingData.VerticalResolution
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 52935800eda641eb9015247e9320f33f22b40251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276178"
---
# <a name="msvm_syntheticdisplaycontrollersettingdata-class"></a><span data-ttu-id="df381-103">MSVM \_ SyntheticDisplayControllerSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="df381-103">Msvm\_SyntheticDisplayControllerSettingData class</span></span>

<span data-ttu-id="df381-104">Describe los datos de configuración de un controlador de pantalla sintético virtual.</span><span class="sxs-lookup"><span data-stu-id="df381-104">Describes the setting data for a virtual synthetic display controller.</span></span>

<span data-ttu-id="df381-105">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="df381-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="df381-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="df381-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticDisplayControllerSettingData : CIM_ResourceAllocationSettingData
{
  uint8  ResolutionType;
  uint16 HorizontalResolution;
  uint16 VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="df381-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="df381-107">Members</span></span>

<span data-ttu-id="df381-108">La clase **MSVM \_ SyntheticDisplayControllerSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="df381-108">The **Msvm\_SyntheticDisplayControllerSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="df381-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="df381-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="df381-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="df381-110">Properties</span></span>

<span data-ttu-id="df381-111">La clase **MSVM \_ SyntheticDisplayControllerSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="df381-111">The **Msvm\_SyntheticDisplayControllerSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="df381-112">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="df381-112">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df381-113">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df381-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df381-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="df381-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="df381-115">Resolución horizontal.</span><span class="sxs-lookup"><span data-stu-id="df381-115">The horizontal resolution.</span></span>

</dd> <dt>

<span data-ttu-id="df381-116">**ResolutionType**</span><span class="sxs-lookup"><span data-stu-id="df381-116">**ResolutionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df381-117">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="df381-117">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="df381-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="df381-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="df381-119">El tipo de resolución.</span><span class="sxs-lookup"><span data-stu-id="df381-119">The resolution type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="df381-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="df381-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="df381-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="df381-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="df381-122"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Máximo** (2)</span><span class="sxs-lookup"><span data-stu-id="df381-122"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Single"></span><span id="single"></span><span id="SINGLE"></span>

<span data-ttu-id="df381-123"><span id="Single"></span><span id="single"></span><span id="SINGLE"></span>**Single** (3)</span><span class="sxs-lookup"><span data-stu-id="df381-123"><span id="Single"></span><span id="single"></span><span id="SINGLE"></span>**Single** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="df381-124"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Valor predeterminado** (4)</span><span class="sxs-lookup"><span data-stu-id="df381-124"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Default** (4)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="df381-125">Agregado en Windows 10, versión 1703.</span><span class="sxs-lookup"><span data-stu-id="df381-125">Added in Windows 10, version 1703.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="df381-126">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="df381-126">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="df381-127">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="df381-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="df381-128">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="df381-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="df381-129">Resolución vertical.</span><span class="sxs-lookup"><span data-stu-id="df381-129">The vertical resolution.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="df381-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df381-130">Requirements</span></span>



| <span data-ttu-id="df381-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="df381-131">Requirement</span></span> | <span data-ttu-id="df381-132">Value</span><span class="sxs-lookup"><span data-stu-id="df381-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df381-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df381-133">Minimum supported client</span></span><br/> | <span data-ttu-id="df381-134">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="df381-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="df381-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="df381-135">Minimum supported server</span></span><br/> | <span data-ttu-id="df381-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="df381-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="df381-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="df381-137">Namespace</span></span><br/>                | <span data-ttu-id="df381-138">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="df381-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="df381-139">MOF</span><span class="sxs-lookup"><span data-stu-id="df381-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="df381-140"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="df381-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="df381-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="df381-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="df381-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="df381-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="df381-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="df381-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df381-144">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="df381-144">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




