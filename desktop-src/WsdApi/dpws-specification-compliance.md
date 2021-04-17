---
description: En este tema se describe cómo WSDAPI implementa la funcionalidad optativa en la especificación del perfil de dispositivos para servicios web (DPWS). También describe qué funcionalidad de DPWS se ha omitido de la implementación de WSDAPI.
ms.assetid: 54d51e56-8022-4696-b488-4b3a226224d8
title: Compatibilidad con la especificación DPWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ed26e57a0f7a94069e802f96f346a3a5eca67b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697309"
---
# <a name="dpws-specification-compliance"></a>Compatibilidad con la especificación DPWS

En este tema se describe cómo WSDAPI implementa la funcionalidad optativa en la especificación del [Perfil de dispositivos para servicios web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS). También describe qué funcionalidad de DPWS se ha omitido de la implementación de WSDAPI.

La especificación DPWS proporciona una manera coherente de mensajes con dispositivos. También agrega restricciones y recomendaciones específicas que simplifican el proceso de admitir servicios web en hardware incrustado.

La especificación DPWS describe la funcionalidad optativa mediante el uso de los términos que se pueden o deben tener en una recomendación o restricción de implementación determinada. La funcionalidad omitida puede ser la que se describe en la especificación de DPWS que no ha implementado WSDAPI, o puede ser una funcionalidad que WSDAPI se implementó en un método que no se haya especificado en la especificación DPWS.

En este tema se sigue el diseño de la sección DPWS en la sección. En cada sección se describe cómo se administran las restricciones específicas, los requisitos y la funcionalidad optativa en la implementación de WSDAPI. Este tema se lee mejor en conjunto con la especificación DPWS.

## <a name="dpws-30-messaging"></a>Mensajería de DPWS 3,0

### <a name="dpws-31-uri-formats"></a>Formatos de URI de DPWS 3,1

Restricciones R0025 y R0027 restringen los URI a \_ los \_ octetos de tamaño máximo de URI. WSDAPI impone ambas restricciones según lo especificado.

### <a name="dpws-32-udp-messaging"></a>Mensajería UDP de DPWS 3,2

Recomendación R0029 sugiere que no se deben enviar paquetes UDP mayores que la unidad de transmisión máxima (MTU) para UDP. WSDAPI no implementa esta recomendación y permitirá a las implementaciones enviar y recibir mensajes de detección mayores que la MTU.

### <a name="dpws-33-http-messaging"></a>Mensajería HTTP de DPWS 3,3

R0001 requiere que los servicios admitan la transferencia fragmentada. WSDAPI acepta datos fragmentados en mensajes de solicitud y enviará datos fragmentados en los mensajes de solicitud.

R0012 y R0013 describen las partes necesarias del enlace HTTP SOAP. En el caso de R0012, WSDAPI implementa el enlace HTTP SOAP, pero no comenzará a leer la respuesta HTTP hasta que WSDAPI haya terminado de enviar la solicitud HTTP. WSDAPI implementa el patrón de intercambio de mensajes necesario en R0013, implementa el nodo SOAP de respuesta opcional en R0014 y no implementa la característica de método Web opcional en R0015. WSDAPI también admite los requisitos de R0030 y R0017.

### <a name="dpws-34-soap-envelope"></a>Sobre DPWS 3,4 SOAP

WSDAPI admite R0034 y aplica R0003 y R0026 de forma predeterminada. Más concretamente, de acuerdo con R0003 y R0026, si WSDAPI recibe un sobre SOAP que es mayor que \_ el tamaño de sobre máximo \_ en http, se rechaza y se cierra la conexión.

### <a name="dpws-35-ws-addressing"></a>DPWS 3,5 WS-Addressing

R0004 refleja el uso recomendado de la API de dispositivo en WSDAPI y es compatible con la API de cliente en WSDAPI. Dado que se trata de una recomendación, WSDAPI permitirá a los clientes y dispositivos usar URI distintos de `urn:uuid` los URI para sus puntos de conexión de dispositivo para garantizar la máxima compatibilidad. Dado que la API de dispositivo en WSDAPI no conserva el estado entre inicializaciones, depende de los desarrolladores de aplicaciones que usan la API de dispositivo en WSDAPI para asegurarse de que R0005 y R0006 se admiten correctamente. La API de cliente en WSDAPI supondrá que las identidades de dispositivo son únicas y se conservan, y la funcionalidad que se basa en la API de cliente en WSDAPI (como PnP-X) requerirá esto para reconocer correctamente el dispositivo a través de los reinicios del dispositivo.

