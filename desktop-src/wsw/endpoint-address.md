---
title: Dirección del extremo
description: Una dirección de punto de conexión representa la dirección de un servicio en la red.
ms.assetid: 5df9c0da-6648-42a0-ae87-06844461042a
keywords:
- Servicios web de dirección de punto de conexión para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb0bffecf49299b73863ddf32d758e4b62ceaa186b876d63e887d69c5b9ef94c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118026268"
---
# <a name="endpoint-address"></a>Dirección del extremo

Una dirección de punto de conexión representa la dirección de un servicio en la red. Al abrir un canal [,](channel.md)llamando a la función [**WsOpenChannel,**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) debe proporcionar la dirección del punto de conexión del servicio con el que se va a comunicar, así como especificar el canal que desea abrir.


Una dirección de punto de conexión consta de:

-   una [dirección URL](url.md)
-   un conjunto de encabezados (opcional)
-   un conjunto de extensiones (opcional)
-   una identidad [opcional que](endpoint-identity.md) representa la identidad de seguridad del servicio.

Cuando se dirige un mensaje, la dirección URL se convierte en el encabezado "To" del mensaje. Los encabezados que forman parte de la dirección del punto de conexión también se agregan al mensaje.

![Diagrama que muestra los encabezados de dirección de punto de conexión que se agregan a un mensaje.](images/endpointaddress.png)

Los canales direcciona automáticamente los mensajes que se envían mediante la estructura [**\_ DE DIRECCIÓN \_**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) DEL PUNTO DE CONEXIÓN de WS que se pasó a [**WsOpenChannel.**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) También puede usar la función [**WsAddressMessage para**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) invalidar este comportamiento predeterminado.

Cuando se pasa [**WS \_ ENDPOINT \_ ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) como parámetro, las funciones [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) y [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) crean una copia del parámetro **WS \_ ENDPOINT \_ ADDRESS** en memoria y su tamaño está limitado por 65536 bytes. [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) no tiene esta limitación porque no requiere la creación de una copia del parámetro **ENDPOINT \_ ADDRESS \_ de WS.**

Las extensiones especificadas  en el campo extensiones de [**WS \_ ENDPOINT \_ ADDRESS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) no se usan para dirigir el mensaje, sino que son un mecanismo de extensibilidad que se puede usar para proporcionar información adicional (por ejemplo, metadatos) sobre el servicio. Las extensiones comunes se pueden leer con la [**función WsReadEndpointAddressExtension.**](/windows/desktop/api/WebServices/nf-webservices-wsreadendpointaddressextension)

El campo de identidad opcional de la dirección del punto de conexión puede incluir, por ejemplo, el nombre DNS de la máquina en la que se ejecuta el servicio o el UPN de la cuenta de Windows con la que se ejecuta el servicio. El campo identity no se usa para direccionar el mensaje, pero se puede usar para obtener un token de seguridad para el servicio (por ejemplo, para obtener un vale Kerberos al UPN de destino) y para comprobar la identidad del servicio responde (por ejemplo, una identidad DNS usada para las comprobaciones de nombre en el certificado de servicio devuelto durante SSL).

Las direcciones de punto de conexión se pueden leer y escribir mediante [la serialización](serialization.md) con el valor de enumeración **\_ WS ENDPOINT \_ ADDRESS \_ TYPE** de [**WS \_ TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type). Tenga en cuenta que, para serializar una dirección de punto de conexión, debe conocer la versión de la especificación utilizada para los encabezados de direccionamiento, como se especifica en la enumeración [**WS \_ ADDRESSING \_ VERSION.**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version)

 

 




