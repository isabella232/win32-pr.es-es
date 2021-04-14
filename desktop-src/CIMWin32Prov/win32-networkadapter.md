---
description: La clase Win32 adaptador de la \_ clase está en desuso. Use la \_ clase msft NetAdapter en su lugar. La \_ clase NetworkAdapterWMI de Win32 representa un adaptador de red de un equipo que ejecuta un sistema operativo Windows.
ms.assetid: f79cb2a1-a249-479d-a495-37a44fdea995
ms.tgt_platform: multiple
title: Win32_NetworkAdapter (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapter
- Win32_NetworkAdapter.Reset
- Win32_NetworkAdapter.SetPowerState
- Win32_NetworkAdapter.AdapterType
- Win32_NetworkAdapter.AdapterTypeID
- Win32_NetworkAdapter.AutoSense
- Win32_NetworkAdapter.Availability
- Win32_NetworkAdapter.Caption
- Win32_NetworkAdapter.ConfigManagerErrorCode
- Win32_NetworkAdapter.ConfigManagerUserConfig
- Win32_NetworkAdapter.CreationClassName
- Win32_NetworkAdapter.Description
- Win32_NetworkAdapter.DeviceID
- Win32_NetworkAdapter.ErrorCleared
- Win32_NetworkAdapter.ErrorDescription
- Win32_NetworkAdapter.GUID
- Win32_NetworkAdapter.Index
- Win32_NetworkAdapter.InstallDate
- Win32_NetworkAdapter.Installed
- Win32_NetworkAdapter.InterfaceIndex
- Win32_NetworkAdapter.LastErrorCode
- Win32_NetworkAdapter.MACAddress
- Win32_NetworkAdapter.Manufacturer
- Win32_NetworkAdapter.MaxNumberControlled
- Win32_NetworkAdapter.MaxSpeed
- Win32_NetworkAdapter.Name
- Win32_NetworkAdapter.NetConnectionID
- Win32_NetworkAdapter.NetConnectionStatus
- Win32_NetworkAdapter.NetEnabled
- Win32_NetworkAdapter.NetworkAddresses
- Win32_NetworkAdapter.PermanentAddress
- Win32_NetworkAdapter.PhysicalAdapter
- Win32_NetworkAdapter.PNPDeviceID
- Win32_NetworkAdapter.PowerManagementCapabilities
- Win32_NetworkAdapter.PowerManagementSupported
- Win32_NetworkAdapter.ProductName
- Win32_NetworkAdapter.ServiceName
- Win32_NetworkAdapter.Speed
- Win32_NetworkAdapter.Status
- Win32_NetworkAdapter.StatusInfo
- Win32_NetworkAdapter.SystemCreationClassName
- Win32_NetworkAdapter.SystemName
- Win32_NetworkAdapter.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 22718802370995cc0515e3f63e731cc86d37eb0f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496601"
---
# <a name="win32_networkadapter-class"></a><span data-ttu-id="2209a-105">Win32 \_ adaptador de clase</span><span class="sxs-lookup"><span data-stu-id="2209a-105">Win32\_NetworkAdapter class</span></span>

<span data-ttu-id="2209a-106">La clase **Win32 \_ adaptador** de la clase está en desuso.</span><span class="sxs-lookup"><span data-stu-id="2209a-106">The **Win32\_NetworkAdapter** class is deprecated.</span></span> <span data-ttu-id="2209a-107">Use la clase [**msft \_ NetAdapter**](/previous-versions/windows/desktop/legacy/hh968170(v=vs.85)) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="2209a-107">Use the [**MSFT\_NetAdapter**](/previous-versions/windows/desktop/legacy/hh968170(v=vs.85)) class instead.</span></span> <span data-ttu-id="2209a-108">La [clase WMI](../wmisdk/retrieving-a-class.md) de **Win32 \_ adaptador** de red representa un adaptador de red de un equipo que ejecuta un sistema operativo Windows.</span><span class="sxs-lookup"><span data-stu-id="2209a-108">The **Win32\_NetworkAdapter**[WMI class](../wmisdk/retrieving-a-class.md) represents a network adapter of a computer running a Windows operating system.</span></span>

<span data-ttu-id="2209a-109">**Win32 \_ El adaptador** de solo proporciona datos IPv4.</span><span class="sxs-lookup"><span data-stu-id="2209a-109">**Win32\_NetworkAdapter** only supplies IPv4 data.</span></span> <span data-ttu-id="2209a-110">Para obtener más información, consulte [compatibilidad con IPv6 e IPv4 en WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-110">For more information, see [IPv6 and IPv4 Support in WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).</span></span>

<span data-ttu-id="2209a-111">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2209a-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2209a-112">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="2209a-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2209a-113">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2209a-113">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapter : CIM_NetworkAdapter
{
  string   AdapterType;
  uint16   AdapterTypeID;
  boolean  AutoSense;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   GUID;
  uint32   Index;
  datetime InstallDate;
  boolean  Installed;
  uint32   InterfaceIndex;
  uint32   LastErrorCode;
  string   MACAddress;
  string   Manufacturer;
  uint32   MaxNumberControlled;
  uint64   MaxSpeed;
  string   Name;
  string   NetConnectionID;
  uint16   NetConnectionStatus;
  boolean  NetEnabled;
  string   NetworkAddresses[];
  string   PermanentAddress;
  boolean  PhysicalAdapter;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   ProductName;
  string   ServiceName;
  uint64   Speed;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="2209a-114">Miembros</span><span class="sxs-lookup"><span data-stu-id="2209a-114">Members</span></span>

<span data-ttu-id="2209a-115">La clase **Win32 \_ adaptador** de tipo tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2209a-115">The **Win32\_NetworkAdapter** class has these types of members:</span></span>

-   [<span data-ttu-id="2209a-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="2209a-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="2209a-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2209a-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2209a-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="2209a-118">Methods</span></span>

<span data-ttu-id="2209a-119">La clase **Win32 \_ adaptador** de tipo tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="2209a-119">The **Win32\_NetworkAdapter** class has these methods.</span></span>



| <span data-ttu-id="2209a-120">Método</span><span class="sxs-lookup"><span data-stu-id="2209a-120">Method</span></span>                                                          | <span data-ttu-id="2209a-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="2209a-121">Description</span></span>                                                                                                                                                                                                                     |
|:----------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2209a-122">**Activa**</span><span class="sxs-lookup"><span data-stu-id="2209a-122">**Disable**</span></span>](disable-method-in-class-win32-networkadapter.md) | <span data-ttu-id="2209a-123">Deshabilita el adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="2209a-123">Disables the network adapter.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="2209a-124">**Habilitar**</span><span class="sxs-lookup"><span data-stu-id="2209a-124">**Enable**</span></span>](enable-method-in-class-win32-networkadapter.md)   | <span data-ttu-id="2209a-125">Habilita el adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="2209a-125">Enables the network adapter.</span></span><br/>                                                                                                                                                                                         |
| <span data-ttu-id="2209a-126">**Reset**</span><span class="sxs-lookup"><span data-stu-id="2209a-126">**Reset**</span></span>                                                       | <span data-ttu-id="2209a-127">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="2209a-127">Not implemented.</span></span> <span data-ttu-id="2209a-128">Para obtener más información sobre cómo implementar este método, vea el método [**RESET**](reset-method-in-class-cim-controller.md) en [**el \_ adaptador**](cim-networkadapter.md)de datos de CIM.</span><span class="sxs-lookup"><span data-stu-id="2209a-128">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span><br/>                 |
| <span data-ttu-id="2209a-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="2209a-129">**SetPowerState**</span></span>                                               | <span data-ttu-id="2209a-130">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="2209a-130">Not implemented.</span></span> <span data-ttu-id="2209a-131">Para obtener más información sobre cómo implementar este método, vea el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) en [**el \_ adaptador**](cim-networkadapter.md)de datos de CIM.</span><span class="sxs-lookup"><span data-stu-id="2209a-131">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2209a-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2209a-132">Properties</span></span>

<span data-ttu-id="2209a-133">La clase **Win32 \_ adaptador** de tipo tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2209a-133">The **Win32\_NetworkAdapter** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2209a-134">**AdapterType**</span><span class="sxs-lookup"><span data-stu-id="2209a-134">**AdapterType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2209a-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-137">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID \_ gen \_ multimedia \_ en \_ uso](/windows-hardware/drivers/network/oid-gen-media-in-use)")</span><span class="sxs-lookup"><span data-stu-id="2209a-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID\_GEN\_MEDIA\_IN\_USE](/windows-hardware/drivers/network/oid-gen-media-in-use)")</span></span>
</dt> </dl>

<span data-ttu-id="2209a-138">Medio de red en uso.</span><span class="sxs-lookup"><span data-stu-id="2209a-138">Network medium in use.</span></span> <span data-ttu-id="2209a-139">Los adaptadores de red son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="2209a-139">The network adapters are as follows:</span></span>

<dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="2209a-140">**Ethernet 802,3** ("Ethernet 802,3")</span><span class="sxs-lookup"><span data-stu-id="2209a-140">**Ethernet 802.3** ("Ethernet 802.3")</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring_802.5"></span><span id="token_ring_802.5"></span><span id="TOKEN_RING_802.5"></span>

<span data-ttu-id="2209a-141">**Token ring 802,5** ("token ring 802,5")</span><span class="sxs-lookup"><span data-stu-id="2209a-141">**Token Ring 802.5** ("Token Ring 802.5")</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_Distributed_Data_Interface__FDDI_"></span><span id="fiber_distributed_data_interface__fddi_"></span><span id="FIBER_DISTRIBUTED_DATA_INTERFACE__FDDI_"></span>

<span data-ttu-id="2209a-142">**Fiber Distributed Data Interface (FDDI)** ("Fiber Distributed Data Interface (FDDI)")</span><span class="sxs-lookup"><span data-stu-id="2209a-142">**Fiber Distributed Data Interface (FDDI)** ("Fiber Distributed Data Interface (FDDI)")</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Area_Network__WAN_"></span><span id="wide_area_network__wan_"></span><span id="WIDE_AREA_NETWORK__WAN_"></span>

<span data-ttu-id="2209a-143">**Red de área extensa (WAN)** ("red de área extensa (WAN)")</span><span class="sxs-lookup"><span data-stu-id="2209a-143">**Wide Area Network (WAN)** ("Wide Area Network (WAN)")</span></span>


</dt> <dd></dd> <dt>

<span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>

<span data-ttu-id="2209a-144">**LocalTalk** ("LocalTalk")</span><span class="sxs-lookup"><span data-stu-id="2209a-144">**LocalTalk** ("LocalTalk")</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_using_DIX_header_format"></span><span id="ethernet_using_dix_header_format"></span><span id="ETHERNET_USING_DIX_HEADER_FORMAT"></span>

<span data-ttu-id="2209a-145">**Ethernet con formato DIX de encabezado** ("Ethernet con formato de encabezado Dix")</span><span class="sxs-lookup"><span data-stu-id="2209a-145">**Ethernet using DIX header format** ("Ethernet using DIX header format")</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

<span data-ttu-id="2209a-146">**ARCNET** ("ARCNET")</span><span class="sxs-lookup"><span data-stu-id="2209a-146">**ARCNET** ("ARCNET")</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET__878.2_"></span><span id="arcnet__878.2_"></span>

<span data-ttu-id="2209a-147">**ARCNET (878,2)** ("ARCNET (878,2)")</span><span class="sxs-lookup"><span data-stu-id="2209a-147">**ARCNET (878.2)** ("ARCNET (878.2)")</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="2209a-148">**ATM** ("ATM")</span><span class="sxs-lookup"><span data-stu-id="2209a-148">**ATM** ("ATM")</span></span>


</dt> <dd></dd> <dt>

<span id="Wireless"></span><span id="wireless"></span><span id="WIRELESS"></span>

<span data-ttu-id="2209a-149">**Inalámbrica** ("inalámbrica")</span><span class="sxs-lookup"><span data-stu-id="2209a-149">**Wireless** ("Wireless")</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared_Wireless"></span><span id="infrared_wireless"></span><span id="INFRARED_WIRELESS"></span>

<span data-ttu-id="2209a-150">**Infrarrojos inalámbricos** ("inalámbrico de infrarrojos")</span><span class="sxs-lookup"><span data-stu-id="2209a-150">**Infrared Wireless** ("Infrared Wireless")</span></span>


</dt> <dd></dd> <dt>

<span id="Bpc"></span><span id="bpc"></span><span id="BPC"></span>

<span data-ttu-id="2209a-151">**BPC** ("BPC")</span><span class="sxs-lookup"><span data-stu-id="2209a-151">**Bpc** ("Bpc")</span></span>


</dt> <dd></dd> <dt>

<span id="CoWan"></span><span id="cowan"></span><span id="COWAN"></span>

<span data-ttu-id="2209a-152">**CoWan** ("CoWan")</span><span class="sxs-lookup"><span data-stu-id="2209a-152">**CoWan** ("CoWan")</span></span>


</dt> <dd></dd> <dt>

<span id="1394"></span>

<span data-ttu-id="2209a-153">**1394** ("1394")</span><span class="sxs-lookup"><span data-stu-id="2209a-153">**1394** ("1394")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2209a-154">**AdapterTypeID**</span><span class="sxs-lookup"><span data-stu-id="2209a-154">**AdapterTypeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-155">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2209a-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-157">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID \_ gen \_ multimedia \_ en \_ uso](/windows-hardware/drivers/network/oid-gen-media-in-use)")</span><span class="sxs-lookup"><span data-stu-id="2209a-157">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID\_GEN\_MEDIA\_IN\_USE](/windows-hardware/drivers/network/oid-gen-media-in-use)")</span></span>
</dt> </dl>

