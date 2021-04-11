---
description: La clase SMTPEventConsumer envía un mensaje de correo electrónico mediante el Protocolo simple de transferencia de correo (SMTP) cada vez que se le entrega un evento.
ms.assetid: 42178360-9e22-4cd1-9b72-5f6b0d7e6c9c
ms.tgt_platform: multiple
title: Clase SMTPEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SMTPEventConsumer
- SMTPEventConsumer.CreatorSID
- SMTPEventConsumer.MachineName
- SMTPEventConsumer.MaximumQueueSize
- SMTPEventConsumer.BccLine
- SMTPEventConsumer.CcLine
- SMTPEventConsumer.FromLine
- SMTPEventConsumer.HeaderFields
- SMTPEventConsumer.Message
- SMTPEventConsumer.Name
- SMTPEventConsumer.ReplyToLine
- SMTPEventConsumer.SMTPServer
- SMTPEventConsumer.Subject
- SMTPEventConsumer.ToLine
api_type:
- DllExport
api_location:
- Smtpcons.dll
ms.openlocfilehash: 76c7fad3b5cb4bbf6c3c0c03689607ba64fbcc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279112"
---
# <a name="smtpeventconsumer-class"></a>Clase SMTPEventConsumer

La clase **SMTPEventConsumer** envía un mensaje de correo electrónico mediante el Protocolo simple de transferencia de correo (SMTP) cada vez que se le entrega un evento. Debe existir un servidor SMTP en la red. La clase SMTPEventConsumer no admite datos adjuntos. La codificación del mensaje de correo electrónico debe ser US-ASCII.

Esta clase es uno de los consumidores de eventos estándar que proporciona WMI. Para obtener un ejemplo del uso de **SMTPEventConsumer** para crear un consumidor, consulte [envío de correo electrónico basado en un evento](sending-e-mail-based-on-an-event.md). Para obtener más información, consulte [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[AMENDMENT]
class SMTPEventConsumer : __EventConsumer
{
  uint8  CreatorSID[];
  string MachineName;
  uint32 MaximumQueueSize;
  string BccLine;
  string CcLine;
  string FromLine;
  string HeaderFields[];
  string Message;
  string Name;
  string ReplyToLine;
  string SMTPServer;
  string Subject;
  string ToLine;
};
```

## <a name="members"></a>Miembros

La clase **SMTPEventConsumer** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **SMTPEventConsumer** tiene estas propiedades.

<dl> <dt>

**BccLine**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una lista de direcciones, separadas por comas o punto y coma, en el formato de una plantilla de cadena estándar a la que se envía el mensaje como una copia oculta. Para obtener más información, consulte la sección Comentarios de este tema.

</dd> <dt>

**CcLine**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una lista de direcciones, separadas por comas o punto y coma, en el formato de una plantilla de cadena estándar a la que se envía el mensaje como una copia carbón. Para obtener más información, consulte la sección Comentarios de este tema.

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

**FromLine**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Desde la línea de un mensaje de correo electrónico con el formato de una plantilla de cadena estándar. Si es **null**, una línea de se construye con el formato "WinMgmt@*MachineName*".

</dd> <dt>

**HeaderFields**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Matriz de campos de encabezado que se insertan en un mensaje de correo electrónico sin interpretación.

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

**Message**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Plantilla de cadena estándar que contiene el cuerpo de un mensaje de correo electrónico.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](key-qualifier.md)
</dt> </dl>

Identificador único para el consumidor de eventos.

</dd> <dt>

**ReplyToLine**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Línea de respuesta de un mensaje de correo electrónico con el formato de una plantilla de cadena estándar. Si es **null**, no se utiliza ninguna línea de respuesta a.

</dd> <dt>

**SMTPServer**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del servidor SMTP a través del cual se envía un correo electrónico. Los nombres permitidos son una dirección IP o un nombre DNS o NetBIOS. Esta propiedad no puede ser **null**.

</dd> <dt>

**Subject**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Plantilla de cadena estándar que contiene el asunto de un mensaje de correo electrónico.

</dd> <dt>

**ToLine**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Una lista de direcciones, separadas por comas o punto y coma, en el formato de una plantilla de cadena estándar que identifica la ubicación a la que se va a enviar el mensaje. Para obtener más información, consulte la sección Comentarios de este tema.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La clase SMTPEventConsumer se deriva de la clase abstracta [**\_ \_ EventConsumer**](--eventconsumer.md) .

Algunas de las propiedades **ToLine**, **CcLine** o **BccLine** pueden ser **null**, pero no pueden ser todas **nulas**.

La recepción de un código de retorno de error del servicio SMTP se considera un error.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo del uso de **SMTPEventConsumer** para crear un consumidor, consulte [envío de correo electrónico basado en un evento](sending-e-mail-based-on-an-event.md). Para obtener más información, consulte [supervisión y respuesta a eventos con consumidores estándar](monitoring-and-responding-to-events-with-standard-consumers.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\Suscripción raíz<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Smtpcons. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Smtpcons.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> <dt>

[Clases de consumidor estándar](standard-consumer-classes.md)
</dt> <dt>

[Envío de correo electrónico basado en un evento](sending-e-mail-based-on-an-event.md)
</dt> <dt>

[Crear un consumidor lógico](creating-a-logical-consumer.md)
</dt> <dt>

[Recepción de eventos en todo momento](receiving-events-at-all-times.md)
</dt> </dl>

 

 




