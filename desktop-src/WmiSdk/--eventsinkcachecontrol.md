---
description: Se usa para determinar cuándo WMI libera un puntero IWbemUnboundObjectSink de proveedores de consumidores de eventos.
ms.assetid: f7b14efc-a2f7-4e99-8ec8-5b5af0743139
ms.tgt_platform: multiple
title: __EventSinkCacheControl clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventSinkCacheControl
- Root.__EventSinkCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: dc73e2cb740486ad08172c10233f4865709a87d9f1122f399002133687744094
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557919"
---
# <a name="__eventsinkcachecontrol-class"></a>\_\_Clase EventSinkCacheControl

La clase del sistema **\_ \_ EventSinkCacheControl** se usa para determinar cuándo WMI libera el puntero [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) de un proveedor de consumidores de eventos. La **\_ \_ clase EventSinkCacheControl** es una clase singleton. Solo se encuentra en el espacio de \\ nombres raíz.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[singleton]
class __EventSinkCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Miembros

La **\_ \_ clase EventSinkCacheControl** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase EventSinkCacheControl** tiene estas propiedades.

<dl> <dt>

**ClearAfter**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Intervalo de tiempo después del cual WMI libera un proveedor de eventos. Puede tardar hasta el doble del intervalo especificado para descargar el proveedor. La hora está en formato [de intervalo.](interval-format.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **\_ \_ clase EventSinkCacheControl** se deriva de [**\_ \_ CacheControl**](--cachecontrol.md). Para obtener más información sobre el uso de esta clase, vea [Unloading a Provider](unloading-a-provider.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Root<br/>                |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

 




