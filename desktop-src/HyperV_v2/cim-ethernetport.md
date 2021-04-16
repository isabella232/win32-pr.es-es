---
description: Representa un puerto Ethernet.
ms.assetid: c9a148c2-cf02-466f-b8ca-b1bf616d75dc
title: CIM_EthernetPort (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EthernetPort
- CIM_EthernetPort.PortType
- CIM_EthernetPort.NetworkAddresses
- CIM_EthernetPort.MaxDataSize
- CIM_EthernetPort.Capabilities
- CIM_EthernetPort.CapabilityDescriptions
- CIM_EthernetPort.EnabledCapabilities
- CIM_EthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a44e93f84178fa2714d3c823735b3d90922e04be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539923"
---
# <a name="cim_ethernetport-class"></a><span data-ttu-id="02ab0-103">\_Clase EthernetPort de CIM</span><span class="sxs-lookup"><span data-stu-id="02ab0-103">CIM\_EthernetPort class</span></span>

<span data-ttu-id="02ab0-104">Representa un puerto Ethernet.</span><span class="sxs-lookup"><span data-stu-id="02ab0-104">Represents an ethernet port.</span></span>

## <a name="syntax"></a><span data-ttu-id="02ab0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="02ab0-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_EthernetPort : CIM_NetworkPort
{
  uint16 PortType;
  string NetworkAddresses[];
  uint32 MaxDataSize;
  uint16 Capabilities[];
  string CapabilityDescriptions[];
  uint16 EnabledCapabilities[];
  string OtherEnabledCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="02ab0-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="02ab0-106">Members</span></span>

<span data-ttu-id="02ab0-107">La clase **CIM \_ EthernetPort** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="02ab0-107">The **CIM\_EthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="02ab0-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="02ab0-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="02ab0-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="02ab0-109">Properties</span></span>

<span data-ttu-id="02ab0-110">La clase **CIM \_ EthernetPort** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="02ab0-110">The **CIM\_EthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="02ab0-111">**Capabilities**</span><span class="sxs-lookup"><span data-stu-id="02ab0-111">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02ab0-112">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="02ab0-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="02ab0-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="02ab0-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02ab0-114">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EthernetPort**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="02ab0-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPort**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="02ab0-115">Las capacidades del puerto Ethernet.</span><span class="sxs-lookup"><span data-stu-id="02ab0-115">The capabilities of the ethernet port.</span></span>

> [!Note]  
> <span data-ttu-id="02ab0-116">Si se habilitan las capacidades de conmutación por error o equilibrio de carga, también se debe definir un objeto [**CIM \_ SpareGroup**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (conmutación por error) o [**CIM \_ ExtraCapacityGroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (equilibrio de carga) para describir completamente la funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="02ab0-116">If failover or load balancing capabilities are enabled, a [**CIM\_SpareGroup**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (failover) or [**CIM\_ExtraCapacityGroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (load balancing) object should also be defined to completely describe the capability.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="02ab0-117">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="02ab0-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="02ab0-118">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="02ab0-118">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>

<span data-ttu-id="02ab0-119">**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="02ab0-119">**AlertOnLan** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>

<span data-ttu-id="02ab0-120">**WakeOnLan** (3)</span><span class="sxs-lookup"><span data-stu-id="02ab0-120">**WakeOnLan** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>

<span data-ttu-id="02ab0-121">**Conmutación por error** (4)</span><span class="sxs-lookup"><span data-stu-id="02ab0-121">**FailOver** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>

<span data-ttu-id="02ab0-122">**Equilibrio** (5)</span><span class="sxs-lookup"><span data-stu-id="02ab0-122">**LoadBalancing** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="02ab0-123">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="02ab0-123">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02ab0-124">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="02ab0-124">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="02ab0-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="02ab0-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02ab0-126">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EthernetPort**.**Funcionalidades**")</span><span class="sxs-lookup"><span data-stu-id="02ab0-126">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPort**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="02ab0-127">Una matriz de cadenas de forma libre que proporciona explicaciones más detalladas para cualquiera de las características que se indican en la matriz de capacidades.</span><span class="sxs-lookup"><span data-stu-id="02ab0-127">An array of free-form strings that provides more detailed explanations for any of the features that are indicated in the Capabilities array.</span></span> <span data-ttu-id="02ab0-128">Los elementos de esta matriz se corresponden con los elementos de la matriz de funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="02ab0-128">The items in this array correspond to the items in the Capabilities array.</span></span>

</dd> <dt>

<span data-ttu-id="02ab0-129">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="02ab0-129">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02ab0-130">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="02ab0-130">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="02ab0-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="02ab0-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02ab0-132">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EthernetPort**.**Capabilities**","**CIM \_ EthernetPort**.**OtherEnabledCapabilities**")</span><span class="sxs-lookup"><span data-stu-id="02ab0-132">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPort**.**Capabilities**", "**CIM\_EthernetPort**.**OtherEnabledCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="02ab0-133">Indica qué capacidades están habilitadas en la matriz de funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="02ab0-133">Indicates which capabilities are enabled in the Capabilities array.</span></span> <span data-ttu-id="02ab0-134">Los elementos de esta matriz se corresponden con los elementos de la matriz de funcionalidades.</span><span class="sxs-lookup"><span data-stu-id="02ab0-134">The items in this array correspond to the items in the Capabilities array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="02ab0-135">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="02ab0-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="02ab0-136">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="02ab0-136">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>

<span data-ttu-id="02ab0-137">**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="02ab0-137">**AlertOnLan** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>

<span data-ttu-id="02ab0-138">**WakeOnLan** (3)</span><span class="sxs-lookup"><span data-stu-id="02ab0-138">**WakeOnLan** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>

<span data-ttu-id="02ab0-139">**Conmutación por error** (4)</span><span class="sxs-lookup"><span data-stu-id="02ab0-139">**FailOver** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>

<span data-ttu-id="02ab0-140">**Equilibrio** (5)</span><span class="sxs-lookup"><span data-stu-id="02ab0-140">**LoadBalancing** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="02ab0-141">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="02ab0-141">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02ab0-142">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="02ab0-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="02ab0-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="02ab0-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02ab0-144">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Puente IETF-MIB. dot1dTpPortMaxInfo ")</span><span class="sxs-lookup"><span data-stu-id="02ab0-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpPortMaxInfo")</span></span>
</dt> </dl>

<span data-ttu-id="02ab0-145">El tamaño máximo del campo de información (no MAC) que se recibirá o transmitirá.</span><span class="sxs-lookup"><span data-stu-id="02ab0-145">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span>

</dd> <dt>

<span data-ttu-id="02ab0-146">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="02ab0-146">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02ab0-147">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="02ab0-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="02ab0-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="02ab0-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02ab0-149">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NetworkAddresses")</span><span class="sxs-lookup"><span data-stu-id="02ab0-149">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NetworkAddresses")</span></span>
</dt> </dl>

<span data-ttu-id="02ab0-150">Las direcciones de red asignadas al puerto.</span><span class="sxs-lookup"><span data-stu-id="02ab0-150">The network addresses assigned to the port.</span></span> <span data-ttu-id="02ab0-151">La dirección es un equipo MAC 802,3 con formato de doce dígitos hexadecimales (por ejemplo, "010203040506"), donde cada par de dígitos representa uno de los seis octetos de la dirección MAC en orden de bits canónico.</span><span class="sxs-lookup"><span data-stu-id="02ab0-151">The address is a 802.3 MAC that is formatted as twelve hexadecimal digits (for example, "010203040506"), where each pair of digits represents one of the six octets of the MAC address in canonical bit order.</span></span>

</dd> <dt>

<span data-ttu-id="02ab0-152">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="02ab0-152">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02ab0-153">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="02ab0-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="02ab0-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="02ab0-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02ab0-155">Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EthernetPort**.**EnabledCapabilities**")</span><span class="sxs-lookup"><span data-stu-id="02ab0-155">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPort**.**EnabledCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="02ab0-156">Matriz de cadenas de forma libre que proporcionan explicaciones más detalladas para cualquiera de los elementos de la matriz de **EnabledCapabilities** que se establecen en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="02ab0-156">An array of free-form strings that provide more detailed explanations for any of the **EnabledCapabilities** array items that are set to 1 (Other).</span></span> <span data-ttu-id="02ab0-157">Los elementos de esta matriz se corresponden con los elementos de la matriz **EnabledCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="02ab0-157">The items in this array correspond to the items in the **EnabledCapabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="02ab0-158">**PortType**</span><span class="sxs-lookup"><span data-stu-id="02ab0-158">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02ab0-159">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="02ab0-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="02ab0-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="02ab0-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02ab0-161">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("portType")</span><span class="sxs-lookup"><span data-stu-id="02ab0-161">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span></span>
</dt> </dl>

<span data-ttu-id="02ab0-162">Modo que está habilitado en el puerto.</span><span class="sxs-lookup"><span data-stu-id="02ab0-162">The mode that is enabled on the port.</span></span> <span data-ttu-id="02ab0-163">Cuando se establece en 1 (otro), la propiedad **OtherPortType** describe el modo.</span><span class="sxs-lookup"><span data-stu-id="02ab0-163">When set to 1 (Other), the **OtherPortType** property describes the mode.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="02ab0-164">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="02ab0-164">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="02ab0-165">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="02ab0-165">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="10BaseT"></span><span id="10baset"></span><span id="10BASET"></span>

<span data-ttu-id="02ab0-166">**10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="02ab0-166">**10BaseT** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>

<span data-ttu-id="02ab0-167">**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="02ab0-167">**10-100BaseT** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>

<span data-ttu-id="02ab0-168">**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="02ab0-168">**100BaseT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>

<span data-ttu-id="02ab0-169">**1000BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="02ab0-169">**1000BaseT** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>

<span data-ttu-id="02ab0-170">**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="02ab0-170">**2500BaseT** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>

<span data-ttu-id="02ab0-171">**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="02ab0-171">**10GBaseT** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>

<span data-ttu-id="02ab0-172">**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="02ab0-172">**10GBase-CX4** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="100Base-FX"></span><span id="100base-fx"></span><span id="100BASE-FX"></span>

<span data-ttu-id="02ab0-173">**100Base-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="02ab0-173">**100Base-FX** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>

<span data-ttu-id="02ab0-174">**100Base-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="02ab0-174">**100Base-SX** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>

<span data-ttu-id="02ab0-175">**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="02ab0-175">**1000Base-SX** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>

<span data-ttu-id="02ab0-176">**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="02ab0-176">**1000Base-LX** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>

<span data-ttu-id="02ab0-177">**1000Base-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="02ab0-177">**1000Base-CX** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>

<span data-ttu-id="02ab0-178">**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="02ab0-178">**10GBase-SR** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>

<span data-ttu-id="02ab0-179">**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="02ab0-179">**10GBase-SW** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>

<span data-ttu-id="02ab0-180">**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="02ab0-180">**10GBase-LX4** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>

<span data-ttu-id="02ab0-181">**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="02ab0-181">**10GBase-LR** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>

<span data-ttu-id="02ab0-182">**10GBASE-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="02ab0-182">**10GBase-LW** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>

<span data-ttu-id="02ab0-183">**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="02ab0-183">**10GBase-ER** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>

<span data-ttu-id="02ab0-184">**10GBASE-uevo** (111)</span><span class="sxs-lookup"><span data-stu-id="02ab0-184">**10GBase-EW** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="02ab0-185">**Proveedor reservado** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="02ab0-185">**Vendor Reserved** (16000..65535)</span></span>


<span data-ttu-id="02ab0-186"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="02ab0-186"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="02ab0-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02ab0-187">Requirements</span></span>



| <span data-ttu-id="02ab0-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="02ab0-188">Requirement</span></span> | <span data-ttu-id="02ab0-189">Value</span><span class="sxs-lookup"><span data-stu-id="02ab0-189">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02ab0-190">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02ab0-190">Minimum supported client</span></span><br/> | <span data-ttu-id="02ab0-191">Windows 8</span><span class="sxs-lookup"><span data-stu-id="02ab0-191">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="02ab0-192">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="02ab0-192">Minimum supported server</span></span><br/> | <span data-ttu-id="02ab0-193">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="02ab0-193">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="02ab0-194">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="02ab0-194">Namespace</span></span><br/>                | <span data-ttu-id="02ab0-195">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="02ab0-195">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="02ab0-196">MOF</span><span class="sxs-lookup"><span data-stu-id="02ab0-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02ab0-197"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="02ab0-197"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="02ab0-198">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="02ab0-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02ab0-199"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="02ab0-199"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="02ab0-200">Vea también</span><span class="sxs-lookup"><span data-stu-id="02ab0-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02ab0-201">**\_NETWORKPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="02ab0-201">**CIM\_NetworkPort**</span></span>](cim-networkport.md)
</dt> </dl>

 

