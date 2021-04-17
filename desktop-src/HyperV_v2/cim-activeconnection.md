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
# <a name="cim_activeconnection-class"></a>\_Clase ActiveConnection de CIM

Define una conexión que está activada y configurada actualmente para proporcionar comunicación entre dos objetos **\_ punto de CIM** . **CIM \_ ActiveConnection** se utiliza cuando la conexión no se trata como un **objeto \_ ManagedElement de CIM** . Los puntos de acceso de servicio que están conectados mediante una conexión activa suelen estar en el mismo nivel de red o de aplicación.

## <a name="syntax"></a>Sintaxis

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

## <a name="members"></a>Miembros

La clase de **\_ ActiveConnection de CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase de **\_ ActiveConnection de CIM** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ punto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

El punto de acceso al servicio que está conectado al otro punto de acceso al servicio a través de la conexión activa. **CIM \_ Objeto punto** . En una conexión unidireccional, este punto de acceso es el que transmite los datos.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ punto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")
</dt> </dl>

El punto de acceso al servicio que está configurado para comunicarse o está comunicándose activamente con el punto de acceso al servicio especificado en la propiedad **antecedente** . En una conexión unidireccional, este punto de acceso es el que recibe los datos.

</dd> <dt>

**IsUnidirectional**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

True si la conexión es unidireccional; false si la conexión es bidireccional. Cuando la conexión es unidireccional, la propiedad **antecedente** especifica el punto de acceso que está transmitiendo datos. En una conexión bidireccional, el **antecedente** puede especificar cualquier punto de acceso asignado a la conexión.

</dd> <dt>

**OtherTrafficDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sin valor"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ ActiveConnection de CIM**.**TrafficType**")
</dt> </dl>

> [!Note]  
> Esta propiedad está desusada. En su lugar, se recomienda especificar esta información en el direccionamiento, el protocolo y la funcionalidad básica de los extremos.

 

Descripción del tipo de tráfico que se especifica cuando la propiedad **TrafficType** se establece en "1" (otro).

</dd> <dt>

**TrafficType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sin valor"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ ActiveConnection de CIM**.**OtherTrafficDescription**")
</dt> </dl>

> [!Note]  
> Esta propiedad está desusada. En su lugar, se recomienda especificar esta información en el direccionamiento, el protocolo y la funcionalidad básica de los extremos.

 

El tipo de tráfico que se transmite a través de esta conexión.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otro** (1)


</dt> <dd></dd> <dt>

<span id="Unicast"></span><span id="unicast"></span><span id="UNICAST"></span>

**Unidifusión** (2)


</dt> <dd></dd> <dt>

<span id="Broadcast"></span><span id="broadcast"></span><span id="BROADCAST"></span>

**Difusión** (3)


</dt> <dd></dd> <dt>

<span id="Multicast"></span><span id="multicast"></span><span id="MULTICAST"></span>

**Multidifusión** (4)


</dt> <dd></dd> <dt>

<span id="Anycast"></span><span id="anycast"></span><span id="ANYCAST"></span>

**Difusión por proximidad** (5)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_SAPSAPDEPENDENCY CIM**](cim-sapsapdependency.md)
</dt> </dl>

 

