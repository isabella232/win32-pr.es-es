---
description: Es una clase base abstracta que se usa en el registro de un consumidor de eventos permanente.
ms.assetid: c1dc9a91-76f9-4527-ad69-0323a9aef28a
ms.tgt_platform: multiple
title: __EventConsumer clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventConsumer
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: ba84549f1120f4f6d2045e9e9c999e56c38dd285e2ab25de5da1e1b12401f345
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120955"
---
# <a name="__eventconsumer-class"></a>\_\_Clase EventConsumer

La **\_ \_ clase del sistema EventConsumer** es una clase base abstracta que se usa en el registro de un consumidor de eventos permanente. Puede derivar una nueva clase de consumidor de eventos de **\_ \_ EventConsumer.**

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[abstract]
class __EventConsumer : __IndicationRelated
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
};
```

## <a name="members"></a>Miembros

La **\_ \_ clase EventConsumer** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **\_ \_ clase EventConsumer** tiene estas propiedades.

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador de seguridad (SID) que identifica de forma única al usuario que crea un filtro. WMI almacena el SID del usuario que crea una instancia de **\_ \_ EventConsumer** o el SID de administrador, según el sistema operativo. Para obtener más información, vea [Enlazar un filtro de eventos con](binding-an-event-filter-with-a-logical-consumer.md) un consumidor lógico y Supervisar y Responder a eventos con [consumidores estándar.](monitoring-and-responding-to-events-with-standard-consumers.md)

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del equipo al que Windows Management Instrumentation (WMI) envía eventos.

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cola máxima para un consumidor específico, en bytes.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **\_ \_ clase EventConsumer** se deriva de [**\_ \_ IndicationRelated**](--indicationrelated.md), que no tiene propiedades.

Los consumidores permanentes definen nuevas clases de consumidor para describir una acción que se debe realizar y los datos que se procesarán cuando los consumidores reciban notificaciones de eventos. Los consumidores permanentes tienen problemas de seguridad especiales. Para obtener más información, [vea Securing WMI Events](securing-wmi-events.md).

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

[Recepción de eventos en todo momento](receiving-events-at-all-times.md)
</dt> <dt>

[Crear una nueva clase de consumidor de eventos permanente](creating-a-new-permanent-event-consumer-class.md)
</dt> <dt>

[Creación de un consumidor lógico](creating-a-logical-consumer.md)
</dt> <dt>

[Protección de eventos WMI](securing-wmi-events.md)
</dt> </dl>

 

