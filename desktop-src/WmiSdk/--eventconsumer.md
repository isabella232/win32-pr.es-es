---
description: Es una clase base abstracta que se utiliza en el registro de un consumidor de eventos permanente.
ms.assetid: c1dc9a91-76f9-4527-ad69-0323a9aef28a
ms.tgt_platform: multiple
title: __EventConsumer (clase)
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
ms.openlocfilehash: b8478b76aebf293d562129d047330f33e52706b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104003110"
---
# <a name="__eventconsumer-class"></a>\_\_Clase EventConsumer

La clase del sistema **\_ \_ EventConsumer** es una clase base abstracta que se utiliza en el registro de un consumidor de eventos permanente. Puede derivar una nueva clase de consumidor de eventos de **\_ \_ EventConsumer**.

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

La clase **\_ \_ EventConsumer** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ EventConsumer** tiene estas propiedades.

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador de seguridad (SID) que identifica de forma única al usuario que crea un filtro. WMI almacena el SID del usuario que crea una instancia de **\_ \_ EventConsumer** o el SID de administrador, dependiendo del sistema operativo. Para obtener más información, vea [enlazar un filtro de eventos con un consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md) y [supervisar y responder a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del equipo al que Instrumental de administración de Windows (WMI) envía eventos.

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cola máxima para un consumidor específico, en bytes.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **\_ \_ EventConsumer** se deriva de [**\_ \_ IndicationRelated**](--indicationrelated.md), que no tiene propiedades.

Los consumidores permanentes definen nuevas clases de consumidor para describir una acción que se realizará y los datos se procesarán cuando los consumidores reciban notificaciones de eventos. Los consumidores permanentes tienen problemas de seguridad especiales. Para obtener más información, consulte [protección de eventos WMI](securing-wmi-events.md).

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

[Crear un consumidor lógico](creating-a-logical-consumer.md)
</dt> <dt>

[Proteger eventos WMI](securing-wmi-events.md)
</dt> </dl>

 