<span data-ttu-id="2209a-158">Medio de red en uso.</span><span class="sxs-lookup"><span data-stu-id="2209a-158">Network medium in use.</span></span> <span data-ttu-id="2209a-159">Devuelve la misma información que la propiedad **AdapterType** , excepto que la información tiene el formato de un entero.</span><span class="sxs-lookup"><span data-stu-id="2209a-159">Returns the same information as the **AdapterType** property, except that the information is in the form of an integer.</span></span>

<dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="2209a-160">**Ethernet 802,3** (0)</span><span class="sxs-lookup"><span data-stu-id="2209a-160">**Ethernet 802.3** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring_802.5"></span><span id="token_ring_802.5"></span><span id="TOKEN_RING_802.5"></span>

<span data-ttu-id="2209a-161">**Token Ring 802,5** (1)</span><span class="sxs-lookup"><span data-stu-id="2209a-161">**Token Ring 802.5** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_Distributed_Data_Interface__FDDI_"></span><span id="fiber_distributed_data_interface__fddi_"></span><span id="FIBER_DISTRIBUTED_DATA_INTERFACE__FDDI_"></span>

<span data-ttu-id="2209a-162">**Fiber Distributed Data Interface (FDDI)** (2)</span><span class="sxs-lookup"><span data-stu-id="2209a-162">**Fiber Distributed Data Interface (FDDI)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Area_Network__WAN_"></span><span id="wide_area_network__wan_"></span><span id="WIDE_AREA_NETWORK__WAN_"></span>

<span data-ttu-id="2209a-163">**Red de área extensa (WAN)** (3)</span><span class="sxs-lookup"><span data-stu-id="2209a-163">**Wide Area Network (WAN)** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>

<span data-ttu-id="2209a-164">**LocalTalk** (4)</span><span class="sxs-lookup"><span data-stu-id="2209a-164">**LocalTalk** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_using_DIX_header_format"></span><span id="ethernet_using_dix_header_format"></span><span id="ETHERNET_USING_DIX_HEADER_FORMAT"></span>

<span data-ttu-id="2209a-165">**Ethernet con formato DIX de encabezado** (5)</span><span class="sxs-lookup"><span data-stu-id="2209a-165">**Ethernet using DIX header format** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

<span data-ttu-id="2209a-166">**ARCNET** (6)</span><span class="sxs-lookup"><span data-stu-id="2209a-166">**ARCNET** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET__878.2_"></span><span id="arcnet__878.2_"></span>

<span data-ttu-id="2209a-167">**ARCNET (878,2)** (7)</span><span class="sxs-lookup"><span data-stu-id="2209a-167">**ARCNET (878.2)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="2209a-168">**ATM** (8)</span><span class="sxs-lookup"><span data-stu-id="2209a-168">**ATM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Wireless"></span><span id="wireless"></span><span id="WIRELESS"></span>

<span data-ttu-id="2209a-169">**Inalámbrica** (9)</span><span class="sxs-lookup"><span data-stu-id="2209a-169">**Wireless** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared_Wireless"></span><span id="infrared_wireless"></span><span id="INFRARED_WIRELESS"></span>

<span data-ttu-id="2209a-170">**Inalámbrico de infrarrojos** (10)</span><span class="sxs-lookup"><span data-stu-id="2209a-170">**Infrared Wireless** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Bpc"></span><span id="bpc"></span><span id="BPC"></span>

<span data-ttu-id="2209a-171">**BPC** (11)</span><span class="sxs-lookup"><span data-stu-id="2209a-171">**Bpc** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="CoWan"></span><span id="cowan"></span><span id="COWAN"></span>

<span data-ttu-id="2209a-172">**CoWan** (12)</span><span class="sxs-lookup"><span data-stu-id="2209a-172">**CoWan** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="1394"></span>

