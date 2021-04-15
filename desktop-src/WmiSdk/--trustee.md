---
description: La \_ \_ clase de sistema abstracta de administrador de confianza representa un administrador de confianza. Se puede usar un nombre o un SID (matriz de bytes).
ms.assetid: 92d17c7c-ebca-4dd0-80d8-6edd999ca394
ms.tgt_platform: multiple
title: __Trustee (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Trustee
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 5c6ba04760e924ffe9d86916cffdb82ea2488219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547182"
---
# <a name="__trustee-class"></a>\_\_Trustee (clase)

La clase de sistema abstracta de [**\_ \_ Administrador de confianza**](--securitydescriptor.md) representa un administrador de [*confianza*](/windows/desktop/SecGloss/t-gly). Se puede usar un nombre o un SID (matriz de bytes).

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __Trustee
{
  string Domain;
  string Name;
  uint8  SID[];
  uint32 SidLength;
  string SidString;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Miembros

La clase **\_ \_ Trustee** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ Trustee** tiene estas propiedades.

<dl> <dt>

**Dominio**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Parte del dominio de la cuenta.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Parte del nombre de la cuenta.

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

El SID del administrador de confianza en el formato de la matriz de bytes binaria.

</dd> <dt>

**SidLength**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Longitud del SID en bytes.

</dd> <dt>

**SidString**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

SID del administrador de confianza en el formato de cadena, por ejemplo, "S-1-1-0".

</dd> <dt>

**HORA de \_ creación**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Hora en el formato de [ \_ fecha y](cim-datetime.md) hora de CIM cuando se creó el descriptor de seguridad.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta clase proporciona propiedades heredadas por la clase [**de \_ Administrador de confianza de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) , que es miembro de la clase [**\_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) . Para obtener más información, vea [objetos de descriptor de seguridad de WMI](wmi-security-descriptor-objects.md) y cambiar la [seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md). Para obtener más información sobre las ACE, vea [componentes de Access Control](/windows/desktop/SecAuthZ/access-control-components).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**Administrador de confianza de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
</dt> <dt>

[Mantenimiento de la seguridad de WMI](maintaining-wmi-security.md)
</dt> </dl>

 

