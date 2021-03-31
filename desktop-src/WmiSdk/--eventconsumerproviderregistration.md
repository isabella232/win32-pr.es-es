---
description: Registra proveedores de consumidores de eventos con WMI.
ms.assetid: 31ff43dc-dc70-4ba0-866f-37445912f837
ms.tgt_platform: multiple
title: __EventConsumerProviderRegistration (clase)
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
ms.openlocfilehash: 38552519221018735c3c7543d9a1f3f2d4b680e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911974"
---
# <a name="__eventconsumerproviderregistration-class"></a>\_\_Clase EventConsumerProviderRegistration

La clase del sistema **\_ \_ EventConsumerProviderRegistration** registra proveedores de consumidores de eventos con WMI.

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

La clase **\_ \_ EventConsumerProviderRegistration** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ EventConsumerProviderRegistration** tiene estas propiedades.

<dl> <dt>

**ConsumerClassNames**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Matriz de nombres de las clases de consumidor lógicas que admite el proveedor de consumidor de eventos.

</dd> <dt>

**presta**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ \_ proveedor**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Ruta de acceso del objeto al proveedor. Esta propiedad se hereda de [**\_ \_ ProviderRegistration**](--providerregistration.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **\_ \_ EventConsumerProviderRegistration** se deriva de [**\_ \_ ProviderRegistration**](--providerregistration.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_ProviderRegistration**](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Registrar un proveedor de consumidor de eventos](registering-an-event-consumer-provider.md)
</dt> <dt>

[Escribir un proveedor de consumidor de eventos](writing-an-event-consumer-provider.md)
</dt> </dl>

 