<span data-ttu-id="2209a-173">**1394** (13)</span><span class="sxs-lookup"><span data-stu-id="2209a-173">**1394** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2209a-174">**Percepción automática**</span><span class="sxs-lookup"><span data-stu-id="2209a-174">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-175">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2209a-175">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2209a-177">Si **es true**, el adaptador de red puede determinar automáticamente la velocidad de los medios de red o conectados.</span><span class="sxs-lookup"><span data-stu-id="2209a-177">If **True**, the network adapter can automatically determine the speed of the attached or network media.</span></span>

<span data-ttu-id="2209a-178">Esta propiedad se hereda de [**la \_ adaptador de adaptador CIM**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-178">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="2209a-179">Esta propiedad aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="2209a-179">This property has not been implemented yet.</span></span> <span data-ttu-id="2209a-180">Devuelve un valor **null** de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2209a-180">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="2209a-181">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="2209a-181">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-182">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2209a-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-184">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="2209a-184">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="2209a-185">Disponibilidad y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2209a-185">Availability and status of the device.</span></span>

<span data-ttu-id="2209a-186">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-186">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2209a-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2209a-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2209a-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="2209a-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="2209a-189"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>En **ejecución/corriente completa** (3)</span><span class="sxs-lookup"><span data-stu-id="2209a-189"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-190">En ejecución o completa</span><span class="sxs-lookup"><span data-stu-id="2209a-190">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="2209a-191"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**ADVERTENCIA** (4)</span><span class="sxs-lookup"><span data-stu-id="2209a-191"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="2209a-192"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (5)</span><span class="sxs-lookup"><span data-stu-id="2209a-192"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2209a-193"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (6)</span><span class="sxs-lookup"><span data-stu-id="2209a-193"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="2209a-194"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desconectar (7** )</span><span class="sxs-lookup"><span data-stu-id="2209a-194"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="2209a-195"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>Sin **conexión (8** )</span><span class="sxs-lookup"><span data-stu-id="2209a-195"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="2209a-196"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fuera del deber** (9)</span><span class="sxs-lookup"><span data-stu-id="2209a-196"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2209a-197"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="2209a-197"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="2209a-198"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**No instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="2209a-198"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="2209a-199"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Error de instalación** (12)</span><span class="sxs-lookup"><span data-stu-id="2209a-199"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="2209a-200"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Ahorro **de energía: desconocido** (13)</span><span class="sxs-lookup"><span data-stu-id="2209a-200"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-201">Se sabe que el dispositivo está en un estado de ahorro de energía, pero su estado exacto es desconocido.</span><span class="sxs-lookup"><span data-stu-id="2209a-201">The device is known to be in a power save state, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="2209a-202"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Ahorro **de energía: modo de baja energía** (14)</span><span class="sxs-lookup"><span data-stu-id="2209a-202"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-203">El dispositivo se encuentra en un estado de ahorro de energía, pero sigue funcionando y puede mostrar un rendimiento degradado.</span><span class="sxs-lookup"><span data-stu-id="2209a-203">The device is in a power save state, but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="2209a-204"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Ahorro **de energía: en espera** (15)</span><span class="sxs-lookup"><span data-stu-id="2209a-204"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-205">El dispositivo no funciona, pero puede que se ponga en marcha rápidamente.</span><span class="sxs-lookup"><span data-stu-id="2209a-205">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="2209a-206"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energía** (16)</span><span class="sxs-lookup"><span data-stu-id="2209a-206"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="2209a-207"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Ahorro **de energía: ADVERTENCIA** (17)</span><span class="sxs-lookup"><span data-stu-id="2209a-207"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-208">El dispositivo está en un estado de advertencia, pero también en un estado de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="2209a-208">The device is in a warning state, though also in a power save state.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="2209a-209"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>En **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="2209a-209"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-210">El dispositivo está en pausa.</span><span class="sxs-lookup"><span data-stu-id="2209a-210">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="2209a-211"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**No está listo** (19)</span><span class="sxs-lookup"><span data-stu-id="2209a-211"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-212">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="2209a-212">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="2209a-213"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**No configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="2209a-213"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-214">El dispositivo no está configurado.</span><span class="sxs-lookup"><span data-stu-id="2209a-214">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="2209a-215"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Inactivo** (21)</span><span class="sxs-lookup"><span data-stu-id="2209a-215"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-216">El dispositivo está en silencio.</span><span class="sxs-lookup"><span data-stu-id="2209a-216">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2209a-217">**Caption**</span><span class="sxs-lookup"><span data-stu-id="2209a-217">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-218">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2209a-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-219">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-220">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**displayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2209a-220">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2209a-221">Breve descripción del objeto: una cadena de una línea.</span><span class="sxs-lookup"><span data-stu-id="2209a-221">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="2209a-222">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-222">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2209a-223">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2209a-223">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-224">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2209a-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-225">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-226">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2209a-226">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2209a-227">Código de error de Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="2209a-227">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="2209a-228">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-228">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="2209a-229"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo funciona correctamente.**</span><span class="sxs-lookup"><span data-stu-id="2209a-229"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="2209a-230"> (0)</span><span class="sxs-lookup"><span data-stu-id="2209a-230">(0)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-231">El dispositivo funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="2209a-231">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="2209a-232"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo no está configurado correctamente.**</span><span class="sxs-lookup"><span data-stu-id="2209a-232"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="2209a-233">(1)</span><span class="sxs-lookup"><span data-stu-id="2209a-233">(1)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-234">El dispositivo no está configurado correctamente.</span><span class="sxs-lookup"><span data-stu-id="2209a-234">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2209a-235"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows no puede cargar el controlador para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2209a-235"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="2209a-236">(2)</span><span class="sxs-lookup"><span data-stu-id="2209a-236">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="2209a-237"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**Es posible que el controlador de este dispositivo esté dañado o que el sistema se esté quedando sin memoria u otros recursos.**</span><span class="sxs-lookup"><span data-stu-id="2209a-237"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="2209a-238">(3)</span><span class="sxs-lookup"><span data-stu-id="2209a-238">(3)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-239">Es posible que el controlador de este dispositivo esté dañado o que el sistema tenga poca memoria u otros recursos.</span><span class="sxs-lookup"><span data-stu-id="2209a-239">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2209a-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo no funciona correctamente. Uno de sus controladores o el registro pueden estar dañados.**</span><span class="sxs-lookup"><span data-stu-id="2209a-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="2209a-241">(4)</span><span class="sxs-lookup"><span data-stu-id="2209a-241">(4)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-242">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="2209a-242">Device is not working properly.</span></span> <span data-ttu-id="2209a-243">Uno de sus controladores o el registro pueden estar dañados.</span><span class="sxs-lookup"><span data-stu-id="2209a-243">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="2209a-244"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**El controlador para este dispositivo necesita un recurso que Windows no puede administrar.**</span><span class="sxs-lookup"><span data-stu-id="2209a-244"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="2209a-245">(5)</span><span class="sxs-lookup"><span data-stu-id="2209a-245">(5)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-246">El controlador del dispositivo requiere un recurso que Windows no puede administrar.</span><span class="sxs-lookup"><span data-stu-id="2209a-246">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="2209a-247"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**La configuración de arranque de este dispositivo entra en conflicto con otros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="2209a-247"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="2209a-248"> (6)</span><span class="sxs-lookup"><span data-stu-id="2209a-248">(6)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-249">La configuración de arranque para el dispositivo entra en conflicto con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="2209a-249">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="2209a-250"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**No se puede filtrar.**</span><span class="sxs-lookup"><span data-stu-id="2209a-250"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="2209a-251">(7)</span><span class="sxs-lookup"><span data-stu-id="2209a-251">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="2209a-252"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**Falta el cargador de controladores para el dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2209a-252"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="2209a-253">(8)</span><span class="sxs-lookup"><span data-stu-id="2209a-253">(8)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-254">Falta el cargador de controladores para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2209a-254">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="2209a-255"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo no funciona correctamente porque el firmware de control informa de los recursos para el dispositivo de forma incorrecta.**</span><span class="sxs-lookup"><span data-stu-id="2209a-255"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="2209a-256">(9)</span><span class="sxs-lookup"><span data-stu-id="2209a-256">(9)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-257">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="2209a-257">Device is not working properly.</span></span> <span data-ttu-id="2209a-258">El firmware de control informa incorrectamente de los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2209a-258">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="2209a-259"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo no se puede iniciar.**</span><span class="sxs-lookup"><span data-stu-id="2209a-259"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="2209a-260">(10)</span><span class="sxs-lookup"><span data-stu-id="2209a-260">(10)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-261">El dispositivo no se puede iniciar.</span><span class="sxs-lookup"><span data-stu-id="2209a-261">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="2209a-262"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Error en este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2209a-262"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="2209a-263">(11)</span><span class="sxs-lookup"><span data-stu-id="2209a-263">(11)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-264">Error en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2209a-264">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="2209a-265"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo no puede encontrar suficientes recursos libres que pueda usar.**</span><span class="sxs-lookup"><span data-stu-id="2209a-265"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="2209a-266">(12)</span><span class="sxs-lookup"><span data-stu-id="2209a-266">(12)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-267">El dispositivo no puede encontrar suficientes recursos disponibles para su uso.</span><span class="sxs-lookup"><span data-stu-id="2209a-267">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="2209a-268"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows no puede comprobar los recursos de este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2209a-268"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="2209a-269">(13)</span><span class="sxs-lookup"><span data-stu-id="2209a-269">(13)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-270">Windows no puede comprobar los recursos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2209a-270">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="2209a-271"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo no puede funcionar correctamente hasta que reinicie el equipo.**</span><span class="sxs-lookup"><span data-stu-id="2209a-271"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="2209a-272">(14)</span><span class="sxs-lookup"><span data-stu-id="2209a-272">(14)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-273">El dispositivo no puede funcionar correctamente hasta que se reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="2209a-273">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="2209a-274"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo no funciona correctamente porque es probable que haya un problema de reenumeración.**</span><span class="sxs-lookup"><span data-stu-id="2209a-274"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="2209a-275">(15)</span><span class="sxs-lookup"><span data-stu-id="2209a-275">(15)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-276">El dispositivo no funciona correctamente debido a un posible problema de reenumeración.</span><span class="sxs-lookup"><span data-stu-id="2209a-276">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="2209a-277"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows no puede identificar todos los recursos que usa este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2209a-277"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="2209a-278">(16)</span><span class="sxs-lookup"><span data-stu-id="2209a-278">(16)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-279">Windows no puede identificar todos los recursos que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2209a-279">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="2209a-280"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo solicita un tipo de recurso desconocido.**</span><span class="sxs-lookup"><span data-stu-id="2209a-280"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="2209a-281">(17)</span><span class="sxs-lookup"><span data-stu-id="2209a-281">(17)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-282">El dispositivo está solicitando un tipo de recurso desconocido.</span><span class="sxs-lookup"><span data-stu-id="2209a-282">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2209a-283"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Vuelva a instalar los controladores para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2209a-283"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="2209a-284">(18)</span><span class="sxs-lookup"><span data-stu-id="2209a-284">(18)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-285">Se deben volver a instalar los controladores de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="2209a-285">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="2209a-286"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Error al usar el cargador de VxD.**</span><span class="sxs-lookup"><span data-stu-id="2209a-286"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="2209a-287">(19)</span><span class="sxs-lookup"><span data-stu-id="2209a-287">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="2209a-288"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Es posible que el registro esté dañado.**</span><span class="sxs-lookup"><span data-stu-id="2209a-288"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="2209a-289">(20)</span><span class="sxs-lookup"><span data-stu-id="2209a-289">(20)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-290">Es posible que el registro esté dañado.</span><span class="sxs-lookup"><span data-stu-id="2209a-290">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="2209a-291"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware. Windows está quitando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2209a-291"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="2209a-292">(21)</span><span class="sxs-lookup"><span data-stu-id="2209a-292">(21)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-293">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="2209a-293">System failure.</span></span> <span data-ttu-id="2209a-294">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="2209a-294">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="2209a-295">Windows está quitando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2209a-295">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="2209a-296"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está deshabilitado.**</span><span class="sxs-lookup"><span data-stu-id="2209a-296"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="2209a-297">(22)</span><span class="sxs-lookup"><span data-stu-id="2209a-297">(22)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-298">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="2209a-298">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="2209a-299"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Error del sistema: intente cambiar el controlador para este dispositivo. Si eso no funciona, consulte la documentación del hardware.**</span><span class="sxs-lookup"><span data-stu-id="2209a-299"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="2209a-300">(23)</span><span class="sxs-lookup"><span data-stu-id="2209a-300">(23)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-301">Error del sistema.</span><span class="sxs-lookup"><span data-stu-id="2209a-301">System failure.</span></span> <span data-ttu-id="2209a-302">Si el cambio de controlador de dispositivo es ineficaz, consulte la documentación del hardware.</span><span class="sxs-lookup"><span data-stu-id="2209a-302">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="2209a-303"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.**</span><span class="sxs-lookup"><span data-stu-id="2209a-303"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="2209a-304">(24)</span><span class="sxs-lookup"><span data-stu-id="2209a-304">(24)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-305">El dispositivo no está presente, no funciona correctamente o no tiene todos sus controladores instalados.</span><span class="sxs-lookup"><span data-stu-id="2209a-305">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2209a-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2209a-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="2209a-307">(25)</span><span class="sxs-lookup"><span data-stu-id="2209a-307">(25)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-308">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2209a-308">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="2209a-309"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows todavía está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2209a-309"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="2209a-310">(26)</span><span class="sxs-lookup"><span data-stu-id="2209a-310">(26)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-311">Windows todavía está configurando el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2209a-311">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="2209a-312"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo no tiene una configuración de registro válida.**</span><span class="sxs-lookup"><span data-stu-id="2209a-312"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="2209a-313">(27)</span><span class="sxs-lookup"><span data-stu-id="2209a-313">(27)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-314">El dispositivo no tiene una configuración de registro válida.</span><span class="sxs-lookup"><span data-stu-id="2209a-314">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="2209a-315"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Los controladores de este dispositivo no están instalados.**</span><span class="sxs-lookup"><span data-stu-id="2209a-315"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="2209a-316">(28)</span><span class="sxs-lookup"><span data-stu-id="2209a-316">(28)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-317">Los controladores de dispositivo no están instalados.</span><span class="sxs-lookup"><span data-stu-id="2209a-317">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="2209a-318"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está deshabilitado porque el firmware del dispositivo no le proporcionó los recursos necesarios.**</span><span class="sxs-lookup"><span data-stu-id="2209a-318"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="2209a-319">(29)</span><span class="sxs-lookup"><span data-stu-id="2209a-319">(29)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-320">El dispositivo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="2209a-320">Device is disabled.</span></span> <span data-ttu-id="2209a-321">El firmware del dispositivo no proporcionó los recursos necesarios.</span><span class="sxs-lookup"><span data-stu-id="2209a-321">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="2209a-322"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo usa un recurso de solicitud de interrupción (IRQ) que otro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="2209a-322"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="2209a-323">(30)</span><span class="sxs-lookup"><span data-stu-id="2209a-323">(30)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-324">El dispositivo usa un recurso de IRQ que otro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="2209a-324">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="2209a-325"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo no funciona correctamente porque Windows no puede cargar los controladores necesarios para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="2209a-325"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="2209a-326">31</span><span class="sxs-lookup"><span data-stu-id="2209a-326">(31)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-327">El dispositivo no funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="2209a-327">Device is not working properly.</span></span> <span data-ttu-id="2209a-328">Windows no puede cargar los controladores de dispositivos necesarios.</span><span class="sxs-lookup"><span data-stu-id="2209a-328">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2209a-329">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="2209a-329">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-330">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2209a-330">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-331">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-332">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2209a-332">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2209a-333">Si es **true**, el dispositivo usa una configuración definida por el usuario.</span><span class="sxs-lookup"><span data-stu-id="2209a-333">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="2209a-334">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2209a-335">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2209a-335">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-336">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2209a-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-337">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-338">Calificadores: [ **\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="2209a-338">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="2209a-339">Nombre de la primera clase concreta que debe aparecer en la cadena de herencia utilizada en la creación de una instancia.</span><span class="sxs-lookup"><span data-stu-id="2209a-339">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="2209a-340">Cuando se usa con las otras propiedades de clave de la clase, la propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="2209a-340">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="2209a-341">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-341">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2209a-342">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="2209a-342">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-343">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2209a-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-344">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-345">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Descripción")</span><span class="sxs-lookup"><span data-stu-id="2209a-345">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2209a-346">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="2209a-346">Description of the object.</span></span>

<span data-ttu-id="2209a-347">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-347">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2209a-348">**ID**</span><span class="sxs-lookup"><span data-stu-id="2209a-348">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-349">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2209a-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-350">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-351">Calificadores: [**key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")</span><span class="sxs-lookup"><span data-stu-id="2209a-351">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E972-E325-11CE-BFC1-08002BE10318}")</span></span>
</dt> </dl>

