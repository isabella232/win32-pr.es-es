---
description: Representa una entrada en la base de datos de reenvío (filtrado) que está asociada con el servicio de puente transparente.
ms.assetid: 3C9FAE99-9543-4A6A-B578-3F4626598DB3
title: Msvm_DynamicForwardingEntry (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DynamicForwardingEntry
- Msvm_DynamicForwardingEntry.InstanceID
- Msvm_DynamicForwardingEntry.Caption
- Msvm_DynamicForwardingEntry.Description
- Msvm_DynamicForwardingEntry.ElementName
- Msvm_DynamicForwardingEntry.InstallDate
- Msvm_DynamicForwardingEntry.Name
- Msvm_DynamicForwardingEntry.OperationalStatus
- Msvm_DynamicForwardingEntry.StatusDescriptions
- Msvm_DynamicForwardingEntry.Status
- Msvm_DynamicForwardingEntry.HealthState
- Msvm_DynamicForwardingEntry.CommunicationStatus
- Msvm_DynamicForwardingEntry.DetailedStatus
- Msvm_DynamicForwardingEntry.OperatingStatus
- Msvm_DynamicForwardingEntry.PrimaryStatus
- Msvm_DynamicForwardingEntry.SystemCreationClassName
- Msvm_DynamicForwardingEntry.SystemName
- Msvm_DynamicForwardingEntry.ServiceCreationClassName
- Msvm_DynamicForwardingEntry.ServiceName
- Msvm_DynamicForwardingEntry.CreationClassName
- Msvm_DynamicForwardingEntry.MACAddress
- Msvm_DynamicForwardingEntry.DynamicStatus
- Msvm_DynamicForwardingEntry.VlanId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f14f8b3a8f5f62e1a474b3d7b7f832b6acd530f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687952"
---
# <a name="msvm_dynamicforwardingentry-class"></a><span data-ttu-id="8ed92-103">MSVM \_ DynamicForwardingEntry (clase)</span><span class="sxs-lookup"><span data-stu-id="8ed92-103">Msvm\_DynamicForwardingEntry class</span></span>

<span data-ttu-id="8ed92-104">Representa una entrada en la base de datos de reenvío (filtrado) que está asociada con el servicio de puente transparente.</span><span class="sxs-lookup"><span data-stu-id="8ed92-104">Represents an entry in the forwarding (filtering) database that is associated with the transparent bridging service.</span></span> <span data-ttu-id="8ed92-105">La entrada es débil para el servicio, como se especifica en [**MSVM \_ TransparentBridgingDynamicForwarding**](msvm-transparentbridgingdynamicforwarding.md).</span><span class="sxs-lookup"><span data-stu-id="8ed92-105">The entry is weak to the service, as specified by [**Msvm\_TransparentBridgingDynamicForwarding**](msvm-transparentbridgingdynamicforwarding.md).</span></span>

<span data-ttu-id="8ed92-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="8ed92-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ed92-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8ed92-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DynamicForwardingEntry : CIM_DynamicForwardingEntry
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   SystemCreationClassName;
  string   SystemName;
  string   ServiceCreationClassName;
  string   ServiceName;
  string   CreationClassName;
  string   MACAddress;
  uint16   DynamicStatus;
  uint16   VlanId;
};
```

## <a name="members"></a><span data-ttu-id="8ed92-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="8ed92-108">Members</span></span>

<span data-ttu-id="8ed92-109">La clase **MSVM \_ DynamicForwardingEntry** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8ed92-109">The **Msvm\_DynamicForwardingEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="8ed92-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8ed92-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8ed92-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8ed92-111">Properties</span></span>

<span data-ttu-id="8ed92-112">La clase **MSVM \_ DynamicForwardingEntry** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8ed92-112">The **Msvm\_DynamicForwardingEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8ed92-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8ed92-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ed92-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8ed92-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ed92-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-116">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="8ed92-116">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="8ed92-117">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="8ed92-117">A short description of the object.</span></span> <span data-ttu-id="8ed92-118">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8ed92-118">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ed92-119">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="8ed92-119">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ed92-120">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8ed92-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ed92-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ed92-122">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="8ed92-122">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="8ed92-123">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="8ed92-123">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8ed92-124">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8ed92-124">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ed92-125">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8ed92-125">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ed92-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8ed92-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ed92-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-128">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="8ed92-128">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="8ed92-129">El nombre de la clase o la subclase utilizada en la creación de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="8ed92-129">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="8ed92-130">Cuando se usa con las otras propiedades de clave de esta clase, esta propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="8ed92-130">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="8ed92-131">Esta propiedad se hereda de [**\_ DynamicForwardingEntry CIM**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8ed92-131">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8ed92-132">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8ed92-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ed92-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8ed92-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ed92-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ed92-135">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="8ed92-135">A description of the object.</span></span> <span data-ttu-id="8ed92-136">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8ed92-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ed92-137">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="8ed92-137">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ed92-138">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8ed92-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ed92-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ed92-140">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="8ed92-140">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="8ed92-141">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="8ed92-141">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8ed92-142">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8ed92-142">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ed92-143">**DynamicStatus**</span><span class="sxs-lookup"><span data-stu-id="8ed92-143">**DynamicStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ed92-144">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8ed92-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ed92-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ed92-146">Estado de la entrada.</span><span class="sxs-lookup"><span data-stu-id="8ed92-146">The status of the entry.</span></span> <span data-ttu-id="8ed92-147">Esta propiedad se hereda de [**\_ DynamicForwardingEntry CIM**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8ed92-147">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="8ed92-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="8ed92-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-149"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**No válido** (2)</span><span class="sxs-lookup"><span data-stu-id="8ed92-149"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Invalid** (2)</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-150"><span id="Learned"></span><span id="learned"></span><span id="LEARNED"></span>**Aprendido** (3)</span><span class="sxs-lookup"><span data-stu-id="8ed92-150"><span id="Learned"></span><span id="learned"></span><span id="LEARNED"></span>**Learned** (3)</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-151"><span id="Self"></span><span id="self"></span><span id="SELF"></span>**Self** (4)</span><span class="sxs-lookup"><span data-stu-id="8ed92-151"><span id="Self"></span><span id="self"></span><span id="SELF"></span>**Self** (4)</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-152"><span id="Mgmt"></span><span id="mgmt"></span><span id="MGMT"></span>**MGMT** (5)</span><span class="sxs-lookup"><span data-stu-id="8ed92-152"><span id="Mgmt"></span><span id="mgmt"></span><span id="MGMT"></span>**Mgmt** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8ed92-153">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8ed92-153">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ed92-154">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8ed92-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ed92-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ed92-156">Nombre para mostrar del elemento.</span><span class="sxs-lookup"><span data-stu-id="8ed92-156">A display name for the element.</span></span> <span data-ttu-id="8ed92-157">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8ed92-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ed92-158">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="8ed92-158">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ed92-159">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8ed92-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ed92-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ed92-161">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="8ed92-161">The current health of the element.</span></span> <span data-ttu-id="8ed92-162">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre está establecida en 5 ("correcto").</span><span class="sxs-lookup"><span data-stu-id="8ed92-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 ("OK").</span></span>

</dd> <dt>

<span data-ttu-id="8ed92-163">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8ed92-163">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ed92-164">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8ed92-164">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ed92-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ed92-166">Se rellena automáticamente cuando se crea la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="8ed92-166">Automatically populated when the virtual machine is created.</span></span> <span data-ttu-id="8ed92-167">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8ed92-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ed92-168">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8ed92-168">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ed92-169">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8ed92-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ed92-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-171">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="8ed92-171">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8ed92-172">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="8ed92-172">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8ed92-173">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8ed92-173">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ed92-174">**Mac**</span><span class="sxs-lookup"><span data-stu-id="8ed92-174">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ed92-175">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8ed92-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ed92-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-177">Calificadores: **clave**, **MaxLen** (12)</span><span class="sxs-lookup"><span data-stu-id="8ed92-177">Qualifiers: **Key**, **MaxLen** (12)</span></span>
</dt> </dl>

<span data-ttu-id="8ed92-178">Dirección MAC de unidifusión para la que el servicio de puentes transparente tiene información de reenvío y filtrado.</span><span class="sxs-lookup"><span data-stu-id="8ed92-178">Unicast MAC address for which the transparent bridging service has forwarding and filtering information.</span></span> <span data-ttu-id="8ed92-179">La dirección MAC tiene el formato de doce dígitos hexadecimales (por ejemplo, "010203040506"), donde cada par representa uno de los seis octetos de la dirección MAC en el orden de bits "canónico" según RFC 2469.</span><span class="sxs-lookup"><span data-stu-id="8ed92-179">The MAC address is formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in "canonical" bit order according to RFC 2469.</span></span> <span data-ttu-id="8ed92-180">Esta propiedad se hereda de [**\_ DynamicForwardingEntry CIM**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8ed92-180">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8ed92-181">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="8ed92-181">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ed92-182">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8ed92-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ed92-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ed92-184">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="8ed92-184">The label by which the object is known.</span></span> <span data-ttu-id="8ed92-185">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8ed92-185">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ed92-186">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="8ed92-186">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ed92-187">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8ed92-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ed92-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ed92-189">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="8ed92-189">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="8ed92-190">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="8ed92-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8ed92-191">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8ed92-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ed92-192">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="8ed92-192">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ed92-193">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8ed92-193">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ed92-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ed92-195">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se admite.</span><span class="sxs-lookup"><span data-stu-id="8ed92-195">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8ed92-196">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="8ed92-196">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ed92-197">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8ed92-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ed92-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ed92-199">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="8ed92-199">Provides high level status information.</span></span> <span data-ttu-id="8ed92-200">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar información de estado de mantenimiento detallada y de alto nivel para el elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="8ed92-200">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="8ed92-201">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="8ed92-201">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="8ed92-202">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="8ed92-202">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="8ed92-203">**ServiceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8ed92-203">**ServiceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ed92-204">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8ed92-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-205">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ed92-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-206">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="8ed92-206">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="8ed92-207">**CreationClassName** del servicio de ámbito.</span><span class="sxs-lookup"><span data-stu-id="8ed92-207">The scoping service's **CreationClassName**.</span></span> <span data-ttu-id="8ed92-208">Esta propiedad se hereda de [**\_ DynamicForwardingEntry CIM**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8ed92-208">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8ed92-209">**ServiceName**</span><span class="sxs-lookup"><span data-stu-id="8ed92-209">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ed92-210">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8ed92-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-211">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ed92-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-212">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="8ed92-212">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="8ed92-213">Nombre del servicio de ámbito.</span><span class="sxs-lookup"><span data-stu-id="8ed92-213">The scoping service's name.</span></span> <span data-ttu-id="8ed92-214">Esta propiedad se hereda de [**\_ DynamicForwardingEntry CIM**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8ed92-214">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8ed92-215">**Estado**</span><span class="sxs-lookup"><span data-stu-id="8ed92-215">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ed92-216">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8ed92-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-217">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ed92-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ed92-218">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="8ed92-218">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8ed92-219">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="8ed92-219">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ed92-220">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="8ed92-220">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-221">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ed92-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ed92-222">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se admite.</span><span class="sxs-lookup"><span data-stu-id="8ed92-222">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="8ed92-223">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8ed92-223">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ed92-224">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8ed92-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-225">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ed92-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-226">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="8ed92-226">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="8ed92-227">**CreationClassName** del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="8ed92-227">The scoping system's **CreationClassName**.</span></span> <span data-ttu-id="8ed92-228">Esta propiedad se hereda de [**\_ DynamicForwardingEntry CIM**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8ed92-228">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8ed92-229">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8ed92-229">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ed92-230">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8ed92-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8ed92-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-232">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="8ed92-232">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="8ed92-233">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="8ed92-233">The scoping system's name.</span></span> <span data-ttu-id="8ed92-234">Esta propiedad se hereda de [**\_ DynamicForwardingEntry CIM**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8ed92-234">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="8ed92-235">**VlanId**</span><span class="sxs-lookup"><span data-stu-id="8ed92-235">**VlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ed92-236">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="8ed92-236">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="8ed92-237">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="8ed92-237">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8ed92-238">Identificador de LAN virtual asociado a esta entrada.</span><span class="sxs-lookup"><span data-stu-id="8ed92-238">The virtual LAN identifier associated with this entry.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ed92-239">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ed92-239">Remarks</span></span>

<span data-ttu-id="8ed92-240">El acceso a la clase **MSVM \_ DynamicForwardingEntry** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="8ed92-240">Access to the **Msvm\_DynamicForwardingEntry** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="8ed92-241">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="8ed92-241">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="8ed92-242">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8ed92-242">Examples</span></span>

<span data-ttu-id="8ed92-243">Consulte [consultar objetos de red](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8ed92-243">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ed92-244">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ed92-244">Requirements</span></span>



| <span data-ttu-id="8ed92-245">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ed92-245">Requirement</span></span> | <span data-ttu-id="8ed92-246">Value</span><span class="sxs-lookup"><span data-stu-id="8ed92-246">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ed92-247">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ed92-247">Minimum supported client</span></span><br/> | <span data-ttu-id="8ed92-248">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="8ed92-248">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8ed92-249">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8ed92-249">Minimum supported server</span></span><br/> | <span data-ttu-id="8ed92-250">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="8ed92-250">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8ed92-251">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8ed92-251">Namespace</span></span><br/>                | <span data-ttu-id="8ed92-252">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="8ed92-252">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8ed92-253">MOF</span><span class="sxs-lookup"><span data-stu-id="8ed92-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ed92-254"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8ed92-254"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8ed92-255">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8ed92-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ed92-256"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8ed92-256"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8ed92-257">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ed92-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ed92-258">**\_DYNAMICFORWARDINGENTRY CIM**</span><span class="sxs-lookup"><span data-stu-id="8ed92-258">**CIM\_DynamicForwardingEntry**</span></span>](cim-dynamicforwardingentry.md)
</dt> <dt>

<span data-ttu-id="8ed92-259">[**\_DYNAMICFORWARDINGENTRY CIM**](/previous-versions//cc136814(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8ed92-259">[**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85))</span></span>
</dt> </dl>

 

