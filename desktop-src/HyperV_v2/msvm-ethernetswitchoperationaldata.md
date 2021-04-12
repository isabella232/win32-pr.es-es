---
description: Representa parámetros operativos del conmutador.
ms.assetid: f225d321-8f40-4e6c-b30d-8fab3f84761d
title: Msvm_EthernetSwitchOperationalData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchOperationalData
- Msvm_EthernetSwitchOperationalData.InstanceID
- Msvm_EthernetSwitchOperationalData.Caption
- Msvm_EthernetSwitchOperationalData.Description
- Msvm_EthernetSwitchOperationalData.ElementName
- Msvm_EthernetSwitchOperationalData.SystemCreationClassName
- Msvm_EthernetSwitchOperationalData.SystemName
- Msvm_EthernetSwitchOperationalData.CreationClassName
- Msvm_EthernetSwitchOperationalData.Name
- Msvm_EthernetSwitchOperationalData.CurrentSwitchingMode
- Msvm_EthernetSwitchOperationalData.SupportedSwitchingModes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3d9aacd8380650ddaf2790aeacf4a2327b54f973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361731"
---
# <a name="msvm_ethernetswitchoperationaldata-class"></a><span data-ttu-id="f520b-103">MSVM \_ EthernetSwitchOperationalData (clase)</span><span class="sxs-lookup"><span data-stu-id="f520b-103">Msvm\_EthernetSwitchOperationalData class</span></span>

<span data-ttu-id="f520b-104">Representa parámetros operativos del conmutador.</span><span class="sxs-lookup"><span data-stu-id="f520b-104">Represents switch operational parameters.</span></span>

