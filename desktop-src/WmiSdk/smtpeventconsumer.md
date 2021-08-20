---
description: La clase SMTPEventConsumer envía un mensaje de correo electrónico mediante el Protocolo simple de transferencia de correo (SMTP) cada vez que se le entrega un evento.
ms.assetid: 42178360-9e22-4cd1-9b72-5f6b0d7e6c9c
ms.tgt_platform: multiple
title: CLASE SMTPEventConsumer
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
ms.openlocfilehash: 4f216647f7ac6796c4b94157a261e535d9e2eb9cd98e02fd1f9cec5ac3dee95d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117922946"
---
# <a name="smtpeventconsumer-class"></a>CLASE SMTPEventConsumer

La **clase SMTPEventConsumer** envía un mensaje de correo electrónico mediante el Protocolo simple de transferencia de correo (SMTP) cada vez que se le entrega un evento. Debe existir un servidor SMTP en la red. La clase SMTPEventConsumer no admite datos adjuntos. La codificación del mensaje de correo electrónico debe ser US-ASCII.

Esta clase es uno de los consumidores de eventos estándar que proporciona WMI. Para obtener un ejemplo del uso **de SMTPEventConsumer para** crear un consumidor, vea [Enviar correo electrónico basado en un evento](sending-e-mail-based-on-an-event.md). Para obtener más información, vea [Supervisión y respuesta a eventos con consumidores estándar.](monitoring-and-responding-to-events-with-standard-consumers.md)

La sintaxis siguiente se simplifica a partir Managed Object Format (MOF) e incluye todas sus propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

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

La **clase SMTPEventConsumer** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase SMTPEventConsumer** tiene estas propiedades.

<dl> <dt>

**BccLine**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista de direcciones, separadas por una coma o punto y coma, en el formato de una plantilla de cadena estándar a la que se envía el mensaje como una copia de carbono invidente. Para obtener más información, vea la sección Comentarios de este tema.

</dd> <dt>

**CcLine**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Lista de direcciones, separadas por una coma o punto y coma, en el formato de una plantilla de cadena estándar a la que se envía el mensaje como una copia de carbono. Para obtener más información, vea la sección Comentarios de este tema.

</dd> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Identificador de seguridad (SID) que identifica de forma única al usuario que crea un filtro. WMI almacena el SID del usuario que crea una instancia de [**\_ \_ EventConsumer**](--eventconsumer.md) o el SID de administrador, según el sistema operativo. Para obtener más información, vea [Enlazar un filtro de eventos con](binding-an-event-filter-with-a-logical-consumer.md) un consumidor lógico y Supervisar y Responder a eventos con [consumidores estándar.](monitoring-and-responding-to-events-with-standard-consumers.md)

Esta propiedad se hereda de [**\_ \_ EventConsumer.**](--eventconsumer.md)

</dd> <dt>

**FromLine**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Desde la línea de un mensaje de correo electrónico con el formato de una plantilla de cadena estándar. Si **es NULL,** se construye una línea From con el formato "WinMgmt@*MachineName".*

</dd> <dt>

**HeaderFields**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
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

**Mensaje**
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

Calificadores: [ **key**](key-qualifier.md)
</dt> </dl>

Identificador único para el consumidor de eventos.

</dd> <dt>

**ReplyToLine**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Línea de respuesta de un mensaje de correo electrónico con el formato de una plantilla de cadena estándar. Si **es NULL,** no se usa ninguna línea de respuesta.

</dd> <dt>

**SMTPServer**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del servidor SMTP a través del que se envía un correo electrónico. Los nombres permitidos son una dirección IP o un nombre DNS o NetBIOS. Esta propiedad no puede ser **NULL.**

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

Lista de direcciones, separadas por una coma o punto y coma, en el formato de una plantilla de cadena estándar que identifica dónde se va a enviar el mensaje. Para obtener más información, vea la sección Comentarios de este tema.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La clase SMTPEventConsumer se deriva de la clase abstracta [**\_ \_ EventConsumer.**](--eventconsumer.md)

Algunas de las **propiedades ToLine,** **CcLine** o **BccLine** pueden ser **NULL,** pero no todas pueden ser **NULL.**

La recepción de un código de retorno de error del servicio SMTP se considera un error.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo del uso **de SMTPEventConsumer para** crear un consumidor, vea [Enviar correo electrónico basado en un evento](sending-e-mail-based-on-an-event.md). Para obtener más información, vea [Supervisión y respuesta a eventos con consumidores estándar.](monitoring-and-responding-to-events-with-standard-consumers.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Suscripción \\ raíz<br/>                                                           |
| MOF<br/>                      | <dl> <dt>Smtpcons.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Smtpcons.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> <dt>

[Clases de consumidor estándar](standard-consumer-classes.md)
</dt> <dt>

[Envío de correo electrónico basado en un evento](sending-e-mail-based-on-an-event.md)
</dt> <dt>

[Creación de un consumidor lógico](creating-a-logical-consumer.md)
</dt> <dt>

[Recepción de eventos en todo momento](receiving-events-at-all-times.md)
</dt> </dl>

 

 




