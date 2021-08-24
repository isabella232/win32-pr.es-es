---
title: datos dinámicos Exchange
description: En esta sección se proporcionan instrucciones para implementar el intercambio dinámico de datos para aplicaciones que no pueden usar la biblioteca de administración de datos dinámicos Exchange (DDEML).
ms.assetid: vs|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchange.htm
keywords:
- datos dinámicos Exchange (DDE),about
- DDE (datos dinámicos Exchange),about
- intercambio de datos,datos dinámicos Exchange (DDE)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4db58f1027f0dfaacf28c4b2ec8d4208747929b0d40ca55d7d377831777f78a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678045"
---
# <a name="dynamic-data-exchange"></a>datos dinámicos Exchange

En esta sección se proporcionan instrucciones para implementar el intercambio dinámico de datos para aplicaciones que no pueden usar la biblioteca de administración de datos dinámicos Exchange (DDEML). Para obtener más información sobre DDEML, [vea datos dinámicos Exchange Management Library](dynamic-data-exchange-management-library.md).

### <a name="overviews"></a>Temas de introducción



| Nombre                                                           | Descripción                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------|
| [Acerca de datos dinámicos Exchange](about-dynamic-data-exchange.md) | Describe la transferencia de datos entre aplicaciones.<br/>       |
| [Uso de datos dinámicos Exchange](using-dynamic-data-exchange.md) | Proporciona ejemplos de código relacionados con el intercambio dinámico de datos.<br/> |
| [Referencia de DDE](dynamic-data-exchange-reference.md)           | Referencia de API.<br/>                                      |



 

### <a name="dde-functions"></a>Funciones DDE



| Nombre                                                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DdeSetQualityOfService**](/windows/desktop/api/Dde/nf-dde-ddesetqualityofservice)         | Especifica la calidad de servicio (QOS) que una aplicación de datos dinámicos Exchange sin procesar (DDE) desea para futuras conversaciones de DDE que inicia. La QOS especificada se aplica a las conversaciones iniciadas mientras esa configuración está en su lugar. La calidad de servicio de una conversación de DDE dura mientras dura la conversación. Las llamadas a [**la función DdeSetQualityOfService**](/windows/desktop/api/Dde/nf-dde-ddesetqualityofservice) durante una conversación no afectan a la QOS de esa conversación. <br/> |
| [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)                           | Libera la memoria especificada por el parámetro *lParam* de un mensaje DDE publicado. Una aplicación que recibe un mensaje DDE publicado debe llamar a esta función después de usar la función [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) para desempaquetar el *valor lParam.* <br/>                                                                                                                                                                                                     |
| [**ImpersonateDdeClientWindow**](/windows/desktop/api/Dde/nf-dde-impersonateddeclientwindow) | Permite que una aplicación de servidor DDE suplante el contexto de seguridad de una aplicación cliente DDE. Esto protege los datos de servidor seguros de clientes DDE no autorizados. <br/>                                                                                                                                                                                                                                                                                                      |
| [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)                           | Empaqueta un valor *LParam* de DDE en una estructura interna que se usa para compartir datos DDE entre procesos.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)                         | Permite que una aplicación reutilice un parámetro *LParam* de DDE empaquetado, en lugar de asignar un *nuevo lParam empaquetado.* El uso de esta función reduce las reasignaciones para las aplicaciones que pasan mensajes DDE empaquetados. <br/>                                                                                                                                                                                                                                                          |
| [**DesempaquetarDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)                       | Desempaqueta un valor *LParam* de DDE recibido de un mensaje DDE publicado. <br/>                                                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="dde-messages"></a>Mensajes DDE



| Nombre                                         | Descripción                                                                                                                                                                                                                                                                                      |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md) | Inicia una conversación con una aplicación de servidor que responde a los nombres de aplicación y tema especificados. Tras recibir este mensaje, se espera que todas las aplicaciones de servidor con nombres que coincidan con la aplicación especificada y que admitan el tema especificado la confirmen.<br/> |



 

### <a name="dde-notifications"></a>Notificaciones DDE



