---
description: Una clase abstracta que representa los datos de tiempo de ejecución de Puerto recopilados por una extensión de conmutador Ethernet.
ms.assetid: bc41ad1d-e7ab-4d04-96a8-26eb68ea6601
title: Msvm_EthernetPortData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortData
- Msvm_EthernetPortData.InstanceID
- Msvm_EthernetPortData.Caption
- Msvm_EthernetPortData.Description
- Msvm_EthernetPortData.ElementName
- Msvm_EthernetPortData.SystemCreationClassName
- Msvm_EthernetPortData.SystemName
- Msvm_EthernetPortData.DeviceCreationClassName
- Msvm_EthernetPortData.DeviceID
- Msvm_EthernetPortData.CreationClassName
- Msvm_EthernetPortData.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 36167d4acad3c0da6b96efb9f9cc1fe58bd41a0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910154"
---
# <a name="msvm_ethernetportdata-class"></a><span data-ttu-id="8a9c7-103">MSVM \_ EthernetPortData (clase)</span><span class="sxs-lookup"><span data-stu-id="8a9c7-103">Msvm\_EthernetPortData class</span></span>

<span data-ttu-id="8a9c7-104">Una clase abstracta que representa los datos de tiempo de ejecución de Puerto recopilados por una extensión de conmutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="8a9c7-104">An abstract class that represents port runtime data collected by an Ethernet switch extension.</span></span> <span data-ttu-id="8a9c7-105">Todas las clases de datos de puerto Ethernet deben derivar de esta clase abstracta.</span><span class="sxs-lookup"><span data-stu-id="8a9c7-105">All Ethernet port data classes must derive from this abstract class.</span></span>

<span data-ttu-id="8a9c7-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="8a9c7-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a9c7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8a9c7-107">Syntax</span></span>

``` syntax
[Abstract, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortData : CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string SystemCreationClassName;
  string SystemName;
  string DeviceCreationClassName = "Msvm_EthernetSwitchPort";
  string DeviceID;
  string CreationClassName;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="8a9c7-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="8a9c7-108">Members</span></span>

<span data-ttu-id="8a9c7-109">La clase **MSVM \_ EthernetPortData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8a9c7-109">The **Msvm\_EthernetPortData** class has these types of members:</span></span>

-   [<span data-ttu-id="8a9c7-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8a9c7-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8a9c7-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8a9c7-111">Properties</span></span>

<span data-ttu-id="8a9c7-112">La clase **MSVM \_ EthernetPortData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8a9c7-112">The **Msvm\_EthernetPortData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8a9c7-113">**Caption**</span><span class="sxs-lookup"><span data-stu-id="8a9c7-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a9c7-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a9c7-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a9c7-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a9c7-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a9c7-116">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="8a9c7-116">A short description of the object.</span></span> <span data-ttu-id="8a9c7-117">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8a9c7-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8a9c7-118">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8a9c7-118">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a9c7-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a9c7-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a9c7-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a9c7-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a9c7-121">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8a9c7-121">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8a9c7-122">Nombre de la subclase utilizada en la creación de esta instancia de datos de puerto.</span><span class="sxs-lookup"><span data-stu-id="8a9c7-122">The name of the subclass used in the creation of this port data instance.</span></span>

</dd> <dt>

<span data-ttu-id="8a9c7-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="8a9c7-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a9c7-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a9c7-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a9c7-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a9c7-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a9c7-126">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="8a9c7-126">A description of the object.</span></span> <span data-ttu-id="8a9c7-127">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8a9c7-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8a9c7-128">**DeviceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8a9c7-128">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a9c7-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a9c7-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a9c7-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a9c7-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a9c7-131">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**propagado**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ LogicalDevice de CIM**](cim-logicaldevice.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8a9c7-131">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8a9c7-132">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="8a9c7-132">The scoping system's creation class name.</span></span> <span data-ttu-id="8a9c7-133">Esta propiedad siempre se establece en "MSVM \_ EthernetSwitchPort".</span><span class="sxs-lookup"><span data-stu-id="8a9c7-133">This property is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="8a9c7-134">**ID**</span><span class="sxs-lookup"><span data-stu-id="8a9c7-134">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a9c7-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a9c7-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a9c7-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a9c7-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a9c7-137">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**propagado**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ LogicalDevice de CIM**](cim-logicaldevice.md).**DeviceID**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="8a9c7-137">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**DeviceID**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="8a9c7-138">El ID. de dispositivo del puerto que limita esta instancia de datos del puerto.</span><span class="sxs-lookup"><span data-stu-id="8a9c7-138">The Device ID of the port that scopes this port data instance.</span></span>

</dd> <dt>

<span data-ttu-id="8a9c7-139">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="8a9c7-139">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a9c7-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a9c7-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a9c7-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a9c7-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8a9c7-142">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="8a9c7-142">A display name for the object.</span></span> <span data-ttu-id="8a9c7-143">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8a9c7-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8a9c7-144">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8a9c7-144">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a9c7-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a9c7-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a9c7-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a9c7-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a9c7-147">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="8a9c7-147">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="8a9c7-148">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="8a9c7-148">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="8a9c7-149">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="8a9c7-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="8a9c7-150">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="8a9c7-150">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a9c7-151">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a9c7-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a9c7-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a9c7-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a9c7-153">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8a9c7-153">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8a9c7-154">Cadena que identifica de forma única esta instancia de datos de puerto en el ámbito del modificador y el puerto.</span><span class="sxs-lookup"><span data-stu-id="8a9c7-154">A string that uniquely identifies this port data instance within the scope of the switch and port.</span></span>

</dd> <dt>

<span data-ttu-id="8a9c7-155">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8a9c7-155">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a9c7-156">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a9c7-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a9c7-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a9c7-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a9c7-158">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8a9c7-158">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8a9c7-159">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="8a9c7-159">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="8a9c7-160">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="8a9c7-160">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a9c7-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="8a9c7-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a9c7-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8a9c7-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a9c7-163">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Nombre**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8a9c7-163">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8a9c7-164">El nombre del conmutador virtual que limita esta instancia de datos de puerto.</span><span class="sxs-lookup"><span data-stu-id="8a9c7-164">The name of the virtual switch that scopes this port data instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8a9c7-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a9c7-165">Requirements</span></span>



| <span data-ttu-id="8a9c7-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a9c7-166">Requirement</span></span> | <span data-ttu-id="8a9c7-167">Value</span><span class="sxs-lookup"><span data-stu-id="8a9c7-167">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a9c7-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a9c7-168">Minimum supported client</span></span><br/> | <span data-ttu-id="8a9c7-169">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="8a9c7-169">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="8a9c7-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a9c7-170">Minimum supported server</span></span><br/> | <span data-ttu-id="8a9c7-171">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="8a9c7-171">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8a9c7-172">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8a9c7-172">Namespace</span></span><br/>                | <span data-ttu-id="8a9c7-173">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="8a9c7-173">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="8a9c7-174">MOF</span><span class="sxs-lookup"><span data-stu-id="8a9c7-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a9c7-175"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a9c7-175"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a9c7-176">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8a9c7-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a9c7-177"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8a9c7-177"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

