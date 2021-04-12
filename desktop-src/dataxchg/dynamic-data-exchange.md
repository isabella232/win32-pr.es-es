---
title: Intercambio dinámico de datos
description: En esta sección se proporcionan instrucciones para implementar el intercambio dinámico de datos para aplicaciones que no pueden usar la biblioteca de administración de Intercambio dinámico de datos (DDEML).
ms.assetid: vs|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchange.htm
keywords:
- Intercambio dinámico de datos (DDE), acerca de
- DDE (Intercambio dinámico de datos), acerca de
- intercambio de datos, Intercambio dinámico de datos (DDE)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d5fa52078c2fa1d2e67a74d019535c801c4c96
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357186"
---
# <a name="dynamic-data-exchange"></a>Intercambio dinámico de datos

En esta sección se proporcionan instrucciones para implementar el intercambio dinámico de datos para aplicaciones que no pueden usar la biblioteca de administración de Intercambio dinámico de datos (DDEML). Para obtener más información acerca de DDEML, consulte [biblioteca de administración de intercambio dinámico de datos](dynamic-data-exchange-management-library.md).

### <a name="overviews"></a>Temas de introducción



| Nombre                                                           | Descripción                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------|
| [Acerca de Intercambio dinámico de datos](about-dynamic-data-exchange.md) | Describe la transferencia de datos entre aplicaciones.<br/>       |
| [Usar Intercambio dinámico de datos](using-dynamic-data-exchange.md) | Proporciona ejemplos de código relacionados con el intercambio dinámico de datos.<br/> |
| [Referencia DDE](dynamic-data-exchange-reference.md)           | Referencia de la API.<br/>                                      |



 

### <a name="dde-functions"></a>Funciones DDE



| Nombre                                                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DdeSetQualityOfService**](/windows/desktop/api/Dde/nf-dde-ddesetqualityofservice)         | Especifica la calidad de servicio (QOS) que una aplicación de Intercambio dinámico de datos sin formato (DDE) previene para futuras conversaciones DDE que inicia. La QOS especificada se aplica a todas las conversaciones iniciadas mientras se realiza la configuración. La calidad de servicio de una conversación DDE dura mientras dure la conversación. las llamadas a la función [**DdeSetQualityOfService**](/windows/desktop/api/Dde/nf-dde-ddesetqualityofservice) durante una conversación no afectan a la QoS de la conversación. <br/> |
| [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)                           | Libera la memoria especificada por el parámetro *lParam* de un mensaje DDE expuesto. Una aplicación que recibe un mensaje DDE expuesto debe llamar a esta función después de que haya usado la función [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) para desempaquetar el valor *lParam* . <br/>                                                                                                                                                                                                     |
| [**ImpersonateDdeClientWindow**](/windows/desktop/api/Dde/nf-dde-impersonateddeclientwindow) | Permite a una aplicación de servidor DDE suplantar el contexto de seguridad de una aplicación cliente DDE. Esto protege los datos de servidor seguros de los clientes de DDE no autorizados. <br/>                                                                                                                                                                                                                                                                                                      |
| [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)                           | Empaqueta un valor *lParam* de DDE en una estructura interna utilizada para compartir datos DDE entre procesos.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)                         | Permite a una aplicación volver a usar un parámetro *lParam* de DDE empaquetado, en lugar de asignar un nuevo *lParam* empaquetado. El uso de esta función reduce las reasignaciones de las aplicaciones que pasan mensajes DDE empaquetados. <br/>                                                                                                                                                                                                                                                          |
| [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)                       | Desempaqueta un valor *lParam* de DDE recibido de un mensaje DDE publicado. <br/>                                                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="dde-messages"></a>Mensajes DDE



| Nombre                                         | Descripción                                                                                                                                                                                                                                                                                      |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Inicio de WM \_ DDE \_**](wm-dde-initiate.md) | Inicia una conversación con una aplicación de servidor que responde a la aplicación y a los nombres de tema especificados. Al recibir este mensaje, se espera que todas las aplicaciones de servidor con nombres que coincidan con la aplicación especificada y que admitan el tema especificado lo confirmen.<br/> |



 

### <a name="dde-notifications"></a>Notificaciones DDE



