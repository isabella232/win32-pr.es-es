---
description: Controla el acceso remoto a versiones no admitidas de Windows.
ms.assetid: eb326bba-a011-4b9c-b4ee-fc08ae364f6f
ms.tgt_platform: multiple
title: __NTLMUser9X clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NTLMUser9X
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 2d05920b0936e8ff4de3eb338938e03e92edb4596efbf01f1064b6952a7df661
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320583"
---
# <a name="__ntlmuser9x-class"></a>\_\_NTLMUser9X (clase)

La **\_ \_ clase del sistema NTLMUser9X** controla el acceso remoto a versiones no admitidas de Windows. La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __NTLMUser9X : __SecurityRelatedClass
{
  string Authority;
  sint32 Flags;
  sint32 Mask;
  string Name;
  sint32 Type;
};
```

## <a name="members"></a>Miembros

La **\_ \_ clase NTLMUser9X** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase NTLMUser9X** tiene estas propiedades.

<dl> <dt>

**Autoridad**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Dominio al que se aplica un nombre de usuario.

</dd> <dt>

**Marcas**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Marcas de herencia.

<dt>

0
</dt> <dd>

Sin herencias.

</dd> <dt>

2
</dt> <dd>

Se aplica a los espacios de nombres secundarios, además del actual.

</dd> </dl>

</dd> <dt>

**Máscara**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Máscara de bits que especifica los derechos de acceso al espacio de nombres en el Windows instrumental de administración de recursos (WMI). Para los valores de bits, vea [**Constantes de derechos de acceso de espacio de nombres**](namespace-access-rights-constants.md).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Nombre de usuario.

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Acceso permitido.

<dt>

0
</dt> <dd>

Acceso permitido.

</dd> <dt>

2
</dt> <dd>

Acceso denegado:

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **\_ \_ clase NTLMUser9X** se usa como parámetro de entrada para los métodos [**\_ \_ SystemSecurity::Get9XUserList**](--systemsecurity-get9xuserlist.md) y [**\_ \_ SystemSecurity::Set9XUserList.**](--systemsecurity-set9xuserlist.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**\_\_SecurityRelatedClass**](/windows/desktop/WmiSdk/--securityrelatedclass)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

