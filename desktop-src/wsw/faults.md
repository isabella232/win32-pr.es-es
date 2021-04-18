---
title: Errores
description: Un mensaje de error se usa para comunicar información de error sobre un error en un punto de conexión remoto.
ms.assetid: d2bada50-2ddd-4f7f-9b25-7bbec77b431b
keywords:
- Servicios Web de errores para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2ecad1b63335b7f2bfc81c099b4f920d9de21c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714139"
---
# <a name="faults"></a>Errores

Un mensaje de error se usa para comunicar información de error sobre un error en un punto de conexión remoto. Un mensaje de error es como cualquier otro mensaje, excepto que el formato del cuerpo del mensaje tiene un formato estándar. Los errores se pueden usar tanto mediante protocolos de infraestructura, como WS-Addressing, como con protocolos de aplicación de nivel superior.

-   [Información general](#overview)
-   [Generar errores en un servicio](#generating-faults-in-a-service)
-   [Control de errores en un cliente](#handling-faults-on-a-client)
-   [Usar errores con mensajes](#using-faults-with-messages)

## <a name="overview"></a>Información general

El contenido del cuerpo de un mensaje de error se representa en esta API mediante la estructura de [**\_ error de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) . Aunque un error tiene un conjunto fijo de campos que se usa para proporcionar información sobre el error (por ejemplo, el [**\_ \_ código de error de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code) que identifica el tipo de error y la [**\_ \_ razón del error de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason) que contiene el texto que describe el error), también contiene un campo de detalle que se puede usar para especificar contenido XML arbitrario relacionado con el error.

## <a name="generating-faults-in-a-service"></a>Generar errores en un servicio

Un servicio normalmente enviará un error debido a algún error detectado durante el procesamiento de la solicitud. El modelo usado por esta API es que el código del servicio que encuentra el error de procesamiento capturará la información de error necesaria en el objeto [de \_ error de WS](ws-error.md) y, a continuación, el código en un nivel superior de la cadena de llamadas enviará realmente el error con la información capturada en la capa inferior. Este esquema permite aislar el código que envía el error de cómo se asignan las situaciones de error a los errores, al tiempo que se permite el envío de información de errores enriquecida.

Las siguientes propiedades se pueden usar con [**WsSetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty) para capturar información de error para un objeto de [ \_ error de WS](ws-error.md) :

-   [**WS \_ acción de la \_ \_ propiedad \_ error Fault**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Especifica la acción que se va a usar para el mensaje de error. Si no se especifica, se proporciona una acción predeterminada.
-   [**WS \_ error de la \_ \_ propiedad \_ error**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Contiene la estructura [**de \_ error de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) que se envía en el cuerpo del mensaje de error.
-   [**WS \_ encabezado de la \_ \_ propiedad \_ de error Fault**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Algunos errores incluyen encabezados de mensajes que se agregan al mensaje de error para transmitir errores de procesamiento relacionados con los encabezados del mensaje de solicitud. Esta propiedad se puede utilizar para especificar un [ \_ \_ búfer de WS XML](ws-xml-buffer.md) que contenga un encabezado que se va a agregar al mensaje de error.

Las cadenas de error que se agreguen al objeto de [ \_ error de WS](ws-error.md) se usan como el texto del error que se envía. Las cadenas de error se pueden agregar al objeto de error mediante [**WsAddErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring).

La función [**WsSetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty) se puede usar para establecer estas propiedades del objeto [de \_ error de WS](ws-error.md) .

Para establecer el detalle del error almacenado en el objeto [de \_ error de WS](ws-error.md) , utilice la función [**WsSetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrordetail) . Esta función se puede utilizar para asociar contenido XML arbitrario con el error.

El [host de servicio](service-host.md) enviará automáticamente los errores mediante la información anterior en el objeto de [ \_ error de WS](ws-error.md) . La propiedad de divulgación de errores de la [**\_ propiedad de servicio \_ \_ \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) se puede usar para controlar la detallación de un error que se enviará.

Si trabaja en la capa del canal, se pueden enviar errores para un objeto de [ \_ error de WS](ws-error.md) mediante [**WsSendFaultMessageForError**](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror).

## <a name="handling-faults-on-a-client"></a>Control de errores en un cliente

Si un cliente recibe un error al usar un [proxy de servicio](service-proxy.md) o a través de [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) o [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage), se devolverá el error de **punto de conexión de WS \_ \_ \_ \_ E** . (Para obtener más información, vea [valores devueltos de servicios Web de Windows](windows-web-services-return-values.md)). Estas funciones también rellenan el objeto de [ \_ error de WS](ws-error.md) proporcionado a la llamada con información sobre el error recibido.

Las siguientes propiedades de un objeto de [ \_ error de WS](ws-error.md) se pueden consultar mediante [**WsGetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrorproperty) para obtener información sobre un error que se recibió:

-   [**WS \_ acción de la \_ \_ propiedad \_ error Fault**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Especifica el valor de la acción del mensaje de error.
-   [**WS \_ error de la \_ \_ propiedad \_ error**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Contiene la estructura [**de \_ error de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) que se deserializó desde el cuerpo del mensaje de error.

Un error puede contener contenido XML adicional arbitrario en el detalle del error. Se puede tener acceso a este mediante el uso de la función [**WsGetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrordetail) .

## <a name="using-faults-with-messages"></a>Usar errores con mensajes

La siguiente sección se aplica al tratar directamente con el contenido del cuerpo de un mensaje de error.

El contenido del cuerpo de un mensaje de error se representa mediante la estructura estándar [**WS \_ error**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) , que tiene compatibilidad integrada para la serialización.

Por ejemplo, el código siguiente puede usarse para escribir un error en el cuerpo de un mensaje:

``` syntax
HRESULT hr;
WS_ELEMENT_DESCRIPTION faultDescription = { NULL, WS_FAULT_TYPE, NULL, NULL };
WS_FAULT fault = { ... };
hr = WsWriteBody(message, &faultDescription, WS_WRITE_REQUIRED_VALUE, &fault, sizeof(fault), error);
```

El siguiente código se puede usar para leer un error del cuerpo de un mensaje:

``` syntax
HRESULT hr;
WS_ELEMENT_DESCRIPTION faultDescription = { NULL, WS_FAULT_TYPE, NULL, NULL };
WS_FAULT fault;
hr = WsReadBody(message, &faultDescription, WS_READ_REQUIRED_VALUE, &fault, sizeof(fault), error);
```

Para saber si un mensaje recibido es un error o no, se puede consultar [**la \_ \_ propiedad \_ \_ WS Message**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) . Esta propiedad se establece en función de si el primer elemento del cuerpo es un elemento Fault durante [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) o [**WsReadEnvelopeStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopestart).

Para crear un error de [**WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) debido a un [ \_ error de WS](ws-error.md), utilice la función [**WsCreateFaultFromError**](/windows/desktop/api/WebServices/nf-webservices-wscreatefaultfromerror) .

Las enumeraciones siguientes forman parte de los errores:

-   [**\_revelación de errores de WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure)
-   [**identificador de la \_ \_ propiedad de error \_ \_ de WS**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id)

Las siguientes funciones forman parte de los errores:

-   [**WsCreateFaultFromError**](/windows/desktop/api/WebServices/nf-webservices-wscreatefaultfromerror)
-   [**WsGetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrordetail)
-   [**WsGetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrorproperty)
-   [**WsSetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrordetail)
-   [**WsSetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty)

Las siguientes estructuras forman parte de los errores:

-   [**error de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault)
-   [**\_código de error de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code)
-   [**\_Descripción del \_ detalle de error de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_detail_description)
-   [**\_razón del error de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason)

 

 




