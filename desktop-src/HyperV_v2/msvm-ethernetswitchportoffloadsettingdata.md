---
description: Representa los datos de configuración de la característica de descarga de puertos.
ms.assetid: 7b8d8bee-86f3-4c55-bb32-987bf840d995
title: Msvm_EthernetSwitchPortOffloadSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortOffloadSettingData
- Msvm_EthernetSwitchPortOffloadSettingData.InstanceID
- Msvm_EthernetSwitchPortOffloadSettingData.Caption
- Msvm_EthernetSwitchPortOffloadSettingData.Description
- Msvm_EthernetSwitchPortOffloadSettingData.ElementName
- Msvm_EthernetSwitchPortOffloadSettingData.IPSecOffloadLimit
- Msvm_EthernetSwitchPortOffloadSettingData.VMQOffloadWeight
- Msvm_EthernetSwitchPortOffloadSettingData.IOVOffloadWeight
- Msvm_EthernetSwitchPortOffloadSettingData.IOVQueuePairsRequested
- Msvm_EthernetSwitchPortOffloadSettingData.IOVInterruptModeration
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectModerationInterval
- Msvm_EthernetSwitchPortOffloadSettingData.VmmqQueuePairs
- Msvm_EthernetSwitchPortOffloadSettingData.VrssVmbusChannelAffinityPolicy
- Msvm_EthernetSwitchPortOffloadSettingData.VrssIndependentHostSpreading
- Msvm_EthernetSwitchPortOffloadSettingData.VrssExcludePrimaryProcessor
- Msvm_EthernetSwitchPortOffloadSettingData.VrssQueueSchedulingMode
- Msvm_EthernetSwitchPortOffloadSettingData.VrssMinQueuePairs
- Msvm_EthernetSwitchPortOffloadSettingData.VmmqEnabled
- Msvm_EthernetSwitchPortOffloadSettingData.VrssEnabled
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectModerationCount
- Msvm_EthernetSwitchPortOffloadSettingData.PacketDirectNumProcs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 150a7b5e54e371c11741dd7c763b0ae145354b09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689581"
---
# <a name="msvm_ethernetswitchportoffloadsettingdata-class"></a><span data-ttu-id="efa33-103">MSVM \_ EthernetSwitchPortOffloadSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="efa33-103">Msvm\_EthernetSwitchPortOffloadSettingData class</span></span>

<span data-ttu-id="efa33-104">Representa los datos de configuración de la característica de descarga de puertos.</span><span class="sxs-lookup"><span data-stu-id="efa33-104">Represents the port offload feature setting data.</span></span>