<span data-ttu-id="f520b-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f520b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f520b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f520b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1D18CDCF-209E-4172-875D-6D208A0A8375"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Modes Supported "), AMENDMENT]
class Msvm_EthernetSwitchOperationalData : Msvm_EthernetSwitchData
{
  string InstanceID;
  string Caption = "Ethernet Switch Modes Supported";
  string Description = "Represents switch operational parameters.";
  string ElementName = "Ethernet Switch Modes Supported";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string CreationClassName = " Msvm_EthernetSwitchOperationalData";
  string Name;
  uint32 CurrentSwitchingMode = 1;
  uint32 SupportedSwitchingModes[] = {1};
};
```

## <a name="members"></a><span data-ttu-id="f520b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f520b-107">Members</span></span>

<span data-ttu-id="f520b-108">La clase **MSVM \_ EthernetSwitchOperationalData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f520b-108">The **Msvm\_EthernetSwitchOperationalData** class has these types of members:</span></span>

-   [<span data-ttu-id="f520b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f520b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f520b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f520b-110">Properties</span></span>

<span data-ttu-id="f520b-111">La clase **MSVM \_ EthernetSwitchOperationalData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f520b-111">The **Msvm\_EthernetSwitchOperationalData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f520b-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f520b-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f520b-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f520b-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f520b-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f520b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f520b-115">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="f520b-115">A short description of the object.</span></span> <span data-ttu-id="f520b-116">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f520b-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f520b-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f520b-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f520b-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f520b-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f520b-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f520b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f520b-120">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="f520b-120">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="f520b-121">Nombre de la clase o subclase utilizada en la creación de esta instancia.</span><span class="sxs-lookup"><span data-stu-id="f520b-121">The name of the class or subclass used in the creation of this instance.</span></span> <span data-ttu-id="f520b-122">Esta propiedad se hereda de [**MSVM \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="f520b-122">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="f520b-123">**CurrentSwitchingMode**</span><span class="sxs-lookup"><span data-stu-id="f520b-123">**CurrentSwitchingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f520b-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f520b-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f520b-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f520b-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f520b-126">Calificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f520b-126">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f520b-127">Modo de cambio actual en el modificador.</span><span class="sxs-lookup"><span data-stu-id="f520b-127">The current switching mode on the switch.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f520b-128">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="f520b-128">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1Q"></span><span id="802.1q"></span>

<span data-ttu-id="f520b-129">**802.1 q** (1)</span><span class="sxs-lookup"><span data-stu-id="f520b-129">**802.1Q** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1Qbg"></span><span id="802.1qbg"></span><span id="802.1QBG"></span>

<span data-ttu-id="f520b-130">**802.1 qbg** (2)</span><span class="sxs-lookup"><span data-stu-id="f520b-130">**802.1Qbg** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1Qbh"></span><span id="802.1qbh"></span><span id="802.1QBH"></span>

<span data-ttu-id="f520b-131">**802.1 QBH** (3)</span><span class="sxs-lookup"><span data-stu-id="f520b-131">**802.1Qbh** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f520b-132">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f520b-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f520b-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f520b-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f520b-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f520b-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f520b-135">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="f520b-135">A description of the object.</span></span> <span data-ttu-id="f520b-136">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f520b-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f520b-137">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="f520b-137">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f520b-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f520b-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f520b-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f520b-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f520b-140">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="f520b-140">A display name for the object.</span></span> <span data-ttu-id="f520b-141">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f520b-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f520b-142">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f520b-142">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f520b-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f520b-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f520b-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f520b-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f520b-145">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="f520b-145">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f520b-146">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="f520b-146">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="f520b-147">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="f520b-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="f520b-148">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="f520b-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f520b-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f520b-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f520b-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f520b-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f520b-151">Calificadores: **clave**, **invalidación**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="f520b-151">Qualifiers: **Key**, **Override**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="f520b-152">Nombre único del recurso.</span><span class="sxs-lookup"><span data-stu-id="f520b-152">The unique name of the resource.</span></span> <span data-ttu-id="f520b-153">Esta propiedad se hereda de [**MSVM \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="f520b-153">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="f520b-154">**SupportedSwitchingModes**</span><span class="sxs-lookup"><span data-stu-id="f520b-154">**SupportedSwitchingModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f520b-155">Tipo de datos: **UInt32** array</span><span class="sxs-lookup"><span data-stu-id="f520b-155">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="f520b-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f520b-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f520b-157">Calificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="f520b-157">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="f520b-158">Modos de cambio admitidos por el modificador.</span><span class="sxs-lookup"><span data-stu-id="f520b-158">The switching modes supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="f520b-159">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f520b-159">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f520b-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f520b-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f520b-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f520b-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f520b-162">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="f520b-162">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="f520b-163">Nombre de la clase de creación del sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="f520b-163">The hosting system's creation class name.</span></span> <span data-ttu-id="f520b-164">Esta propiedad se hereda de [**MSVM \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="f520b-164">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="f520b-165">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f520b-165">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f520b-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f520b-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f520b-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f520b-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f520b-168">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="f520b-168">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="f520b-169">El nombre del conmutador virtual al que está enlazada la instancia de recurso asociada.</span><span class="sxs-lookup"><span data-stu-id="f520b-169">The name of the virtual switch to which the associated resource instance is bound.</span></span> <span data-ttu-id="f520b-170">Esta propiedad se hereda de [**MSVM \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="f520b-170">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f520b-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f520b-171">Requirements</span></span>



| <span data-ttu-id="f520b-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="f520b-172">Requirement</span></span> | <span data-ttu-id="f520b-173">Value</span><span class="sxs-lookup"><span data-stu-id="f520b-173">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f520b-174">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f520b-174">Minimum supported client</span></span><br/> | <span data-ttu-id="f520b-175">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="f520b-175">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f520b-176">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f520b-176">Minimum supported server</span></span><br/> | <span data-ttu-id="f520b-177">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="f520b-177">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f520b-178">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f520b-178">Namespace</span></span><br/>                | <span data-ttu-id="f520b-179">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f520b-179">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f520b-180">MOF</span><span class="sxs-lookup"><span data-stu-id="f520b-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f520b-181"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f520b-181"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f520b-182">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f520b-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f520b-183"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f520b-183"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

