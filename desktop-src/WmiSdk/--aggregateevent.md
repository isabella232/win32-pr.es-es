---
description: Representa un evento agregado de varios eventos intrínsecos o extrínsecos individuales.
ms.assetid: 99afa390-01fe-4a13-ba21-27587470f111
ms.tgt_platform: multiple
title: __AggregateEvent clase
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967180"
---
# <a name="__aggregateevent-class"></a>\_\_AggregateEvent (clase)

La **\_ \_ clase del sistema AggregateEvent** representa un evento agregado de varios eventos intrínsecos o extrínsecos individuales. WMI genera una instancia de **\_ \_ AggregateEvent en** lugar de [**\_ \_ Event cuando**](--event.md) los consumidores se registran con la cláusula GROUP [WITHIN](group-clause.md) en su consulta de eventos.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __AggregateEvent : __IndicationRelated
{
  uint32 NumberOfEvents;
  object Representative;
};
```

## <a name="members"></a>Members

La **\_ \_ clase AggregateEvent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase AggregateEvent** tiene estas propiedades.

<dl> <dt>

**NumberOfEvents**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de eventos combinados para generar este evento de resumen único.

</dd> <dt>

**Representative**
</dt> <dd> <dl> <dt>

Tipo de datos: **objeto**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Copia de uno de los eventos entregados dentro del intervalo de agregación. Por ejemplo, si un consumidor se ha registrado para los eventos de cambio de clave del Registro desde el proveedor de eventos del Registro, **Representative** tendría una instancia de **la clase RegistryKeyChangeEvent.**

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **\_ \_ clase AggregateEvent** se deriva de [**\_ \_ IndicationRelated ,**](--indicationrelated.md)que no tiene propiedades.

Los proveedores de eventos nunca generan eventos agregados. Deben omitir la cláusula GROUP WITHIN en su procesamiento de consultas de eventos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**\_\_IndicationRelated**](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Consulta con WQL](querying-with-wql.md)
</dt> </dl>

 

