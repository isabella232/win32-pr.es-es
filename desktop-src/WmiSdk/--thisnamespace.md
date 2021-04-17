---
description: Contiene los derechos de seguridad para el espacio de nombres en forma de un descriptor de seguridad.
ms.assetid: 84e514f5-b114-4bfc-ab0b-9745f249168b
ms.tgt_platform: multiple
title: __thisNAMESPACE (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __thisNAMESPACE
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 440ccdf0eda794b5d648cae756f9a9c808eb2db6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688246"
---
# <a name="__thisnamespace-class"></a>\_\_clase thisNAMESPACE

La clase del sistema **\_ \_ thisNAMESPACE** contiene los derechos de seguridad para el espacio de nombres en forma de un descriptor de seguridad. Esta clase y una sola instancia se encuentran en todos los espacios de nombres.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[singleton]
class __thisNAMESPACE : __SystemClass
{
  uint8 SECURITY_DESCRIPTOR[];
};
```

## <a name="members"></a>Miembros

La clase **\_ \_ thisNAMESPACE** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ thisNAMESPACE** tiene estas propiedades.

<dl> <dt>

**descriptor de seguridad \_**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descriptor de seguridad que describe quién puede tener acceso al espacio de nombres y quién puede leer o escribir en el espacio de nombres. Esta propiedad se hereda del [**\_ \_ evento**](--event.md). Para obtener más información sobre el formato de los descriptores de seguridad, consulte [descriptores de seguridad](/windows/desktop/SecAuthZ/security-descriptors) en la sección seguridad de la Windows SDK.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La instancia singleton de **\_ \_ thisNAMESPACE** es de solo lectura. Para cambiar la configuración de la propiedad del descriptor de seguridad, use los métodos de la clase [**\_ \_ SystemSecurity**](--systemsecurity.md) . La clase **\_ \_ thisNAMESPACE** se deriva de [**\_ \_ SystemClass**](--systemclass.md).

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
</dt> </dl>

 

