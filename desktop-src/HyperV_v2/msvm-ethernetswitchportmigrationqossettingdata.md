---
description: Representa la configuración de QOS de VFP.
ms.assetid: e58a7a8d-0301-43ea-9338-18bc8c458e2d
title: Msvm_EthernetSwitchPortMigrationQosSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortMigrationQosSettingData
- Msvm_EthernetSwitchPortMigrationQosSettingData.QueueId
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_ReservationMode
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_LinkSpeedPercentage
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_DefaultReservation
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableHardwareLimits
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableHardwareReservations
- Msvm_EthernetSwitchPortMigrationQosSettingData.Switch_EnableSoftwareReservations
- Msvm_EthernetSwitchPortMigrationQosSettingData.OutboundReservedValue
- Msvm_EthernetSwitchPortMigrationQosSettingData.OutboundMaximumMbps
- Msvm_EthernetSwitchPortMigrationQosSettingData.InboundMaximumMbps
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e279b24178c33c760477995ff744a0699cea1aaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687781"
---
# <a name="msvm_ethernetswitchportmigrationqossettingdata-class"></a><span data-ttu-id="5d5be-103">MSVM \_ EthernetSwitchPortMigrationQosSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="5d5be-103">Msvm\_EthernetSwitchPortMigrationQosSettingData class</span></span>

<span data-ttu-id="5d5be-104">Representa la configuración de QOS de VFP.</span><span class="sxs-lookup"><span data-stu-id="5d5be-104">Represents the VFP QOS settings.</span></span>

