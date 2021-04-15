---
description: Representa una entrada de control de acceso (ACE).
ms.assetid: 47daffd0-b9db-4367-b0b8-654a2da30fed
ms.tgt_platform: multiple
title: __ACE (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ACE
- All
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
ms.openlocfilehash: ea2a765225145ce3d44e0aff89aeaca0a7563e0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498070"
---
# <a name="__ace-class"></a>\_\_ACE (clase)

La clase **\_ \_ ACE** Abstract System representa una entrada de control de acceso ([*ACE*](/windows/desktop/SecGloss/a-gly)).

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class  __ACE : __SecurityRelatedClass
{
            AceFlags;
            AccessMask;
            AceType;
            GuidInheritedObjectType;
            GuidObjectType;
  uint64    TIME_CREATED;
  __Trustee Trustee;
};
```

## <a name="members"></a>Miembros

La clase **\_ \_ ACE** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ ACE** tiene estas propiedades.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Tipo de datos: 
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Marcas de bits que representan derechos que se conceden o deniegan al administrador de confianza. Para obtener más información y una descripción de las marcas, consulte propiedad **AccessMask** en la clase [**\_ ACE de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .

</dd> <dt>

**AceFlags**
</dt> <dd> <dl> <dt>

Tipo de datos: 
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Marcas de bits que especifican la herencia de la ACE. Para obtener más información y una descripción de las marcas, consulte la propiedad **AceFlags** en la clase [**\_ ACE de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .

</dd> <dt>

**AceType**
</dt> <dd> <dl> <dt>

Tipo de datos: 
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Tipo de entrada ACE que representa esta instancia.

</dd> <dt>

**GuidInheritedObjectType**
</dt> <dd> <dl> <dt>

Tipo de datos: 
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

GUID del objeto primario del objeto al que se aplican los derechos de acceso en la propiedad **AccessMask** .

</dd> <dt>

**GuidObjectType**
</dt> <dd> <dl> <dt>

Tipo de datos: 
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

GUID que indica el tipo de objeto al que se aplican los derechos de la propiedad **AccessMask** .

</dd> <dt>

**HORA de \_ creación**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La hora, en el formato de [ \_ fecha y](cim-datetime.md) hora de CIM, cuando se creó el descriptor de seguridad.

</dd> <dt>

**Confianza**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **\_ \_ Administrador de confianza**](--trustee.md)**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Administrador de confianza de la entrada ACE representada por esta instancia de la clase **\_ \_ ACE** .

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta clase proporciona las propiedades que hereda la clase [**\_ ACE de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) , que es miembro de la clase [**\_ SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) . Para obtener más información, vea [objetos de descriptor de seguridad de WMI](wmi-security-descriptor-objects.md) y cambiar la [seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md). Para obtener más información sobre las ACE, vea [componentes de Access Control](/windows/desktop/SecAuthZ/access-control-components).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_SecurityRelatedClass**](--securityrelatedclass.md)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**ACE de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[Mantenimiento de la seguridad de WMI](maintaining-wmi-security.md)
</dt> </dl>

 

