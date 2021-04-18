---
description: Representa la configuración de ancho de banda del puerto.
ms.assetid: 62a42c4c-8ea1-47c6-8ae6-e9252f2ed0e4
title: Msvm_EthernetSwitchPortBandwidthSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortBandwidthSettingData
- Msvm_EthernetSwitchPortBandwidthSettingData.InstanceID
- Msvm_EthernetSwitchPortBandwidthSettingData.Caption
- Msvm_EthernetSwitchPortBandwidthSettingData.Description
- Msvm_EthernetSwitchPortBandwidthSettingData.ElementName
- Msvm_EthernetSwitchPortBandwidthSettingData.Reservation
- Msvm_EthernetSwitchPortBandwidthSettingData.Weight
- Msvm_EthernetSwitchPortBandwidthSettingData.Limit
- Msvm_EthernetSwitchPortBandwidthSettingData.BurstLimit
- Msvm_EthernetSwitchPortBandwidthSettingData.BurstSize
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 932207a8157e34c5f42894c31efa78090a6a80f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688359"
---
# <a name="msvm_ethernetswitchportbandwidthsettingdata-class"></a><span data-ttu-id="4d4b7-103">MSVM \_ EthernetSwitchPortBandwidthSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="4d4b7-103">Msvm\_EthernetSwitchPortBandwidthSettingData class</span></span>

<span data-ttu-id="4d4b7-104">Representa la configuración de ancho de banda del puerto.</span><span class="sxs-lookup"><span data-stu-id="4d4b7-104">Represents the port bandwidth settings.</span></span>

<span data-ttu-id="4d4b7-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="4d4b7-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d4b7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d4b7-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("24AD3CE1-69BD-4978-B2AC-DAAD389D699C"), Provider("VmmsWmiInstanceAndMethodProvider"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Bandwidth Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortBandwidthSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Bandwidth Settings";
  string Description = "Represents the port bandwidth settings.";
  string ElementName = "Ethernet Switch Port Bandwidth Settings";
  uint64 Reservation = 0;
  uint64 Weight = 0;
  uint64 Limit = 0;
  uint64 BurstLimit = 0;
  uint64 BurstSize = 0;
};
```

## <a name="members"></a><span data-ttu-id="4d4b7-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4d4b7-107">Members</span></span>

<span data-ttu-id="4d4b7-108">La clase **MSVM \_ EthernetSwitchPortBandwidthSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4d4b7-108">The **Msvm\_EthernetSwitchPortBandwidthSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="4d4b7-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4d4b7-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4d4b7-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4d4b7-110">Properties</span></span>

<span data-ttu-id="4d4b7-111">La clase **MSVM \_ EthernetSwitchPortBandwidthSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4d4b7-111">The **Msvm\_EthernetSwitchPortBandwidthSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4d4b7-112">**BurstLimit**</span><span class="sxs-lookup"><span data-stu-id="4d4b7-112">**BurstLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d4b7-113">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4d4b7-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4d4b7-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4d4b7-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4d4b7-115">Calificadores: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4d4b7-115">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4d4b7-116">El ancho de banda máximo permitido desde el puerto durante las ráfagas.</span><span class="sxs-lookup"><span data-stu-id="4d4b7-116">The peak bandwidth allowed from the port during bursts.</span></span>

</dd> <dt>

<span data-ttu-id="4d4b7-117">**BurstSize**</span><span class="sxs-lookup"><span data-stu-id="4d4b7-117">**BurstSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d4b7-118">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4d4b7-118">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4d4b7-119">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4d4b7-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4d4b7-120">Calificadores: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4d4b7-120">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4d4b7-121">Tamaño de ráfaga máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="4d4b7-121">The maximum burst size allowed.</span></span>

</dd> <dt>

<span data-ttu-id="4d4b7-122">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4d4b7-122">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d4b7-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4d4b7-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d4b7-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d4b7-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d4b7-125">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="4d4b7-125">A short description of the object.</span></span> <span data-ttu-id="4d4b7-126">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración de ancho de banda del puerto del conmutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="4d4b7-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="4d4b7-127">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4d4b7-127">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d4b7-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4d4b7-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d4b7-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d4b7-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d4b7-130">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="4d4b7-130">A description of the object.</span></span> <span data-ttu-id="4d4b7-131">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "representa la configuración de ancho de banda del puerto".</span><span class="sxs-lookup"><span data-stu-id="4d4b7-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port bandwidth settings.".</span></span>

</dd> <dt>

<span data-ttu-id="4d4b7-132">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4d4b7-132">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d4b7-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4d4b7-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d4b7-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d4b7-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4d4b7-135">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="4d4b7-135">A display name for the object.</span></span> <span data-ttu-id="4d4b7-136">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración de ancho de banda del puerto del conmutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="4d4b7-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Settings".</span></span>

</dd> <dt>

<span data-ttu-id="4d4b7-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4d4b7-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d4b7-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4d4b7-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d4b7-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d4b7-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d4b7-140">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="4d4b7-140">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4d4b7-141">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="4d4b7-141">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="4d4b7-142">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4d4b7-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4d4b7-143">**Límite**</span><span class="sxs-lookup"><span data-stu-id="4d4b7-143">**Limit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d4b7-144">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4d4b7-144">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4d4b7-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4d4b7-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4d4b7-146">Calificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4d4b7-146">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4d4b7-147">Límite de ancho de banda permitido para el puerto.</span><span class="sxs-lookup"><span data-stu-id="4d4b7-147">The bandwidth limit allowed for the port.</span></span>

</dd> <dt>

<span data-ttu-id="4d4b7-148">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="4d4b7-148">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d4b7-149">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4d4b7-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4d4b7-150">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4d4b7-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4d4b7-151">Calificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4d4b7-151">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4d4b7-152">El ancho de banda absoluto mínimo garantizado para el puerto.</span><span class="sxs-lookup"><span data-stu-id="4d4b7-152">The minimum absolute bandwidth guaranteed for the port.</span></span>

</dd> <dt>

<span data-ttu-id="4d4b7-153">**Peso**</span><span class="sxs-lookup"><span data-stu-id="4d4b7-153">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d4b7-154">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="4d4b7-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="4d4b7-155">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4d4b7-155">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4d4b7-156">Calificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4d4b7-156">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4d4b7-157">Ancho de banda mínimo en el peso garantizado para el puerto.</span><span class="sxs-lookup"><span data-stu-id="4d4b7-157">The minimum bandwidth in weight guaranteed for the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4d4b7-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d4b7-158">Requirements</span></span>



| <span data-ttu-id="4d4b7-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d4b7-159">Requirement</span></span> | <span data-ttu-id="4d4b7-160">Value</span><span class="sxs-lookup"><span data-stu-id="4d4b7-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d4b7-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d4b7-161">Minimum supported client</span></span><br/> | <span data-ttu-id="4d4b7-162">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="4d4b7-162">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4d4b7-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d4b7-163">Minimum supported server</span></span><br/> | <span data-ttu-id="4d4b7-164">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="4d4b7-164">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4d4b7-165">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4d4b7-165">Namespace</span></span><br/>                | <span data-ttu-id="4d4b7-166">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="4d4b7-166">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4d4b7-167">MOF</span><span class="sxs-lookup"><span data-stu-id="4d4b7-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d4b7-168"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d4b7-168"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d4b7-169">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4d4b7-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d4b7-170"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4d4b7-170"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

