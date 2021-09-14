---
description: Clase es la clase base abstracta para las clases que se usan para determinar cuándo WMI debe liberar un objeto De modelo de objetos componentes (COM).
ms.assetid: 32631610-8c0e-4f04-b0b2-62e5f8e23ef4
ms.tgt_platform: multiple
title: __CacheControl clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CacheControl
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: fe5358630a7ac5eb48751135d39c2fd998196bf7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967179"
---
# <a name="__cachecontrol-class"></a>\_\_CacheControl (clase)

La **\_ \_ clase del sistema CacheControl** es la clase base abstracta para las clases que se usan para determinar cuándo WMI debe liberar un objeto De modelo de objetos componentes (COM). Nunca se crean instancias de esta clase. La **\_ \_ clase CacheControl** solo se encuentra en el espacio de nombres raíz. Para obtener más información sobre el uso de esta clase, vea [Descargar un proveedor](unloading-a-provider.md).

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[abstract]
class __CacheControl : __SystemClass
{
};
```

## <a name="members"></a>Members

La **\_ \_ clase CacheControl** no define ningún miembro.

## <a name="remarks"></a>Observaciones

La **\_ \_ clase CacheControl** se deriva de [**\_ \_ SystemClass**](--systemclass.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**\_\_SystemClass**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**\_\_EventConsumerProviderCacheControl**](--eventconsumerprovidercachecontrol.md)
</dt> <dt>

[**\_\_EventProviderCacheControl**](--eventprovidercachecontrol.md)
</dt> <dt>

[**\_\_EventSinkCacheControl**](--eventsinkcachecontrol.md)
</dt> <dt>

[**\_\_ObjectProviderCacheControl**](--objectprovidercachecontrol.md)
</dt> <dt>

[\_\_PropertyProviderCacheControl](--propertyprovidercachecontrol.md)
</dt> <dt>

[Descargar un proveedor](unloading-a-provider.md)
</dt> </dl>

 