<span data-ttu-id="2209a-352">Identificador único del adaptador de red de otros dispositivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="2209a-352">Unique identifier of the network adapter from other devices on the system.</span></span>

<span data-ttu-id="2209a-353">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-353">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2209a-354">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="2209a-354">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-355">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2209a-355">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-356">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2209a-357">Si es **true**, el error que se ha comunicado en **LastErrorCode** se borra.</span><span class="sxs-lookup"><span data-stu-id="2209a-357">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="2209a-358">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-358">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2209a-359">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="2209a-359">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-360">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2209a-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-361">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2209a-362">Más información sobre el error registrado en **LastErrorCode** e información sobre las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="2209a-362">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="2209a-363">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2209a-364">**GUID**</span><span class="sxs-lookup"><span data-stu-id="2209a-364">**GUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-365">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2209a-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-366">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2209a-367">Identificador único global para la conexión.</span><span class="sxs-lookup"><span data-stu-id="2209a-367">Globally unique identifier for the connection.</span></span>

</dd> <dt>

<span data-ttu-id="2209a-368">**Index**</span><span class="sxs-lookup"><span data-stu-id="2209a-368">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-369">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2209a-369">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-370">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-371">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ control \\ \\ Class \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")</span><span class="sxs-lookup"><span data-stu-id="2209a-371">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E972-E325-11CE-BFC1-08002BE10318}")</span></span>
</dt> </dl>

