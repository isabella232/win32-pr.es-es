---
description: Clase abstracta que representa un recurso para una instancia determinada de un modificador Ethernet.
ms.assetid: 5ae1be2a-8d59-4efe-a4ae-7cac1727cfa2
title: Msvm_EthernetSwitchData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchData
- Msvm_EthernetSwitchData.InstanceID
- Msvm_EthernetSwitchData.Caption
- Msvm_EthernetSwitchData.Description
- Msvm_EthernetSwitchData.ElementName
- Msvm_EthernetSwitchData.SystemCreationClassName
- Msvm_EthernetSwitchData.SystemName
- Msvm_EthernetSwitchData.CreationClassName
- Msvm_EthernetSwitchData.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dca2e4e01266a0a7da0f3ec85a86615406625f45
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667563"
---
# <a name="msvm_ethernetswitchdata-class"></a><span data-ttu-id="49000-103">MSVM \_ EthernetSwitchData (clase)</span><span class="sxs-lookup"><span data-stu-id="49000-103">Msvm\_EthernetSwitchData class</span></span>

<span data-ttu-id="49000-104">Clase abstracta que representa un recurso para una instancia determinada de un modificador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="49000-104">Abstract class that represents a resource for a given instance of an Ethernet switch.</span></span>

<span data-ttu-id="49000-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="49000-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="49000-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="49000-106">Syntax</span></span>

``` syntax
[Abstract, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchData : CIM_ManagedElement
{
  string InstanceID;
  string Caption = "Ethernet Switch Bandwidth data";
  string Description = "Represents the switch bandwidth resource status.";
  string ElementName = "Ethernet Switch Bandwidth data";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string CreationClassName = " Msvm_EthernetSwitchBandwidthData";
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="49000-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="49000-107">Members</span></span>

<span data-ttu-id="49000-108">La clase **MSVM \_ EthernetSwitchData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="49000-108">The **Msvm\_EthernetSwitchData** class has these types of members:</span></span>

-   [<span data-ttu-id="49000-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="49000-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="49000-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="49000-110">Properties</span></span>

<span data-ttu-id="49000-111">La clase **MSVM \_ EthernetSwitchData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="49000-111">The **Msvm\_EthernetSwitchData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="49000-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="49000-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49000-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="49000-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49000-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="49000-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49000-115">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="49000-115">A short description of the object.</span></span> <span data-ttu-id="49000-116">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="49000-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="49000-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="49000-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49000-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="49000-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49000-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="49000-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49000-120">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="49000-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="49000-121">Nombre de la clase o subclase utilizada en la creación de esta instancia.</span><span class="sxs-lookup"><span data-stu-id="49000-121">The name of the class or subclass used in the creation of this instance.</span></span>

</dd> <dt>

<span data-ttu-id="49000-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="49000-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49000-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="49000-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49000-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="49000-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49000-125">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="49000-125">A description of the object.</span></span> <span data-ttu-id="49000-126">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="49000-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="49000-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="49000-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49000-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="49000-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49000-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="49000-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="49000-130">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="49000-130">A display name for the object.</span></span> <span data-ttu-id="49000-131">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="49000-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="49000-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="49000-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49000-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="49000-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49000-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="49000-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49000-135">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="49000-135">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="49000-136">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="49000-136">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="49000-137">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="49000-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="49000-138">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="49000-138">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49000-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="49000-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49000-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="49000-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49000-141">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="49000-141">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="49000-142">Nombre único del recurso.</span><span class="sxs-lookup"><span data-stu-id="49000-142">The unique name of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="49000-143">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="49000-143">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49000-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="49000-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49000-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="49000-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49000-146">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="49000-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="49000-147">Nombre de la clase de creación del sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="49000-147">The hosting system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="49000-148">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="49000-148">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="49000-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="49000-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="49000-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="49000-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="49000-151">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Nombre**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="49000-151">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="49000-152">El nombre del conmutador virtual al que está enlazada la instancia de recurso asociada.</span><span class="sxs-lookup"><span data-stu-id="49000-152">The name of the virtual switch to which the associated resource instance is bound.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="49000-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49000-153">Requirements</span></span>



| <span data-ttu-id="49000-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="49000-154">Requirement</span></span> | <span data-ttu-id="49000-155">Value</span><span class="sxs-lookup"><span data-stu-id="49000-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49000-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49000-156">Minimum supported client</span></span><br/> | <span data-ttu-id="49000-157">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="49000-157">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="49000-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="49000-158">Minimum supported server</span></span><br/> | <span data-ttu-id="49000-159">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="49000-159">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="49000-160">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="49000-160">Namespace</span></span><br/>                | <span data-ttu-id="49000-161">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="49000-161">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="49000-162">MOF</span><span class="sxs-lookup"><span data-stu-id="49000-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49000-163"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="49000-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="49000-164">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="49000-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49000-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="49000-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

