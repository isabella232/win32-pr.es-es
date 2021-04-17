---
description: Representa un evento de agregado de varios eventos intrínsecos o extrínsecos individuales.
ms.assetid: 99afa390-01fe-4a13-ba21-27587470f111
ms.tgt_platform: multiple
title: __AggregateEvent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __AggregateEvent
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: f93a962e57452ac555214e42f00af8ac8a4ea3db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688408"
---
# <a name="__aggregateevent-class"></a>\_\_Clase AggregateEvent

La clase del sistema **\_ \_ AggregateEvent** representa un evento agregado de varios eventos intrínsecos o extrínsecos individuales. WMI genera una instancia de **\_ \_ AggregateEvent** en lugar de un [**\_ \_ evento**](--event.md) cuando los consumidores se registran con la cláusula [Group Within](group-clause.md) en su consulta de eventos.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __AggregateEvent : __IndicationRelated
{
  uint32 NumberOfEvents;
  object Representative;
};
```

## <a name="members"></a>Miembros

La clase **\_ \_ AggregateEvent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ AggregateEvent** tiene estas propiedades.

<dl> <dt>

**NumberOfEvents**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de eventos combinados para producir este evento de Resumen único.

</dd> <dt>

**Representative**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Copia de uno de los eventos entregados en el intervalo de agregación. Por ejemplo, si un consumidor se ha registrado para eventos de cambio de clave del registro del proveedor de eventos del registro, **representador** contendría una instancia de la clase **RegistryKeyChangeEvent** .

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **\_ \_ AggregateEvent** se deriva de [**\_ \_ IndicationRelated**](--indicationrelated.md), que no tiene propiedades.

Los proveedores de eventos nunca generan eventos agregados. Deben pasar por alto la cláusula GROUP WITHIN en el procesamiento de consultas de eventos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_IndicationRelated**](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Realizar consultas con WQL](querying-with-wql.md)
</dt> </dl>

 

