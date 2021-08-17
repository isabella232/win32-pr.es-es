---
description: En este tema se describe cómo WSDAPI implementa la funcionalidad optativa en la especificación perfil de dispositivos para servicios web (DPWS). También se describe qué funcionalidad de DPWS se omitió de la implementación de WSDAPI.
ms.assetid: 54d51e56-8022-4696-b488-4b3a226224d8
title: Cumplimiento de la especificación de DPWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce59ba29e8e36fd5030732c0b61a2dfd164d9c887bdd9881a775c8b1ce6ec353
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130837"
---
# <a name="dpws-specification-compliance"></a>Cumplimiento de la especificación de DPWS

En este tema se describe cómo WSDAPI implementa la funcionalidad optativa en la especificación perfil [de](https://specs.xmlsoap.org/ws/2006/02/devprof/) dispositivos para servicios web (DPWS). También se describe qué funcionalidad de DPWS se omitió de la implementación de WSDAPI.

La especificación DPWS proporciona una manera coherente de enviar mensajes con dispositivos. También agrega restricciones y recomendaciones específicas que simplifican el proceso de compatibilidad de servicios web en hardware incrustado.

La especificación DPWS describe la funcionalidad optativa mediante los términos MAY o SHOULD en una recomendación o restricción de implementación determinada. La funcionalidad omitida puede ser una funcionalidad descrita como REQUIRED en la especificación de DPWS que no se implementó por WSDAPI, o bien puede ser una funcionalidad que WSDAPI implementó en un método distinto del especificado en la especificación DPWS.

En este tema se sigue el diseño de la sección por sección de DPWS. En cada sección se describe cómo la implementación de WSDAPI controla las restricciones, los requisitos y la funcionalidad optativa específicos. Este tema se lee mejor junto con la especificación de DPWS.

## <a name="dpws-30-messaging"></a>Mensajería de DPWS 3.0

### <a name="dpws-31-uri-formats"></a>Formatos de URI de DPWS 3.1

Las restricciones R0025 y R0027 restringen los URI a octetos MAX \_ URI \_ SIZE. WSDAPI aplica ambas restricciones según lo especificado.

### <a name="dpws-32-udp-messaging"></a>Mensajería UDP de DPWS 3.2

La recomendación R0029 sugiere que no se deben enviar paquetes UDP mayores que la unidad de transferencia máxima (MTU) para UDP. WSDAPI no implementa esta recomendación y permitirá que las implementaciones envíen y reciban mensajes de detección mayores que la MTU.

### <a name="dpws-33-http-messaging"></a>Mensajería HTTP de DPWS 3.3

R0001 requiere que los servicios admitan la transferencia fragmentada. WSDAPI acepta datos fragmentados en los mensajes de solicitud y enviará datos fragmentados en los mensajes de solicitud.

R0012 y R0013 describen las partes necesarias del enlace HTTP de SOAP. Para R0012, WSDAPI implementa el enlace HTTP SOAP, pero no comenzará a leer la respuesta HTTP hasta que WSDAPI haya terminado de enviar la solicitud HTTP. WSDAPI implementa el patrón de intercambio de mensajes necesario en R0013, implementa el nodo SOAP de respuesta opcional en R0014 y no implementa la característica de método web opcional en R0015. WSDAPI también admite los requisitos de R0030 y R0017.

### <a name="dpws-34-soap-envelope"></a>Sobre SOAP de DPWS 3.4

WSDAPI admite R0034 y aplica R0003 y R0026 de forma predeterminada. Más concretamente, de acuerdo con R0003 y R0026, si WSDAPI recibe un sobre SOAP mayor que MAX ENVELOPE SIZE a través de HTTP, se rechaza y se cierra la \_ \_ conexión.

### <a name="dpws-35-ws-addressing"></a>DPWS 3.5 WS-Addressing

R0004 refleja el uso recomendado de la API de dispositivo en WSDAPI y es compatible con la API de cliente en WSDAPI. Puesto que se trata de una recomendación, WSDAPI permitirá a los clientes y dispositivos usar URI que no son URI para sus puntos de conexión de dispositivo a fin de `urn:uuid` garantizar la máxima compatibilidad. Dado que la API de dispositivo en WSDAPI no conserva el estado entre inicializaciones, son los desarrolladores de aplicaciones los que usan la API de dispositivo en WSDAPI para asegurarse de que R0005 y R0006 se admiten correctamente. La API de cliente de WSDAPI asumirá que las identidades de dispositivo son únicas y persistentes, y la funcionalidad que se cree en la API de cliente en WSDAPI (como PnP-X) requerirá esto para reconocer correctamente el dispositivo en los reinicios del dispositivo.

R0007 recomienda evitar el uso de propiedades de referencia en las referencias de punto de conexión. WSDAPI todavía reconocerá y aceptará puntos de conexión con propiedades de referencia, y los desarrolladores pueden optar por usarlos, pero de forma predeterminada WSDAPI no los rellenará en los puntos de conexión que cree. Del mismo modo, con R0042, cuando WSDAPI crea puntos de conexión de servicio, usará una dirección de transporte HTTP o HTTPS, pero no requerirá que los dispositivos usen direcciones de transporte HTTP o HTTPS en sus puntos de conexión de servicio. El comportamiento del cliente al intentar comunicarse con un servicio que no usa HTTP o HTTPS es indefinido.

En caso de errores, R0031 restringe el punto de conexión de respuesta y describe el error que se va a enviar si el error no es anónimo. WSDAPI fuerza al punto de conexión de respuesta a usar el valor correcto al enviar mensajes y se mostrará un error correctamente si WSDAPI recibe un mensaje de solicitud con el punto de conexión de respuesta incorrecto. R0041 ofrece a las implementaciones la opción de quitar un error si el punto de conexión de respuesta no es válido. En lugar de quitar el error, WSDAPI enviará el error de vuelta en el canal de solicitud, dirigido al punto de conexión anónimo, como un "mejor esfuerzo" para comunicarse con el cliente.

Por último, hay dos restricciones en los encabezados SOAP, R0019 y R0040, que WSDAPI cumple y aplica en los mensajes recibidos.

### <a name="dpws-36-attachments"></a>Datos adjuntos de DPWS 3.6

WSDAPI admite datos adjuntos y cumple con R0022. WSDAPI también cumple con R0037. Al enviar datos adjuntos, WSDAPI siempre establecerá la codificación de transferencia de contenido en "binario" para todas las partes MIME. Sin embargo, WSDAPI no aplica R0036. El comportamiento de WSDAPI al recibir una parte MIME con una codificación de transferencia de contenido no establecida en "binario" no está definido.

DPWS también define cláusulas de ordenación de partes MIME. Para R0038, WSDAPI aplicará el orden de las partes y rechazará un mensaje MIME si el sobre SOAP no es la primera parte MIME. Para R0039, WSDAPI siempre enviará el sobre SOAP como la primera parte MIME.

## <a name="dpws-40-discovery"></a>Detección de DPWS 4.0

R1013 y R1001 diferencian la detección de dispositivos y la detección de servicios. WSDAPI cumple con R1013. La implementación de hospedaje cumple con R1001, pero WSDAPI no aplica esta recomendación en el cliente.

DPWS también proporciona instrucciones sobre los tipos y las reglas de coincidencia de ámbito. WSDAPI admite todas las reglas de coincidencia de ámbito definidas en [WS-Discovery excepto](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) LDAP. WSDAPI también proporciona un modelo extensible para definir reglas de coincidencia de ámbito personalizadas, lo que cumple con R1019. La API de hospedaje también siempre proporcionará el tipo de detección por R1020, pero la API de cliente no requiere `wsdp:Device` que esté presente. Otras aplicaciones creadas en WSDAPI, como PnP-X, tienen un requisito difícil de que el tipo esté `wsdp:Device` presente en la detección.

Para facilitar la detección y el enlace, WSDAPI admite R1009 y R1016. Según R1018, WSDAPI omitirá udp de multidifusión no enviado a la dirección anónima. R1015, R1021 y R1022 definen un enlace HTTP para el mensaje probe, que WSDAPI admite como se describe.

## <a name="dpws-50-description"></a>Descripción de DPWS 5.0

WSDAPI aplica R2044 en el cliente. En el lado de hospedaje, WSDAPI solo proporcionará nunca el `wsx:Metadata` elemento en el cuerpo del sobre SOAP. R2045 permite que los dispositivos admitan un subconjunto de la [funcionalidad WS-Transfer.](https://specs.xmlsoap.org/ws/2004/09/transfer/WS-Transfer.pdf) La API de hospedaje siempre generará el `wsa:ActionNotSupported` error.

### <a name="dpws-51-characteristics"></a>Características de DPWS 5.1

DPWS describe las características básicas del dispositivo. Además de las restricciones descritas en este tema, se definen límites de longitud para cadenas y URI específicos. WSDAPI aplica los límites de longitud de esta sección 5.1 de DPWS, ya sea antes de enviar el mensaje o después de analizar su contenido.

DPWS también describe las secciones de metadatos necesarias y el ciclo de la versión de metadatos. La implementación del cliente exige la presencia de los metadatos ThisModel y ThisDevice. La implementación de hospedaje también administra correctamente la versión de metadatos y siempre proporciona estas secciones, de acuerdo con R2038, R2012, R2001, R2039, R2014 y R2002.

### <a name="dpws-52-hosting"></a>Hospedaje de DPWS 5.2

En esta sección se describe la jerarquía de servicios y metadatos de relación. WSDAPI no aplica la unidad de ServiceId como se describe en esta sección en el cliente o en el lado del dispositivo.

WSDAPI cumple con R2040 y es posible que la implementación de hospedaje envíe una respuesta de metadatos sin ninguna relación si no hay servicios hospedados. La implementación del cliente acepta correctamente la respuesta de metadatos.

R2029 permite varias secciones de relación en una respuesta de metadatos, que WSDAPI aceptará correctamente. R2030 y R2042 describen la administración de la versión de metadatos, que se implementa correctamente en la API de hospedaje.

### <a name="dpws-53-wsdl"></a>DPWS 5.3 WSDL

Si un servicio proporciona datos del Lenguaje de descripción de servicios Web (WSDL), las implementaciones de cliente pueden obtener la definición del servicio y manipular el servicio sobre la marcha. Los clientes enlazados en tiempo de tarde lo usan. La implementación del cliente WSDAPI aceptará WSDL proporcionado desde un servicio, pero el cliente no lo valida y el cliente no proporciona un modelo de programación enlazado en tiempo de ejecución. La implementación de hospedaje se puede usar para proporcionar WSDL, pero no es necesario que el host lo haga, ya que el propio host no administra los metadatos del nivel de servicio.

### <a name="dpws-54-ws-policy"></a>DPWS 5.4 WS-Policy

DPWS describe las aserciones de directiva que se usarán para los dispositivos. Puesto que WSDAPI no proporciona y no interpreta WSDL, no puede reconocer ni aplicar la directiva incrustada en datos WSDL.

## <a name="dpws-60-eventing"></a>Eventos de DPWS 6.0

### <a name="dpws-61-subscription"></a>Suscripción a DPWS 6.1

DPWS requiere compatibilidad con la entrega push. WSDAPI implementa la entrega push en el lado del servicio, cumpliendo así con R3009 y R3010, y solo aceptará el modo de entrega push en el lado cliente. R3017 y R3018 requieren errores específicos del servicio si no reconoce las `NotifyTo` direcciones `EndTo` o . WSDAPI no valida estas direcciones por adelantado y no generará estos errores. Sin embargo, la implementación del cliente reconocerá estos errores correctamente. Del mismo modo, R3019 es opcional y WSDAPI no implementa esta recomendación, pero la implementación del cliente reconocerá correctamente el mensaje y notificará a la aplicación de un error de `SubscriptionEnd` entrega.

### <a name="dpws-611-filtering"></a>Filtrado de DPWS 6.1.1

WSDAPI cumple con R3008 e implementa el `Action` filtro. En cumplimiento con R3011 y R3012, WSDAPI no generará los errores en las condiciones indicadas. WSDAPI también implementa el error descrito en R3020 si no reconoce las acciones en las que se le pide que filtre.

### <a name="dpws-62-subscription-duration-and-renewal"></a>Duración y renovación de la suscripción de DPWS 6.2

WSDAPI cumple con R3005, R3006 y R3016. WSDAPI siempre usará , pero aceptará si se proporciona y, por tanto, no emitirá `xs:duration` el error opcional en `xs:dateTime` R3013. WSDAPI admite `GetStatus` y no emitirá el `wsa:ActionNotSupported` error por R3015. WSDAPI acepta el `wsa:ActionNotSupported` error si un servicio responde a una solicitud con `GetStatus` él.

## <a name="dpws-70-security"></a>Seguridad de DPWS 7.0

DPWS describe un modelo de seguridad recomendado para dispositivos. WSDAPI no implementa estas recomendaciones como se describe y no aplica las restricciones de esta sección como se describe.

## <a name="dpws-appendix-i"></a>Apéndice I de DPWS

DPWS modifica las constantes globales de otras especificaciones para adaptarse a los dispositivos. WSDAPI usa las constantes de esta sección e invalida las constantes predeterminadas en la implementación de [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) con estas constantes. Las aplicaciones que usan WSDAPI para WS-Discovery se enlazarán a las constantes definidas en DPWS, no a las constantes definidas en [WS-Discovery.](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)

 

 