<span data-ttu-id="5d5be-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5d5be-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d5be-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d5be-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("FD2A5DE3-DC6C-4320-82A5-234D3AF55297"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("E9B59CFA-2BE1-4B21-828F-B6FBDBDDC017"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port VFP QOS Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortMigrationQosSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  QueueId = "";
  uint8   Switch_ReservationMode = 0;
  uint8   Switch_LinkSpeedPercentage = 0;
  uint64  Switch_DefaultReservation = 0;
  boolean Switch_EnableHardwareLimits = FALSE;
  boolean Switch_EnableHardwareReservations = FALSE;
  boolean Switch_EnableSoftwareReservations = TRUE;
  uint64  OutboundReservedValue = 0;
  uint64  OutboundMaximumMbps = 0;
  uint64  InboundMaximumMbps = 0;
};
```

## <a name="members"></a><span data-ttu-id="5d5be-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="5d5be-107">Members</span></span>

<span data-ttu-id="5d5be-108">La clase **MSVM \_ EthernetSwitchPortMigrationQosSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5d5be-108">The **Msvm\_EthernetSwitchPortMigrationQosSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="5d5be-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5d5be-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5d5be-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5d5be-110">Properties</span></span>

<span data-ttu-id="5d5be-111">La clase **MSVM \_ EthernetSwitchPortMigrationQosSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5d5be-111">The **Msvm\_EthernetSwitchPortMigrationQosSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5d5be-112">**InboundMaximumMbps**</span><span class="sxs-lookup"><span data-stu-id="5d5be-112">**InboundMaximumMbps**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d5be-113">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5d5be-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5d5be-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5d5be-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5d5be-115">Calificadores: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="5d5be-115">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5d5be-116">Valor de límite de ancho de banda para el tráfico entrante.</span><span class="sxs-lookup"><span data-stu-id="5d5be-116">The bandwidth cap value for inbound traffic.</span></span>

</dd> <dt>

<span data-ttu-id="5d5be-117">**OutboundMaximumMbps**</span><span class="sxs-lookup"><span data-stu-id="5d5be-117">**OutboundMaximumMbps**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d5be-118">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5d5be-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5d5be-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5d5be-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5d5be-120">Calificadores: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="5d5be-120">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5d5be-121">El valor de límite de ancho de banda para el tráfico de salida.</span><span class="sxs-lookup"><span data-stu-id="5d5be-121">The bandwidth cap value for outbound traffic.</span></span>

</dd> <dt>

<span data-ttu-id="5d5be-122">**OutboundReservedValue**</span><span class="sxs-lookup"><span data-stu-id="5d5be-122">**OutboundReservedValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d5be-123">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5d5be-123">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5d5be-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5d5be-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5d5be-125">Calificadores: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="5d5be-125">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5d5be-126">Valor de reserva de ancho de banda.</span><span class="sxs-lookup"><span data-stu-id="5d5be-126">The bandwidth reservation value.</span></span>

</dd> <dt>

<span data-ttu-id="5d5be-127">**QueueId**</span><span class="sxs-lookup"><span data-stu-id="5d5be-127">**QueueId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d5be-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5d5be-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d5be-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5d5be-129">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5d5be-130">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="5d5be-130">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5d5be-131">IDENTIFICADOR de la cola de QOS.</span><span class="sxs-lookup"><span data-stu-id="5d5be-131">The ID of the QOS queue.</span></span>

</dd> <dt>

<span data-ttu-id="5d5be-132">**Cambiar \_ DefaultReservation**</span><span class="sxs-lookup"><span data-stu-id="5d5be-132">**Switch\_DefaultReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d5be-133">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5d5be-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5d5be-134">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5d5be-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5d5be-135">Calificadores: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="5d5be-135">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5d5be-136">Valor de reserva predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5d5be-136">The default reservation value.</span></span>

</dd> <dt>

<span data-ttu-id="5d5be-137">**Cambiar \_ EnableHardwareLimits**</span><span class="sxs-lookup"><span data-stu-id="5d5be-137">**Switch\_EnableHardwareLimits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d5be-138">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5d5be-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d5be-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5d5be-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5d5be-140">Calificadores: **WmiDataId** (5), [**versión**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**revisión**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="5d5be-140">Qualifiers: **WmiDataId** (5), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="5d5be-141">Indica si se intentan las descargas de hardware para los límites si están disponibles.</span><span class="sxs-lookup"><span data-stu-id="5d5be-141">Indicates whether hardware offloads for limits are attempted if available.</span></span>

</dd> <dt>

<span data-ttu-id="5d5be-142">**Cambiar \_ EnableHardwareReservations**</span><span class="sxs-lookup"><span data-stu-id="5d5be-142">**Switch\_EnableHardwareReservations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d5be-143">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5d5be-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d5be-144">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5d5be-144">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5d5be-145">Calificadores: **WmiDataId** (6), [**versión**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**revisión**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="5d5be-145">Qualifiers: **WmiDataId** (6), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="5d5be-146">Indica si se intentan las descargas de hardware para las reservas si están disponibles.</span><span class="sxs-lookup"><span data-stu-id="5d5be-146">Indicates whether hardware offloads for reservations are attempted if available.</span></span>

</dd> <dt>

<span data-ttu-id="5d5be-147">**Cambiar \_ EnableSoftwareReservations**</span><span class="sxs-lookup"><span data-stu-id="5d5be-147">**Switch\_EnableSoftwareReservations**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d5be-148">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5d5be-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5d5be-149">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5d5be-149">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5d5be-150">Calificadores: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="5d5be-150">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5d5be-151">Indica si la reserva basada en software está disponible.</span><span class="sxs-lookup"><span data-stu-id="5d5be-151">Indicates whether software based reservation is available.</span></span>

</dd> <dt>

<span data-ttu-id="5d5be-152">**Cambiar \_ LinkSpeedPercentage**</span><span class="sxs-lookup"><span data-stu-id="5d5be-152">**Switch\_LinkSpeedPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d5be-153">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="5d5be-153">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="5d5be-154">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5d5be-154">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5d5be-155">Calificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="5d5be-155">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5d5be-156">Porcentaje de velocidad del vínculo que se va a utilizar para la reserva.</span><span class="sxs-lookup"><span data-stu-id="5d5be-156">The link speed percentage to be used for reservation.</span></span>

</dd> <dt>

<span data-ttu-id="5d5be-157">**Cambiar \_ ReservationMode**</span><span class="sxs-lookup"><span data-stu-id="5d5be-157">**Switch\_ReservationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d5be-158">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="5d5be-158">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="5d5be-159">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5d5be-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5d5be-160">Calificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="5d5be-160">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5d5be-161">Modo de reserva de QOS en el conmutador.</span><span class="sxs-lookup"><span data-stu-id="5d5be-161">The QOS reservation mode on the switch.</span></span>

<dt>

<span id="Absolute"></span><span id="absolute"></span><span id="ABSOLUTE"></span>

<span data-ttu-id="5d5be-162">**Absolute** (0)</span><span class="sxs-lookup"><span data-stu-id="5d5be-162">**Absolute** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Weight"></span><span id="weight"></span><span id="WEIGHT"></span>

<span data-ttu-id="5d5be-163">**Peso** (1)</span><span class="sxs-lookup"><span data-stu-id="5d5be-163">**Weight** (1)</span></span>


<span data-ttu-id="5d5be-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5d5be-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="5d5be-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d5be-165">Requirements</span></span>



| <span data-ttu-id="5d5be-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d5be-166">Requirement</span></span> | <span data-ttu-id="5d5be-167">Value</span><span class="sxs-lookup"><span data-stu-id="5d5be-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d5be-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d5be-168">Minimum supported client</span></span><br/> | <span data-ttu-id="5d5be-169">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="5d5be-169">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5d5be-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d5be-170">Minimum supported server</span></span><br/> | <span data-ttu-id="5d5be-171">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5d5be-171">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="5d5be-172">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5d5be-172">Namespace</span></span><br/>                | <span data-ttu-id="5d5be-173">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="5d5be-173">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5d5be-174">MOF</span><span class="sxs-lookup"><span data-stu-id="5d5be-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d5be-175"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d5be-175"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d5be-176">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5d5be-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d5be-177"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5d5be-177"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5d5be-178">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d5be-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d5be-179">**MSVM \_ EthernetSwitchPortFeatureSettingData**</span><span class="sxs-lookup"><span data-stu-id="5d5be-179">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

