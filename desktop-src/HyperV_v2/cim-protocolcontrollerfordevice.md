---
description: Representa una asociación entre un dispositivo lógico y un controlador de protocolo que está conectado al dispositivo.
ms.assetid: 1a1efc60-6108-4376-9f73-d2dd41443645
title: CIM_ProtocolControllerForDevice (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolControllerForDevice
- CIM_ProtocolControllerForDevice.Antecedent
- CIM_ProtocolControllerForDevice.Dependent
- CIM_ProtocolControllerForDevice.DeviceNumber
- CIM_ProtocolControllerForDevice.AccessPriority
- CIM_ProtocolControllerForDevice.AccessState
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7d3ef7799cccc6e8fe8e219cddfba37cf12b8637
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911353"
---
# <a name="cim_protocolcontrollerfordevice-class"></a><span data-ttu-id="6baeb-103">\_Clase ProtocolControllerForDevice de CIM</span><span class="sxs-lookup"><span data-stu-id="6baeb-103">CIM\_ProtocolControllerForDevice class</span></span>

<span data-ttu-id="6baeb-104">Representa una asociación entre un dispositivo lógico y un controlador de protocolo que está conectado al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6baeb-104">Represents an association between a logical device and a protocol controller that is connected to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="6baeb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6baeb-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.1000"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_ProtocolControllerForDevice : CIM_Dependency
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  string                     DeviceNumber;
  uint16                     AccessPriority;
  uint16                     AccessState;
};
```

## <a name="members"></a><span data-ttu-id="6baeb-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="6baeb-106">Members</span></span>

<span data-ttu-id="6baeb-107">La clase **CIM \_ ProtocolControllerForDevice** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6baeb-107">The **CIM\_ProtocolControllerForDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="6baeb-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6baeb-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6baeb-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6baeb-109">Properties</span></span>

<span data-ttu-id="6baeb-110">La clase **CIM \_ ProtocolControllerForDevice** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6baeb-110">The **CIM\_ProtocolControllerForDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6baeb-111">**AccessPriority**</span><span class="sxs-lookup"><span data-stu-id="6baeb-111">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6baeb-112">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6baeb-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6baeb-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6baeb-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6baeb-114">La prioridad de acceso dada al dispositivo a través del controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="6baeb-114">The access priority given to the device through the protocol controller.</span></span> <span data-ttu-id="6baeb-115">La prioridad más alta tiene el valor más bajo.</span><span class="sxs-lookup"><span data-stu-id="6baeb-115">The highest priority has the lowest value.</span></span>

</dd> <dt>

<span data-ttu-id="6baeb-116">**AccessState**</span><span class="sxs-lookup"><span data-stu-id="6baeb-116">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6baeb-117">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6baeb-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6baeb-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6baeb-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6baeb-119">Accesibilidad del dispositivo lógico a través del controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="6baeb-119">The accessibility of the logical device through the protocol controller</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6baeb-120">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="6baeb-120">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

<span data-ttu-id="6baeb-121">**Activo** (2)</span><span class="sxs-lookup"><span data-stu-id="6baeb-121">**Active** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

<span data-ttu-id="6baeb-122">**Inactivo** (3)</span><span class="sxs-lookup"><span data-stu-id="6baeb-122">**Inactive** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Replication_In_Progress"></span><span id="replication_in_progress"></span><span id="REPLICATION_IN_PROGRESS"></span>

<span data-ttu-id="6baeb-123">**Replicación en curso** (4)</span><span class="sxs-lookup"><span data-stu-id="6baeb-123">**Replication In Progress** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Mapping_Inconsistency"></span><span id="mapping_inconsistency"></span><span id="MAPPING_INCONSISTENCY"></span>

<span data-ttu-id="6baeb-124">**Incoherencia de asignación** (5)</span><span class="sxs-lookup"><span data-stu-id="6baeb-124">**Mapping Inconsistency** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6baeb-125">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="6baeb-125">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6baeb-126">Tipo de datos: **CIM \_ ProtocolController**</span><span class="sxs-lookup"><span data-stu-id="6baeb-126">Data type: **CIM\_ProtocolController**</span></span>
</dt> <dt>

<span data-ttu-id="6baeb-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6baeb-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6baeb-128">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="6baeb-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="6baeb-129">Controlador de protocolo de la asociación.</span><span class="sxs-lookup"><span data-stu-id="6baeb-129">The protocol controller in the association.</span></span>

</dd> <dt>

<span data-ttu-id="6baeb-130">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="6baeb-130">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6baeb-131">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="6baeb-131">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="6baeb-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6baeb-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6baeb-133">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="6baeb-133">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="6baeb-134">El dispositivo lógico de la asociación.</span><span class="sxs-lookup"><span data-stu-id="6baeb-134">The logical device in the association.</span></span>

</dd> <dt>

<span data-ttu-id="6baeb-135">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="6baeb-135">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6baeb-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6baeb-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6baeb-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6baeb-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6baeb-138">La dirección del dispositivo asociado en el contexto del controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="6baeb-138">The address of the associated device in the context of the protocol controler.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6baeb-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6baeb-139">Requirements</span></span>



| <span data-ttu-id="6baeb-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="6baeb-140">Requirement</span></span> | <span data-ttu-id="6baeb-141">Value</span><span class="sxs-lookup"><span data-stu-id="6baeb-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6baeb-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6baeb-142">Minimum supported client</span></span><br/> | <span data-ttu-id="6baeb-143">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6baeb-143">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="6baeb-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6baeb-144">Minimum supported server</span></span><br/> | <span data-ttu-id="6baeb-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6baeb-145">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="6baeb-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6baeb-146">Namespace</span></span><br/>                | <span data-ttu-id="6baeb-147">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="6baeb-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6baeb-148">MOF</span><span class="sxs-lookup"><span data-stu-id="6baeb-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6baeb-149"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6baeb-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6baeb-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6baeb-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6baeb-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6baeb-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6baeb-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="6baeb-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6baeb-153">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="6baeb-153">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

