---
description: Registra proveedores de consumidores de eventos con WMI.
ms.assetid: 31ff43dc-dc70-4ba0-866f-37445912f837
ms.tgt_platform: multiple
title: __EventConsumerProviderRegistration clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumerProviderRegistration
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: bc3acec16b92c375f07836318be0e77c335862aec826c80bb77815865a337a72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557939"
---
# <a name="__eventconsumerproviderregistration-class"></a>\_\_Clase EventConsumerProviderRegistration

La **\_ \_ clase del sistema EventConsumerProviderRegistration** registra proveedores de consumidores de eventos con WMI.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __EventConsumerProviderRegistration : __ProviderRegistration
{
  string         ConsumerClassNames[];
  __Provider REF provider;
};
```

## <a name="members"></a>Miembros

La **\_ \_ clase EventConsumerProviderRegistration** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase EventConsumerProviderRegistration** tiene estas propiedades.

<dl> <dt>

**ConsumerClassNames**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> </dl>

Matriz de nombres de las clases de consumidor lógico que admite el proveedor de consumidores de eventos.

</dd> <dt>

**Proveedor**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ \_ Proveedor**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso del objeto al proveedor. Esta propiedad se hereda de [**\_ \_ ProviderRegistration.**](--providerregistration.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **\_ \_ clase EventConsumerProviderRegistration** se deriva de [**\_ \_ ProviderRegistration.**](--providerregistration.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**\_\_ProviderRegistration**](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Registro de un proveedor de consumidores de eventos](registering-an-event-consumer-provider.md)
</dt> <dt>

[Escribir un proveedor de consumidores de eventos](writing-an-event-consumer-provider.md)
</dt> </dl>

 