| Nombre                                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_confirmación de DDE de WM \_**](wm-dde-ack.md)             | Nnotifies una aplicación DDE de la recepción y el procesamiento de los siguientes mensajes: [**WM DDE de WM, ejecución de \_ \_**](wm-dde-poke.md) [**WM \_ DDE \_ Ejecutar**](wm-dde-execute.md), [**\_ \_ datos de DDE**](wm-dde-data.md)de WM, [**\_ \_ aviso de DDE**](wm-dde-advise.md)de WM, [**\_ \_ desaconsejar**](wm-dde-unadvise.md)DDE de WM, [**Inicio de WM \_ DDE \_**](wm-dde-initiate.md)o [**\_ \_ solicitud de DDE de WM**](wm-dde-request.md) (en algunos casos). <br/> |
| [**\_aviso de DDE de WM \_**](wm-dde-advise.md)       | Una aplicación cliente DDE envía el mensaje de [**\_ \_ aviso de DDE de WM**](wm-dde-advise.md) a una aplicación de servidor DDE para solicitar al servidor que proporcione una actualización para un elemento de datos cada vez que cambie el elemento. <br/>                                                                                                                                                                                                              |
| [**\_datos DDE de WM \_**](wm-dde-data.md)           | Una aplicación de servidor DDE envía un mensaje de [**\_ \_ datos DDE de WM**](wm-dde-data.md) a una aplicación cliente DDE para pasar un elemento de datos al cliente o para notificar al cliente la disponibilidad de un elemento de datos. <br/>                                                                                                                                                                                                           |
| [**ejecución de WM \_ DDE \_**](wm-dde-execute.md)     | Una aplicación cliente DDE envía un mensaje de [**\_ \_ ejecución de WM DDE**](wm-dde-execute.md) a una aplicación de servidor DDE para enviar una cadena al servidor que se va a procesar como una serie de comandos. Se espera que la aplicación de servidor publique un mensaje de [**\_ \_ confirmación de WM DDE**](wm-dde-ack.md) en respuesta. <br/>                                                                                                                      |
| [**hiperdinámico de WM \_ \_**](wm-dde-poke.md)           | Una aplicación cliente DDE envía un mensaje de mensaje de error de [**WM \_ DDE \_**](wm-dde-poke.md) a una aplicación de servidor DDE. Un cliente usa este mensaje para solicitar al servidor que acepte un elemento de datos no solicitado. Se espera que el servidor responda con un mensaje de [**\_ \_ confirmación de DDE de WM**](wm-dde-ack.md) que indica si aceptó el elemento de datos. <br/>                                                                                   |
| [**\_solicitud de DDE de WM \_**](wm-dde-request.md)     | Una aplicación cliente DDE envía un mensaje de [**\_ \_ solicitud de WM DDE**](wm-dde-request.md) a una aplicación de servidor DDE para solicitar el valor de un elemento de datos. <br/>                                                                                                                                                                                                                                                              |
| [**\_finalización de WM DDE \_**](wm-dde-terminate.md) | Una aplicación DDE (cliente o servidor) envía un mensaje de [**\_ \_ finalización de WM DDE**](wm-dde-terminate.md) para finalizar una conversación. <br/>                                                                                                                                                                                                                                                                                  |
| [**\_DESaconsejar DDE de WM \_**](wm-dde-unadvise.md)   | Una aplicación cliente de DDE envía un mensaje de [**\_ \_ desaconsejar DDE de WM**](wm-dde-unadvise.md) para informar a una aplicación de servidor DDE de que el elemento especificado o un formato de Portapapeles determinado para el elemento ya no debe actualizarse. Esto finaliza el vínculo de datos activo o activo para el elemento especificado. <br/>                                                                                                                     |



 

### <a name="dde-structures"></a>Estructuras DDE



| Nombre                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack)       | Contiene las marcas de estado que una aplicación DDE pasa a su asociado como parte del mensaje de [**\_ \_ confirmación de DDE de WM**](wm-dde-ack.md) . Las marcas proporcionan detalles acerca de la respuesta de la aplicación a los mensajes [**WM \_ DDE \_ Data**](wm-dde-data.md), [**WM \_ DDE \_**](wm-dde-poke.md), la [**\_ \_ ejecución**](wm-dde-execute.md)de WM DDE y la [**\_ \_**](wm-dde-unadvise.md) [**\_ \_ solicitud**](wm-dde-request.md)de [**WM DDE. \_ \_**](wm-dde-advise.md) <br/> |
| [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) | Contiene marcas que especifican cómo una aplicación de servidor DDE debe enviar datos a una aplicación cliente durante un bucle de notificación. Un cliente pasa un identificador a una estructura [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) a un servidor como parte de un mensaje de [**\_ \_ notificación de DDE de WM**](wm-dde-advise.md) . <br/>                                                                                                                                                                                               |
| [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata)     | Contiene los datos e información sobre los datos que se envían como parte de un mensaje de [**\_ \_ datos de WM DDE**](wm-dde-data.md) . <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke)     | Contiene los datos e información sobre los datos que se envían como parte de un mensaje de mensajes de error de [**WM \_ DDE \_**](wm-dde-poke.md) . <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair)     | Contiene el nombre del servicio DDE y el nombre del tema. Una aplicación de servidor DDE puede utilizar esta estructura durante una transacción [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) para enumerar los pares de tema de servicio que admite. <br/>                                                                                                                                                                                                                                                   |



 

 

 





