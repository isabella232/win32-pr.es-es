---
description: Representa una asociación entre un controlador de protocolo y una unidad lógica expuesta.
ms.assetid: e8bf2b32-b4a6-4963-8a50-2b06776965e8
title: CIM_ProtocolControllerForUnit (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolControllerForUnit
- CIM_ProtocolControllerForUnit.Antecedent
- CIM_ProtocolControllerForUnit.Dependent
- CIM_ProtocolControllerForUnit.DeviceAccess
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 26020745057d5963ed4a892ba8639ac078aaa20b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667952"
---
# <a name="cim_protocolcontrollerforunit-class"></a><span data-ttu-id="af8a2-103">\_Clase ProtocolControllerForUnit de CIM</span><span class="sxs-lookup"><span data-stu-id="af8a2-103">CIM\_ProtocolControllerForUnit class</span></span>

<span data-ttu-id="af8a2-104">Representa una asociación entre un controlador de protocolo y una unidad lógica expuesta.</span><span class="sxs-lookup"><span data-stu-id="af8a2-104">Represents an association between a protocol controller and an exposed logical unit.</span></span>

## <a name="syntax"></a><span data-ttu-id="af8a2-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="af8a2-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_ProtocolControllerForUnit : CIM_ProtocolControllerForDevice
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  uint16                     DeviceAccess;
};
```

## <a name="members"></a><span data-ttu-id="af8a2-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="af8a2-106">Members</span></span>

<span data-ttu-id="af8a2-107">La clase **CIM \_ ProtocolControllerForUnit** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="af8a2-107">The **CIM\_ProtocolControllerForUnit** class has these types of members:</span></span>

-   [<span data-ttu-id="af8a2-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="af8a2-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="af8a2-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="af8a2-109">Properties</span></span>

<span data-ttu-id="af8a2-110">La clase **CIM \_ ProtocolControllerForUnit** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="af8a2-110">The **CIM\_ProtocolControllerForUnit** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="af8a2-111">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="af8a2-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af8a2-112">Tipo de datos: **CIM \_ ProtocolController**</span><span class="sxs-lookup"><span data-stu-id="af8a2-112">Data type: **CIM\_ProtocolController**</span></span>
</dt> <dt>

<span data-ttu-id="af8a2-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="af8a2-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af8a2-114">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="af8a2-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="af8a2-115">El controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="af8a2-115">The protocol controller.</span></span>

</dd> <dt>

<span data-ttu-id="af8a2-116">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="af8a2-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af8a2-117">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="af8a2-117">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="af8a2-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="af8a2-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af8a2-119">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="af8a2-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="af8a2-120">Unidad lógica asociada con el controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="af8a2-120">The logical unit associated with the protocol controller.</span></span>

</dd> <dt>

<span data-ttu-id="af8a2-121">**DeviceAccess**</span><span class="sxs-lookup"><span data-stu-id="af8a2-121">**DeviceAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af8a2-122">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="af8a2-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="af8a2-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="af8a2-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af8a2-124">Los derechos de acceso concedidos a la unidad lógica a través del controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="af8a2-124">The access rights granted to the logical unit through the protocol controller.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="af8a2-125">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="af8a2-125">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Read_Write"></span><span id="read_write"></span><span id="READ_WRITE"></span>

<span data-ttu-id="af8a2-126">**Lectura y escritura** (2)</span><span class="sxs-lookup"><span data-stu-id="af8a2-126">**Read Write** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Read-Only"></span><span id="read-only"></span><span id="READ-ONLY"></span>

<span data-ttu-id="af8a2-127">**Solo lectura** (3)</span><span class="sxs-lookup"><span data-stu-id="af8a2-127">**Read-Only** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Access"></span><span id="no_access"></span><span id="NO_ACCESS"></span>

<span data-ttu-id="af8a2-128">**Sin acceso** (4)</span><span class="sxs-lookup"><span data-stu-id="af8a2-128">**No Access** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="af8a2-129">**DMTF reservado** (5.. 15999)</span><span class="sxs-lookup"><span data-stu-id="af8a2-129">**DMTF Reserved** (5..15999)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="af8a2-130">**Proveedor reservado** (16000...)</span><span class="sxs-lookup"><span data-stu-id="af8a2-130">**Vendor Reserved** (16000..)</span></span>


<span data-ttu-id="af8a2-131"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="af8a2-131"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="af8a2-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af8a2-132">Requirements</span></span>



| <span data-ttu-id="af8a2-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="af8a2-133">Requirement</span></span> | <span data-ttu-id="af8a2-134">Value</span><span class="sxs-lookup"><span data-stu-id="af8a2-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af8a2-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af8a2-135">Minimum supported client</span></span><br/> | <span data-ttu-id="af8a2-136">Windows 8</span><span class="sxs-lookup"><span data-stu-id="af8a2-136">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="af8a2-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af8a2-137">Minimum supported server</span></span><br/> | <span data-ttu-id="af8a2-138">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="af8a2-138">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="af8a2-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="af8a2-139">Namespace</span></span><br/>                | <span data-ttu-id="af8a2-140">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="af8a2-140">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="af8a2-141">MOF</span><span class="sxs-lookup"><span data-stu-id="af8a2-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af8a2-142"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="af8a2-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="af8a2-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="af8a2-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af8a2-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="af8a2-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="af8a2-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="af8a2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af8a2-146">**\_PROTOCOLCONTROLLERFORDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="af8a2-146">**CIM\_ProtocolControllerForDevice**</span></span>](cim-protocolcontrollerfordevice.md)
</dt> </dl>

 

