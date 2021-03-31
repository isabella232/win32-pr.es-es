---
description: Representa un descriptor de seguridad.
ms.assetid: 1ade1751-52a2-4ada-8255-323321111663
ms.tgt_platform: multiple
title: __SecurityDescriptor (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SecurityDescriptor
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
ms.openlocfilehash: 5f305387a29d1d1569addafd127f53c98246e1a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277128"
---
# <a name="__securitydescriptor-class"></a>\_\_SecurityDescriptor (clase)

La clase del sistema de Resumen de **\_ \_ SecurityDescriptor** representa un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly).

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __SecurityDescriptor
{
  uint32 ControlFlags;
  __ACE  DACL[];
  __ACE  Group;
  __ACE  Owner;
  __ACE  SACL;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Miembros

La clase **\_ \_ SecurityDescriptor** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ SecurityDescriptor** tiene estas propiedades.

<dl> <dt>

**ControlFlags**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Marcas de bits que proporcionan información sobre el contenido y el formato del descriptor. Vea la propiedad **ControlFlags** de la [**clase \_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) para obtener una descripción de las marcas.

</dd> <dt>

**DACL**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **[**\_ \_ ACE**](--ace.md)**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Matriz de entradas [**\_ \_ ACE**](--ace.md) que especifican el acceso al objeto.

</dd> <dt>

**Grupo**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

ACE que identifica el administrador de confianza que representa el grupo del objeto.

</dd> <dt>

**Propietario**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

ACE que identifica el administrador de confianza que representa el propietario del objeto.

</dd> <dt>

**SACL**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de entradas [**\_ \_ ACE**](--ace.md) que identifica los usuarios y los grupos para los que se recopila información de auditoría.

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

Esta clase proporciona propiedades heredadas por el [**\_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor). Para obtener más información, vea [objetos de descriptor de seguridad de WMI](wmi-security-descriptor-objects.md) y cambiar la [seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md). Para obtener más información sobre las ACE, vea [componentes de Access Control](/windows/desktop/SecAuthZ/access-control-components).

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

[**SecurityDescriptor de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Mantenimiento de la seguridad de WMI](maintaining-wmi-security.md)
</dt> </dl>

 

