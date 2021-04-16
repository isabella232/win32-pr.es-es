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
# <a name="msvm_fcactiveconnection-class"></a>MSVM \_ FcActiveConnection (clase)

Conecta un puerto del conmutador al punto de conexión Canal de fibra al que está conectado el puerto. La existencia de este objeto significa que el puerto del conmutador y el extremo de Canal de fibra están conectados activamente y que el puerto Canal de fibra asociado al extremo de Canal de fibra puede comunicarse con la red a través del puerto del conmutador.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

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

## <a name="members"></a>Miembros

La clase **MSVM \_ FcActiveConnection** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ FcActiveConnection** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **MSVM \_ FcEndpoint**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")
</dt> </dl>

Una referencia a una instancia de la clase [**MSVM \_ FcEndpoint**](msvm-fcendpoint.md) que representa el punto de acceso al servicio (SAP) que está configurado para comunicarse o se comunica activamente con el SAP dependiente. En una conexión unidireccional, este SAP es el que se está transmitiendo.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **MSVM \_ FcEndpoint**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")
</dt> </dl>

Una referencia a una instancia de la clase [**MSVM \_ FcEndpoint**](msvm-fcendpoint.md) que representa el SAP que está configurado para comunicarse o que se comunica activamente con el SAP antecedente. En una conexión unidireccional, este SAP es el que está recibiendo.

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

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

