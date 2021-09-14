---
description: La clase NTEventLogEventConsumer registra un mensaje específico en el registro de eventos del sistema operativo cuando se le entrega un evento.
ms.assetid: cf986812-f09a-4f32-ba76-db76a23e2e4c
ms.tgt_platform: multiple
title: NTEventLogEventConsumer (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NTEventLogEventConsumer
- NTEventLogEventConsumer.CreatorSID
- NTEventLogEventConsumer.MachineName
- NTEventLogEventConsumer.MaximumQueueSize
- NTEventLogEventConsumer.Category
- NTEventLogEventConsumer.NameOfRawDataProperty
- NTEventLogEventConsumer.EventID
- NTEventLogEventConsumer.EventType
- NTEventLogEventConsumer.InsertionStringTemplates
- NTEventLogEventConsumer.Name
- NTEventLogEventConsumer.NumberOfInsertionStrings
- NTEventLogEventConsumer.NameOfUserSidProperty
- NTEventLogEventConsumer.SourceName
- NTEventLogEventConsumer.UNCServerName
api_type:
- DllExport
api_location:
- Wbemcons.dll
ms.openlocfilehash: e98948688b0fee37316102b2c37039de1c139310
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063961"
---
# <a name="nteventlogeventconsumer-class"></a>NTEventLogEventConsumer (clase)

La **clase NTEventLogEventConsumer** registra un mensaje específico en el registro de eventos del sistema operativo cuando se le entrega un evento. Esta clase es uno de los consumidores de eventos estándar que proporciona WMI. Para obtener más información, [vea Supervisión y respuesta a eventos con consumidores estándar.](monitoring-and-responding-to-events-with-standard-consumers.md)

## <a name="syntax"></a>Sintaxis

``` syntax
[AMENDMENT]
class NTEventLogEventConsumer : __EventConsumer
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
  uint16 Category;
  string NameOfRawDataProperty;
  uint32 EventID;
  uint32 EventType = 1;
  string InsertionStringTemplates[] = {""};
  string Name;
  uint32 NumberOfInsertionStrings = 0;
  string NameOfUserSidProperty;
  string SourceName;
  string UNCServerName;
};
```

## <a name="members"></a>Members

La **clase NTEventLogEventConsumer** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase NTEventLogEventConsumer** tiene estas propiedades.

<dl> <dt>

**Categoría**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Categoría de eventos. Se trata de información específica del origen y puede tener cualquier valor.

</dd> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador de seguridad (SID) que identifica de forma única al usuario que crea un filtro. WMI almacena el SID del usuario que crea una instancia de [**\_ \_ EventConsumer**](--eventconsumer.md) o el SID de administrador, en función del sistema operativo. Para obtener más información, vea [Enlazar un filtro de eventos con](binding-an-event-filter-with-a-logical-consumer.md) un consumidor lógico y Supervisar y Responder a eventos con [consumidores estándar.](monitoring-and-responding-to-events-with-standard-consumers.md)

Esta propiedad se hereda de [**\_ \_ EventConsumer.**](--eventconsumer.md)

</dd> <dt>

**Id. de evento**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Mensaje de evento en el archivo DLL del mensaje. Esta propiedad no puede ser **NULL.**

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de evento. Este parámetro puede tener uno de los valores enumerados en la lista siguiente, que se definen en Winnt.h.

<dt>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>**REGISTRO DE EVENTOS \_ SUCCESS** (0 (0x0))


</dt> <dd>

Evento correcto

</dd> <dt>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>**REGISTRO DE EVENTOS \_ ERROR \_ TPYE** (1 (0x1))


</dt> <dd>

Evento de error

</dd> <dt>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>**REGISTRO DE EVENTOS \_ TIPO \_ DE** ADVERTENCIA (2 (0x2))


</dt> <dd>

Evento de advertencia

</dd> <dt>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>**REGISTRO DE EVENTOS \_ TIPO \_ DE** INFORMACIÓN (4 (0x4))


</dt> <dd>

Evento de información

</dd> <dt>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>**REGISTRO DE EVENTOS \_ AUDIT \_ SUCCESS** (8 (0x8))


</dt> <dd>

Tipo de auditoría correcto

</dd> <dt>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>**REGISTRO DE EVENTOS \_ ERROR \_ DE AUDITORÍA** (16 (0x10))


</dt> <dd>

Tipo de auditoría de error

</dd> </dl>

</dd> <dt>

**InsertionStringTemplates**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de plantillas de cadena estándar que se usa como cadena de inserción para un registro de eventos.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del equipo al que Windows Management Instrumentation (WMI) envía eventos.

Esta propiedad se hereda de [**\_ \_ EventConsumer.**](--eventconsumer.md)

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cola máxima para un consumidor específico, en bytes.

Esta propiedad se hereda de [**\_ \_ EventConsumer.**](--eventconsumer.md)

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](key-qualifier.md)
</dt> </dl>

Nombre único de un consumidor.

</dd> <dt>

**NameOfRawDataProperty**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la propiedad de evento que contiene los datos que se pasarán al parámetro *lpRawData* de la función [**ReportEvent.**](/windows/desktop/api/winbase/nf-winbase-reporteventa)

</dd> <dt>

**NameOfUserSidProperty**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la propiedad de evento que contiene un identificador de seguridad (SID) que se va a pasar al parámetro *lpUserSid* de la función [**ReportEvent.**](/windows/desktop/api/winbase/nf-winbase-reporteventa) La propiedad debe ser una matriz de bytes (**uint8**) o una cadena. Si es una matriz de bytes, se supone que es un SID. Si es una cadena, es un SID de cadena que se convierte en un SID.

</dd> <dt>

**NumberOfInsertionStrings**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de elementos de la **matriz InsertionStringTemplates.**

</dd> <dt>

**SourceName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de origen donde se encuentra un mensaje. Se supone que el cliente ha registrado un archivo DLL con los mensajes necesarios.

> [!Note]  
> El valor de este parámetro no debe incluir dos puntos (:) Carácter.

 

</dd> <dt>

**UNCServerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del equipo en el que se va a registrar un evento o **NULL** si el evento se va a registrar en un servidor local.

Los usuarios autenticados no pueden, de forma predeterminada, registrar eventos en el registro de aplicación en un equipo remoto. Como resultado, el uso de esta propiedad para especificar un equipo remoto no funcionará. Para obtener información sobre cómo cambiar la seguridad del registro de eventos, consulte este [artículo de KB](https://support.microsoft.com/kb/323076).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase NTEventLogEventConsumer** se deriva de la [**\_ \_ clase abstracta EventConsumer.**](--eventconsumer.md)

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo del uso **de NTEventLogEventConsumer** para crear un consumidor, vea Registro en el registro de eventos [NT basado en un evento](logging-to-nt-event-log-based-on-an-event.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Suscripción \\ raíz<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Wbemcons.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemcons.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Clases de consumidor estándar](standard-consumer-classes.md)
</dt> <dt>

[Creación de un consumidor lógico](creating-a-logical-consumer.md)
</dt> <dt>

[Recepción de eventos en todo momento](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 

