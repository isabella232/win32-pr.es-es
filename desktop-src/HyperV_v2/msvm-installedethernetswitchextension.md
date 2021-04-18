---
description: Representa una instancia de un componente de extensión instalado en un sistema host.
ms.assetid: ad24fb08-36af-42a8-a910-63eae54fa5b8
title: Msvm_InstalledEthernetSwitchExtension (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InstalledEthernetSwitchExtension
- Msvm_InstalledEthernetSwitchExtension.InstanceID
- Msvm_InstalledEthernetSwitchExtension.Caption
- Msvm_InstalledEthernetSwitchExtension.Description
- Msvm_InstalledEthernetSwitchExtension.ElementName
- Msvm_InstalledEthernetSwitchExtension.InstallDate
- Msvm_InstalledEthernetSwitchExtension.Name
- Msvm_InstalledEthernetSwitchExtension.OperationalStatus
- Msvm_InstalledEthernetSwitchExtension.StatusDescriptions
- Msvm_InstalledEthernetSwitchExtension.Status
- Msvm_InstalledEthernetSwitchExtension.HealthState
- Msvm_InstalledEthernetSwitchExtension.CommunicationStatus
- Msvm_InstalledEthernetSwitchExtension.DetailedStatus
- Msvm_InstalledEthernetSwitchExtension.OperatingStatus
- Msvm_InstalledEthernetSwitchExtension.PrimaryStatus
- Msvm_InstalledEthernetSwitchExtension.ExtensionType
- Msvm_InstalledEthernetSwitchExtension.Vendor
- Msvm_InstalledEthernetSwitchExtension.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bfbe0b1996751613c31913447cb0d200d71b8168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666607"
---
# <a name="msvm_installedethernetswitchextension-class"></a><span data-ttu-id="a6b0f-103">MSVM \_ InstalledEthernetSwitchExtension (clase)</span><span class="sxs-lookup"><span data-stu-id="a6b0f-103">Msvm\_InstalledEthernetSwitchExtension class</span></span>

<span data-ttu-id="a6b0f-104">Representa una instancia de un componente de extensión instalado en un sistema host.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-104">Represents an instance of an extension component installed on a host system.</span></span>

<span data-ttu-id="a6b0f-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6b0f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a6b0f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InstalledEthernetSwitchExtension : CIM_ManagedSystemElement
{
  string   InstanceID;
  string   Caption = " System Virtual Ethernet Switch Extension";
  string   Description = "Microsoft NDIS Packet Capture Filter Driver";
  string   ElementName = "Microsoft NDIS Capture";
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = 2;
  string   StatusDescriptions[] = "OK";
  string   Status = "OK";
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint8    ExtensionType;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="a6b0f-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="a6b0f-107">Members</span></span>

<span data-ttu-id="a6b0f-108">La clase **MSVM \_ InstalledEthernetSwitchExtension** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a6b0f-108">The **Msvm\_InstalledEthernetSwitchExtension** class has these types of members:</span></span>

-   [<span data-ttu-id="a6b0f-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a6b0f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a6b0f-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a6b0f-110">Properties</span></span>

<span data-ttu-id="a6b0f-111">La clase **MSVM \_ InstalledEthernetSwitchExtension** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-111">The **Msvm\_InstalledEthernetSwitchExtension** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a6b0f-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b0f-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6b0f-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-115">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="a6b0f-115">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="a6b0f-116">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-116">A short description of the object.</span></span> <span data-ttu-id="a6b0f-117">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a6b0f-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a6b0f-118">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-118">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b0f-119">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6b0f-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6b0f-121">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-121">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="a6b0f-122">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-122">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a6b0f-123">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a6b0f-123">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a6b0f-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b0f-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6b0f-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6b0f-127">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-127">A description of the object.</span></span> <span data-ttu-id="a6b0f-128">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a6b0f-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a6b0f-129">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-129">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b0f-130">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6b0f-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6b0f-132">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-132">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="a6b0f-133">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-133">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a6b0f-134">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a6b0f-134">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a6b0f-135">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-135">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b0f-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6b0f-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6b0f-138">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-138">A display name for the object.</span></span> <span data-ttu-id="a6b0f-139">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a6b0f-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a6b0f-140">**ExtensionType**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-140">**ExtensionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b0f-141">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-141">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6b0f-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6b0f-143">Indica el tipo del componente de extensión.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-143">Indicates the type of the extension component.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a6b0f-144">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="a6b0f-144">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Capture"></span><span id="capture"></span><span id="CAPTURE"></span>

<span data-ttu-id="a6b0f-145">**Capturar** (1)</span><span class="sxs-lookup"><span data-stu-id="a6b0f-145">**Capture** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Filter"></span><span id="filter"></span><span id="FILTER"></span>

<span data-ttu-id="a6b0f-146">**Filtrar** (2)</span><span class="sxs-lookup"><span data-stu-id="a6b0f-146">**Filter** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Forwarding"></span><span id="forwarding"></span><span id="FORWARDING"></span>

<span data-ttu-id="a6b0f-147">**Reenvío** (3)</span><span class="sxs-lookup"><span data-stu-id="a6b0f-147">**Forwarding** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Monitoring"></span><span id="monitoring"></span><span id="MONITORING"></span>

<span data-ttu-id="a6b0f-148">**Supervisión** (4)</span><span class="sxs-lookup"><span data-stu-id="a6b0f-148">**Monitoring** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Native"></span><span id="native"></span><span id="NATIVE"></span>

<span data-ttu-id="a6b0f-149">**Nativo** (5)</span><span class="sxs-lookup"><span data-stu-id="a6b0f-149">**Native** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a6b0f-150">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-150">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b0f-151">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6b0f-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6b0f-153">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-153">The current health of the element.</span></span> <span data-ttu-id="a6b0f-154">Este atributo expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-154">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="a6b0f-155">Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-155">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="a6b0f-156">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5 (Aceptar).</span><span class="sxs-lookup"><span data-stu-id="a6b0f-156">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="a6b0f-157">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-157">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b0f-158">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-158">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-159">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6b0f-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6b0f-160">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-160">The date and time when the object was installed.</span></span> <span data-ttu-id="a6b0f-161">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-161">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="a6b0f-162">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a6b0f-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a6b0f-163">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-163">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b0f-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6b0f-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-166">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-166">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a6b0f-167">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-167">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a6b0f-168">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a6b0f-168">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a6b0f-169">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-169">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b0f-170">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6b0f-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-172">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a6b0f-172">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a6b0f-173">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-173">The label by which the object is known.</span></span> <span data-ttu-id="a6b0f-174">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a6b0f-174">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a6b0f-175">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-175">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b0f-176">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-176">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6b0f-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6b0f-178">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="a6b0f-178">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="a6b0f-179">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-179">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a6b0f-180">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a6b0f-180">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a6b0f-181">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-181">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b0f-182">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-182">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6b0f-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6b0f-184">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-184">The current statuses of the object.</span></span> <span data-ttu-id="a6b0f-185">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en 2 (correcto).</span><span class="sxs-lookup"><span data-stu-id="a6b0f-185">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="a6b0f-186">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-186">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b0f-187">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6b0f-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6b0f-189">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-189">Provides high level status information.</span></span> <span data-ttu-id="a6b0f-190">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar información de estado de mantenimiento detallada y de alto nivel para el elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-190">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="a6b0f-191">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-191">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="a6b0f-192">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a6b0f-192">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="a6b0f-193">**Estado**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-193">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b0f-194">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-195">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6b0f-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6b0f-196">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-196">The current status of the object.</span></span> <span data-ttu-id="a6b0f-197">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="a6b0f-197">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="a6b0f-198">ACEPTAR</span><span class="sxs-lookup"><span data-stu-id="a6b0f-198">"OK"</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-199"><span id="OK"></span><span id="ok"></span>**Vale**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-199"><span id="OK"></span><span id="ok"></span>**OK**</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-200"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-200"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error**</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-201"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-201"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded**</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-202"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown**</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-203"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Pred error**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-203"><span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>**Pred Fail**</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-204"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Comenzar**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-204"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting**</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-205"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Bloqueo**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-205"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping**</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-206"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Servicio**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-206"><span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service**</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-207"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Calca**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-207"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed**</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-208"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**No recuperable**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-208"><span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>**NonRecover**</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-209"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-209"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact**</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-210"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Comunicación perdida**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-210"><span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>**Lost Comm**</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a6b0f-211">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-211">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b0f-212">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-212">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6b0f-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6b0f-214">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="a6b0f-214">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="a6b0f-215">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en "OK".</span><span class="sxs-lookup"><span data-stu-id="a6b0f-215">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "OK".</span></span>

</dd> <dt>

<span data-ttu-id="a6b0f-216">**Proveedor**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-216">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b0f-217">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-218">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6b0f-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6b0f-219">Indica que el proveedor proporciona la extensión.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-219">Indicates the vendor providing the extension.</span></span>

</dd> <dt>

<span data-ttu-id="a6b0f-220">**Versión**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-220">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a6b0f-221">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a6b0f-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a6b0f-222">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a6b0f-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a6b0f-223">Versión de la extensión en un formato de "Major. minor", por ejemplo "2,0".</span><span class="sxs-lookup"><span data-stu-id="a6b0f-223">The version of the extension in a format of "major.minor", for example "2.0".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a6b0f-224">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6b0f-224">Requirements</span></span>



| <span data-ttu-id="a6b0f-225">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6b0f-225">Requirement</span></span> | <span data-ttu-id="a6b0f-226">Value</span><span class="sxs-lookup"><span data-stu-id="a6b0f-226">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6b0f-227">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6b0f-227">Minimum supported client</span></span><br/> | <span data-ttu-id="a6b0f-228">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6b0f-228">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a6b0f-229">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6b0f-229">Minimum supported server</span></span><br/> | <span data-ttu-id="a6b0f-230">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6b0f-230">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a6b0f-231">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a6b0f-231">Namespace</span></span><br/>                | <span data-ttu-id="a6b0f-232">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="a6b0f-232">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a6b0f-233">MOF</span><span class="sxs-lookup"><span data-stu-id="a6b0f-233">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a6b0f-234"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a6b0f-234"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a6b0f-235">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a6b0f-235">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6b0f-236"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a6b0f-236"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

