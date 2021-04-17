---
description: El registro de un consumidor de eventos permanente requiere una instancia de la \_ \_ clase del sistema EventFilter.
ms.assetid: 369d3c28-2b69-456f-9144-d7c73e3123bc
ms.tgt_platform: multiple
title: __EventFilter (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __EventFilter
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 0316e158eb2098f89106c64ba0057f8d9b4fc26b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706659"
---
# <a name="__eventfilter-class"></a>\_\_Clase EventFilter

El registro de un consumidor de eventos permanente requiere una instancia de la clase del sistema **\_ \_ EventFilter** .

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class __EventFilter : __IndicationRelated
{
  uint8  CreatorSID[] = {1,1,0,0,0,0,0,5,18,0,0,0};
  string EventAccess;
  string EventNamespace;
  string Name;
  string Query;
  string QueryLanguage;
};
```

## <a name="members"></a>Miembros

La clase **\_ \_ EventFilter** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **\_ \_ EventFilter** tiene estas propiedades.

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Identificador de seguridad (SID) que identifica de forma única al usuario que crea este filtro. Instrumental de administración de Windows (WMI) almacena el SID del usuario que crea una instancia de **\_ \_ EventFilter** o el SID de administrador, dependiendo del sistema operativo. Para obtener más información, vea [enlazar un filtro de eventos con un consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md) y [supervisar y responder a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).

</dd> <dt>

**EventAccess**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Descriptor de seguridad (SD) en el lenguaje de definición de descriptores de seguridad (SDDL) que controla el acceso a los eventos entregados al filtro. Utilice esta propiedad para especificar que solo se puedan entregar a este filtro los eventos en el contexto de seguridad de cuentas específicas. Por ejemplo, un consumidor de eventos permanente puede borrar los registros de seguridad solo cuando un usuario específico genera un evento específico. Para especificar quién puede publicar eventos en este filtro, use la máscara de **\_ \_ publicación derecha de WBEM** en la entrada de Access Control (ACE) para la propiedad [**\_ descriptor de seguridad**](--event.md) . Para obtener más información, vea [lenguaje de definición de descriptores de seguridad](/windows/desktop/SecAuthZ/security-descriptor-definition-language). Para obtener más información sobre las constantes que se usan para establecer este descriptor de seguridad, vea [constantes de seguridad de WMI](wmi-security-constants.md). Para obtener más información y ejemplos, vea reemplazar:[recibir eventos de forma segura](receiving-events-securely.md).

Puede configurar un descriptor de seguridad de acceso a eventos para permitir que se entregue un evento solo cuando la cuenta de sistema local genera el evento. Para obtener más información sobre cómo crear un descriptor de seguridad y autorizar el acceso, consulte [Access Control](/windows/desktop/SecAuthZ/access-control).

Ejemplo: la siguiente cadena SDDL permite que solo los administradores proporcionen eventos al filtro. El derecho necesario para proporcionar eventos es **WBEM \_ right \_ PUBLISH** (x80).


```VB
O:BAG:BAD:(A;;0x80;;;BA)
```



</dd> <dt>

**EventNamespace**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Espacio de nombres de la instancia de evento utilizada para las suscripciones entre espacios de nombres.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: [ **clave**](standard-qualifiers.md)
</dt> </dl>

Identificador único de un filtro de eventos. Dado que WMI solo usa un filtro de eventos, se recomienda que establezca esta propiedad en un identificador único global (**GUID**) convertido en una cadena. Sin embargo, los consumidores pueden usar cualquier esquema privado para un nombre de filtro siempre y cuando no haya ningún conflicto con otros filtros.

</dd> <dt>

**Consultar**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Instrumental de administración de Windows consulta de eventos del lenguaje de consulta (WQL) que especifica el conjunto de eventos para la notificación del consumidor y las condiciones específicas para la notificación.

</dd> <dt>

**QueryLanguage**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> </dl>

Lenguaje usado para la consulta. Dado que WMI actualmente solo admite lenguaje de consulta de WMI (WQL) como lenguaje de consulta, esta propiedad debe establecerse en "WQL".

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **\_ \_ EventFilter** se deriva de [**\_ \_ IndicationRelated**](--indicationrelated.md).

## <a name="examples"></a>Ejemplos

El ejemplo de [creación de registro de eventos de WMI permanente para supervisar archivos](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) de PowerShell en la galería de TechNet usa **\_ \_ EventFilter** como parte de un script complejo para configurar un registro de eventos de WMI permanente.

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

[Crear un filtro de eventos](creating-an-event-filter.md)
</dt> <dt>

[Recepción de eventos en todo momento](receiving-events-at-all-times.md)
</dt> <dt>

[Supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md)
</dt> <dt>

[Supervisión de eventos](monitoring-events.md)
</dt> <dt>

[Clases de consumidor estándar](standard-consumer-classes.md)
</dt> <dt>

[Proteger eventos WMI](securing-wmi-events.md)
</dt> </dl>

 

