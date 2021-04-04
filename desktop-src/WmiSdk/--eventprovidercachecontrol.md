---
description: Controla cuándo se descarga un proveedor de eventos.
ms.assetid: 7f11e521-d0f6-4c3c-8bfe-ceed2d106ed3
ms.tgt_platform: multiple
title: __EventProviderCacheControl (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventProviderCacheControl
- Root.__EventProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: c54ec47b1f67d96816cf24a6b6e0108ee0b1de70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277710"
---
# <a name="__eventprovidercachecontrol-class"></a>\_\_Clase EventProviderCacheControl

La clase del sistema **\_ \_ EventProviderCacheControl** controla cuándo se descarga un proveedor de eventos. Solo se encuentra en el \\ espacio de nombres raíz.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[singleton]
class __EventProviderCacheControl : __CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Miembros

La clase **\_ \_ EventProviderCacheControl** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ EventProviderCacheControl** tiene estas propiedades.

<dl> <dt>

**ClearAfter**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

El intervalo de tiempo después de que Instrumental de administración de Windows (WMI) libera un proveedor de eventos. La hora está en [formato de intervalo](interval-format.md). Puede tardar hasta dos veces el intervalo especificado para descargar el proveedor.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **\_ \_ EventProviderCacheControl** se deriva de [**\_ \_ CacheControl**](--cachecontrol.md).

Para obtener más información sobre el uso de esta clase, vea [descargar un proveedor](unloading-a-provider.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Root<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_CacheControl**](/windows/desktop/WmiSdk/--cachecontrol)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