<span data-ttu-id="efa33-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="efa33-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="efa33-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="efa33-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("C885BFD1-ABB7-418F-8163-9F379C9F7166"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("4"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Offload Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortOffloadSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Offload Settings";
  string  Description = "Represents the port offload feature setting data.";
  string  ElementName = "Ethernet Switch Port Offload Settings";
  uint32  IPSecOffloadLimit = 512;
  uint32  VMQOffloadWeight = 100;
  uint32  IOVOffloadWeight = 0;
  uint32  IOVQueuePairsRequested = 1;
  uint32  IOVInterruptModeration = 0;
  uint32  PacketDirectModerationInterval = 0;
  uint32  VmmqQueuePairs = 16;
  uint32  VrssVmbusChannelAffinityPolicy = 3;
  boolean VrssIndependentHostSpreading = FALSE;
  boolean VrssExcludePrimaryProcessor = FALSE;
  uint32  VrssQueueSchedulingMode = 2;
  uint32  VrssMinQueuePairs = 1;
  boolean VmmqEnabled = FALSE;
  boolean VrssEnabled = TRUE;
  uint32  PacketDirectModerationCount = 0;
  uint32  PacketDirectNumProcs = 1;
};
```

## <a name="members"></a><span data-ttu-id="efa33-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="efa33-107">Members</span></span>

<span data-ttu-id="efa33-108">La clase **MSVM \_ EthernetSwitchPortOffloadSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="efa33-108">The **Msvm\_EthernetSwitchPortOffloadSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="efa33-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="efa33-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="efa33-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="efa33-110">Properties</span></span>

<span data-ttu-id="efa33-111">La clase **MSVM \_ EthernetSwitchPortOffloadSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="efa33-111">The **Msvm\_EthernetSwitchPortOffloadSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="efa33-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="efa33-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efa33-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="efa33-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efa33-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efa33-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efa33-115">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="efa33-115">A short description of the object.</span></span> <span data-ttu-id="efa33-116">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración de descarga de puertos del conmutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="efa33-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Settings".</span></span>

</dd> <dt>

<span data-ttu-id="efa33-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="efa33-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efa33-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="efa33-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efa33-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efa33-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efa33-120">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="efa33-120">A description of the object.</span></span> <span data-ttu-id="efa33-121">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "representa los datos de configuración de la característica de descarga de puertos".</span><span class="sxs-lookup"><span data-stu-id="efa33-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port offload feature setting data.".</span></span>

</dd> <dt>

<span data-ttu-id="efa33-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="efa33-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efa33-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="efa33-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efa33-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efa33-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="efa33-125">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="efa33-125">A display name for the object.</span></span> <span data-ttu-id="efa33-126">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración de descarga de puertos del conmutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="efa33-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Settings".</span></span>

</dd> <dt>

<span data-ttu-id="efa33-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="efa33-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efa33-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="efa33-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="efa33-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="efa33-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="efa33-130">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="efa33-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="efa33-131">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="efa33-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="efa33-132">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="efa33-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="efa33-133">**IOVInterruptModeration**</span><span class="sxs-lookup"><span data-stu-id="efa33-133">**IOVInterruptModeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efa33-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="efa33-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="efa33-135">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="efa33-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="efa33-136">Calificadores: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="efa33-136">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="efa33-137">Valor de moderación de interrupción para la descarga de la virtualización de e/s (IOV).</span><span class="sxs-lookup"><span data-stu-id="efa33-137">The interrupt moderation value for I/O virtualization (IOV) offloading.</span></span> <span data-ttu-id="efa33-138">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="efa33-138">The default is 0.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="efa33-139">**Valor predeterminado** (0)</span><span class="sxs-lookup"><span data-stu-id="efa33-139">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Adaptive"></span><span id="adaptive"></span><span id="ADAPTIVE"></span>

<span data-ttu-id="efa33-140">**Adaptable** (1)</span><span class="sxs-lookup"><span data-stu-id="efa33-140">**Adaptive** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Off"></span><span id="off"></span><span id="OFF"></span>

<span data-ttu-id="efa33-141">**Desactivado** (2)</span><span class="sxs-lookup"><span data-stu-id="efa33-141">**Off** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span data-ttu-id="efa33-142">**Bajo** (100)</span><span class="sxs-lookup"><span data-stu-id="efa33-142">**Low** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span data-ttu-id="efa33-143">**Medio** (200)</span><span class="sxs-lookup"><span data-stu-id="efa33-143">**Medium** (200)</span></span>


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span data-ttu-id="efa33-144">**Alto** (300)</span><span class="sxs-lookup"><span data-stu-id="efa33-144">**High** (300)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="efa33-145">**IOVOffloadWeight**</span><span class="sxs-lookup"><span data-stu-id="efa33-145">**IOVOffloadWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efa33-146">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="efa33-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="efa33-147">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="efa33-147">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="efa33-148">Calificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="efa33-148">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="efa33-149">El peso asignado a este puerto para la descarga de la virtualización de e/s (IOV).</span><span class="sxs-lookup"><span data-stu-id="efa33-149">The weight assigned to this port for I/O virtualization (IOV) offloading.</span></span> <span data-ttu-id="efa33-150">El peso es la importancia relativa al asignar recursos IOV.</span><span class="sxs-lookup"><span data-stu-id="efa33-150">The weight is the relative importance when assigning IOV resources.</span></span> <span data-ttu-id="efa33-151">Si se establece la propiedad **IOVOffloadWeight** en 0, se deshabilita la descarga de IOV en el puerto.</span><span class="sxs-lookup"><span data-stu-id="efa33-151">Setting the **IOVOffloadWeight** property to 0 disables IOV offloading on the port.</span></span> <span data-ttu-id="efa33-152">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="efa33-152">The default is 0.</span></span>

</dd> <dt>

<span data-ttu-id="efa33-153">**IOVQueuePairsRequested**</span><span class="sxs-lookup"><span data-stu-id="efa33-153">**IOVQueuePairsRequested**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efa33-154">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="efa33-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="efa33-155">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="efa33-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="efa33-156">Calificadores: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="efa33-156">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="efa33-157">El número de pares de cola solicitados para este puerto para la descarga de la virtualización de e/s (IOV).</span><span class="sxs-lookup"><span data-stu-id="efa33-157">The number of queue pairs requested for this port for I/O virtualization (IOV) offloading.</span></span> <span data-ttu-id="efa33-158">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="efa33-158">The default is 1.</span></span>

</dd> <dt>

<span data-ttu-id="efa33-159">**IPSecOffloadLimit**</span><span class="sxs-lookup"><span data-stu-id="efa33-159">**IPSecOffloadLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efa33-160">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="efa33-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="efa33-161">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="efa33-161">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="efa33-162">Calificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="efa33-162">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="efa33-163">El número máximo de ranuras de descarga de la Asociación de seguridad (SA) permitidas desde el puerto.</span><span class="sxs-lookup"><span data-stu-id="efa33-163">The maximum number of security association (SA) offload slots allowed from the port.</span></span>

</dd> <dt>

<span data-ttu-id="efa33-164">**PacketDirectModerationCount**</span><span class="sxs-lookup"><span data-stu-id="efa33-164">**PacketDirectModerationCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efa33-165">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="efa33-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="efa33-166">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="efa33-166">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="efa33-167">Calificadores: **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="efa33-167">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="efa33-168">El valor de recuento de moderación de interrupciones para Packet Direct (PD). El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="efa33-168">The interrupt moderation count value for Packet Direct (PD).The default is 0.</span></span>

> [!Note]  
> <span data-ttu-id="efa33-169">Propiedad agregada en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="efa33-169">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="efa33-170">**PacketDirectModerationInterval**</span><span class="sxs-lookup"><span data-stu-id="efa33-170">**PacketDirectModerationInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efa33-171">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="efa33-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="efa33-172">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="efa33-172">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="efa33-173">Calificadores: **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="efa33-173">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="efa33-174">El valor de intervalo de moderación de interrupciones para Packet Direct (PD). El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="efa33-174">The interrupt moderation interval value for Packet Direct (PD).The default is 0.</span></span>

> [!Note]  
> <span data-ttu-id="efa33-175">Propiedad agregada en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="efa33-175">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="efa33-176">**PacketDirectNumProcs**</span><span class="sxs-lookup"><span data-stu-id="efa33-176">**PacketDirectNumProcs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efa33-177">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="efa33-177">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="efa33-178">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="efa33-178">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="efa33-179">Calificadores: **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="efa33-179">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="efa33-180">El número de procesadores utilizados por el host para procesar paquetes enviados desde este puerto en modo de paquete directo.</span><span class="sxs-lookup"><span data-stu-id="efa33-180">The number of processors used by the host for processing packets sent from this port in Packet Direct mode.</span></span> <span data-ttu-id="efa33-181">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="efa33-181">The default is 1.</span></span>

> [!Note]  
> <span data-ttu-id="efa33-182">Propiedad agregada en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="efa33-182">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="efa33-183">**VmmqEnabled**</span><span class="sxs-lookup"><span data-stu-id="efa33-183">**VmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efa33-184">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="efa33-184">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="efa33-185">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="efa33-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="efa33-186">Calificadores: **WmiDataId** (10), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="efa33-186">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="efa33-187">Habilite la descarga de VMMQ si es compatible con el hardware. El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="efa33-187">Enable VMMQ offload if supported by hardware.The default is False.</span></span>

> [!Note]  
> <span data-ttu-id="efa33-188">Esta propiedad se agregó en Windows 10, versión 1703 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="efa33-188">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="efa33-189">**VmmqQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="efa33-189">**VmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efa33-190">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="efa33-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="efa33-191">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="efa33-191">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="efa33-192">Calificadores: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="efa33-192">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="efa33-193">El número de colas que se asignan cuando se habilita VRSS.</span><span class="sxs-lookup"><span data-stu-id="efa33-193">The number of queues to allocate when VRSS is enabled.</span></span> <span data-ttu-id="efa33-194">El valor predeterminado es 16.</span><span class="sxs-lookup"><span data-stu-id="efa33-194">The default is 16.</span></span>

> [!Note]  
> <span data-ttu-id="efa33-195">Esta propiedad se agregó en Windows 10, versión 1703 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="efa33-195">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="efa33-196">**VMQOffloadWeight**</span><span class="sxs-lookup"><span data-stu-id="efa33-196">**VMQOffloadWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efa33-197">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="efa33-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="efa33-198">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="efa33-198">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="efa33-199">Calificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="efa33-199">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="efa33-200">El peso asignado a este puerto para la descarga de Virtual Machine Queue (VMQ).</span><span class="sxs-lookup"><span data-stu-id="efa33-200">The weight assigned to this port for virtual machine queue (VMQ) offloading.</span></span> <span data-ttu-id="efa33-201">El peso es la importancia relativa al asignar recursos VMQ.</span><span class="sxs-lookup"><span data-stu-id="efa33-201">The weight is the relative importance when assigning VMQ resources.</span></span> <span data-ttu-id="efa33-202">Al establecer la propiedad **VMQOffloadWeight** en 0, se deshabilita VMQ en el puerto.</span><span class="sxs-lookup"><span data-stu-id="efa33-202">Setting the **VMQOffloadWeight** property to 0 disables VMQ on the port.</span></span> <span data-ttu-id="efa33-203">El valor predeterminado es 100.</span><span class="sxs-lookup"><span data-stu-id="efa33-203">The default is 100.</span></span>

</dd> <dt>

<span data-ttu-id="efa33-204">**VrssEnabled**</span><span class="sxs-lookup"><span data-stu-id="efa33-204">**VrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efa33-205">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="efa33-205">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="efa33-206">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="efa33-206">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="efa33-207">Calificadores: **WmiDataId** (9), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="efa33-207">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="efa33-208">Habilite VRSS.</span><span class="sxs-lookup"><span data-stu-id="efa33-208">Enable VRSS.</span></span> <span data-ttu-id="efa33-209">El valor predeterminado es true.</span><span class="sxs-lookup"><span data-stu-id="efa33-209">The default is true.</span></span>

> [!Note]  
> <span data-ttu-id="efa33-210">Esta propiedad se agregó en Windows 10, versión 1703 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="efa33-210">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="efa33-211">**VrssExcludePrimaryProcessor**</span><span class="sxs-lookup"><span data-stu-id="efa33-211">**VrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efa33-212">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="efa33-212">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="efa33-213">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="efa33-213">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="efa33-214">Calificadores: **WmiDataId** (14), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="efa33-214">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="efa33-215">Si se debe excluir el procesador VMQ principal de la tabla de indirección de VRSS cuando se habilita VRSS. El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="efa33-215">Whether to exclude primary VMQ processor from the VRSS indirection table when VRSS is enabled.The default is false.</span></span>

> [!Note]  
> <span data-ttu-id="efa33-216">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="efa33-216">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="efa33-217">**VrssIndependentHostSpreading**</span><span class="sxs-lookup"><span data-stu-id="efa33-217">**VrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efa33-218">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="efa33-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="efa33-219">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="efa33-219">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="efa33-220">Calificadores: **WmiDataId** (15), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="efa33-220">Qualifiers: **WmiDataId** (15), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="efa33-221">Indica si se va a realizar siempre el VRSS del host cuando se habilita VRSS, independientemente de la configuración de RSS de la NIC virtual. El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="efa33-221">Whether to always do host-side VRSS when VRSS is enabled, regardless of RSS setting of the virtual NIC.The default is false.</span></span>

> [!Note]  
> <span data-ttu-id="efa33-222">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="efa33-222">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="efa33-223">**VrssMinQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="efa33-223">**VrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efa33-224">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="efa33-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="efa33-225">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="efa33-225">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="efa33-226">Calificadores: **WmiDataId** (12), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="efa33-226">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="efa33-227">El número mínimo de colas que se asignan cuando VRSS está habilitado. El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="efa33-227">The minimum number of queues to allocate when VRSS is enabled.The default is 1.</span></span>

> [!Note]  
> <span data-ttu-id="efa33-228">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="efa33-228">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="efa33-229">**VrssQueueSchedulingMode**</span><span class="sxs-lookup"><span data-stu-id="efa33-229">**VrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efa33-230">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="efa33-230">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="efa33-231">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="efa33-231">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="efa33-232">Calificadores: **WmiDataId** (13), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="efa33-232">Qualifiers: **WmiDataId** (13), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="efa33-233">Modo de programación de la cola que se va a usar cuando se habilita VRSS. El valor predeterminado es la programación estática.</span><span class="sxs-lookup"><span data-stu-id="efa33-233">The queue scheduling mode to use when VRSS is enabled.The default is static scheduling.</span></span>

> [!Note]  
> <span data-ttu-id="efa33-234">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="efa33-234">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="efa33-235">**VrssVmbusChannelAffinityPolicy**</span><span class="sxs-lookup"><span data-stu-id="efa33-235">**VrssVmbusChannelAffinityPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efa33-236">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="efa33-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="efa33-237">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="efa33-237">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="efa33-238">Calificadores: **WmiDataId** (16), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="efa33-238">Qualifiers: **WmiDataId** (16), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="efa33-239">La Directiva de afinidad del canal de Vmbus que se va a usar cuando se habilita VRSS. El valor predeterminado es strong.</span><span class="sxs-lookup"><span data-stu-id="efa33-239">The vmbus channel affinity policy to use when VRSS is enabled.The default is strong.</span></span>

> [!Note]  
> <span data-ttu-id="efa33-240">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="efa33-240">Added in Windows 10, version 1709.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="efa33-241">Requisitos</span><span class="sxs-lookup"><span data-stu-id="efa33-241">Requirements</span></span>



| <span data-ttu-id="efa33-242">Requisito</span><span class="sxs-lookup"><span data-stu-id="efa33-242">Requirement</span></span> | <span data-ttu-id="efa33-243">Value</span><span class="sxs-lookup"><span data-stu-id="efa33-243">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efa33-244">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="efa33-244">Minimum supported client</span></span><br/> | <span data-ttu-id="efa33-245">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="efa33-245">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="efa33-246">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="efa33-246">Minimum supported server</span></span><br/> | <span data-ttu-id="efa33-247">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="efa33-247">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="efa33-248">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="efa33-248">Namespace</span></span><br/>                | <span data-ttu-id="efa33-249">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="efa33-249">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="efa33-250">MOF</span><span class="sxs-lookup"><span data-stu-id="efa33-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="efa33-251"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="efa33-251"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="efa33-252">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="efa33-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="efa33-253"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="efa33-253"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

