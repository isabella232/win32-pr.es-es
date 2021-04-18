---
description: Controla el acceso remoto a versiones no admitidas de Windows.
ms.assetid: eb326bba-a011-4b9c-b4ee-fc08ae364f6f
ms.tgt_platform: multiple
title: __NTLMUser9X (clase)
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
ms.openlocfilehash: 79aa5153869c7337b6849e8c465dbbf8b36a0f58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707105"
---
# <a name="__ntlmuser9x-class"></a>\_\_Clase NTLMUser9X

La clase del sistema **\_ \_ NTLMUser9X** controla el acceso remoto a versiones no admitidas de Windows. La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

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

La clase **\_ \_ NTLMUser9X** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ NTLMUser9X** tiene estas propiedades.

<dl> <dt>

**Autoridad**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Dominio al que se aplica un nombre de usuario.

</dd> <dt>

**Marcas**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Marcadores de herencia.

<dt>

0
</dt> <dd>

Sin herencias.

</dd> <dt>

2
</dt> <dd>

Aplicar a los espacios de nombres secundarios, además del actual.

</dd> </dl>

</dd> <dt>

**Máscara**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Máscara de máscara que especifica los derechos de acceso al espacio de nombres en el repositorio de Instrumental de administración de Windows (WMI). Para los valores de bit, consulte [**constantes de derechos de acceso de espacio de nombres**](namespace-access-rights-constants.md).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Nombre de usuario.

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo de datos: **sint32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Acceso permitido.

<dt>

0
</dt> <dd>

Acceso permitido.

</dd> <dt>

2
</dt> <dd>

Acceso denegado.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **\_ \_ NTLMUser9X** se usa como parámetro de entrada para los métodos [**\_ \_ SystemSecurity:: Get9XUserList**](--systemsecurity-get9xuserlist.md) y [**\_ \_ SystemSecurity:: Set9XUserList**](--systemsecurity-set9xuserlist.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_SecurityRelatedClass**](/windows/desktop/WmiSdk/--securityrelatedclass)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

