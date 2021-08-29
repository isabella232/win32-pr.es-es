---
description: Actúa como clase primaria para la clase del sistema \_ \_ Win32Provider.
ms.assetid: e4cad7c6-4650-4334-b8c4-ac65381bced7
ms.tgt_platform: multiple
title: __Provider clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Provider
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 31f50f731942e056b201146abeccb038b32f2230c3bcd058f44279bc95bd326b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132058"
---
# <a name="__provider-class"></a>\_\_Clase de proveedor

La **\_ \_ clase** de sistema Provider es una clase base abstracta que actúa como clase primaria para la clase del sistema [**\_ \_ Win32Provider.**](--win32provider.md)

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[abstract]
class __Provider : __SystemClass
{
  string Name;
};
```

## <a name="members"></a>Miembros

La **\_ \_ clase Provider** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase Provider** tiene estas propiedades.

<dl> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [ **Clave**](standard-qualifiers.md)
</dt> </dl>

Cadena neutra del idioma que identifica de forma única el proveedor. Se recomienda el formato siguiente para evitar conflictos de nomenclatura:

versión \| del proveedor \|

Por ejemplo, este nombre de proveedor representa la versión 1.0 de Microsoft TestProvider:

"Microsoft \| TestProvider \| V1.0"

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **\_ \_ clase Provider** se deriva de [**\_ \_ SystemClass**](--systemclass.md), que no tiene propiedades.

Los proveedores crean [**\_ \_ instancias de Win32Provider**](--win32provider.md) para especificar información sobre su implementación física.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_SystemClass**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**\_\_Win32Provider**](--win32provider.md)
</dt> </dl>

 

