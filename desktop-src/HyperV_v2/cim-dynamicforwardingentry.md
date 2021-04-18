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
# <a name="cim_dynamicforwardingentry-class"></a>\_Clase DynamicForwardingEntry de CIM

Representa una entrada en la base de datos de reenvío asociada a la clase [**\_ TransparentBridgingService de CIM**](cim-transparentbridgingservice.md) .

## <a name="syntax"></a>Sintaxis

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

## <a name="members"></a>Miembros

La clase **CIM \_ DynamicForwardingEntry** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ DynamicForwardingEntry** tiene estas propiedades.

<dl> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

El nombre de la clase o la subclase utilizada para crear la instancia. Cuando se usa con las otras propiedades de clave de esta clase, esta propiedad permite que todas las instancias de esta clase y sus subclases se identifiquen de forma única.

</dd> <dt>

**DynamicStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Puente IETF-MIB. dot1dTpFdbStatus ")
</dt> </dl>

Estado de la entrada.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otro** (1)


</dt> <dd></dd> <dt>

<span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>

**No válido** (2)


</dt> <dd></dd> <dt>

<span id="Learned"></span><span id="learned"></span><span id="LEARNED"></span>

**Aprendido** (3)


</dt> <dd></dd> <dt>

<span id="Self"></span><span id="self"></span><span id="SELF"></span>

**Self** (4)


</dt> <dd></dd> <dt>

<span id="Mgmt"></span><span id="mgmt"></span><span id="MGMT"></span>

**MGMT** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**Mac**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (12), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Puente IETF-MIB. dot1dTpFdbAddress ")
</dt> </dl>

Dirección MAC de unidifusión para la que el servicio de puente filtra la información. La dirección MAC tiene el formato de doce dígitos hexadecimales, como 010203040506, donde cada par representa uno de los seis octetos de la dirección MAC en orden de bits canónico según RFC 2469.

</dd> <dt>

**ServiceCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ servicio CIM**](cim-service.md).**CreationClassName**")
</dt> </dl>

El valor de **CreationClassName** del objeto de servicio de ámbito.

</dd> <dt>

**ServiceName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ servicio CIM**](cim-service.md).**Nombre**")
</dt> </dl>

Nombre del servicio de ámbito.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**")
</dt> </dl>

El valor de **CreationClassName** del objeto del sistema de ámbito.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Nombre**")
</dt> </dl>

Nombre del sistema de ámbito.

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

[**\_LOGICALELEMENT CIM**](cim-logicalelement.md)
</dt> </dl>

 