R0007 recomienda el uso de propiedades de referencia en referencias de extremo. WSDAPI seguirá reconociendo y aceptará puntos de conexión con propiedades de referencia, y los desarrolladores pueden optar por usarlos, pero de forma predeterminada WSDAPI no los rellenará en los puntos de conexión que crea. De forma similar, con R0042, cuando WSDAPI crea puntos de conexión de servicio, usará una dirección de transporte HTTP o HTTPS, pero no necesitará que los dispositivos usen direcciones de transporte HTTP o HTTPS en sus puntos de conexión de servicio. El comportamiento del cliente al intentar comunicarse con un servicio que no usa HTTP o HTTPS no está definido.

En los errores, R0031 restringe el punto de conexión de respuesta y describe el error que se va a enviar si el error no es anónimo. WSDAPI fuerza al extremo de la respuesta a usar el valor correcto al enviar mensajes y generará un error correctamente si WSDAPI recibe un mensaje de solicitud con el extremo de respuesta incorrecto. R0041 proporciona a las implementaciones la opción de quitar un error si el punto de conexión de respuesta no es válido. En lugar de quitar el error, WSDAPI devolverá el error en el canal de solicitud, dirigido al extremo anónimo, como un "mejor esfuerzo" para comunicarse con el cliente.

Por último, hay dos restricciones en los encabezados SOAP, R0019 y R0040, que WSDAPI cumple con y aplica en los mensajes recibidos.

### <a name="dpws-36-attachments"></a>Datos adjuntos de DPWS 3,6

WSDAPI admite datos adjuntos y cumple con R0022. WSDAPI también cumple con R0037. Al enviar datos adjuntos, WSDAPI siempre establecerá la codificación de transferencia de contenido en "binario" para todas las partes MIME. Sin embargo, WSDAPI no aplica R0036. El comportamiento de WSDAPI al recibir una parte MIME con una codificación de transferencia de contenido no establecida en "binario" es indefinido.

DPWS también define cláusulas de ordenación de partes MIME. En el caso de R0038, WSDAPI aplicará el orden de las partes y rechazará un mensaje MIME si la envoltura SOAP no es la primera parte MIME. En el caso de R0039, WSDAPI siempre enviará la envoltura SOAP como la primera parte MIME.

## <a name="dpws-40-discovery"></a>Detección de DPWS 4,0

R1013 y R1001 diferencian la detección de dispositivos y la detección de servicios. WSDAPI es compatible con R1013. La implementación de hospedaje es compatible con R1001, pero WSDAPI no aplica esta recomendación en el cliente.

DPWS también proporciona instrucciones sobre tipos y reglas de coincidencia de ámbito. WSDAPI es compatible con todas las reglas de coincidencia de ámbito definidas en [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) excepto LDAP. WSDAPI también proporciona un modelo extensible para definir reglas de coincidencia de ámbito personalizado, con lo que se cumple con R1019. La API de hospedaje también proporcionará siempre el `wsdp:Device` tipo de detección por R1020, pero la API de cliente no requiere que esté presente. Otras aplicaciones basadas en WSDAPI, como PnP-X, tienen un requisito difícil para que el `wsdp:Device` tipo esté presente en la detección.

Para facilitar la detección y el enlace, WSDAPI es compatible con R1009 y R1016. Por R1018, WSDAPI omitirá UDP de multidifusión que no se envía a la dirección anónima. R1015, R1021 y R1022 definen un enlace HTTP para el mensaje de sondeo, que WSDAPI admite como se describe.

## <a name="dpws-50-description"></a>Descripción de DPWS 5,0

