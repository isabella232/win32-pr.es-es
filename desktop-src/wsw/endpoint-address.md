---
title: Dirección del extremo
description: Una dirección de punto de conexión representa la dirección de un servicio en la red.
ms.assetid: 5df9c0da-6648-42a0-ae87-06844461042a
keywords:
- Servicios Web de la dirección de extremo para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 787326197bc73d57945720c34773d33b613a4aab
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "104558018"
---
# <a name="endpoint-address"></a>Dirección del extremo

Una dirección de punto de conexión representa la dirección de un servicio en la red. Al abrir un [canal](channel.md)mediante una llamada a la función [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) , debe proporcionar la dirección del punto de conexión del servicio con el que se va a comunicar, así como especificar el canal que desea abrir.


Una dirección de punto de conexión consta de:

-   una [dirección URL](url.md)
-   un conjunto de encabezados (opcional)
-   un conjunto de extensiones (opcional)
-   [identidad](endpoint-identity.md) opcional que representa la identidad de seguridad del servicio.

Cuando se trata de un mensaje, la dirección URL se convierte en el encabezado "para" del mensaje. Todos los encabezados que forman parte de la dirección del punto de conexión también se agregan al mensaje.

![Diagrama que muestra los encabezados de dirección de extremo que se agregan a un mensaje.](images/endpointaddress.png)

Los canales abordan automáticamente los mensajes que se envían mediante la estructura de [**\_ \_ direcciones del punto de conexión de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) que se pasó a [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel). También puede usar la función [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) para invalidar este comportamiento predeterminado.

Cuando se pasa la [**\_ \_ dirección del punto de conexión de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) como parámetro, las funciones [**WsOpenChannel**](/windows/desktop/api/WebServices/nf-webservices-wsopenchannel) y [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) crean una copia del parámetro de dirección del **punto de \_ conexión \_ de WS** en la memoria y su tamaño está limitado por 65536 bytes. [**WsAddressMessage**](/windows/desktop/api/WebServices/nf-webservices-wsaddressmessage) no tiene esta limitación porque no requiere la creación de una copia del parámetro de **\_ \_ dirección del punto de conexión de WS** .

Las extensiones especificadas en el campo **extensiones** de la [**dirección del punto de \_ conexión \_ de WS**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) no se usan para direccionar el mensaje, sino que son un mecanismo de extensibilidad que se puede usar para proporcionar información adicional (por ejemplo, metadatos) sobre el servicio. Las extensiones comunes se pueden leer con la función [**WsReadEndpointAddressExtension**](/windows/desktop/api/WebServices/nf-webservices-wsreadendpointaddressextension) .

El campo de identidad opcional de la dirección del extremo puede incluir, por ejemplo, el nombre DNS del equipo en el que se ejecuta el servicio o el UPN de la cuenta de Windows con la que se está ejecutando el servicio. El campo identidad no se utiliza para direccionar el mensaje, pero se puede usar para obtener un token de seguridad para el servicio (por ejemplo, para obtener un vale de Kerberos para el UPN de destino) y para comprobar la identidad de las respuestas del servicio (por ejemplo, una identidad DNS utilizada para las comprobaciones de nombres en el certificado de servicio devuelto durante SSL).

Las direcciones de punto de conexión se pueden leer y escribir mediante la [serialización](serialization.md) con el valor de enumeración de **\_ tipo de \_ dirección \_ de extremo WS** de [**\_ tipo WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type). Nota para serializar una dirección de extremo, debe conocer la versión de la especificación utilizada para los encabezados de direccionamiento, tal como se especifica en la enumeración de la [**versión de WS \_ Addressing \_**](/windows/desktop/api/WebServices/ne-webservices-ws_addressing_version) .

 

 