<span data-ttu-id="2209a-372">Número de índice del adaptador de red almacenado en el registro del sistema.</span><span class="sxs-lookup"><span data-stu-id="2209a-372">Index number of the network adapter, stored in the system registry.</span></span>

<span data-ttu-id="2209a-373">Ejemplo: 0</span><span class="sxs-lookup"><span data-stu-id="2209a-373">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="2209a-374">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2209a-374">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-375">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2209a-375">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-376">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-377">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**displayName**](../wmisdk/standard-qualifiers.md) (" instalación de fecha ")</span><span class="sxs-lookup"><span data-stu-id="2209a-377">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2209a-378">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="2209a-378">Date and time the object was installed.</span></span> <span data-ttu-id="2209a-379">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="2209a-379">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="2209a-380">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-380">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2209a-381">Esta propiedad aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="2209a-381">This property has not been implemented yet.</span></span> <span data-ttu-id="2209a-382">Devuelve un valor **null** de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2209a-382">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="2209a-383">**Instalado**</span><span class="sxs-lookup"><span data-stu-id="2209a-383">**Installed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-384">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2209a-384">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-385">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-386">Calificadores: [**desusados**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WIN32REGISTRY \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| DriverDate")</span><span class="sxs-lookup"><span data-stu-id="2209a-386">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|DriverDate")</span></span>
</dt> </dl>

<span data-ttu-id="2209a-387">Si es **true**, el adaptador de red está instalado en el sistema.</span><span class="sxs-lookup"><span data-stu-id="2209a-387">If **True**, the network adapter is installed in the system.</span></span>

</dd> <dt>

<span data-ttu-id="2209a-388">**InterfaceIndex**</span><span class="sxs-lookup"><span data-stu-id="2209a-388">**InterfaceIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-389">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2209a-389">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-390">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2209a-391">Valor de índice que identifica de forma única la interfaz de red local.</span><span class="sxs-lookup"><span data-stu-id="2209a-391">Index value that uniquely identifies the local network interface.</span></span> <span data-ttu-id="2209a-392">El valor de esta propiedad es el mismo que el valor de la propiedad **InterfaceIndex** de la instancia de [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) que representa la interfaz de red en la tabla de rutas.</span><span class="sxs-lookup"><span data-stu-id="2209a-392">The value in this property is the same as the value in the **InterfaceIndex** property in the instance of [**Win32\_IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) that represents the network interface in the route table.</span></span>

</dd> <dt>

<span data-ttu-id="2209a-393">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="2209a-393">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-394">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2209a-394">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-395">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2209a-396">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2209a-396">Last error code reported by the logical device.</span></span>

<span data-ttu-id="2209a-397">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2209a-398">**Mac**</span><span class="sxs-lookup"><span data-stu-id="2209a-398">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-399">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2209a-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-400">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-401">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("inesperados win32api \| Device INPUT and Output Functions \| [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)")</span><span class="sxs-lookup"><span data-stu-id="2209a-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)")</span></span>
</dt> </dl>

<span data-ttu-id="2209a-402">Dirección de control de acceso de medios para este adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="2209a-402">Media access control address for this network adapter.</span></span> <span data-ttu-id="2209a-403">Una dirección MAC es un número único de 48 bits asignado al adaptador de red por el fabricante.</span><span class="sxs-lookup"><span data-stu-id="2209a-403">A MAC address is a unique 48-bit number assigned to the network adapter by the manufacturer.</span></span> <span data-ttu-id="2209a-404">Identifica de forma única este adaptador de red y se usa para asignar comunicaciones de red TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="2209a-404">It uniquely identifies this network adapter and is used for mapping TCP/IP network communications.</span></span>

</dd> <dt>

<span data-ttu-id="2209a-405">**Le**</span><span class="sxs-lookup"><span data-stu-id="2209a-405">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-406">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2209a-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-407">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-408">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| manufacturer")</span><span class="sxs-lookup"><span data-stu-id="2209a-408">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="2209a-409">Nombre del fabricante del adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="2209a-409">Name of the network adapter's manufacturer.</span></span>

<span data-ttu-id="2209a-410">Ejemplo: "3COM"</span><span class="sxs-lookup"><span data-stu-id="2209a-410">Example: "3COM"</span></span>

</dd> <dt>

<span data-ttu-id="2209a-411">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="2209a-411">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-412">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2209a-412">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-413">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-414">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Puerto de bus DMTF \| 001,9 \| número máximo de datos adjuntos ")</span><span class="sxs-lookup"><span data-stu-id="2209a-414">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9\|Maximum Number of Attachments")</span></span>
</dt> </dl>

<span data-ttu-id="2209a-415">Número máximo de puertos directamente direccionables admitidos por este adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="2209a-415">Maximum number of directly addressable ports supported by this network adapter.</span></span> <span data-ttu-id="2209a-416">Se debe utilizar un valor de 0 (cero) si se desconoce el número.</span><span class="sxs-lookup"><span data-stu-id="2209a-416">A value of 0 (zero) should be used if the number is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="2209a-417">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="2209a-417">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-418">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2209a-418">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-419">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-420">Calificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="2209a-420">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="2209a-421">Velocidad máxima, en bits por segundo, del adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="2209a-421">Maximum speed, in bits per second, for the network adapter.</span></span>

