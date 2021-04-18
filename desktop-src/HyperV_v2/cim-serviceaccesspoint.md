---
description: Representa un punto de acceso al servicio (SAP), que puede utilizarse o invocar un servicio. SAP indica que un servicio está disponible para que lo usen otras entidades.
ms.assetid: 09349c95-3f7e-46c5-bea1-c3d14ee16a2a
title: CIM_ServiceAccessPoint (clase, administración de Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAccessPoint
- CIM_ServiceAccessPoint.SystemCreationClassName
- CIM_ServiceAccessPoint.SystemName
- CIM_ServiceAccessPoint.CreationClassName
- CIM_ServiceAccessPoint.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e3e27fc667c55cd101b06a34f9140cb9eed8923f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686900"
---
# <a name="cim_serviceaccesspoint-class-hyper-v-management"></a>CIM_ServiceAccessPoint (clase, administración de Hyper-V)

Representa un punto de acceso al servicio (SAP), que puede utilizarse o invocar un servicio. SAP indica que un servicio está disponible para que lo usen otras entidades.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ServiceAccessPoint : CIM_EnabledLogicalElement
{
  string SystemCreationClassName;
  string SystemName;
  string CreationClassName;
  string Name;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ punto** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ punto** tiene estas propiedades.

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

El nombre único de SAP que indica las características admitidas por SAP.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**CreationClassName**")
</dt> </dl>

Nombre de clase que se usa para crear una instancia del sistema que contiene SAP. **SystemCreationClassName** se combina con otras propiedades clave de esta clase para identificar de forma única las instancias de esta clase y sus subclases.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ Sistema CIM**](cim-system.md).**Nombre**")
</dt> </dl>

Nombre del sistema que contiene SAP.

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

 

