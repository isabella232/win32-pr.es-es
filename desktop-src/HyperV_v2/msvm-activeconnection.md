---
description: Conecta un puerto de conmutador al punto de conexión de LAN al que está conectado el puerto.
ms.assetid: 963EC004-6A67-4F75-BD93-1BCD17F32490
title: Msvm_ActiveConnection clase
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
ms.openlocfilehash: 2f8326fe50d3fef4e7776fa865afdd730416cb38fccd6347b4b27f0079966501
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693615"
---
# <a name="msvm_activeconnection-class"></a>Clase ActiveConnection de Msvm \_

Conecta un puerto de conmutador al punto de conexión de LAN al que está conectado el puerto. La existencia de este objeto significa que el puerto del conmutador y el punto de conexión LAN están conectados activamente y el puerto Ethernet asociado al punto de conexión LAN puede comunicarse con la red a través del puerto del conmutador.

La sintaxis siguiente se Managed Object Format código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

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

La **clase \_ ActiveConnection de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ActiveConnection de Msvm** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Msvm \_ LANEndpoint**](msvm-lanendpoint.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

Referencia a una instancia de la clase [**\_ Msvm LANEndpoint**](msvm-lanendpoint.md) que representa el punto de acceso de servicio (SAP) configurado para comunicarse o que se comunica activamente con el SAP dependiente. En una conexión unidireccional, este SAP es el que transmite.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ LANEndpoint**](cim-lanendpoint.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

Referencia a una instancia de la clase [**\_ Msvm LANEndpoint**](cim-lanendpoint.md) que representa el SAP configurado para comunicarse o que se está comunicando activamente con el SAP anterior. En una conexión unidireccional, este SAP es el que recibe.

</dd> <dt>

**IsUnidirectional**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si esta propiedad es **True**, esta conexión es unidireccional; De lo contrario, esta conexión es bidireccional. Cuando una conexión es unidireccional, el "hablante" debe definirse como referencia **anterior.** En una conexión bidireccional, no importa si el punto de acceso seleccionado es el **antecedente** o **dependiente.** Esta propiedad se hereda de [**CIM \_ ActiveConnection.**](/previous-versions//cc136779(v=vs.85))

</dd> <dt>

**OtherTrafficDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda de [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)), pero no se usa.

</dd> <dt>

**TrafficType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda de [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)), pero no se usa.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a **la clase \_ ActiveConnection de Msvm** podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Ejemplos

Consulte [Consulta de objetos de red.](querying-networking-objects.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ ActiveConnection**](cim-activeconnection.md)
</dt> <dt>

[**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))
</dt> </dl>

 

