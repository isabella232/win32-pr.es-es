---
description: Conecta un puerto del conmutador al punto de conexión de LAN al que está conectado el puerto.
ms.assetid: 963EC004-6A67-4F75-BD93-1BCD17F32490
title: Msvm_ActiveConnection (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ActiveConnection
- Msvm_ActiveConnection.Antecedent
- Msvm_ActiveConnection.Dependent
- Msvm_ActiveConnection.TrafficType
- Msvm_ActiveConnection.OtherTrafficDescription
- Msvm_ActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cf682fac419658785cfe7594aa6fc17e4b2dd28e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911925"
---
# <a name="msvm_activeconnection-class"></a><span data-ttu-id="ec12e-103">MSVM ( \_ clase de ActiveConnection)</span><span class="sxs-lookup"><span data-stu-id="ec12e-103">Msvm\_ActiveConnection class</span></span>

<span data-ttu-id="ec12e-104">Conecta un puerto del conmutador al punto de conexión de LAN al que está conectado el puerto.</span><span class="sxs-lookup"><span data-stu-id="ec12e-104">Connects a switch port to the LAN endpoint to which the port is connected.</span></span> <span data-ttu-id="ec12e-105">La existencia de este objeto significa que el puerto del conmutador y el punto de conexión de LAN están conectados activamente y el puerto Ethernet asociado al punto de conexión de LAN puede comunicarse con la red a través del puerto del conmutador.</span><span class="sxs-lookup"><span data-stu-id="ec12e-105">The existence of this object means that the switch port and the LAN endpoint are actively connected and the Ethernet port associated with the LAN endpoint can communicate with the network through the switch port.</span></span>

<span data-ttu-id="ec12e-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ec12e-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec12e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ec12e-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ActiveConnection : CIM_ActiveConnection
{
  Msvm_LANEndpoint REF Antecedent;
  CIM_LANEndpoint  REF Dependent;
  uint16               TrafficType;
  string               OtherTrafficDescription;
  boolean              IsUnidirectional;
};
```

## <a name="members"></a><span data-ttu-id="ec12e-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="ec12e-108">Members</span></span>

<span data-ttu-id="ec12e-109">La clase **MSVM \_ ActiveConnection** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ec12e-109">The **Msvm\_ActiveConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="ec12e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ec12e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ec12e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ec12e-111">Properties</span></span>

<span data-ttu-id="ec12e-112">La clase **MSVM \_ ActiveConnection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ec12e-112">The **Msvm\_ActiveConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ec12e-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="ec12e-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec12e-114">Tipo de datos: **[ **MSVM \_ LANEndpoint**](msvm-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="ec12e-114">Data type: **[**Msvm\_LANEndpoint**](msvm-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="ec12e-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ec12e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec12e-116">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="ec12e-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="ec12e-117">Una referencia a una instancia de la clase [**MSVM \_ LANEndpoint**](msvm-lanendpoint.md) que representa el punto de acceso al servicio (SAP) que está configurado para comunicarse o se comunica activamente con el SAP dependiente.</span><span class="sxs-lookup"><span data-stu-id="ec12e-117">A reference to an instance of the [**Msvm\_LANEndpoint**](msvm-lanendpoint.md) class that represents the service access point (SAP) that is configured to communicate or is actively communicating with the dependent SAP.</span></span> <span data-ttu-id="ec12e-118">En una conexión unidireccional, este SAP es el que se está transmitiendo.</span><span class="sxs-lookup"><span data-stu-id="ec12e-118">In an unidirectional connection, this SAP is the one that is transmitting.</span></span>

</dd> <dt>

<span data-ttu-id="ec12e-119">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="ec12e-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec12e-120">Tipo de datos: **[ **CIM \_ LANEndpoint**](cim-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="ec12e-120">Data type: **[**CIM\_LANEndpoint**](cim-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="ec12e-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ec12e-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec12e-122">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="ec12e-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="ec12e-123">Una referencia a una instancia de la clase [**MSVM \_ LANEndpoint**](cim-lanendpoint.md) que representa el SAP que está configurado para comunicarse o que se comunica activamente con el SAP antecedente.</span><span class="sxs-lookup"><span data-stu-id="ec12e-123">A reference to an instance of the [**Msvm\_LANEndpoint**](cim-lanendpoint.md) class that represents the SAP that is configured to communicate or is actively communicating with the antecedent SAP.</span></span> <span data-ttu-id="ec12e-124">En una conexión unidireccional, este SAP es el que está recibiendo.</span><span class="sxs-lookup"><span data-stu-id="ec12e-124">In an unidirectional connection, this SAP is the one that is receiving.</span></span>

</dd> <dt>

<span data-ttu-id="ec12e-125">**IsUnidirectional**</span><span class="sxs-lookup"><span data-stu-id="ec12e-125">**IsUnidirectional**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec12e-126">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="ec12e-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ec12e-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ec12e-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec12e-128">Si esta propiedad es **true**, esta conexión es unidireccional. de lo contrario, esta conexión es bidireccional.</span><span class="sxs-lookup"><span data-stu-id="ec12e-128">If this property is **True**, this connection is unidirectional; otherwise, this connection is bidirectional.</span></span> <span data-ttu-id="ec12e-129">Cuando una conexión es unidireccional, el "altavoz" debe definirse como referencia **antecedente** .</span><span class="sxs-lookup"><span data-stu-id="ec12e-129">When a connection is unidirectional, the "speaker" should be defined as the **Antecedent** reference.</span></span> <span data-ttu-id="ec12e-130">En una conexión bidireccional, no importa si el punto de acceso seleccionado es el **antecedente** o **dependiente**.</span><span class="sxs-lookup"><span data-stu-id="ec12e-130">In a bidirectional connection, it does not matter whether the selected access point is the **Antecedent** or **Dependent**.</span></span> <span data-ttu-id="ec12e-131">Esta propiedad se hereda de [**la \_ ActiveConnection de CIM**](/previous-versions//cc136779(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ec12e-131">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ec12e-132">**OtherTrafficDescription**</span><span class="sxs-lookup"><span data-stu-id="ec12e-132">**OtherTrafficDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec12e-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ec12e-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ec12e-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ec12e-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec12e-135">Esta propiedad se hereda de [**la \_ ActiveConnection de CIM**](/previous-versions//cc136779(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ec12e-135">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ec12e-136">**TrafficType**</span><span class="sxs-lookup"><span data-stu-id="ec12e-136">**TrafficType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec12e-137">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ec12e-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ec12e-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ec12e-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ec12e-139">Esta propiedad se hereda de [**la \_ ActiveConnection de CIM**](/previous-versions//cc136779(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="ec12e-139">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec12e-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ec12e-140">Remarks</span></span>

<span data-ttu-id="ec12e-141">El acceso a la clase **MSVM \_ ActiveConnection** podría estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="ec12e-141">Access to the **Msvm\_ActiveConnection** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ec12e-142">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ec12e-142">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="ec12e-143">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="ec12e-143">Examples</span></span>

<span data-ttu-id="ec12e-144">Consulte [consultar objetos de red](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ec12e-144">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec12e-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec12e-145">Requirements</span></span>



| <span data-ttu-id="ec12e-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec12e-146">Requirement</span></span> | <span data-ttu-id="ec12e-147">Value</span><span class="sxs-lookup"><span data-stu-id="ec12e-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec12e-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec12e-148">Minimum supported client</span></span><br/> | <span data-ttu-id="ec12e-149">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="ec12e-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ec12e-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec12e-150">Minimum supported server</span></span><br/> | <span data-ttu-id="ec12e-151">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="ec12e-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ec12e-152">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ec12e-152">Namespace</span></span><br/>                | <span data-ttu-id="ec12e-153">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ec12e-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ec12e-154">MOF</span><span class="sxs-lookup"><span data-stu-id="ec12e-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec12e-155"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ec12e-156">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ec12e-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec12e-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ec12e-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ec12e-158">Vea también</span><span class="sxs-lookup"><span data-stu-id="ec12e-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec12e-159">**ActiveConnection de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="ec12e-159">**CIM\_ActiveConnection**</span></span>](cim-activeconnection.md)
</dt> <dt>

<span data-ttu-id="ec12e-160">[**ActiveConnection de CIM \_**](/previous-versions//cc136779(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ec12e-160">[**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85))</span></span>
</dt> </dl>

 

