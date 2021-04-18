---
description: Determina cuándo debe publicar WMI un proveedor de consumidor de eventos.
ms.assetid: 93246826-8070-4e05-96f0-f773041ed1d4
ms.tgt_platform: multiple
title: __EventConsumerProviderCacheControl (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumerProviderCacheControl
- Root.__EventConsumerProviderCacheControl.ClearAfter
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: f769427c77f6efdf9a521a63f7334d5d27416c04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707413"
---
# <a name="__eventconsumerprovidercachecontrol-class"></a>\_\_Clase EventConsumerProviderCacheControl

La clase del sistema **\_ \_ EventConsumerProviderCacheControl** determina cuándo debe liberar WMI un proveedor de consumidores de eventos. La clase **\_ \_ EventConsumerProviderCacheControl** es una clase singleton. Solo se encuentra en el \\ espacio de nombres raíz.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[singleton]
class __EventConsumerProviderCacheControl : CacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Miembros

La clase **\_ \_ EventConsumerProviderCacheControl** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ EventConsumerProviderCacheControl** tiene estas propiedades.

<dl> <dt>

**ClearAfter**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Intervalo de tiempo después del cual WMI libera un proveedor de consumidor de eventos. Puede tardar hasta dos veces el intervalo especificado para descargar el proveedor. La hora está en [formato de intervalo](interval-format.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **\_ \_ EventConsumerProviderCacheControl** se deriva de [**\_ \_ CacheControl**](--cachecontrol.md). Para obtener más información sobre el uso de esta clase, vea [descargar un proveedor](unloading-a-provider.md).

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

 

 




