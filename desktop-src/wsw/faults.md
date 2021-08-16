---
title: Errores
description: Un mensaje de error se usa para comunicar información de error sobre un error en un punto de conexión remoto.
ms.assetid: d2bada50-2ddd-4f7f-9b25-7bbec77b431b
keywords:
- Servicios web de errores para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55cd9e28e9ec9ce2f3068643d44306f542eebabb9b0b0c8860b15e9e986b49b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841775"
---
# <a name="faults"></a>Errores

Un mensaje de error se usa para comunicar información de error sobre un error en un punto de conexión remoto. Un mensaje de error es como cualquier otro mensaje, salvo que el formato del cuerpo del mensaje tiene un formato estándar. Los errores se pueden usar tanto en protocolos de infraestructura, como WS-Addressing, como en protocolos de aplicación de nivel superior.

-   [Información general](#overview)
-   [Generación de errores en un servicio](#generating-faults-in-a-service)
-   [Control de errores en un cliente](#handling-faults-on-a-client)
-   [Uso de errores con mensajes](#using-faults-with-messages)

## <a name="overview"></a>Información general

El contenido del cuerpo de un mensaje de error se representa en esta API mediante la [**estructura \_ FAULT de WS.**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) Aunque un error tiene un conjunto fijo de campos que se usan para proporcionar información sobre el error (como el código de error de [**WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code) que identifica el tipo de error y el motivo del error de [**WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason) que contiene texto que describe el error), también contiene un campo de detalle que se puede usar para especificar contenido XML arbitrario relacionado con el error.

## <a name="generating-faults-in-a-service"></a>Generación de errores en un servicio

Un servicio normalmente enviará un error debido a algún error que se encontró al procesar la solicitud. El modelo que usa esta API es que el código del servicio que encuentra el error de procesamiento capturará la información de error necesaria en el objeto ERROR de [WS \_ ](ws-error.md) y, a continuación, el código de un nivel superior de la cadena de llamadas enviará realmente el error mediante la información capturada en la capa inferior. Este esquema permite que el código que envía el error se aísle de cómo se asignan las situaciones de errores a los errores, a la vez que permite enviar información de error enriquecida.

Las siguientes propiedades se pueden usar con [**WsSetFaultErrorProperty para**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty) capturar información de error para un [objeto \_ ERROR de WS:](ws-error.md)

-   [**WS \_ ACCIÓN \_ DE PROPIEDAD DE \_ ERROR \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Especifica la acción que se va a usar para el mensaje de error. Si no se especifica, se proporciona una acción predeterminada.
-   [**WS \_ ERROR \_ DE LA PROPIEDAD \_ \_ ERROR**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Contiene la estructura [**\_ FAULT de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) que se envía en el cuerpo del mensaje de error.
-   [**WS \_ ENCABEZADO \_ DE PROPIEDAD DE \_ ERROR \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Algunos errores incluyen encabezados de mensaje que se agregan al mensaje de error para transmitir errores de procesamiento relacionados con los encabezados del mensaje de solicitud. Esta propiedad se puede usar para especificar un búfer XML de [WS \_ \_ ](ws-xml-buffer.md) que contiene un encabezado que se va a agregar al mensaje de error.

Las cadenas de error que se agregan al [objeto \_ ERROR](ws-error.md) de WS se usan como texto en el error que se envía. Las cadenas de error se pueden agregar al objeto de error mediante [**WsAddErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring).

La [**función WsSetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty) se puede usar para establecer estas propiedades del [objeto \_ ERROR de WS.](ws-error.md)

Para establecer los detalles del error almacenado en el objeto ERROR de [WS, \_](ws-error.md) use la [**función WsSetFaultErrorDetail.**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrordetail) Esta función se puede usar para asociar contenido XML arbitrario con el error.

El [host de](service-host.md) servicio enviará automáticamente errores mediante la información anterior en el objeto [ \_ WS ERROR.](ws-error.md) La [**propiedad WS \_ SERVICE PROPERTY \_ FAULT \_ \_ DISCLOSURE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) se puede usar para controlar cómo se enviarán los detalles de un error.

Si trabaja en la capa de canal, se pueden enviar errores para un objeto [ \_ WS ERROR](ws-error.md) mediante [**WsSendFaultMessageForError**](/windows/desktop/api/WebServices/nf-webservices-wssendfaultmessageforerror).

## <a name="handling-faults-on-a-client"></a>Control de errores en un cliente

Si un cliente recibe un error al usar un [proxy](service-proxy.md) de servicio o a través de [**WsRequestReply**](/windows/desktop/api/WebServices/nf-webservices-wsrequestreply) o [**WsReceiveMessage**](/windows/desktop/api/WebServices/nf-webservices-wsreceivemessage), se devolverá el error ERROR RECIBIDO DEL PUNTO DE CONEXIÓN de **WS \_ \_ \_ \_ E.** (Para obtener más información, [vea Windows valores devueltos de servicios web).](windows-web-services-return-values.md) Estas funciones también rellenarán el [objeto \_ ERROR](ws-error.md) de WS proporcionado a la llamada con información sobre el error recibido.

Las siguientes propiedades de un [objeto \_ WS ERROR](ws-error.md) se pueden consultar mediante [**WsGetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrorproperty) para obtener información sobre un error recibido:

-   [**WS \_ ACCIÓN \_ DE PROPIEDAD DE \_ ERROR \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Especifica el valor de acción del mensaje de error.
-   [**WS \_ ERROR \_ DE LA PROPIEDAD \_ \_ ERROR**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id). Contiene la estructura [**FAULT de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) que se deserializó del cuerpo del mensaje de error.

Un error puede contener contenido XML adicional arbitrario en los detalles del error. Se puede acceder a este método mediante la función [**WsGetFaultErrorDetail.**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrordetail)

## <a name="using-faults-with-messages"></a>Uso de errores con mensajes

La siguiente sección se aplica cuando se trabaja directamente con el contenido del cuerpo de un mensaje de error.

El contenido del cuerpo de un mensaje de error se representa mediante la estructura FAULT de [**WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) estándar, que tiene compatibilidad integrada para la serialización.

Por ejemplo, se puede usar el código siguiente para escribir un error en un cuerpo del mensaje:

``` syntax
HRESULT hr;
WS_ELEMENT_DESCRIPTION faultDescription = { NULL, WS_FAULT_TYPE, NULL, NULL };
WS_FAULT fault = { ... };
hr = WsWriteBody(message, &faultDescription, WS_WRITE_REQUIRED_VALUE, &fault, sizeof(fault), error);
```

El código siguiente se puede usar para leer un error de un cuerpo del mensaje:

``` syntax
HRESULT hr;
WS_ELEMENT_DESCRIPTION faultDescription = { NULL, WS_FAULT_TYPE, NULL, NULL };
WS_FAULT fault;
hr = WsReadBody(message, &faultDescription, WS_READ_REQUIRED_VALUE, &fault, sizeof(fault), error);
```

Para saber si un mensaje recibido es un error o no, se puede consultar [**WS \_ MESSAGE PROPERTY \_ IS \_ \_ FAULT.**](/windows/desktop/api/WebServices/ne-webservices-ws_message_property_id) Esta propiedad se establece en función de si el primer elemento del cuerpo es un elemento de error durante [**WsReadMessageStart**](/windows/desktop/api/WebServices/nf-webservices-wsreadmessagestart) o [**WsReadEnvelopeStart.**](/windows/desktop/api/WebServices/nf-webservices-wsreadenvelopestart)

Para crear un [**error de WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault) dado un [ \_ error de WS,](ws-error.md)use la [**función WsCreateFaultFromError.**](/windows/desktop/api/WebServices/nf-webservices-wscreatefaultfromerror)

Las enumeraciones siguientes forman parte de los errores:

-   [**DIVULGACIÓN DE ERRORES DE WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure)
-   [**IDENTIFICADOR DE PROPIEDAD \_ DE \_ ERROR \_ DE \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_error_property_id)

Las siguientes funciones forman parte de los errores:

-   [**WsCreateFaultFromError**](/windows/desktop/api/WebServices/nf-webservices-wscreatefaultfromerror)
-   [**WsGetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrordetail)
-   [**WsGetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetfaulterrorproperty)
-   [**WsSetFaultErrorDetail**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrordetail)
-   [**WsSetFaultErrorProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetfaulterrorproperty)

Las estructuras siguientes forman parte de los errores:

-   [**ERROR \_ DE WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault)
-   [**CÓDIGO DE ERROR DE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_code)
-   [**DESCRIPCIÓN DE DETALLES \_ DEL \_ ERROR DE \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_detail_description)
-   [**MOTIVO DEL ERROR DE WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_fault_reason)

 

 




