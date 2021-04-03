---
description: La clase NTEventLogEventConsumer registra un mensaje específico en el registro de eventos del sistema operativo cuando se le entrega un evento.
ms.assetid: cf986812-f09a-4f32-ba76-db76a23e2e4c
ms.tgt_platform: multiple
title: Clase NTEventLogEventConsumer
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908327"
---
# <a name="nteventlogeventconsumer-class"></a>Clase NTEventLogEventConsumer

La clase **NTEventLogEventConsumer** registra un mensaje específico en el registro de eventos del sistema operativo cuando se le entrega un evento. Esta clase es uno de los consumidores de eventos estándar que proporciona WMI. Para obtener más información, consulte [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).

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

## <a name="members"></a>Miembros

La clase **NTEventLogEventConsumer** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **NTEventLogEventConsumer** tiene estas propiedades.

<dl> <dt>

**Categoría**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Categoría de evento. Esta información es específica del origen y puede tener cualquier valor.

</dd> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo de datos: **Uint8** array
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador de seguridad (SID) que identifica de forma única al usuario que crea un filtro. WMI almacena el SID del usuario que crea una instancia de [**\_ \_ EventConsumer**](--eventconsumer.md) o el SID de administrador, dependiendo del sistema operativo. Para obtener más información, vea [enlazar un filtro de eventos con un consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md) y [supervisar y responder a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).

Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**Id. de evento**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Mensaje de evento en el archivo DLL del mensaje. Esta propiedad no puede ser **null**.

</dd> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de evento. Este parámetro puede tener uno de los valores enumerados en la lista siguiente, que se definen en Winnt. h.

<dt>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>

<span id="EVENTLOG_SUCCESS"></span><span id="eventlog_success"></span>**Registro de eventos \_ CORRECTO** (0 (0X0))


</dt> <dd>

Evento correcto

</dd> <dt>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>

<span id="EVENTLOG_ERROR_TPYE"></span><span id="eventlog_error_tpye"></span>**Registro de eventos \_ ERROR \_ TPYE** (1 (0x1))


</dt> <dd>

Evento de error

</dd> <dt>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>

<span id="EVENTLOG_WARNING_TYPE"></span><span id="eventlog_warning_type"></span>**Registro de eventos \_ \_Tipo de advertencia** (2 (0X2))


</dt> <dd>

Evento de advertencia

</dd> <dt>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>

<span id="EVENTLOG_INFORMATION_TYPE"></span><span id="eventlog_information_type"></span>**Registro de eventos \_ \_Tipo de información** (4 (0x4))


</dt> <dd>

Evento de información

</dd> <dt>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>

<span id="EVENTLOG_AUDIT_SUCCESS"></span><span id="eventlog_audit_success"></span>**Registro de eventos \_ AUDITORÍA \_ correcta** (8 (0x8))


</dt> <dd>

Tipo de auditoría Success

</dd> <dt>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>

<span id="EVENTLOG_AUDIT_FAILURE"></span><span id="eventlog_audit_failure"></span>**Registro de eventos \_ \_Error de auditoría** (16 (0x10))


</dt> <dd>

Tipo de auditoría de error

</dd> </dl>

</dd> <dt>

**InsertionStringTemplates**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de plantillas de cadena estándar que se utiliza como cadena de inserción para una entrada del registro de eventos.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del equipo al que Instrumental de administración de Windows (WMI) envía eventos.

Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cola máxima para un consumidor específico, en bytes.

Esta propiedad se hereda de [**\_ \_ EventConsumer**](--eventconsumer.md).

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

Nombre de la propiedad de evento que contiene los datos que se van a pasar al parámetro *lpRawData* de la función [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) .

</dd> <dt>

**NameOfUserSidProperty**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la propiedad de evento que contiene un identificador de seguridad (SID) que se va a pasar al parámetro *lpUserSid* de la función [**ReportEvent**](/windows/desktop/api/winbase/nf-winbase-reporteventa) . La propiedad debe ser una matriz de bytes (**Uint8**) o una cadena. Si es una matriz de bytes, se supone que es un SID. Si es una cadena, es un SID de cadena que se convierte en un SID.

</dd> <dt>

**NumberOfInsertionStrings**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número de elementos de la matriz **InsertionStringTemplates** .

</dd> <dt>

**SourceName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del origen donde se encuentra un mensaje. Se supone que el cliente ha registrado un archivo DLL con los mensajes necesarios.

> [!Note]  
> El valor de este parámetro no debe incluir un signo de dos puntos (:) óptico.

 

</dd> <dt>

**UNCServerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del equipo en el que se va a registrar un evento, o **null** si se va a registrar el evento en un servidor local.

De forma predeterminada, los usuarios autenticados no pueden registrar los eventos en el registro de aplicaciones de un equipo remoto. Como resultado, el uso de esta propiedad para especificar un equipo remoto no funcionará. Para obtener información sobre cómo cambiar la seguridad del registro de eventos, consulte este [artículo de Knowledge Base](https://support.microsoft.com/kb/323076).

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase **NTEventLogEventConsumer** se deriva de la clase abstracta [**\_ \_ EventConsumer**](--eventconsumer.md) .

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo del uso de **NTEventLogEventConsumer** para crear un consumidor, consulte [registro de eventos de NT basado en un evento](logging-to-nt-event-log-based-on-an-event.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\Suscripción raíz<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Wbemcons. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemcons.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de consumidor estándar](standard-consumer-classes.md)
</dt> <dt>

[Crear un consumidor lógico](creating-a-logical-consumer.md)
</dt> <dt>

[Recepción de eventos en todo momento](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 

