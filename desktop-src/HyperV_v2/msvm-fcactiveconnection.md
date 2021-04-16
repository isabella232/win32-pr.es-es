---
description: Conecta un puerto del conmutador al punto de conexión Canal de fibra al que está conectado el puerto.
ms.assetid: e2762e0c-2f78-4159-a67c-31213e311072
title: Msvm_FcActiveConnection (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcActiveConnection
- Msvm_FcActiveConnection.Antecedent
- Msvm_FcActiveConnection.Dependent
- Msvm_FcActiveConnection.TrafficType
- Msvm_FcActiveConnection.OtherTrafficDescription
- Msvm_FcActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e29330e073266f2f2a8749ec3c70d9e26b35ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686960"
---
# <a name="msvm_fcactiveconnection-class"></a><span data-ttu-id="f6429-103">MSVM \_ FcActiveConnection (clase)</span><span class="sxs-lookup"><span data-stu-id="f6429-103">Msvm\_FcActiveConnection class</span></span>

<span data-ttu-id="f6429-104">Conecta un puerto del conmutador al punto de conexión Canal de fibra al que está conectado el puerto.</span><span class="sxs-lookup"><span data-stu-id="f6429-104">Connects a switch port to the Fibre Channel endpoint to which the port is connected.</span></span> <span data-ttu-id="f6429-105">La existencia de este objeto significa que el puerto del conmutador y el extremo de Canal de fibra están conectados activamente y que el puerto Canal de fibra asociado al extremo de Canal de fibra puede comunicarse con la red a través del puerto del conmutador.</span><span class="sxs-lookup"><span data-stu-id="f6429-105">The existence of this object means that the switch port and the Fibre Channel endpoint are actively connected, and the Fibre Channel port associated with the Fibre Channel endpoint can communicate with the network through the switch port.</span></span>

<span data-ttu-id="f6429-106">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f6429-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6429-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6429-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcActiveConnection : CIM_ActiveConnection
{
  Msvm_FcEndpoint REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
  uint16              TrafficType;
  string              OtherTrafficDescription;
  boolean             IsUnidirectional;
};
```

## <a name="members"></a><span data-ttu-id="f6429-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="f6429-108">Members</span></span>

<span data-ttu-id="f6429-109">La clase **MSVM \_ FcActiveConnection** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f6429-109">The **Msvm\_FcActiveConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="f6429-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6429-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f6429-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6429-111">Properties</span></span>

<span data-ttu-id="f6429-112">La clase **MSVM \_ FcActiveConnection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f6429-112">The **Msvm\_FcActiveConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f6429-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="f6429-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6429-114">Tipo de datos: **MSVM \_ FcEndpoint**</span><span class="sxs-lookup"><span data-stu-id="f6429-114">Data type: **Msvm\_FcEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="f6429-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6429-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6429-116">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="f6429-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="f6429-117">Una referencia a una instancia de la clase [**MSVM \_ FcEndpoint**](msvm-fcendpoint.md) que representa el punto de acceso al servicio (SAP) que está configurado para comunicarse o se comunica activamente con el SAP dependiente.</span><span class="sxs-lookup"><span data-stu-id="f6429-117">A reference to an instance of the [**Msvm\_FcEndpoint**](msvm-fcendpoint.md) class that represents the service access point (SAP) that is configured to communicate or is actively communicating with the dependent SAP.</span></span> <span data-ttu-id="f6429-118">En una conexión unidireccional, este SAP es el que se está transmitiendo.</span><span class="sxs-lookup"><span data-stu-id="f6429-118">In a unidirectional connection, this SAP is the one that is transmitting.</span></span>

</dd> <dt>

<span data-ttu-id="f6429-119">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="f6429-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6429-120">Tipo de datos: **MSVM \_ FcEndpoint**</span><span class="sxs-lookup"><span data-stu-id="f6429-120">Data type: **Msvm\_FcEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="f6429-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6429-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6429-122">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="f6429-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="f6429-123">Una referencia a una instancia de la clase [**MSVM \_ FcEndpoint**](msvm-fcendpoint.md) que representa el SAP que está configurado para comunicarse o que se comunica activamente con el SAP antecedente.</span><span class="sxs-lookup"><span data-stu-id="f6429-123">A reference to an instance of the [**Msvm\_FcEndpoint**](msvm-fcendpoint.md) class that represents the SAP that is configured to communicate or is actively communicating with the antecedent SAP.</span></span> <span data-ttu-id="f6429-124">En una conexión unidireccional, este SAP es el que está recibiendo.</span><span class="sxs-lookup"><span data-stu-id="f6429-124">In a unidirectional connection, this SAP is the one that is receiving.</span></span>

</dd> <dt>

<span data-ttu-id="f6429-125">**IsUnidirectional**</span><span class="sxs-lookup"><span data-stu-id="f6429-125">**IsUnidirectional**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6429-126">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f6429-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6429-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6429-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6429-128">Si esta propiedad es **true**, esta conexión es unidireccional. de lo contrario, esta conexión es bidireccional.</span><span class="sxs-lookup"><span data-stu-id="f6429-128">If this property is **True**, this connection is unidirectional; otherwise, this connection is bidirectional.</span></span> <span data-ttu-id="f6429-129">Cuando una conexión es unidireccional, el "altavoz" debe definirse como referencia **antecedente** .</span><span class="sxs-lookup"><span data-stu-id="f6429-129">When a connection is unidirectional, the "speaker" should be defined as the **Antecedent** reference.</span></span> <span data-ttu-id="f6429-130">En una conexión bidireccional, no importa si el punto de acceso seleccionado es el **antecedente** o **dependiente**.</span><span class="sxs-lookup"><span data-stu-id="f6429-130">In a bidirectional connection, it does not matter whether the selected access point is the **Antecedent** or **Dependent**.</span></span> <span data-ttu-id="f6429-131">Esta propiedad se hereda de [**la \_ ActiveConnection de CIM**](/previous-versions//cc136779(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f6429-131">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f6429-132">**OtherTrafficDescription**</span><span class="sxs-lookup"><span data-stu-id="f6429-132">**OtherTrafficDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6429-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6429-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6429-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6429-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6429-135">Esta propiedad se hereda de [**la \_ ActiveConnection de CIM**](/previous-versions//cc136779(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="f6429-135">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="f6429-136">**TrafficType**</span><span class="sxs-lookup"><span data-stu-id="f6429-136">**TrafficType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6429-137">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6429-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6429-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6429-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6429-139">Esta propiedad se hereda de [**la \_ ActiveConnection de CIM**](/previous-versions//cc136779(v=vs.85)), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="f6429-139">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6429-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6429-140">Requirements</span></span>



| <span data-ttu-id="f6429-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6429-141">Requirement</span></span> | <span data-ttu-id="f6429-142">Value</span><span class="sxs-lookup"><span data-stu-id="f6429-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6429-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6429-143">Minimum supported client</span></span><br/> | <span data-ttu-id="f6429-144">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6429-144">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f6429-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6429-145">Minimum supported server</span></span><br/> | <span data-ttu-id="f6429-146">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6429-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f6429-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f6429-147">Namespace</span></span><br/>                | <span data-ttu-id="f6429-148">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f6429-148">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f6429-149">MOF</span><span class="sxs-lookup"><span data-stu-id="f6429-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6429-150"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6429-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6429-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f6429-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6429-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f6429-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