<span data-ttu-id="2209a-422">Esta propiedad se hereda de [**la \_ adaptador de adaptador CIM**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-422">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="2209a-423">Esta propiedad aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="2209a-423">This property has not been implemented yet.</span></span> <span data-ttu-id="2209a-424">Devuelve un valor **null** de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2209a-424">It returns a **NULL** value by default.</span></span>

<span data-ttu-id="2209a-425">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2209a-425">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2209a-426">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="2209a-426">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-427">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2209a-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-428">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-429">Calificadores: [**displayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="2209a-429">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2209a-430">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="2209a-430">Label by which the object is known.</span></span> <span data-ttu-id="2209a-431">Cuando se subclasen, la propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="2209a-431">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="2209a-432">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-432">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2209a-433">**NetConnectionID**</span><span class="sxs-lookup"><span data-stu-id="2209a-433">**NetConnectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-434">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2209a-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-435">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2209a-435">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2209a-436">Nombre de la conexión de red tal y como aparece en el programa del panel de control **conexiones de red** .</span><span class="sxs-lookup"><span data-stu-id="2209a-436">Name of the network connection as it appears in the **Network Connections** Control Panel program.</span></span>

</dd> <dt>

<span data-ttu-id="2209a-437">**NetConnectionStatus**</span><span class="sxs-lookup"><span data-stu-id="2209a-437">**NetConnectionStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-438">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2209a-438">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-439">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2209a-440">Estado de la conexión del adaptador de red a la red.</span><span class="sxs-lookup"><span data-stu-id="2209a-440">State of the network adapter connection to the network.</span></span>

<dt>

<span id="Disconnected"></span><span id="disconnected"></span><span id="DISCONNECTED"></span>

<span data-ttu-id="2209a-441">**Desconectado** (0)</span><span class="sxs-lookup"><span data-stu-id="2209a-441">**Disconnected** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Connecting"></span><span id="connecting"></span><span id="CONNECTING"></span>

<span data-ttu-id="2209a-442">**Conectando** (1)</span><span class="sxs-lookup"><span data-stu-id="2209a-442">**Connecting** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Connected"></span><span id="connected"></span><span id="CONNECTED"></span>

<span data-ttu-id="2209a-443">**Conectado** (2)</span><span class="sxs-lookup"><span data-stu-id="2209a-443">**Connected** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disconnecting"></span><span id="disconnecting"></span><span id="DISCONNECTING"></span>

<span data-ttu-id="2209a-444">**Desconectar** (3)</span><span class="sxs-lookup"><span data-stu-id="2209a-444">**Disconnecting** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Not_Present"></span><span id="hardware_not_present"></span><span id="HARDWARE_NOT_PRESENT"></span>

<span data-ttu-id="2209a-445">**Hardware no presente** (4)</span><span class="sxs-lookup"><span data-stu-id="2209a-445">**Hardware Not Present** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Disabled"></span><span id="hardware_disabled"></span><span id="HARDWARE_DISABLED"></span>

<span data-ttu-id="2209a-446">**Hardware deshabilitado** (5)</span><span class="sxs-lookup"><span data-stu-id="2209a-446">**Hardware Disabled** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Malfunction"></span><span id="hardware_malfunction"></span><span id="HARDWARE_MALFUNCTION"></span>

<span data-ttu-id="2209a-447">**Funcionamiento defectuoso de hardware** (6)</span><span class="sxs-lookup"><span data-stu-id="2209a-447">**Hardware Malfunction** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Media_Disconnected"></span><span id="media_disconnected"></span><span id="MEDIA_DISCONNECTED"></span>

<span data-ttu-id="2209a-448">**Medios desconectados** (7)</span><span class="sxs-lookup"><span data-stu-id="2209a-448">**Media Disconnected** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Authenticating"></span><span id="authenticating"></span><span id="AUTHENTICATING"></span>

<span data-ttu-id="2209a-449">**Autenticación** (8)</span><span class="sxs-lookup"><span data-stu-id="2209a-449">**Authenticating** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Succeeded"></span><span id="authentication_succeeded"></span><span id="AUTHENTICATION_SUCCEEDED"></span>

<span data-ttu-id="2209a-450">**Autenticación correcta** (9)</span><span class="sxs-lookup"><span data-stu-id="2209a-450">**Authentication Succeeded** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Failed"></span><span id="authentication_failed"></span><span id="AUTHENTICATION_FAILED"></span>

<span data-ttu-id="2209a-451">**Error de autenticación** (10)</span><span class="sxs-lookup"><span data-stu-id="2209a-451">**Authentication Failed** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid_Address"></span><span id="invalid_address"></span><span id="INVALID_ADDRESS"></span>

<span data-ttu-id="2209a-452">**Dirección no válida** (11)</span><span class="sxs-lookup"><span data-stu-id="2209a-452">**Invalid Address** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Credentials_Required"></span><span id="credentials_required"></span><span id="CREDENTIALS_REQUIRED"></span>

<span data-ttu-id="2209a-453">**Credenciales necesarias** (12)</span><span class="sxs-lookup"><span data-stu-id="2209a-453">**Credentials Required** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2209a-454">**Otros**</span><span class="sxs-lookup"><span data-stu-id="2209a-454">**Other**</span></span>


</dt> <dd><span data-ttu-id="2209a-455">de 13 a 65535</span><span class="sxs-lookup"><span data-stu-id="2209a-455">13–65535</span></span></dd> </dl>

</dd> <dt>

<span data-ttu-id="2209a-456">**NetEnabled**</span><span class="sxs-lookup"><span data-stu-id="2209a-456">**NetEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-457">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2209a-457">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-458">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2209a-459">Indica si el adaptador está habilitado o no.</span><span class="sxs-lookup"><span data-stu-id="2209a-459">Indicates whether the adapter is enabled or not.</span></span> <span data-ttu-id="2209a-460">Si es **true**, el adaptador está habilitado.</span><span class="sxs-lookup"><span data-stu-id="2209a-460">If **True**, the adapter is enabled.</span></span> <span data-ttu-id="2209a-461">Puede habilitar o deshabilitar la NIC mediante los métodos [**enable**](enable-method-in-class-win32-networkadapter.md) y [**Disable**](disable-method-in-class-win32-networkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="2209a-461">You can enable or disable the NIC by using the [**Enable**](enable-method-in-class-win32-networkadapter.md) and [**Disable**](disable-method-in-class-win32-networkadapter.md) methods.</span></span>

</dd> <dt>

<span data-ttu-id="2209a-462">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="2209a-462">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-463">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="2209a-463">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="2209a-464">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-464">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-465">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Adaptador de red DMTF 802 puerto \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="2209a-465">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Network Adapter 802 Port\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="2209a-466">Matriz de direcciones de red para un adaptador.</span><span class="sxs-lookup"><span data-stu-id="2209a-466">Array of network addresses for an adapter.</span></span>

<span data-ttu-id="2209a-467">Esta propiedad se hereda de [**la \_ adaptador de adaptador CIM**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-467">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="2209a-468">Esta propiedad aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="2209a-468">This property has not been implemented yet.</span></span> <span data-ttu-id="2209a-469">Devuelve un valor **null** de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2209a-469">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="2209a-470">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="2209a-470">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-471">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2209a-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-472">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-473">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Adaptador de red DMTF 802 puerto \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="2209a-473">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Network Adapter 802 Port\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="2209a-474">Dirección de red codificada de forma rígida en un adaptador.</span><span class="sxs-lookup"><span data-stu-id="2209a-474">Network address hard-coded into an adapter.</span></span> <span data-ttu-id="2209a-475">Esta dirección codificada de forma rígida puede cambiarse mediante la actualización del firmware o la configuración del software.</span><span class="sxs-lookup"><span data-stu-id="2209a-475">This hard-coded address may be changed by firmware upgrade or software configuration.</span></span> <span data-ttu-id="2209a-476">Si es así, este campo debe actualizarse cuando se realiza el cambio.</span><span class="sxs-lookup"><span data-stu-id="2209a-476">If so, this field should be updated when the change is made.</span></span> <span data-ttu-id="2209a-477">La propiedad debe dejarse en blanco si no existe ninguna dirección codificada de forma rígida para el adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="2209a-477">The property should be left blank if no hard-coded address exists for the network adapter.</span></span>

<span data-ttu-id="2209a-478">Esta propiedad se hereda de [**la \_ adaptador de adaptador CIM**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-478">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="2209a-479">Esta propiedad aún no se ha implementado.</span><span class="sxs-lookup"><span data-stu-id="2209a-479">This property has not been implemented yet.</span></span> <span data-ttu-id="2209a-480">Devuelve un valor **null** de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2209a-480">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="2209a-481">**PhysicalAdapter**</span><span class="sxs-lookup"><span data-stu-id="2209a-481">**PhysicalAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-482">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2209a-482">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-483">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2209a-484">Indica si el adaptador es un adaptador físico o lógico.</span><span class="sxs-lookup"><span data-stu-id="2209a-484">Indicates whether the adapter is a physical or a logical adapter.</span></span> <span data-ttu-id="2209a-485">Si es **true**, el adaptador es físico.</span><span class="sxs-lookup"><span data-stu-id="2209a-485">If **True**, the adapter is physical.</span></span>

</dd> <dt>

<span data-ttu-id="2209a-486">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="2209a-486">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-487">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2209a-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-488">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-489">Calificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="2209a-489">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="2209a-490">Identificador de dispositivo de Windows Plug and Play del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2209a-490">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="2209a-491">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="2209a-492">Ejemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="2209a-492">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="2209a-493">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="2209a-493">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-494">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2209a-494">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="2209a-495">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-495">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2209a-496">Matriz de las capacidades específicas de energía relacionadas con el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2209a-496">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="2209a-497">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-497">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2209a-498"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="2209a-498"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="2209a-499"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (1)</span><span class="sxs-lookup"><span data-stu-id="2209a-499"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2209a-500"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="2209a-500"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2209a-501"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="2209a-501"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-502">Las características de administración de energía están habilitadas actualmente, pero el conjunto de características exacto es desconocido o la información no está disponible.</span><span class="sxs-lookup"><span data-stu-id="2209a-502">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="2209a-503"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de ahorro de energía introducidos automáticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="2209a-503"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-504">El dispositivo puede cambiar su estado de energía en función del uso u otros criterios.</span><span class="sxs-lookup"><span data-stu-id="2209a-504">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="2209a-505"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energía configurable** (5)</span><span class="sxs-lookup"><span data-stu-id="2209a-505"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-506">Se admite el método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="2209a-506">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="2209a-507">Este método se encuentra en la clase primaria de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) y se puede implementar.</span><span class="sxs-lookup"><span data-stu-id="2209a-507">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="2209a-508">Para obtener más información, vea [diseñar clases Managed Object Format (MOF)](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-508">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="2209a-509"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energía admitido** (6)</span><span class="sxs-lookup"><span data-stu-id="2209a-509"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-510">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de alimentación).</span><span class="sxs-lookup"><span data-stu-id="2209a-510">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="2209a-511"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>Se **admite el encendido con tiempo** (7)</span><span class="sxs-lookup"><span data-stu-id="2209a-511"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="2209a-512">Power-On de tiempo admitido</span><span class="sxs-lookup"><span data-stu-id="2209a-512">Timed Power-On Supported</span></span>

<span data-ttu-id="2209a-513">El método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) se puede invocar con el parámetro *PowerState* establecido en 5 (ciclo de energía) y la *hora* establecida en una fecha y hora específicas, o intervalo, para el encendido.</span><span class="sxs-lookup"><span data-stu-id="2209a-513">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2209a-514">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="2209a-514">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-515">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2209a-515">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-516">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2209a-517">Si **es true**, el dispositivo puede administrarse con energía (se puede poner en modo de suspensión, etc.).</span><span class="sxs-lookup"><span data-stu-id="2209a-517">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="2209a-518">La propiedad no indica que las características de administración de energía están habilitadas actualmente, solo que el dispositivo lógico es capaz de administrar energía.</span><span class="sxs-lookup"><span data-stu-id="2209a-518">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="2209a-519">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-519">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2209a-520">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="2209a-520">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-521">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2209a-521">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-522">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-523">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| ServiceName")</span><span class="sxs-lookup"><span data-stu-id="2209a-523">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|ServiceName")</span></span>
</dt> </dl>

<span data-ttu-id="2209a-524">Nombre del producto del adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="2209a-524">Product name of the network adapter.</span></span>

<span data-ttu-id="2209a-525">Ejemplo: "Fast EtherLink XL"</span><span class="sxs-lookup"><span data-stu-id="2209a-525">Example: "Fast EtherLink XL"</span></span>

</dd> <dt>

<span data-ttu-id="2209a-526">**ServiceName**</span><span class="sxs-lookup"><span data-stu-id="2209a-526">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-527">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2209a-527">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-528">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-528">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-529">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| ProductName")</span><span class="sxs-lookup"><span data-stu-id="2209a-529">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|ProductName")</span></span>
</dt> </dl>

