---
description: Una representación lógica de un puerto de red en un dispositivo de red.
ms.assetid: afcfc93d-174e-43b5-a16f-28937b4bf81a
title: CIM_NetworkPort (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkPort
- CIM_NetworkPort.Speed
- CIM_NetworkPort.OtherNetworkPortType
- CIM_NetworkPort.PortNumber
- CIM_NetworkPort.LinkTechnology
- CIM_NetworkPort.OtherLinkTechnology
- CIM_NetworkPort.PermanentAddress
- CIM_NetworkPort.NetworkAddresses
- CIM_NetworkPort.FullDuplex
- CIM_NetworkPort.AutoSense
- CIM_NetworkPort.SupportedMaximumTransmissionUnit
- CIM_NetworkPort.ActiveMaximumTransmissionUnit
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9e3ac64b55e17d0526527ebbaca168c3f7b289f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278621"
---
# <a name="cim_networkport-class"></a><span data-ttu-id="2cb21-103">\_Clase NetworkPort de CIM</span><span class="sxs-lookup"><span data-stu-id="2cb21-103">CIM\_NetworkPort class</span></span>

<span data-ttu-id="2cb21-104">Una representación lógica de un puerto de red en un dispositivo de red.</span><span class="sxs-lookup"><span data-stu-id="2cb21-104">A logical representation of a network port on a network device.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cb21-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2cb21-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_NetworkPort : CIM_LogicalPort
{
  uint64  Speed;
  string  OtherNetworkPortType;
  uint16  PortNumber;
  uint16  LinkTechnology;
  string  OtherLinkTechnology;
  string  PermanentAddress;
  string  NetworkAddresses[];
  boolean FullDuplex;
  boolean AutoSense;
  uint64  SupportedMaximumTransmissionUnit;
  uint64  ActiveMaximumTransmissionUnit;
};
```

## <a name="members"></a><span data-ttu-id="2cb21-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="2cb21-106">Members</span></span>

<span data-ttu-id="2cb21-107">La clase **CIM \_ NetworkPort** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2cb21-107">The **CIM\_NetworkPort** class has these types of members:</span></span>

-   [<span data-ttu-id="2cb21-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2cb21-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2cb21-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2cb21-109">Properties</span></span>

<span data-ttu-id="2cb21-110">La clase **CIM \_ NetworkPort** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2cb21-110">The **CIM\_NetworkPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2cb21-111">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="2cb21-111">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cb21-112">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2cb21-112">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2cb21-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2cb21-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cb21-114">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **punitivo** ("byte")</span><span class="sxs-lookup"><span data-stu-id="2cb21-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="2cb21-115">La unidad de transmisión máxima (MTU) activa o negociada que es compatible con el puerto.</span><span class="sxs-lookup"><span data-stu-id="2cb21-115">The active or negotiated maximum transmission unit (MTU) that is supported by the port.</span></span>

</dd> <dt>

<span data-ttu-id="2cb21-116">**Percepción automática**</span><span class="sxs-lookup"><span data-stu-id="2cb21-116">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cb21-117">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2cb21-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2cb21-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2cb21-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cb21-119">**true** si el puerto puede determinar automáticamente la velocidad y otras características de comunicación del medio de red conectado; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="2cb21-119">**true** if the port can automatically determine the speed or other communications characteristic of the attached network media; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="2cb21-120">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="2cb21-120">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cb21-121">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2cb21-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2cb21-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2cb21-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cb21-123">**true** si el puerto está funcionando en modo dúplex completo; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="2cb21-123">**true** if the port is operating in full duplex mode; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="2cb21-124">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="2cb21-124">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cb21-125">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2cb21-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2cb21-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2cb21-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cb21-127">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ NetworkPort**.**OtherLinkTechnology**")</span><span class="sxs-lookup"><span data-stu-id="2cb21-127">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_NetworkPort**.**OtherLinkTechnology**")</span></span>
</dt> </dl>

<span data-ttu-id="2cb21-128">Tecnología de vínculo utilizada por el puerto.</span><span class="sxs-lookup"><span data-stu-id="2cb21-128">The link technology used by the port.</span></span> <span data-ttu-id="2cb21-129">Cuando se establece en "1" (otro), la propiedad **OtherLinkTechnology** contiene una descripción del tipo de vínculo.</span><span class="sxs-lookup"><span data-stu-id="2cb21-129">When set to "1" (other), the **OtherLinkTechnology** property contains a description of the link type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2cb21-130">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="2cb21-130">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2cb21-131">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2cb21-131">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="2cb21-132">**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="2cb21-132">**Ethernet** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IB"></span><span id="ib"></span>

<span data-ttu-id="2cb21-133">**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="2cb21-133">**IB** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="FC"></span><span id="fc"></span>

<span data-ttu-id="2cb21-134">**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="2cb21-134">**FC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="2cb21-135">**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="2cb21-135">**FDDI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="2cb21-136">**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="2cb21-136">**ATM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

<span data-ttu-id="2cb21-137">**Token ring** (7)</span><span class="sxs-lookup"><span data-stu-id="2cb21-137">**Token Ring** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>

<span data-ttu-id="2cb21-138">**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="2cb21-138">**Frame Relay** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="2cb21-139">**Infrarrojos** (9)</span><span class="sxs-lookup"><span data-stu-id="2cb21-139">**Infrared** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>

<span data-ttu-id="2cb21-140">**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="2cb21-140">**BlueTooth** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>

<span data-ttu-id="2cb21-141">**LAN inalámbrica** (11)</span><span class="sxs-lookup"><span data-stu-id="2cb21-141">**Wireless LAN** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2cb21-142">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="2cb21-142">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cb21-143">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="2cb21-143">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2cb21-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2cb21-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cb21-145">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Adaptador de red DMTF 802 puerto \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="2cb21-145">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Network Adapter 802 Port\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="2cb21-146">Una matriz que contiene las direcciones de red para el puerto.</span><span class="sxs-lookup"><span data-stu-id="2cb21-146">An array that contains the network addresses for the port.</span></span>

</dd> <dt>

<span data-ttu-id="2cb21-147">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="2cb21-147">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cb21-148">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2cb21-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cb21-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2cb21-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cb21-150">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ NetworkPort**.**LinkTechnology**")</span><span class="sxs-lookup"><span data-stu-id="2cb21-150">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_NetworkPort**.**LinkTechnology**")</span></span>
</dt> </dl>

<span data-ttu-id="2cb21-151">La tecnología de vínculo cuando **LinkTechnology** se establece en "1", (otro).</span><span class="sxs-lookup"><span data-stu-id="2cb21-151">The link technology when **LinkTechnology** is set to "1", (other).</span></span>

</dd> <dt>

<span data-ttu-id="2cb21-152">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="2cb21-152">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cb21-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2cb21-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cb21-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2cb21-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cb21-155">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM \_ NetworkPort**.**OtherPortType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalPort**](cim-logicalport.md).**PortType**")</span><span class="sxs-lookup"><span data-stu-id="2cb21-155">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_NetworkPort**.**OtherPortType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalPort**](cim-logicalport.md).**PortType**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="2cb21-156">Descripción desusada: el tipo de módulo del puerto, cuando la propiedad **portType** contiene 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="2cb21-156">Deprecated description: The module type of the port, when the **PortType** property contains 1 (other).</span></span>

 

<span data-ttu-id="2cb21-157">Esta propiedad está desusada.</span><span class="sxs-lookup"><span data-stu-id="2cb21-157">This property is deprecated.</span></span> <span data-ttu-id="2cb21-158">En su lugar, se recomienda la propiedad **portType** en la clase [**\_ LogicalPort de CIM**](cim-logicalport.md) .</span><span class="sxs-lookup"><span data-stu-id="2cb21-158">Instead, we recommend the **PortType** property in the [**CIM\_LogicalPort**](cim-logicalport.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="2cb21-159">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="2cb21-159">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cb21-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2cb21-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2cb21-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2cb21-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cb21-162">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Adaptador de red DMTF 802 puerto \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="2cb21-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Network Adapter 802 Port\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="2cb21-163">La dirección de red que está codificada en un puerto.</span><span class="sxs-lookup"><span data-stu-id="2cb21-163">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="2cb21-164">Se puede cambiar la dirección codificada mediante una actualización de firmware o una configuración de software.</span><span class="sxs-lookup"><span data-stu-id="2cb21-164">The hardcoded address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="2cb21-165">Cuando se realiza este cambio, esta propiedad debe actualizarse al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="2cb21-165">When this change is made, this property should be updated at the same time.</span></span> <span data-ttu-id="2cb21-166">**PermanentAddress** debe dejarse en blanco si la dirección no existe.</span><span class="sxs-lookup"><span data-stu-id="2cb21-166">**PermanentAddress** should be left blank if the address doesn't exist.</span></span>

</dd> <dt>

<span data-ttu-id="2cb21-167">**NúmeroDePuerto**</span><span class="sxs-lookup"><span data-stu-id="2cb21-167">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cb21-168">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2cb21-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2cb21-169">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2cb21-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2cb21-170">El número de puerto del puerto de red.</span><span class="sxs-lookup"><span data-stu-id="2cb21-170">The port number of the network port.</span></span> <span data-ttu-id="2cb21-171">Los puertos de red suelen numerarse con respecto a un módulo lógico o a un elemento de red.</span><span class="sxs-lookup"><span data-stu-id="2cb21-171">Network ports are often numbered relative to either a logical module or a network element.</span></span>

</dd> <dt>

<span data-ttu-id="2cb21-172">**Velocidad**</span><span class="sxs-lookup"><span data-stu-id="2cb21-172">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cb21-173">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2cb21-173">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2cb21-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2cb21-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cb21-175">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("velocidad"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| MIB-II. ifSpeed "," MIF. \|Adaptador de red DMTF 802 puerto \| 001,5 "), **punitivo** (" bit por segundo ")</span><span class="sxs-lookup"><span data-stu-id="2cb21-175">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Speed"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|MIB-II.ifSpeed", "MIF.DMTF\|Network Adapter 802 Port\|001.5"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="2cb21-176">El ancho de banda actual del puerto en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="2cb21-176">The current bandwidth of the port in bits per second.</span></span> <span data-ttu-id="2cb21-177">En el caso de los puertos que varían en ancho de banda o para aquellos en los que no se puede realizar una estimación precisa, esta propiedad debe contener el ancho de banda nominal.</span><span class="sxs-lookup"><span data-stu-id="2cb21-177">For ports that vary in bandwidth, or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="2cb21-178">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="2cb21-178">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2cb21-179">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2cb21-179">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2cb21-180">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2cb21-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2cb21-181">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **punitivo** ("byte")</span><span class="sxs-lookup"><span data-stu-id="2cb21-181">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="2cb21-182">La unidad de transmisión máxima (MTU) que es compatible con el puerto.</span><span class="sxs-lookup"><span data-stu-id="2cb21-182">The maximum transmission unit (MTU) that is supported by the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2cb21-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2cb21-183">Requirements</span></span>



| <span data-ttu-id="2cb21-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cb21-184">Requirement</span></span> | <span data-ttu-id="2cb21-185">Value</span><span class="sxs-lookup"><span data-stu-id="2cb21-185">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cb21-186">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cb21-186">Minimum supported client</span></span><br/> | <span data-ttu-id="2cb21-187">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2cb21-187">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="2cb21-188">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2cb21-188">Minimum supported server</span></span><br/> | <span data-ttu-id="2cb21-189">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2cb21-189">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="2cb21-190">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2cb21-190">Namespace</span></span><br/>                | <span data-ttu-id="2cb21-191">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="2cb21-191">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2cb21-192">MOF</span><span class="sxs-lookup"><span data-stu-id="2cb21-192">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2cb21-193"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2cb21-193"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2cb21-194">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2cb21-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cb21-195"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2cb21-195"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2cb21-196">Vea también</span><span class="sxs-lookup"><span data-stu-id="2cb21-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cb21-197">**\_LOGICALPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="2cb21-197">**CIM\_LogicalPort**</span></span>](cim-logicalport.md)
</dt> </dl>

 

