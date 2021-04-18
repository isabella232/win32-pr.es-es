---
description: Representa una entrada en la base de datos de reenvío asociada a la \_ clase TransparentBridgingService de CIM.
ms.assetid: 4c3afe7c-f7e5-4a83-8ba1-f0b1909cee52
title: CIM_DynamicForwardingEntry (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DynamicForwardingEntry
- CIM_DynamicForwardingEntry.SystemCreationClassName
- CIM_DynamicForwardingEntry.SystemName
- CIM_DynamicForwardingEntry.ServiceCreationClassName
- CIM_DynamicForwardingEntry.ServiceName
- CIM_DynamicForwardingEntry.CreationClassName
- CIM_DynamicForwardingEntry.MACAddress
- CIM_DynamicForwardingEntry.DynamicStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65cf4f1bc5e678089d54dd99a09a6d3b7aeb3dfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687035"
---
# <a name="cim_dynamicforwardingentry-class"></a><span data-ttu-id="1082b-103">\_Clase DynamicForwardingEntry de CIM</span><span class="sxs-lookup"><span data-stu-id="1082b-103">CIM\_DynamicForwardingEntry class</span></span>

<span data-ttu-id="1082b-104">Representa una entrada en la base de datos de reenvío asociada a la clase [**\_ TransparentBridgingService de CIM**](cim-transparentbridgingservice.md) .</span><span class="sxs-lookup"><span data-stu-id="1082b-104">Represents an entry in the forwarding database associated with the [**CIM\_TransparentBridgingService**](cim-transparentbridgingservice.md) class.</span></span>

## <a name="syntax"></a><span data-ttu-id="1082b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1082b-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_DynamicForwardingEntry : CIM_LogicalElement
{
  string SystemCreationClassName;
  string SystemName;
  string ServiceCreationClassName;
  string ServiceName;
  string CreationClassName;
  string MACAddress;
  uint16 DynamicStatus;
};
```

## <a name="members"></a><span data-ttu-id="1082b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="1082b-106">Members</span></span>

<span data-ttu-id="1082b-107">La clase **CIM \_ DynamicForwardingEntry** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1082b-107">The **CIM\_DynamicForwardingEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="1082b-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1082b-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1082b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1082b-109">Properties</span></span>

<span data-ttu-id="1082b-110">La clase **CIM \_ DynamicForwardingEntry** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1082b-110">The **CIM\_DynamicForwardingEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1082b-111">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1082b-111">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1082b-112">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1082b-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1082b-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1082b-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1082b-114">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="1082b-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1082b-115">El nombre de la clase o la subclase utilizada para crear la instancia.</span><span class="sxs-lookup"><span data-stu-id="1082b-115">The name of the class or the subclass used to create the instance.</span></span> <span data-ttu-id="1082b-116">Cuando se usa con las otras propiedades de clave de esta clase, esta propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.</span><span class="sxs-lookup"><span data-stu-id="1082b-116">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="1082b-117">**DynamicStatus**</span><span class="sxs-lookup"><span data-stu-id="1082b-117">**DynamicStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1082b-118">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1082b-118">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1082b-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1082b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1082b-120">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Puente IETF-MIB. dot1dTpFdbStatus ")</span><span class="sxs-lookup"><span data-stu-id="1082b-120">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpFdbStatus")</span></span>
</dt> </dl>

<span data-ttu-id="1082b-121">Estado de la entrada.</span><span class="sxs-lookup"><span data-stu-id="1082b-121">The status of the entry.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1082b-122">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="1082b-122">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>

<span data-ttu-id="1082b-123">**No válido** (2)</span><span class="sxs-lookup"><span data-stu-id="1082b-123">**Invalid** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Learned"></span><span id="learned"></span><span id="LEARNED"></span>

<span data-ttu-id="1082b-124">**Aprendido** (3)</span><span class="sxs-lookup"><span data-stu-id="1082b-124">**Learned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Self"></span><span id="self"></span><span id="SELF"></span>

<span data-ttu-id="1082b-125">**Self** (4)</span><span class="sxs-lookup"><span data-stu-id="1082b-125">**Self** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Mgmt"></span><span id="mgmt"></span><span id="MGMT"></span>

<span data-ttu-id="1082b-126">**MGMT** (5)</span><span class="sxs-lookup"><span data-stu-id="1082b-126">**Mgmt** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1082b-127">**Mac**</span><span class="sxs-lookup"><span data-stu-id="1082b-127">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1082b-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1082b-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1082b-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1082b-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1082b-130">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Puente IETF-MIB. dot1dTpFdbAddress ")</span><span class="sxs-lookup"><span data-stu-id="1082b-130">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpFdbAddress")</span></span>
</dt> </dl>

<span data-ttu-id="1082b-131">Dirección MAC de unidifusión para la que el servicio de puente filtra la información.</span><span class="sxs-lookup"><span data-stu-id="1082b-131">The Unicast MAC address for which the bridging service filters information.</span></span> <span data-ttu-id="1082b-132">La dirección MAC tiene el formato de doce dígitos hexadecimales, como 010203040506, donde cada par representa uno de los seis octetos de la dirección MAC en orden de bits canónico según RFC 2469.</span><span class="sxs-lookup"><span data-stu-id="1082b-132">The MAC address is formatted as twelve hexadecimal digits, such as 010203040506, with each pair representing one of the six octets of the MAC address in canonical bit order according to RFC 2469.</span></span>

</dd> <dt>

<span data-ttu-id="1082b-133">**ServiceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1082b-133">**ServiceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1082b-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1082b-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1082b-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1082b-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1082b-136">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ servicio CIM**](cim-service.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="1082b-136">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Service**](cim-service.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="1082b-137">El valor de **CreationClassName** del objeto de servicio de ámbito.</span><span class="sxs-lookup"><span data-stu-id="1082b-137">The **CreationClassName** value of the scoping service object.</span></span>

</dd> <dt>

<span data-ttu-id="1082b-138">**ServiceName**</span><span class="sxs-lookup"><span data-stu-id="1082b-138">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1082b-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1082b-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1082b-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1082b-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1082b-141">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ servicio CIM**](cim-service.md).**Nombre**")</span><span class="sxs-lookup"><span data-stu-id="1082b-141">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Service**](cim-service.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="1082b-142">Nombre del servicio de ámbito.</span><span class="sxs-lookup"><span data-stu-id="1082b-142">The name of the scoping service.</span></span>

</dd> <dt>

<span data-ttu-id="1082b-143">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1082b-143">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1082b-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1082b-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1082b-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1082b-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1082b-146">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="1082b-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="1082b-147">El valor de **CreationClassName** del objeto del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="1082b-147">The **CreationClassName** value of the scoping system object.</span></span>

</dd> <dt>

<span data-ttu-id="1082b-148">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1082b-148">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1082b-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1082b-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1082b-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1082b-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1082b-151">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Nombre**")</span><span class="sxs-lookup"><span data-stu-id="1082b-151">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="1082b-152">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="1082b-152">The name of the scoping system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1082b-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1082b-153">Requirements</span></span>



| <span data-ttu-id="1082b-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="1082b-154">Requirement</span></span> | <span data-ttu-id="1082b-155">Value</span><span class="sxs-lookup"><span data-stu-id="1082b-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1082b-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1082b-156">Minimum supported client</span></span><br/> | <span data-ttu-id="1082b-157">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1082b-157">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="1082b-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1082b-158">Minimum supported server</span></span><br/> | <span data-ttu-id="1082b-159">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1082b-159">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="1082b-160">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1082b-160">Namespace</span></span><br/>                | <span data-ttu-id="1082b-161">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="1082b-161">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1082b-162">MOF</span><span class="sxs-lookup"><span data-stu-id="1082b-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1082b-163"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1082b-163"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1082b-164">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1082b-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1082b-165"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1082b-165"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1082b-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="1082b-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1082b-167">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="1082b-167">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

