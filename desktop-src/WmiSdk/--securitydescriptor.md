---
description: Representa un descriptor de seguridad.
ms.assetid: 1ade1751-52a2-4ada-8255-323321111663
ms.tgt_platform: multiple
title: __SecurityDescriptor clase
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
ms.openlocfilehash: c248a437651396811f71c04e72dd8b209c5d10823f49d03abbe7e9d9ee6b6867
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110202"
---
# <a name="__securitydescriptor-class"></a>\_\_Clase SecurityDescriptor

La **\_ \_ clase del sistema abstracta SecurityDescriptor** representa un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly).

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

La **\_ \_ clase SecurityDescriptor** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase SecurityDescriptor** tiene estas propiedades.

<dl> <dt>

**ControlFlags**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Marcas de bits que proporcionan información sobre el contenido y el formato del descriptor. Consulte la **propiedad ControlFlags** en la [**clase \_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) para obtener una descripción de las marcas.

</dd> <dt>

**Dacl**
</dt> <dd> <dl> <dt>

Tipo de datos: **[**\_ \_ matriz ACE**](--ace.md)**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Matriz de [**\_ \_ entradas ACE**](--ace.md) que especifican el acceso al objeto .

</dd> <dt>

**Grupo**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

ACE que identifica al administrador de confianza que representa el grupo del objeto.

</dd> <dt>

**Propietario**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

ACE que identifica al administrador de confianza que representa al propietario del objeto.

</dd> <dt>

**Sacl**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de [**\_ \_ entradas ACE**](--ace.md) que identifica usuarios y grupos para los que se recopila información de auditoría.

</dd> <dt>

**HORA \_ CREADA**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Hora en el [formato \_ DATETIME de CIM](cim-datetime.md) en la que se creó el descriptor de seguridad.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta clase proporciona propiedades heredadas por [**Win32 \_ SecurityDescriptor.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) Para obtener más información, vea [Objetos descriptores de seguridad WMI y](wmi-security-descriptor-objects.md) Cambiar la seguridad de acceso en objetos [protegibles.](changing-access-security-on-securable-objects.md) Para obtener más información sobre las ACE, [vea Access Control Components](/windows/desktop/SecAuthZ/access-control-components).

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

[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Mantener la seguridad de WMI](maintaining-wmi-security.md)
</dt> </dl>

 

