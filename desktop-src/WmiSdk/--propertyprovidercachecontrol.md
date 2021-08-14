---
description: Controla la memoria caché cuando se descarga un proveedor de propiedades.
ms.assetid: 8fc7de7a-889c-4d53-97ea-a676879de1d3
ms.tgt_platform: multiple
title: __PropertyProviderCacheControl clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PropertyProviderCacheControl
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 33edad107859328e9a81a6c77c3c02e29e2ee3aebbbe411ee20fb438e51517a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110543"
---
# <a name="__propertyprovidercachecontrol-class"></a>\_\_Clase PropertyProviderCacheControl

La **\_ \_ clase PropertyProviderCacheControl controla** la memoria caché cuando se descarga un proveedor de propiedades. Esta clase solo existe en el espacio \\ de nombres raíz.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __PropertyProviderCacheControl
{
  datetime ClearAfter;
};
```

## <a name="members"></a>Miembros

La **\_ \_ clase PropertyProviderCacheControl** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase PropertyProviderCacheControl** tiene estas propiedades.

<dl> <dt>

**ClearAfter**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Intervalo de tiempo después de que WMI libere un proveedor de propiedades. La hora está en formato de intervalo.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **\_ \_ clase PropertyProviderCacheControl** se deriva de [**\_ \_ CacheControl**](--cachecontrol.md). Para obtener más información, [vea Descargar un proveedor](unloading-a-provider.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

 




