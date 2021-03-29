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
# <a name="msvm_activeconnection-class"></a>MSVM ( \_ clase de ActiveConnection)

Conecta un puerto del conmutador al punto de conexión de LAN al que está conectado el puerto. La existencia de este objeto significa que el puerto del conmutador y el punto de conexión de LAN están conectados activamente y el puerto Ethernet asociado al punto de conexión de LAN puede comunicarse con la red a través del puerto del conmutador.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

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

## <a name="members"></a>Miembros

La clase **MSVM \_ ActiveConnection** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ ActiveConnection** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **MSVM \_ LANEndpoint**](msvm-lanendpoint.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Una referencia a una instancia de la clase [**MSVM \_ LANEndpoint**](msvm-lanendpoint.md) que representa el punto de acceso al servicio (SAP) que está configurado para comunicarse o se comunica activamente con el SAP dependiente. En una conexión unidireccional, este SAP es el que se está transmitiendo.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ LANEndpoint**](cim-lanendpoint.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")
</dt> </dl>

Una referencia a una instancia de la clase [**MSVM \_ LANEndpoint**](cim-lanendpoint.md) que representa el SAP que está configurado para comunicarse o que se comunica activamente con el SAP antecedente. En una conexión unidireccional, este SAP es el que está recibiendo.

</dd> <dt>

**IsUnidirectional**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si esta propiedad es **true**, esta conexión es unidireccional. de lo contrario, esta conexión es bidireccional. Cuando una conexión es unidireccional, el "altavoz" debe definirse como referencia **antecedente** . En una conexión bidireccional, no importa si el punto de acceso seleccionado es el **antecedente** o **dependiente**. Esta propiedad se hereda de [**la \_ ActiveConnection de CIM**](/previous-versions//cc136779(v=vs.85)).

</dd> <dt>

**OtherTrafficDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda de [**la \_ ActiveConnection de CIM**](/previous-versions//cc136779(v=vs.85)), pero no se usa.

</dd> <dt>

**TrafficType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda de [**la \_ ActiveConnection de CIM**](/previous-versions//cc136779(v=vs.85)), pero no se usa.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la clase **MSVM \_ ActiveConnection** podría estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Ejemplos

Consulte [consultar objetos de red](querying-networking-objects.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ActiveConnection de CIM \_**](cim-activeconnection.md)
</dt> <dt>

[**ActiveConnection de CIM \_**](/previous-versions//cc136779(v=vs.85))
</dt> </dl>

 

