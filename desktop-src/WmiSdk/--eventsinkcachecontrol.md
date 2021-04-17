---
description: Se utiliza para determinar si WMI libera un puntero IWbemUnboundObjectSink de proveedores de consumidor de eventos.
ms.assetid: f7b14efc-a2f7-4e99-8ec8-5b5af0743139
ms.tgt_platform: multiple
title: __EventSinkCacheControl (clase)
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
ms.openlocfilehash: 9d20e64fed1ee6ba5622d5e6a342a60485f53d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697650"
---
# <a name="__eventsinkcachecontrol-class"></a>\_\_Clase EventSinkCacheControl

La clase del sistema **\_ \_ EventSinkCacheControl** se usa para determinar cuándo el WMI libera un puntero [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) del proveedor del consumidor de eventos. La clase **\_ \_ EventSinkCacheControl** es una clase singleton. Solo se encuentra en el \\ espacio de nombres raíz.

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

La clase **\_ \_ EventSinkCacheControl** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ EventSinkCacheControl** tiene estas propiedades.

<dl> <dt>

**ClearAfter**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Intervalo de tiempo después del cual WMI libera un proveedor de eventos. Puede tardar hasta dos veces el intervalo especificado para descargar el proveedor. La hora está en [formato de intervalo](interval-format.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **\_ \_ EventSinkCacheControl** se deriva de [**\_ \_ CacheControl**](--cachecontrol.md). Para obtener más información sobre el uso de esta clase, vea [descargar un proveedor](unloading-a-provider.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Root<br/>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

 




