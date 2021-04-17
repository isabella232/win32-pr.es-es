---
description: Representa un conjunto de componentes que funcionan como una única entidad de nivel superior.
ms.assetid: 784cee32-e0ae-4632-8dac-e5110513f5c9
title: CIM_System (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_System
- CIM_System.CreationClassName
- CIM_System.Name
- CIM_System.NameFormat
- CIM_System.PrimaryOwnerName
- CIM_System.PrimaryOwnerContact
- CIM_System.Roles
- CIM_System.OtherIdentifyingInfo
- CIM_System.IdentifyingDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a51e56ad3e8f91200fbe5bc7e09ac2f14c4ee232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666911"
---
# <a name="cim_system-class-hyper-v-management"></a>CIM_System (clase, administración de Hyper-V)

Representa un conjunto de componentes que funcionan como una única entidad de nivel superior.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.15.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_System : CIM_EnabledLogicalElement
{
  string CreationClassName;
  string Name;
  string NameFormat;
  string PrimaryOwnerName;
  string PrimaryOwnerContact;
  string Roles[];
  string OtherIdentifyingInfo[];
  string IdentifyingDescriptions[];
};
```

## <a name="members"></a>Miembros

La **clase \_ del sistema CIM** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ del sistema CIM** tiene estas propiedades.

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

**IdentifyingDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ Sistema CIM**.**OtherIdentifyingInfo**")
</dt> </dl>

Una matriz que contiene descripciones de los valores de la propiedad **OtherIdentifyingInfo** . Los elementos de la matriz de **IdentifyingDescriptions** se corresponden con los elementos de la propiedad **IdentifyingDescriptions** .

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("nombre"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

La clave de esta instancia en un entorno empresarial.

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

La Convención de nomenclatura utilizada por la propiedad Name para asegurarse de que los valores de **nombre** son únicos.

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ Sistema CIM**.**IdentifyingDescriptions**")
</dt> </dl>

Una matriz que contiene un conjunto de datos adicionales, más allá de la información del nombre del sistema, que se puede usar para identificar un sistema informático.

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información general de DMTF \| 001,4 ")
</dt> </dl>

Una cadena que proporciona información sobre cómo se puede alcanzar el propietario del sistema principal (por ejemplo, el número de teléfono, la dirección de correo electrónico, etc.).

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Información general de DMTF \| 001,3 ")
</dt> </dl>

Nombre del usuario primario del sistema.

</dd> <dt>

**Roles**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Una matriz que contiene los roles que realiza el sistema en un entorno empresarial.

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

 

