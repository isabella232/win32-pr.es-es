---
description: La \_ \_ clase de sistema abstracta Trustee representa a un administrador de confianza. Se puede usar un nombre o un SID (matriz de bytes).
ms.assetid: 92d17c7c-ebca-4dd0-80d8-6edd999ca394
ms.tgt_platform: multiple
title: __Trustee clase
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
ms.openlocfilehash: ac1e80bceb3dc584a22e342780bbf32660276868e473ff33ff01d6c2ad65d504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131958"
---
# <a name="__trustee-class"></a>\_\_Clase de administrador de confianza

La clase de sistema [**\_ \_ abstracta Trustee**](--securitydescriptor.md) representa a un [*administrador de confianza.*](/windows/desktop/SecGloss/t-gly) Se puede usar un nombre o un SID (matriz de bytes).

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

La **\_ \_ clase Trustee** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase Trustee** tiene estas propiedades.

<dl> <dt>

**Dominio**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Parte de dominio de la cuenta.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Nombre de la parte de la cuenta.

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

SID del administrador de confianza en el formato de matriz de bytes binarios.

</dd> <dt>

**SidLength**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Longitud del SID en bytes.

</dd> <dt>

**SidString**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

SID del administrador de confianza en formato de cadena, por ejemplo, "S-1-1-0".

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

Esta clase proporciona propiedades heredadas por la clase De confianza de [**\_ Win32,**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) que es miembro de la clase [**\_ SecurityDescriptor de Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) Para obtener más información, vea [Objetos descriptores de seguridad WMI y](wmi-security-descriptor-objects.md) Cambiar la seguridad de acceso en objetos [protegibles.](changing-access-security-on-securable-objects.md) Para obtener más información sobre las ACE, [vea Access Control Components](/windows/desktop/SecAuthZ/access-control-components).

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

[**Administrador de \_ Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
</dt> <dt>

[Mantener la seguridad de WMI](maintaining-wmi-security.md)
</dt> </dl>

 

