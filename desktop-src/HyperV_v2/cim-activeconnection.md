---
description: Define una conexión que está activada y configurada actualmente para proporcionar comunicación entre dos objetos \_ ServiceAccessPoint de CIM.
ms.assetid: 03f8e43f-a77b-46e2-bb7d-c29758c65aee
title: CIM_ActiveConnection clase
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
ms.openlocfilehash: a2961779744e90d0e4281e53c3d78c92081993027deb6c435846abbffb41b110
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041765"
---
# <a name="cim_activeconnection-class"></a>Cim \_ ActiveConnection (clase)

Define una conexión que está activada y configurada actualmente para proporcionar comunicación entre dos objetos **\_ ServiceAccessPoint de CIM.** **CIM \_ ActiveConnection** se usa cuando la conexión no se trata como un **objeto \_ ManagedElement de CIM.** Los puntos de acceso de servicio conectados por una conexión activa suelen estar en la misma capa de red o aplicación.

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

La **clase \_ ActiveConnection** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ActiveConnection** de CIM tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cim \_ ServiceAccessPoint**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

Punto de acceso de servicio que está conectado al otro punto de acceso de servicio a través de la conexión activa. **CIM \_ Objeto ServiceAccessPoint.** En una conexión unidireccional, este punto de acceso es el que transmite datos.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cim \_ ServiceAccessPoint**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidar**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

Punto de acceso de servicio configurado para comunicarse o que se comunica activamente con el punto de acceso de servicio especificado en la **propiedad Antecedente.** En una conexión unidireccional, este punto de acceso es el que recibe datos.

</dd> <dt>

**IsUnidirectional**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

True si la conexión es unidireccional; false si la conexión es bidireccional. Cuando la conexión es unidireccional, la **propiedad Antecedente** especifica el punto de acceso que transmite los datos. En una conexión bidireccional, **Antecedent** puede especificar cualquier punto de acceso asignado a la conexión.

</dd> <dt>

**OtherTrafficDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**En desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Sin valor"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ActiveConnection**.**TrafficType**")
</dt> </dl>

> [!Note]  
> Esta propiedad está desusada. En su lugar, se recomienda especificar esta información en el direccionamiento, el protocolo y la funcionalidad básica de los puntos de conexión.

 

Descripción del tipo de tráfico que se especifica cuando la **propiedad TrafficType** se establece en "1" (Otros).

</dd> <dt>

**TrafficType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**En desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Sin valor"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ActiveConnection**.**OtherTrafficDescription**")
</dt> </dl>

> [!Note]  
> Esta propiedad está desusada. En su lugar, se recomienda especificar esta información en el direccionamiento, el protocolo y la funcionalidad básica de los puntos de conexión.

 

Tipo de tráfico que se transmite a través de esta conexión.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


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

**Anycast** (5)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ SAPSAPDependency**](cim-sapsapdependency.md)
</dt> </dl>

 

