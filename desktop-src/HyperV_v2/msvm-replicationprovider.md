---
description: Representa los proveedores disponibles para la replicación.
ms.assetid: CAAD1CFC-6473-4642-8366-0A5625AE1F70
title: Msvm_ReplicationProvider (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationProvider
- Msvm_ReplicationProvider.InstanceID
- Msvm_ReplicationProvider.Caption
- Msvm_ReplicationProvider.Description
- Msvm_ReplicationProvider.ElementName
- Msvm_ReplicationProvider.Name
- Msvm_ReplicationProvider.OperationalStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8cc821b6bdd5d6f5d1c1085a804799c662f9d62e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910138"
---
# <a name="msvm_replicationprovider-class"></a><span data-ttu-id="ca327-103">MSVM \_ ReplicationProvider (clase)</span><span class="sxs-lookup"><span data-stu-id="ca327-103">Msvm\_ReplicationProvider class</span></span>

<span data-ttu-id="ca327-104">Representa los proveedores disponibles para la replicación.</span><span class="sxs-lookup"><span data-stu-id="ca327-104">Represents the available providers for replication.</span></span>

<span data-ttu-id="ca327-105">La siguiente sintaxis se simplifica desde el código MOF e incluye estas propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ca327-105">The following syntax is simplified from MOF code and includes these inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca327-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ca327-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationProvider : CIM_ManagedSystemElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string Name;
  uint16 OperationalStatus[];
};
```

## <a name="members"></a><span data-ttu-id="ca327-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ca327-107">Members</span></span>

<span data-ttu-id="ca327-108">La clase **MSVM \_ ReplicationProvider** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ca327-108">The **Msvm\_ReplicationProvider** class has these types of members:</span></span>

-   [<span data-ttu-id="ca327-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ca327-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ca327-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ca327-110">Properties</span></span>

<span data-ttu-id="ca327-111">La clase **MSVM \_ ReplicationProvider** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ca327-111">The **Msvm\_ReplicationProvider** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ca327-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ca327-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca327-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ca327-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca327-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca327-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca327-115">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="ca327-115">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="ca327-116">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="ca327-116">A short description of the object.</span></span> <span data-ttu-id="ca327-117">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ca327-117">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span> <span data-ttu-id="ca327-118">Para este objeto, el valor es:</span><span class="sxs-lookup"><span data-stu-id="ca327-118">For this object, the value is:</span></span>

<span data-ttu-id="ca327-119">"Proveedor de replicación"</span><span class="sxs-lookup"><span data-stu-id="ca327-119">"Replication Provider"</span></span>

</dd> <dt>

<span data-ttu-id="ca327-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ca327-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca327-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ca327-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca327-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca327-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca327-123">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="ca327-123">A description of the object.</span></span> <span data-ttu-id="ca327-124">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ca327-124">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span> <span data-ttu-id="ca327-125">En el caso de los proveedores externos, el valor lo proporcionan.</span><span class="sxs-lookup"><span data-stu-id="ca327-125">For external providers, the value is provided by them.</span></span> <span data-ttu-id="ca327-126">Para que el host hospede un proveedor integrado, el valor es:</span><span class="sxs-lookup"><span data-stu-id="ca327-126">For host to host inbuilt provider, the value is:</span></span>

<span data-ttu-id="ca327-127">"Proveedor de replicación de máquina virtual para el host de Hyper-V"</span><span class="sxs-lookup"><span data-stu-id="ca327-127">"Virtual machine replication provider to Hyper-V host"</span></span>

</dd> <dt>

<span data-ttu-id="ca327-128">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ca327-128">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca327-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ca327-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca327-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca327-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca327-131">Un nombre para mostrar para el proveedor de extremos.</span><span class="sxs-lookup"><span data-stu-id="ca327-131">A display name for the endpoint provider.</span></span> <span data-ttu-id="ca327-132">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ca327-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

<span data-ttu-id="ca327-133">Para que el host hospede un proveedor integrado, esta propiedad siempre se establece en:</span><span class="sxs-lookup"><span data-stu-id="ca327-133">For host to host inbuilt provider, this property is always set to:</span></span>

<span data-ttu-id="ca327-134">"Proveedor de replicación de máquina virtual para el host de Hyper-V"</span><span class="sxs-lookup"><span data-stu-id="ca327-134">"Virtual machine replication provider to Hyper-V host"</span></span>

</dd> <dt>

<span data-ttu-id="ca327-135">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ca327-135">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca327-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ca327-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca327-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca327-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca327-138">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="ca327-138">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="ca327-139">IDENTIFICADOR de la instancia de WMI, que identifica el proveedor.</span><span class="sxs-lookup"><span data-stu-id="ca327-139">The WMI instance ID, which identifies the provider.</span></span> <span data-ttu-id="ca327-140">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ca327-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span> <span data-ttu-id="ca327-141">El formato de esta propiedad es "Microsoft: <nombre del equipo host>\\ ReplicationProvider \\<nombre del proveedor>".</span><span class="sxs-lookup"><span data-stu-id="ca327-141">The format of this property is "Microsoft:<host-machine-name>\\ReplicationProvider\\<provider-Name>."</span></span>

</dd> <dt>

<span data-ttu-id="ca327-142">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="ca327-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca327-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ca327-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca327-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca327-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ca327-145">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ca327-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ca327-146">Identificador único global (GUID) del proveedor que identifica el proveedor de extremos.</span><span class="sxs-lookup"><span data-stu-id="ca327-146">The globally unique identifier (GUID) of the provider that identifies the endpoint provider.</span></span> <span data-ttu-id="ca327-147">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ca327-147">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<span data-ttu-id="ca327-148">En el caso de un proveedor externo, esta propiedad es el CLSID del objeto de la clase COM del proveedor.</span><span class="sxs-lookup"><span data-stu-id="ca327-148">In the case of an external provider, this property is the CLSID of the provider COM class object.</span></span> <span data-ttu-id="ca327-149">Para que el host hospede un proveedor integrado, esta propiedad se fija como:</span><span class="sxs-lookup"><span data-stu-id="ca327-149">For host to host inbuilt provider, this property is fixed as:</span></span>

<span data-ttu-id="ca327-150">"22391CDC-272C-4DDF-BA88-9BEFB1A0975C"</span><span class="sxs-lookup"><span data-stu-id="ca327-150">"22391CDC-272C-4DDF-BA88-9BEFB1A0975C"</span></span>

</dd> <dt>

<span data-ttu-id="ca327-151">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="ca327-151">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca327-152">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ca327-152">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ca327-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ca327-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca327-154">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="ca327-154">The current statuses of the object.</span></span> <span data-ttu-id="ca327-155">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de la matriz siempre se establece en:</span><span class="sxs-lookup"><span data-stu-id="ca327-155">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to:</span></span>

<dl> <dt>

<span data-ttu-id="ca327-156"><span id="S_OK"></span><span id="s_ok"></span>**S \_ Aceptar** (2)</span><span class="sxs-lookup"><span data-stu-id="ca327-156"><span id="S_OK"></span><span id="s_ok"></span>**S\_OK** (2)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca327-157">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ca327-157">Remarks</span></span>

<span data-ttu-id="ca327-158">Puede usar cualquiera de los proveedores disponibles y la clase [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) para habilitar una relación de replicación.</span><span class="sxs-lookup"><span data-stu-id="ca327-158">You can use any of available providers and the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class to enable a replication relationship.</span></span> <span data-ttu-id="ca327-159">De forma predeterminada, Hyper-V elige el host integrado para hospedar el proveedor, que se puede cambiar durante la creación de la replicación.</span><span class="sxs-lookup"><span data-stu-id="ca327-159">Hyper-V by default chooses the inbuilt host to host provider, which can be changed while creating the replication.</span></span> <span data-ttu-id="ca327-160">El servicio de administración de Hyper-V se comunica con un proveedor externo mediante COM.</span><span class="sxs-lookup"><span data-stu-id="ca327-160">Hyper-V management service communicates with an external provider by using COM.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca327-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca327-161">Requirements</span></span>



| <span data-ttu-id="ca327-162">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca327-162">Requirement</span></span> | <span data-ttu-id="ca327-163">Value</span><span class="sxs-lookup"><span data-stu-id="ca327-163">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca327-164">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca327-164">Minimum supported client</span></span><br/> | <span data-ttu-id="ca327-165">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="ca327-165">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="ca327-166">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ca327-166">Minimum supported server</span></span><br/> | <span data-ttu-id="ca327-167">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ca327-167">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ca327-168">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ca327-168">Namespace</span></span><br/>                | <span data-ttu-id="ca327-169">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ca327-169">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ca327-170">MOF</span><span class="sxs-lookup"><span data-stu-id="ca327-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca327-171"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca327-171"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca327-172">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ca327-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca327-173"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ca327-173"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ca327-174">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca327-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca327-175">**ManagedSystemElement de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="ca327-175">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dt>

[<span data-ttu-id="ca327-176">**ManagedSystemElement de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="ca327-176">**CIM\_ManagedSystemElement**</span></span>](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)
</dt> </dl>

 

