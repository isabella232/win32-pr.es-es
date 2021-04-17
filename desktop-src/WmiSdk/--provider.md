---
description: Actúa como la clase primaria de la \_ \_ clase del sistema Win32Provider.
ms.assetid: e4cad7c6-4650-4334-b8c4-ac65381bced7
ms.tgt_platform: multiple
title: __Provider (clase)
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
ms.openlocfilehash: 733323c106a5d682e7eddbe3a41bf9c156520c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716217"
---
# <a name="__provider-class"></a>\_\_Provider (clase)

La clase de sistema de **\_ \_ proveedor** es una clase base abstracta que actúa como la clase primaria de la clase del sistema [**\_ \_ Win32Provider**](--win32provider.md) .

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

La clase de **\_ \_ proveedor** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase de **\_ \_ proveedor** tiene estas propiedades.

<dl> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [ **clave**](standard-qualifiers.md)
</dt> </dl>

Cadena independiente del lenguaje que identifica de forma única el proveedor. Se sugiere el siguiente formato para evitar conflictos de nomenclatura:

\|versión del proveedor del proveedor \|

Por ejemplo, este nombre de proveedor representa la versión 1,0 de Microsoft TestProvider:

"Microsoft \| TestProvider \| v 1.0"

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase de **\_ \_ proveedor** se deriva de [**\_ \_ SystemClass**](--systemclass.md), que no tiene propiedades.

Los proveedores crean instancias de [**\_ \_ Win32Provider**](--win32provider.md) para especificar información sobre su implementación física.

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

 