<span data-ttu-id="2209a-530">Nombre del servicio del adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="2209a-530">Service name of the network adapter.</span></span> <span data-ttu-id="2209a-531">Este nombre suele ser más corto que el nombre completo del producto.</span><span class="sxs-lookup"><span data-stu-id="2209a-531">This name is usually shorter than the full product name.</span></span>

<span data-ttu-id="2209a-532">Ejemplo: "Elnkii"</span><span class="sxs-lookup"><span data-stu-id="2209a-532">Example: "Elnkii"</span></span>

</dd> <dt>

<span data-ttu-id="2209a-533">**Velocidad**</span><span class="sxs-lookup"><span data-stu-id="2209a-533">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-534">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2209a-534">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-535">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-535">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-536">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| RFC1213-MIB. ifSpeed "," MIF. \|Adaptador de red DMTF 802 puerto \| 001,5 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" bits por segundo ")</span><span class="sxs-lookup"><span data-stu-id="2209a-536">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|RFC1213-MIB.ifSpeed", "MIF.DMTF\|Network Adapter 802 Port\|001.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="2209a-537">Estimación del ancho de banda actual en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="2209a-537">Estimate of the current bandwidth in bits per second.</span></span> <span data-ttu-id="2209a-538">En el caso de los puntos de conexión que varían en ancho de banda o para aquellos en los que no se puede realizar una estimación precisa, esta propiedad debe contener el ancho de banda nominal.</span><span class="sxs-lookup"><span data-stu-id="2209a-538">For endpoints which vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span>

<span data-ttu-id="2209a-539">Esta propiedad se hereda de [**la \_ adaptador de adaptador CIM**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-539">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="2209a-540">Para obtener más información sobre el uso de valores **UInt64** en scripts, vea [scripting en WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2209a-540">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2209a-541">**Estado**</span><span class="sxs-lookup"><span data-stu-id="2209a-541">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-542">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2209a-542">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-543">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-544">Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**displayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="2209a-544">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2209a-545">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="2209a-545">Current status of the object.</span></span> <span data-ttu-id="2209a-546">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-546">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2209a-547">Los valores son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="2209a-547">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2209a-548">**Aceptar** ("Aceptar")</span><span class="sxs-lookup"><span data-stu-id="2209a-548">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2209a-549">**Error** ("error")</span><span class="sxs-lookup"><span data-stu-id="2209a-549">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2209a-550">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="2209a-550">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2209a-551">**Desconocido** ("desconocido")</span><span class="sxs-lookup"><span data-stu-id="2209a-551">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2209a-552">**Pred FAIL** ("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="2209a-552">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2209a-553">**Iniciando** ("iniciando")</span><span class="sxs-lookup"><span data-stu-id="2209a-553">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2209a-554">**Detener** ("detener")</span><span class="sxs-lookup"><span data-stu-id="2209a-554">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2209a-555">**Servicio** ("servicio")</span><span class="sxs-lookup"><span data-stu-id="2209a-555">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2209a-556">Con **estrés** ("acentuado")</span><span class="sxs-lookup"><span data-stu-id="2209a-556">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2209a-557">**Recover** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="2209a-557">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2209a-558">**Sin contacto** ("sin contacto")</span><span class="sxs-lookup"><span data-stu-id="2209a-558">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2209a-559">**Comunicación perdida** ("pérdida de comunicación")</span><span class="sxs-lookup"><span data-stu-id="2209a-559">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2209a-560">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="2209a-560">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-561">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2209a-561">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-562">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-562">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-563">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operativo DMTF \| 003,3 ")</span><span class="sxs-lookup"><span data-stu-id="2209a-563">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="2209a-564">Estado del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2209a-564">State of the logical device.</span></span> <span data-ttu-id="2209a-565">Si esta propiedad no se aplica al dispositivo lógico, se debe usar el valor 5 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="2209a-565">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="2209a-566">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-566">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2209a-567">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="2209a-567">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2209a-568">**Desconocido** (2)</span><span class="sxs-lookup"><span data-stu-id="2209a-568">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="2209a-569">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="2209a-569">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="2209a-570">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="2209a-570">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="2209a-571">**No aplicable** (5)</span><span class="sxs-lookup"><span data-stu-id="2209a-571">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="2209a-572">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2209a-572">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-573">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2209a-573">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-574">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-574">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-575">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="2209a-575">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="2209a-576">Valor de la propiedad **CreationClassName** del equipo de ámbito.</span><span class="sxs-lookup"><span data-stu-id="2209a-576">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="2209a-577">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-577">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2209a-578">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2209a-578">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-579">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2209a-579">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-580">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-581">Calificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ Sistema CIM**](cim-system.md).**Name**"), [**\_ clave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="2209a-581">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="2209a-582">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="2209a-582">Name of the scoping system.</span></span>

<span data-ttu-id="2209a-583">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-583">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="2209a-584">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="2209a-584">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2209a-585">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2209a-585">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2209a-586">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2209a-586">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2209a-587">Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Perflib \\ \\ 009 \| System up time")</span><span class="sxs-lookup"><span data-stu-id="2209a-587">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Perflib\\\\009\|System Up Time")</span></span>
</dt> </dl>

<span data-ttu-id="2209a-588">Fecha y hora de la última vez que se restableció el adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="2209a-588">Date and time the network adapter was last reset.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2209a-589">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2209a-589">Remarks</span></span>

