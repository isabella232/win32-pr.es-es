---
description: Representa una entrada de control de acceso (ACE).
ms.assetid: 47daffd0-b9db-4367-b0b8-654a2da30fed
ms.tgt_platform: multiple
title: __ACE clase
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967192"
---
# <a name="__ace-class"></a>\_\_Ace (clase)

La **\_ \_ clase abstracta** del sistema ACE representa una entrada de control de acceso [*(ACE).*](/windows/desktop/SecGloss/a-gly)

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

## <a name="members"></a>Members

La **\_ \_ clase ACE** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase ACE** tiene estas propiedades.

<dl> <dt>

**Máscara de acceso**
</dt> <dd> <dl> <dt>

Tipo de datos: 
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Marcas de bits que representan derechos concedidos o denegados al administrador de confianza. Para obtener más información y una descripción de las marcas, vea **Propiedad AccessMask** en la [**clase \_ ACE de Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)

</dd> <dt>

**AceFlags**
</dt> <dd> <dl> <dt>

Tipo de datos: 
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Marcas de bits que especifican la herencia de la ACE. Para obtener más información y una descripción de las marcas, vea La propiedad **AceFlags** en la [**clase \_ ACE de Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)

</dd> <dt>

**AceType**
</dt> <dd> <dl> <dt>

Tipo de datos: 
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Tipo de entrada ACE que representa esta instancia.

</dd> <dt>

**GuidInheritedObjectType**
</dt> <dd> <dl> <dt>

Tipo de datos: 
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

GUID del elemento primario del objeto al que se aplican los derechos de acceso en la **propiedad AccessMask.**

</dd> <dt>

**GuidObjectType**
</dt> <dd> <dl> <dt>

Tipo de datos: 
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

GUID que indica el tipo de objeto al que se aplican los derechos de la propiedad **AccessMask.**

</dd> <dt>

**HORA \_ CREADA**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Hora, en formato [ \_ CIM DATETIME,](cim-datetime.md) en la que se creó el descriptor de seguridad.

</dd> <dt>

**Fideicomisario**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **\_ \_ Administrador de confianza**](--trustee.md)**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Administrador de confianza de la entrada ace representada por esta instancia de la **\_ \_ clase ACE.**

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta clase proporciona las propiedades heredadas por la clase [**\_ ACE de Win32,**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) que es miembro de la clase [**\_ SecurityDescriptor de Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) Para obtener más información, vea [Objetos de descriptor de seguridad WMI](wmi-security-descriptor-objects.md) y Cambiar la seguridad de acceso en objetos [protegibles.](changing-access-security-on-securable-objects.md) Para obtener más información sobre las ACE, [vea Access Control Components](/windows/desktop/SecAuthZ/access-control-components).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**\_\_SecurityRelatedClass**](--securityrelatedclass.md)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[Mantenimiento de la seguridad wmi](maintaining-wmi-security.md)
</dt> </dl>

 