WSDAPI aplica R2044 en el cliente. En el lado del host, WSDAPI solo proporcionará el `wsx:Metadata` elemento en el cuerpo de la envoltura SOAP. R2045 permite que los dispositivos admitan un subconjunto de la funcionalidad de [WS-Transfer](https://specs.xmlsoap.org/ws/2004/09/transfer/WS-Transfer.pdf) . La API de hospedaje siempre generará el `wsa:ActionNotSupported` error.

### <a name="dpws-51-characteristics"></a>Características de DPWS 5,1

DPWS describe las características básicas del dispositivo. Además de las restricciones descritas en este tema, se definen los límites de longitud para cadenas y URI específicos. WSDAPI aplica los límites de longitud en esta sección 5,1 de DPWS, antes de enviar el mensaje o después de analizar su contenido.

DPWS también describe las secciones de metadatos necesarias y el ciclo de la versión de los metadatos. La implementación del cliente exige la presencia de metadatos de ThisModel y ThisDevice. La implementación de hospedaje también administra correctamente la versión de los metadatos y siempre proporciona estas secciones, que cumplen con R2038, R2012, R2001, R2039, R2014 y R2002.

### <a name="dpws-52-hosting"></a>Hospedaje de DPWS 5,2

En esta sección se describe la jerarquía de servicios y metadatos de relación. WSDAPI no exige la unicidad de ServiceId tal y como se describe en esta sección, tanto en el lado cliente como en el dispositivo.

WSDAPI cumple con R2040 y es posible que la implementación de hospedaje envíe una respuesta de metadatos sin ninguna sección de relación si no hay ningún servicio hospedado. La implementación del cliente acepta correctamente la respuesta de los metadatos.

R2029 permite varias secciones de relación en una respuesta de metadatos, que WSDAPI aceptará correctamente. R2030 y R2042 describen la administración de la versión de metadatos, que se implementa correctamente en la API de hospedaje.

### <a name="dpws-53-wsdl"></a>DPWS 5,3 WSDL

Si un servicio proporciona datos del lenguaje de descripción de servicios web (WSDL), las implementaciones del cliente pueden obtener la definición del servicio y manipular el servicio sobre la marcha. Lo usan los clientes enlazados en tiempo de ejecución. La implementación del cliente WSDAPI aceptará el WSDL proporcionado desde un servicio, pero el cliente no lo valida y el cliente no proporciona un modelo de programación enlazado en tiempo de ejecución. La implementación de hospedaje se puede usar para proporcionar WSDL, pero no es necesario que el host lo haga, ya que el propio host no administra los metadatos de nivel de servicio.

### <a name="dpws-54-ws-policy"></a>DPWS 5,4 WS-Policy

DPWS describe las aserciones de directiva que se van a usar para los dispositivos. Dado que WSDAPI no proporciona y no interpreta WSDL, no puede reconocer ni aplicar directivas incrustadas en datos WSDL.

## <a name="dpws-60-eventing"></a>Eventos de DPWS 6,0

### <a name="dpws-61-subscription"></a>Suscripción a DPWS 6,1

DPWS requiere compatibilidad con la entrega de la extracción. WSDAPI implementa la entrega de inserciones en el lado del servicio, con lo que se cumple con R3009 y R3010, y solo acepta el modo de entrega de inserciones en el lado cliente. R3017 y R3018 requieren errores específicos del servicio si no reconoce las `NotifyTo` `EndTo` direcciones o. WSDAPI no valida estas direcciones por adelantado y no generará estos errores. Sin embargo, la implementación del cliente reconocerá correctamente estos errores. Del mismo modo, R3019 es opcional y WSDAPI no implementa esta recomendación, pero la implementación del cliente reconocerá correctamente el `SubscriptionEnd` mensaje y notificará a la aplicación un error de entrega.

### <a name="dpws-611-filtering"></a>Filtrado de DPWS 6.1.1

WSDAPI cumple con R3008 e implementa el `Action` filtro. En cumplimiento con R3011 y R3012, WSDAPI no generará los errores en las condiciones indicadas. WSDAPI también implementa el error descrito R3020 si no reconoce las acciones en las que se le pide que filtre.

### <a name="dpws-62-subscription-duration-and-renewal"></a>Duración y renovación de la suscripción a DPWS 6,2

WSDAPI cumple con R3005, R3006 y R3016. WSDAPI usará siempre `xs:duration` , pero aceptará `xs:dateTime` si se proporciona y, por lo tanto, no emitirá el error opcional en R3013. WSDAPI admite `GetStatus` y no emitirá el `wsa:ActionNotSupported` error por R3015. WSDAPI acepte el `wsa:ActionNotSupported` error si un servicio responde a una `GetStatus` solicitud con él.

## <a name="dpws-70-security"></a>Seguridad de DPWS 7,0

DPWS describe un modelo de seguridad recomendado para dispositivos. WSDAPI no implementa estas recomendaciones, tal y como se describe, y no aplica las restricciones en esta sección, tal y como se describe.

## <a name="dpws-appendix-i"></a>DPWS Apéndice I

DPWS modifica las constantes globales de otras especificaciones para que se adapten a los dispositivos. WSDAPI usa las constantes de esta sección y reemplaza las constantes predeterminadas en la implementación de [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) con estas constantes. Las aplicaciones que usan WSDAPI para WS-Discovery se enlazarán a las constantes definidas en DPWS, no a las constantes definidas en [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

 

 