| Nombre                                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ DDE \_ ACK**](wm-dde-ack.md)             | Nnotifa una aplicación DDE de la recepción y el procesamiento de los mensajes siguientes: [**WM \_ DDE \_ WM WM,**](wm-dde-poke.md) [**WM \_ DDE \_ EXECUTE**](wm-dde-execute.md), WM DDE DATA , WM [**\_ \_ DDE**](wm-dde-data.md) [**\_ \_ ADVISE,**](wm-dde-advise.md) [**WM \_ DDE \_ UNADVISE,**](wm-dde-unadvise.md) [**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md)o [**WM \_ DDE \_ REQUEST**](wm-dde-request.md) (en algunos casos). <br/> |
| [**WM \_ DDE \_ ADVISE**](wm-dde-advise.md)       | Una aplicación cliente DDE envía el mensaje [**WM \_ DDE \_ ADVISE**](wm-dde-advise.md) a una aplicación de servidor DDE para solicitar al servidor que proporcione una actualización para un elemento de datos cada vez que cambia el elemento. <br/>                                                                                                                                                                                                              |
| [**WM \_ DDE \_ DATA**](wm-dde-data.md)           | Una aplicación de servidor DDE envía un mensaje [**WM \_ DDE \_ DATA**](wm-dde-data.md) a una aplicación cliente DDE para pasar un elemento de datos al cliente o para notificar al cliente la disponibilidad de un elemento de datos. <br/>                                                                                                                                                                                                           |
| [**WM \_ DDE \_ EXECUTE**](wm-dde-execute.md)     | Una aplicación cliente DDE envía un mensaje [**WM \_ DDE \_ EXECUTE**](wm-dde-execute.md) a una aplicación de servidor DDE para enviar una cadena al servidor que se va a procesar como una serie de comandos. Se espera que la aplicación de servidor publique un [**mensaje \_ wm DDE \_ ACK**](wm-dde-ack.md) en respuesta. <br/>                                                                                                                      |
| [**WM \_ DDE \_ POKE**](wm-dde-poke.md)           | Una aplicación cliente de DDE envía un mensaje [**\_ WM DDE \_ TFTPE**](wm-dde-poke.md) a una aplicación de servidor DDE. Un cliente usa este mensaje para solicitar al servidor que acepte un elemento de datos no solicitado. Se espera que el servidor responda con un mensaje [**\_ wm DDE \_ ACK**](wm-dde-ack.md) que indica si ha aceptado el elemento de datos. <br/>                                                                                   |
| [**SOLICITUD \_ DDE de WM \_**](wm-dde-request.md)     | Una aplicación cliente DDE envía un mensaje [**DE \_ SOLICITUD de DDE \_ WM**](wm-dde-request.md) a una aplicación de servidor DDE para solicitar el valor de un elemento de datos. <br/>                                                                                                                                                                                                                                                              |
| [**WM \_ DDE \_ TERMINATE**](wm-dde-terminate.md) | Una aplicación DDE (cliente o servidor) publica un mensaje [**WM \_ DDE \_ TERMINATE**](wm-dde-terminate.md) para finalizar una conversación. <br/>                                                                                                                                                                                                                                                                                  |
| [**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md)   | Una aplicación cliente DDE publica un mensaje [**\_ WM DDE \_ UNADVISE**](wm-dde-unadvise.md) para informar a una aplicación de servidor DDE de que el elemento especificado o un formato de Portapapeles determinado para el elemento ya no se deben actualizar. Esto finaliza el vínculo de datos en caliente o en caliente para el elemento especificado. <br/>                                                                                                                     |



 

### <a name="dde-structures"></a>Estructuras DDE



| Nombre                           | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack)       | Contiene marcas de estado que una aplicación DDE pasa a su asociado como parte del [**mensaje WM \_ DDE \_ ACK.**](wm-dde-ack.md) Las marcas proporcionan detalles sobre la respuesta de la aplicación a los mensajes [**WM \_ DDE \_ DATA**](wm-dde-data.md), [**WM \_ \_ DDEDVE,**](wm-dde-poke.md) [**WM \_ DDE \_ EXECUTE,**](wm-dde-execute.md) [**WM \_ DDE \_ ADVISE,**](wm-dde-advise.md) [**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md)y [**WM \_ DDE \_ REQUEST**](wm-dde-request.md). <br/> |
| [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) | Contiene marcas que especifican cómo una aplicación de servidor DDE debe enviar datos a una aplicación cliente durante un bucle de asesoramiento. Un cliente pasa un identificador a una [**estructura DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) a un servidor como parte de un [**mensaje \_ DDE ADVISE \_ de WM.**](wm-dde-advise.md) <br/>                                                                                                                                                                                               |
| [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata)     | Contiene los datos e información sobre los datos enviados como parte de un [**mensaje WM \_ DDE \_ DATA.**](wm-dde-data.md) <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke)     | Contiene los datos, y la información sobre los datos, enviados como parte de un [**mensaje \_ WM DDE \_ WM.**](wm-dde-poke.md) <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair)     | Contiene un nombre de servicio DDE y un nombre de tema. Una aplicación de servidor DDE puede usar esta estructura durante una transacción [**\_ XTYP WILDCONNECT**](xtyp-wildconnect.md) para enumerar los pares de servicio-tema que admite. <br/>                                                                                                                                                                                                                                                   |



 

 

 





