---
description: Contiene los derechos de seguridad para el espacio de nombres en forma de descriptor de seguridad.
ms.assetid: 84e514f5-b114-4bfc-ab0b-9745f249168b
ms.tgt_platform: multiple
title: __thisNAMESPACE clase
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
ms.openlocfilehash: 02e92bd8cb1c1827af86d23320e7347baa08c395d32def8c9b8adea2fcfd35bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132028"
---
# <a name="__thisnamespace-class"></a>\_\_thisNAMESPACE (clase)

La **\_ \_ clase del sistema thisNAMESPACE** contiene los derechos de seguridad para el espacio de nombres en forma de descriptor de seguridad. Esta clase y una única instancia se encuentran en todos los espacios de nombres.

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

La **\_ \_ clase thisNAMESPACE** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase thisNAMESPACE** tiene estas propiedades.

<dl> <dt>

**DESCRIPTOR \_ DE SEGURIDAD**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descriptor de seguridad que describe quién puede acceder al espacio de nombres y quién puede leer o escribir en el espacio de nombres. Esta propiedad se hereda del [**\_ \_ evento**](--event.md). Para obtener más información sobre el formato de los descriptores de seguridad, vea [Descriptores](/windows/desktop/SecAuthZ/security-descriptors) de seguridad en la sección Seguridad del SDK Windows seguridad.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La instancia singleton de **\_ \_ thisNAMESPACE** es de solo lectura. Para cambiar la configuración de la propiedad descriptor de seguridad, use los métodos de la [**\_ \_ clase SystemSecurity.**](--systemsecurity.md) La **\_ \_ clase thisNAMESPACE** se deriva de [**\_ \_ SystemClass**](--systemclass.md).

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

 

