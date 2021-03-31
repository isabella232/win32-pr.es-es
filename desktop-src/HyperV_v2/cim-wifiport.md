---
description: Representa un dispositivo de comunicaciones de red de área local inalámbrica que se ajusta a la serie de especificaciones de IEEE 802,11.
ms.assetid: c4e3345f-5c7d-4d1d-9a94-64112d7334ff
title: CIM_WiFiPort (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_WiFiPort
- CIM_WiFiPort.Speed
- CIM_WiFiPort.MaxSpeed
- CIM_WiFiPort.PortType
- CIM_WiFiPort.PermanentAddress
- CIM_WiFiPort.NetworkAddresses
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 098bd0a3795f3e8e0531be5286a65b79d9f6ee0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910397"
---
# <a name="cim_wifiport-class"></a><span data-ttu-id="ae450-103">\_Clase WiFiPort de CIM</span><span class="sxs-lookup"><span data-stu-id="ae450-103">CIM\_WiFiPort class</span></span>

<span data-ttu-id="ae450-104">Representa un dispositivo de comunicaciones de red de área local inalámbrica que se ajusta a la serie de especificaciones de IEEE 802,11.</span><span class="sxs-lookup"><span data-stu-id="ae450-104">Represents a wireless local area network communications device that conforms to the IEEE 802.11 series of specifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae450-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae450-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_WiFiPort : CIM_NetworkPort
{
  uint64 Speed;
  uint64 MaxSpeed;
  uint16 PortType;
  string PermanentAddress;
  string NetworkAddresses[];
};
```

## <a name="members"></a><span data-ttu-id="ae450-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="ae450-106">Members</span></span>

<span data-ttu-id="ae450-107">La clase **CIM \_ WiFiPort** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ae450-107">The **CIM\_WiFiPort** class has these types of members:</span></span>

-   [<span data-ttu-id="ae450-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ae450-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ae450-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ae450-109">Properties</span></span>

<span data-ttu-id="ae450-110">La clase **CIM \_ WiFiPort** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ae450-110">The **CIM\_WiFiPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ae450-111">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="ae450-111">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae450-112">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ae450-112">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ae450-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae450-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae450-114">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxSpeed")</span><span class="sxs-lookup"><span data-stu-id="ae450-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("MaxSpeed")</span></span>
</dt> </dl>

<span data-ttu-id="ae450-115">El ancho de banda máximo admitido, en bits por segundo, basado en el modo de funcionamiento especificado en la propiedad **portType** .</span><span class="sxs-lookup"><span data-stu-id="ae450-115">The maximum supported bandwidth, in bits per second, based on the operating mode specified in the **PortType** property.</span></span> <span data-ttu-id="ae450-116">Por ejemplo, **MaxSpeed** es "11 millones" Si **PortType** contiene "71" (802.11 b).</span><span class="sxs-lookup"><span data-stu-id="ae450-116">For example, **MaxSpeed** is "11000000" if **PortType** contains "71" (802.11b).</span></span>

</dd> <dt>

<span data-ttu-id="ae450-117">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="ae450-117">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae450-118">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="ae450-118">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ae450-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae450-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae450-120">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NetworkAddresses")</span><span class="sxs-lookup"><span data-stu-id="ae450-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NetworkAddresses")</span></span>
</dt> </dl>

<span data-ttu-id="ae450-121">Una matriz que contiene las direcciones MAC de IEEE 802 EUI-48.</span><span class="sxs-lookup"><span data-stu-id="ae450-121">An array that contains the IEEE 802 EUI-48 MAC addresses.</span></span> <span data-ttu-id="ae450-122">La dirección MAC tiene el formato de doce dígitos hexadecimales, donde cada par representa uno de los seis octetos de la dirección MAC en orden de bits canónico.</span><span class="sxs-lookup"><span data-stu-id="ae450-122">The MAC address is formatted as twelve hexadecimal digits, with each pair representing one of the six octets of the MAC address in canonical bit order.</span></span>

</dd> <dt>

<span data-ttu-id="ae450-123">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="ae450-123">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae450-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ae450-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae450-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae450-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae450-126">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PermanentAddress")</span><span class="sxs-lookup"><span data-stu-id="ae450-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PermanentAddress")</span></span>
</dt> </dl>

<span data-ttu-id="ae450-127">La dirección MAC de IEEE 802 EUI-48 del puerto.</span><span class="sxs-lookup"><span data-stu-id="ae450-127">The IEEE 802 EUI-48 MAC address of the port.</span></span> <span data-ttu-id="ae450-128">La dirección MAC tiene el formato de doce dígitos hexadecimales, donde cada par representa uno de los seis octetos de la dirección MAC en orden de bits canónico.</span><span class="sxs-lookup"><span data-stu-id="ae450-128">The MAC address is formatted as twelve hexadecimal digits, with each pair representing one of the six octets of the MAC address in canonical bit order.</span></span>

</dd> <dt>

<span data-ttu-id="ae450-129">**PortType**</span><span class="sxs-lookup"><span data-stu-id="ae450-129">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae450-130">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae450-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae450-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae450-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae450-132">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("portType")</span><span class="sxs-lookup"><span data-stu-id="ae450-132">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span></span>
</dt> </dl>

<span data-ttu-id="ae450-133">El modo de funcionamiento 802,11 que está habilitado en el puerto.</span><span class="sxs-lookup"><span data-stu-id="ae450-133">The 802.11 operating mode that is enabled on the port.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="ae450-134">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="ae450-134">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="ae450-135">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="ae450-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11a"></span><span id="802.11A"></span>

<span data-ttu-id="ae450-136">**802.11 a** (70)</span><span class="sxs-lookup"><span data-stu-id="ae450-136">**802.11a** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11b"></span><span id="802.11B"></span>

<span data-ttu-id="ae450-137">**802.11 b** (71)</span><span class="sxs-lookup"><span data-stu-id="ae450-137">**802.11b** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11g"></span><span id="802.11G"></span>

<span data-ttu-id="ae450-138">**802.11 g** (72)</span><span class="sxs-lookup"><span data-stu-id="ae450-138">**802.11g** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="802.11n"></span><span id="802.11N"></span>

<span data-ttu-id="ae450-139">**802.11 n** (73)</span><span class="sxs-lookup"><span data-stu-id="ae450-139">**802.11n** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="ae450-140">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="ae450-140">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="ae450-141">**Proveedor reservado** (16000...)</span><span class="sxs-lookup"><span data-stu-id="ae450-141">**Vendor Reserved** (16000..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ae450-142">**Velocidad**</span><span class="sxs-lookup"><span data-stu-id="ae450-142">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae450-143">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="ae450-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="ae450-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ae450-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae450-145">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("velocidad")</span><span class="sxs-lookup"><span data-stu-id="ae450-145">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Speed")</span></span>
</dt> </dl>

<span data-ttu-id="ae450-146">La velocidad de datos a la que se recibió la unidad de datos del protocolo PPDU (PLCP (Protocolo de convergencia de capa física) actual, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="ae450-146">The data rate at which the current PPDU (PLCP (Physical Layer Convergence Protocol) Protocol Data Unit) was received, in bits per second.</span></span> <span data-ttu-id="ae450-147">Este valor se codifica en los primeros 4 bits del encabezado PLCP en cada fotograma PLCP.</span><span class="sxs-lookup"><span data-stu-id="ae450-147">This value is encoded in the first 4 bits of the PLCP header in each PLCP frame.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ae450-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae450-148">Requirements</span></span>



| <span data-ttu-id="ae450-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae450-149">Requirement</span></span> | <span data-ttu-id="ae450-150">Value</span><span class="sxs-lookup"><span data-stu-id="ae450-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae450-151">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae450-151">Minimum supported client</span></span><br/> | <span data-ttu-id="ae450-152">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ae450-152">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="ae450-153">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae450-153">Minimum supported server</span></span><br/> | <span data-ttu-id="ae450-154">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ae450-154">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="ae450-155">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ae450-155">Namespace</span></span><br/>                | <span data-ttu-id="ae450-156">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ae450-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ae450-157">MOF</span><span class="sxs-lookup"><span data-stu-id="ae450-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae450-158"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae450-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae450-159">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ae450-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae450-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ae450-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ae450-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="ae450-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae450-162">**\_NETWORKPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="ae450-162">**CIM\_NetworkPort**</span></span>](cim-networkport.md)
</dt> </dl>

 

