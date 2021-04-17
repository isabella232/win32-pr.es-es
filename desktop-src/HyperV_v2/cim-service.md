---
description: Representa un elemento lógico que contiene información para representar y administrar la funcionalidad proporcionada por una característica de dispositivo o software.
ms.assetid: 0b2312da-433b-43d8-8d21-babab12a5b2c
title: CIM_Service (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service
- CIM_Service.SystemCreationClassName
- CIM_Service.SystemName
- CIM_Service.CreationClassName
- CIM_Service.Name
- CIM_Service.PrimaryOwnerName
- CIM_Service.PrimaryOwnerContact
- CIM_Service.StartMode
- CIM_Service.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b6ee3c51b6af50d77e94bb0a29bd1c8148cda8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666566"
---
# <a name="cim_service-class-hyper-v-management"></a>CIM_Service (clase, administración de Hyper-V)

Representa un elemento lógico que contiene información para representar y administrar la funcionalidad proporcionada por una característica de dispositivo o software. Un servicio es un objeto de uso general para configurar y administrar la implementación de la funcionalidad. no es la propia funcionalidad.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_Service : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  string  Name;
  string  PrimaryOwnerName;
  string  PrimaryOwnerContact;
  string  StartMode;
  boolean Started;
};
```

## <a name="members"></a>Miembros

La clase de **\_ servicio CIM** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase de **\_ servicio CIM** tiene estos métodos.



| Método                                           | Descripción                    |
|:-------------------------------------------------|:-------------------------------|
| [**StartService**](cim-service-startservice.md) | inicia el servicio.<br/> |
| [**StopService**](cim-service-stopservice.md)   | detiene el servicio.<br/>  |



 

### <a name="properties"></a>Propiedades

La clase de **\_ servicio CIM** tiene estas propiedades.

<dl> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nombre de clase utilizado para crear una instancia de esta clase. **CreationClassName** se combina con otras propiedades de clave de esta clase para identificar de forma única las instancias de esta clase y sus subclases.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificador único del servicio que indica la funcionalidad del servicio.

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información general de DMTF \| 001,4 ")
</dt> </dl>

Información de contacto del propietario principal del servicio.

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información general de DMTF \| 001,3 ")
</dt> </dl>

Nombre del propietario principal del servicio.

</dd> <dt>

**Iniciado**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

**true** si se ha iniciado el servicio; en caso contrario, **false**.

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**desusados**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) (**" \_ servicio CIM**.**EnabledDefault**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Esta propiedad está desusada. En su lugar, use la propiedad **EnabledDefault** que se hereda [**de \_ EnabledLogicalElement CIM**](cim-enabledlogicalelement.md).

> [!Note]  
> Descripción en desuso: indica si el servicio se inicia automáticamente (por ejemplo, por un sistema operativo) o solo se inicia después de la solicitud.

 

<dt>



 ("Automático")


</dt> <dd></dd> <dt>



 ("Manual")


</dt> <dd></dd> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**")
</dt> </dl>

Nombre de clase utilizado para crear una instancia del sistema que contiene el servicio. **SystemCreationClassName** se combina con otras propiedades clave de esta clase para identificar de forma única las instancias de esta clase y sus subclases.

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

[**\_ENABLEDLOGICALELEMENT CIM**](cim-enabledlogicalelement.md)
</dt> </dl>

 

