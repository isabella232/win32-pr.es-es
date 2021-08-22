---
description: Class es la clase base abstracta para las clases que se usan para determinar cuándo WMI debe liberar un objeto de Modelo de objetos componentes (COM).
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
ms.openlocfilehash: 429e973d83e1f213b011998c75dfbfabd81fb7bb4921f0f8b9f61bcedd6080c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051103"
---
# <a name="__cachecontrol-class"></a>\_\_Clase CacheControl

La clase del sistema **\_ \_ CacheControl** es la clase base abstracta para las clases que se usan para determinar cuándo WMI debe liberar un objeto del Modelo de objetos componentes (COM). Nunca se crean instancias de esta clase. La **\_ \_ clase CacheControl** solo se encuentra en el espacio de nombres raíz. Para obtener más información sobre el uso de esta clase, vea [Unloading a Provider](unloading-a-provider.md).

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[abstract]
class __CacheControl : __SystemClass
{
};
```

## <a name="members"></a>Miembros

La **\_ \_ clase CacheControl** no define ningún miembro.

## <a name="remarks"></a>Comentarios

La **\_ \_ clase CacheControl** se deriva de [**\_ \_ SystemClass**](--systemclass.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

