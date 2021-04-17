---
description: Define una conexión que está activada y configurada actualmente para proporcionar comunicación entre dos \_ objetos punto de CIM.
ms.assetid: 03f8e43f-a77b-46e2-bb7d-c29758c65aee
title: CIM_ActiveConnection (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActiveConnection
- CIM_ActiveConnection.Antecedent
- CIM_ActiveConnection.Dependent
- CIM_ActiveConnection.TrafficType
- CIM_ActiveConnection.OtherTrafficDescription
- CIM_ActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 644e8aaae1368e4164ceca7f7db29e343116c93c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687140"
---
# <a name="cim_activeconnection-class"></a><span data-ttu-id="b7732-103">\_Clase ActiveConnection de CIM</span><span class="sxs-lookup"><span data-stu-id="b7732-103">CIM\_ActiveConnection class</span></span>

<span data-ttu-id="b7732-104">Define una conexión que está activada y configurada actualmente para proporcionar comunicación entre dos objetos **\_ punto de CIM** .</span><span class="sxs-lookup"><span data-stu-id="b7732-104">Defines a connection that is currently turned on and configured to provide communication between two **CIM\_ServiceAccessPoint** objects.</span></span> <span data-ttu-id="b7732-105">**CIM \_ ActiveConnection** se utiliza cuando la conexión no se trata como un **objeto \_ ManagedElement de CIM** .</span><span class="sxs-lookup"><span data-stu-id="b7732-105">**CIM\_ActiveConnection** is used when the connection is not treated as a **CIM\_ManagedElement** object.</span></span> <span data-ttu-id="b7732-106">Los puntos de acceso de servicio que están conectados mediante una conexión activa suelen estar en el mismo nivel de red o de aplicación.</span><span class="sxs-lookup"><span data-stu-id="b7732-106">Service access points that are connected by an active connection are typically at the same networking or application layer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7732-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7732-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ActiveConnection : CIM_SAPSAPDependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
  uint16                     TrafficType;
  string                     OtherTrafficDescription;
  boolean                    IsUnidirectional;
};
```

## <a name="members"></a><span data-ttu-id="b7732-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b7732-108">Members</span></span>

<span data-ttu-id="b7732-109">La clase de **\_ ActiveConnection de CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b7732-109">The **CIM\_ActiveConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="b7732-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b7732-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b7732-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b7732-111">Properties</span></span>

<span data-ttu-id="b7732-112">La clase de **\_ ActiveConnection de CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b7732-112">The **CIM\_ActiveConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b7732-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="b7732-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7732-114">Tipo de datos: **CIM \_ punto**</span><span class="sxs-lookup"><span data-stu-id="b7732-114">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="b7732-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7732-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7732-116">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="b7732-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="b7732-117">El punto de acceso al servicio que está conectado al otro punto de acceso al servicio a través de la conexión activa.</span><span class="sxs-lookup"><span data-stu-id="b7732-117">The service access point that is connected to the other service access point through the active connection.</span></span> <span data-ttu-id="b7732-118">**CIM \_ Objeto punto** .</span><span class="sxs-lookup"><span data-stu-id="b7732-118">**CIM\_ServiceAccessPoint** object.</span></span> <span data-ttu-id="b7732-119">En una conexión unidireccional, este punto de acceso es el que transmite los datos.</span><span class="sxs-lookup"><span data-stu-id="b7732-119">In a unidirectional connection, this access point is the one that is transmitting data.</span></span>

</dd> <dt>

<span data-ttu-id="b7732-120">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="b7732-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7732-121">Tipo de datos: **CIM \_ punto**</span><span class="sxs-lookup"><span data-stu-id="b7732-121">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="b7732-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7732-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7732-123">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="b7732-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="b7732-124">El punto de acceso al servicio que está configurado para comunicarse o está comunicándose activamente con el punto de acceso al servicio especificado en la propiedad **antecedente** .</span><span class="sxs-lookup"><span data-stu-id="b7732-124">The service access point that is configured to communicate or is actively communicating with the service access point specified in the **Antecedent** property.</span></span> <span data-ttu-id="b7732-125">En una conexión unidireccional, este punto de acceso es el que recibe los datos.</span><span class="sxs-lookup"><span data-stu-id="b7732-125">In a unidirectional connection, this access point is the one that is receiving data.</span></span>

</dd> <dt>

<span data-ttu-id="b7732-126">**IsUnidirectional**</span><span class="sxs-lookup"><span data-stu-id="b7732-126">**IsUnidirectional**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7732-127">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="b7732-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b7732-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7732-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7732-129">True si la conexión es unidireccional; false si la conexión es bidireccional.</span><span class="sxs-lookup"><span data-stu-id="b7732-129">True if the connection is unidirectional; false if the connection is bidirectional.</span></span> <span data-ttu-id="b7732-130">Cuando la conexión es unidireccional, la propiedad **antecedente** especifica el punto de acceso que está transmitiendo datos.</span><span class="sxs-lookup"><span data-stu-id="b7732-130">When the connection is unidirectional, the **Antecedent** property specifies the access point that is transmitting data.</span></span> <span data-ttu-id="b7732-131">En una conexión bidireccional, el **antecedente** puede especificar cualquier punto de acceso asignado a la conexión.</span><span class="sxs-lookup"><span data-stu-id="b7732-131">In a bidirectional connection, **Antecedent** can specify either access point assigned to the connection.</span></span>

</dd> <dt>

<span data-ttu-id="b7732-132">**OtherTrafficDescription**</span><span class="sxs-lookup"><span data-stu-id="b7732-132">**OtherTrafficDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7732-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7732-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7732-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7732-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7732-135">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sin valor"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ ActiveConnection de CIM**.**TrafficType**")</span><span class="sxs-lookup"><span data-stu-id="b7732-135">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ActiveConnection**.**TrafficType**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="b7732-136">Esta propiedad está desusada.</span><span class="sxs-lookup"><span data-stu-id="b7732-136">This property is deprecated.</span></span> <span data-ttu-id="b7732-137">En su lugar, se recomienda especificar esta información en el direccionamiento, el protocolo y la funcionalidad básica de los extremos.</span><span class="sxs-lookup"><span data-stu-id="b7732-137">Instead, we recommend that you specify this information in the addressing, protocol, and basic functionality of the endpoints.</span></span>

 

<span data-ttu-id="b7732-138">Descripción del tipo de tráfico que se especifica cuando la propiedad **TrafficType** se establece en "1" (otro).</span><span class="sxs-lookup"><span data-stu-id="b7732-138">A description of the traffic type that is specified when the **TrafficType** property is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="b7732-139">**TrafficType**</span><span class="sxs-lookup"><span data-stu-id="b7732-139">**TrafficType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7732-140">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b7732-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b7732-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7732-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7732-142">Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sin valor"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ ActiveConnection de CIM**.**OtherTrafficDescription**")</span><span class="sxs-lookup"><span data-stu-id="b7732-142">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ActiveConnection**.**OtherTrafficDescription**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="b7732-143">Esta propiedad está desusada.</span><span class="sxs-lookup"><span data-stu-id="b7732-143">This property is deprecated.</span></span> <span data-ttu-id="b7732-144">En su lugar, se recomienda especificar esta información en el direccionamiento, el protocolo y la funcionalidad básica de los extremos.</span><span class="sxs-lookup"><span data-stu-id="b7732-144">Instead, we recommend that you specify this information in the addressing, protocol, and basic functionality of the endpoints.</span></span>

 

<span data-ttu-id="b7732-145">El tipo de tráfico que se transmite a través de esta conexión.</span><span class="sxs-lookup"><span data-stu-id="b7732-145">The type of traffic that is transmitted over this connection.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b7732-146">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="b7732-146">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="b7732-147">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="b7732-147">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unicast"></span><span id="unicast"></span><span id="UNICAST"></span>

<span data-ttu-id="b7732-148">**Unidifusión** (2)</span><span class="sxs-lookup"><span data-stu-id="b7732-148">**Unicast** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Broadcast"></span><span id="broadcast"></span><span id="BROADCAST"></span>

<span data-ttu-id="b7732-149">**Difusión** (3)</span><span class="sxs-lookup"><span data-stu-id="b7732-149">**Broadcast** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Multicast"></span><span id="multicast"></span><span id="MULTICAST"></span>

<span data-ttu-id="b7732-150">**Multidifusión** (4)</span><span class="sxs-lookup"><span data-stu-id="b7732-150">**Multicast** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Anycast"></span><span id="anycast"></span><span id="ANYCAST"></span>

<span data-ttu-id="b7732-151">**Difusión por proximidad** (5)</span><span class="sxs-lookup"><span data-stu-id="b7732-151">**Anycast** (5)</span></span>


<span data-ttu-id="b7732-152"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b7732-152"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="b7732-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7732-153">Requirements</span></span>



| <span data-ttu-id="b7732-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7732-154">Requirement</span></span> | <span data-ttu-id="b7732-155">Value</span><span class="sxs-lookup"><span data-stu-id="b7732-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7732-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7732-156">Minimum supported client</span></span><br/> | <span data-ttu-id="b7732-157">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b7732-157">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="b7732-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7732-158">Minimum supported server</span></span><br/> | <span data-ttu-id="b7732-159">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b7732-159">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="b7732-160">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b7732-160">Namespace</span></span><br/>                | <span data-ttu-id="b7732-161">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b7732-161">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b7732-162">MOF</span><span class="sxs-lookup"><span data-stu-id="b7732-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7732-163"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7732-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7732-164">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b7732-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7732-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b7732-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b7732-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7732-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7732-167">**\_SAPSAPDEPENDENCY CIM**</span><span class="sxs-lookup"><span data-stu-id="b7732-167">**CIM\_SAPSAPDependency**</span></span>](cim-sapsapdependency.md)
</dt> </dl>

 

