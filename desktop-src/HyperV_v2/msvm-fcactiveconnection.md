---
description: Conecta un puerto de conmutador al punto de conexión Canal de fibra al que está conectado el puerto.
ms.assetid: e2762e0c-2f78-4159-a67c-31213e311072
title: Msvm_FcActiveConnection clase
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
ms.openlocfilehash: 892fcb386f7362c10d89dffb4b0695fe07f6fad02929402d1ac2206f75cbf08b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117994286"
---
# <a name="msvm_fcactiveconnection-class"></a>Clase FcActiveConnection de Msvm \_

Conecta un puerto de conmutador al punto de conexión Canal de fibra al que está conectado el puerto. La existencia de este objeto significa que el puerto del conmutador y el punto de conexión de Canal de fibra están conectados activamente y el puerto Canal de fibra asociado al punto de conexión de Canal de fibra puede comunicarse con la red a través del puerto del conmutador.

La sintaxis siguiente se Managed Object Format código (MOF) e incluye todas las propiedades heredadas.

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

La **clase \_ FcActiveConnection de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ FcActiveConnection de Msvm** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Msvm \_ FcEndpoint**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

Referencia a una instancia de la clase [**\_ FcEndpoint de Msvm**](msvm-fcendpoint.md) que representa el punto de acceso de servicio (SAP) configurado para comunicarse o que se está comunicando activamente con el SAP dependiente. En una conexión unidireccional, este SAP es el que transmite.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Msvm \_ FcEndpoint**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidar**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

Referencia a una instancia de la clase [**\_ FcEndpoint de Msvm**](msvm-fcendpoint.md) que representa el SAP configurado para comunicarse o que se está comunicando activamente con el SAP anterior. En una conexión unidireccional, este SAP es el que recibe.

</dd> <dt>

**IsUnidirectional**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Si esta propiedad es **True**, esta conexión es unidireccional; de lo contrario, esta conexión es bidireccional. Cuando una conexión es unidireccional, el "hablante" debe definirse como la **referencia anterior.** En una conexión bidireccional, no importa si el punto de acceso seleccionado es el antecedente **o** **dependiente.** Esta propiedad se hereda de [**CIM \_ ActiveConnection.**](/previous-versions//cc136779(v=vs.85))

</dd> <dt>

**OtherTrafficDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda de [**CIM \_ ActiveConnection,**](/previous-versions//cc136779(v=vs.85))pero no se usa.

</dd> <dt>

**TrafficType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda de [**CIM \_ ActiveConnection,**](/previous-versions//cc136779(v=vs.85))pero no se usa.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

