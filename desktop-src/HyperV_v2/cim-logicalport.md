---
description: Abstracción de un puerto o punto de conexión de un dispositivo.
ms.assetid: ee725c64-587b-4e5f-9b1c-7a58902b0631
title: CIM_LogicalPort (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalPort
- CIM_LogicalPort.Speed
- CIM_LogicalPort.MaxSpeed
- CIM_LogicalPort.RequestedSpeed
- CIM_LogicalPort.UsageRestriction
- CIM_LogicalPort.PortType
- CIM_LogicalPort.OtherPortType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: eeed69e9669048377340cb0ca21e7a2e89f4baff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000899"
---
# <a name="cim_logicalport-class"></a><span data-ttu-id="0a3d8-103">\_Clase LogicalPort de CIM</span><span class="sxs-lookup"><span data-stu-id="0a3d8-103">CIM\_LogicalPort class</span></span>

<span data-ttu-id="0a3d8-104">Abstracción de un puerto o punto de conexión de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0a3d8-104">The abstraction of a port or connection point of a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a3d8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a3d8-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_LogicalPort : CIM_LogicalDevice
{
  uint64 Speed;
  uint64 MaxSpeed;
  uint64 RequestedSpeed;
  uint16 UsageRestriction;
  uint16 PortType;
  string OtherPortType;
};
```

## <a name="members"></a><span data-ttu-id="0a3d8-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="0a3d8-106">Members</span></span>

<span data-ttu-id="0a3d8-107">La clase **CIM \_ LogicalPort** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0a3d8-107">The **CIM\_LogicalPort** class has these types of members:</span></span>

-   [<span data-ttu-id="0a3d8-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0a3d8-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0a3d8-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0a3d8-109">Properties</span></span>

<span data-ttu-id="0a3d8-110">La clase **CIM \_ LogicalPort** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0a3d8-110">The **CIM\_LogicalPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0a3d8-111">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="0a3d8-111">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a3d8-112">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0a3d8-112">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0a3d8-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0a3d8-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a3d8-114">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo"), **punitivo** ("bit por segundo")</span><span class="sxs-lookup"><span data-stu-id="0a3d8-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="0a3d8-115">Ancho de banda máximo del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="0a3d8-115">The maximum bandwidth of the port, in bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="0a3d8-116">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="0a3d8-116">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a3d8-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0a3d8-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a3d8-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0a3d8-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a3d8-119">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ LogicalPort**.**PortType**")</span><span class="sxs-lookup"><span data-stu-id="0a3d8-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalPort**.**PortType**")</span></span>
</dt> </dl>

<span data-ttu-id="0a3d8-120">Describe el tipo de módulo, cuando **portType** se establece en **other** ("1").</span><span class="sxs-lookup"><span data-stu-id="0a3d8-120">Describes the type of module, when **PortType** is set to **Other** ("1").</span></span>

</dd> <dt>

<span data-ttu-id="0a3d8-121">**PortType**</span><span class="sxs-lookup"><span data-stu-id="0a3d8-121">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a3d8-122">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0a3d8-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0a3d8-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0a3d8-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a3d8-124">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ NetworkPort**](cim-networkport.md).**OtherNetworkPortType**")</span><span class="sxs-lookup"><span data-stu-id="0a3d8-124">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_NetworkPort**](cim-networkport.md).**OtherNetworkPortType**")</span></span>
</dt> </dl>

<span data-ttu-id="0a3d8-125">El tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="0a3d8-125">The port type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0a3d8-126">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="0a3d8-126">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="0a3d8-127">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="0a3d8-127">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0a3d8-128">**No aplicable** (2)</span><span class="sxs-lookup"><span data-stu-id="0a3d8-128">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0a3d8-129">**DMTF reservado** (3.. 15999)</span><span class="sxs-lookup"><span data-stu-id="0a3d8-129">**DMTF Reserved** (3..15999)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0a3d8-130">**Proveedor reservado** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0a3d8-130">**Vendor Reserved** (16000..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0a3d8-131">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="0a3d8-131">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a3d8-132">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0a3d8-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0a3d8-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0a3d8-133">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="0a3d8-134">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ LogicalPort CIM**.**Speed**"), **punitivo** (" bit/segundo ")</span><span class="sxs-lookup"><span data-stu-id="0a3d8-134">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_LogicalPort**.**Speed**"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="0a3d8-135">Ancho de banda solicitado del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="0a3d8-135">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="0a3d8-136">El ancho de banda real se registra en la propiedad **Speed** .</span><span class="sxs-lookup"><span data-stu-id="0a3d8-136">The actual bandwidth is reported in the **Speed** property.</span></span>

</dd> <dt>

<span data-ttu-id="0a3d8-137">**Velocidad**</span><span class="sxs-lookup"><span data-stu-id="0a3d8-137">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a3d8-138">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0a3d8-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0a3d8-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0a3d8-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a3d8-140">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo"), **punitivo** ("bit por segundo")</span><span class="sxs-lookup"><span data-stu-id="0a3d8-140">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="0a3d8-141">Ancho de banda del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="0a3d8-141">The bandwidth of the port, in bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="0a3d8-142">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="0a3d8-142">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a3d8-143">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0a3d8-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0a3d8-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0a3d8-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0a3d8-145">Indica si el puerto está restringido a ser un puerto front-end o back-end.</span><span class="sxs-lookup"><span data-stu-id="0a3d8-145">Indicates whether the port is restricted to being a front-end or back-end port.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0a3d8-146">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="0a3d8-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>

<span data-ttu-id="0a3d8-147">**Solo front-end** (2)</span><span class="sxs-lookup"><span data-stu-id="0a3d8-147">**Front-end only** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>

<span data-ttu-id="0a3d8-148">**Solo back-end** (3)</span><span class="sxs-lookup"><span data-stu-id="0a3d8-148">**Back-end only** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_restricted"></span><span id="not_restricted"></span><span id="NOT_RESTRICTED"></span>

<span data-ttu-id="0a3d8-149">**No restringido** (4)</span><span class="sxs-lookup"><span data-stu-id="0a3d8-149">**Not restricted** (4)</span></span>


<span data-ttu-id="0a3d8-150"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0a3d8-150"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0a3d8-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a3d8-151">Requirements</span></span>



| <span data-ttu-id="0a3d8-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a3d8-152">Requirement</span></span> | <span data-ttu-id="0a3d8-153">Value</span><span class="sxs-lookup"><span data-stu-id="0a3d8-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a3d8-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a3d8-154">Minimum supported client</span></span><br/> | <span data-ttu-id="0a3d8-155">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0a3d8-155">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="0a3d8-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0a3d8-156">Minimum supported server</span></span><br/> | <span data-ttu-id="0a3d8-157">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0a3d8-157">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="0a3d8-158">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0a3d8-158">Namespace</span></span><br/>                | <span data-ttu-id="0a3d8-159">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="0a3d8-159">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0a3d8-160">MOF</span><span class="sxs-lookup"><span data-stu-id="0a3d8-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a3d8-161"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0a3d8-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a3d8-162">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0a3d8-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a3d8-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0a3d8-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0a3d8-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a3d8-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a3d8-165">**LogicalDevice de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="0a3d8-165">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