<span data-ttu-id="2209a-590">La clase **Win32 el \_ adaptador** de tipo se deriva de la [**adaptador de \_ adaptador CIM**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="2209a-590">The **Win32\_NetworkAdapter** class is derived from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="2209a-591">En la lista siguiente se describen las clases de Asociator para el **\_ adaptador de Win32**.</span><span class="sxs-lookup"><span data-stu-id="2209a-591">The following list describes the Associator classes for **Win32\_NetworkAdapter**:</span></span>

-   [<span data-ttu-id="2209a-592">**Win32 \_ PnPEntity**</span><span class="sxs-lookup"><span data-stu-id="2209a-592">**Win32\_PnPEntity**</span></span>](win32-pnpentity.md)
-   [<span data-ttu-id="2209a-593">**ComputerSystem de Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="2209a-593">**Win32\_ComputerSystem**</span></span>](win32-computersystem.md)
-   [<span data-ttu-id="2209a-594">**Win32 \_ NetworkAdapterConfiguration**</span><span class="sxs-lookup"><span data-stu-id="2209a-594">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
-   [<span data-ttu-id="2209a-595">**Win32 \_ IRQResource**</span><span class="sxs-lookup"><span data-stu-id="2209a-595">**Win32\_IRQResource**</span></span>](win32-irqresource.md)
-   [<span data-ttu-id="2209a-596">**Win32 \_ DeviceMemoryAddress**</span><span class="sxs-lookup"><span data-stu-id="2209a-596">**Win32\_DeviceMemoryAddress**</span></span>](win32-devicememoryaddress.md)
-   [<span data-ttu-id="2209a-597">**Win32 \_ PortResource**</span><span class="sxs-lookup"><span data-stu-id="2209a-597">**Win32\_PortResource**</span></span>](win32-portresource.md)
-   [<span data-ttu-id="2209a-598">**Win32 \_ NetworkProtocol**</span><span class="sxs-lookup"><span data-stu-id="2209a-598">**Win32\_NetworkProtocol**</span></span>](win32-networkprotocol.md)
-   [<span data-ttu-id="2209a-599">**Win32 \_ SystemDriver**</span><span class="sxs-lookup"><span data-stu-id="2209a-599">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)

<span data-ttu-id="2209a-600">Muchos sistemas tienen varios adaptadores de red.</span><span class="sxs-lookup"><span data-stu-id="2209a-600">Many systems have a number of network adapters on them.</span></span> <span data-ttu-id="2209a-601">Considere la posibilidad de usar lo siguiente como referencia para buscar los adaptadores actuales:</span><span class="sxs-lookup"><span data-stu-id="2209a-601">Consider using the following as a reference to find the current adapters:</span></span>

``` syntax
AdapterType: "Ethernet 802.3"
MACAddress: String Length > 16
Availability: 3
PNPDeviceID: InStr ( PNPDeviceID, "PCI") = 1
Installed: vbTrue
ConfigManagerErrorCode: 0
: <keep this as an index to Win32_NetworkAdapterConfiguration>
```

<span data-ttu-id="2209a-602">Incluso con los calificadores anteriores, es probable que recupere más de un adaptador de red válido.</span><span class="sxs-lookup"><span data-stu-id="2209a-602">Even using the above qualifiers, you will likely retrieve more than one valid network adapter.</span></span> <span data-ttu-id="2209a-603">En ese caso, puede usar la siguiente información para calificar más la búsqueda de Win32 \_ NetworkAdapterConfiguration:</span><span class="sxs-lookup"><span data-stu-id="2209a-603">If that is the case, Then you can use the following information to further qualify your search of the Win32\_NetworkAdapterConfiguration:</span></span>

``` syntax
Index: <match to DeviceID above>
MACAddress: Length > 16
DefaultIPGateway: String Length > 6
DNSServerSearchOrder: Array of strings with length > 6
IPEnabled: vbTrue
IPAddress: Array of strings with length > 6
```

<span data-ttu-id="2209a-604">Una vez hecho esto, probablemente habrá reducido la lista a uno o dos adaptadores configurados.</span><span class="sxs-lookup"><span data-stu-id="2209a-604">Once you have done so, you will likely have reduced your list to one or two configured adapters.</span></span>

<span data-ttu-id="2209a-605">También puede usar el siguiente procedimiento para buscar el adaptador predeterminado:</span><span class="sxs-lookup"><span data-stu-id="2209a-605">You can also use the following procedure to find the default adapter:</span></span>

1.  <span data-ttu-id="2209a-606">Ejecute la siguiente consulta:</span><span class="sxs-lookup"><span data-stu-id="2209a-606">Run the following query:</span></span>

    `"SELECT InterfaceIndex, Destination FROM Win32_IP4RouteTable WHERE Destination='0.0.0.0'"`

    <span data-ttu-id="2209a-607">Solo debe tener un destino de red predeterminado 0.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="2209a-607">You should only have one default network destination 0.0.0.0.</span></span>

2.  <span data-ttu-id="2209a-608">Use **InterfaceIndex** para recuperar el adaptador de red que desee.</span><span class="sxs-lookup"><span data-stu-id="2209a-608">Use the **InterfaceIndex** to retrieve the Network Adapter you want.</span></span>

    `"SELECT * FROM Win32_NetworkAdapter WHERE InterfaceIndex=" + insertVariableHere`

## <a name="examples"></a><span data-ttu-id="2209a-609">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2209a-609">Examples</span></span>

<span data-ttu-id="2209a-610">En el ejemplo de código de PowerShell de [dos funciones de WMI](https://Gallery.TechNet.Microsoft.Com/Two-WMI-Functions-94c31b5f) de la galería de TechNet se usa el **\_ adaptador de Win32** para volver a crear el cmdlet [Get-NetAdapter](/powershell/module/netadapter/get-netadapter?view=win10-ps) de Windows.</span><span class="sxs-lookup"><span data-stu-id="2209a-610">The [Two WMI Functions](https://Gallery.TechNet.Microsoft.Com/Two-WMI-Functions-94c31b5f) PowerShell code example in the TechNet Gallery uses **Win32\_NetworkAdapter** to re-create the Windows [Get-NetAdapter](/powershell/module/netadapter/get-netadapter?view=win10-ps) cmdlet.</span></span>

<span data-ttu-id="2209a-611">El ejemplo de PowerShell [Get-ComputerInfo-Query Computer info from local/Remote Computers-(WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) de PowerShell en la galería de TechNet usa una serie de llamadas a hardware y software, incluido **Win32 \_ adaptador** de comandos, para mostrar información acerca de un sistema local o remoto.</span><span class="sxs-lookup"><span data-stu-id="2209a-611">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_NetworkAdapter**, to display information about a local or remote system.</span></span>

<span data-ttu-id="2209a-612">El siguiente \# ejemplo de código C usa el espacio de nombres [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) para recuperar los adaptadores de red actuales en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="2209a-612">The following C\# code sample uses [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace to retrieve the current network adapters on the local machine.</span></span>


```CSharp
using Microsoft.Management.Infrastructure;
...
static void QueryInstanceFunc()
        {
 
            CimSession session = CimSession.Create("localHost");
            IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_NetworkAdapter");

            foreach (CimInstance cimObj in queryInstance)
            {
                Console.WriteLine(cimObj.CimInstanceProperties["Name"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["Description"].ToString());
                Console.WriteLine();
            }

            Console.ReadLine();
        }
```



<span data-ttu-id="2209a-613">El siguiente \# ejemplo de código C usa el espacio de https://msdn.microsoft.com/library/system.management.aspx nombres para recuperar los adaptadores de red actuales en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="2209a-613">The following C\# code sample uses https://msdn.microsoft.com/library/system.management.aspx namespace to retrieve the current network adapters on the local machine.</span></span>

> [!Note]  
> <span data-ttu-id="2209a-614"> https://msdn.microsoft.com/library/system.management.aspx contiene las clases originales utilizadas para tener acceso a WMI; sin embargo, se consideran más lentos y, por lo general, no se escalan, así como sus homólogos [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2209a-614">https://msdn.microsoft.com/library/system.management.aspx contains the original classes used to access WMI; however, they are considered slower and generally do not scale as well as their [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) counterparts.</span></span>

 


```CSharp
using System.Management;
...
        static void oldSchoolQueryInstanceFunc()
        {

            ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_NetworkAdapter");
            ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);


            ManagementObjectCollection queryCollection = searcher.Get();
            foreach (ManagementObject m in queryCollection)
            {
                Console.WriteLine("ServiceName : {0}", m["Name"]);
                Console.WriteLine("MACAddress : {0}", m["Description"]);
                Console.WriteLine();
            }
            Console.ReadLine();

        }
```



<span data-ttu-id="2209a-615">En el siguiente ejemplo de código de VBScript se describe cómo recuperar los adaptadores de red actuales en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="2209a-615">The following VBScript code sample describes how to retrieve the current network adapters on the local machine.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_NetworkAdapter")

For Each objItem in colItems 
    Wscript.Echo "Name: " & objItem.Name
    Wscript.Echo "Description: " & objItem.Description
    Wscript.Echo
Next
```



## <a name="requirements"></a><span data-ttu-id="2209a-616">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2209a-616">Requirements</span></span>



| <span data-ttu-id="2209a-617">Requisito</span><span class="sxs-lookup"><span data-stu-id="2209a-617">Requirement</span></span> | <span data-ttu-id="2209a-618">Value</span><span class="sxs-lookup"><span data-stu-id="2209a-618">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2209a-619">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2209a-619">Minimum supported client</span></span><br/> | <span data-ttu-id="2209a-620">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2209a-620">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2209a-621">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2209a-621">Minimum supported server</span></span><br/> | <span data-ttu-id="2209a-622">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2209a-622">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2209a-623">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2209a-623">Namespace</span></span><br/>                | <span data-ttu-id="2209a-624">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2209a-624">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2209a-625">MOF</span><span class="sxs-lookup"><span data-stu-id="2209a-625">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2209a-626"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2209a-626"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2209a-627">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2209a-627">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2209a-628"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2209a-628"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2209a-629">Vea también</span><span class="sxs-lookup"><span data-stu-id="2209a-629">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2209a-630">**Adaptador de la CIM \_**</span><span class="sxs-lookup"><span data-stu-id="2209a-630">**CIM\_NetworkAdapter**</span></span>](cim-networkadapter.md)
</dt> <dt>

[<span data-ttu-id="2209a-631">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="2209a-631">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="2209a-632">Tareas de WMI: redes</span><span class="sxs-lookup"><span data-stu-id="2209a-632">WMI Tasks: Networking</span></span>](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[<span data-ttu-id="2209a-633">Compatibilidad con IPv6 e IPv4 en WMI</span><span class="sxs-lookup"><span data-stu-id="2209a-633">IPv6 and IPv4 Support in WMI</span></span>](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
